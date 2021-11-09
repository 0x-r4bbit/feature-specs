---
title: "Mutual Contact Requests spec"
description: ""
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  raw:
    parent: "chat"
weight: 100
toc: true
---

# Mutual Contact Requests

## Designs

* [designs](https://www.figma.com/file/Mr3rqxxgKJ2zMQ06UAKiWL/%F0%9F%92%AC-Chat%E2%8E%9CDesktop?node-id=5224%3A0)

## Use Cases

TODO

## Functional Requirements

User A wants to chat with User B and so adds User B as a contact, User B receives a contact request with a message and can either accept or reject. User A can only chat with User B if User B accepts the contact request.

### User A that sends contact request
- User A CANNOT send messages to User B if User B has not accepted the contact request
- User A MAY send a contact request to User B containing a message
- If User A has sent a contact request they MUST see that the contact request is pending and the message they have sent
- If User A has sent a contact request they MUST be able to cancel the contact request

### User B that receives contact request
- A User CANNOT receive messages from users that are not in their contact list
- A User MAY receive contact requests from users that are not in their contact list
- A User CANNOT receive contact requests from users that are already in their contact list
- If a User has pending contact requests the contact requests section MUST be displayed
- If a User has no pending contact requests the contact requests section MUST NOT be displayed
- If a User receives a contact request the counter of message requests MUST increase

### Contact Requests Section
- A User MAY Decline ALL pending contact requests
- A User MAY Accept ALL pending contact requests
- The user MUST be able to accept a contact request directly
- The user MUST be able to decline & block a contact request directly in this type of activity item
- Clicking the context menu of a contact request item MUST show 2 options: "view profile" and "Decline and Block"
- If a contact request item is rejected it MUST disapear from the UI
- If a contact request item is accepted it MUST disapear from the UI
- Clicking on this type of activity item MUST open that chat and jump to that message
