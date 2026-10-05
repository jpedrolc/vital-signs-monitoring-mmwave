# Vital Signs Monitoring using mmWave Radar

Research project exploring contactless respiratory and heart rate monitoring with 60 GHz mmWave radar for people resting or in bed.

**Status: 🟡 Research / Design — hardware integration and experimental validation pending.**

## Problem

Contactless sensing could support observation during rest without a camera or wearable. The study must establish whether radar measurements remain usable across changes in posture, movement and sensor placement.

## Proposed Approach

Investigate a Seeed Studio MR60BHA1 module connected to an ESP32, with data visualization in Home Assistant. Respiratory rate, heart rate, bed exit detection and alerts are study objectives; none has been experimentally validated by this project.

Sleep-related signal analysis is exploratory. Reliable sleep-stage classification remains an open research question.

## Planned Architecture

**MR60BHA1 → UART → ESP32 → Wi-Fi / MQTT or ESPHome → Home Assistant**

The radar would provide sensing data, the ESP32 would handle acquisition and communication, and Home Assistant would display measurements and proposed alerts. The choice between MQTT and ESPHome remains open.

An initial installation hypothesis places the radar above the headboard, aimed at the chest, around 0.8–1.5 m from the subject. Placement and distance must be tested for the selected module.

## Proposed Technologies

- Seeed Studio MR60BHA1, 60 GHz radar.
- ESP32 WROOM or S3; UART and Wi-Fi.
- MQTT or ESPHome; Home Assistant.
- Optional load cells for bed presence confirmation; not integrated.

## Current Status and Limitations

**Documented:** use case, sensor/controller architecture, installation hypotheses and research objectives.

**Pending:** hardware integration, firmware, bench measurements and comparison with reference measurements. No firmware, datasets or experimental results are published.

Movement, posture, bedding and placement are variables to evaluate. Respiratory inactivity alerts, heart rate trends and bed exit alerts remain proposed capabilities.

This is an educational research project, not a validated medical or diagnostic device. Any future alert requires human verification.

## Next Steps

1. Validate UART acquisition and basic presence sensing on the bench.
2. Compare respiratory and heart rate readings with reference measurements under documented conditions.
3. Integrate data visualization after validating acquisition.
4. Assess alert reliability and sleep-related analysis using recorded data.

## License

[MIT License](LICENSE).
