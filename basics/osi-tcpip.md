# OSI and TCP/IP

## OSI
The Osi, a standard model to demo the theory behind computer networking. TCP/IP model, is the actual real-world model. 
7 layers f the OSI model: 

![OSI](pictures/OSI-Table.png "OSI: APSTNDP")

### Layer 7 -- Application
Networking options to programs running on a computer, **providing an interface**. 
When data is given to the Application layer, it is passed down into the Presentation layer.

### Layer 6 -- Presentation
Receives data from Application layer, the data teends to be in a format the application understands,  which is not necessarily in the standardised format that could be understood but the application layer on the receiving computer. 
Presentation layer **translates the data into a standardised format**, handling any encryption, compression or other data transformations. Data is passed down to the Session layer.

### Layer 5 -- Session
Receives correctly formatted data from the Presentation layer. **It looks to make a connection with the computer across the network**. If it cannot, an error is sent back, and the process goes no further. If a session can be estabilished, then **it is the Session layer's job to maintain, cooperate with the remote computer's Session layer**. When connection is successfuly logged, the data is passed down to the Transport layer. 

### Layer 4 -- Transport
First purpose is to choose the protocol over which the data is to be transmitted. 
 - 2 most common protocols: 
   + TCP(=Transmission Control Protocol)
   + UDP(=User Datagram Protocol)
A TCP connection allows the two computers to remain in constant communication to ensure that the data is sent at an acceptable speed, and that any lost data is re-sent. With UDP, the opposite is true; packets of data are essentially thrown at the receiving computer -- if it can't keep up then that's its problem (this is why a video transmission over something like Skype can be pixelated if the connection is bad). What this means is that TCP would usually be chosen for situations where accuracy is favoured over speed (e.g. file transfer, or loading a webpage), and UDP would be used in situations where speed is more important (e.g. video streaming).

**With a protocol selected, the transport layer then divides the transmission up into bite-sized pieces** (over TCP these are called **segments**, over UDP they're called **datagrams**), which makes it easier to transmit the message successfully. 

 - packet segmentation = process of dividing a data packet into smaller units for transmission over the network
 - datagram = independent entity of data carrying sufficient info to be routed from the source to destination without relience on early exchanges

