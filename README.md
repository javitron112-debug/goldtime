# ⏱️ TimeTracker Pro

Una aplicación web progresiva (**PWA**), ligera y moderna diseñada bajo la filosofía estética de Apple para la gestión y cuantificación del tiempo dedicado a tareas o proyectos. Funciona completamente del lado del cliente (HTML/CSS/JavaScript nativo), de manera local y sin necesidad de bases de datos externas ni registros.

---

## ✨ Características Principales

* **⏱️ Doble Modo de Conteo:**
  * **Cronómetro (Count-up):** Ideal para registrar tareas de duración indeterminada.
  * **Alarma / Temporizador (Count-down):** Configura un tiempo límite (ej. bloques Pomodoro). Al finalizar, emite un aviso visual y acústico.
* **🔊 Alarma Integrada:** Genera un triple pitido electrónico limpio utilizando la API nativa `AudioContext` del navegador, garantizando funcionamiento sin archivos de audio externos.
* **🌗 Tema Dinámico Inteligente:** Soporta Modo Claro y Modo Oscuro. Detecta la preferencia del sistema operativo de manera automática e incluye un conmutador manual en la cabecera.
* **📱 Diseño Adaptativo y Mobile-First:** Interfaz táctil optimizada para teléfonos móviles, tablets y ordenadores con tipografía y dimensionamiento dinámico.
* **📥 Instalable como App (PWA):** Incluye manifiesto y configuraciones para agregarse a la pantalla de inicio en iOS (Safari) y Android (Chrome), funcionando como una aplicación nativa sin barras de navegación.
* **🧮 Suma Interactiva Personalizada:** Cada registro en el historial cuenta con casillas de selección. Puedes marcar manualmente qué tareas deseas sumar y ver el cómputo total en tiempo real.
* **💾 Almacenamiento Local Ilimitado:** Guarda de forma persistente miles de registros en el navegador mediante `localStorage`. Los datos se mantienen al cerrar la pestaña o apagar el equipo.
* **📊 Exportación Directa:** Botón para generar y descargar instantáneamente un reporte en formato `.csv` compatible con Microsoft Excel y Google Sheets con codificación UTF-8 (BOM).

---

## 🚀 Instalación y Uso

Al ser una aplicación autocontenida de un único archivo, no requiere dependencias ni servidores NodeJS:

1. Copia el código completo de la aplicación y guárdalo en tu equipo con el nombre `index.html` (o cualquier nombre con extensión `.html`).
2. Haz doble clic sobre el archivo para abrirlo en tu navegador favorito.
3. **Para móviles (Instalación):**
   * **iOS (Safari):** Pulsa el botón **Compartir** (icono del cuadro con la flecha hacia arriba) y selecciona **Añadir a la pantalla de inicio**.
   * **Android (Chrome):** Pulsa el menú de tres puntos superiores y selecciona **Instalar aplicación** o **Añadir a la pantalla de inicio**.

---

## 📁 Estructura del Código

El archivo cuenta con una arquitectura unificada en tres capas estándar:
* **HTML5:** Estructuración semántica con inputs adaptados para evitar comportamientos disruptivos en dispositivos móviles (como el zoom forzado en campos de texto).
* **CSS3:** Uso de variables nativas (`:root` y `[data-theme="dark"]`) y transiciones fluidas para el intercambio de temas visuales. Layouts flexibles mediante CSS Grid adaptativo.
* **JavaScript (ES6+):** Motor lógico asíncrono para la gestión del tiempo mediante `setInterval`, manipulación dinámica del DOM, serialización JSON para `localStorage` y sintetización de audio por hardware.

---

## 🛠️ Especificaciones Técnicas

* **Persistencia:** `window.localStorage` (~5MB de límite por dominio, permitiendo más de 30,000 registros de texto).
* **Audio:** Web Audio API (`OscillatorNode` de onda senoidal a 900Hz).
* **Exportación:** Separador por punto y coma (`;`) idóneo para configuraciones regionales en español de hojas de cálculo.

---

## 📄 Licencia

Este proyecto utiliza una licencia de código disponible con restricciones comerciales (**PolyForm Noncommercial License 1.0.0**).

* **Uso Personal y Educativo:** Completamente gratuito. Puedes descargar, modificar y usar la aplicación para gestionar tu propio tiempo de forma ilimitada.
* **Uso Comercial / Aplicaciones de Pago:** Queda estrictamente **prohibida** la venta, distribución comercial, sublicencia o inclusión de esta aplicación (o derivados de su código) en plataformas de pago, tiendas de aplicaciones (App Store, Google Play) o modelos SaaS sin una autorización expresa y un acuerdo de pago de regalías con el autor original.

Si deseas utilizar este software con fines comerciales o integrarlo en un producto de pago, por favor ponte en contacto con el autor para adquirir una **Licencia Comercial**.
⚠️ Una advertencia fáctica importante:
