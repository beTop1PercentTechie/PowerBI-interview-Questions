### 167. What is Row-Level Security (RLS) in Power BI, and how is it implemented?
**Answer.**  
Row-Level Security (RLS) is a feature in Power BI that restricts access to specific rows in a dataset based on the user’s identity. It is implemented by:  
- Defining roles within Power BI Desktop.  
- Creating DAX filter expressions that control data visibility.  
- Assigning users to these roles after publishing the report to the Power BI Service.  
---

### 168. What is Object-Level Security (OLS) in Power BI, and how does it differ from Row-Level Security (RLS)?
**Answer.**  
Object-Level Security (OLS) controls access at the schema level, hiding entire tables or specific columns from users.  
- Unlike RLS, which filters data rows, OLS ensures users don’t see or query specific objects.  
- OLS is configured using external tools like Tabular Editor.  
---

### 169. What roles are available in a Power BI workspace, and what are their permissions?
**Answer.**  
- **Admin:** Full control, including managing access, publishing, and configuring settings.  
- **Member:** Can edit reports, dashboards, and datasets.  
- **Contributor:** Can publish and modify content but cannot manage access.  
- **Viewer:** Read-only access to view content but cannot make changes.  
---

### 170. What are the key differences between Row-Level Security (RLS) and Object-Level Security (OLS)?
**Answer.**

| Feature        | Row-Level Security (RLS)         | Object-Level Security (OLS)      |
|----------------|----------------------------------|----------------------------------|
| Scope          | Filters specific rows in a table | Hides entire tables or columns   |
| Implementation | DAX expressions in roles         | Configured using Tabular Editor  |
| Visibility     | Data visible but filtered        | Objects completely hidden        |
---

### 171. What is Data Loss Prevention (DLP) in Power BI?
**Answer.**  
Data Loss Prevention in Power BI is used to protect sensitive information by:  
- Applying policies to restrict data export, sharing, or embedding.  
- Scanning data for sensitive content using Microsoft Purview integration.  
- Enforcing compliance standards within the organization.  
---

### 172. What are best practices for troubleshooting Power BI Gateway errors?
**Answer.**  
- Restart the On-Premises Data Gateway service.  
- Check firewall and proxy configurations.  
- Ensure the gateway is updated to the latest version.  
- Review Gateway logs for specific error messages in the Event Viewer or Power BI Service diagnostics.  
---

### 173. What is Sensitivity Labeling in Power BI and how does it help?
**Answer.**  
Sensitivity labels classify and protect content by:  
- Assigning labels like "Confidential" or "Highly Confidential" to datasets, reports, and dashboards.  
- Preventing unauthorized sharing or exporting.  
- Integrating with Microsoft Information Protection (MIP) for broader security compliance.  
---

### 174. How does Power BI support Multi-Factor Authentication (MFA)?
**Answer.**  
Power BI leverages Azure Active Directory’s MFA to secure user authentication.  
- Users validate identity through SMS, authenticator apps, or biometrics.  
- Organizations can enforce MFA using Conditional Access Policies, ensuring secure access to reports and datasets.  
---

### 175. How can you restrict data export in Power BI reports?
**Answer.**  
- Disable export options at the tenant or workspace level through admin settings.  
- Implement RLS to limit the data scope available to users.  
- Apply Sensitivity Labels to prevent unauthorized copying, printing, or exporting.  
---

### 176. What is Power BI Data Protection and how does it work?
**Answer.**  
Power BI Data Protection is a combination of tools and policies that:  
- Uses Sensitivity Labels and Data Loss Prevention (DLP) to classify and protect data.  
- Integrates with Microsoft Purview for data governance.  
- Enforces role-based access control and encryption to prevent data leaks.  
---
### 177. What is the difference between tenant-level and workspace-level settings for export control in Power BI?
**Answer.**  
- Tenant-level settings are applied across the entire Power BI environment by the administrator and affect all users and workspaces.  
- Workspace-level settings provide more granular control, allowing specific workspaces to override or follow tenant-level policies.  
---

### 178. Can Object-Level Security (OLS) and Row-Level Security (RLS) be used together in Power BI?
**Answer.**  
Yes, OLS and RLS can be combined.  
- OLS hides entire tables or columns from the data model.  
- RLS filters data within visible tables based on user roles.  
Together, they provide a layered approach to data security.  
---

### 179. How can you monitor security compliance in Power BI?
**Answer.**  
- Use Power BI Activity Logs and Audit Logs to track user activity.  
- Monitor Sensitivity Labels and DLP policy reports in Microsoft Purview.  
- Regularly audit workspace permissions and access levels.  
---

### 180. What is the role of Microsoft Purview in Power BI security?
**Answer.**  
Microsoft Purview provides unified data governance across Power BI by:  
- Classifying sensitive data.  
- Monitoring usage and compliance.  
- Enforcing DLP and sensitivity labeling across cloud and on-prem sources.  
---

### 181. How can you prevent unauthorized report sharing in Power BI?
**Answer.**  
- Use Sensitivity Labels to restrict sharing.  
- Disable "Share" and "Export" options in report settings.  
- Control sharing through Azure AD Conditional Access and Power BI tenant settings.  
---

### 182. How does Power BI Service Principal enhance security and automation?
**Answer.**  
A Service Principal is a security identity used by applications or services to access Power BI resources.  
- Enables secure automation using APIs.  
- Supports role-based access without requiring user credentials.  
- Ideal for enterprise-level deployments and CI/CD pipelines.  
---

### 183. What is the role of workspace-level permissions in securing content in Power BI?
**Answer.**  
Workspace permissions define what users can do within a workspace:  
- Avoid granting Admin access unless necessary.  
- Use Viewer for consumers of reports.  
- Review access regularly to follow the principle of least privilege.  
---

### 184. How do sensitivity labels persist across export and download in Power BI?
**Answer.**  
When a report or dataset is exported to Excel, PDF, or PowerPoint:  
- The sensitivity label is retained in the exported file.  
- Protection policies (like encryption and access restriction) are also applied.  
---

### 185. What is the impact of RLS on report performance in large datasets?
**Answer.**  
RLS may affect performance due to additional filtering logic. Best practices include:  
- Optimizing DAX filter expressions.  
- Using indexed columns in filters.  
- Testing roles with representative data volumes before production.  
---

### 186. How do you manage and deploy RLS/OLS changes across environments (Dev → UAT → Prod)?
**Answer.**  
- Define RLS/OLS in Power BI Desktop or Tabular Editor.  
- Use Deployment Pipelines to move content between environments.  
- Use parameterization and Power BI APIs to automate role assignments and security updates.  
---
### 187. What are Power BI tenant settings, and how do they impact security?
**Answer.**  
Tenant settings are administrative configurations at the organizational level in the Power BI Admin Portal. They control capabilities such as:  
- Export and sharing permissions  
- Content pack publishing  
- Use of custom visuals  
- Integration with external services  
These settings help enforce consistent security and governance policies across the organization.  
---

### 188. How do you audit access and activity in Power BI?
**Answer.**  
Auditing is achieved by:  
- Enabling Microsoft 365 Audit Logs for user activities such as sharing, viewing, and exporting.  
- Accessing Power BI Activity Logs through the Power BI Admin API.  
- Using tools like Microsoft Purview to centralize compliance monitoring.  
---

### 189. What is a Power BI service principal name (SPN), and how is it used in security?
**Answer.**  
A Service Principal Name (SPN) is used to represent a service account in Azure Active Directory. In Power BI:  
- It is used for API access and automation tasks.  
- Grants secure access to datasets without requiring user login credentials.  
- Must be assigned to appropriate workspace roles for scoped access.  
---

### 190. What are Conditional Access policies in Azure AD, and how do they work with Power BI?
**Answer.**  
Conditional Access policies enforce security requirements before granting access. In Power BI, they can:  
- Require Multi-Factor Authentication (MFA)  
- Block access from unmanaged or untrusted devices  
- Limit access based on user location or risk level  
---

### 191. How can you implement least privilege access in Power BI workspaces?
**Answer.**  
- Assign users the minimum role necessary (e.g., Viewer instead of Member).  
- Avoid broad Admin assignments.  
- Use security groups for scalable and auditable access control.  
- Review and update permissions regularly.  
---

### 192. How does Power BI integrate with Microsoft Defender for Cloud Apps (MCAS)?
**Answer.**  
Microsoft Defender for Cloud Apps provides visibility and control over Power BI activity. It can:  
- Detect unusual sharing or download behavior  
- Block risky user actions based on DLP policies  
- Generate alerts for policy violations  
---

### 193. What is the significance of encryption in Power BI data protection?
**Answer.**  
Power BI uses encryption at rest and in transit:  
- At rest: Data stored in Azure is encrypted using Microsoft-managed keys or customer-managed keys (CMK).  
- In transit: All communication is encrypted using HTTPS and TLS protocols.  
This ensures confidentiality and integrity of the data.  
---

### 194. Can users bypass RLS using Power BI export options?
**Answer.**  
No, users cannot bypass RLS.  
- Exported data respects the security filters applied by RLS.  
- However, administrators must ensure no over-permissioned roles or datasets expose broader access.  
---

### 195. What is the role of Azure Active Directory (AAD) groups in Power BI security management?
**Answer.**  
AAD groups simplify access control in Power BI:  
- Assign workspace roles to groups instead of individuals.  
- Automatically manage access when users join or leave departments.  
- Facilitate RLS by mapping AAD group membership in DAX filters.  
---

### 196. What is the difference between Power BI dataset permissions and workspace roles?
**Answer.**  
- Workspace roles define what users can do within a workspace (edit, view, manage).  
- Dataset permissions control who can use a dataset across workspaces.  
Granular dataset permissions can be managed via Build, Read, or Reshare access.  
---
### 197. What are the different types of Sensitivity Labels in Power BI?
**Answer.**  
Labels typically include categories like:  
- Public – No restrictions  
- Internal – Limited sharing  
- Confidential – Controlled access, limited export  
- Highly Confidential – Enforced encryption and strict sharing rules  
Custom labels can be defined using Microsoft Purview and applied in Power BI.  
---

### 198. How does Power BI support secure embedding in external applications?
**Answer.**  
Power BI supports:  
- Embed for your organization: Requires Azure AD authentication.  
- Embed for your customers: Uses service principal or master user account.  
Security must be managed using RLS and token-based authentication (AAD or Azure Power BI Embedded tokens).  
---

### 199. What are potential risks if RLS is not implemented correctly?
**Answer.**  
Incorrect RLS setup can lead to:  
- Unauthorized users accessing sensitive data  
- Business rule violations and data leaks  
- Compliance issues under GDPR, HIPAA, etc.  
Always test roles with actual user accounts before deployment.  
---

### 200. What security concerns exist with using third-party Power BI visuals?
**Answer.**  
Custom or third-party visuals may:  
- Execute external scripts or APIs  
- Transmit data outside Power BI ecosystem  
Mitigation includes:  
- Enabling only certified visuals in tenant settings  
- Reviewing visual source and publisher  
---

### 201. How can you control Power BI sharing outside your organization?
**Answer.**  
- Disable external sharing in tenant settings  
- Use Sensitivity Labels to prevent external export  
- Configure Azure AD B2B settings to whitelist approved external domains  
---

### 202. How does Power BI Service protect reports hosted in the cloud?
**Answer.**  
The Power BI Service ensures:  
- Secure data storage in Azure with encryption  
- Isolation of customer data  
- Compliance with certifications like ISO 27001, SOC 2, and GDPR  
- Access control using Azure AD and RLS/OLS  
---

### 203. What is the difference between Build permission and Read permission on a dataset?
**Answer.**  
- Read: Allows users to view reports created from the dataset  
- Build: Grants ability to create new content (reports/dashboards) using the dataset  
Build permission provides more access and must be given with care.  
---

### 204. How can you revoke user access to reports and dashboards in Power BI?
**Answer.**  
- Remove them from the workspace or group  
- Remove their access from the shared link  
- Adjust dataset or report permissions in the Power BI Service  
- Use audit logs to confirm access revocation  
---

### 205. What are the security implications of using DirectQuery in Power BI?
**Answer.**  
- Queries are executed in real time against the data source  
- User credentials may be passed to the underlying source if configured with Single Sign-On (SSO)  
- Data access must be secured at both Power BI and data source level to prevent leakage  
---

### 206. What is Single Sign-On (SSO) in Power BI gateways, and how does it enhance security?
**Answer.**  
SSO allows users to access data sources via the On-Premises Gateway using their Azure AD credentials.  
- Prevents the need to store or manage credentials in Power BI  
- Enhances security by aligning authentication with organizational identity providers  
- Supports Kerberos and OAuth-based delegation  
---
