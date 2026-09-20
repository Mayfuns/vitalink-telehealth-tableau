# Findings & Recommendations

## Patient alert profile

- 10,500 alerts were generated during January 2026.
- 1,591 were Critical, representing 15.2% of total alert workload.
- Warning alerts represented 34.9% of total alerts.
- Blood Pressure generated the highest alert count, although the spread across vital types was narrow.
- New York recorded the most Critical alerts, closely followed by Chicago.

## Clinical SLA performance

- Overall SLA compliance was 19.8%.
- Critical alerts were responded to faster on average than lower-priority alerts.
- Critical SLA compliance was 54.2%, so almost half of Critical alerts still exceeded the 2-hour target.
- North Hub performed best at 57.1% Critical SLA compliance.
- West Hub recorded 51.6%.

### Interpretation

The average Critical response time being below two hours does not mean every Critical alert met the target.

The compliance rate reveals variation that the average alone can hide. This creates a stronger case for real-time SLA monitoring and escalation.

## Device-health investigation

- CelluPulse Pro recorded the highest Warning Alert Rate at 37.0%.
- GlucoTrack X recorded the lowest at 33.3%.
- The model-level spread was modest.
- Battery level showed little visible relationship with Warning Alert Rate.
- Bluetooth and Cellular devices followed similar patterns.

### Interpretation

Device condition may contribute to individual cases, but the available evidence does not support battery or connectivity as the primary driver of Warning Alert volume.

## Recommendations

### 1. Separate priority queues

Create a dedicated Critical-alert queue and escalation rule so high-priority alerts are not buried among Normal and Warning alerts.

### 2. Monitor Critical SLA in real time

Track Critical SLA compliance by hub and clinician and trigger operational review when performance falls below target.

### 3. Review workload distribution

Use clinician workload and SLA performance together to investigate staffing pressure, process bottlenecks and potential training needs.

### 4. Target device review

Prioritise investigation of higher-warning device models such as CelluPulse Pro, while avoiding blanket replacement without stronger evidence.

## Decision-support takeaway

The project demonstrates why stakeholder assumptions should be tested rather than built into the conclusion.

The initial concern focused on the devices. The analysis redirected attention toward **alert prioritisation, SLA compliance and clinical-response workflow**, while preserving device health as a targeted secondary investigation.
