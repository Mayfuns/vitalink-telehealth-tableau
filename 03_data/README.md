# Data Model

The project uses a star-schema-style analytical model centred on alert activity.

## Alert Fact Table

Key fields:

- AlertID
- AlertDate
- VitalType
- AlertSeverity
- Response Time Hrs
- PatientID
- ClinicianID
- DeviceID

## Patient Dimension

Key fields:

- PatientID
- PatientAge
- PatientCity
- Primary Condition

## Clinician Dimension

Key fields:

- ClinicianID
- ClinicianName
- Grade
- Hub Region

## Device Dimension

Key fields:

- DeviceID
- Model Name
- Connectivity
- Battery Status

## Model purpose

The model allows the same alert records to be analysed across three different operational perspectives:

1. **Patient risk** — who is generating alerts and what type?
2. **Clinical operations** — who responded, how quickly, and was the SLA met?
3. **Device investigation** — are Warning alerts associated with a particular model, connectivity type or battery condition?

## Scope

The analysed period is January 2026 and contains:

- 10,500 alert records
- 5,000 patients
- 12 clinicians
- 40 devices
