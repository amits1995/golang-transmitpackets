### Goal
the goal is to be able to send more than one udp packet in one syscall.  
This should improve performance for some networking applications that use UDP.  
There is a large overhead when calling ``UdpConn.Write`` for each udp packet.  
Using the ``TransmitPackets`` in windows should help solve that overhead.
