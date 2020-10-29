# Proposals

## Problem
For many types of applications, we need to support notification system, such as notify user for renew subscriptions, notifiy user when someone sent a message,
or even some promotional messages. We need to store it, send the notification via email, sms or web push notification. It seems there is no one open source
system/service to do this whole stuffs, so we want to build something which can do all this stuffs. Developer can integrate this service to their own ecosystem
and then no need to worry about this feature.

## Features
1. Multiple channel support (User can subscribe to multiple channel, will get notification from those channels).
2. Persistence (All the notifications should be persisted).
3. Notification medium can be Email, SMS, Webhook, Websocket, GCM, Web push notification.
4. Real time notification (Notification should be sent in real time, specially for web push or websocket one).
5. Plug and play mechanism, other developer can add plugins if they need special customization. As we will support basic API integration for email, but
people might add mailgun integrations with a plugin.


## Tech Stack
1. NodeJS with Typescript
2. Socket.io or other websocket implementations
3. PostgresSQL or Cassandra
4. Docker


## System Requirements
1. Should be scalable by design
2. Should be designed to handle huge amount of load, notifications, subscribers
3. Should have resiliency.
4. Should be designed to support deployment on Kubernetes. 
