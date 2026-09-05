# Incident Lifecycle Automation in ServiceNow

## 📌 Project Overview

**Incident Lifecycle Automation in ServiceNow** is a ServiceNow-based project designed to automate and standardize the complete Incident Management lifecycle.

The project demonstrates how an IT incident can be created, classified, investigated, escalated, linked with Change Management, resolved, and converted into a Knowledge Article while maintaining SLA and related-record tracking.

---

## 🎯 Objectives

* Create and classify incidents through Service Operations Workspace.
* Use Knowledge Management to assist in incident resolution.
* Reassign incidents to appropriate support teams.
* Enable Level 2 teams to investigate and resolve incidents.
* Create emergency Change Requests from incidents.
* Create and track child incidents.
* Document incident cause and resolution.
* Generate Knowledge Articles from resolved incidents.
* Monitor SLA and related records.
* Improve collaboration between multiple support teams.

---

## 🛠️ ServiceNow Modules / Features Used

* **Incident Management**
* **Service Operations Workspace**
* **Agent Assist**
* **Knowledge Management**
* **Change Management**
* **Configuration Management Database (CMDB)**
* **Service Catalog / Service Offerings**
* **Task SLAs**
* **Related Lists**
* **Child Incidents**
* **Impersonation**
* **Work Notes & Watch List**

---

## 🔄 Project Workflow

```text
Create Service
      ↓
Create Service Offering
      ↓
Create Incident
      ↓
Classify Incident
      ↓
Agent Assist / Knowledge Assistance
      ↓
Add Watch List & Work Notes
      ↓
Reassign to Network Support
      ↓
Level 2 Investigation
      ↓
Create Emergency Change
      ↓
Create Child Incident
      ↓
Add Probable Cause
      ↓
Add Resolution
      ↓
Resolve Incident
      ↓
Create Knowledge Article
      ↓
Validate SLA & Related Records
```

---

## 📋 Project Implementation

### 1. Create Service

A new service named **Remote Access** is created.

**Configuration:**

* Name: Remote Access
* Operational Status: Operational

---

### 2. Create Service Offering

A service offering named **Corporate VPN** is created under the Remote Access service.

**Configuration:**

* Name: Corporate VPN
* Parent: Remote Access
* Operational Status: Operational

---

### 3. Create Incident

An incident is created from **Service Operations Workspace**.

**Incident Details:**

* **Short Description:** Unable to connect to Corporate VPN from home office
* **Caller:** Michael Hoefer
* **Assignment Group:** Service Desk

---

### 4. Classify Incident

The incident is classified with the required technical and business information.

| Field              | Value           |
| ------------------ | --------------- |
| Channel            | Phone           |
| Category           | Network         |
| Subcategory        | VPN             |
| Urgency            | 2 - Medium      |
| Service            | Remote Access   |
| Service Offering   | Corporate VPN   |
| Configuration Item | ThinkStationS20 |
| Assignment Group   | Service Desk    |

Work notes are added to document the classification and assignment.

---

### 5. Agent Assist & Knowledge Management

**Agent Assist** is used to find relevant Knowledge Articles based on the incident description.

The process includes:

* Open Agent Assist.
* Select Knowledge Articles.
* Review suggested articles.
* Open a relevant article.
* Mark the article as **Helpful**.
* Attach the article to the incident.
* Add a comment explaining how the article can help resolve the issue.

This demonstrates the integration between **Incident Management and Knowledge Management**.

---

### 6. Watch List & Work Notes

Additional users are added to ensure proper communication and tracking.

* **Watch List:** Samantha Bordwell
* **Work Notes List:** Beth Anglin

This allows stakeholders to monitor incident updates and resolution activities.

---

### 7. Reassignment & Escalation

The incident is escalated from the **Service Desk** to the **Network** support team.

```text
Service Desk
     ↓
Network Support
     ↓
Level 2 Investigation
```

The assignment group is changed to **Network**, and the assigned user is cleared automatically.

---

### 8. Level 2 Investigation

The incident is reviewed by a Network team member.

The following are verified:

* Incident description
* Knowledge Articles
* SLA information
* Related records
* Incident assignment

This demonstrates multi-team collaboration during incident resolution.

---

### 9. Emergency Change Request

During investigation, the Configuration Item is updated from the original system to **PowerEdge**.

The incident is then placed on hold:

* **State:** On Hold
* **On Hold Reason:** Awaiting Change

An emergency Change Request is created and linked to the incident to support the required corrective action.

---

### 10. Child Incident Creation

A child incident is created from the parent incident using the **Related Records** section.

**Child Incident:**

* **Short Description:** Unable to connect to Corporate VPN
* **Description:** User receiving VPN authentication failure error

The child incident number is recorded and verified from the parent incident's related records.

---

### 11. Incident Cause

The probable cause is documented:

> PowerEdge service was suspended and required restart.

Recording the cause provides a clear explanation of why the incident occurred.

---

### 12. Incident Resolution

The resolution details are documented.

**Resolution Code:** Workaround provided

**Resolution Notes:**

> Restarted VPN-SRV-02 service as per emergency change request.

The incident is then marked as **Resolved**.

---

### 13. Knowledge Article Creation

After resolving the incident, a Knowledge Article is created from the incident.

**Configuration:**

* **Knowledge Base:** IT
* **Article Template:** Standard

The incident details are reviewed and saved.

The created Knowledge Article is then verified under the incident's **Related Records**.

---

## ✅ Final Validation

The complete incident lifecycle is validated by checking:

* [x] Parent incident is Resolved
* [x] Child incident is Resolved
* [x] Incident activity contains resolution updates
* [x] Change Request is linked
* [x] Knowledge Article is created
* [x] SLA tracking is visible
* [x] Related records are available
* [x] Incident escalation is completed
* [x] Multi-team collaboration is demonstrated

---

## 👥 Stakeholders

| Stakeholder            | Role                            | Expected Benefit                            |
| ---------------------- | ------------------------------- | ------------------------------------------- |
| End Users              | Report IT issues                | Faster resolution and visibility            |
| Service Desk Agents    | First-level support             | Standardized incident intake and escalation |
| Level 2 Support        | Diagnose and resolve issues     | Better technical investigation              |
| Change Management Team | Handle emergency changes        | Structured change control                   |
| ServiceNow Admin       | Maintain platform configuration | Controlled and scalable processes           |

---

## 🧪 Testing

The project validates the following end-to-end scenarios:

* Incident creation
* Incident classification
* Knowledge assistance
* Incident reassignment
* Level 2 investigation
* Emergency Change integration
* Child Incident management
* Incident cause documentation
* Incident resolution
* Knowledge Article creation
* SLA tracking
* Related record validation
* Multi-team collaboration

---

## 📊 Key Outcomes

The implementation demonstrates how ServiceNow can provide a structured workflow for handling IT incidents from initial reporting through final resolution.

### Benefits

* **Faster incident resolution**
* **Standardized incident management**
* **Better escalation process**
* **Integrated Change Management**
* **Knowledge reuse**
* **Improved SLA visibility**
* **Better collaboration between support teams**
* **Complete incident traceability**

---

## 🏁 Conclusion

This project demonstrates a complete **Incident Management lifecycle in ServiceNow**.

The workflow integrates **Incident, Knowledge, Change, CMDB, SLA, and related-record capabilities** to provide a structured approach to IT issue management.

By automating and standardizing the incident lifecycle, organizations can improve resolution efficiency, maintain better documentation, support SLA compliance, and provide improved IT service delivery.

---

## 👩‍💻 Project Information

**Project:** Incident Lifecycle Automation in ServiceNow
**Platform:** ServiceNow
**Primary Module:** Incident Management
**Focus Areas:** Incident Management, Knowledge Management, Change Management, SLA, CMDB
**Project Type:** ServiceNow ITSM Project
