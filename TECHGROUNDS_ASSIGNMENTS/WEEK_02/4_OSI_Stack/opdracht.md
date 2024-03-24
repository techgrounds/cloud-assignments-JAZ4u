# [4- OSI Stack]

[Geef een korte beschrijving van het onderwerp]

## Key-terms

- OSI Model  
- TCP/IP Model

## Opdracht

 Study:

- 1] A/ The OSI model and B/ its uses.
- 2] A/ The TCP/IP model and B/ its uses.

### Gebruikte bronnen

- https://www.youtube.com/watch?v=Ilk7UXzV_Qc
- CHAT GPT

### Ervaren problemen

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Resultaat

1]The OSI MODEL

Study:
- A/ The OSI model, 
- B/ and its uses.

<u>A/ The OSI model:</u>
The OSI (Open Systems Interconnection) model is a conceptual framework used to understand and standardize the functions of a telecommunication or computing system. Developed by the International Organization for Standardization (ISO) in the 1980s, it provides a structured approach to network communication by dividing the process into layers. Each layer has specific functions and interacts with adjacent layers to facilitate communication between devices. The OSI model consists of seven layers:

1. **Physical Layer**: This layer deals with the physical transmission of data over the network medium. It defines characteristics such as voltage levels, cable types, and data rates. Examples of devices operating at this layer include network interface cards (NICs) and hubs.

2. **Data Link Layer**: The data link layer is responsible for error detection and correction, as well as organizing data into frames for transmission. It ensures reliable point-to-point communication over the physical layer. Devices such as switches and bridges operate at this layer.

3. **Network Layer**: The network layer is concerned with addressing, routing, and forwarding data packets across multiple networks. It establishes logical connections between devices and determines the optimal path for data transmission. The most well-known protocol at this layer is the Internet Protocol (IP).

4. **Transport Layer**: This layer ensures end-to-end communication between hosts and is responsible for segmenting, reassembling, and error-checking data. It provides mechanisms for flow control and reliability. Protocols like TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) operate at this layer.

5. **Session Layer**: The session layer manages communication sessions between devices, including establishment, maintenance, and termination of connections. It facilitates dialogue control and synchronization between applications. Examples of session layer protocols include NetBIOS and RPC (Remote Procedure Call).

6. **Presentation Layer**: The presentation layer is responsible for data translation, encryption, and compression to ensure compatibility between different systems. It handles data formatting and syntax conversion, allowing applications to exchange information seamlessly. Examples of presentation layer formats include JPEG, MPEG, and ASCII.

7. **Application Layer**: The application layer provides network services directly to end-users and applications. It enables functions such as file transfer, email, and remote login. Protocols like HTTP (Hypertext Transfer Protocol), SMTP (Simple Mail Transfer Protocol), and FTP (File Transfer Protocol) operate at this layer.
   


<u>B/ Uses of the OSI model:</u>

1. **Standardization**: The OSI model provides a standardized framework for designing, implementing, and troubleshooting network communication protocols and systems.

2. **Interoperability**: It enables different types of computers and networks to communicate with each other, facilitating interoperability across diverse hardware and software platforms.

3. **Educational Tool**: The OSI model serves as an educational tool for understanding network communication concepts and the interactions between different layers.

4. **Basis for Protocols**: The OSI model provides a basis for the development and implementation of network protocols, guiding the design process and ensuring compatibility between different systems.
   
   Overall, the OSI model is a fundamental concept in networking, providing a structured approach to understanding and implementing network communication protocols and systems.


2]The TCP/IP MODEL

Study:
- A/ The TCP/IP model,
- B/ and its uses.

A/ The TCP/IP model

The TCP/IP (Transmission Control Protocol/Internet Protocol) model is a conceptual framework used for understanding how data is transmitted over networks, particularly the internet. It's organized into layers, each responsible for specific functions related to communication. The TCP/IP model is often compared to the OSI (Open Systems Interconnection) model, but it's simpler and more closely aligned with the architecture of the internet.

- The TCP/IP model consists of four layers:
  
  1. **Application Layer**: This layer interacts directly with end-users and application software. It provides network services to applications, including protocols like HTTP (Hypertext Transfer Protocol), FTP (File Transfer Protocol), SMTP (Simple Mail Transfer Protocol), and DNS (Domain Name System). This layer deals with high-level protocols and data formats.
  
  2. **Transport Layer**: The transport layer ensures end-to-end communication between hosts. It's responsible for segmenting data from the application layer into smaller packets for transmission and ensuring their reliable delivery. The main protocols used in this layer are TCP (Transmission Control Protocol) and UDP (User Datagram Protocol).
  
  3. **Internet Layer (also known as the Network Layer)**: This layer handles the addressing, routing, and packaging of data packets for transmission across networks. It's where the IP (Internet Protocol) resides, which is responsible for addressing and routing packets between hosts on different networks. The Internet Layer enables internetworking by connecting multiple networks together.
  
  4. **Link Layer (also known as the Network Interface Layer or Data Link Layer)**: The lowest layer of the TCP/IP model, the link layer deals with the physical connection between devices and the local network medium, such as Ethernet or Wi-Fi. It's responsible for transferring data frames between neighboring network nodes on the same local network segment.

<u>B/ Uses of the TCP/IP model:</u>

1. **Standardization**: The TCP/IP model provides a standardized framework for designing, implementing, and troubleshooting network communication protocols and systems.

2. **Interoperability**: It enables different types of computers and networks to communicate with each other, facilitating interoperability across diverse hardware and software platforms.

3. **Scalability**: TCP/IP supports large-scale networks, such as the internet, by providing a flexible architecture that can accommodate a wide range of devices and network sizes.

4. **Flexibility**: The modular design of TCP/IP allows for easy modification and adaptation to evolving network technologies and requirements.

5. **Global Connectivity**: The TCP/IP model underpins the internet, enabling global connectivity and communication between billions of devices worldwide.
   
   Overall, the TCP/IP model serves as a foundational framework for modern networking, enabling the reliable and efficient transmission of data across diverse networks.
