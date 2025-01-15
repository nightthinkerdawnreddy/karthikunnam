# MoniThor - Monitoring Delivery Failures for Canadian Alerts

## Getting Started
MoniThor is a monitoring solution designed to provide stakeholders with accurate and timely information regarding the delivery status of messages triggered by the Canadian Enterprise Engine (CEE). The solution focuses on delivering failure notifications in near-real time, enabling quick remediation of delivery issues.

## Key Features
- **Unified Monitoring**: A single source of truth for monitoring message delivery.
- **Real-Time Notifications**: Alerts sent within 15 minutes of identifying failures, supporting up to 50 notifications per second.
- **Incremental Coverage**: Starting with Hermes-triggered real-time C86 alerts, with plans to expand to all Canadian LOB messages.

## Installation
Follow these steps to set up MoniThor:

1. Clone the repository:
   ```bash
   git clone [repository-url]
   ```

2. Install dependencies:
   ```bash
   npm install # or appropriate package manager
   ```

3. Configure the environment variables in the `.env` file.

4. Start the application:
   ```bash
   npm start
   ```

## Usage
- Monitor real-time C86 intent failures via email notifications.
- Receive alerts for failure codes such as "Failed to Send" and "Not Yet Reviewed."
- Use the notifications to understand failure codes and timestamps.

## Contributing
We welcome contributions! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`feature/your-feature-name`).
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Create a Pull Request.

## Maintainers
This project is maintained by the **Studio X team** and **CEE Product Managers**. For questions, please reach out directly.

## Diagrams
### System Architecture:
*(Add system architecture diagram here)*

### Alert Flow:
*(Add alert flow diagram here)*

## Related Repositories
- **Repository 1**
- **Repository 2**

## Related Content
- Canadian Enterprise Engine Documentation
- Hermes Alerting System

## Noteworthy
### Current Challenges:
- Lack of Centralized Monitoring: No unified system exists for tracking delivery success and failures.
- Unclear Failure Codes: Existing codes lack plain-language descriptions, complicating remediation.
- Delayed Discovery: Manual processes delay identification of failures.
- Customer Impact: Delivery delays harm satisfaction and increase regulatory risks.

### MoniThor's Solution:
- **Real-Time Alerting**: Near-real-time notifications for stakeholders.
- **Root Cause Analysis**: Plain-language descriptions of failure codes.
- **Unified Understanding**: Standardized failure definitions.

## MVP Scope
### In Scope:
- Real-time alerting for C86 email failures triggered by Hermes.
- Notifications for specific failure codes ("Failed to Send" and "Not Yet Reviewed").
- Emails containing failure codes, timestamps, and plain-language descriptions.

### Out of Scope:
- Batch C86 messages or other Hermes campaigns.
- Failures at Hermes or Maestro stages.
- UI or customization for alerts.

## Expected Results
| Objective              | Metrics                                      | Frequency          |
|------------------------|----------------------------------------------|--------------------|
| No unalerted failures | All failures detected and alerted within 15 minutes. | Always on post-launch |
| Quicker remediation   | Notifications sent within 15 minutes of failures. | Always on post-launch |
| Reduced risk events   | Fewer delivery-related risk events.           | Quarterly          |
| Stakeholder satisfaction | Improved confidence in reliability.         | Immediate, then quarterly |

## Timelines
| Milestone          | Description                                      | Deadline          |
|--------------------|--------------------------------------------------|-------------------|
| Foundational Tech  | Enable message delivery outcome tracking through Maestro. | Sept 28, 2024    |
| MVP Release        | Provide near-real-time alerting for real-time C86 failures. | Oct 28, 2024     |

## How to Measure Success
- **Validation**: Manual scripts will verify failure detection post-launch.
- **Stakeholder Feedback**: Guides adjustments for future enhancements.
- **Metrics**:
  - Notifications sent within 15 minutes of failure detection.
  - Reduced delivery failure-related risk events.

## Future Enhancements
- Support for additional Hermes-triggered campaigns.
- Customizable alerting thresholds for stakeholders.
- UI for easier monitoring and customization.

## Contact Information
For more information, feedback, or contributions:

- **Studio X team**
- **CEE Product Managers**

## License
This project is licensed under [Your License Name].
