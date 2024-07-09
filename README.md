**POST Management**

PostManagementservice
This repository is for the Post service of the FriendPost Application

```mermaid
C4Context
title "Post management Application diagram"

System(postmanagement,"Post Management","")
System(timeline,"Timerline")
System(auth,"Authentication")

Rel(timeline,postmanagement,"Get list of posts")
Rel(auth,postmanagement,"Create a post")

UpdateLayoutConfig("2","1")
```
