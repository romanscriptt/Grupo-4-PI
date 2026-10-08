#  CAPÍTULO I: INTRODUCCIÓN

> **Proyecto:** StockScan SGA (SCAN ALMACÉN)  
> **Módulo:** Proyecto Intermodular - Desarrollo de Aplicaciones Multiplataforma (DAM)  
> **Entrega:** Sprint Review 01  

---

##  Índice de Contenidos

1. [Contexto del Proyecto](#1-contexto-del-proyecto)
   * [1.1. Descripción General](#11-descripción-general)
   * [1.2. Ficha Técnica del Prototipo](#12-ficha-técnica-del-prototipo)
   * [1.3. Sector y Ámbito Operativo](#13-sector-y-ámbito-operativo)
   * [1.4. Perfil de Usuarios](#14-perfil-de-usuarios)
   * [1.5. Entorno de Uso e Infraestructura](#15-entorno-de-uso-e-infraestructura)
   * [1.6. Naturaleza del Proyecto](#16-naturaleza-del-proyecto)
   * [1.7. Referencias Académicas](#17-referencias-académicas)
2. [Problema o Necesidad Detectada](#2-problema-o-necesidad-detectada)
   * [2.1. Objetivo y Fuente de Datos](#21-objetivo-y-fuente-de-datos)
   * [2.2. Perfil de los Encuestados](#22-perfil-de-los-encuestados)
   * [2.3. Diagnóstico del Control de Stock Actual](#23-diagnóstico-del-control-de-stock-actual)
   * [2.4. Dificultades Detectadas y Tiempos](#24-dificultades-detectadas-y-tiempos)
   * [2.5. Requisitos y Validación de la Propuesta](#25-requisitos-y-validación-de-la-propuesta)
   * [2.6. Resumen de la Necesidad Detectada](#26-resumen-de-la-necesidad-detectada)
3. [Propuesta de Solución](#3-propuesta-de-solución)
   * [3.1. Visión General de la Solución](#31-visión-general-de-la-solución)
   * [3.2. Funcionalidades Principales y Prioridad](#32-funcionalidades-principales-y-prioridad)
   * [3.3. Principios de Diseño UI/UX](#33-principios-de-diseño-uiux)
   * [3.4. Requisitos No Funcionales y Tecnología](#34-requisitos-no-funcionales-y-tecnología)
   * [3.5. Alcance por Fases y Gestión de Riesgos](#35-alcance-por-fases-y-gestión-de-riesgos)
4. [Objetivos del Proyecto](#4-objetivos-del-proyecto)
   * [4.1. Objetivo General](#41-objetivo-general)
   * [4.2. Objetivos Específicos](#42-objetivos-específicos)
5. [Alcance del Proyecto](#5-alcance-del-proyecto)
6. [Limitaciones y Exclusiones](#6-limitaciones-y-exclusiones)
   * [6.1. Limitaciones del Sistema (Factores Condicionantes)](#61-limitaciones-del-sistema-factores-condicionantes)
   * [6.2. Exclusiones del Alcance](#62-exclusiones-del-alcance)
7. [Estructura de la Memoria](#7-estructura-de-la-memoria)
8. [Puntos a Mejorar](#8-puntos-a-mejorar)
9. [Coevaluación del Equipo](#9-coevaluación-del-equipo)

---

## 1. Contexto del proyecto

### 1.1. Descripción General
Nuestra aplicación es un prototipo de Sistema de Gestión de Almacén (SGA) modular, escalable y de alto rendimiento, diseñado para entornos logísticos industriales, basada en la observación de distintas empresas como Sortly / Stockagile (Gestión de Stock), When I work / Factorial (Control de Turnos y Tareas) y Slack / Microsoft Teams (Comunicación Interna) dedicadas al sector de gestión y cómo se organizan.

La idea principal es diseñar una aplicación pensada para este tipo de empresas que ofrezca, a parte de la opción de gestionar el Stock, servicios como un chat integrado y un panel que se encarga de controlar los turnos y tareas de los trabajadores.

Además de estas observaciones que hemos contemplado en la investigación de las empresas, hemos recogido diversas opiniones en un formulario que hemos realizado que nos hace pensar en qué podríamos mejorar en nuestra futura aplicación y qué podríamos añadir o eliminar. La opinión general está recogida en el **Issue #32**.

Este repositorio recoge la documentación y el desarrollo del prototipo, que parte de una idea central: en un almacén, la calidad de la herramienta de software condiciona directamente la rapidez, la precisión y el bienestar de las personas que trabajan con ella.

---

### 1.2. Ficha Técnica del Prototipo

| Campo | Detalle |
| :--- | :--- |
| **Proyecto** | StockScan SGA (SCAN ALMACÉN) |
| **Tipo** | Prototipo de Sistema de Gestión de Almacén (SGA) |
| **Sector** | Logística industrial / gestión de almacenes |
| **Usuarios finales** | Operarios de almacén |
| **Dispositivos objetivo** | Pantallas industriales (HiDPI) y terminales PDA |
| **Estado** | Prototipo en desarrollo |

---

### 1.3. Sector y Ámbito Operativo
El proyecto se enmarca en la logística industrial, y en concreto en la gestión de almacenes.

**Procesos que abarca el ámbito del proyecto:**
* **Control de stock:** conocer qué hay, cuánto hay y dónde está.
* **Historial de movimientos:** registro de entradas, salidas y cambios de ubicación.
* **Picking:** preparación de pedidos recogiendo productos de sus ubicaciones.
* **Packing:** embalaje y preparación de los pedidos para su envío.

**Por qué importa este ámbito:**
* El *order picking* está identificado como la actividad más intensiva en mano de obra y más costosa de casi cualquier almacén, con un coste que se estima de hasta el 55 % del gasto operativo total del almacén [1].
* Un mal rendimiento en esta actividad se traduce en un servicio deficiente y en costes elevados para toda la cadena de suministro [1].

---

### 1.4. Perfil de Usuarios
La aplicación está pensada para los operarios de almacén.

| Característica del usuario | Implicación para el producto |
| :--- | :--- |
| Trabaja a un ritmo elevado y de forma continua | La interfaz no puede exigir pasos innecesarios |
| Realiza tareas repetitivas (escanear, identificar, confirmar) | Cada pantalla debe leerse de un vistazo |
| Trabaja en entornos de trabajo exigentes | Poco margen para interpretar pantallas complejas |
| Puede incorporarse en picos de demanda con poca experiencia | La herramienta debe ser fácil de aprender |

---

### 1.5. Entorno de Uso e Infraestructura
StockScan SGA está orientado a ejecutarse sobre pantallas industriales (HiDPI) y dispositivos PDA, habituales en los almacenes.

**Condiciones del entorno que influyen en el diseño:**
* Iluminación variable según la zona del almacén.
* Contraste y legibilidad dependientes del tipo de pantalla.
* Tamaño reducido de pantalla en dispositivos móviles tipo PDA.
* Rapidez y ausencia de errores como requisitos críticos.

---

### 1.6. Naturaleza del Proyecto
StockScan SGA es un prototipo con enfoque modular y escalable, orientado al diseño de sistemas industriales con interfaces de alta usabilidad (UI/UX).

| ✅ Es | ❌ No es |
| :--- | :--- |
| Un prototipo para validar el diseño de la interfaz | Un SGA comercial listo para producción |
| Un caso de estudio de usabilidad en entornos industriales | Un sustituto de un ERP completo |
| Una base documentada y extensible | Un producto cerrado |

---

### 1.7. Referencias Académicas
* **[1]** R. de Koster, T. Le-Duc, and K. J. Roodbergen, "Design and control of warehouse order picking: A literature review," *Eur. J. Oper. Res.*, vol. 182, no. 2, pp. 481–501, Oct. 2007. [Online]. Available: https://doi.org/10.1016/j.ejor.2006.07.009

---

## 2. Problema o necesidad detectada

### 2.1. Objetivo y Fuente de Datos
* **Fuente de datos:** Formulario de opinión pública (30 respuestas, 1/10/2026).
* **Objetivo:** Documentar el problema real que motiva StockScan SGA y la necesidad detectada en el mercado, apoyándonos en los datos recogidos en el formulario.

**Diagnóstico General del Problema:**
La gestión de stock es una tarea común a casi cualquier negocio, pero muchas organizaciones la resuelven con herramientas improvisadas o no la resuelven:
* El 63 % (19/30) controla el stock con Excel, papel o sin control formal.
* Las dificultades más repetidas son las roturas de stock y los errores al contar o apuntar.
* El 73 % de quienes hacen inventario semanal le dedica más de 1 hora.
* Falta información en tiempo real sobre el stock.

---

### 2.2. Perfil de los Encuestados
Participaron 30 personas con perfiles muy distintos:

| Perfil | Nº |
| :--- | :--- |
| Usuario/a interesado/a (sin relación directa) | 14 |
| Mozo/a de almacén | 5 |
| Encargado/a o administrador/a | 4 |
| Autónomo/a o dueño/a de negocio | 3 |
| Gestiona una tienda online | 2 |
| Trabajador/a de hostelería | 2 |

* **Sectores representados:** logística y distribución, comercio minorista, e-commerce, hostelería, construcción, administración, entre otros.

---

### 2.3. Diagnóstico del Control de Stock Actual

| Sistema actual | Respuestas | % |
| :--- | :--- | :--- |
| Sin control formal | 9 | 30 % |
| Excel / hoja de cálculo | 8 | 27 % |
| ERP / SGA | 7 | 23 % |
| Papel o libreta | 2 | 7 % |
| Escáner de códigos dedicado | 2 | 7 % |
| Otros (programa propio, TPV) | 2 | 7 % |

**Conclusiones:**
* El **63 %** trabaja con métodos manuales o sin control formal.
* Solo 2 de 30 usan un escáner dedicado: el hardware específico no está extendido.

---

### 2.4. Dificultades Detectadas y Tiempos

| Dificultad | Menciones |
| :--- | :--- |
| Roturas de stock (nos quedamos sin producto) | 13 |
| Errores al contar o apuntar | 11 |
| Mucho tiempo dedicado a inventarios | 7 |
| Falta de información en tiempo real | 6 |
| Exceso de stock o caducidades | 5 |

* El **80 % (24/30)** señala al menos un problema relevante.
* Las dos principales (roturas y errores de conteo) son consecuencia directa de procesos manuales o poco actualizados.

**Tiempo dedicado a inventarios (entre quienes realizan inventario semanal, 22 de 30):**
* **73 % (16)** dedica más de 1 hora a la semana.
* **41 % (9)** dedica más de 3 horas.
* Hay casos de 8-24 horas e incluso más de 1 día.
* **Satisfacción con el sistema actual:** la valoración más repetida es **3 sobre 5**, lo que indica un margen claro de mejora.

---

### 2.5. Requisitos y Validación de la Propuesta

**Lo más importante en un sistema de escaneo:**
1. Rapidez
2. Precisión
3. Facilidad de uso

* **Operatividad Offline:** 12 de 30 personas (40 %) pidieron que funcione sin internet.
* **Funcionalidades más valoradas:** Stock en tiempo real, alertas de stock bajo, escáner de estanterías con cámara, informes y estadísticas, chat interno y agenda de turnos/tareas (en menor medida).
* **Tecnología de identificación:** Más aceptados: código QR y código de barras tradicional. Minoritarios: DataMatrix y etiquetas RFID/NFC.
* **Preocupaciones sobre escanear con el móvil:** Privacidad de los datos (la más repetida, más de la mitad), batería, fiabilidad de la cámara y curva de aprendizaje (puntual).

**Validación de la Propuesta:**

| Pregunta clave | Resultado |
| :--- | :--- |
| ¿Usarías el móvil en lugar de un lector dedicado? | 67 % (20/30) «Sí» o «Probablemente sí»; 27 % (8/30) «Sí, sin dudarlo» |
| ¿Tu empresa probaría una herramienta así? | 50 % Sí · 37 % Tal vez · 13 % No |
| ¿Todo en una sola app o por separado? | Mayoría a favor de una sola app (chat + agenda + stock) |
| Dispositivo principal | Android como más habitual, seguido de iPhone, «ambos» y tablet |

* **Motivos de rechazo o duda:** Empresas grandes con sistema propio o equipo interno de desarrollo, o decisión dependiente de la dirección / coste-beneficio.
* **Beneficios más valorados:** Ahorro de tiempo, reducción de pérdidas y mermas, menos errores.

---

### 2.6. Resumen de la Necesidad Detectada
> Una herramienta de control de stock rápida, sencilla, barata y accessible desde el móvil, especialmente para pymes y negocios que hoy usan Excel, papel o nada.

---

## 3. Propuesta de solución

**Basada en:** necesidades detectadas en el formulario de opinión pública (30 respuestas).

**Objetivo:** Definir la solución que da respuesta a los problemas detectados: control de stock manual, errores de conteo, roturas de stock, inventarios lentos y falta de información en tiempo real.

**Propuesta:** StockScan SGA es un Sistema de Gestión de Almacén modular y escalable que convierte el móvil en el lector de códigos y centraliza el stock en tiempo real:
* Escaneo con el móvil (códigos QR y de barras) en lugar de un lector dedicado.
* Flujos simplificados para reducir el tiempo de escaneo e identificación.
* Validación y confirmación en tiempo real, con historial de movimientos.
* Alertas de stock bajo para evitar roturas.
* Interfaz de alto contraste con retroalimentación por color (verde, ámbar, rojo).
* Todo en una sola app: stock, chat interno y agenda de turnos/tareas.

---

### 3.1. Visión General de la Solución
StockScan SGA se organiza en módulos desacoplados, de forma que cada sector (logística, comercio, e-commerce, hostelería…) active solo lo que necesita.

| Componente | Usuario principal | Función |
| :--- | :--- | :--- |
| **App móvil** | Operarios (mozos, camareros, dependientes) | Escanear, consultar y confirmar movimientos de stock |
| **Panel de gestión** | Encargados y administradores | Ver stock en tiempo real, informes, alertas y configuración |
| **Núcleo de datos** | Todos | Stock, historial de movimientos y usuarios |

**Por qué esta estructura:**
* Cubre el perfil que escanea (operario) y el que decide (encargado) sin mezclar interfaces.
* La modularidad permite empezar con lo esencial y escalar sin rehacer el sistema.
* La mayoría de las personas encuestadas prefiere una sola app frente a herramientas separadas.

---

### 3.2. Funcionalidades Principales y Prioridad

| Necesidad detectada (formulario) | Funcionalidad propuesta | Prioridad |
| :--- | :--- | :--- |
| Errores al contar o apuntar (11 menciones) | Escaneo con la cámara + confirmación y validación en tiempo real | 🔴 Alta |
| Roturas de stock (13 menciones) | Alertas de stock bajo | 🔴 Alta |
| Falta de información en tiempo real (6 menciones) | Stock en tiempo real e historial de movimientos | 🔴 Alta |
| Mucho tiempo en inventarios (7 menciones) | Escáner de estanterías con cámara | 🟠 Media-alta |
| Informes y estadísticas | Panel de informes para administradores | 🟠 Media |
| Coordinación del equipo (hoy WhatsApp, Teams o Telegram) | Chat interno entre administradores y equipo | 🟡 Media |
| Organización de turnos y tareas | Agenda de turnos y tareas, check-in de asistencia | 🟡 Media |

>  **Nota:** Las funcionalidades de stock, escaneo y alertas fueron las más valoradas en el formulario, por eso se priorizan. Chat y agenda se valoraron menos, pero son parte del valor diferencial de tener «todo en una sola app».

---

### 3.3. Principios de Diseño UI/UX

**1. Tokens semánticos de color:**

| Color | Significado | Uso |
| :--- | :--- | :--- |
| 🟢 **Verde** | Éxito | Escaneo correcto, movimiento confirmado |
| 🔴 **Rojo** | Conflicto | Error, producto no encontrado, stock inconsistente |
| 🟠 **Ámbar** | Alerta | Stock bajo, caducidad próxima, revisión pendiente |

**2. Contraste extremo y legibilidad:**
* Paleta de alto contraste pensada para pantallas de móvil y PDA en entornos industriales.
* Textos y botones grandes, válidos para uso con una mano.

**3. Mínima carga cognitiva:**
* Un solo objetivo por pantalla y el menor número de pasos posible.
* Retroalimentación inmediata tras cada escaneo (color, vibración o sonido).
* Objetivo de diseño: escaneo e identificación en menos de 2 segundos.

>  **Nota:** El objetivo de 2 segundos es una meta de diseño. Hay que medirlo en pruebas de usabilidad con usuarios reales.

---

### 3.4. Requisitos No Funcionales y Tecnología

| Requisito | Motivo |
| :--- | :--- |
| Funcionamiento sin conexión (sincronización posterior) | Lo pidieron 12 de 30 personas |
| Privacidad y seguridad de los datos | Principal preocupación sobre el escaneo con móvil |
| Bajo consumo de batería | Segunda preocupación más repetida junto con la fiabilidad de la cámara |
| Lectura fiable de la cámara, también con poca luz | Condición para sustituir al lector dedicado |
| Multiplataforma (Android como prioridad, también iPhone) | Android fue el dispositivo más habitual |
| Escalabilidad | Pymes y empresas medianas de distintos sectores |

**Códigos de identificación:**
* **Soportados desde el inicio:** Código QR y código de barras tradicional (los más aceptados).
* **Valorables más adelante:** DataMatrix y etiquetas RFID/NFC (interés minoritario).

---

### 3.5. Alcance por Fases y Gestión de Riesgos

| Fase | Contenido |
| :--- | :--- |
| **Fase 1** | Escaneo con cámara (QR y barras), stock en tiempo real, historial de movimientos, alertas de stock bajo, interfaz con tokens semánticos |
| **Fase 2** | Modo offline con sincronización, informes y estadísticas, escáner de estanterías con cámara |
| **Fase 3** | Chat interno, agenda de turnos y tareas, check-in de asistencia, formatos adicionales (DataMatrix, RFID/NFC) |

**Riesgos y Puntos a Validar:**

| Riesgo | Mitigación |
| :--- | :--- |
| La cámara no es tan fiable como un lector dedicado | Pruebas con distintos móviles y condiciones de luz |
| Empresas grandes con sistema propio no adoptarán la herramienta | Orientarse a pymes y negocios con Excel, papel o sin control |
| Desconfianza por la privacidad de los datos | Comunicar y aplicar medidas de seguridad desde el diseño |
| El 63 % usa métodos manuales: puede haber resistencia al cambio | Interfaz muy simple y curva de aprendizaje mínima |

>  **Nota:** Esta distribución por fases es una propuesta del equipo y puede ajustarse al tiempo y los recursos disponibles en el Sprint.

---

## 4. Objetivos del proyecto

### 4.1. Objetivo General
Diseñar, desarrollar e implantar un Sistema de Gestión de Almacenes multiplataforma denominado StockScan SGA, un panel de gestión web y una aplicación móvil nativa/híbrida para operarios, orientado a optimizar la trazabilidad, gestión de ubicaciones y control de inventario en tiempo real mediante el uso de códigos de barras y notificaciones operativas [1].

#### Referencia
* **[1]** Asana, «Objetivos generales y específicos: qué son y ejemplos [2026] • Asana», Asana. Accedido: 7 de octubre de 2026. [En línea]. Disponible en: https://asana.com/es/resources/general-and-specific-objetives

---

### 4.2. Objetivos Específicos

1. **Analizar e identificar las necesidades del sector:**
   - Evaluar las ineficiencias de los procesos manuales en Pymes a partir de datos reales de mercado (estudio con 30 usuarios encuestados).
   - Definir los requisitos funcionales para los perfiles de Operario, Supervisor y Administrador.

2. **Diseñar la experiencia de usuario y sistema de interfaz adaptativo (UI/UX):**
   - Crear prototipos interactivos en Figma adaptados a pantallas móviles (PDAs) y de escritorio (Desktop).
   - Desarrollar un sistema de diseño unificado en Flutter con tokens semánticos (colores, tipografía y componentes industriales) optimizado para reducir la carga cognitiva del operario.

3. **Construir una arquitectura de software robusta y modular:**
   - Implementar el patrón Modelo-Vista-Controlador (MVC) junto con la capa Data Access Object (DAO) en Java.
   - Garantizar la mantenibilidad, escalabilidad y la total independencia entre la lógica de negocio y las interfaces gráficas.

4. **Desarrollar el módulo móvil operativo (Flutter Mobile / PDA):**
   - Implementar la lectura rápida de códigos de barras/QR mediante cámara o lector integrado para operaciones de entrada, salida y traspaso.
   - Integrar el registro instantáneo de mermas y roturas, emitiendo tickets digitales de devolución.
   - Incluir utilidades de fichaje de jornada laboral y chat interno en planta para la resolución de incidencias en vivo.

5. **Desarrollar el cuadro de mando de escritorio (Flutter Desktop / Web):**
   - Diseñar una interfaz adaptativa (*responsive*) mediante Layout Widgets de Flutter (`LayoutBuilder`, `Flex`, `Grid`) para monitores de supervisión.
   - Integrar la visualización de métricas en tiempo real (KPIs), alertas de stock bajo, historial de movimientos y gestión de roles/usuarios.

6. **Integrar la capa de datos e infraestructura local:**
   - Diseñar e implementar el modelo relacional de datos en SQLite utilizando conectores nativos de Flutter (`sqflite` / `drift`).
   - Garantizar rendimiento inmediato, cero latencia de red y capacidad de trabajo sin conexión a internet (*offline-first*).

---

### 5. Alcance del proyecto

---

## 6. Limitaciones y exclusiones

### 6.1. Limitaciones del Sistema (Factores Condicionantes)
Las limitaciones representan restricciones técnicas, operativas o de entorno bajo las cuales funcionará StockScan SGA:

* **Entorno de Red Local y Conectividad:**
  La aplicación móvil para operarios requiere conectividad continua Wi-Fi. Se asume una cobertura de red estable dentro del almacén, excluyendo la sincronización *offline* o la persistencia local en cola dentro del dispositivo móvil en este MVP.

* **Hardware de Escaneo:**
  El escaneo de códigos de barras/QR en la versión móvil dependerá exclusivamente de la cámara integrada del *smartphone* o PDA mediante librerías de visión por computador.

* **Gestión de Impresión:**
  La generación de etiquetas se limitará a la importación de los tickets a la aplicación para llevar a cabo la contabilidad de los materiales que se importen al inventario del almacén y poder manejar las posibles pérdidas.

---

### 6.2. Exclusiones del Alcance
Las exclusiones definen qué módulos o procesos de la logística industrial **no formarán parte del entregable** para acotar el desarrollo al Mínimo Viable (MVP):

* **Módulos Secundarios de la Interfaz:**
  Los módulos de Agenda y Chat interno quedan excluidos del alcance funcional principal del proyecto intermodular, pasando a considerarse posibles líneas de trabajo futuro para centrar el esfuerzo en la lógica logística (Stock, Ubicaciones, Trazabilidad y Alertas).

* **Logística Externa y Transporte:**
  No se contempla la integración con APIs de agencias de transporte ni el seguimiento de flotas fuera de las instalaciones físicas del almacén.

* **Integración ERP / Software de Terceros:**
  El sistema funcionará de forma independiente. No se desarrollarán conectores o *middleware* de integración automatizada con ERPs comerciales (SAP, Sage, Odoo) ni plataformas de *e-commerce* (WooCommerce, Shopify).

* **Gestión de Pasarelas de Pago y Facturación:**
  El sistema gestionará movimientos físicos de almacén y unidades en stock, pero no incluirá módulos de contabilidad, emisión de facturas legales ni cobro a clientes.

* **Algoritmos Avanzados de Rutas:**
  La asignación de ubicaciones de mercancía se realizará mediante reglas estáticas fijas definibles por el supervisor.

---

## 7. Estructura de la memoria

A continuación se detalla el guión de trabajo explícito que se va a seguir para la elaboración de la memoria técnica del proyecto **StockScan SGA**, estructurado por capítulos y fases metodológicas:

* **Capítulo I: Introducción:**  
  Contextualización del sector logístico, diagnóstico del problema a partir de datos de mercado ($N=30$), propuesta de solución (StockScan SGA), definición de objetivos (general y específicos), alcance, limitaciones/exclusiones y estructura de la memoria.

* **Capítulo II: Análisis del Dominio y Requisitos:**  
  Clasificación de empresas tipo, análisis de la competencia (*benchmarking* de soluciones existentes), especificación de requisitos funcionales mediante casos de uso (perfiles Operario, Supervisor y Administrador) y requisitos no funcionales (rendimiento, disponibilidad y seguridad).

* **Capítulo III: Diseño de Interfaz y Experiencia de Usuario (UI/UX):**  
  Definición de la arquitectura visual, creación del *Design System* (tokens semánticos, paleta cromática de alto contraste y tipografía industrial), prototipado interactivo en Figma y flujos de navegación optimizados para terminales móviles/PDAs y monitores *Desktop*.

* **Capítulo IV: Arquitectura Técnica y Modelo de Datos:**  
  Diseño arquitectónico basado en el patrón MVC, diagrama de clases, modelo Entidad-Relación y definición del esquema relacional de datos en SQLite con conectores de persistencia local.

* **Capítulo V: Desarrollo e Implementación:**  
  Construcción de módulos y componentes en Flutter (Mobile y Desktop/Web), implementación de la lógica del controlador, gestión de eventos, integración de lectura de códigos QR/barras y notificaciones operativas.

* **Capítulo VI: Pruebas, Conclusiones y Vías Futuras:**  
  Batería de pruebas unitarias y de integración, validación de resultados frente a los objetivos iniciales del proyecto y definición de líneas de trabajo futuro (modo *offline*, módulos de chat/agenda).

---

## 8. Puntos a mejorar

---

## 9. Coevaluación del equipo
