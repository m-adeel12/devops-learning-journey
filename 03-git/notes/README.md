# Git

What is Git ?
- Git isnt something that just stores code, in fact it is the foundation of how modern teams collaborate, build, test, ship and even recover from when an engineer breaks a production at lets say 2 am. 

## Version Control

- Something that seems simple however is essential for any DevOps/Engineering workflow.
  1. It tracks changes to code over time
  2. Lets you undo, inspect and collaborate
  3. Its like a time machine where you can review previous codes. 





## Centralised (SVN) vs Distributed (VCS)

- Centralised server is where everyone back then would work off, suppose if the server went down it was game over , you couldnt commit, update or work. It would lead to a merge of conflicts. 
- Then came 2005 where Linus Toravlds lost access to an important tool called bitkeeper, Linus being Linus came up with an idea why not write my own verison control, a few years later Git was born. 
- Git changed everything, instead of relying on one server, every developer like myself  has a fully copy of the repo. 


<img width="488" height="254" alt="image" src="https://github.com/user-attachments/assets/9a006295-b0e7-4c97-9332-19cd34c4c8d8" />


## Git Architecture and Internals 

Git is not a File Tracker !

- In fact what Git tracks is snapshots, eveytime you do a commit  or a change, Git takes a snapshot  not of the line you just changed but the whole file. For example, if you was to change one line it would save that verison of the file efficently. 
- Git uses a key value store called SHA-1 hash which are long files of string that uniquely represent the contents of your file. So no two different blobs or file contents would have the same hash.

- In simple words, its not just a tracker its a smart,compress hash-based snapshot engine.

<img width="480" height="241" alt="image" src="https://github.com/user-attachments/assets/e94d3839-9bde-4777-8ac3-2cbb15766b41" />


## Git Terminology and Key Concepts 

- Repository: A git project with all your files stored
- Commit: A snapshot of your files and metadata (author,timestamp,message etc)
- 



