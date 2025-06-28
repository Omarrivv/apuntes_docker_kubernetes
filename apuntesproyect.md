# Sistema Integral de Gestión para Restaurante

## 1. DECLARACIÓN DEL ALCANCE DEL PROYECTO

### Información Básica
- **Nombre del Proyecto:** Sistema Integral de Gestión para Restaurante "Sabores del Mundo"
- **Sector:** Restauración y servicios gastronómicos
- **Duración Estimada:** 5 meses (20 semanas)
- **Presupuesto:** S/. 295,000

### Descripción del Proyecto
Desarrollo e implementación de un sistema completo de gestión para restaurante que incluye módulos de reservas, gestión de mesas, punto de venta (POS), gestión de cocina, inventario de ingredientes, análisis de rentabilidad por plato y sistema de delivery integrado.

### Objetivos del Proyecto

**Objetivo Principal:** 
Crear una plataforma digital integral que automatice todos los procesos operativos del restaurante, desde la reserva hasta la entrega, mejorando la eficiencia operacional y la experiencia del cliente.

**Objetivos Específicos:**
- Reducir el tiempo de atención al cliente en un 30%
- Optimizar el control de inventario con alertas automáticas
- Implementar sistema de reservas online con confirmación automática
- Establecer análisis de rentabilidad por plato en tiempo real
- Integrar sistema de delivery con tracking en tiempo real
- Crear dashboard ejecutivo para toma de decisiones

### Alcance Incluido

**Módulos Principales:**
1. **Sistema de Reservas:** Reservas online, gestión de mesas, calendario de disponibilidad
2. **Punto de Venta (POS):** Toma de pedidos, división de cuentas, múltiples métodos de pago
3. **Gestión de Cocina:** Órdenes de cocina digitales, tiempos de preparación, estado de platos
4. **Inventario Inteligente:** Control de ingredientes, recetas con costos, alertas de stock mínimo
5. **Sistema de Delivery:** Integración con repartidores, tracking, estimación de tiempos
6. **Análisis y Reportes:** Rentabilidad por plato, análisis de ventas, reportes de desempeño
7. **Gestión de Personal:** Horarios, turnos, comisiones de meseros
8. **Sistema de Fidelización:** Programa de puntos, descuentos personalizados

**Funcionalidades Transversales:**
- Sistema de usuarios con roles diferenciados (gerente, cajero, mesero, cocinero, repartidor)
- Notificaciones en tiempo real
- Integración con redes sociales
- Sistema de feedback de clientes
- Backup automático y recuperación de datos

### Alcance Excluido
- Integración con sistemas contables externos (SAP, Contaplus)
- Aplicación móvil nativa para clientes
- Sistema de facturación electrónica SUNAT
- Integración con plataformas de delivery externas (Rappi, UberEats)
- Sistema de nómina y RRHH completo
- Marketing automation y email marketing

### Entregables
1. **Base de Datos:** Estructura optimizada con más de 25 tablas
2. **Backend API:** Servicios REST completos con documentación
3. **Frontend Web:** Interfaz responsive para todos los módulos
4. **Dashboard Móvil:** Versión optimizada para tablets
5. **Documentación Técnica:** Arquitectura, APIs, base de datos
6. **Manuales de Usuario:** Para cada rol del sistema
7. **Plan de Capacitación:** Material y cronograma de formación
8. **Soporte Post-Implementación:** 3 meses de soporte incluido

### Criterios de Aceptación
- **Rendimiento:** Tiempo de respuesta < 1.5 segundos para transacciones POS
- **Disponibilidad:** 99.7% de uptime durante horarios de operación
- **Usabilidad:** Interfaz intuitiva con máximo 3 clics para funciones principales
- **Compatibilidad:** Funcional en Chrome, Firefox, Safari, Edge
- **Seguridad:** Encriptación de datos de pago y cumplimiento PCI DSS
- **Escalabilidad:** Soporte para hasta 200 mesas y 500 pedidos simultáneos

---

## 2. ESTRUCTURA DE DESGLOSE DE TRABAJO (EDT)

```
SISTEMA INTEGRAL PARA RESTAURANTE
│
├── 1.1 ANÁLISIS Y PLANIFICACIÓN
│   ├── 1.1.1 Análisis de Procesos Actuales
│   ├── 1.1.2 Requerimientos Funcionales
│   ├── 1.1.3 Diseño de Arquitectura
│   ├── 1.1.4 Prototipado de Interfaces
│   └── 1.1.5 Plan Detallado de Proyecto
│
├── 1.2 INFRAESTRUCTURA Y BASE DE DATOS
│   ├── 1.2.1 Diseño del Modelo de Datos
│   ├── 1.2.2 Creación de Base de Datos
│   ├── 1.2.3 Stored Procedures y Triggers
│   ├── 1.2.4 Configuración de Servidor
│   └── 1.2.5 Seguridad y Backup
│
├── 1.3 DESARROLLO BACKEND
│   ├── 1.3.1 Core del Sistema y Autenticación
│   ├── 1.3.2 Módulo de Reservas
│   ├── 1.3.3 Módulo POS y Pagos
│   ├── 1.3.4 Módulo de Cocina
│   ├── 1.3.5 Módulo de Inventario
│   ├── 1.3.6 Módulo de Delivery
│   ├── 1.3.7 Módulo de Reportes
│   ├── 1.3.8 Integración de Pagos
│   └── 1.3.9 API Documentation
│
├── 1.4 DESARROLLO FRONTEND
│   ├── 1.4.1 Dashboard Principal
│   ├── 1.4.2 Interfaz de Reservas
│   ├── 1.4.3 Sistema POS
│   ├── 1.4.4 Panel de Cocina
│   ├── 1.4.5 Gestión de Inventario
│   ├── 1.4.6 Sistema de Delivery
│   ├── 1.4.7 Reportes y Analytics
│   └── 1.4.8 Responsive Design
│
├── 1.5 INTEGRACIÓN Y TESTING
│   ├── 1.5.1 Integración de Módulos
│   ├── 1.5.2 Testing Funcional
│   ├── 1.5.3 Testing de Performance
│   ├── 1.5.4 Testing de Seguridad
│   └── 1.5.5 User Acceptance Testing
│
├── 1.6 CAPACITACIÓN Y DOCUMENTACIÓN
│   ├── 1.6.1 Documentación Técnica
│   ├── 1.6.2 Manuales de Usuario
│   ├── 1.6.3 Material de Capacitación
│   └── 1.6.4 Sesiones de Entrenamiento
│
└── 1.7 IMPLEMENTACIÓN Y GO-LIVE
    ├── 1.7.1 Migración de Datos
    ├── 1.7.2 Configuración en Producción
    ├── 1.7.3 Pruebas Finales
    ├── 1.7.4 Go-Live
    └── 1.7.5 Soporte Post-Implementación
```

---

## 3. LÍNEA BASE DEL PROYECTO

### Línea Base del Alcance
- **Módulos Principales:** 8 módulos core del sistema
- **Roles de Usuario:** 6 tipos de usuarios (Gerente, Cajero, Mesero, Cocinero, Repartidor, Cliente)
- **Integraciones:** 3 integraciones principales (Pagos, SMS, Email)
- **Reportes:** 15 tipos de reportes diferentes
- **Funcionalidades:** 45 funcionalidades principales identificadas

### Línea Base del Cronograma

**Duración Total:** 20 semanas

**Distribución por Fases:**
- **Análisis y Planificación:** 2 semanas
- **Infraestructura y BD:** 2 semanas  
- **Desarrollo Backend:** 7 semanas
- **Desarrollo Frontend:** 5 semanas
- **Integración y Testing:** 2 semanas
- **Capacitación y Documentación:** 1 semana
- **Implementación:** 1 semana

**Hitos Críticos:**
- Semana 2: Aprobación de requerimientos
- Semana 4: Base de datos implementada
- Semana 11: Backend completo
- Semana 16: Frontend completo  
- Semana 18: Testing completado
- Semana 20: Go-Live exitoso

### Línea Base de Costos

**Recursos Humanos:** S/. 245,000
- Project Manager: S/. 50,000
- Líder Técnico: S/. 70,000
- Desarrollador Backend Senior: S/. 55,000
- Desarrollador Frontend: S/. 45,000
- DBA: S/. 35,000
- QA Tester: S/. 25,000
- Diseñador UX/UI: S/. 15,000

**Infraestructura y Licencias:** S/. 20,000
- Servidor en la nube: S/. 12,000
- Licencias de software: S/. 5,000
- Herramientas de desarrollo: S/. 3,000

**Otros Gastos:** S/. 8,000
- Capacitación: S/. 5,000
- Contingencias: S/. 3,000

**Contingencia (10%):** S/. 22,000

**TOTAL DEL PROYECTO:** S/. 295,000

---

## 4. OBJETIVOS DE GESTIÓN DE CALIDAD

### Objetivo General
Entregar un sistema robusto, confiable y fácil de usar que mejore significativamente la operación del restaurante, cumpliendo con todos los estándares de calidad de software y satisfaciendo completamente las expectativas del cliente.

### Objetivos Específicos de Calidad

#### 4.1 Calidad Funcional
- **Completitud:** 100% de casos de uso implementados según especificaciones
- **Precisión:** 99.9% de precisión en cálculos de precios y transacciones
- **Interoperabilidad:** Integración exitosa con 3 sistemas externos
- **Conformidad:** Cumplimiento con estándares PCI DSS para pagos

#### 4.2 Calidad de Rendimiento  
- **Tiempo de Respuesta:** < 1.5 segundos para transacciones críticas
- **Throughput:** Mínimo 500 transacciones por minuto
- **Disponibilidad:** 99.7% durante horarios de operación
- **Escalabilidad:** Soporte para crecimiento del 200% en volumen

#### 4.3 Calidad de Usabilidad
- **Facilidad de Aprendizaje:** 90% de usuarios competentes en < 1 hora
- **Eficiencia de Uso:** Reducción del 30% en tiempo de procesamiento de pedidos
- **Satisfacción del Usuario:** Score > 4.5/5 en encuestas post-implementación
- **Accesibilidad:** Cumplimiento con estándares WCAG 2.1

#### 4.4 Calidad de Mantenibilidad
- **Modularidad:** Arquitectura basada en microservicios
- **Documentación:** 100% de código documentado
- **Testabilidad:** 90% de cobertura en pruebas automatizadas
- **Modificabilidad:** Cambios menores implementables en < 2 días

### Métricas de Control de Calidad
- **Defectos por Módulo:** < 3 defectos críticos por módulo
- **Tiempo de Resolución:** < 4 horas para issues críticos
- **Code Review:** 100% del código revisado por pares
- **Performance Testing:** Pruebas de carga con 150% de capacidad esperada

---

## 5. ANÁLISIS DE RIESGOS - DIAGRAMA ISHIKAWA

### Problema Central: "Retrasos en la Implementación del Sistema"

#### Categoría: PERSONAS (People)
**Causas Identificadas:**
- Falta de experiencia del equipo en sistemas POS
- Alta rotación en el sector tecnológico
- Resistencia al cambio del personal del restaurante
- Sobrecarga de trabajo en temporadas altas
- **Impacto:** Alto - La experiencia específica es crítica
- **Probabilidad:** Media - Mercado laboral competitivo

#### Categoría: PROCESOS (Process)
**Causas Identificadas:**
- Cambios frecuentes en requerimientos por parte del cliente
- Proceso de aprobación lento entre stakeholders
- Falta de metodología ágil bien implementada
- Comunicación deficiente entre equipos técnicos y operativos
- **Impacto:** Alto - Los procesos deficientes generan retrabajos
- **Probabilidad:** Alta - Es común en proyectos de esta complejidad

#### Categoría: TECNOLOGÍA (Technology)
**Causas Identificadas:**
- Limitaciones de infraestructura del restaurante
- Problemas de conectividad a internet
- Incompatibilidad con hardware existente (impresoras, lectores)
- Actualizaciones de APIs de terceros (pasarelas de pago)
- **Impacto:** Medio - Pueden generar retrasos significativos
- **Probabilidad:** Media - Factores externos no controlables

#### Categoría: MÉTODOS (Methods)
**Causas Identificadas:**
- Subestimación de la complejidad de integración POS
- Planificación inadecuada de las pruebas en ambiente real
- Falta de estándares de desarrollo específicos para restaurantes
- Metodología de testing insuficiente para sistemas críticos
- **Impacto:** Alto - Métodos inadecuados comprometen calidad
- **Probabilidad:** Media - Requiere experiencia específica

#### Categoría: MATERIALES/RECURSOS (Materials)
**Causas Identificadas:**
- Presupuesto insuficiente para hardware especializado
- Falta de licencias de software necesarias
- Documentación técnica incompleta de sistemas existentes
- Datos históricos inconsistentes para migración
- **Impacto:** Medio - Pueden generar costos adicionales
- **Probabilidad:** Baja - Con buena planificación se mitiga

#### Categoría: MEDIO AMBIENTE (Environment)
**Causas Identificadas:**
- Regulaciones cambiantes en el sector gastronómico
- Condiciones del local (ruido, espacio, temperatura)
- Horarios de operación que limitan las pruebas
- Interferencias con operación normal del restaurante
- **Impacto:** Medio - Factores externos que complican implementación
- **Probabilidad:** Alta - Son factores del entorno operativo

---

## 6. MATRIZ DE ROLES Y RESPONSABILIDADES (RACI)

### Estructura del Equipo

| ROL | RESPONSABILIDADES PRINCIPALES |
|-----|-------------------------------|
| **Sponsor/Dueño** | Aprobar presupuesto, definir objetivos de negocio, resolver conflictos estratégicos |
| **Project Manager** | Planificar, ejecutar y controlar el proyecto, gestionar recursos y comunicación |
| **Líder Técnico** | Arquitectura del sistema, supervisión técnica, estándares de desarrollo |
| **Backend Developer** | APIs, lógica de negocio, integraciones, base de datos |
| **Frontend Developer** | Interfaces de usuario, experiencia del usuario, responsive design |
| **DBA** | Diseño de BD, optimización, seguridad de datos, backup/recovery |
| **QA Tester** | Casos de prueba, testing funcional, reporte de bugs |
| **UX/UI Designer** | Diseño de experiencia, prototipos, guías de interfaz |
| **Gerente Restaurante** | Requerimientos operativos, validación funcional, capacitación |

### Matriz RACI por Actividades Clave

| ACTIVIDAD | Sponsor | PM | Líder Téc | Backend | Frontend | DBA | QA | UX/UI | Gerente |
|-----------|---------|----|-----------|---------|---------|----|-------|-------|---------|
| **Definir Requerimientos** | A | R | C | C | C | I | I | C | C |
| **Diseño de Arquitectura** | I | C | R/A | C | C | C | I | I | I |
| **Desarrollo Backend** | I | C | C | R/A | I | C | I | I | I |
| **Desarrollo Frontend** | I | C | C | C | R/A | I | I | C | C |
| **Diseño de Base de Datos** | I | C | C | C | I | R/A | I | I | C |
| **Testing del Sistema** | I | C | C | I | I | I | R/A | I | C |
| **Diseño de Interfaces** | I | C | I | I | C | I | I | R/A | C |
| **Capacitación Usuarios** | I | R | I | I | I | I | I | I | A |
| **Go-Live** | A | R | C | C | C | C | C | I | C |
| **Soporte Post-Implementación** | I | R | C | C | C | C | I | I | A |

**Leyenda:**
- **R (Responsible):** Ejecuta la actividad
- **A (Accountable):** Aprueba y es responsable del resultado
- **C (Consulted):** Es consultado antes de decidir
- **I (Informed):** Es informado del resultado

---

## CONCEPTOS CLAVE EXPLICADOS

### 1. **Declaración del Alcance (Project Scope Statement)**
Es el documento fundamental que define QUÉ se va a hacer y QUÉ NO se va a hacer en el proyecto. Incluye:
- **Objetivos:** El "para qué" del proyecto
- **Entregables:** Los productos concretos que se van a crear
- **Criterios de Aceptación:** Cómo sabemos que está bien hecho
- **Exclusiones:** Lo que específicamente NO se incluye

### 2. **EDT - Estructura de Desglose de Trabajo (WBS)**
Es la descomposición jerárquica de TODO el trabajo del proyecto en paquetes manejables:
- **Nivel 1:** El proyecto completo
- **Nivel 2:** Fases principales 
- **Nivel 3:** Entregables específicos
- **Nivel 4:** Paquetes de trabajo (work packages)

### 3. **Línea Base (Baseline)**
Son los planes aprobados que sirven como referencia para medir el progreso:
- **Línea Base del Alcance:** Qué se va a entregar
- **Línea Base del Cronograma:** Cuándo se va a entregar
- **Línea Base de Costos:** Cuánto va a costar

### 4. **Gestión de Calidad**
Asegura que el proyecto cumpla con los requisitos de calidad:
- **Planificación:** Definir estándares y métricas
- **Aseguramiento:** Procesos para cumplir estándares
- **Control:** Monitoreo y corrección de desviaciones

### 5. **Análisis de Causa Raíz (Ishikawa)**
Herramienta para identificar las causas fundamentales de problemas potenciales:
- **6M:** Mano de obra, Métodos, Máquinas, Materiales, Medición, Medio ambiente
- **Objetivo:** Prevenir problemas antes que ocurran

### 6. **Matriz RACI**
Define quién hace qué en cada actividad del proyecto:
- Elimina confusiones sobre responsabilidades
- Asegura que alguien sea responsable de cada tarea
- Facilita la comunicación y coordinación

### Diferencias Clave entre los Dos Proyectos

| ASPECTO | BODEGA DE LICORES | RESTAURANTE |
|---------|-------------------|-------------|
| **Complejidad Operativa** | Media - Principalmente inventario y ventas | Alta - Operaciones en tiempo real |
| **Usuarios Concurrentes** | Moderado - Clientes online | Alto - Staff + clientes simultáneos |
| **Criticidad de Tiempo** | Baja - Pedidos pueden esperar | Muy Alta - Servicio inmediato |
| **Integración Hardware** | Básica - Lectores de código | Compleja - POS, impresoras, cocina |
| **Variabilidad de Procesos** | Baja - Procesos estándar | Alta - Cada mesa es diferente |

Ambos proyectos requieren una gestión rigurosa pero con enfoques diferentes según la naturaleza operativa del negocio.
