# 📊 ERP Gerentus — Guía Profesional para Desarrollo de Gráficos Estadísticos

Este documento describe la **metodología oficial** para la creación e integración de nuevos componentes de gráficos en el sistema **ERP Gerentus**.  
Su propósito es asegurar un desarrollo **estandarizado, escalable y mantenible**.

---

## 📂 Ubicación de la Plantilla

La carpeta base para iniciar un nuevo gráfico se encuentra en:

```bash
erp/sistema/ayuda_plantilla_graficos
```

---

## 🚀 Flujo de Trabajo para Crear un Nuevo Gráfico

### 1️⃣ Clonar la plantilla

- Copiar la carpeta `ayuda_plantilla_graficos`.
- Renombrarla con el nombre solicitado, por ejemplo:
  ```bash
  nuevacarpetaejemplo
  ```

---

### 2️⃣ Editar la Vista Principal (`vista/vista.php`)

Realizar los siguientes cambios:

- 🔹 **2.1 Nombre del Gráfico** → Actualizar el título mostrado en la vista.
- 🔹 **2.2 Nombre del Botón** → Cambiar el texto para identificar la acción del gráfico.
- 🔹 **2.3 Función Asociada** → Modificar el nombre de la función PHP/JS correspondiente.

---

### 3️⃣ Editar el Modelo (`modelo/modelo.php`)

- 🔹 **3.1 Nombre del Endpoint**  
  Definir un endpoint único para el nuevo gráfico:
  ```php
  $endpoint = "nuevacarpetaejemplo";
  ```

Cada gráfico debe tener su propio endpoint para mantener independencia en el consumo de datos.

---

### 4️⃣ Editar el Controlador (`controlador/controlador.js`)

- 🔹 **4.1 Función Principal**

  ```javascript
  function crearGraficoEjemplo() { ... }
  ```

- 🔹 **4.2 URL del Proxy**

  ```javascript
  const url_endpoint = "../nuevacarpetaejemplo/modelo/modelo.php";
  ```

- 🔹 **4.3 Objeto Canvas**

  ```javascript
  const ctx = document.getElementById("canvas_graficoNN").getContext("2d");
  ```

- 🔹 **4.4 Función Autoejecutable**
  ```javascript
  CrearGraficoNN();
  ```

---

## 🧪 Prueba Unitaria del Gráfico

Para probar el gráfico antes de integrarlo al dashboard:

1. Editar el archivo:
   ```bash
   nuevacarpetaejemplo/index.php
   ```
2. Descomentar las siguientes líneas:
   ```php
   include("../librerias/php/header.php");
   ```
   ```html
   <script src="../librerias_chartjs/Chart.min.js"></script>
   <script
     src="../librerias/javascript/header.js<?php echo "
     ?t=" . time(); ?>"
   ></script>
   ```
3. Ejecutar el gráfico accediendo a:
   ```bash
   https://v24.sistemafactronica.cl/erp/sistema/nuevacarpetaejemplo
   ```

De esta forma, podrá **visualizar y depurar errores** directamente en el navegador.

---

## 📊 Integración del Gráfico en el Dashboard

1. Volver a **comentar** las líneas modificadas en:

   ```bash
   nuevacarpetaejemplo/index.php
   ```

2. Editar el dashboard en la ruta:

   ```bash
   sistema/dashboard/dashboard_gerencia_general_10.php
   ```

3. Incluir el nuevo gráfico con:

   ```php
   <?php
   include("../nuevacarpetaejemplo/index.php");
   ?>
   ```

4. Verificar que el usuario tenga asignado el escritorio **Gerencia General 10** para visualizarlo.

---

## ✅ Buenas Prácticas Recomendadas

- 📝 Usar nombres **claros y descriptivos** para funciones, endpoints y carpetas.
- 💡 Comentar el código para facilitar el mantenimiento.
- 📂 Mantener la estructura de carpetas del ERP.
- 🌐 Probar en distintos navegadores antes de liberar el gráfico.
- 🔒 Asegurar independencia entre gráficos mediante endpoints únicos.

---

📌 Con este procedimiento garantizamos que los gráficos estadísticos en **ERP Factronica** sean desarrollados con un **estándar moderno, profesional y confiable**.
