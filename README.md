IT Knowledge Bot — IT Support Assistant

Project Overview

The IT Knowledge Bot is an IT support assistant built using Microsoft Copilot Studio and Power Platform. It helps employees find approved answers to common IT questions and raise support tickets when further assistance is required.

Technologies Used

- Microsoft Copilot Studio
- Microsoft Dataverse
- Power Automate
- Microsoft Teams
- Power BI

Key Features

- 15 FAQ topics: Covers password resets, account lockouts, VPN connectivity, Outlook, Microsoft Teams, OneDrive, MFA, software installation, printers, phishing, application access, and remote desktop.
- Approved knowledge source: Uses a Dataverse table to maintain approved IT answers.
- Automated ticket creation: Creates IT support tickets through Power Automate when users need further assistance.
- Teams notifications: Notifies the IT support channel about ticket creation.
- Ticket tracking: Stores ticket details, category, user information, status, and ticket number in Dataverse.
- Analytics dashboard: Visualizes ticket categories, knowledge-base answers, handovers, and answer success rate in Power BI.
- User feedback: Enables users to submit reactions to agent responses.

Architecture

1. Employees interact with the Copilot Studio agent.
2. The agent uses approved IT knowledge to answer supported questions.
3. Unresolved questions can be escalated to the ticket creation flow.
4. Power Automate creates a ticket in Dataverse and posts a notification in Microsoft Teams.
5. Power BI displays support and knowledge-base analytics.

Validation

The project was tested using the Copilot Studio test chat. A question about recovering a OneDrive file deleted six months earlier was escalated successfully, creating ticket `IT-0040`. The ticket was verified in Dataverse.

The Power BI report displayed a knowledge-base answer success rate of 71.43% in the tested dataset. This result should be interpreted in the context of the test data and is not a guarantee of production performance.

Repository Contents

- `ITKnowledgeBot_1_0_0_1.zip` — exported Power Platform solution.

Setup Notes

Importing the solution requires a suitable Power Platform environment. Connections, permissions, and environment-specific resources may need to be configured after import. The Power BI report and its data are not included in the exported solution ZIP unless separately provided.

Project Objective

To demonstrate an end-to-end IT support workflow combining conversational AI, approved knowledge, automated ticket creation, notifications, and analytics.


