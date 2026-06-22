# The Shared Responsibility Model
The responibilities vary based on where the workload is hosted
- On-premises (On-Prem): Your organization manages and secures the entire stack—from the physical building and hardware to the operating system, applications, and data.
- Infrastructure as a Service (IaaS): The cloud provider secures the physical datacenter, the network hardware, and the host machines. You're responsible for the operating systems, applications, network controls you configure, and your data.
- Platform as a Service (PaaS): The cloud provider also takes on responsibility for the operating system and the runtime environment. You're responsible for your application code, its configuration, access controls, and your data.
- Software as a Service (SaaS): The cloud provider manages the entire application stack and its underlying infrastructure. You're responsible for access management—controlling who uses the service—your data, and how you configure tenant-level settings.

<img width="3858" height="2475" alt="image" src="https://github.com/user-attachments/assets/f2cc9596-e6de-4efd-89f0-05f8cedb55fa" />

# Defense in depth
Defense in depth uses a layered apporoach to security. Each layer provides protection so that if one layer is breached the other layers is used to catch or limit the attack. Examples include:

- Physical security: Limiting access to a datacenter to only authorized personnel.
- Identity and access security: Controlling access to infranstructure and change
- Perimeter-security Distributed denial of service (DDoS) protection to flter large-scale attacks before they can cause a distrpution for users.
- Network security: Limit communication between resources using segmentation and access controls.
- Compute layer security: Securing access to virtual machines by closing certain ports
- Application layer security: Ensure applications are secure and free of security vulnerabilities.
- Data layer security: Control acess to business and customer data and use encryption to protect data
<img width="245" height="271" alt="image" src="https://github.com/user-attachments/assets/da97ea61-5a8d-4f52-ae07-8a963b616ad2" />

# Confidentiality, integrity, availability (CIA)
CIA- the goals of a cybersecurity strategy

- Confidentiality: ensuring sensetitive data, such as customer information remains condifential.
- Integrity: ensuring data or messages haven't been tampered with.
- Availability: refers to making data available to those who need it.

- # The Zero Trust Model
Zero Trust guiding Principles 
 - Verify explicitly
  - Least Privileged access
  - Assume breach

Six foundation pillars:
- Identities: may be users, services, or devices
- Devices: create a large attack surface as data flows
- Applications: the way that data is consumed
- Data: classified, labeled, and encrypted
- Infranstrucucture: represents a threat vector
- Networks: should be segmented
<img width="597" height="376" alt="image" src="https://github.com/user-attachments/assets/6100a404-fdcb-490e-b5b8-79dea2096532" />

# Encryption

Encryption is the process of making data unreadable and usuable to unauthorized viewers.
- Encryption of data at rest
- Encryption of data in transit
- Encryption of data in use

Two top-level typesof encryption:
- Symmetric: Uses the same key to encrypt and decrypt data
- Asymmetric: Uses a public key and a private key pair
<img width="471" height="355" alt="image" src="https://github.com/user-attachments/assets/2d00c264-dd1d-4b36-a36a-910dfc594371" />

# Hashing

Hashing uses an algorithm to convert the orginal text to a unique fixed-length hash value. Hash functions are:
- Deterministic: the same input produces the same ouput
- A unique identifier of its associated data
- Different to encryption in that the hashed value isn't subsequently decrypted back to the original
- Used to store passwords; the password is "salted" to mitigate the risk of brute force dictionary attacks.
<img width="248" height="133" alt="image" src="https://github.com/user-attachments/assets/f223f806-9312-4917-a1ce-07797090deae" />

# Governane. compliance, and risk (GRC) concepts

GRC helps organizations reduce risk and improve compliance effectiveness.
- Governane: The rules, practices, and processes an organization uses to direct and control its activities
- Risk management: The process of identifying, asessing, and responding to threats or events that can impact business objectives
- Compliance: The country/region, state, or federal lawsor even multi-national regulations that an organization must follow
<img width="443" height="408" alt="image" src="https://github.com/user-attachments/assets/4438299c-0f96-4fac-9807-fd6b64be846c" />

