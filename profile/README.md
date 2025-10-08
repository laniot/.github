# LAN IoT
LAN‑first IoT components. Fast and Small

**Audience:** Developers and Integrators  
**License:** Apache‑2.0 (all repos)  
**Contributing:** See `CONTRIBUTING.md` in each repo  
**Note:** Org‑level quickstarts and demos are omitted due to mixed hardware + software. Use per‑repo docs.

## Projects
- **core** — Multi‑tasking system for ESP32‑S3 with FreeRTOS. HTTPS server, secure WebSocket (WSS), UART→WSS/TCP broadcast, and certificate management.  
  https://github.com/laniot/core
- **signer** — Minimal CA signer service for issuing short‑lived device certificates via `POST /v1/sign`. Node.js.  
  https://github.com/laniot/signer

## Stack summary
- **core:** ESP32‑S3, ESP‑IDF, FreeRTOS, C/CMake, mbedTLS, NVS; protocols: HTTPS, WSS, TCP.  
- **signer:** JavaScript/Node.js; REST API; `.env` with `SIGNER_TOKEN`, `DEV_INT_CRT`, `DEV_INT_KEY`.

## Consulting & Expertise
Design reviews, integration, deployment. Contact via LinkedIn: https://www.linkedin.com/in/carloshuggins

---

## Español

**Público:** Desarrolladores e Integradores  
**Licencia:** Apache‑2.0 (todos los repos)  
**Contribución:** Revisa `CONTRIBUTING.md` en cada repositorio  
**Nota:** No hay *quickstarts* ni demos a nivel de organización por la mezcla HW + SW. Usa la documentación de cada repo.

## Proyectos
- **core** — Sistema multitarea para ESP32‑S3 con FreeRTOS. Servidor HTTPS, WebSocket seguro (WSS), difusión UART→WSS/TCP y gestión de certificados.  
  https://github.com/laniot/core
- **signer** — Servicio mínimo de firmado que emite certificados de dispositivo de corta duración vía `POST /v1/sign`. Node.js.  
  https://github.com/laniot/signer

## Resumen de *stack*
- **core:** ESP32‑S3, ESP‑IDF, FreeRTOS, C/CMake, mbedTLS, NVS; protocolos: HTTPS, WSS, TCP.  
- **signer:** JavaScript/Node.js; API REST; `.env` con `SIGNER_TOKEN`, `DEV_INT_CRT`, `DEV_INT_KEY`.

## Consultoría y Experticia
Revisiones de diseño, integración, despliegue. Contacto por LinkedIn: https://www.linkedin.com/in/carloshuggins
