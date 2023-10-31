Web RTC

WebRTC (Web Real-Time Communication) is an open-source project that enables real-time communication capabilities in web browsers and mobile applications. It allows peer-to-peer communication, including audio and video streaming, as well as data sharing, without the need for plugins or additional software installations.

WebRTC uses a combination of JavaScript APIs and protocols, such as the Session Description Protocol (SDP) and the Interactive Connectivity Establishment (ICE), to establish and maintain direct connections between devices. This technology has various applications, including video conferencing, live streaming, file sharing, and online gaming.

One of the key advantages of WebRTC is its ease of use and compatibility. It is supported by major web browsers, including Chrome, Firefox, Safari, and Edge, making it accessible to a wide range of users. Additionally, WebRTC provides secure communication through encryption and authentication mechanisms, ensuring the privacy and integrity of the transmitted data.

Overall, WebRTC has revolutionized real-time communication on the web, enabling seamless and immersive experiences for users across different platforms and devices.

WebRTC is a set of JS API’s that allow us to establish peer to peer connection between two browsers to exchange data such as audio and video in real time .

It is not like WebSockets becouse in websockets it is done with real time communication through server where as in WebRTC it is done without data going to server.

Web RTC transports it’s data over UDP and  UDP is fast.

**LIMITATIONS of WebRTC**

- UDP is not a reliable protocol  for transferring important data.
- no built in signaling.

**So what exactly is sent between the two clients and how is it sent ?**

- SDP
    
    A session Description Protocol , is an object containing information about the session connection such as the codec, address , media type. audio and video and so on
    
- ICE Candidates
    
    An ICR candidate is a public IP address and  port that could potentially be an address that receives data
    

**The way it works is :**

The client 1 will send the sdp to the server and the server send it to the client 2 then client 2 will do the same now the two are connected.

The each client has each stunt server where the each client asks for there public IP.

Once the path  is found by them then they will start communicsting to each othere without the database or the data never goes to the server.

We use Trickling ICE Candidates trick

Pess the blow to view a simple app to demonstrate how two peers exchange SDP offer and SDP Answer WITHOUT signaling.

**[WebRTC-Simple-SDP-Handshake-Demo](https://divanov11.github.io/WebRTC-Simple-SDP-Handshake-Demo/)**
