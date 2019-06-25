###Document
A generic term describing base level entity describing media content. This not only covers posts, but signatures, avatar areas in posts, etc.

###Post
is-a document.

###Thread 
is-a document. A collection of posts displayed from earliest to latest date created.

###Board
is-a document. A collection of threads displayed from earliest to latest date created.

###Category 
is-a document. A collection of boards (e.g. *Public boards* is where the Recruitment Board will live, *Private* is where boards only accessible to guild members will live, etc.)

###Forum Hierarchy
Denotes the Board, Thread, and Post documents and the parent to child relationship of that order.

###User
A clump on data associated with a human being.

###User Access Level
An integer that defines the default ability to access and interact with documents and other forum features.

###Document Access Level
An integer that defines the default user access level needed to view/interact with said document.

###Permission
A boolean denoting the ability of a user to access/interact with specific documents which overrides the user access level.

###Role
A set of default permissions and/or user access levels.