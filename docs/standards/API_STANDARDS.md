# API Standards

## API Design Principle

APIs should represent reusable platform capabilities, not single-screen workflows.

Avoid:

POST /trainer-dashboard/create-session-card

Prefer:

POST /activities
POST /offers
POST /bookings

## Command Pattern

Commands change state.

Examples:

- CreateUser
- CreateRelationship
- CreateOffer
- BookActivity
- CancelActivity
- CreateReferral
- RedeemOffer

## Query Pattern

Queries read state.

Examples:

- GetUser
- ListRelationships
- ListAvailableActivities
- ListOffers
- GetTransactionHistory
- ListCommunityMembers

## Domain Events

Events describe something that already happened.

Examples:

- user.created
- relationship.created
- offer.created
- activity.booked
- transaction.completed
- referral.converted

## API Requirements

Each API should define:

- Purpose
- Request body
- Response body
- Permissions
- Domain events emitted
- Error states
- Audit requirements
