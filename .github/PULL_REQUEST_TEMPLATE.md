# Description

JIRA ticket: HOT-XXXX

<!-- Include a summary of the change -->

...

## Purpose / goal

<!-- What is the reason of this PR? Add any relevant context. -->

...

## Key changes

<!-- List the specific changes to guide reviewers on what to look for. -->

- ...

## Change impact

<!-- Describe what is the impact of this change: which carriers are affected, what features, any known risk, etc. -->

...

## Next steps / other

<!-- Future tasks, TODOs not addressed in this PR, related/blocking PRs etc. -->

- [ ] ...

## Checklists

<!-- Consider the following checklists and tick the appropriate boxes. Remove any items that do not apply. -->

**If you think a mandatory check is not needed, please provide reasoning.**

### Risk and Impact Assessment (mandatory)

- [ ] This change does not include any data or database migration OR the migration is backward compatible
- [ ] This change does not include any data or database migration OR the migration can be rolled back
- [ ] This change does not destroy any persisted data
- [ ] This change will not cause any downtime while being deployed
- [ ] This change is fully backward compatible
- [ ] This change is behind a feature flag, will not cause any visible impact to end-users OR is ready for immediate release in production
- [ ] The change is not dependent on some other deployments (infrastructure or third-party)

:warning: If any of the above is not true and the change impacts production, the change is considered `High Risk`. If that's the case, the following must be done:

- Add `[high risk :warning:]` to the PR title
- Add `[high risk :warning:]` to the PR merge commit
- Add the label `high risk` to the PR
- A director must approve the PR
- Update the [Deployment status page](https://breathelife.atlassian.net/wiki/spaces/ENG/pages/481231139/Deployment+status) with the risk/impact and associated PRs and tasks.

### Security

- [ ] New or updated attributes in schemas have the proper [data labels](/getbreathelife/bliss/blob/develop/shared/meta-cruncher/README.md) to ensure PII is properly anonymized
- [ ] No sensitive data is being output in the logs
- [ ] This change contains no console logs or includes an explanation why the log is necessary
- [ ] A [security assessment](https://breathelife.atlassian.net/servicedesk/customer/portal/1/group/1/create/66) has been created to validate new features or design changes with potential impacts on the system security
- [ ] The code has been reviewed for [OWASP top 10](https://owasp.org/Top10/) security vulnerabilities

### Testing

- [ ] Tested carriers locally [Required]
- [ ] Tested on sandboxes [Required]

### Frontend

- [ ] Received and acted on UI feedback from a designer
- [ ] Tested general accessibility with Axe tooling
- [ ] Manually tested WCAG screen reader support (if required)
- [ ] Updated Storybook for `ui-components`, `field-generator`, `consumer-flow` or `dynamic-pdf`

### Backend

- [ ] Wrote unit and integration tests
- [ ] Created database migrations
  - [ ] Tested the `migrate:down` logic
  - [ ] Tested the migration by deploying a sandbox [mandatory in migrations]
  - [ ] Data migration: Tested with prod-like data using a staging / demo db export ( with EXPLAIN data in the PR description to display the execution plan of a statement for big/complex migrations when needed )
  - [ ] Data migration: Unit tests on the business logic

### Tracking

- [ ] Includes tracking calls for new events
- [ ] Updated `larousse` with new tracking properties

### Other

- [ ] Updated necessary documentation
- [ ] Requires `yarn install` for new dependencies
- [ ] Requires `pdf-generator` deployment

## Sandbox links

- ...

## Screenshots

...
