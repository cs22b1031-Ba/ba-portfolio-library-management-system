# Business Requirements Document

## Project Title
**Library Management System Implementation**

## Document Control

| Item | Details |
|------|---------|
| Document Type | Business Requirements Document (BRD) |
| Prepared By | Business Analyst Portfolio Project |
| Version | 1.0 |
| Date | 06 April 2026 |
| Industry Context | Indian College / Public Library |
| Intended Audience | Client Stakeholders, Library Management, IT Team, Implementation Vendor |

## 1. Executive Summary
The proposed Library Management System (LMS) is intended to help a college or public library move away from manual registers, member cards, and disconnected spreadsheets toward a more reliable and user-friendly digital process. The solution will support day-to-day activities such as catalog management, member management, issue and return, reservations, fine handling, notifications, and reporting through a single centralized platform. From a business perspective, the project is expected to reduce manual effort, improve record accuracy, strengthen operational visibility, and provide a better experience for both library staff and members. It will also create a stronger foundation for future growth, whether that means supporting additional departments, service points, or library branches.

## 2. Project Objectives
- Digitize end-to-end library operations to reduce dependency on manual registers and spreadsheets.
- Improve the accuracy and speed of book issue, return, renewal, and fine management processes.
- Provide members with easy access to catalog search, availability status, and reservation services.
- Strengthen inventory tracking and reporting for better decision-making and audit readiness.
- Enhance service quality for students, faculty, librarians, and public users through a user-friendly system.

## 3. Scope

### In-Scope
1. Member registration and profile management for students, faculty, staff, and external members where applicable.
2. Book catalog creation and maintenance including ISBN, title, author, publisher, subject, and accession number.
3. Book issue, return, renewal, and due-date tracking.
4. Fine calculation based on configurable overdue rules.
5. Reservation and waitlist management for unavailable books.
6. User login and role-based access for librarians, assistants, and members.
7. Standard operational and management reports such as issued books, overdue items, fines collected, and inventory status.
8. Notifications to members for due dates, overdue books, and reservation availability through email, SMS, or internal alerts.

### Out-of-Scope
1. Procurement management for purchasing books from vendors.
2. Full accounting integration with the institution's finance or ERP system.
3. RFID hardware implementation and biometric attendance integration.
4. Management of digital copyrighted content such as licensed e-books and online journals beyond basic catalog reference.

## 4. Stakeholder Table

| Stakeholder | Role | Key Interests | Pain Points |
|-------------|------|---------------|-------------|
| Library Head / Chief Librarian | Project sponsor and decision-maker | Efficient operations, accurate reports, policy enforcement | Limited visibility, manual workload, audit pressure |
| Librarian | Primary system user | Fast issue/return, easy catalog updates, reduced paperwork | Repetitive manual entries, errors in records |
| Library Assistant | Supports daily operations | Simple workflows, quick member lookup, fine handling | Time-consuming searches, queue management |
| Students | Primary borrowers in college context | Easy book search, quick issue/return, reservation alerts | Long queues, unclear availability, missed due dates |
| Faculty Members | High-value library users | Priority access, research support, accurate availability | Difficulty locating books, delayed issue process |
| Public Members / External Readers | Secondary borrowers in public library context | Transparent borrowing rules, smooth registration | Manual forms, slow verification, poor communication |
| College Administration / Municipal Authority | Oversight stakeholder | Compliance, budget utilization, usage trends | Lack of timely MIS reports |
| IT Support Team / Vendor | Technical support and implementation partner | Stable deployment, manageable support, clear requirements | Ambiguous process rules, inconsistent data sources |
| Accounts / Admin Team | Monitors fines and memberships | Accurate fine records, reconciliation support | Manual fine tracking, missing records |
| Audit / Compliance Team | Reviews stock and process compliance | Traceability, inventory history, user accountability | Incomplete logs, hard-to-verify paper records |

## 5. As-Is Process
In the current environment, many college and public libraries in India still rely on manual registers, physical member cards, and Excel sheets maintained separately by different staff members. Members often need to ask at the circulation desk to confirm whether a book is available, and staff then check shelves, accession registers, or spreadsheets before responding. Issue and return transactions are commonly written by hand, which slows down service and makes records harder to track and reconcile. Fine calculation, reservation follow-up, and reporting are also largely manual, creating avoidable pressure on staff and increasing the risk of errors, delays, and member dissatisfaction. During audits or accreditation reviews, this manual dependency can become even more visible because staff must spend extra time pulling information together from multiple sources.

### Current Manual Process
1. Member visits the library and searches physically through shelves or card catalogs.
2. If assistance is needed, the member asks the librarian to check book availability.
3. Librarian verifies the book using accession registers, shelf checks, or Excel files.
4. Member presents ID card or membership card at the circulation desk.
5. Librarian manually records issue details in a register or spreadsheet.
6. Due date is written manually on a slip, stamp, or borrowing card.
7. On return, staff check the issue register to confirm transaction details.
8. Librarian manually calculates overdue days and applicable fine, if any.
9. Fine payment is recorded separately in a register or receipt book.
10. Reservation requests and follow-ups are handled informally through notes or verbal tracking.
11. Monthly reports are compiled manually for management, audit, or accreditation review.

## 6. Pain Points
1. Book availability cannot be checked instantly, resulting in delays for members and staff.
2. Manual issue and return entries increase the likelihood of human error.
3. Overdue fine calculations are inconsistent and may lead to disputes with members.
4. Separate registers and spreadsheets cause duplicate data entry and reconciliation issues.
5. Staff spend excessive time searching for member and book records during peak hours.
6. There is limited visibility into real-time stock status, damaged books, and lost books.
7. Reservation requests are handled informally, leading to poor transparency and missed allocations.
8. Reporting for administration, NAAC/NBA reviews, or municipal audits is time-consuming.
9. Member communication regarding due dates or overdue items is unreliable or absent.
10. Historical transaction tracking is weak, making it difficult to investigate missing or disputed books.

## 7. Functional Requirements

| ID | Functional Requirement |
|----|------------------------|
| FR-01 | The system shall allow authorized staff to create, update, deactivate, and view member profiles. |
| FR-02 | The system shall support different member categories such as student, faculty, staff, and external member. |
| FR-03 | The system shall store member details including name, ID number, department, course, contact details, address, and membership status. |
| FR-04 | The system shall allow authorized users to add, edit, classify, and archive book catalog records. |
| FR-05 | The system shall capture book metadata including title, author, ISBN, edition, publisher, subject, language, and accession number. |
| FR-06 | The system shall maintain copy-level inventory status for each book item, including available, issued, reserved, lost, damaged, or under maintenance. |
| FR-07 | The system shall provide search functionality by title, author, subject, ISBN, accession number, and keywords. |
| FR-08 | The system shall display real-time availability status of each book copy. |
| FR-09 | The system shall allow librarians to issue books to eligible members based on configurable borrowing rules. |
| FR-10 | The system shall validate member eligibility before issue, including active membership, issue limits, and outstanding dues. |
| FR-11 | The system shall generate and store due dates automatically based on member type and item type. |
| FR-12 | The system shall allow book return processing and automatically update inventory status. |
| FR-13 | The system shall calculate overdue fines automatically based on configurable rules and grace periods. |
| FR-14 | The system shall support renewal of issued books subject to policy rules and reservation conflicts. |
| FR-15 | The system shall allow members or staff to place reservations on unavailable books. |
| FR-16 | The system shall manage reservation queues on a first-come, first-served basis or as per configured priority rules. |
| FR-17 | The system shall notify members when a reserved book becomes available for collection. |
| FR-18 | The system shall allow staff to record lost, damaged, or missing books and apply related penalties if required. |
| FR-19 | The system shall maintain a full transaction history of issue, return, renewal, reservation, and fine activities. |
| FR-20 | The system shall provide dashboards and reports for issued books, overdue items, inactive members, fine collections, and stock summary. |
| FR-21 | The system shall support role-based access control for librarian, assistant, administrator, and member roles. |
| FR-22 | The system shall allow authorized users to configure library policies such as borrowing limits, loan periods, fine rates, holidays, and grace periods. |
| FR-23 | The system shall support barcode-based book and member identification to speed up circulation activities. |
| FR-24 | The system shall generate printable or digital acknowledgements for issue, return, and fine payment transactions. |
| FR-25 | The system shall maintain audit logs of key user actions such as record creation, update, deletion, fine override, and policy changes. |

## 8. Non-Functional Requirements

| Category | Requirement |
|----------|-------------|
| Performance | The system shall return search results within 3 seconds for standard catalog searches and complete issue/return transactions within 5 seconds under normal load. |
| Security | The system shall enforce secure login, password protection, role-based authorization, and protection of member personal data in compliance with institutional data handling policies. |
| Usability | The user interface shall be simple and intuitive so that library staff with basic computer knowledge can perform routine operations with minimal training. |
| Availability | The system shall be available at least 99% during library working hours, excluding planned maintenance. |
| Scalability | The system shall support growth in users, transactions, and catalog size without major redesign, including expansion to multiple departments or branches. |
| Maintainability | The solution shall be modular, documented, and easy to configure for policy changes such as fine rules, issue limits, and member categories. |

## 9. To-Be Process
In the proposed future state, core library activities will be managed through a centralized Library Management System that is accessible to authorized staff and, where appropriate, to members as well. Members will be able to search the catalog digitally, check availability in real time, and receive clearer communication around due dates, reservations, and returns. Library staff will be supported by a more structured process for issue, return, renewal, fine handling, and reporting, with fewer manual checks and less duplicate entry. The system will automate routine validations and calculations while still allowing staff to manage exceptions when needed. Overall, the future process is expected to improve turnaround time, strengthen compliance with library policies, and create a more transparent and dependable service model.

### Automated To-Be Process
1. Member searches the catalog using a portal or assisted desk search.
2. System displays matching titles with real-time status, location, and copy availability.
3. Member selects an available book or places a reservation if the item is unavailable.
4. Librarian scans member ID and book barcode to initiate circulation.
5. System validates membership status, borrowing limit, overdue items, and fine rules.
6. System records the issue transaction and generates the due date automatically.
7. Member receives an acknowledgement through print, email, or SMS notification.
8. System sends reminders before the due date and overdue alerts after the due date.
9. On return, librarian scans the book and the system updates inventory instantly.
10. If overdue, the system calculates the fine automatically and records payment if collected.
11. If the item is reserved, the system allocates it to the next member in the queue and sends an alert.
12. Management dashboards and standard reports are generated directly from the system when required.

## 10. Success Metrics

| KPI | Target |
|-----|--------|
| Issue/Return Processing Time | Reduce average circulation transaction time from 3-5 minutes to less than 1 minute. |
| Record Accuracy | Achieve at least 98% accuracy in inventory and circulation records within 3 months of go-live. |
| Overdue Tracking Efficiency | Ensure 95% of overdue items are identified and reported automatically on a daily basis. |
| Member Satisfaction | Achieve at least 85% satisfaction in post-implementation user feedback surveys. |
| Reporting Time Reduction | Reduce time required to prepare monthly management reports by 80%. |
| System Adoption | Achieve 100% staff usage of the system for all circulation transactions within 1 month of deployment. |

## 11. User Stories
1. As a student member, I want to search books by title, author, or subject so that I can quickly find relevant books for my coursework.
2. As a librarian, I want to issue books by scanning barcodes so that I can reduce manual effort and serve members faster.
3. As a faculty member, I want to view book availability before visiting the library so that I can plan my borrowings efficiently.
4. As a library assistant, I want the system to calculate fines automatically so that I can avoid manual errors and disputes.
5. As a student member, I want to receive reminders before the due date so that I can return or renew books on time.
6. As a member, I want to place a reservation on an unavailable book so that I can be notified when it becomes available.
7. As a librarian, I want to see a member's borrowing history so that I can handle queries and exceptions effectively.
8. As a library head, I want monthly reports on issued, overdue, and lost books so that I can monitor library performance.
9. As an administrator, I want to configure borrowing limits and fine rules by member type so that the system aligns with library policy.
10. As an audit stakeholder, I want access to transaction logs and stock records so that I can verify compliance and accountability.

## Assumptions and Dependencies

| Type | Details |
|------|---------|
| Assumption | Library staff and members will have access to basic computing devices and internet connectivity within the library environment. |
| Assumption | Existing book and member records can be cleaned and migrated into the new system before go-live. |
| Assumption | Library policies for borrowing limits, fine rates, and holidays will be finalized before configuration. |
| Dependency | Availability of barcode labels and scanners for faster circulation processing. |
| Dependency | Support from the institution's IT team or vendor for system setup, user access, backup, and maintenance. |
| Dependency | Stakeholder approval of process changes and operating rules before implementation. |

## Conclusion
This BRD captures the business need, project scope, key pain points, future-state process, and detailed requirements for implementing a Library Management System in an Indian college or public library setting. The proposed solution is designed to address practical operational issues around circulation, stock visibility, reporting, and member service while also giving stakeholders a clearer basis for implementation planning and solution discussion. From a business analysis perspective, the document demonstrates how current-state problems can be translated into structured requirements, measurable outcomes, and a realistic target process. As a portfolio project, it is intended to reflect the kind of clear, stakeholder-focused documentation a Business Analyst would prepare in a real client environment.
