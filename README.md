Enterprise Hybrid Infrastructure & Identity Lab

Project Overview
This project demonstrates the deployment and management of a production-grade enterprise environment. It showcases a hybrid identity model integrating On-Premises Active Directory (ADDS) with Microsoft Entra ID, alongside critical infrastructure services like DNS (Route 53), DHCP, and IIS Web Services.

The environment is built to simulate a multi-site corporate infrastructure (Oakmont Chemical) with a focus on security, scalability, and automated governance.

Technical Architectures Demonstrated
1. Hybrid Identity & Governance
Active Directory Domain Services (ADDS): Established a multi-OU structure (Houston, Global Groups) to manage users and computer objects within the oakmont.org forest.

Entra ID Integration: Deployed Microsoft Entra Connect Sync to bridge the on-premises environment with the cloud, enabling seamless identity lifecycle management.

Group Policy Objects (GPO): Implemented security baselines, such as the "Disable Guest" policy, applied to specific OUs to enforce corporate compliance.

2. Infrastructure & Network Services
Cloud DNS Management (AWS Route 53): Configured public DNS records for cthomas.cloud, including CNAME aliases pointing to AWS S3 static website endpoints.

Automated IP Management (DHCP): Configured Windows DHCP scopes with active address pools and policies to automate client networking.

Web Infrastructure (IIS): Deployed and managed an internal corporate intranet (intranet.oakmont.org) using Internet Information Services (IIS).


Lab Evidence & Screenshots
Active Directory & Group Policy
The core of the identity management system, showing the organizational structure and security enforcement.

Figure 1: Active Directory Users and Computers showing the 'Houston' OU structure.
<img width="379" height="266" alt="AD1" src="https://github.com/user-attachments/assets/5dd99d42-bc6d-43ff-abb6-f1bc1e7f1a9f" />


Figure 2: GPO 'Disable Guest' linked and enforced on the Houston OU.
<img width="508" height="341" alt="GPO" src="https://github.com/user-attachments/assets/e24f4e6d-2175-41ad-aff1-7e198914297b" />

Hybrid Cloud Integration (AWS & Entra ID)
Evidence of the bridge between on-premises servers and cloud services.
<img width="493" height="374" alt="EntraConnect" src="https://github.com/user-attachments/assets/dbde8046-a8d0-43b8-bdcc-a69f0f940841" />

Figure 3: Configuration of Microsoft Entra Connect for hybrid identity sync.
<img width="893" height="380" alt="image" src="https://github.com/user-attachments/assets/4b15ad45-18ac-4d6f-ac82-8d88e20caacb" />

Figure 4: Route 53 Hosted Zone management for cthomas.cloud.
<img width="800" height="363" alt="image" src="https://github.com/user-attachments/assets/f2b799c5-dc72-4867-a06e-a97745e1e447" />


Network Services & Internal Portal
The "Oakmont Chemical" intranet and the networking services that power it.

Figure 5: Active DHCP IPv4 scope for the internal network.
<img width="776" height="450" alt="DHCP" src="https://github.com/user-attachments/assets/49b0ea93-9648-4bc5-af34-c36471292cb2" />

Figure 6: The live corporate intranet dashboard featuring safety metrics and resources.
<img width="954" height="429" alt="ActualSite" src="https://github.com/user-attachments/assets/36846c68-d125-4fb9-b8af-6c5094aac5a2" />

Figure 7: IIS Manager overseeing the web server configuration.
<img width="854" height="463" alt="IISWebSite" src="https://github.com/user-attachments/assets/b6866885-c863-48c7-a748-81b8cb8a5c0a" />

Tools & Technologies
Directory Services: Active Directory, Microsoft Entra ID (Azure AD).

Cloud Provider: AWS (Route 53, S3).

Web Server: IIS (Internet Information Services).

Networking: DHCP, DNS (CNAME/SOA Records).

Governance: Group Policy Management (GPMC).
