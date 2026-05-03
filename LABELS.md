# GitHub Labels & Organization Guide

**Professional labeling system for FlashFix SaaS project**

---

## 📋 Issue Labels

### Priority Labels
- **🔴 priority/critical** — Blocks release or customer-facing functionality
- **🟠 priority/high** — Important feature or bug affecting core workflow
- **🟡 priority/medium** — Standard feature or improvement
- **🟢 priority/low** — Nice-to-have or documentation

### Type Labels
- **type/bug** — Defect in existing functionality
- **type/feature** — New feature or capability
- **type/enhancement** — Improvement to existing feature
- **type/documentation** — Documentation, guides, or README updates
- **type/refactor** — Code cleanup or technical debt
- **type/chore** — Maintenance tasks, dependencies, infrastructure

### Status Labels
- **status/backlog** — Not yet started or prioritized
- **status/in-progress** — Actively being worked on
- **status/review** — Awaiting code review or feedback
- **status/blocked** — Waiting on external dependency or decision
- **status/done** — Completed and merged

### Component Labels
- **component/frontend** — React, UI, client-side code
- **component/backend** — tRPC, Express, server-side code
- **component/database** — Schema, migrations, queries
- **component/auth** — Authentication and authorization
- **component/api** — API design and endpoints
- **component/infrastructure** — Deployment, hosting, DevOps
- **component/mobile** — Mobile app or responsive design

### Feature Area Labels
- **feature/quote-builder** — Quote generation and management
- **feature/job-tracking** — Job tracking and task management
- **feature/admin-portal** — Admin dashboard and controls
- **feature/pm-portal** — Property manager portal
- **feature/contractor-portal** — Contractor mobile app
- **feature/analytics** — Analytics and reporting
- **feature/payments** — Payment processing and billing
- **feature/marketplace** — Contractor marketplace

### Team Labels
- **team/product** — Product and design decisions
- **team/engineering** — Engineering and technical implementation
- **team/sales** — Sales and customer success
- **team/operations** — Operations and infrastructure

---

## 🏷️ Pull Request Labels

### Review Status
- **review/ready** — Ready for code review
- **review/in-progress** — Currently being reviewed
- **review/approved** — Approved, ready to merge
- **review/changes-requested** — Changes needed before merge

### Merge Strategy
- **merge/squash** — Squash commits on merge
- **merge/rebase** — Rebase and merge
- **merge/create-merge-commit** — Create merge commit

### Release Labels
- **release/patch** — Patch version bump (v1.0.x)
- **release/minor** — Minor version bump (v1.x.0)
- **release/major** — Major version bump (vx.0.0)

---

## 📑 Milestone Labels

### Development Phases
- **milestone/mvp** — MVP feature set
- **milestone/beta** — Beta launch features
- **milestone/v1.0** — Version 1.0 release
- **milestone/v2.0** — Version 2.0 release

### Business Phases
- **milestone/pre-launch** — Before public launch
- **milestone/launch** — Public launch phase
- **milestone/growth** — Growth and scaling phase
- **milestone/profitability** — Path to profitability

---

## 🎯 Project Board Columns

### Development Workflow
1. **Backlog** — Issues not yet prioritized
2. **Ready** — Issues ready to start (groomed and estimated)
3. **In Progress** — Actively being worked on
4. **In Review** — Awaiting code review
5. **Testing** — QA and testing phase
6. **Done** — Completed and deployed

### Investor Presentation
1. **Backlog** — Presentation ideas and content
2. **Content Draft** — Initial content written
3. **Design** — Visual design and styling
4. **Review** — Stakeholder review
5. **Final** — Ready for presentation

---

## 📊 Issue Template Labels

### Bug Report
```
- type/bug
- priority/[critical|high|medium|low]
- component/[frontend|backend|database|etc]
- status/backlog
```

### Feature Request
```
- type/feature
- priority/[critical|high|medium|low]
- feature/[quote-builder|job-tracking|etc]
- status/backlog
```

### Documentation
```
- type/documentation
- priority/[high|medium|low]
- status/backlog
```

---

## 🔄 Workflow Examples

### Bug Fix Workflow
1. Create issue with labels: `type/bug`, `priority/high`, `component/frontend`
2. Move to `status/in-progress` when starting work
3. Create PR with label: `review/ready`
4. Move to `status/review` when PR created
5. Update to `review/approved` when approved
6. Merge and close issue with label: `status/done`

### Feature Development Workflow
1. Create issue with labels: `type/feature`, `priority/medium`, `feature/quote-builder`
2. Move to `status/backlog` for prioritization
3. Move to `status/in-progress` when starting work
4. Create PR with label: `review/ready`
5. Move to `status/review` when PR created
6. Update to `review/approved` when approved
7. Merge and close issue with label: `status/done`

### Release Workflow
1. Create milestone: `milestone/v1.0`
2. Add issues to milestone
3. Track progress through project board
4. When complete, create release with label: `release/minor`
5. Tag commit: `v1.0.0`

---

## 📝 Commit Message Labels

### Commit Prefix Convention
```
<type>(<scope>): <subject>

<body>

<footer>
```

**Type:**
- `feat` — New feature
- `fix` — Bug fix
- `docs` — Documentation
- `style` — Code style (formatting, semicolons, etc)
- `refactor` — Code refactoring
- `perf` — Performance improvement
- `test` — Test addition or update
- `chore` — Build, dependency, or infrastructure

**Scope:**
- `quote-builder` — Quote builder feature
- `job-tracking` — Job tracking feature
- `admin-portal` — Admin portal
- `pm-portal` — Property manager portal
- `contractor-portal` — Contractor portal
- `api` — API changes
- `db` — Database changes
- `auth` — Authentication changes
- `ui` — UI/styling changes

**Examples:**
```
feat(quote-builder): Add service category filtering

fix(job-tracking): Correct task completion timestamp

docs(readme): Update installation instructions

refactor(api): Simplify quote calculation logic

perf(frontend): Optimize component re-renders

test(auth): Add login flow unit tests

chore(deps): Update React to v19.2.1
```

---

## 🚀 Release Labeling

### Release Checklist
- [ ] All issues closed and labeled `status/done`
- [ ] All PRs merged and labeled `review/approved`
- [ ] Version bumped (patch/minor/major)
- [ ] Changelog updated
- [ ] Release notes written
- [ ] Tag created: `v{version}`
- [ ] GitHub release published
- [ ] Announcement posted

### Release Label Format
```
Release v1.0.0 — Investor Presentation Ready

## Features
- 12-slide professional investor deck
- Technical blueprint design system
- Comprehensive documentation

## Bug Fixes
- [List any critical fixes]

## Breaking Changes
- [List any breaking changes]

## Contributors
- [List contributors]
```

---

## 📌 Best Practices

1. **Always Label Issues:** Every issue should have at least `type/*` and `priority/*` labels
2. **Use Consistent Naming:** Follow the label naming convention across all projects
3. **Update Status Regularly:** Keep `status/*` labels current as work progresses
4. **Link Related Issues:** Use issue references (#123) to link related work
5. **Review Before Merge:** All PRs should have `review/approved` before merging
6. **Tag Releases:** Always tag releases with semantic versioning (v1.0.0)
7. **Document Decisions:** Use issue comments to document decisions and rationale

---

## 🔗 Related Resources

- [GitHub Labels Documentation](https://docs.github.com/en/issues/using-labels-and-milestones-to-track-work)
- [Semantic Versioning](https://semver.org/)
- [Conventional Commits](https://www.conventionalcommits.org/)

---

**Last Updated:** March 24, 2026  
**Version:** 1.0  
**Status:** Active
