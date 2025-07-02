# Threshold Scheduler

**Category:** Monitoring / Alerts  
**Tags:** scheduler, threshold, notification, alerts, time interval, date range, IoT Open, function monitoring

---

## 📝 Description

**Threshold Scheduler** is an advanced IoT Open edge app for monitoring sensor or function values and sending notifications when thresholds are breached. The app supports scheduling by both **date** and **time**, with detailed control over **weekdays**, **time-of-day**, and whether notifications should be sent **inside or outside** the defined period.

### 🔧 Features

- Select one or multiple **trigger functions** to monitor.
- Define whether to trigger when values go **over** or **under** a configurable **threshold**.
- Set **date range** (ignores year) and optionally restrict to specific **weekdays** and **hour ranges**.
- Toggle between triggering **inside** or **outside** the specified hours.
- Choose a **notification output** for alerts.
- Optional setting to **send only one notification per state**, avoiding repeated alerts.

### 📅 Example Use Cases

- Alert when room temperature exceeds 30°C during working hours.
- Notify if CO₂ levels drop too low overnight.
- Monitor water level thresholds in a tank only during weekends.

---

## ⚙️ Configuration Steps

The app setup consists of two stages:

### Stage 1: Basic Settings
- Select functions to monitor.
- Choose over/under threshold direction.
- Enter the numeric threshold.
- Select a notification output.
- (Optional) Enable "send only once" to limit repeat alerts.

### Stage 2: Time Interval Settings
- Define the active start and end dates (MM-DD format).
- (Optional) Set time interval in hours (e.g., 08–17).
- Select active weekdays (Mon–Sun).
- Toggle between triggering **inside** or **outside** the defined time range.

---

## 📤 Output

When triggered, a notification is sent to the selected output. The notification includes:
- Current value
- Threshold type (over/under)
- Function and unit info
- Device metadata (if available)

---

## 🛠️ Requirements

- IoT Open Edge Runtime
- MQTT-connected functions with readable values (`topic_read`)
- Configured notification output

---

## 📄 License

MIT License
