# VitalLink Telehealth Analytics

**Tableau case study | Remote Patient Monitoring | Clinical Operations & Device Investigation**

VitalLink is a telehealth analytics project designed around a stakeholder assumption: **were device problems causing excessive warning alerts?**

The analysis combines patient-alert data, clinician response performance and device-health indicators to test that assumption and identify where operational attention should be focused.

## Business question

> What is driving alert overload, where is the 2-hour clinical response target being missed, and does the data support the assumption that device health is the main cause of warning-alert volume?

## Dataset

- **10,500** alert records
- **5,000** patients
- **12** clinicians
- **40** devices
- Period: **January 2026**

## Dashboard structure

### Page 1 — Patient Alert Profile

Focuses on alert volume, severity and patient-risk concentration.

![VitalLink Patient Alert Profile](01_dashboard/vitalink-patient-alert-profile.svg)

Key measures:

- 10,500 total alerts
- 1,591 Critical alerts
- 15.2% Critical-alert rate
- 3,668 Warning alerts
- 4,417 patients with alerts

### Page 2 — Clinical SLA & Device Health

Measures response efficiency and tests whether device characteristics are associated with warning-alert volume.

![VitalLink Clinical SLA & Device Health](01_dashboard/vitalink-clinical-sla-device-health.svg)

Key measures:

- 7.7 hours overall average response time
- 19.8% overall SLA compliance
- 8,425 SLA breaches
- 54.2% Critical SLA compliance
- 34.9% Warning Alert Rate

## Key findings

- Overall SLA compliance was **19.8%**, largely because lower-priority alerts took longer to close.
- Critical alerts were handled faster on average, but only **54.2%** met the 2-hour SLA.
- North Hub recorded the strongest Critical SLA compliance at **57.1%**; West Hub recorded **51.6%**.
- Device-model Warning Alert Rates were relatively close, ranging from **33.3% to 37.0%**.
- Battery level showed little visible relationship with Warning Alert Rate.
- Bluetooth and Cellular devices followed similar patterns.

## What the evidence changed

The data did **not** support a blanket conclusion that device condition was the primary cause of warning-alert volume.

The stronger operational concern was **alert prioritisation, SLA monitoring and response workflow**.

Device health still warrants targeted investigation, but the evidence supports reviewing selected higher-warning models rather than broad device replacement.

## Recommendations

1. **Separate priority queues** — create a dedicated Critical-alert queue with escalation rules.
2. **Monitor Critical SLA in real time** — track performance by hub and clinician rather than relying only on average response time.
3. **Review workload distribution** — compare clinician workload and SLA performance to identify bottlenecks.
4. **Target device review** — investigate higher-warning models selectively rather than assuming battery or connectivity is the main cause.

## Analytical approach

A star-schema-style model was structured around the alert fact table, supported by patient, clinician and device dimensions.

The workflow moved through:

**Model & validate → profile alerts → measure SLA performance → test device hypothesis → communicate recommendations**

## Tools & skills

**Tableau • Data Modelling • KPI Design • SLA Analysis • Root-Cause Investigation • Stakeholder Reporting**

## Repository structure

```
01_dashboard/
    vitalink-patient-alert-profile.svg
    vitalink-clinical-sla-device-health.svg
    README.md

02_tableau/
    README.md

03_data/
    README.md

04_documentation/
    README.md
    findings-and-recommendations.md
```

## Portfolio

View the full interactive case-study presentation on my portfolio:

**https://mayfuns.github.io/mariam-analytics-portfolio/vitalink.html**
