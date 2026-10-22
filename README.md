
# TestPilot

![Status: Planning](https://img.shields.io/badge/status-planning-blue)
![License: Apache-2.0](https://img.shields.io/badge/license-Apache--2.0-blue)

**An open-source platform for managing Android and iOS testing campaigns, collecting genuine feedback, and preparing apps for release.**

TestPilot helps Android and iOS developers organize testing before release. It brings campaigns, tester onboarding, testing tasks, feedback, and bug tracking into one workspace so developers can understand what has been tested, what needs fixing, and how prepared their app is for production. The initial focus is mobile apps, with testing support for web, Windows, macOS, and Linux applications planned for the future.

## Why TestPilot?

Running a closed test involves more than sharing an installation link. Developers need to coordinate testers, explain what to test, follow up on participation, collect useful feedback, and turn reported problems into improvements.

When this information is scattered across messages, spreadsheets, and separate tools, it becomes difficult to follow progress or explain what was learned during testing. TestPilot aims to make that process clear, organized, and repeatable.

## Project goal

The main goal is to help developers run meaningful testing campaigns that improve app quality and produce a clear record of testing activity and outcomes.

The Android campaign plan includes a target of **12 testers over 14 continuous days**. This is a planning target, not a statement that every Google Play account has the same requirements. Developers must confirm the requirements applicable to their app in Play Console. This target does not apply to iOS campaigns, which will have their own onboarding instructions and testing goals.

## Platform roadmap

| Phase | Applications to be tested | Scope |
| --- | --- | --- |
| Initial focus | Android and iOS | Mobile testing campaigns, tester onboarding, tasks, feedback, bug tracking, and readiness reports. |
| Future expansion | Web, Windows, macOS, and Linux | Extend the shared testing workflow with platform-specific access instructions and issue details. |

These platforms describe the applications managed through TestPilot. The planned TestPilot management interface is a responsive web application; native TestPilot clients are not specified in this roadmap.

TestPilot aims to help developers:

- Organize projects and closed testing campaigns in one place.
- Invite testers and guide them through onboarding.
- Assign practical tasks that encourage real use of the app.
- Track reported participation and identify gaps that need follow-up.
- Collect structured feedback and reproducible bug reports.
- Manage issues and document improvements made during testing.
- Prepare readiness reports summarizing participation, feedback, and unresolved issues.

## Who is it for?

- **Independent Android and iOS developers** coordinating their testing campaigns.
- **Web and desktop developers** as support expands to web, Windows, macOS, and Linux applications.
- **Small development teams** managing testers, feedback, and release preparation together.
- **Testers** who need a simple, mobile-friendly way to access tasks and report their experience.
- **Platform administrators** managing the TestPilot service and user access.

## Planned MVP

The first release will focus on the complete workflow from creating a campaign to reviewing its results.

| Area | Planned functionality |
| --- | --- |
| Accounts and access | Authentication and role-based access for project owners, team members, testers, and administrators. |
| Projects and campaigns | Create Android and iOS projects, configure platform-specific campaigns, and view campaign progress. |
| Tester onboarding | Invite testers and share platform-specific access instructions, including Google Play testing links or iOS TestFlight invitation links supplied by the developer. Record self-reported enrollment where applicable. |
| Testing tasks | Assign testing activities and record completion and participation. |
| Feedback and bugs | Submit structured feedback and bug reports, with reproduction details. |
| Issue management | Review reports, prioritize problems, and track their resolution. |
| Readiness reports | Summarize campaign activity, tester feedback, fixes, and remaining issues. |

The developer experience will center on a dashboard, campaign details, a feedback inbox, and a campaign creation flow. Testers will use a responsive portal designed for mobile devices.

## Example workflow

1. A developer creates a project for their Android or iOS app.
2. They create a testing campaign and add onboarding instructions and testing tasks.
3. Testers accept invitations, follow the Android or iOS access instructions, and report their enrollment where applicable.
4. Testers try the app, complete tasks, and submit feedback or bug reports.
5. The developer reviews participation, follows up with testers, and resolves issues.
6. TestPilot summarizes the campaign results in a readiness report to support the developer's release preparation in Google Play Console or App Store Connect.

## Product principles

- **Genuine feedback:** Encourage useful testing and actionable reports.
- **Honest progress reporting:** Distinguish self-reported participation from independently confirmed information.
- **Privacy:** Limit access to tester information and handle personal data carefully.
- **Accessible design:** Provide clear navigation, accessible components, and responsive layouts.
- **Focused scope:** Deliver a usable testing workflow before adding advanced integrations.

TestPilot is an independent project and is not affiliated with Google or Apple. It does not replace Google Play Console, App Store Connect, or TestFlight, independently certify tester eligibility, or guarantee production access or store approval. Tester enrollment will be treated as self-reported unless separately confirmed through an authoritative source. Readiness reports summarize project evidence; they do not represent Google or Apple approval.

## Planned technology stack

| Layer | Technology |
| --- | --- |
| Frontend | Next.js App Router, React, and TypeScript |
| Interface | Tailwind CSS, shadcn/ui, and Lucide icons |
| Backend | NestJS with TypeScript |
| Database | PostgreSQL |
| Forms and validation | React Hook Form and Zod |
| Charts | Recharts |

The frontend will communicate with a dedicated NestJS API. NestJS will handle business logic, authentication, authorization, and access to PostgreSQL. The database access library and migration tooling will be selected during implementation.

The planned interface includes project switching, a collapsible sidebar, and light and dark themes. Initial screens will use mock data before integration with the NestJS backend.

## Future directions

The long-term goal is to support testing across mobile, web, and desktop applications. After establishing the Android and iOS workflow, TestPilot will expand to web, Windows, macOS, and Linux, adapting campaign instructions and bug-report context to each platform.

After the core workflow is usable, the project will explore integrations with Google Play Console, Firebase, Firebase Cloud Messaging (FCM), Google Cloud, Sentry, and app activity reporting. Each integration will depend on available APIs, permissions, and a clear use case. These are planned directions, not implemented capabilities.

Direct integrations with App Store Connect and TestFlight may also be explored. The initial iOS workflow will use developer-provided links and instructions without assuming automated access to Apple services.

## Current status

TestPilot is in the planning and design stage. This README describes the intended product. No application code or setup instructions have been published yet.

The next milestones are:

- [ ] Finalize the Android and iOS MVP user flows and data model.
- [ ] Build the application layout and navigation.
- [ ] Implement campaign details and the developer dashboard.
- [ ] Build the tester portal and feedback inbox.
- [ ] Add campaign creation, authentication, and role-based access.
- [ ] Build the NestJS API, define the PostgreSQL schema and migrations, and implement the core testing workflow.
- [ ] Connect the Next.js frontend to the NestJS API.
- [ ] Add readiness reporting and validate the workflow with a pilot campaign.
- [ ] Document installation, configuration, and testing instructions.
- [ ] After the mobile MVP, plan and implement support for web, Windows, macOS, and Linux applications.

## Contributing

Contributions to product design, documentation, and early feedback are welcome. Open an issue to propose an improvement or discuss the roadmap. Code contributions will open up once the initial architecture is in place.

## License

TestPilot is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0) (SPDX identifier: `Apache-2.0`).

All product names and trademarks belong to their respective owners.