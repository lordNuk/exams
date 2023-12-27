UNIT – IV
Cloud security fundamentals:
    - issues, 
    - threats,
    - data security and information security,
    - Vulnerability assessment tool for cloud,
    - Privacy and Security in cloud,
Cloud computing security architecture: 
    - Architectural Considerations- General Issues,
    - Trusted Cloud computing,
    - Secure Execution Environments and Communications,
    - Micro-architectures;

Identity Management and Access control-
    - Identity management,
    - Access control,

Autonomic Security 

Cloud computing security challenges:
    - Virtualization security management,
    - virtual threats,
    - VM Security Recommendations,
    - VM-Specific Security techniques,
    - Secure Execution Environments and Communications in cloud.

---

# Identity Management and Access Control

- Identity management and access control are fundamental functions required for secure cloud computing. 
- The simplest form of identity management is user ID and password. 
- cloud computing requires more robust authentication, authorization, and access control. 
    - using technology such as biometrics or smart cards, 
    - and determine when a resource has been accessed by unauthorized entities.

## Identity Management

- Identification and authentication are the keystones of most access control systems. 
- Identification is the act of a user professing an identity to a system, usually in the form of a username or user login ID to the system. 
- It establishes user accountability for the actions on the system. 
- User IDs should be 
    - unique and not shared among different individuals. 
    - follow set standards, such as first initial followed by last name, and so on. 
    - should not reflect the user’s job title or function (for security purposes).

- Authentication is verification that the user’s claimed identity is valid, and it is usually implemented through a user password at login. 
- Authentication is based on the following three factor types:
    1. Type 1 — Something you know, such as a personal identification number (PIN) or password
    2. Type 2 — Something you have, such as an ATM card or smart card
    3. Type 3 — Something you are (physically), such as a fingerprint or retina scan
    - Sometimes a fourth factor, something you do, is added to this list. 

- Two-factor authentication requires two of the three factors to be used in the authentication process. 
    - For example, withdrawing funds from an ATM machine requires two-factor authentication in the form of the ATM card (something you have) and a PIN number (something you know).

- A front-end authentication device or a back-end authen- tication server, which services multiple workstations or the host, can perform the authentication.

### Passwords
- Because passwords can be compromised, they must be protected. 
- In the ideal case, a password should be used only once. 
    - This “one-time password,” or OTP, provides maximum security. 
- Static and Dynamic password:
    - A password that is the same for each logon is called a static password. 
    - A password that changes with each logon is termed a dynamic password. 
- The changing of passwords can also fall between these two extremes. Depending on:
    - the criticality of the information needing protection 
    - the password’s frequency of use. 

- Passphrase:
    - sequence of characters that is usually longer than the allotted number for a password. 
    - it is converted into a virtual password by the system.

Passwords can be provided by a number of devices, including:
    - tokens
    - memory cards
    - smart cards

#### Tokens
- Tokens, in the form of small, hand-held devices, are used to provide passwords.
- Four basic types of tokens:
1. Static password tokens
    - Owners authenticate themselves to the token by typing in a secret password.
    - If the password is correct, the token authenticates the owner to an information system.
2. Synchronous dynamic password tokens, clock-based
    - The token generates a new, unique password value at fixed time intervals that is synchronized with the same password on the authentication server (this password is the time of day encrypted with a secret key).
    - The unique password is entered into a system or workstation along with an owner’s PIN.
    - The authentication entity in a system or workstation knows an owner’s secret key and PIN, and the entity verifies that the entered password is valid and that it was entered during the valid time window.
3. Synchronous dynamic password tokens, counter-based
    - The token increments a counter value that is synchronized with a counter in the authentication server.
    - The counter value is encrypted with the user’s secret key inside the token and this value is the unique password that is entered into the system authentication server.
    - The authentication entity in the system or workstation knows the user’s secret key and the entity verifies that the entered password is valid by performing the same encryption on its identical counter value.
4. Asynchronous tokens, challenge-response
    - A workstation or system generates a random challenge string, and the owner enters the string into the token along with the proper PIN.
    - The token performs a calculation on the string using the PIN and generates a response value that is then entered into the workstation or system.
    - The authentication mechanism in the workstation or system performs the same calculation as the token using the owner’s PIN and challenge string and compares the result with the value entered by the owner. If the results match, the owner is authenticated.

#### Memory Cards
- A memory card stores encrypted passwords and other related identifying information.
    - for eg: telephone calling card and an ATM cards

#### Smart Cards
- Smart cards provide even more capability than memory cards by incorporating additional processing power on the cards. 
- These credit-card-size devices comprise microprocessor and memory and are used to store:
    - digital signatures, private keys, passwords, and other personal information.

### Biometrics
- It is based on the Type 3 authentication mechanism — something you are. 
- Biometrics is defined as an automated means of identifying or authenticating the identity of a living person based on physiological or behavioral characteristics.
- In biometrics, 
    - identification is a one-to-many search of an individual’s characteristics from a database of stored images. 
    - authentication is a one-to-one search to verify a claim to an identity made by a person. 

- There are three main performance measures in biometrics:
    1. False rejection rate (FRR) or Type I Error — The percentage of valid subjects that are falsely rejected.
    2. False acceptance rate (FAR) or Type II Error — The percentage of invalid subjects that are falsely accepted.
    3. Crossover error rate (CER) — The percentage at which the FRR equals the FAR. The smaller the CER, the better the device is performing.

- factors to considere:
    - enrollment time, throughput rate, and acceptability.
- Enrollment time is the time that it takes to initially register with a system by providing samples of the biometric characteristic to be evaluated.
    - An acceptable enrollment time is around two minutes.
- The throughput rate is the rate at which the system processes and identifies or authenticates individuals. 
    - Acceptable throughput rates are in the range of 10 subjects per minute. 
- Acceptability refers to considerations of privacy, invasiveness, and psychological and physical comfort when using the system. 

- The following are typical biometric characteristics that are used to uniquely authenticate an individual’s identity:
    1. Fingerprints — Fingerprint characteristics are captured and stored. Typical CERs are 4–5%.
    2. Retina scans — The eye is placed approximately two inches from a camera and an invisible light source scans the retina for blood vessel patterns. CERs are approximately 1.4%.
    3. Iris scans — A video camera remotely captures iris patterns and characteristics. CER values are around 0.5%.
    4. Hand geometry — Cameras capture three-dimensional hand characteristics. CERs are approximately 2%.
    5. Voice — Sensors capture voice characteristics, including throat vibrations and air pressure, when the subject speaks a phrase. CERs are in the range of 10%.
    6. Handwritten signature dynamics — The signing characteristics of an individual making a signature are captured and recorded. Typical characteristics including writing pressure and pen direction. CERs are not published at this time.

### Implementing Identity Management
- implementing identity management requires a high-level corporate commitment and dedication of sufficient resources to accomplish the task. 
- Tasks required:
    1. Establishing a database of identities and credentials
    2. Managing users’ access rights
    3. Enforcing security policy
    4. Developing the capability to create and modify accounts
    5. Setting up monitoring of resource accesses
    6. Installing a procedure for removing access rights
    7. Providing training in proper procedures

- An identity management effort can be supported by software that automates many of the required tasks.

- Identity management is also addressed by the XML-based eXtensible Name Service (XNS) open protocol for universal addressing. 
- XNS provides the following capabilities:
    1. A permanent identification address for a container of an individual’s personal data and contact information
    2. Means to verify whether an individual’s contact information is valid
    3. A platform for negotiating the exchange of information among different entities

## Access Control
- Access control is intrinsically tied to identity management and is necessary to preserve the confidentiality, integrity, and availability of cloud data.
- This policy is a high-level statement of management intent regarding the control of access to information and the personnel who are authorized to receive that information.
- Three things that must be considered for the planning and implementation of access control mechanisms are:
    - threats to the system, 
    - the system’s vulnerability to these threats, and 
    - the risk that the threats might materialize. 
- These concepts are defined as follows:
    1. Threat — An event or activity that has the potential to cause harm to the information systems or networks
    2. Vulnerability — A weakness or lack of a safeguard that can be exploited by a threat, causing harm to the information systems or networks
    3. Risk — The potential for harm or loss to an information system or network; the probability that a threat will materialize

### Controls
- Controls are implemented to mitigate risk and reduce the potential for loss.
- Two important control concepts are:
    - separation of duties 
    - the principle of least privilege 
- Separation of duties requires an activity or process to be performed by two or more entities for successful completion.
- Least privilege means that the entity that has a task to perform should be provided with the minimum resources and privileges required to complete the task for the minimum necessary period of time.

- Control measures can be:
    - administrative, logical (also called technical), and physical in their implementation.
    1. Administrative controls include policies and procedures, security awareness training, background checks, work habit checks, a review of vacation history, and increased supervision.
    2. Logical or technical controls involve the restriction of access to systems and the protection of information. Examples of these types of controls are encryption, smart cards, access control lists, and transmission protocols.
    3. Physical controls incorporate guards and building security in general, such as the locking of doors, the securing of server rooms or laptops, the protection of cables, the separation of duties, and the backing up of ﬁles.

- Controls provide accountability for individuals who are accessing sensitive information in a cloud environment.
- This accountability is accomplished through access control mechanisms that require identiﬁcation and authentication, and through the audit function.
- Assurance procedures:
    - they ensure that the control mechanisms correctly implement the security policy for the entire life cycle of a cloud information system.

- In general, a group of processes that share access to the same resources is called a protection domain, and the memory space of these processes is isolated from other running processes.

#### Models for Controlling Access
- Controlling access by a subject (an active entity such as an individual or process) to an object (a passive entity such as a ﬁle) involves setting up access rules.
- These rules can be classiﬁed into three categories or models.
1. Mandatory Access Control
    - The authorization of a subject’s access to an object depends upon labels, which indicate the subject’s clearance, and the classiﬁcation or sensitivity of the object.
    - For example, the military classiﬁes documents as unclassiﬁed, conﬁdential, secret, and top secret.
    - Similarly, an individual can receive a clearance of conﬁdential, secret, or top secret and can have access to documents classiﬁed at or below his or her speciﬁed clearance level.
    - Rule-based access control is a type of mandatory access control because rules determine this access (such as the correspondence of clearance labels to classiﬁcation labels), rather than the identity of the subjects and objects alone.
2. Discretionary Access Control
    - the subject has authority, within certain limitations, to specify what objects are accessible.
    - For example, access control lists (ACLs) can be used.
    - An access control list is a list denoting which users have what privileges to a particular resource.
    - An access control triple consists of the user, program, and ﬁle, with the corresponding access privileges noted for each user.
    - This type of access control is used in local, dynamic situations in which the subjects must have the discretion to specify what resources certain users are permitted to access.
    - When a user within certain limitations has the right to alter the access control to certain objects, this is termed a user-directed discretionary access control.
    - An identity-based access control is a type of discretionary access control based on an individual’s identity.
3. Nondiscretionary Access Control
    - A central authority determines which subjects can have access to certain objects based on the organizational security policy.
    - The access controls might be based on the individual’s role in the organization (role-based) or the subject’s responsibilities and duties (task-based).
    - useful in an organization with frequent personnel changes.
    - Access control can also be characterized as context-dependent or content-dependent. Context-dependent access control is a function of factors such as location, time of day, and previous access history. It is concerned with the environment or context of the data.
    - In content-dependent access control, access is determined by the information contained in the item being accessed.

### Single Sign-On (SSO)
- Single sign-on (SSO) addresses the cumbersome situation of logging on multiple times to access different resources.
- When users must remember numerous passwords and IDs, they might take shortcuts in creating them that could leave them open to exploitation.
- In SSO, a user provides one ID and password per work session and is automatically logged on to all the required applications.
- For SSO security, the passwords should not be stored or transmitted in the clear.
- SSO applications can run either on a user’s workstation or on authentication servers.
- The advantages of SSO: 
    - having the ability to use stronger passwords,
    - easier administration of changing or deleting the passwords,
    - less time to access resources.
- The major disadvantage of many SSO:
    - once users obtain access to the system through the initial logon, they can freely roam the network resources without any restrictions.
- Authentication mechanisms include items such as smart cards and magnetic badges.
- Strict controls must be enforced to prevent a user from changing conﬁgurations that another authority sets.
- SSO can be implemented by using scripts that replay the users’ multiple logins or by using authentication servers to verify a user’s identity, and encrypted authentication tickets to permit access to system services.

---

# Autonomic Security

Autonomic computing refers to a self-managing computing model in which computer systems reconfigure themselves in response to changing conditions and are self-healing.

It offers capabilities that can improve the security of information systems and cloud computing.

The ability of autonomic systems to collect and interpret data and recommend or implement solutions can go a long way toward enhancing security and providing for recovery from harmful events.

## Autonomic Systems

Autonomic systems are based on the human autonomic nervous system, which is self-managing, monitors changes that affect the body, and maintains internal balances.

Therefore, an autonomic computing system has the goal of performing self-management to maintain correct operations despite perturbations to the system.

Such a system requires sensory inputs, decision-making capability, and the ability to implement remedial activities to maintain an equilibrium state of normal operation.

Examples of events that would have to be handled autonomously include the following:
1. Malicious attacks
2. Hardware or software faults
3. Excessive CPU utilization
4. Power failures
5. Organizational policies
6. Inadvertent operator errors
7. Interaction with other systems
8. Software updates

IBM introduced the concept of autonomic computing and its eight defining characteristics as follows:
1. Self-awareness — An autonomic application/system “knows itself” and is aware of its state and its behaviors.
2. Self-configuring — An autonomic application/system should be able configure and reconfigure itself under varying and unpredictable conditions.
3. Self-optimizing — system should be able to detect sub-optimal behaviors and optimize itself to improve its execution.
4. Self-healing — system should be able to detect and recover from potential problems and continue to function smoothly.
5. Self-protecting — system should be capable of detecting and protecting its resources from both internal and external attack and maintaining overall system security and integrity.
6. Context-aware — system should be aware of its execution environment and be able to react to changes in the environment.
7. Open — system must function in a heterogeneous world and should be portable across multiple hardware and software architectures. Consequently, it must be built on standard and open protocols and interfaces.
8. Anticipatory — system should be able to anticipate, to the extent possible, its needs and behaviors and those of its context, and be able to manage itself proactively.

The underlying concept of autonomic systems is self-management, whereby a computational system maintains proper operation in the face of changing external and internal conditions, evaluates the necessity for upgrades, installs software, conducts regression testing, performs performance tuning of middleware, and detects and corrects problem situations in general.

## Autonomic Protection

Autonomic self-protection involves detecting a harmful situation and taking actions that will mitigate the situation.

These systems will also be designed to predict problems from analysis of sensory inputs and initiate corrective measures.

An autonomous system security response is based on:
    - network knowledge,
    - capabilities of connected resources,
    - information aggregation,
    - the complexity of the situation,
    - the impact on affected applications.

The decision-making element of autonomic computing, taking into account the current security posture and security context of the system to be protected, can take actions such as:
    - changing the strength of required authentications or
    - modifying encryption keys.

The security context is derived from information acquired from network and system supervising elements and then collected into a higher-level representation of the system security status.

An often overlooked aspect of autonomic systems is that security vulnerabilities can be introduced by configuration changes and additional autonomous activities that are intended to address other computational areas.

Autonomous protection systems should, therefore, adhere to the following guidelines:
1. Minimize overhead requirements.
2. Be consistent with security policies.
3. Optimize security-related parameters.
4. Minimize impact on performance.
5. Minimize potential for introducing new vulnerabilities.
6. Conduct regression analysis and return to previous software versions if problems are introduced by changes.
7. Ensure that reconfiguration processes are secure.

## Autonomic Self-Healing

The process of diagnosing and repairing failures in IT systems can be difficult, time consuming, and usually requires intensive labor effort. Autonomic selfhealing systems can provide the capability to detect and repair software problems and identify hardware faults without manual intervention.

The autonomic process would obtain logged and monitored information and perform an analysis to diagnose the problem area.

This procedure is usually conducted by an autonomic manager that controls computing resource elements with well-defined interfaces that support the diagnostic and mitigation actions.

The managed elements control their internal states and have defined performance characteristics and relationships with other computational elements.

The objective of the autonomous self-healing process is to keep the elements operating according to their design specifications.


---

# Cloud computing security challenges

## Virtualization Security Management

Includes examining the threats and vulnerabilities inherent in virtualized systems and look at some common management solutions to those threats.

### VIRTUALIZATION TYPES
- The Virtual Machine (VM), Virtual Memory Manager (VMM), and hypervisor or host OS are the minimum set of components needed in a virtual environment.
- They comprise virtual environments in a few distinct ways:
    1. Type 1 virtual environments are considered “full virtualization” environments and have VMs running on a hypervisor that interacts with the hardware.
    2. Type 2 virtual environments are also considered “full virtualization” but work with a host OS instead of a hypervisor.
    3. Para-virtualized environments offer performance gains by eliminating some of the emulation that occurs in full virtualization environments.
    4. Other type designations include hybrid virtual machines (HVMs) and hardware-assisted techniques.

- Type 2 environment increases the potential risk of attacks against the host OS. For example, a laptop running VMware with a Linux VM on a Windows XP system inherits the attack surface of both OSs, plus the virtualization code.

### VIRTUALIZATION MANAGEMENT ROLES
- Typically, the VMware Infrastructure is managed by several users performing different roles. The roles assumed by administrators are:
    - Virtualization Server Administrator
    - Virtual Machine Administrator
    - Guest Administrator

- The roles assumed by administrators are configured in VMS and are defined to provide role responsibilities:
    1. Virtual Server Administrator — This role is responsible for installing and configuring the ESX Server hardware, storage, physical and virtual networks, service console, and management applications.
    2. Virtual Machine Administrator — This role is responsible for creating and configuring virtual machines, virtual networks, virtual machine resources, and security policies. The Virtual Machine Administrator creates, maintains, and provisions virtual machines.
    3. Guest Administrator — This role is responsible for managing a guest virtual machine or machines. Tasks typically performed by Guest Administrators include connecting virtual devices, adding system updates, and managing applications that may reside on the operating system.

## Virtual Threats

Some threats to virtualized systems are general in nature, as they are inherent threats to all computerized systems (such as denial-of-service, or DoS, attacks).

Other threats and vulnerabilities, however, are unique to virtual machines. Many VM vulnerabilities stem from the fact that a vulnerability in one VM system can be exploited to attack other VM systems or the host systems, as multiple virtual machines share the same physical hardware.

Some of the vulnerabilities:
1. Shared clipboard — Shared clipboard technology allows data to be transferred between VMs and the host, providing a means of moving data between malicious programs in VMs of different security realms.
2. Keystroke logging — Some VM technologies enable the logging of key- strokes and screen updates to be passed across virtual terminals in the virtual machine, writing to host files and permitting the monitoring of encrypted terminal connections inside the VM.
3. VM monitoring from the host — Because all network packets coming from or going to a VM pass through the host, the host may be able to affect the VM by the following:
    1. Starting, stopping, pausing, and restart VMs
    2. Monitoring and configuring resources available to the VMs, including CPU, memory, disk, and network usage of VMs
    3. Adjusting the number of CPUs, amount of memory, amount and number of virtual disks, and number of virtual network interfaces available to a VM
    4. Monitoring the applications running inside the VM
    5. Viewing, copying, and modifying data stored on the VM’s virtual disks
4. Virtual machine monitoring from another VM — Usually, VMs should not be able to directly access one another’s virtual disks on the host. However, if the VM platform uses a virtual hub or switch to connect the VMs to the host, then intruders may be able to use a hacker technique known as “ARP poisoning” to redirect packets going to or from the other VM for sniffing.
5. Virtual machine backdoors — A backdoor, covert communications channel between the guest and host could allow intruders to perform potentially dangerous operations.

According to the Burton Group five immutable laws of virtualization security must be understood and used to drive security decisions:
1. Law 1: All existing OS-level attacks work in the exact same way.
2. Law 2: The hypervisor attack surface is additive to a system’s risk profile.
3. Law 3: Separating functionality and/or content into VMs will reduce risk.
4. Law 4: Aggregating functions and resources onto a physical platform will increase risk.
5. Law 5: A system containing a “trusted” VM on an “untrusted” host has a higher risk level than a system containing a “trusted” host with an “untrusted” VM.

### VM THREAT LEVELS
Vulnerability/threat matrix is classified into three levels of compromise:
1. Abnormally terminated — 
    - Availability to the virtual machine is compromised, as the VM is placed into an infinite loop that prevents the VM administrator from accessing the VM’s monitor.
2. Partially compromised — 
    - The virtual machine allows a hostile process to interfere with the virtualization manager, contaminating security checkpoints or over-allocating resources.
3. Totally compromised — 
        - The virtual machine is completely overtaken and directed to execute unauthorized commands on its host with elevated privileges.

### Hypervisor Risks
the ability of the hypervisor to provide the necessary isolation during intentional attack greatly determines how well the virtual machine can survive risk.

One reason why the hypervisor is susceptible to risk is because it’s a software program; risk increases as the volume and complexity of application code increases.

Ideally, software code operating within a defined VM would not be able to communicate or affect code running either on the physical host itself or within a different VM: 
- but several issues, such as bugs in the software, or limitations to the virtualization implementation, may put this isolation at risk.

Major vulnerabilities inherent in the hypervisor consist of:
- rogue hypervisor rootkits, 
- external modification to the hypervisor, and 
- VM escape

- Rogue Hypervisors
    - The hypervisor, therefore, has a great level of control over the system, not only in the VM but also on the host machine.
    - VM-based rootkits can hide from normal malware detection systems by initiating a “rogue” hypervisor and creating a cover channel to dump unauthorized code into the system.
    - Proof-of-concept (PoC) exploits have demonstrated that a hypervisor rootkit can insert itself into RAM, downgrade the host OS to a VM, and make itself invisible. A properly designed rootkit could then stay “undetectable” to the host OS, resisting attempts by malware detectors to discover and remove it.

- External Modification of the Hypervisor
    - a poorly protected or designed hypervisor can also create an attack vector.
    - Therefore, a self-protected virtual machine may allow direct modification of its hypervisor by an external intruder. 
    - This can occur in virtualized systems that don’t validate the hypervisor as a regular process.

- VM Escape
    - Virtual machine escape refers to the attacker’s ability to execute arbitrary code on the VM’s physical host, by “escaping” the hypervisor. 
    - Due to improperly configured VM that could allow code to completely bypass the virtual environment, and obtain full root or kernel access to the physical host.
    - This would result in a complete failure of the security mechanisms of the system, and is called VM escape.

### Increased Denial of Service Risk

As the virtual machines share the host’s resources, such as memory, processor, disk, I/O devices, and so on, a denial-of-service attack risk against another VM, the host, or an external service is actually greatly increased.

Because the VM has more complex layers of resource allocation than a traditional system, DoS prevention techniques can become equally more complex.

Like IT protections traditionally implemented against denial-of-service attacks, limiting the consumption of host resources through resource allocation may help lessen the exposure to DoS attacks.

## VM Security Recommendations

### Best Practice Security Techniques
The following security implementation techniques are required for most computer systems, and are still best practices for virtualized systems. These areas include physical security, patching, and remote management techniques.
1. Hardening The Host OS:
    - Vulnerabilities in the host OS can impact the virtual machine (VM) operating system. Compromising the host OS gives an intruder access to all services on hosted VMs.
    - Hardening Techniques:
        - Use strong, regularly changed passwords.
        - Disable unneeded services, especially networked ones.
        - Implement full authentication for access control.
        - Individually firewall the host.
        - Regularly patch and update the host OS after testing on a nonproduction unit.
        - Follow vendor-supplied best practice guides for both guest and host domains. Refer to standards like NIST, DISA STIGS, Center for Internet Security, SANS Institute, and NSA.
2. Limiting Physical Access to Host:
    - Basic physical host security is essential to prevent attacks on the hardware.
    - Implement controls such as card/guard access, locks on machines, and removal of unnecessary drives.
    - BIOS settings should disable booting from any device except the primary hard drive.

3. Encrypted Communications:
    - Use encryption technologies (HTTPS, VPNs, TLS, SSH) for secure communication links.
    - Prevents man-in-the-middle attacks, spoofed attacks, and session hijacking.

4. Disabling Background Tasks:
    - Identify and manage low-priority background processes.
        - disable, limit or offload these to other servers.
    - Virtual machines may have challenges in accurately detecting the host's idle state.
        - causing a situation where background task demands more processor cycles than intended.
        - hacker exploits are designed to piggyback off of these processes.

5. Updating and Patching:
    - Timely patching and updating are crucial for both host and guest VMs.
    - Standardization of the operating system across the enterprise is recommended.
    - Testing patches on nonproduction systems is essential to avoid unforeseen consequences.

6. Enabling Perimeter Defense on VMs:
    - Use firewalls or intrusion detection systems on virtual machines to control data traffic.
    - Implement a defense-in-depth strategy to secure both the perimeter and internal network.

7. Implementing File Integrity Checks:
    - Verify file integrity at the host OS level.
    - Store hash values of core OS files offline for comparison.

8. Maintaining Backups:
    - Perform frequent image backups for all production VMs.
    - Protect backup data streams through encryption and control physical backup media transport and storage.

9. Understanding Attack Surface:
    - Attack surface refers to all running services exposing a host to attacks.
    - Shrinking the attack surface reduces vulnerability exposure and simplifies security.

10. Auditing VM:
    - Auditors must understand risks of virtualized systems connected to public networks.
    - Guidelines from organizations like DISA, CIS, and others provide recommendations for securing virtual environments.


## VM-Specific Security Techniques

Virtual machines are dynamic entities that can be easily provisioned, migrated, and scaled. Security measures must adapt to the changing states of VMs to ensure ongoing protection. Following security techniques must be implemented in addition to traditional best practices described above.

1. Hardening the Virtual Machine:
    - Resource Consumption Limits:
        - Set limits on CPU, memory, and disk usage to prevent one VM from adversely affecting others.
    - Network and Storage Configuration:
        - Properly configure virtual network interfaces and storage to minimize vulnerabilities.
    - Isolation of Shared Components:
        - Ensure components shared across virtual network devices are isolated and secured.
    - Audit Logging:
        - Maintain detailed audit logs for the virtualized infrastructure to track and analyze security events.

2. Hypervisor Security:
    - Change and Configuration Controls:
        - Implement controls for managing patches and configuration changes to the hypervisor.
    - Third-Party Testing:
        - Engage third-party testing services to assess vulnerabilities in the virtualization technology.

3. Root Secure the Monitor:
    - Privilege Escalation Prevention:
        - Ensure that no privilege level within the virtualized guest environment allows interference with the host system.
   
4. One Primary Function per VM:
    - Process Separation:
        - Configure each VM with a single primary function to simplify security management.
        - Complicates the hacker's ability to compromise multiple system components.
   
5. Firewall Additional VM Ports:
    - Independently firewall ports opened by virtual machines, reducing the attack surface.

6. Harden the Host Domain:
    - before securing VMs it's host domain must be secured.
    - Attack Surface Reduction:
        - Reduce the attack surface of the host domain by removing unnecessary elements.
    - Monitoring and Detection:
        - Implement monitoring or Host Intrusion Detection Systems (HIDS) for early threat detection.

7. Unique NICs for Sensitive VMs:
    - Isolation for Confidential Data:
        - Binding network interface addresses to distinct NICs isolates VMs with sensitive information from potential attacks on external NICs.

8. Disconnect Unused Devices:
    - Preventing Undesired Code Execution:
        - Disconnect unnecessary virtual machine device connections during configuration to prevent potential security risks.

9. Additional Recommendations:
    - Treat VMs like Services:
        - Use security measures like chroot, systrace, acls, and least privileged users.
    - Disable Unused Emulated Hardware:
        - Reduce the attack surface by disabling unnecessary emulated hardware and external services.
    - Maintain Guest Software Integrity:
        - Regularly update guest software to address published vulnerabilities and enhance overall security.
10. Securing VM Remote Access:
    - Dedicated Management NIC:
        - Use a separate network interface for remote management tasks to avoid interference with regular network traffic.
    - Encrypted Communications:
        - Utilize secure communication protocols such as SSH or VPNs for remote access.





