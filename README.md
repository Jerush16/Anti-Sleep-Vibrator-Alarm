# Anti-Sleep Vibrator Alarm

A wearable drowsiness detection system mounted on a spectacle frame.
Detects prolonged eye closure using an IR sensor and triggers an instant
buzzer alert to prevent fatigue-related accidents.

> **Status:** Hardware prototype built and demonstrated at Tech Expo 2024,
> GCE Tirunelveli

---

## The Problem It Solves

Drowsiness causes thousands of road accidents annually. Commercial solutions
are expensive and require complex camera setups. This system achieves
real-time drowsiness detection with under ₹200 in components, worn like
regular glasses — no external hardware, no phone, no app required.

---

## Project Photos

### Wearable Setup
![Setup1](image/setup1.jpg)
![Setup2](image/setup2.jpg)

---

## How It Works

The IR sensor continuously emits infrared light toward the eye region.

- **Eyes open** — IR reflects back normally. No alert.
- **Eyes closed** — reflected signal drops. Buzzer triggers immediately.
- **Eyes reopen** — buzzer stops. System resets automatically.

The detection and alert cycle is fully analog — no microcontroller,
no code, no processing latency. Response is instantaneous.

---

## Hardware

[`hardware/components.md`](hardware/components.md)

| Component | Role |
|-----------|---|
| IR Sensor Module | Eye closure detection |
| Active Buzzer | Instant audio alert |
| Spectacle Frame | Wearable mount — consistent sensor positioning |
| 5V Battery | Portable power |

---

## Circuit Diagram

![Circuit Diagram](image/circuit diagram.jpg)


## Design Decisions

**Why analog instead of microcontroller?**
A purely analog circuit responds faster than any software loop — zero
processing delay between eye closure and alert. For a safety-critical
wearable this matters. It also keeps the build lighter and cheaper,
both important for something worn on the face.

**Why a spectacle frame?**
The IR sensor needs consistent positioning relative to the eye — within
2–3cm at a fixed angle. A spectacle frame provides this without straps
or adhesives, making it comfortable during long driving sessions.

**Limitation acknowledged:**
Ambient IR sources (direct sunlight, halogen lamps) can interfere with
detection. This is a known tradeoff of passive IR sensing without
modulation. A future version would use modulated IR with a bandpass
filter to eliminate ambient interference entirely.

---

## Achievement

Presented at **Tech Expo 2024**, Government College of Engineering,
Tirunelveli. Selected for demonstration among department projects.

---

## Author

**Jerush Thanusha T**
B.E. Electronics and Communication Engineering
Government College of Engineering, Tirunelveli

[LinkedIn](https://www.linkedin.com/in/jerush-thanusha-871188291) · [GitHub](https://github.com/Jerush16)
