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

HTTP

REST

WebSockets

gRPC

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



# Document Links:
