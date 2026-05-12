# SolarOne SolarOS Product Plan

## Source Repository Context

SolarOne should be built as a solar-contractor version of the existing OneReq Pro SaaS CRM. The original CRM codebase lives in `mlomas1972/onereqpro-saas` and is already structured as a Next.js, React, TypeScript, Supabase, and Capacitor multi-tenant SaaS platform.

The SolarOne repository should become the destination for the solar-specific version. Because the destination repository is currently empty, this file is the first implementation planning document and should guide the first code migration from the SaaS repo.

## Product Position

SolarOne SolarOS should be positioned as:

> From lead to PTO in one platform.

Do not position this as just another solar CRM. The stronger product category is:

> An AI-powered solar operations, permitting, subcontractor, consultant communication, commission, and contest platform for solar dealers, EPCs, installers, and multi-trade energy contractors.

## Target Customers

Primary initial customer:

- Mid-sized solar EPCs using subcontracted installation crews
- Solar sales organizations needing post-sale project visibility
- Roofing and solar hybrid contractors
- Electrical contractors expanding into solar
- Multi-trade home service companies adding solar divisions

## SaaS CRM Features To Reuse From OneReq Pro

The existing SaaS repo already includes several systems that should be adapted instead of rebuilt from scratch:

- Multi-tenant SaaS structure
- Supabase authentication and tenant scoping
- Role and permission system
- CRM customer management
- Dispatch scheduling
- Quote builder foundation
- Permits and rebates foundation
- Invoicing and payments
- Commission engine foundation
- Team Hub / internal communication foundation
- Customer portal foundation
- Tech app / field app foundation through Capacitor
- File uploads and document attachments
- AI-assisted workflows
- Reporting dashboards
- Payroll / earnings concepts
- Fleet module concepts
- Inventory / purchasing concepts

## SolarOne Core Workflow

SolarOne should track every project through this workflow:

1. Lead
2. Proposal
3. Contract signed
4. Site survey
5. Engineering request
6. Permit draft
7. AHJ submission
8. Corrections required, if applicable
9. Permit approved
10. Utility / interconnection submission
11. Install ready
12. Install scheduled
13. Install completed
14. Inspection scheduled
15. Inspection passed or failed
16. PTO submitted
17. PTO approved
18. Funding received
19. Commission approved
20. Commission paid
21. Warranty / service support

Each stage should include:

- Status
- Assigned owner
- Department owner
- Required documents
- Required checklist items
- Internal notes
- Customer-visible status
- SLA timer
- Automated reminders
- Escalation rules
- AI risk detection
- Audit history

## Major Modules

### 1. Dealer / Sales Organization Portal

Purpose: manage solar dealers, sales companies, reps, managers, and consultant performance.

Required features:

- Dealer onboarding
- Sales rep onboarding
- Rep hierarchy
- Setter / closer structure
- Territory management
- Redline configuration
- Adders system
- Proposal approval workflow
- Financing status visibility
- Contract status tracking
- Project stage tracking
- Commission visibility
- Leaderboards
- Training center
- Marketing material access
- Dealer-specific branding

### 2. EPC Operations Management

Purpose: run the back-office fulfillment workflow from sold project through PTO and funding.

Required features:

- Project pipeline dashboard
- Stage-based workflow engine
- Operations task board
- Assignment by department
- Permit status tracking
- Engineering tracking
- Install scheduling
- Inspection tracking
- PTO tracking
- Funding tracking
- Stalled-job alerts
- Department workload view
- SLA reports
- Manager escalation queue

Departments to support:

- Sales
- Operations
- Site survey
- Engineering
- Permitting
- Utility / interconnection
- Install
- Inspection
- Finance
- Service

### 3. Permit Automation + Tracking Hub

Purpose: make permitting and utility coordination a flagship differentiator.

Permit workflow:

1. Contract approved
2. Site survey complete
3. Engineering requested
4. Permit packet drafted
5. AHJ submission
6. AHJ corrections, if required
7. Resubmission
8. Permit approval
9. Utility submission
10. Inspection scheduled
11. Inspection result
12. PTO package submitted
13. PTO approved

Permit tracking fields:

- AHJ / municipality
- Utility provider
- Permit coordinator
- Engineering provider
- Required forms
- Submission date
- Expected approval date
- Approval date
- Rejection / correction reason
- Resubmission date
- Permit expiration date
- Inspection date
- PTO date

Auto-generated documents:

- Permit applications
- Utility applications
- Interconnection applications
- Scope of work
- Equipment spec sheets
- Placards
- Homeowner signature packets
- Electrical load calculations
- Battery forms
- Engineering packets
- Inspection packets
- PTO submission packets

AHJ database:

- Municipality name
- State / county
- Permit requirements
- Submission method
- Required forms
- Typical turnaround time
- Fees
- Contacts
- Inspection requirements
- Common rejection reasons
- Template packets
- Prior approval notes

AI permit engine:

- Missing data detection
- Form autofill suggestions
- AHJ requirement matching
- Rejection risk prediction
- Correction response drafting
- Equipment compatibility checks
- Permit packet completeness checks
- Utility submission readiness checks

### 4. Solar Consultant Communication Hub

Purpose: replace scattered text messages, calls, email, Slack, and spreadsheets with project-linked communication.

Chat types:

- Project-based chat
- Consultant-to-operations chat
- Dealer channel
- Sales team channel
- Permit department channel
- Engineering channel
- Install channel
- Inspection channel
- Finance / commission channel
- Management announcements

Message features:

- File attachments
- Project tagging
- User mentions
- Task creation from message
- Read receipts
- Urgent flag
- Internal-only notes
- Homeowner-visible messages where permitted
- Searchable message history

AI communication layer:

- Conversation summaries
- Unresolved issue detection
- Automatic task creation
- Urgency scoring
- Stalled communication alerts
- Suggested responses
- Daily digest by role

### 5. Commission Tracking System

Purpose: eliminate commission confusion and pay disputes.

Supported roles:

- Setter
- Closer
- Self-generated rep
- Sales manager
- Dealer owner
- Regional manager
- EPC override
- Recruiter override

Commission components:

- Base commission
- Redline spread
- Adders
- Battery bonus
- Roofing attachment bonus
- MPU / electrical bonus
- Dealer override
- Manager override
- Install bonus
- PTO bonus
- Funding bonus
- Contest bonus
- Chargeback
- Clawback
- Deduction

Configurable trigger points:

- Contract signed
- Permit approval
- Install completion
- Inspection passed
- PTO achieved
- Funding received
- Manual approval

Rep dashboard:

- Pending commissions
- Approved commissions
- Paid commissions
- Projected payout date
- Project status
- Funding status
- Deductions
- Chargebacks
- Bonus progress
- Contest ranking

Finance/admin dashboard:

- Payout approvals
- Funding verification
- Split calculations
- Deductions
- Overrides
- Batch payouts
- Payroll/accounting export

### 6. Contest + Gamification System

Purpose: drive behavior for sales consultants, crews, and operations teams.

Sales contest types:

- Most installs
- Highest kW sold
- Battery attachment rate
- Roofing attachment rate
- Financing conversions
- Referrals
- Self-generated leads

Operational contest types:

- Fastest permit approvals
- Lowest inspection failures
- Fastest PTO
- Best QA scores
- Best review generation

Crew contest types:

- Zero callbacks
- Clean installs
- Production bonuses
- Safety scores
- Photo compliance

Leaderboard views:

- Company-wide
- Branch-wide
- Region-wide
- Team-based
- Individual

Gamification features:

- Points
- Badges
- Streaks
- Playoff brackets
- Weekly winners
- Bonus tracking
- Prize tracking
- Recognition feed posts

### 7. Subcontractor Management

Purpose: manage install partners, electrical partners, roofing partners, and service crews.

Required features:

- Subcontractor profiles
- License tracking
- Insurance tracking
- W9 tracking
- Certification tracking
- Territory assignment
- Crew assignment
- Ratings
- Compliance status
- Install dispatch
- GPS tracking
- Route visibility
- Install photos
- Punch lists
- Material confirmation
- Completion forms
- Milestone payout approvals
- Chargeback tracking

### 8. Solar Proposal Engine

Purpose: evolve the existing quote system into a solar-specific proposal engine.

Required features:

- Utility bill OCR
- kWh usage modeling
- Utility escalation modeling
- Solar offset calculation
- PPA / lease / cash / loan comparison
- Dealer fee handling
- Redline and adder logic
- Battery recommendations
- Roof age logic
- Electrical panel upgrade logic
- Production estimate integration
- Incentive assumptions
- Proposal approval controls

### 9. Homeowner Portal

Purpose: provide project transparency and reduce inbound status calls.

Required features:

- Project tracker
- Upload documents
- View install calendar
- View permit status
- View utility / PTO status
- View financing status
- Message project team
- Referral tracking
- Warranty requests
- Production monitoring link
- Savings tracker

## Recommended Database Additions

Core solar tables:

- solar_projects
- solar_project_stages
- solar_site_surveys
- solar_engineering_requests
- solar_permits
- solar_ahjs
- solar_utility_submissions
- solar_interconnections
- solar_inspections
- solar_pto
- solar_install_assignments
- solar_install_photos
- solar_punch_lists

Dealer / sales tables:

- solar_dealers
- solar_consultants
- solar_rep_hierarchy
- solar_redlines
- solar_adders
- solar_commission_plans
- solar_commissions
- solar_commission_splits
- solar_payout_batches

Communication tables:

- solar_channels
- solar_messages
- solar_message_attachments
- solar_notifications
- solar_tasks

Contest tables:

- solar_contests
- solar_contest_rules
- solar_contest_scores
- solar_contest_prizes
- solar_badges
- solar_leaderboard_snapshots

Subcontractor tables:

- solar_subcontractors
- solar_crews
- solar_crew_members
- solar_compliance_documents
- solar_subcontractor_payouts
- solar_chargebacks

## Recommended Roles

- Super Admin
- EPC Admin
- Operations Manager
- Permit Coordinator
- Utility Coordinator
- Engineering Coordinator
- Sales Manager
- Dealer Admin
- Solar Consultant
- Setter
- Closer
- Installer
- Crew Lead
- Subcontractor Admin
- Finance Manager
- Homeowner

Permissions must be granular and tenant-scoped.

## MVP Build Order

### Phase 1 — Foundation

- Copy/adapt SaaS repo structure into SolarOne
- Confirm environment strategy
- Set up SolarOne branding
- Confirm Supabase project strategy
- Confirm tenant model
- Build solar project schema
- Build role and permission adjustments
- Build project workflow engine

### Phase 2 — Operational MVP

- Solar project dashboard
- Dealer portal
- Consultant dashboard
- Permit tracking hub
- Messaging hub
- Commission engine
- Contest engine
- Basic subcontractor profiles
- Homeowner project tracker

### Phase 3 — Solar Automation

- Permit packet generator
- AHJ database
- Utility submission tracker
- Financing status tracker
- AI missing-document detection
- AI project risk alerts
- Install crew dispatch
- QA photo collection

### Phase 4 — Differentiators

- AI permit generation
- AI communication summaries
- AI contest recommendations
- Battery recommendation logic
- Roofing + solar workflows
- Production monitoring integrations
- Financing integrations
- Accounting exports

## Migration Strategy From OneReq Pro SaaS

1. Do not rebuild from scratch.
2. Start by cloning the architecture from `onereqpro-saas`.
3. Keep the proven multi-tenant, auth, permissions, dispatch, portal, Team Hub, files, and reporting foundations.
4. Replace HVAC / plumbing / electrical-specific workflows with solar-specific project stages.
5. Keep commissions, permits, customer portal, Team Hub, and dispatch concepts, but rename and reshape them for solar.
6. Build database schema before UI.
7. Build workflow engine before dashboards.
8. Build dashboards around the workflow engine, not the other way around.

## Critical Product Rules

- Do not make this a generic CRM.
- Do not overbuild proposal design before operations.
- Permitting, communication, commissions, install coordination, and PTO visibility are the highest-value early features.
- Every job must have a single source of truth.
- Every status change must be timestamped and attributable.
- Every commission calculation must be auditable.
- Every permit and utility submission must have clear ownership.
- Homeowners should see simple project progress, not internal chaos.
- Sales consultants should see enough project visibility to reduce complaints, but not enough admin access to break workflows.

## First Engineering Action Items

1. Pull the `onereqpro-saas` structure as the source architecture.
2. Create SolarOne app branding and route naming.
3. Create the solar project schema.
4. Create the solar workflow stage configuration.
5. Create role mapping for EPC, dealer, consultant, subcontractor, and homeowner access.
6. Build the first dashboard: Solar Projects Pipeline.
7. Build the first operational module: Permit Tracking Hub.
8. Build the first sales module: Consultant Dashboard.
9. Build the first finance module: Commission Tracking.
10. Build the first engagement module: Contests / Leaderboards.
