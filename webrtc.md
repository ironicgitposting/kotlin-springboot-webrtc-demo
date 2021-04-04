# Guide to WebRTC

## Rationale
When two browsers need to communicate => Typically there is a server in the middle.
- Server in the middle = Delay

WebRTC = communication without a server in the middle.

For client discovering, WebRTC uses a mechanism called signaling.

## Signaling

Signaling refers to the processes involved in network discovery, creation of a session, managing the session, and exchanging the media-capability metadata.

This is essential as the clients need to know each other up front to initiate the communication.

To achieve all these, WebRTC does not specify a standard for signaling and leaves it to the developer’s implementation. So, this provides us the flexibility to use WebRTC on a range of devices with any technology and supporting protocol.

## Building the signaling server

Put in Pom.xml the websocket library

[Get from MavenCentral](https://search.maven.org/search?q=g:org.springframework.boot%20AND%20a:spring-boot-starter-websocket)
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-websocket</artifactId>
    <version>x.x.x</version>
</dependency>
```
The implementation is simple:
- Create an endpoint that a client application can use to register as a websocket connection.




