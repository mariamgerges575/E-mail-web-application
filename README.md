# E-mail-web-application
Designed object-oriented model was used with some design pattern to create mail service web application with the basic functionalities using angular for frontend and java with spring boot framework for backend

##### the basic functionalities include:
- Composing and Drafts. 
- Default folders:
  - Inbox (default, priority)
  - Sent
  - Trash: auto delete emails after 30 days
  - Drafts
- Any additional folder that user can create and move messages to it.
- User Folders (Adding, Deleting).
- Filters according to:
  - subject or sender.
  - Subject only in sent folder.
  - both categories.
  - multiple elements in the same category
- Searching:
  - Date
  - Sender
  - Receivers
  - Subject
  - Body
  - Attachments
- Sorting:
  - Date
  - Sender
  - Receivers
  - Importance
  - Subject
  - Body
  - Attachments
- Attachment:
  - Sending multiple attachments.
  - Any type of attachments
  - View
  - delete
- contacts:
  - adding, deleting
  - a contact can have multiple emails with one set default
  - searching and Sorting
- selecting multiple emails to
  - move
  - mark as read
  - delete
 ## UML Class Diagram:
 ![mail](https://user-images.githubusercontent.com/96488115/218330960-6af9d26b-60f1-4b50-9aff-5593bedd37a2.png)

## Design Patterns Used:
##### 1. Proxy design pattern:
  used to control access database class, allowing to 
perform something either before or after the request gets through to it (e.g., 
verifying password or making sure that the receiver’s email is an actual existing 
email).
##### 2. Singleton design pattern:
  used to make sure that the database class has only one instance to 
  provide a global access point to this instance.
##### 3. Filter design pattern:
  used simply to implement filter feat.
##### 4. Builder design pattern:
  used to build an object of type user with a different 
  number of attributes.
##### 5. State design pattern:
  We implemented the state design pattern to handle the different states of the user’s 
  opened folder. Since the behavior of each folder is different from the other. For 
  example, you can’t sort by sender in the “sent” folder while you can do that in the 
  “inbox” folder. Moreover, the list of summarized that appears when you request a 
  certain folder should contain the receiver’s username in case of “sent” folder and the 
  sender’s username in case of “inbox” folder.
##### 6. Mediator design pattern:
  the Mediator DP to reduce dependencies between objects and restricts 
  direct communications between these objects and forces them to collaborate only 
  via a mediator object.
##### 7. Flyweight design pattern:
  this design pattern to avoid destroying unused objects
  (Objects of type users who have logged out) which is hard, also leaving them will 
  waste a lot of storage, so we used this design pattern to reuse already existing objects 
  instead of creating new ones.
##### 8. Prototype Design Pattern
  this DP allows to make clone of mail objects so that each can be edited before saving them to database (e.g. message with multiple receivers should appear to each receiver with only one receiver which is his name). 

