# Reading 13: Local Storage

## The Past, Present, and Future of Local Storage for Web Applications

Web-based applications have historically been very restricted in terms of local storage options when compared to native applications. The main solution for the web application has been cookies, which were invented early in the web's history. However, cookies have major weaknesses.

- Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over.
- Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL).
- Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful.

Fortunately, the advent of HTML5 has made it possible to access lots of client-based storage space that persists beyond a page refresh, and isn't transmitted to a server. More specifically, HTML5 has succeeded in providing a standardized API for storage access, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins. This specification is named Web Storage (though it is alternatively referred to as Local Storage or DOM Storage).

From JavaScript code, HTML5 Storage is accessed through the localStorage object on the global window object.

### Checking for HTML5 Storage Compatibility

function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}
Instead of writing this function yourself, you can use Modernizr to detect support for HTML5 Storage.

if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}

### Using HTML5 Storage

HTML5 Storage is based on named key/value pairs. The named key is a string, and the data can be any type supported by JavaScript (e.g. strings, Booleans, integers, or floats). However, the data is actually stored as a string. If a program is storing and retrieving anything other than strings, it will need to use functions like parseInt() or parseFloat() to coerce retrieved data into the expected JavaScript datatype.

interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};

Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.

Like other JavaScript objects, a localStorage object can be treated as an associative array. Instead of using the getItem() and setItem() methods, all that is needed are square brackets, per below:

var foo = localStorage["bar"];
// ...
localStorage["bar"] = foo;

There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).

interface Storage {
  deleter void removeItem(in DOMString key);
  void clear();
};

Calling removeItem() with a non-existent key will do nothing.

Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).

interface Storage {
  readonly attribute unsigned long length;
  getter DOMString key(in unsigned long index);
};

When a function calls key() with an index that is not between 0–(length-1), the function will return null.

#### Tracking Changes to the HTML5 Storage Area

To programmatically keep track of when the storage area changes, JavaScript can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something. For example, if an item is set to its existing value or call clear() when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.

function handle_storage(e) {
  if (!e) { e = window.event; }
}

##### StorageEvent Object

Property | Type | Description
-------- | ---- | ------------
key | string | the named key that was added, removed, or modified
oldValue | any | the previous value (now overwritten), or null if a new item was added
newValue | any | the new value, or null if an item was removed
url | string | the page which called a method that triggered this change

The storage event is not cancelable. From within the handle_storage callback function, there is no way to stop the change from occurring.
