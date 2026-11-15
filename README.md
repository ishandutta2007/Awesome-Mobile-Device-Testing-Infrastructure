# Awesome-Mobile-Device-Testing-Infrastructure

# Awesome Mobile Device Testing Infrastructure

> A curated list of top Mobile Device Testing Infrastructure platforms — both SaaS/Hosted commercial device clouds and open-source alternatives for accessing real Android and iOS devices for manual testing, automation, and debugging.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [BrowserStack Mobile Device Cloud](#browserstack-mobile-device-cloud)
  - [Sauce Labs Real Device Cloud](#sauce-labs-real-device-cloud)
  - [Kobiton](#kobiton)
  - [AWS Device Farm](#aws-device-farm)
  - [HeadSpin](#headspin)
  - [BitBar](#bitbar)
  - [Perfecto](#perfecto)
  - [TestGrid](#testgrid)
  - [Firebase Test Lab](#firebase-test-lab)
  - [Samsung Remote Test Lab](#samsung-remote-test-lab)
- [Open-Source Software](#-open-source-software)
  - [GADS](#gads)
  - [Device Farmer STF](#device-farmer-stf)
  - [AppiumTestDistribution](#appiumtestdistribution)
  - [Mobile MCP](#mobile-mcp)
  - [OpenSTF (Archived)](#openstf-archived)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Mobile Device Testing Infrastructure platforms. These are not open-source but are included as reference points for feature comparison.

### BrowserStack Mobile Device Cloud
**Type:** Large-scale real device cloud with broad framework support
BrowserStack provides access to **30,000+ real iOS and Android devices** hosted across 19 global data centers, with no setup or maintenance required [citation:3][citation:10]. Key capabilities include **App Live** for interactive manual testing with natural gestures, real-time debugging, and network throttling (2G/3G/Edge), plus **App Automate** for automated testing via Appium, Espresso, XCUITest, Flutter, and Detox [citation:3][citation:10]. Devices are wiped clean after each session, and day-0 device availability ensures testing on newly launched hardware [citation:3]. A free forever plan is available.  
**Best for:** Teams wanting the broadest device coverage and a mature manual testing experience with a free entry point.

### Sauce Labs Real Device Cloud
**Type:** Programmable device cloud with deep API access for AI workflows
Sauce Labs provides real devices across iPhone, iPad, Samsung Galaxy, Google Pixel, Oppo, Huawei, and Xiaomi, with a **Real Device Access API** that exposes the device itself as programmable infrastructure [citation:7]. Engineers can allocate devices in seconds, issue raw ADB and xcrun commands, stream live video and logs, manage files, and maintain sessions up to **24 hours** — all through HTTP requests without requiring Appium or Espresso [citation:7]. The API is **MCP-ready**, allowing AI agents to interact with devices as native tools, and early adopters reclaimed up to **40% of device time** by eliminating setup-and-teardown cycles [citation:7]. An IDE plugin also enables device access directly from VS Code, Cursor, and IntelliJ [citation:14].  
**Best for:** Teams needing deep device-level control for AI-driven workflows, soak tests, and custom automation beyond standard frameworks.

### Kobiton
**Type:** Real device cloud with AI automation and on-premises options
Kobiton offers real device access in public, private, and local clouds, plus **on-premises deployment** for sensitive environments [citation:5][citation:12]. Its **Nova AI engine** generates scriptless automation that runs across Android and iOS devices, with features including parallel execution, CI/CD integration, and detailed logs with video, screenshots, and system metrics (memory, battery) [citation:5][citation:12]. Migration services move existing test scripts from competing labs with zero risk [citation:12].  
**Best for:** Teams wanting AI-assisted automation and flexibility for on-premises device lab management.

### AWS Device Farm
**Type:** Pay-per-minute real device testing within AWS
AWS Device Farm provides access to physical Android, iOS, and web apps on real devices hosted by AWS [citation:13]. It offers a **fully managed Appium endpoint** for remote testing with live debugging, video, logs, and Appium Inspector support, plus support for Espresso, XCTest, and built-in test suites [citation:13]. Remote access allows interactive browser-based device control or automated Appium testing from a local client [citation:13]. Pricing is pay-per-minute after a free trial.  
**Best for:** AWS-centric teams with uneven testing schedules wanting pay-as-you-go pricing and native AWS integration.

### HeadSpin
**Type:** Performance-focused real device cloud across global locations
HeadSpin focuses on performance as well as functionality, with **SIM-enabled devices** deployed in numerous countries for validating app behavior on local carriers and networks [from previous context]. It tracks 130+ performance metrics across UI, network, and device, with AI-driven issue detection for freezes, crashes, and latency.  
**Best for:** Teams needing real-world performance validation across global markets and network conditions.

### BitBar
**Type:** Real device cloud with monitoring integration
BitBar (SmartBear) provides real device cloud testing with support for Appium, XCTest, XCUITest, and mobile browser testing, plus integration with AlertSite for converting functional tests into scheduled production monitoring.  
**Best for:** Teams wanting to extend test infrastructure into production monitoring with automated alerts.

### Perfecto
**Type:** Enterprise device cloud with flexible deployment
Perfecto (Perforce) provides real device cloud testing with SaaS, on-premises, and hybrid deployment options, multi-region hosting, and support for biometrics, sensor testing, and device vitals.  
**Best for:** Enterprises needing air-gapped on-premises device infrastructure and multi-region coverage.

### TestGrid
**Type:** Real device cloud with AI CoTester and device vitals
TestGrid provides real Android and iOS devices with its AI **CoTester** for generating and maintaining test flows, plus **AgentRx** for self-healing automation. Real-time device vitals (CPU, memory, battery, network) are available during testing.  
**Best for:** Teams wanting AI-assisted test creation with strong real-world scenario simulation.

### Firebase Test Lab
**Type:** Google-hosted device testing within Firebase
Firebase Test Lab provides cloud-based app testing on devices hosted in Google data centers, supporting instrumentation tests, Robo tests (no pre-written tests), game loop tests, and XCTest for iOS.  
**Best for:** Teams already in the Firebase/Google ecosystem wanting automated testing without infrastructure management.

### Samsung Remote Test Lab
**Type:** Free remote access to Samsung Galaxy devices
Samsung Remote Test Lab is a **free service** that lets developers test apps on the latest Samsung Galaxy devices remotely over the web [citation:4]. Users sign up with a Samsung Developer account, receive **20 credits per day** (1 credit = 15 minutes of device use), and can reserve devices for 30 minutes to 10 hours [citation:11]. The RTL Client allows screen control, hardware buttons, keyboard, S-Pen, app installation, logs, and screen capture/recording [citation:11]. **Limitations:** No audio, multi-touch, or camera support, and performance depends on network distance to Samsung servers [citation:11].  
**Best for:** Developers needing free access to Samsung-specific hardware for compatibility testing, accepting the credit-based usage limits and feature restrictions.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Mobile Device Testing Infrastructure tools. The open-source ecosystem spans **Appium-based device farms with remote control**, **Android device farm managers**, **Appium session distribution plugins**, and **AI-agent device access**.

### GADS
**Stack:** Go / Appium / WebDriverAgent | **License:** AGPL-3.0 (core) / Proprietary (hub-ui)  
GADS is a simple self-hosted device farm for remote control of Android and iOS devices and Appium test execution [citation:9]. Key features include:
- **Real-time video streaming** (MJPEG/WebRTC) for both iOS (via WebDriverAgent) and Android 
- **Remote interactions**: tap, swipe, text input, clipboard, keyboard typing 
- **App installation/uninstallation**, high-quality screenshots, device reservation system 
- **Appium-compatible** with optional Selenium Grid 4 node registration 
- **Smart TV automation** for Samsung Tizen OS and LG WebOS (automation only, no remote control) 
- **Workspace management** with user access control per workspace 

Platform support: full Android and iOS on macOS; limited iOS on Linux/Windows (Xcode dependency) . The project is **dual-licensed** with the core under AGPL-3.0 and the `hub-ui` directory under a separate proprietary license (obfuscated, not modifiable) . The repository has **254 stars** and is actively maintained (last push within days as of late 2026) [citation:9].  
**Best for:** Teams wanting a self-hosted device farm with Appium compatibility and remote control across Android, iOS, and even Smart TVs, accepting the dual-license arrangement.

### Device Farmer STF
**Stack:** Node.js / TypeScript / RethinkDB / ADB | **License:** Apache-2.0  
Device Farmer STF is the leading actively maintained open-source **real-device device farm for Android**, allowing teams to share and control physical devices remotely via a web interface [from previous context]. It supports the full ADB workflow including shell, logcat, and file management through the web UI, with a **Remote Debug panel** that exposes an `adb connect` command for connecting a remote device to your workstation for Chrome DevTools inspection . It is a maintained fork/derivative of the original OpenSTF project. Deployment via Docker Compose with RethinkDB is documented.  
**Best for:** Android QA teams wanting to share physical devices across a distributed team with genuine remote ADB debugging access.

### AppiumTestDistribution
**Stack:** TypeScript / Appium 2.0 | **License:** Open Source (GitHub)  
AppiumTestDistribution (appium-device-farm) is an **Appium 2.0 plugin** designed to manage and create driver sessions on available devices automatically [citation:2]. It has **262 stars** and **81 forks**, making it one of the more established open-source tools for distributing Appium tests across a device farm [citation:2]. It eliminates the need for manual device allocation logic in test frameworks, handling session creation and device management transparently.  
**Best for:** Teams already running Appium tests at scale wanting automatic device allocation and session distribution, accepting the Appium 2.0 dependency.

### Mobile MCP
**Stack:** TypeScript / MCP (Model Context Protocol) | **License:** Apache-2.0  
Mobile MCP gives AI agents (Claude Code, Cursor, Copilot) direct access to iOS simulators, iOS real devices (USB), Android emulators, and Android real devices (ADB) through **30+ MCP tools** [from previous context]. It reads UI elements from the native accessibility tree rather than screenshots, reducing token usage and enabling deterministic interactions across screen sizes . Tools cover device management (orientation, GPS, clipboard), app lifecycle (install, launch, terminate), screen interaction (tap, swipe, long press), input (type text, hardware buttons), and diagnostics (logs, crash reports, screen recording). It also supports **cloud device access** via Mobile Next Cloud, billed per device-minute.  
**Best for:** Developers using AI coding agents wanting device access within the same session, or teams integrating mobile verification into CI/CD pipelines with agent-driven workflows.

### OpenSTF (Archived)
**Stack:** JavaScript / Node.js / MongoDB | **License:** Other (open source)  
OpenSTF (Smartphone Test Farm) was the original open-source Android device farm, allowing control and management of Android devices from a browser [from previous context]. It had **13,958 GitHub stars** and 2,995 forks, with real-time screen viewing at 30-40 FPS, multitouch, drag-and-drop APK installation, reverse port forwarding, device inventory monitoring, and booking/partitioning systems . **Critical status:** The original project was **last pushed in May 2023** and has 464 open issues, making it effectively unmaintained [citation:2]. Forks and derivatives exist, but the original OpenSTF is not recommended for new deployments.  
**Best for:** Historical reference only; evaluate maintained forks or alternatives like GADS and Device Farmer STF for new projects.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Real Devices | Remote Control | Self-Hosted | Best For |
|----------|---------|-------|--------------|----------------|-------------|----------|
| **BrowserStack** | Proprietary | Cloud | ✅ 30,000+ | ✅ App Live | ❌ | Broadest coverage + free plan |
| **Sauce Labs** | Proprietary | Cloud | ✅ Extensive | ✅ RDA API | (Private) | Deep device control + AI |
| **Kobiton** | Proprietary | Cloud/On-prem | ✅ | ✅ | (On-prem) | AI automation + on-prem lab |
| **AWS Device Farm** | Proprietary | Cloud | ✅ | ✅ Remote access | (Private lab) | AWS-native pay-per-minute |
| **Samsung RTL** | Proprietary | Cloud | ✅ Samsung only | ✅ RTL Client | ❌ | Free Samsung device access |
| **GADS** | AGPL-3.0 | Go/Appium | ✅ Android/iOS | ✅ MJPEG/WebRTC | ✅ | Appium-compatible farm |
| **Device Farmer STF** | Apache-2.0 | Node.js/ADB | ✅ Android | ✅ ADB remote | ✅ | Shared Android devices |
| **AppiumTestDistribution** | Open Source | TypeScript | ✅ (Via Appium) | ❌ (Session mgmt) | ✅ | Appium test distribution |
| **Mobile MCP** | Apache-2.0 | TypeScript/MCP | ✅ Local/cloud | ✅ Agent-driven | ✅ | AI agent device access |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Mobile Device Testing Infrastructure tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** The open-source landscape for **self-hosted mobile device testing infrastructure** has matured significantly in 2026. **GADS** is the most comprehensive option, providing a full device farm with Appium compatibility, real-time video streaming, and remote control across Android, iOS, and even Smart TVs, though its `hub-ui` component is proprietary . **Device Farmer STF** remains the leading maintained Android device farm for shared device access with ADB debugging . **AppiumTestDistribution** addresses a different layer—automatically distributing Appium test sessions across available devices [citation:2]. **Mobile MCP** represents a newer paradigm: AI-agent-driven device access via MCP rather than a traditional web console . The original **OpenSTF** project is effectively unmaintained since May 2023 and should not be used for new deployments [citation:2].

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
