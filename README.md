#  StockScan SGA — Sistema de Gestión de Almacenes Inteligente

<p align="center">
  <img src="logo_stockscan.png" alt="StockScan SGA Logo" width="350"/>
</p>

<p align="center">
  <b>Proyecto Intermodular — 2º DAM (Desarrollo de Aplicaciones Multiplataforma)</b><br>
  <i>Gestión de stock en tiempo real mediante escaneo inteligente para hostelería, e-commerce y logística.</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Sprint-Sprint%20(En%20cierre)-orange?style=for-the-badge" alt="Sprint 2">
  <img src="https://img.shields.io/badge/JDK-21-blue?style=for-the-badge&logo=openjdk" alt="Java 21">
  <img src="https://img.shields.io/badge/GUI-FlatLaf%20%2F%20Swing-informational?style=for-the-badge" alt="FlatLaf">
  <img src="https://img.shields.io/badge/Database-SQLite-green?style=for-the-badge&logo=sqlite" alt="SQLite">
  <img src="https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge" alt="Licencia">
</p>

---

##  ¿Qué es StockScan SGA?

**StockScan SGA** es una solución multiplataforma orientada al control y gestión inteligente de inventarios en tiempo real. Diseñado para optimizar la operativa en sectores exigentes como hostelería, comercio electrónico y distribución logística, el sistema permite la identificación automatizada de productos en estanterías a través de dispositivos móviles y de escritorio, reduciendo los tiempos de auditoría y eliminando los errores de rotura de stock.

---

##  Funcionalidades Principales

*  **Escáner Inteligente de Stock:** Identificación inmediata de productos y cajas en estanterías mediante lectura óptica con la cámara del dispositivo.
*  **Chat Interno y Comunicación:** Canal directo de mensajería en tiempo real entre administradores, supervisores y operarios de almacén/camareros.
*  **Agenda, Tareas y Check-in:** Control integral de turnos de trabajo, asignación de tareas operativas y registro digital de asistencia.
*  **Arquitectura Multi-sector:** Configuración flexible adaptada a las necesidades específicas de restaurantes, almacenes logísticos y tiendas online.
*  **Arquitectura Offline-First:** Persistencia local garantizada con sincronización en segundo plano para trabajar sin interrupciones en zonas de baja cobertura.

---

##  Estado del Proyecto

| Hito / Sprint | Estado | Entregables Clave |
| :--- | :---: | :--- |
| **Sprint 1** |  **Completado** | Definición de requisitos, diagrama de casos de uso, arquitectura base del sistema y prototipo inicial. |
| **Sprint 2** |  **Finalizando** | Implementación del módulo visual (Java Swing + FlatLaf), base de datos SQLite con jBCrypt, auditorías de accesibilidad (WCAG 2.1 / UNE-EN 301 549), RGPD y viabilidad legal. |
| **Sprint 3** |  *Próximamente* | Integración del motor de escaneo, comunicación en tiempo real del chat y pruebas de integración finales. |

---

##  Stack Tecnológico

* **Lenguaje Principal:** Java SE (JDK 21)
* **Interfaz Gráfica (GUI):** Java Swing + FlatLaf (Look & Feel Moderno / HiDPI)
* **Persistencia & Base de Datos:** SQLite (SQLite JDBC Driver)
* **Seguridad & Cifrado:** jBCrypt (Hashing de contraseñas de operarios)
* **Iconografía & UI Assets:** Lucide Icons / FontAwesome
* **Testing & Calidad:** JUnit 5

---

##  Miembros del Equipo y Roles

###  Equipo Frontend
* **Elena Sáez Lascurain** — *Desarrolladora Frontend & UX/UI*
* **Álvaro** — *Desarrollador Frontend*

###  Equipo Backend
* **Carmen Monge Montes** — *Desarrolladora Backend & Base de Datos*
* **Ángel Luis Sánchez Pérez** — *Desarrollador Backend & Arquitectura*

---

##  Licencia y Cumplimiento Legal

Este proyecto se distribuye bajo una **Licencia Propietaria Comercial (SaaS / On-Premise)**. La propiedad intelectual del código fuente, arquitectura y diseños pertenece exclusivamente al equipo desarrollador de StockScan SGA.

Todas las dependencias de terceros integradas (OpenJDK, FlatLaf, SQLite, jBCrypt) disponen de licencias permisivas (Apache 2.0, MIT, GPLv2 + Classpath Exception) compatibles con el uso comercial sin transmisión de efecto *copyleft*.
