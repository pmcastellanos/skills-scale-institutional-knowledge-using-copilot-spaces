# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

### Cross-functional Release Coordination
- **DevOps/SRE Engineer**: Validates deployment pipelines, prepares rollback procedures, monitors system during deployment, and ensures observability tooling is ready.
- **Technical Writer**: Finalizes documentation updates, ensures release notes are accurate and user-friendly, and coordinates documentation publication timing.
- **Support Lead**: Reviews release notes for customer impact, prepares support team with training materials, and establishes escalation procedures for release issues.

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] DevOps/SRE Engineer has validated deployment pipeline and rollback plan
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] DevOps/SRE Engineer monitors system health during and after deployment
- [ ] Run post-deploy verifications
- [ ] Technical Writer has published documentation updates
- [ ] Support Lead has briefed support team on changes
- [ ] Announce release to stakeholders and support

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
