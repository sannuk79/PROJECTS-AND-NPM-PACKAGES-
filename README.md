# 🚀 Sannu Kumar - Full-Stack & Systems Engineer

> **Portfolio:** [sannu-portfolio.vercel.app](https://sannu-portfolio.vercel.app/portfolio) | **Catalog:** [Projects Catalog](https://sannu-portfolio.vercel.app/portfolio/projects)

Welcome to my professional laboratory. Here, I build production-grade NPM packages, enterprise-scale web applications, and high-performance mobile solutions.

---
## Official Website: https://www.codeevaai.com/
## 🏆 MAJOR ACHIEVEMENT: 1 MILLION CARDS WITH SMOOTH SCROLL

### **Performance Benchmark: 10,00,000 Cards**

```
📊 Generated 1,00,000 categories with 10,00,000 total cards
⚡ Response Time: 3378ms → <100ms (with pagination)
🚀 Scroll Performance: 60 FPS (smooth)
💾 Memory Usage: 99% reduction
📉 Data Transfer: 500MB → 25KB per request
```

### **Before Optimization:**
- ❌ API Response: **3378ms** (3.3 seconds)
- ❌ Data Transfer: **~500MB**
- ❌ Initial Load: **3+ seconds**
- ❌ Memory: **Very High**
- ❌ Scroll: **Janky/Laggy**

### **After Optimization (lazy-render + Backend Pagination):**
- ✅ API Response: **<100ms** (**33x faster**)
- ✅ Data Transfer: **~25KB** (**20,000x less**)
- ✅ Initial Load: **<200ms** (**15x faster**)
- ✅ Memory: **Very Low** (**99% reduction**)
- ✅ Scroll: **Smooth 60 FPS**

### **Technology Stack:**
- **Frontend:** lazy-render-virtual-scroll (Virtual Scrolling)
- **Backend:** Pagination with cursor-based navigation
- **Database:** MongoDB/PostgreSQL with indexed queries
- **Caching:** Redis with TTL-based cleanup

---


## 💎 Featured NPM Packages

### 📊 1. API Response Monitor
**Debug production API issues in seconds with request tracing and slow endpoint detection.**

[![NPM Version](https://img.shields.io/npm/v/@sannuk792/api-response-monitor?color=brightgreen)](https://www.npmjs.com/package/@sannuk792/api-response-monitor)
[![NPM Downloads](https://img.shields.io/npm/dm/@sannuk792/api-response-monitor)](https://www.npmjs.com/package/@sannuk792/api-response-monitor)

![API Monitor Dashboard](./APIRESPONSEDASH.png)

### � Workflow Overview
```mermaid
graph LR
    A[Request] --> B[Generate RequestID]
    B --> C[Intercept Response]
    C --> D[Calculate Metrics]
    D --> E[Async Logging/Storage]
    E --> F[Dashboard/Analytics]
```

- **Production Tracing**: Auto-generated `requestId` in every response.
- **Protocol Metadata**: Built-in SDK version, platform, and service tagging for microservices.
- **Hardened Stability**: Verified with a **14-point stress test** (100 req/sec, circular ref protection, middleware isolation).
- **Advanced Monitoring**: Built-in slow endpoint detection & health metrics.
- **Fail-Safe Design**: Monitoring logic never blocks or crashes your API.
- **Non-Blocking**: Non-allocation fast paths with ~0.2ms overhead.


### ⛑️ Maintained actively.
**Bug fixes usually within 24–48 hours.**


**[View on NPM](https://www.npmjs.com/package/@sannuk792/api-response-monitor)** | **[Source Code](https://github.com/sannuk79/ApiMonitor)**

---

### 🛡️ 2. Payload Guard
**Lightweight, zero-dependency shape-based filtering & sanitization.**

[![NPM Version](https://img.shields.io/npm/v/payload-guard-filter?color=blue)](https://www.npmjs.com/package/payload-guard-filter)

![Payload Guard Workflow](./PAYLOAD.png)

### �️ Workflow Overview
```mermaid
graph LR
    A[Request] --> B(Gatekeeper)
    B --> C{Shape Check}
    C -- Valid --> D[Redact & Clean]
    C -- Invalid --> E[Strict Error / Fail Safe]
    D --> F[Secure Response]
    E --> F
    F --> G((Metrics))
```

- **Shape-based Filtering**: Define what you want, auto-remove everything else.
- **Sensitive Protection**: `password`, `token`, `secret` auto-redacted.
- **High Performance**: Optimized schema compilation for sub-millisecond execution.

**[View on NPM](https://www.npmjs.com/package/payload-guard-filter)**

---

### 🔍 3. Flow Debugger
**Production-safe request tracing with root cause detection and live analytics dashboard.**

[![NPM Version](https://img.shields.io/npm/v/flow-debugger?color=purple)](https://www.npmjs.com/package/flow-debugger)
[![GitHub](https://img.shields.io/badge/GitHub-debugerpackages-purple)](https://github.com/sannuk79/debugerpackages)

![Flow Debugger Dashboard](./FLOWDEBUGGERDASH.png)
---
![PROJECT Debugger Dashboard](./FLOWDUBGERDASH.png)
---
### 🔄 Workflow Overview
```mermaid
graph LR
    A[Request] --> B[Generate TraceID]
    B --> C[Step-by-Step Tracking]
    C --> D[Auto-Classify: INFO/WARN/ERROR/CRITICAL]
    D --> E[Root Cause Detection]
    E --> F[Analytics Dashboard]
    F --> G[Search & Filter]
```

**Key Features:**
- **Zero-Config Setup**: Only **3 lines of code** needed for beginners to get full tracing & dashboard.
- **Auto-Instrumentation**: MongoDB, MySQL, PostgreSQL, Redis, Fetch, Axios — zero code changes
- **Waterfall View**: (New v1.1.0) High-res visual timeline of every request step.
- **Python Support**: (New v1.1.0) Cross-language tracing for Flask/FastAPI services.
- **Root Cause Detection**: Timeout → Failure → Slow bottleneck algorithm
- **Live Dashboard**: Real-time analytics at `/__debugger/dashboard`

**Performance:**
- **Load Tested**: 56,000 requests in 10s (100 concurrent connections)
- **Throughput**: 5,600 req/sec
- **Overhead**: <1ms per request

**[View on NPM](https://www.npmjs.com/package/flow-debugger)** | **[Source Code](https://github.com/sannuk79/debugerpackages)**

---

### 🚀 4. Lazy Render
**Framework-agnostic virtual scrolling and lazy rendering solution for efficient large dataset rendering.**

[![NPM Version](https://img.shields.io/npm/v/lazy-render?color=red)](https://www.npmjs.com/package/lazy-render)
[![NPM Downloads](https://img.shields.io/npm/dm/lazy-render)](https://www.npmjs.com/package/lazy-render)
![lazy card load](./cutcard.png)

![lazy one million card](../onemillioncard.png)

### 🔄 Performance Comparison
| Scenario | Without lazy-render | With lazy-render |
|----------|-------------------|------------------|
| 10,000 items render | 1800ms | 45ms |
| Memory usage (10k items) | High | Low |
| Initial load time | Slow | Fast |
| Scroll performance | Janky | Smooth |

### 🔄 Workflow Overview
```mermaid
graph LR
    A[Scroll Event] --> B[Detect Visible Range]
    B --> C[Calculate Render Window]
    C --> D[Render Only Visible Items]
    D --> E[Prefetch Next Batch]
    E --> F[Clean Up Off-Screen Items]
    F --> G[Smooth Scrolling Experience]
```

**Key Features:**
- **Framework Agnostic Core**: Pure logic implementation that works across different environments
- **Virtual Scrolling**: Only renders visible items to improve performance
- **Smart Prefetching**: Loads data ahead of user scroll to prevent loading gaps
- **Memory Efficient**: Automatically cleans up off-screen elements
- **React Adapter**: Easy integration with React applications
- **Configurable Buffer**: Adjustable buffer size for optimal performance
- **Overscan Support**: Additional buffer for smoother scrolling

**Performance Benefits:**
- **Efficient Rendering**: Only visible items render
- **Memory Management**: Unnecessary items removed
- **Smart Prefetch**: Data loads ahead of scroll
- **Smooth Scrolling**: Overscan provides seamless experience

**[View on NPM](https://www.npmjs.com/package/lazy-render)** | **[Source Code](https://github.com/sannuk79/lezzyrender)**

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

Build a hardened, monitored, and debuggable API:
```javascript
const { apiMonitor } = require('@sannuk792/api-response-monitor');
const { guard } = require('payload-guard-filter');
const { flowDebugger } = require('flow-debugger');

const debugger_ = flowDebugger({ environment: 'production' });

app.use(apiMonitor({ mode: 'minimal' }));  // Global Monitoring
app.use(debugger_.middleware);              // Request Tracing

app.post('/api/secure-data', (req, res) => {
  const safeBody = userShape(req.body);     // Precise Filtering
  res.json(safeBody);
});

// Dashboard: http://localhost:3000/__debugger/dashboard
```

---
## Official Website: https://www.codeevaai.com/
<p align="center">
  Connect with me on <strong>[Portfolio](https://sannu-portfolio.vercel.app/portfolio)</strong>
  <br>
  Made with ❤️ for High-Performance Systems
</p>
