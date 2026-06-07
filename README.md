# DTC Team Projects — Presentation Report

**Last Updated**: June 8, 2026
**Team**: Digital Transformation Center (DTC)
**Report Type**: Project Progress & Summary

---

## 📋 Overview

This report summarizes the four major projects developed by the **Digital Transformation Center (DTC)** team. Each project tackles a distinct aspect of our digital transformation goals — from IoT-based greenhouse automation, to full-stack web portals, a lightweight static website, and a Kubernetes-powered computing cluster for enhanced infrastructure performance.

---

## 📊 Overall Team Progress

| # | Project | Status | Completion |
|---|---------|--------|------------|
| 1 | ATLANTIS 2.0 | ✅ Ready to Use | 90% |
| 2 | DTC Web Portal | ⚠️ Possible to Use | 85% |
| 3 | DTC Web Page 2.0 | ✅ Ready to Serve | ~95% |
| 4 | DTC Cluster (Kubernetes) | ✅ Deployed | Operational |

---

---

# 🌿 ATLANTIS 2.0

**Repository**: https://github.com/ScarletVonRosefall/ATLANTIS-2.0.git
**Version**: 2.0 — Greenhouse IoT Application
**Status**: ✅ Ready to Use

### Progress

```
█████████░ 90% Complete
```

| Area | Completion | Notes |
|------|-----------|-------|
| Core Features | ✅ 95% | Dashboard, Sensors, Actuators, Alerts, Activity Logging |
| IoT Integration | ✅ 90% | ESP32 device support, real-time data synchronization |
| Cloud Integration | ✅ 95% | Firebase authentication, Firestore database, real-time updates |
| Advanced Features | ⚠️ 85% | Advanced analytics and predictive alerts pending |
| Code Quality | ✅ 90% | Localization support, theme management, comprehensive services |

### What We Built

**ATLANTIS 2.0** is an integrated smart greenhouse management system that automates and monitors environmental control. The system combines an Android mobile dashboard with embedded **ESP32 hardware**, letting operators manage greenhouse conditions both manually and automatically in real time.

**System Architecture:**
- **Frontend** — Android mobile application for real-time monitoring and control
- **Hardware Controller** — ESP32 microcontroller managing physical sensors and actuators
- **Cloud Backend** — Firebase for data synchronization, authentication, and live updates
- **Control Modes** — Manual (dashboard) and Automatic (rules-based scheduling)

**Key Features:**
- Real-time sensor monitoring — temperature, humidity, soil moisture, light levels
- Remote actuator control — irrigation, heating, cooling, and lighting systems
- Customizable alert system for critical environmental conditions
- Full activity logging and audit trail
- Live video/photo feed from the greenhouse
- Multi-language support (English & Spanish) and light/dark theme
- Secure user authentication with password reset

**Tech Stack:** Flutter · Dart · Firebase · Firestore · ESP32 (Arduino) · Android

### Remaining Work
- Fine-tune ESP32 command listeners
- Implement advanced analytics dashboard
- Add predictive alert system

### Optional Future Enhancements
- Machine learning-based environmental predictions
- Mobile push notifications
- Export and reporting features

---

---

# 📊 DTC Web Portal

**Repository**: https://github.com/Kyle-Geronimo/DTC-MPM-Web-System.git
**Version**: 2.0 — Full Backend Implementation
**Status**: ⚠️ Possible to Use

### Progress

```
█████████░ 85% Complete
```

| Area | Completion | Notes |
|------|-----------|-------|
| Core Features | ✅ 95% | Authentication, Projects, Tasks, Teams, Messaging, Reports |
| Production Readiness | ⚠️ 70% | Dev tools still present; test files and dev-only endpoints remain |
| Advanced Features | ⚠️ 75% | 2FA not yet implemented; advanced permissions pending |
| Code Quality | ⚠️ 85% | Some hard-coded test data and sample credentials in database |

### What We Built

The **DTC Web Portal** is a comprehensive full-stack web application for managing projects, monitoring system performance, and coordinating DTC team activities. It features a robust backend API, real-time updates, and advanced admin capabilities — all accessible through a browser.

**Key Features:**
- Complete authentication and user management system
- Project, task, and team management
- Real-time messaging and communication system
- System monitoring and performance tracking
- Comprehensive reporting and analytics dashboard
- Admin panel with full system management
- User notifications and alerts
- Data export and reporting tools

**Tech Stack:** PHP 7.4+ · MySQL / MariaDB · Apache/Nginx · HTML · CSS (Dark Mode) · JavaScript

**Project Structure:** 70+ files organized across `page/`, `settings/`, `css/`, `js/`, `Doc/`, and `Database/` directories.

### Remaining Work
- Remove and disable all development-only files for production
- Replace hard-coded test credentials with environment variables
- Implement two-factor authentication (2FA)
- Build out the advanced permission system
- Remove sample data from database setup scripts

### Optional Future Enhancements
- Native mobile applications

---

---

# 🌐 DTC Web Page 2.0

**Repository**: https://github.com/Sayki17/DTC-WEB-2.0.git
**Version**: 2.0 — Static Website
**Status**: ✅ Ready to Serve

### Progress

```
██████████ ~95% Complete
```

| Area | Completion | Notes |
|------|-----------|-------|
| Core Website | ✅ | Main HTML/CSS pages fully built and styled |
| Almanac / DTC Chapter Viewer | ✅ | Gallery slideshow with thumbnails and autoplay |
| Achievement Pages | ✅ | Achievement cards and image assets added |
| Optional Upload Server | ✅ | Flask-based dev server for local image uploads |
| Deployment Readiness | ✅ | Ready for GitHub Pages / Netlify / static hosting |

### What We Built

**DTC Web Page 2.0** is a lightweight, dependency-free static website for the Digital Transformation Center. It is designed for easy hosting on GitHub Pages, Netlify, or any static server — no build tools required.

**Key Features:**
- Clean, responsive static website with site-wide `style.css`
- **Almanac / DTC Chapter Page** — a full-viewport gallery viewer featuring:
  - Full-screen featured photo with `object-fit: contain` (no cropping)
  - Bottom thumbnail scroller for quick navigation
  - Automatic slideshow loop with pause-on-hover
  - Restart after manual navigation
  - Preloads assets for instant previews
- Achievement image cards (e.g., `achievements/2.jpeg`, `achievements/3.jpeg`)
- Optional Flask upload server (`upload_server.py`) for local development image management

**Tech Stack:** HTML · CSS · (Optional) Python 3 / Flask (dev only)

### Recent Changes
- Added achievement images and updated `actual_web.html` with new cards
- Built `almanac/dtc-chapter.html` with full gallery/slideshow/thumbnail functionality
- Added optional `upload_server.py` for local testing

### Remaining Work
- Minor accessibility improvements (additional `alt` attributes for images)
- Optional: deployment guide for GitHub Pages

---

---

# 🖥️ DTC Cluster (Kubernetes)

**Status**: ✅ Operational
**Technology**: Kubernetes (K8s)

### Progress

```
██████████ Deployed & Operational
```

### What We Built

The **DTC Cluster** is an on-premise computing cluster built from **7 physical PCs** to provide the Digital Transformation Center with significantly improved processing power and resource availability.

**Cluster Architecture:**

```
                    [ Internet / Ethernet ]
                             |
                         [ Switch ]
                             |
        ┌────────────────────┴────────────────────┐
        |                                         |
  [ Master Node ]                         [ Worker Nodes x6 ]
  (Orchestration &                  (Offering CPU, RAM, Storage
   Scheduling via K8s)               resources to the cluster)
```

**Node Breakdown:**

| Role | Count | Function |
|------|-------|----------|
| Master Node | 1 | Manages cluster orchestration, scheduling, and control plane via Kubernetes |
| Worker Nodes | 6 | Provide hardware resources (CPU, RAM, Storage) to the cluster |

**How It Works:**
- All 7 PCs are interconnected through a **network switch**
- The switch is also connected to the **Ethernet/internet**, giving all nodes network access
- The **6 Worker Nodes** pool their hardware specifications and offer them to the **Master Node**
- The Master Node orchestrates workloads across workers using **Kubernetes (K8s)**
- This setup gives the DTC significantly better compute performance for hosting, workloads, and services

**Key Benefit:** The cluster allows the DTC to run containerized applications, distributed workloads, and services with much greater performance and resilience than a single machine could provide.

**Tech Stack:** Kubernetes (K8s) · Linux · Network Switch · Ethernet

---

---

## 🤝 Contributing (All Projects)

For any of the projects above:
1. Create a new branch for your feature or fix
2. Make changes and test thoroughly
3. Update relevant documentation
4. Submit a pull request with a clear description

---

## 📝 License

See the `LICENSE` file in each respective repository for details.
