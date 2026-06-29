# Data Model Rules

## Rule 1: Prefer Platform Primitives

Before creating a new entity, first map the concept to:

- User
- Organization
- Community
- Relationship
- Activity
- Offer
- Transaction
- Conversation
- Referral
- Affiliate
- Event
- ReputationSignal

## Rule 2: Avoid Fitness-Specific Core Names

Do not use these names in platform-core unless there is a deliberate ADR:

- trainer
- client
- workout
- gym
- class
- session
- package
- membership

Prefer:

- provider
- customer
- activity
- location
- event
- offer
- entitlement
- subscription

## Rule 3: Tenant Ownership Required

Tenant-sensitive records must include one of:

- tenant_id
- organization_id
- account_id

## Rule 4: Time Fields Required

Most records should include:

- created_at
- updated_at

Soft-deletable records should include:

- deleted_at

## Rule 5: Domain Events Required

Material business actions should emit domain events.

Examples:

- user.created
- relationship.created
- offer.created
- transaction.completed
- referral.converted
- activity.booked
- activity.cancelled
- conversation.started
- community.joined

## Rule 6: Application Labels Are Allowed at the Edge

The Famm app may call a provider a “trainer” in the UI.

The platform core should call that same actor a “provider.”
