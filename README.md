# Sistema ERP Gerentus.com v26

**Sistema ERP Gerentus.com** moderno, modular y escalable diseñado para digitalizar y optimizar la gestión integral de empresas.  
Integra en una sola plataforma todos los procesos del negocio, desde ventas y compras hasta contabilidad y remuneraciones, facilitando la toma de decisiones con información en tiempo real.

Orientado a empresas que buscan eficiencia, trazabilidad y cumplimiento normativo, Factrónica permite centralizar la operación, reducir errores operativos y aumentar la productividad mediante automatización y conectividad entre áreas.

Su arquitectura flexible permite adaptarse a distintos rubros y crecer junto con las necesidades del negocio.

# 🌐 Sistema Web Multiusuario y Multiempresa

Bienvenido al repositorio oficial de **Sistema ERP Gerentus.com**, un sistema 100% web, multiusuario y multiempresa diseñado para ofrecer rendimiento, escalabilidad y seguridad, con comunicación API REST y tecnología PHP + JavaScript.

---

## 🚀 Características Principales

- ✅ **100% Web Responsive**
- 👥 **Multiusuario y Multiempresa**
- 🔄 **Peticiones Asíncronas con API REST**
- 🗂️ **Estructura Modular con MVC en el Frontend**
- 🔐 **Base de Datos Segura con Acceso Restringido**
- 📦 **Backend PHP con Arquitectura en Capas Distribuida**
- 🖥️ **Frontend en JavaScript Vanilla + Bootstrap**
- 🌟 **Interfaz Amigable y Adaptable a Dispositivos**

---

## 🏗️ Arquitectura del Sistema

El sistema está construido bajo una **arquitectura N-Tier distribuida** con separación física y lógica:

[Cliente Web]  
⬇️ AJAX / REST  
[Servidor 3 - Frontend]  
⬇️ API REST  
[Servidor 2 - Backend (PHP API)]  
⬇️ MySQL  
[Servidor 1 - Base de Datos]

# ⚙️ Arquitectura del Sistema:

## SSR Inicial + CSR Incremental

Factronica ERP utiliza una arquitectura **mixta** moderna, combinando lo mejor de **Server-Side Rendering (SSR)** con una capa dinámica de **Client-Side Rendering (CSR)**.
Este enfoque permite una experiencia rápida, interactiva y optimizada tanto para el usuario como para los motores de búsqueda.

---

## 🧩 1. Fase de Carga Inicial (SSR)

🖥️ **Renderizado del lado del servidor**

- Al acceder al sistema por primera vez, el servidor PHP genera y entrega el HTML completo de la página.
- Esto permite que el navegador muestre contenido inmediatamente, incluso si JavaScript aún no ha cargado.
- Beneficio: excelente rendimiento inicial y compatibilidad con SEO.

## 🧩 2. Interactividad Dinámica (CSR Incremental)

🧠 **Comportamiento del lado del cliente**

Una vez cargada la interfaz, JavaScript se activa para gestionar eventos e interacciones del usuario.

Al pulsar botones o realizar acciones, se ejecutan llamadas fetch() para traer componentes HTML parciales desde scripts PHP.

Luego, esos fragmentos HTML se insertan dinámicamente en el DOM (innerHTML o similar).
Esto permite cargar solo lo necesario, reduciendo carga innecesaria y mejorando la experiencia del usuario.

🧱 Ventajas de esta arquitectura  
✅ Carga rápida inicial  
✅ Contenido visible aún sin JavaScript  
✅ Actualización dinámica de partes del DOM  
✅ Menor consumo de red y recursos  
✅ Mejor experiencia de usuario (UX)

🧭 Comparación con otras arquitecturas

Arquitectura Inicial rápido Interactivo SEO friendly Complejidad  
SSR puro ✅ ❌ ✅ 🔽 Simple  
CSR puro ❌ ✅ ❌ 🔼 Alta  
SSR + CSR (tu caso) ✅ ✅ ✅ ⚖️ Balanceado

📌 Resumen Técnico  
Factronica ERP está bien alineado con un modelo moderno y eficiente, donde:

El servidor se encarga del renderizado inicial ✅

El cliente se encarga de la interacción dinámica ✅

Este enfoque híbrido ofrece performance, escalabilidad e interactividad, manteniendo el desarrollo en PHP con JavaScript nativo sin necesidad de frameworks pesados.

# Secciones del Sistema ERP

## 📦 Sección Catálogo

Administra la información maestra de productos, servicios, categorías, unidades de medida y precios. Sirve como base central para todas las operaciones del sistema, garantizando datos consistentes y organizados.
[Ver Lista de Módulos Sección Catálogo](https://github.com/FacTronica/erpfactronica/blob/main/secciones/catalogo.md)

## 🧾 Sección Ventas

Gestiona todo el ciclo de ventas, desde cotizaciones hasta la emisión de documentos tributarios como facturas, boletas y notas de crédito. Incluye control de clientes, precios especiales, condiciones de pago y seguimiento de ventas.
[Ver Lista de Módulos Sección Ventas](https://github.com/FacTronica/erpfactronica/blob/main/secciones/ventas.md)

## 📥 Sección Compras

Controla el proceso de adquisición de bienes y servicios. Permite generar órdenes de compra, registrar recepciones, gestionar proveedores y controlar precios y condiciones de compra.
[Ver Lista de Módulos Sección Compras](https://github.com/FacTronica/erpfactronica/blob/main/secciones/compras.md)

## 🚚 Sección Logística

Coordina el flujo de productos desde la recepción hasta la entrega. Incluye gestión de inventarios, bodegas, movimientos internos, despachos y trazabilidad de productos en tiempo real.
[Ver Lista de Módulos Sección Logística](https://github.com/FacTronica/erpfactronica/blob/main/secciones/logistica.md)

## 💰 Sección Tesorería

Administra los flujos de caja, cuentas por cobrar y pagar, conciliaciones bancarias y planificación financiera. Brinda visibilidad y control del estado financiero diario de la empresa.
[Ver Lista de Módulos Sección Tesorería](https://github.com/FacTronica/erpfactronica/blob/main/secciones/tesoreria.md)

## 🏭 Sección Producción

Controla y gestiona los procesos productivos de la empresa, desde la planificación de la producción hasta el control de insumos, órdenes de trabajo, tiempos y costos de fabricación. Permite transformar materias primas en productos terminados de forma eficiente y trazable, integrándose con inventario, compras y ventas.
[Ver Lista de Módulos Sección Producción](https://github.com/FacTronica/erpfactronica/blob/main/secciones/produccion.md)

## ⏱️ Sección Control de Asistencia

Registra y supervisa la asistencia, puntualidad y jornadas laborales del personal. Permite llevar un control detallado de entradas, salidas, horas trabajadas, atrasos, ausencias y permisos, integrándose con el módulo de remuneraciones para el cálculo preciso de sueldos y cumplimiento de normativas laborales.
[Ver Lista de Módulos Sección Asistencia](https://github.com/FacTronica/erpfactronica/blob/main/secciones/asistencia.md)

## 🗂️ Sección Proyectos

Permite planificar, ejecutar y supervisar proyectos internos o para clientes. Gestiona tareas, recursos, presupuestos, tiempos y responsables, facilitando el seguimiento del avance y control de costos en cada etapa del proyecto. Se integra con otras áreas como compras, tesorería y recursos humanos para una gestión integral.
[Ver Lista de Módulos Sección Proyectos](https://github.com/FacTronica/erpfactronica/blob/main/secciones/proyectos.md)

## 🤝 Sección CRM

Gestiona las relaciones con los clientes, desde la captación de oportunidades hasta el seguimiento postventa. Permite registrar interacciones, agendar actividades, administrar contactos y analizar el ciclo de vida del cliente para mejorar la atención, fidelización y las oportunidades comerciales.
[Ver Lista de Módulos Sección CRM](https://github.com/FacTronica/erpfactronica/blob/main/secciones/crm.md)

## 👥 Sección Remuneraciones

Gestiona contratos, liquidaciones, imposiciones, horas extras, ausencias y todos los aspectos relacionados con la administración del personal, cumpliendo con la normativa laboral vigente.
[Ver Lista de Módulos Sección Remuneraciones](https://github.com/FacTronica/erpfactronica/blob/main/secciones/remuneraciones.md)

## 📘 Sección Contabilidad

Automatiza el registro contable de todas las operaciones del sistema. Genera libros contables, balances, estados financieros y declaraciones tributarias, integrándose con otros módulos para asegurar una contabilidad actualizada y precisa.
[Ver Lista de Módulos Sección Contabilidad](https://github.com/FacTronica/erpfactronica/blob/main/secciones/contabilidad.md)
