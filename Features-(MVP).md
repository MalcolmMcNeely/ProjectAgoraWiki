#Basic Forum Requirements
**Posts:** Create, Edit, Delete, Move, Lock
**Threads:** Create, Edit, Delete, Move, Lock, Sticky, Announcement
**Boards:** Create, Edit, Delete, Move
**Categories:** Create, Edit, Delete
* Threads and Posts require pagination navigation. While not a difficult obstacle, Azure Table queries [return a maximum of 1000 results](https://docs.microsoft.com/en-us/rest/api/storageservices/query-timeout-and-pagination) at any one time.
* Re: limits, an Azure Table Storage row [cannot exceed 1MB](https://docs.microsoft.com/en-us/rest/api/storageservices/understanding-the-table-service-data-model) and so we will need to use Blob Storage for large pieces of data.

##Permissions
* The Forum Hierarchy will have assignable Access Levels 
* By default, Forum Hierarchy access levels will inherit from the parent i.e. Threads will inherit from Boards
* Some boards (Access Level 0) may not require an account to sign up, however there does need to be some human detection going on to prevent spam posts.

##User Profile
**Characters:** TBD pending BNet integration
**Profile Names:** TBD - if using BNet authentication then users can set a character as their 'main' character from which the profile name will inherit
**Rank:** Guild Rank, Editable by permission or with Bnet integration
**Signatures:** Create, Edit, Delete
**Avatars:** Edit
* It is required to have special guild accounts that do not require Bnet integration. For example, old members who want to interact with the Board concerning the annual real life guildmeet.

#Raid Calendar
A permission based event organisation tool where users can sign up with one of their characters

