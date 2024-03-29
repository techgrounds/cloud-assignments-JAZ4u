# [5\ Networking_case_study]

CASE STUDY:
Case studies are a little different from the regular exercises you do here at Techgrounds. Up until now every exercise has introduced a new topic, where you had to figure out how to make it work. In a case study we combine your previously learned knowledge with a real life example (or a fictional example closely resembling a real life situation).

In this case study you take the role of a network administrator setting up a network in the new office of a small e-commerce company. Of course there are multiple ways to go about this problem, but this company has specifically said that network security is extremely important to them.

The office contains the following devices:

- A web server where our webshop is hosted
- A database with login credentials for users on the webshop
- 5 workstations for the office workers
- A printer
- An AD server
- A file server containing internal documents

As a network administrator you get to choose which networking devices get used.

![bad_network_design.png](bad_network_design.png)

![good_network_design.png](good_network_design.png)

## Key-terms

- https://app.diagrams.net/
  
  [https://app.diagrams.net/](https://app.diagrams.net/) is a web-based application for creating diagrams and flowcharts. Formerly known as Draw.io, it provides a user-friendly interface for designing various types of diagrams, including flowcharts, network diagrams, organizational charts, UML diagrams, and more.
  
  Here are some key features of diagrams.net:
  
  1. **Ease of Use:** The application offers a simple and intuitive interface, making it easy for users to create diagrams without extensive training or experience.
  
  2. **Wide Range of Diagram Types:** diagrams.net supports a variety of diagram types, catering to different needs and purposes. Users can choose from templates or start from scratch to create diagrams suited to their specific requirements.
  
  3. **Collaboration:** Users can collaborate on diagrams in real-time by sharing diagrams with others and working together on the same document simultaneously. Changes made by one user are instantly visible to others, facilitating teamwork and communication.
  
  4. **Integration:** diagrams.net integrates with various cloud storage services such as Google Drive, OneDrive, Dropbox, and GitHub, allowing users to save and access their diagrams seamlessly across different platforms and devices.
  
  5. **Customization:** The application offers extensive customization options, including the ability to change colors, fonts, shapes, and styles to match the user's preferences or corporate branding.
  
  6. **Export and Import:** Users can export diagrams in various formats, including PNG, JPEG, SVG, PDF, and XML. Additionally, diagrams created in other applications can be imported into diagrams.net for further editing or collaboration.
  
  Overall, diagrams.net is a versatile and user-friendly tool for creating diagrams and flowcharts, suitable for individuals, teams, and organizations across different industries and domains.

- Network Case Study
  
  A network case study is an in-depth analysis of a specific networking scenario or implementation. It typically involves examining real-world examples of network design, deployment, troubleshooting, or optimization to understand the challenges, solutions, and outcomes involved.
  
  Here's what a network case study may include:
  
  1. **Background Information:** This section provides context for the case study, including details about the organization or environment in which the network operates. It may describe the organization's size, industry, network infrastructure, goals, challenges, and any relevant constraints.
  
  2. **Problem Statement:** The case study outlines the specific network-related problem or issue that prompted the need for analysis. This could involve issues such as network downtime, performance degradation, security breaches, scalability concerns, or inefficiencies in network design.
  
  3. **Solution Implementation:** It describes the steps taken to address the problem, including the design, deployment, and configuration of network solutions or technologies. This may involve hardware (routers, switches, firewalls), software (network management systems, security tools), or architectural changes (subnetting, VLAN implementation).
  
  4. **Challenges and Considerations:** The case study discusses any challenges or obstacles encountered during the implementation process. This could include technical complexities, budget constraints, compatibility issues, stakeholder buy-in, or unforeseen complications.
  
  5. **Results and Outcomes:** It evaluates the effectiveness of the implemented solution in addressing the initial problem or issue. This may involve quantitative metrics (e.g., network uptime, throughput, latency) as well as qualitative assessments (user feedback, operational improvements).
  
  6. **Lessons Learned:** The case study concludes with reflections on key takeaways and lessons learned from the experience. This may include insights into best practices, areas for improvement, recommendations for future projects, or strategies for mitigating similar challenges in the future.
  
  Examples of network case studies could include:
  
  - Migration from a traditional on-premises network to a cloud-based network infrastructure.
  - Implementation of a software-defined networking (SDN) solution to improve network agility and scalability.
  - Deployment of a wireless network in a large enterprise environment.
  - Network optimization for a high-traffic e-commerce website to improve performance and reliability.
  - Security enhancements for a network infrastructure to protect against cyber threats and data breaches.
  
  Overall, network case studies provide valuable insights into real-world networking scenarios, helping practitioners and organizations learn from both successes and failures in network design and management.
  
  

- VLAN
  A VLAN, or Virtual Local Area Network, is a technology used in computer networking to logically divide a single physical network into multiple broadcast domains. This segmentation allows network administrators to create isolated networks within the same physical infrastructure, providing improved security, performance, and manageability.
  
  Here are some key points about VLANs:
  
  1. **Logical Segmentation:** VLANs create virtual LANs by grouping together devices based on criteria such as department, function, or security requirements, regardless of their physical location within the network.
  
  2. **Broadcast Control:** By dividing the network into multiple VLANs, broadcast traffic is contained within each VLAN, reducing network congestion and improving overall network performance.
  
  3. **Enhanced Security:** VLANs provide security benefits by isolating traffic between different segments of the network. Devices within one VLAN typically cannot communicate directly with devices in another VLAN without the use of routing or firewall rules.
  
  4. **Flexibility and Scalability:** VLANs offer flexibility in network design and allow for easy reconfiguration as network requirements change. They also enable efficient use of network resources and facilitate network expansion without the need for physical reconfiguration.
  
  5. **Simplifies Network Management:** VLANs simplify network management by allowing administrators to apply consistent policies and configurations across groups of devices within a VLAN. This centralized management approach enhances network administration and troubleshooting.
  
  6. **Inter-VLAN Communication:** While VLANs isolate traffic within their own broadcast domain, communication between VLANs requires routing or Layer 3 devices such as routers or Layer 3 switches. This allows for controlled communication between different segments of the network while maintaining segmentation for security purposes.
  
  Overall, VLANs provide a powerful tool for network segmentation, enabling organizations to optimize network performance, enhance security, and streamline network management. They are widely used in enterprise environments, data centers, and service provider networks to create scalable and secure network architectures.

## Opdracht

Exercise

- Design a network architecture for the above use case.
- Explain your design decisions

### Gebruikte bronnen

- https://www.youtube.com/watch?v=oopkClg1kxM
  
  Beer:30 - Network Architecture Review

### Ervaren problemen

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

# Resultaat

 Exercise

- Design a network architecture for the above use case.
- Explain your design decisions
