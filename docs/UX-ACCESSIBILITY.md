# UX and Accessibility Baseline

## Information architecture

Use consistent navigation for overview, product, members/roles, integrations, support, audit, security and settings. Show only sections permitted by the current role.

## Interaction states

Every asynchronous action needs loading, success, empty, validation-error, permission-denied, dependency-failure and retry states. Destructive actions require confirmation and clear consequences.

## Accessibility

- semantic headings and landmarks
- keyboard navigation and visible focus
- labels and accessible names for controls
- sufficient contrast and non-color error messaging
- responsive layouts for mobile and desktop
- reduced-motion support
- screen-reader friendly status and error announcements
- no secrets or sensitive data in tooltips, URLs or browser storage

## Performance

Set budgets for initial JavaScript, largest contentful paint, interaction latency, API response time and dependency calls. Measure in CI or a reproducible staging environment.

## Privacy

Avoid unnecessary personal data in UI, analytics and logs. Provide privacy notice, account/session controls and data export/deletion entry points.
