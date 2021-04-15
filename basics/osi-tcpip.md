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
 - 2 most common: 
   + TCP(=Transmission Control Protocol)
   + UDP(=User Datagram Protocol)
