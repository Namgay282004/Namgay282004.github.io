---
Title:  WEB FinalJournal
categories: [WEB101, WEB102 FinalJournal]
tags: [WEB101, WEB102]
---
# Final Practical Assignment Report: Instagram Clone Chat Application

## Introduction

This report describes my experience developing the chat feature for an Instagram clone as part of a full-stack web application project. I focused on the frontend, working on the user interface and basic message-sending functionality. Despite facing several challenges, I learned a lot throughout the process.

## Development Process
### Front-End Development
To begin, I set up the frontend environment using React. I chose Create React App because it simplifies the setup process. I installed libraries like React Router for navigation and Chakra UI for styling. Chakra UI was especially useful for creating a consistent and attractive design.

I built key components: **ChatList** for displaying recent chats, **ChatWindow** for showing messages in a selected chat, and **MessageInput** for sending new messages. Chakra UI helped ensure these components looked good and worked well together. I managed state using React's useState and useEffect hooks to handle updates and changes efficiently.

### Basic Functionality Implementation
I implemented basic functionality that allows users to send text messages. Unfortunately, I couldn't include voice messages due to time constraints. Handling message sending involved updating the chat window dynamically whenever a new message was sent.

## Challenges Faced
### WebSocket Integration
One major challenge was integrating WebSocket for real-time messaging. We struggled with issues like messages not being delivered in real-time, inconsistent connection states, and difficulties managing multiple user connections. Messages were often delayed, out of order, or missing. To address this, we needed better error handling for connection drops, a connection manager for handling multiple WebSocket connections, and tools like Postman and debugging logs to identify and fix issues.


### Voice Message Implementation
I referred to the React Recorder documentation to implement voice messaging. I managed to get the voice recording feature working, allowing users to record and stop recordings. Additionally, I was able to send voice messages. However, I encountered an issue where previously sent voice messages couldn't be played back. This was a main issue, as the functionality to listen to voice messages is crucial for a chat application.

## Back-End Development
Although we focused mainly on the frontend, we also began setting up the backend using Hono, Socket.IO, and SQLite. We created a simple Hono server connected to a SQLite database, using raw SQL queries for database interaction and Socket.IO for real-time communication. The backend aimed to provide secure authentication and efficient real-time communication.

## Lessons  I Learned 
During the project to create a chat feature for an Instagram clone, I focused on building the part of the app that users see and interact with (frontend) using React and Chakra UI. I learned how to manage messages and display them in real-time, which was challenging because messages sometimes arrived late or didn't show up right away. I also tried adding voice messages, but getting them to work reliably across different browsers was tricky. On the backend (the part of the app users don't see), I started setting up a system to store messages using SQLite and manage real-time updates using Socket.IO. This project taught me that building web apps involves lots of planning, learning, and testing to solve problems and create a smooth experience for users.

## References

- [Prisma](https://www.prisma.io/docs/getting-started)
- [react-audio-voice-recorder](https://www.npmjs.com/package/react-audio-voice-recorder)
- [Websocket](https://hackernoon.com/building-a-real-time-chat-application-with-websocket)
