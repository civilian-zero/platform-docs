# CLAUDE.md

## Repository Purpose

You are working in the `platform-docs` repository.

This repository is the source of truth for Famm's platform architecture, governance standards, architecture decision records, AI prompts, and implementation guardrails.

Famm is not the platform.

Famm is the first application built on top of a broader multi-tenant relationship-commerce platform.

## Primary Responsibility

Your job in this repository is to help maintain clear, durable, industry-neutral platform documentation.

Do not write application code in this repository.

Do not create product implementation files in this repository.

This repository should contain documentation, governance standards, review prompts, architecture decisions, and operating rules.

## Platform Principle

The platform exists to support relationship-driven commerce across multiple industries.

Fitness is the initial proving ground, but the platform must eventually support:

- Fitness professionals
- Therapists
- Tutors
- Music teachers
- Tattoo artists
- Coaches
- Consultants
- Creators
- Future peer-to-peer industries not yet identified

## Required Context

Before creating or editing architecture documents, review:

- `docs/constitution/PLATFORM_CONSTITUTION.md`
- `docs/standards/DATA_MODEL_RULES.md`
- `docs/standards/API_STANDARDS.md`
- `docs/standards/EVENT_STANDARDS.md`
- `docs/standards/NAMING_CONVENTIONS.md`
- `docs/adr/`
- `.ai/prompts/`

## Documentation Rules

When editing documents in this repository:

1. Preserve industry-neutral platform language.
2. Avoid making Famm-specific assumptions part of the platform core.
3. Distinguish clearly between:
   - Platform Core
   - Application Layer
   - User Experience Layer
   - Infrastructure
4. Prefer platform primitives over vertical-specific entities.
5. Keep documentation actionable for engineers and AI coding tools.
6. Use Markdown formatting consistently.
7. Use concise headings and explicit decision language.
8. Record major architecture decisions as ADRs.

## Platform Primitives

Before introducing a new platform concept, determine whether it can be represented by one of the following primitives:

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

Prefer these primitives unless a new concept is justified by an ADR.

## Naming Rules

In platform-level documentation, prefer industry-neutral names:

- provider
- customer
- activity
- offer
- transaction
- subscription
- entitlement
- organization
- community
- relationship
- referral
- affiliate
- reputation_signal
- conversation
- event

Avoid making these Famm-specific terms part of the platform core:

- trainer
- client
- workout
- gym
- fitness
- session
- package
- membership

These Famm-specific terms may appear only when explaining application-layer mappings.

Example:

- Platform provider = Famm trainer
- Platform customer = Famm client
- Platform activity = Famm session or class
- Platform offer = Famm package or membership

## ADR Rules

When creating or editing ADRs:

1. Use the ADR template in `docs/adr/ADR-TEMPLATE.md`.
2. Use numbered filenames.
3. Use lowercase kebab-case filenames.
4. Include status, date, context, decision, consequences, alternatives, scale impact, and final decision.
5. Make the decision explicit.
6. Explain cross-industry impact.
7. Explain how the decision affects platform primitives.
8. Avoid vague strategy language without an implementation consequence.

ADR filename format:

```text
ADR-001-multi-tenant-strategy.md
ADR-002-relationship-graph-architecture.md
ADR-003-commerce-architecture.md
