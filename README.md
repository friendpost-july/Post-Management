**POST Management**
This repository is for the Post service of the FriendPost Application

## C4 Context Diagram

```mermaid
C4Context
title "Post management Application diagram"

System(postmanagement,"Post Management","")
System(timeline,"Timeline")
System(auth,"Authentication")

Rel(timeline,postmanagement,"Get list of posts")
Rel(auth,postmanagement,"Create a post")

UpdateLayoutConfig("2","1")
```

## Tech Stack

The Posts Service will be implemented using the MERN stack.

## C4 Container Diagram

```mermaid
C4Container
title FriendPost Application Posts Service

Container_Boundary(userservice, "User Management") {
    Container(nodeapp, "Posts API Node App","node.js")
    ContainerDb(usersdb, "Posts Service Database", "MongoDB")
}

Container_Ext(webapp,"Web Application")
Container_Ext(friendsservice,"Friends Service")
Container_Ext(timelineservice,"Timeline Service")

Rel(webapp, nodeapp, "Adds new post, edits post")
Rel(timelineservice, nodeapp,"Gets Post data as required")
Rel(friendsservice, nodeapp,"Gets Post data as required")

UpdateRelStyle(webapp, nodeapp, $offsetY="-40")
UpdateRelStyle(timelineservice, nodeapp,$offsetY="-40")
UpdateRelStyle(friendsservice, nodeapp,$offsetY="-40")
```
