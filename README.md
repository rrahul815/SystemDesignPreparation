# SystemDesignPreparation
Preparation for System Design

This documents the journey of System Design Interview Preparation

# Fundamentals of System Design
How to approach a system design interview? What are the steps involved in a system design?
interviewing.io is a great resource for System Design preparation. This site proposes a 3 step formula to approach any system design from first principles even if we do not know anything about the system we need to design.


# Components of a System
Networking components

Gateway

Loadbalancer

DNS

CDN

Communication Protocols

Communcation protocols can be broadly divided into Synchronous and Asynchronous communication. In synchronous, the client waits for a response from the server. In asynchronous communication, the client sends a request to the server and does not wait for a response. The response can be received by the client in a variety of ways depending on the use case.
The network components have multiple layers which are based on the OSI model, with the physical layer on the bottom and the application layer on the top. There are 7 layers, 1. physical layer, 2.data link layer 3. network layer 4. transport layer 5. session layer 6. presentation layer 7. application layer

HTTP
HTTP stands for HyperText Transfer Protocol. There are multiple HTTP protocol versions. HTTP started with 0.9 and subsequent releases of 1.0 and 1.1. HTTP 1.1 is the most widely used protocol currently in 2025. The initial version 0.9 only had one method GET, 1.0 and 1.1 added more methods. The most common ones are POST, DELETE, PUT. There are others like PATCH, HEAD, CONNECT, TRACE and OPTIONS. HTTP 2.0 was released in 2015, having certain additional features on top of 1.1. They are primarily a) request multiplexing and prioritization b) automatic compression c) connection reset d) server push. HTTP 3.0 is an internet draft proposed in 2020. This version changes the underlying Transport layer from TCP to QUIC (Quick UDP Internet Connections). There will be no HTTPS/HTTP separation, but all connections will be encrypted by default.

REST
REST protocol is implemented on top of HTTP and uses the existing methods of HTTP.

WebSockets

gRPC

WebRTC

HTTP-DASH

SignalR


Storage components

Cache

Database

Queueing system

Algorithms and Techniques

Compression

Leader election

Conflict resolution


# Designing a System

## Designing YouTube
YouTube is a video upload and streaming viewing platform. It also has additional features to download and play the video locally. Each video has a description by the content creator and other users have ability to comment, reply to a comment, like. There is a stats section like videos, subscribers.

### Functional requirements
1. User should be able to upload a video
2. User should be able to play video on multiple devices. Start on one and continue on another
3. Comment on a video and reply

### Non-functional requirements
There should be minimal buffering of the video\
Scalable\
Available

### Out of scope
Likes on a video, and download

### Estimates

### Data

### API

### High level design
![High level diagram of YouTube](/diagrams/png/youtube_github.excalidraw.png)

## Designing Slack
What is Slack? Slack started as a simple communication tool at work, but has evolved into an integrated Work environment for collaboration. Website url: slack.com

### Functional Requirements
Send messages, files to other users
Create channels to communicate as a group


### Non-functional Requirements
Scalable
Fault tolerant
Low latency to receive messages
consistency in the order of messages

### Out of scope
Integrating AI and third party tools and applications

### Estimates
Support milions of users and send and receive messages.
Store those messages, in case the user is offline.

### Data
The main entites will be users,channels,messages

### API
API will be primarily used to sign up and authenticate a user. For bidirectional communication between users, API would not work.
API to create user and login will be discussed in detail in other sections.

### High level design
The high level design involves, a user A sending a message to user B and receiving a response back. This message needs to be stored incase the user is not online to receive it.

![High level diagram of Slack](/diagrams/png/slack_github.excalidraw.png)

# Document Links:
