# Vital Signs Monitoring using mmWave Radar

**Status: 🟡 Research / Design — hardware integration and experimental validation pending.**

Research project exploring contactless vital signs monitoring with 60GHz millimeter-wave radar for elderly people resting or in bed.
**Note on this Project:** This repository serves as a documentation of my progress and evolution as I develop this system. Since I am learning the implementation process from the ground up, you will find my step-by-step journey, technical challenges, and milestones here.

## 🎯 Proposed Capabilities

- **Privacy-First**: No cameras, no images - only radar waves
- **Passive Monitoring**: No wearables required
- **Measurements to investigate**:
  - Respiratory rate
  - Heart rate (ballistocardiography)
  - Sleep-related signal analysis (exploratory; sleep-stage classification is not validated)
  - Bed exit detection

## 🔬 How It Works

The proposed study uses a 60GHz module intended for respiratory and heartbeat sensing. It explores body-surface micro-movements:

- **Breathing**: Detects chest expansion/contraction
- **Heartbeat**: Investigates smaller body-surface vibrations associated with cardiac activity
- **Sleep Analysis**: Investigates signal variations; reliable sleep-stage classification remains an open research question

## 🛠️ Proposed Hardware

| Component | Recommended Model | Purpose |
|-----------|------------------|---------|
| **Radar Sensor** | Seeed Studio MR60BHA1 | 60GHz respiratory & heartbeat detection |
| **Microcontroller** | ESP32 (WROOM/S3) | Data processing & WiFi connectivity |
| **Home Automation** | Home Assistant | Data visualization & alerts |
| **Optional** | Load Cells (4x 50kg) | Bed presence confirmation & weight tracking |

The planned data path is **MR60BHA1 → UART → ESP32 → Wi-Fi / MQTT or ESPHome → Home Assistant**. Load cells are optional and have not been integrated.

The Notion research notes propose testing a sensor above the headboard, aimed at the chest, initially around 0.8–1.5 m from the subject. These are **installation hypotheses**, not measurements validated by this project; placement must be checked for the selected module.

## 📋 Research Scenarios

- Investigation of respiratory inactivity alerts
- Long-term resting heart rate trends
- Bed exit alerts as a possible nighttime assistance feature
- Elderly care facilities
- Home health monitoring

## ⚠️ Limitations

1. **Motion Sensitivity**: Accurate readings require the subject to be **stationary** (sleeping/resting). Movement degrades heart rate accuracy.
2. **Not Medical-Grade**: This is an educational research proposal, not a validated monitoring or diagnostic device. Any future alert would require human verification; it must not be treated as an emergency diagnosis.
3. **Obstruction**: Very thick bedding (heavy down comforters) may slightly attenuate signal.

## 🚀 Roadmap

**Documented so far:** use case, proposed sensor/controller architecture, installation hypotheses and limitations. This repository contains documentation and a license; firmware, datasets and experimental results are not yet published.

- [x] Initial research notes & project documentation
- [ ] **Phase 1**: Basic presence detection (proof of concept)
- [ ] **Phase 2**: Respiratory rate measurement
- [ ] **Phase 3**: Heart rate detection integration
- [ ] **Phase 4**: Home Assistant integration (MQTT/ESPHome)
- [ ] **Phase 5**: Evaluate feasibility of sleep-related signal analysis
- [ ] **Phase 6**: Alert system (Telegram/Alexa)
- [ ] **Phase 7**: Data logging & trend analysis

## 📚 Documentation

This README summarizes the current research scope. Hardware setup and installation guides will be added after bench testing; no working setup is claimed here.

## 🤝 Contributing

This is a personal learning project, but suggestions and improvements are welcome! Feel free to open an issue or submit a pull request.

## ⚖️ License

MIT License - See [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

**This project is for educational and monitoring purposes only. It is NOT a medical device and should not be used as a substitute for professional medical advice, diagnosis, or treatment.**

---

**Current Status**: Research & Planning Phase  
**Next Step**: Implementing Phase 1 (Basic Presence Detection)
