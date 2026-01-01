# ☁️ Cloudflare Speed Test Monitoring

This configuration visualizes results from the Cloudflare Speed Test
integration in Home Assistant.

It provides visibility into:
- Latency and jitter
- Download throughput at multiple payload sizes
- Upload throughput trends
- Percentile-based performance degradation

This setup is useful for:
- Diagnosing ISP congestion
- Detecting bufferbloat / jitter spikes
- Comparing small vs large payload behavior
- Long-term link quality analysis

---

## 📊 Included Dashboards

### 1️⃣ Latency & Jitter (Statistics Graph)

Displays maximum latency and jitter per period.

**Metrics**
- `sensor.cloudflare_speed_test_latency`
- `sensor.cloudflare_speed_test_jitter`

**Aggregation**
- `max` (worst-case visibility)

**Time window**
- 3 days

---

### 2️⃣ Download Speed (ApexCharts)

Displays download speeds for different payload sizes:
- 100 KB
- 1 MB
- 10 MB
- 25 MB
- 90th percentile

This highlights:
- TCP slow-start effects
- Congestion under sustained load
- Peak vs degraded throughput

---

### 3️⃣ Upload Speed (ApexCharts)

Displays upload performance using:
- 1 MB
- 10 MB
- 90th percentile

Useful for:
- Detecting upstream shaping
- Video call / VPN stability issues

---

## 🛠 Requirements

- Home Assistant with Cloudflare Speed Test integration
- `custom:apexcharts-card`
- Long-term statistics enabled (recorder)

---

## 📌 Notes

- Graphs intentionally use **smooth curves** for trend analysis
- Percentiles are included to expose degradation, not just peaks
- Max-per-period aggregation highlights worst-case behavior

This is a monitoring view, not a vanity speed test.
