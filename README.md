# MoniThor: A Monitoring Solution for Message Delivery

## Introduction

MoniThor is a cutting-edge monitoring solution designed to provide accurate and timely information about the delivery status of messages triggered by CEE. In cases of delivery failures, customizable notifications will alert stakeholders, ensuring swift remediation. MoniThor's MVP phase focuses on monitoring real-time C86 intents, providing near-real-time failure notifications.

---

## What's Changing

This is a new product for monitoring delivery status (success/failure) of Canadian alerts. It introduces:

- **Unified Monitoring**: A single source of truth for message delivery.
- **Timely Notifications**: Near-real-time alerts for non-compliance-approved delivery failures.
- **Incremental Coverage**: Starting with real-time digital alerts from Hermes, aiming for full coverage of all Canadian Lines of Business (LOB) messages, including digital, statements, and letters.

---

## Diagrams
- **Deployment**
  ![image](https://github.com/user-attachments/assets/d21b895f-b298-406c-81c8-8393f4cc20f5)


---

## Related Repositories
### Testing Repositories
- **[mocks](www.example.com)**
- **[integration tests](www.example.com)**
- **[ATDD tests](www.example.com)**
- **[smoke tests](www.example.com)**

### AWS Repositories
- **[Security Group](www.example.com)**
- **[IAM](www.example.com)**
- **[Shared infrastructure repo](www.example.com)**
- **[Proxy Repo](www.example.com)**
- **[s3-bucket-repo](www.example.com)**
- **[datastore repo](www.example.com)**
  
### Operational Repositories
- **[trex repo](www.example.com)**
- **[utilities repo](www.example.com)**
- **[tools repo](www.example.com)**

---

## Related Content
### Developer Links
- **[Slack Channel](www.example.com)**
- **[Jira Board](www.example.com)**
- **[Jenkins](www.example.com)**
- **[Sonar](www.example.com)**
- **[Checkmarx](www.example.com)**
- **[Artifactory: artifact ID, path](www.example.com)**

### Other Documentation
- **[Confluence docs](www.example.com)**
- **[Github Pages](www.example.com)**
- **[Architectural Diagrams](www.example.com)**

### Operational Links
- **[runbooks](www.example.com)**
- **[pagerduty](www.example.com)**
- **[Splunk](www.example.com)**
- **[new relic](www.example.com)**
- **[dashboards](www.example.com)**

---
## Noteworthy
## Jenkins
This is built using Managed Pipeline
- **[Build](www.example.com)**
- **[Release](www.example.com)**
- **[Destroy](www.example.com)**

---
## External Dependencies
**DevExchange**

---

## Rationale

### Current Gaps:

- **No Unified Monitoring**: Fragmented monitoring by intent owners leads to inefficiency.
- **Unclear Failure Codes**: Lack of plain language explanations for failure codes.
- **Delayed Failure Discovery**: Failures discovered days later, delaying remediation.

### Impact:

- Increased customer frustration.
- Erosion of trust in message delivery reliability.
- Delays in identifying and addressing root causes.

---

## Role of MoniThor

- **Unified Monitoring**: A comprehensive system to track message delivery status.
- **Timely Alerting**: Real-time notifications for failures based on compliance-approved definitions.
- **Quicker Remediation**: Plain language failure notifications to facilitate swift action.

---

## Expected Results

| **Metric**                   | **Target**                            | **Frequency**         |
| ---------------------------- | ------------------------------------- | --------------------- |
| **Unalerted Failures**       | 0 unalerted failures for C86 messages | Always on post-launch |
| **Notification Timing**      | Notifications sent within 15 minutes  | Always on post-launch |
| **Reduction in Risk Events** | Decrease compared to prior quarters   | Quarterly             |
| **Stakeholder Satisfaction** | Improved satisfaction and confidence  | Monthly/Quarterly     |

---

## MVP Scope

- **In Scope**:

  - Near real-time failure alerting for C86 real-time campaigns.
  - Notifications for failures between Gumbo and Vendor, and Vendor to Customer.
  - Email template with campaign type, timestamp, account ID, error code, and plain language explanation link.

- **Out of Scope**:

  - Batch C86 alerts.
  - UI for notification customization or thresholding.
  - Monitoring for Hermes or Maestro stage failures.

### Personas

| **Persona**         | **Description**                                    | **Needs**                                                                |
| ------------------- | -------------------------------------------------- | ------------------------------------------------------------------------ |
| **Intent Owner**    | Owns the content and delivery of messages.         | Reliable delivery and failure insights for swift remediation.            |
| **Studio X Team**   | Manages message delivery funnel.                   | Real-time alerts and failure insights for investigation and remediation. |
| **Product Manager** | Oversees the technical delivery process.           | Trends in delivery rates and insights into key issues.                   |
| **CEE Leadership**  | Ensures successful delivery of all communications. | Trends, key risk areas, and awareness of major breakdowns.               |

---

## Requirements for MVP

### Functional Requirements

- Failure notifications sent within 15 minutes of failure detection.
- Alerts for all codes classified as "Failed to Send" or "Not Yet Reviewed."
- Vendor failure notifications include vendor error messages in plain language.
- Capability to send up to 50 notifications per second.

### Non-Functional Requirements

- **Performance**: Handle up to 50 notifications/second; maximum delay of 1 hour.
- **Reliability**: Less than 5% downtime.
- **Scalability**: Expandable to support all Canadian messages.

---

## How to Measure Success

- **Accuracy**: Compare detected failures with manual script findings.
- **Notification Speed**: Monitor time taken for alerts to reach stakeholders.
- **Risk Event Reduction**: Compare risk events to prior quarters.
- **User Feedback**: Regular surveys and interviews to assess satisfaction.

---

## Contact

For questions , please reach out to the MoniThor development team at [StudioX@capitalone.com](mailto:StudioX@capitalone.com).

---

MoniThor: Ensuring reliable and compliant message delivery for Canadian LOBs.
