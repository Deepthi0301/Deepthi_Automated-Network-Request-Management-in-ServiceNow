# 🌐 Automated Network Request and Management System

## 📌 Overview

The **Automated Network Request and Management System** is a ServiceNow-based application designed to simplify, automate, and manage network service requests within an organization.

The system provides a structured way for users to submit network-related requests through the ServiceNow Service Portal. Requests are automatically processed through predefined workflows, routed to the appropriate teams, tracked throughout their lifecycle, and updated based on their status.

This solution reduces manual effort, improves request visibility, and helps organizations manage network services efficiently.

---

## 🎯 Problem Statement

In traditional network request management, users may submit requests through emails, phone calls, or informal communication channels. This can lead to:

* Delays in processing requests
* Manual assignment of requests
* Lack of request tracking
* Communication gaps between users and network teams
* Difficulty monitoring request status
* Increased chances of errors
* Lack of centralized request information

The proposed ServiceNow application addresses these issues by providing a **centralized and automated network request management system**.

---

## 💡 Solution

The application allows users to submit network service requests through a structured catalog item.

Once a request is submitted:

1. The system captures the request details.
2. A request record is automatically created.
3. The request is routed to the appropriate team.
4. Approval is triggered when required.
5. The assigned team works on the request.
6. Request status is updated throughout the process.
7. Users can track the progress of their requests.
8. The request is closed after successful completion.

---

## 🚀 Key Features

### 👤 User Request Submission

Users can submit network-related requests through the ServiceNow Service Portal.

Examples include:

* New network connection
* Network access request
* Wi-Fi access
* VPN access
* Firewall access
* Network troubleshooting
* Network equipment/service request

### 🔄 Automated Workflow

Requests move automatically through predefined stages such as:

**Submitted → Approval → Assignment → In Progress → Completed → Closed**

This reduces manual intervention and improves processing speed.

### 👥 Automatic Assignment

Requests can be automatically assigned to the appropriate network support group based on request type, priority, or other predefined conditions.

### ✅ Approval Management

Requests requiring authorization can be routed to the appropriate approver before work begins.

### 📊 Request Tracking

Users and administrators can monitor:

* Request number
* Request type
* Requested service
* Priority
* Current status
* Assigned group
* Assigned technician
* Created date
* Completion date

### 🔔 Notifications

Automated notifications can be triggered when:

* A request is submitted
* Approval is required
* A request is approved or rejected
* Assignment changes
* Work begins
* Request is completed
* Request is closed

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │       End User      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ ServiceNow Service  │
                    │       Portal        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │  Network Request    │
                    │   Catalog Item      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Automated Workflow  │
                    └──────────┬──────────┘
                               │
                  ┌────────────┼────────────┐
                  ▼            ▼            ▼
             Approval      Assignment   Notification
                  │            │            │
                  └────────────┼────────────┘
                               ▼
                    ┌─────────────────────┐
                    │ Network Support     │
                    │       Team          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Request Resolution  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     Closure &       │
                    │   Status Update     │
                    └─────────────────────┘
```

---

## 🔄 Request Lifecycle

| Stage                         | User Activity                           | System Response                            |
| ----------------------------- | --------------------------------------- | ------------------------------------------ |
| **1. Request Identification** | User identifies a network requirement   | User accesses ServiceNow Service Portal    |
| **2. Request Submission**     | User opens Network Request catalog item | System displays structured request form    |
| **3. Request Creation**       | User enters required information        | System creates request                     |
| **4. Validation**             | User submits request                    | System validates the entered information   |
| **5. Approval**               | Approver reviews request                | System records approval/rejection          |
| **6. Assignment**             | Request is approved                     | System assigns request to appropriate team |
| **7. Processing**             | Network team works on request           | Status changes to In Progress              |
| **8. Completion**             | Network task is completed               | System updates request                     |
| **9. Closure**                | User/request is confirmed               | Request is closed                          |

---

## 🧩 ServiceNow Components

The project can be implemented using the following ServiceNow components:

### Service Catalog

A **Network Request Catalog Item** provides a standardized interface for users to submit requests.

### Custom Tables

A dedicated table can be used to store network request information.

Example fields:

| Field            | Description                 |
| ---------------- | --------------------------- |
| Request Number   | Unique request identifier   |
| Requested For    | User requesting the service |
| Request Type     | Type of network request     |
| Description      | Details of the requirement  |
| Priority         | Request priority            |
| Location         | Required network location   |
| Status           | Current request state       |
| Assignment Group | Responsible team            |
| Assigned To      | Responsible technician      |
| Approval Status  | Approval state              |
| Created Date     | Request creation date       |
| Completion Date  | Request completion date     |

### Flow Designer

Flow Designer can automate:

* Request creation
* Approval
* Assignment
* Notifications
* Status updates
* Closure

### Service Portal

Provides a user-friendly interface for submitting and tracking requests.

### Notifications

Email or system notifications keep users and support teams informed.

### Reports & Dashboards

Used to monitor request volume, status, priorities, and performance.

---

## 🛠️ Technologies Used

* **ServiceNow**
* **Service Catalog**
* **Service Portal**
* **Flow Designer**
* **Business Rules**
* **Client Scripts**
* **UI Policies**
* **Notifications**
* **Reports & Dashboards**
* **Custom Tables**
* **JavaScript**

---

## 👨‍💻 User Roles

### End User

Can:

* Submit network requests
* View submitted requests
* Track request status
* Receive notifications

### Network Support Team

Can:

* View assigned requests
* Update request status
* Work on network requests
* Add work notes
* Complete requests

### Approver

Can:

* Review requests
* Approve requests
* Reject requests
* Provide approval comments

### Administrator

Can:

* Configure the application
* Manage users and roles
* Configure workflows
* Manage catalog items
* Create reports and dashboards

---

## 🔐 Security

The application uses ServiceNow role-based access control to ensure that users only access information appropriate to their roles.

Security can be implemented using:

* User Roles
* ACLs
* Role-based permissions
* Data access restrictions
* Catalog user criteria

---

## ⭐ Benefits

The application provides several benefits:

* **Reduced manual work** through automation
* **Faster request processing**
* **Centralized request management**
* **Improved visibility and tracking**
* **Better communication**
* **Standardized request submission**
* **Reduced processing errors**
* **Improved accountability**
* **Better reporting and monitoring**

---

## 🔮 Future Enhancements

The application can be extended with:

* Integration with network monitoring systems
* Automated network device provisioning
* REST API integrations
* Real-time network status monitoring
* SLA-based escalation
* Advanced analytics
* Mobile request management
* Automated incident creation for failed requests
* Integration with Configuration Management Database (CMDB)
* AI-assisted request classification and routing

---

## 🎓 Project Objective

The primary objective of this project is to demonstrate how ServiceNow can be used to **digitize, automate, and manage network service requests** using Service Catalog, Flow Designer, notifications, role-based access, and reporting.

The project demonstrates practical implementation of IT Service Management concepts while providing a scalable foundation for enterprise network request management.

---

## 👩‍💻 Author

**Ravipati Sri Sai Deepthi**

Computer Science & Engineering

ServiceNow Certified System Administrator (CSA)

ServiceNow Certified Application Developer (CAD)

---

## 📄 License

This project is created for **educational and portfolio purposes**.
