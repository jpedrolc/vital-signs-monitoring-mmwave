# Vital Signs Monitoring using mmWave Radar

![Status]( * )
![Hardware]( * )
![Sensor]( * )

Contactless vital signs monitoring system using 60GHz millimeter-wave radar technology. Designed for elderly care, bedridden patients, or anyone requiring non-invasive health monitoring.
**Note on this Project:** This repository serves as a documentation of my progress and evolution as I develop this system. Since I am learning the implementation process from the ground up, you will find my step-by-step journey, technical challenges, and milestones here.

## 🎯 Key Features

- **Privacy-First**: No cameras, no images - only radar waves
- **Passive Monitoring**: No wearables required
- **Real-time Detection**:
  - Respiratory rate
  - Heart rate (ballistocardiography)
  - Sleep states (awake/light/deep)
  - Bed exit detection

## 🔬 How It Works

Unlike common 24GHz radars that detect gross movements, 60GHz sensors have wavelengths short enough to detect micro-vibrations (< 5mm) on the body surface:

- **Breathing**: Detects chest expansion/contraction
- **Heartbeat**: Detects micro-vibrations from blood pumping
- **Sleep Analysis**: Analyzes signal variations to determine sleep state

## 🛠️ Hardware Requirements

| Component | Recommended Model | Purpose |
|-----------|------------------|---------|
| **Radar Sensor** | Seeed Studio MR60BHA1 | 60GHz respiratory & heartbeat detection |
| **Microcontroller** | ESP32 (WROOM/S3) | Data processing & WiFi connectivity |
| **Home Automation** | Home Assistant | Data visualization & alerts |
| **Optional** | Load Cells (4x 50kg) | Bed presence confirmation & weight tracking |

See [Bill of Materials]( * ) for complete list.

## 📋 Use Cases

- Apnea/respiratory arrest detection
- Long-term heart rate trend monitoring (early infection detection)
- Nighttime fall prevention (bed exit alerts)
- Elderly care facilities
- Home health monitoring

## ⚠️ Limitations

1. **Motion Sensitivity**: Accurate readings require the subject to be **stationary** (sleeping/resting). Movement degrades heart rate accuracy.
2. **Not Medical-Grade**: This is a monitoring tool for trends and alerts, not a diagnostic device.
3. **Obstruction**: Very thick bedding (heavy down comforters) may slightly attenuate signal.

## 🚀 Roadmap

- [x] Research & documentation
- [ ] **Phase 1**: Basic presence detection (proof of concept)
- [ ] **Phase 2**: Respiratory rate measurement
- [ ] **Phase 3**: Heart rate detection integration
- [ ] **Phase 4**: Home Assistant integration (MQTT/ESPHome)
- [ ] **Phase 5**: Sleep state classification
- [ ] **Phase 6**: Alert system (Telegram/Alexa)
- [ ] **Phase 7**: Data logging & trend analysis

## 📚 Documentation

- [Hardware Setup Guide]( * )
- [Installation Instructions]( * )

## 🤝 Contributing

This is a personal learning project, but suggestions and improvements are welcome! Feel free to open an issue or submit a pull request.

## ⚖️ License

MIT License - See [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

**This project is for educational and monitoring purposes only. It is NOT a medical device and should not be used as a substitute for professional medical advice, diagnosis, or treatment.**

---

**Current Status**: Research & Planning Phase  
**Next Step**: Implementing Phase 1 (Basic Presence Detection)
