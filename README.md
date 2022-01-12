# PeerToPeerVideo
Creates a WebRTC PeerConnection and shares video between two peers without a signalling server 

Please modify index.html to accomplish the following:
1. Add an audio track to the video stream

- add the audio member in line 39
- update the offerOptions in line 41

2. Create a video stream of the local screen using getDisplayMedia

- Using `getDisplayMedia` to get the screen media from lines 90 - 100

3. Add a video element, alongside the local video, that displays the screen

- Add more video elements for local and remote screen in lines 17 and 19
- Get HTML elements for screen media in lines 48 and 49

4. Add the shared screen video track to the peer media stream

- add remote video track and add audio and video in `gotRemoteMediaStream` (lines 127 - 133)

5. When a remote connection is made, display the remote shared screen alongside the remote video

- Set the `muted` to be true and avoid echo when the connection is made in lines 81 and 94
- Open the `index.html` in two adjacent windows
- Using the clipboard(copy / paste) to transfer the connection information betwen local and remote sides

The final index.html should have 2 video elements displaying the local camera and local screen, and two video elements displaying the remote video and remote screen.
The peers should be able to see each other's cameras, screens and to speak with each other.


## Reference 

- <https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia>
- <https://developer.mozilla.org/en-US/docs/Web/API/RTCPeerConnection>
- <https://mac-blog.org.ua/webrtc-one-to-one-without-signaling-server>