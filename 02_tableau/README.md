# Tableau Analysis

## Analytical design

The Tableau analysis was designed as a two-page story rather than a collection of unrelated charts.

### Page 1 — Understand the demand

The first page answers:

- How many alerts are being generated?
- What proportion are Critical or Warning?
- Which vital types generate the most alerts?
- Are alerts concentrated in particular patient groups or locations?

### Page 2 — Investigate operational performance

The second page answers:

- How quickly are alerts being handled?
- How often is the 2-hour SLA being met?
- Which hubs or clinicians need closer investigation?
- Do specific device models generate materially more Warning alerts?
- Is battery level visibly associated with Warning Alert Rate?

## Measures used

The analysis required measures for:

- Total Alerts
- Critical Alerts
- Critical Alert %
- Warning Alerts
- Patients with Alerts
- Average Response Time
- SLA Compliance %
- SLA Breaches
- Critical SLA Compliance %
- Warning Alert Rate

## Design principle

The dashboard deliberately separates **average response time** from **SLA compliance**.

An average can appear acceptable while a large number of individual alerts still breach the target. Showing both measures prevents the operational story from being hidden by an aggregate average.

## Root-cause approach

The device-health page was used to test a stakeholder hypothesis rather than confirm it.

Battery status, connectivity and model-level Warning Alert Rates were compared before drawing a conclusion. The observed patterns did not show a strong enough relationship to justify treating device condition as the primary cause of Warning Alert volume.
