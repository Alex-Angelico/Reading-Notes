# Class 3: Revisions to the Cloud

## Principles of Version Control
In brief, version control is a cpncept that allows software developers--or creators of any kind, in theory--catalog and revisit a history of iterative versions of a given file. This allows modifications to be tracked and compared, and reverted if necessary. The standard approach to version control has evolved over the years, per the sequence below:  

    1. **Local Version Control**  
       Consists of a single database on a local storage drive that stores file changes.  
    2. **Centralized Version Control**  
       An advent of growing collaboration between developer teams, centralized version control takes the form of a single server tracking and storing file changes, which is accessible by client machines used by team members. This allowed for better administration of team resources and oversight of project development.  
    3. **Distributed Version Control**  
       Preserves all the advances of centralized version control while resolving its major weakness--server hardware failure, which would result in the loss of all project work not stored on client machines. Distributed version control creates mirrored repositories of a team's total contribution on each client machine, allowing for far greater flexibility in operations and collaboration.  

## Git
Git is a distributed version control system developed in the mid-2000s on the Linux platform. It has since become one of the one widely-used version control systems in the world due to its ease of use for localized operations even while offline, modification tracking, and redundant data storage.

## Setting Up a Git Repository
This process is also very easily completed through terminal. All that is neccessary is to navigate to the desired directory for storing the repository, and then using the 'git clone "repository URL"' command to download the repository from a cloud service such as GitHub. Then a developer can begin modifying files in the repository.

The process of modifying a file, staging the changes for upload to distributed client repositories, and committing and pushing those changes is simple and requires only a few commands in a terminal instance collective known as ACP:
    1. Add (git add)
    2. Commit (git commit -m "developer message documenting changes made")
    3. Push (git push origin master)

Additionally, the command 'git status' can be used at any point in the ACP flow to ensure no anomalies are being encountered.