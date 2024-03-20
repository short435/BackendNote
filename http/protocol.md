# Protocol

## TCP/IP

- Require established connection before transmitting data
- Sequnce for the data sending
- Retrasimit data if losting.
- End-to-end connection, not able to do multiple boardcast


### How TCP/IP work

**3-way handshake**

1. Ack message from client to server **[synchronization]**
2. Syn-Ack message from server to client **[synchronization acknowledgment]**
3. Syn message from client to server **[final acknowledgment]**
4. Connecting!


**Error Control**

- Checksum
Example: 
Send [1 ,2 ,3 ,20 ,13] Sum of the array is 39 Than send 9 to client to check the completeness of the data.
==P.S UDP also do checksum but not necessory==

- Acknowledgment
Acknowledgment Number:
There would include sequence number in the header. Client would tell server the received squence number.
- Retransmission
Retransmission Timeout, RTO
Fast Retransmit

## UDP

- Not required for connection.
- Can't retransimit, no promise for the completeness of data
- Faster and efficient ,but risk for the uncomplete data send
- No fixed order
- Multiple boardcast


## Websocket

## WebRTC

## Reference

- [TCP error control](https://notfalse.net/27/tcp-error-control)
- [WebRTC vs TCP/IP](https://www.linkedin.com/pulse/webrtc-vs-websocket-which-one-choose-your-web-mikhail-garber/)
- [TCP vs UDP](https://www.spiceworks.com/tech/networking/articles/tcp-vs-udp/)