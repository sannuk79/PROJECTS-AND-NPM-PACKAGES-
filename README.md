# 🚀 Sannu Kumar - Full-Stack & Systems Engineer

> **Portfolio:** [sannu-portfolio.vercel.app](https://sannu-portfolio.vercel.app/portfolio) | **Catalog:** [Projects Catalog](https://sannu-portfolio.vercel.app/portfolio/projects)

Welcome to my professional laboratory. Here, I build production-grade NPM packages, enterprise-scale web applications, and high-performance mobile solutions.

---

## 💎 Featured NPM Packages

### 📊 1. API Response Monitor
**Enterprise-grade monitoring middleware for Node.js.**

[![NPM Version](https://img.shields.io/npm/v/@sannuk792/api-response-monitor?color=brightgreen)](https://www.npmjs.com/package/@sannuk792/api-response-monitor)
[![NPM Downloads](https://img.shields.io/npm/dm/@sannuk792/api-response-monitor)](https://www.npmjs.com/package/@sannuk792/api-response-monitor)

![API Monitor Dashboard](./APIRESPONSE%20DASH.png)

- **Production Tracing**: Auto-generated `requestId` in every response.
- **Advanced Monitoring**: Built-in slow endpoint detection & health metrics.
- **Fail-Safe Design**: Monitoring logic never blocks or crashes your API.
- **Non-Blocking**: Non-allocation fast paths with ~0.2ms overhead.

**[View on NPM](https://www.npmjs.com/package/@sannuk792/api-response-monitor)** | **[Source Code](https://github.com/sannuk79/ApiMonitor)**

---

### 🛡️ 2. Payload Guard
**Lightweight, zero-dependency shape-based filtering & sanitization.**

[![NPM Version](https://img.shields.io/npm/v/payload-guard-filter?color=blue)](https://www.npmjs.com/package/payload-guard-filter)

![Payload Guard Workflow](./PAYLOAD.png)

- **Shape-based Filtering**: Define what you want, auto-remove everything else.
- **Sensitive Protection**: `password`, `token`, `secret` auto-redacted.
- **High Performance**: Optimized schema compilation for sub-millisecond execution.

**[View on NPM](https://www.npmjs.com/package/payload-guard-filter)**

---

## 📂 Project Catalog

A selection of production-grade applications and experimental prototypes.

| Project | Category | Description | Tech Stack |
|:---|:---|:---|:---|
| **DRIVERRUNNER** | Mobile | Complete Ride Sharing Platform with real-time tracking & payments. | Node, Mongo, RN, Socket.IO |
| **SHOPMIND AI** | Web | AI-powered price comparison with Rust-accelerated scraping. | Next.js 15, FastAPI, Rust |
| **URBANCRUISE LMS** | Web | Enterprise Lead Management System with real-time visualization. | Next.js, Express, MySQL |
| **TASKVISTA** | Web | Team Management Dashboard for developer communities. | React, Kendo UI, Tailwind |
| **BIOMETRIC AUTH** | Tools | WebAuthn system for passwordless fingerprint login. | WebAuthn, React 19, Security |
| **API MONITOR** | Tools | The official NPM package for API latency and health tracking. | NPM, Node.js, Metrics |

### ✨ Project Deep Dives

#### 🚕 [DriverRunner](#)
A comprehensive ride-hailing solution featuring 3 separate apps. Includes OTP-based authentication, real-time driver tracking (React Native Maps), and live booking systems via Socket.IO.

#### 🤖 [ShopMind AI](https://shopmind-ai.vercel.app/)
Intelligent price comparison platform. Uses Rust-accelerated scraping engines for speed and WebAuthn for biometric fingerprint login.

#### 📊 [UrbanCruise LMS](https://lms-leadmangsystem.vercel.app/)
Enterprise-grade lead tracking system. Handles multi-source collection (Meta, Google Ads) with real-time dashboards using Recharts and role-based access control.

---

## ⚡ Performance Benchmarks

### 🛡️ Payload Guard (Production Scale)
| Benchmark | ops/sec | avg (ms) |
|-----------|---------|----------|
| **Small payload** | 449,365 | **0.0022ms** |
| **Medium payload** | 7,791 | **0.1284ms** |
| **Large payload** | 246 | **4.0724ms** |

### 📊 API Monitor (Middleware Overhead)
| Metric | Full Mode | Minimal Mode |
|-----------|---------|----------|
| **Latency** | ~0.18ms | **<0.05ms** |
| **Throughput** | 50k+ RPM | 100k+ RPM |

---

## 🛠️ Combined Usage

Build a hardened and monitored API:
```javascript
const { apiMonitor } = require('@sannuk792/api-response-monitor');
const { guard } = require('payload-guard-filter');

app.use(apiMonitor({ mode: 'minimal' })); // Global Monitoring
app.post('/api/secure-data', (req, res) => {
  const safeBody = userShape(req.body);   // Precise Filtering
  res.json(safeBody);
});
```

---

<p align="center">
  Connect with me on <strong>[Portfolio](https://sannu-portfolio.vercel.app/portfolio)</strong>
  <br>
  Made with ❤️ for High-Performance Systems
</p>