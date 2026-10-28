# StockScan SGA — Sistema de Gestión de Almacenes Inteligente

<p align="center">
  <img src="https://github.com/user-attachments/assets/397f44bc-698a-4786-83b8-885fd3b894c2" alt="StockScan SGA Logo" width="450"/>
</p>

<p align="center">
  <b>Proyecto Intermodular — 2º DAM (Desarrollo de Aplicaciones Multiplataforma)</b><br>
  Gestión de stock en tiempo real mediante escaneo inteligente para hostelería, e-commerce y distribución.
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=java,sqlite,git,github,idea,vscode" height="50" />
  <img src="https://cdn.simpleicons.org/openjdk/430098" height="50" alt="OpenJDK" />
  <img src="https://cdn.simpleicons.org/junit5/25A162" height="50" alt="JUnit5" />
</p>

---

## Descripción del Sistema

StockScan SGA es una solución multiplataforma orientada al control y gestión inteligente de inventarios en tiempo real. Diseñado para optimizar la operativa en sectores como hostelería, comercio electrónico y distribución logística, el sistema permite la identificación automatizada de productos en estanterías a través de dispositivos móviles y de escritorio, reduciendo los tiempos de auditoría y eliminando los errores de rotura de stock.

---

## Funcionalidades Principales

* **Escáner Inteligente de Stock:** Identificación inmediata de productos y cajas en estanterías mediante lectura óptica con la cámara del dispositivo.
* **Chat Interno y Comunicación:** Canal directo de mensajería en tiempo real entre administradores, supervisores y operarios de almacén o camareros.
* **Agenda, Tareas y Check-in:** Control integral de turnos de trabajo, asignación de tareas operativas y registro digital de asistencia.
* **Arquitectura Multi-sector:** Configuración flexible adaptada a las necesidades específicas de restaurantes, almacenes logísticos y tiendas online.
* **Arquitectura Offline-First:** Persistencia local garantizada con sincronización en segundo plano para trabajar sin interrupciones en zonas de baja cobertura.

---

## Estado del Proyecto

| Hito / Sprint | Estado | Entregables Clave |
| :--- | :---: | :--- |
| **Sprint 1** | **Completado** | Definición de requisitos, diagrama de casos de uso, arquitectura base del sistema y prototipo inicial. |
| **Sprint 2** | **Finalizando** | Implementación del módulo visual (Java Swing + FlatLaf), base de datos SQLite con jBCrypt, auditorías de accesibilidad (WCAG 2.1 / UNE-EN 301 549), RGPD y viabilidad legal. |
| **Sprint 3** | **Planificado** | Integración del motor de escaneo, comunicación en tiempo real del chat y pruebas de integración finales. |

---

## Stack Tecnológico

* **Lenguaje Principal:** Java SE (JDK 21)
* **Interfaz Gráfica (GUI):** Java Swing + FlatLaf (Look & Feel Moderno / HiDPI)
* **Persistencia & Base de Datos:** SQLite (SQLite JDBC Driver)
* **Seguridad & Cifrado:** jBCrypt (Hashing de contraseñas de operarios)
* **Iconografía & UI Assets:** Lucide Icons / FontAwesome
* **Testing & Calidad:** JUnit 5

---

## Miembros del Equipo y Roles

### Equipo Frontend
* **Elena Sáez Lascurain** — Desarrolladora Frontend & UX/UI
* **Álvaro** — Desarrollador Frontend

### Equipo Backend
* **Carmen Monge Montes** — Desarrolladora Backend & Base de Datos
* **Ángel Luis Sánchez Pérez** — Desarrollador Backend & Arquitectura

---

## Licencia y Cumplimiento Legal

Este proyecto se distribuye bajo una **Licencia Propietaria Comercial (SaaS / On-Premise)**. La propiedad intelectual del código fuente, arquitectura y diseños pertenece exclusivamente al equipo desarrollador de StockScan SGA.

Todas las dependencias de terceros integradas (OpenJDK, FlatLaf, SQLite, jBCrypt) disponen de licencias permisivas (Apache 2.0, MIT, GPLv2 + Classpath Exception) compatibles con el uso comercial sin transmisión de efecto copyleft.
