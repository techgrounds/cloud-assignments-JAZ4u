# [3/ IAM]

- Security goes in two steps: authentication and authorization. Both are two different actions that happen whenever you log in.

        Multi-factor authentication (MFA) is a common way to improve security.It is best         practice to follow the principle of least privilege for authorization.

- IAM (Identity and Access Management) is a framework of policies and technologies that ensures the right individuals have appropriate access to technology resources within an organization. It involves managing digital identities, authentication, authorization, and accountability to secure systems, applications, and data.

## Key-terms

- Multi-factor authentication (MFA)
  
  Multifactor Authentication (MFA) is a security measure that requires users to provide multiple forms of verification to access an account or system. It adds an extra layer of protection beyond just a username and password, making it more difficult for unauthorized users to gain access to sensitive information or resources.
  
  Typically, MFA involves the following factors of authentication:
  
  1. **Something You Know**: This factor refers to knowledge-based authentication, such as a password, PIN, or security questions. It is something that the user knows and can provide to prove their identity.
  
  2. **Something You Have**: This factor involves possession-based authentication, such as a physical token, smart card, or mobile device. It is something that the user possesses and can use to authenticate their identity.
  
  3. **Something You Are**: This factor is based on biometric authentication, such as fingerprint scans, facial recognition, iris scans, or voice recognition. It is something inherent to the user's physical characteristics that can be used to verify their identity.
  
  By requiring multiple factors from different categories, MFA significantly enhances security compared to traditional single-factor authentication methods, which typically rely solely on something the user knows (e.g., a password). Even if one factor is compromised (such as a stolen password), the additional factors provide an extra layer of defense against unauthorized access.
  
  MFA is commonly used in various contexts, including online accounts (such as email, banking, and social media), corporate networks, remote access systems, and cloud services. It helps organizations mitigate the risk of unauthorized access, data breaches, identity theft, and other security threats by ensuring that only authorized users can access protected resources.

- (network) authorization
  
  **Network authorization** refers to the process of granting or denying access to network resources based on the identity and permissions of the user or device requesting access. Here are some key points about network authorization:
  
  - Network authorization is a critical component of network security that helps ensure that only authorized users or devices can access specific resources within a network.
  - Authorization is typically the second step in the broader process of network access control, following authentication (verification of the identity of the user or device).
  - Once a user or device is authenticated, the network authorization process determines what actions they are allowed to take and what resources they can access based on predefined policies and permissions.
  - Network authorization policies can be defined at various levels, such as user roles, device types, time of day, location, and other contextual factors, to enforce granular access control.
  - Authorization decisions are based on access control lists (ACLs), role-based access control (RBAC), attribute-based access control (ABAC), and other policy enforcement mechanisms.
  - Network authorization mechanisms help organizations enforce security policies, maintain compliance with regulatory requirements, and protect sensitive data from unauthorized access.
  - Authorization policies can be managed centrally through network access control (NAC) solutions, identity and access management (IAM) systems, and other security tools that enforce access control rules across the network.
  - Effective network authorization plays a key role in preventing unauthorized access, reducing the risk of data breaches, and maintaining the confidentiality, integrity, and availability of network resources.
  
  In summary, network authorization is a fundamental aspect of network security that governs access to resources based on user identity, device characteristics, and defined policies to protect sensitive information and maintain the integrity of the network infrastructure.

- (network) authentication
  
  Network authentication is the process of verifying the identity of a user or device attempting to connect to a network. This authentication ensures that only authorized users or devices gain access to the network resources, thereby helping to maintain the security and integrity of the network.
  
   Key Aspects of Network Authentication:
  
  1. **User Identification**: Network authentication involves confirming the identity of individual users or devices seeking access to the network. This can be done through a variety of means, such as usernames, passwords, digital certificates, or biometric credentials.
  
  2. **Authentication Protocols**: Various authentication protocols, such as RADIUS (Remote Authentication Dial-In User Service), TACACS+ (Terminal Access Controller Access-Control System Plus), and 802.1X, are used to facilitate the authentication process and ensure secure access to network resources.
  
  3. **Multi-Factor Authentication (MFA)**: In many cases, network authentication incorporates multi-factor authentication, requiring users to provide more than one form of verification, such as a password and a unique code sent to their mobile device, to enhance security.
  
  4. **Integration with Identity Management Systems**: Network authentication often integrates with identity management systems to centralize user authentication and access control, streamlining the management of user credentials and permissions across the network.
     
     Benefits of Network Authentication:
  - **Security**: By verifying the identity of users and devices, network authentication helps prevent unauthorized access and protects sensitive data and resources from potential threats.
  
  - **Access Control**: It enables administrators to control and manage access to network resources based on user identities and predefined permissions, ensuring that users only have access to the resources they are authorized to use.
  
  - **Accountability**: Authentication mechanisms provide an audit trail, allowing network administrators to track user activities and hold users accountable for their actions on the network.
    
    Common Authentication Methods:
  
  - **Username and Password**: The most common form of authentication, requiring users to provide a unique username and a corresponding password.
  
  - **Biometric Authentication**: Involves using unique biological traits such as fingerprints, iris patterns, or facial recognition for user verification.
  
  - **Certificate-Based Authentication**: Utilizes digital certificates to authenticate users and devices on the network.
  
  In summary, network authentication is a critical process that validates the identity of users and devices seeking access to a network, ensuring security, access control, and accountability. It encompasses various methods and protocols to verify user identities and safeguard network resources from unauthorized access.

- IAM
  
   stands for Identity and Access Management. In the context of networks and information technology, IAM refers to the framework of policies and technologies for ensuring that the right individuals have the appropriate access to technology resources. This includes systems, applications, and data, and it involves managing digital identities and their permissions within an organization.
  
  IAM systems typically involve processes for authentication, authorization, and accountability.
  
  1. **Authentication**: Verifying the identity of users, typically through methods like passwords, biometric scans, security tokens, or multi-factor authentication.
  
  2. **Authorization**: Determining what actions and resources users are allowed to access based on their authenticated identity. This involves assigning permissions and privileges, often through role-based access control (RBAC) or attribute-based access control (ABAC) mechanisms.
  
  3. **Accountability**: Logging and monitoring user activities to ensure compliance, detect unauthorized access, and facilitate forensic analysis in case of security incidents.
  
  IAM helps organizations manage user access across various platforms and applications securely. It ensures that only authorized users have access to sensitive information and resources, thereby reducing the risk of data breaches and unauthorized access.

- The principle of least privilege 
  The principle of least privilege is a security concept and best practice that advocates for limiting user or system accounts' access rights only to the minimum permissions required to perform their necessary tasks or functions. In other words, users should be granted the least amount of access necessary to accomplish their job responsibilities, and systems should operate with minimal privileges to reduce the potential impact of security breaches or malicious activities.

Key principles of the least privilege include:

1. **Minimize Access**: Users should only be granted access to the resources, data, and functionalities required to perform their job duties effectively. Unnecessary access rights should be revoked to reduce the attack surface and mitigate the risk of unauthorized access or misuse.

2. **Default Deny**: By default, access to resources or systems should be denied unless explicitly authorized. This approach ensures that users must request and justify access, promoting accountability and reducing the likelihood of unintended or unauthorized access.

3. **Need-to-Know Basis**: Access should be granted on a need-to-know basis, meaning users should only have access to information or resources essential to their specific roles or tasks. This principle helps prevent the exposure of sensitive information to unauthorized individuals or entities.

4. **Separation of Duties**: Responsibilities and access rights should be divided among multiple users or roles to prevent conflicts of interest and reduce the risk of insider threats. For example, the person responsible for approving transactions should not be the same person responsible for executing them.

5. **Regular Reviews and Audits**: Access rights should be periodically reviewed and audited to ensure alignment with business requirements and security policies. This includes removing outdated or unnecessary access privileges and identifying and addressing potential security vulnerabilities.

Implementing the principle of least privilege helps organizations enhance security, reduce the likelihood of security incidents, and minimize the potential impact of security breaches or insider threats. It is a fundamental aspect of access control and security management practices across various industries and sectors. 

## Assignment

Study:

- The difference between authentication and authorization.
- The three factors of authentication and how MFA improves security.
- What the principle of least privilege is and how it improves security.

### Used sources

[Plaats hier de bronnen die je hebt gebruikt.]

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Result

Study:

- The difference between authentication and authorization.
  
  **Authorization**: Determining what actions and resources users are allowed to access based on their authenticated identity. This involves assigning permissions and privileges, often through role-based access control (RBAC) or attribute-based access control (ABAC) mechanisms.
  
  **Authorization**: Determining what actions and resources users are allowed to access based on their authenticated identity. This involves assigning permissions and privileges, often through role-based access control (RBAC) or attribute-based access control (ABAC) mechanisms.

- The three factors of authentication and how MFA improves security.
  
  Typically, MFA involves the following factors of authentication:
  
  1. **Something You Know**: This factor refers to knowledge-based authentication, such as a password, PIN, or security questions. It is something that the user knows and can provide to prove their identity.
  
  2. **Something You Have**: This factor involves possession-based authentication, such as a physical token, smart card, or mobile device. It is something that the user possesses and can use to authenticate their identity.
  
  3. **Something You Are**: This factor is based on biometric authentication, such as fingerprint scans, facial recognition, iris scans, or voice recognition. It is something inherent to the user's physical characteristics that can be used to verify their identity.
  
  By requiring multiple factors from different categories, MFA significantly enhances security compared to traditional single-factor authentication methods, which typically rely solely on something the user knows (e.g., a password). Even if one factor is compromised (such as a stolen password), the additional factors provide an extra layer of defense against unauthorized access.
  
  MFA is commonly used in various contexts, including online accounts (such as email, banking, and social media), corporate networks, remote access systems, and cloud services. It helps organizations mitigate the risk of unauthorized access, data breaches, identity theft, and other security threats by ensuring that only authorized users can access protected resources.

- What the principle of least privilege is and how it improves security.
  
  Implementing the principle of least privilege helps organizations enhance security, reduce the likelihood of security incidents, and minimize the potential impact of security breaches or insider threats. It is a fundamental aspect of access control and security management practices across various industries and sectors.
1. **Minimize Access**: Users should only be granted access to the resources, data, and functionalities required to perform their job duties effectively. Unnecessary access rights should be revoked to reduce the attack surface and mitigate the risk of unauthorized access or misuse.

2. **Default Deny**: By default, access to resources or systems should be denied unless explicitly authorized. This approach ensures that users must request and justify access, promoting accountability and reducing the likelihood of unintended or unauthorized access.

3. **Need-to-Know Basis**: Access should be granted on a need-to-know basis, meaning users should only have access to information or resources essential to their specific roles or tasks. This principle helps prevent the exposure of sensitive information to unauthorized individuals or entities.

4. **Separation of Duties**: Responsibilities and access rights should be divided among multiple users or roles to prevent conflicts of interest and reduce the risk of insider threats. For example, the person responsible for approving transactions should not be the same person responsible for executing them.

5. **Regular Reviews and Audits**: Access rights should be periodically reviewed and audited to ensure alignment with business requirements and security policies. This includes removing outdated or unnecessary access privileges and identifying and addressing potential security vulnerabilities.