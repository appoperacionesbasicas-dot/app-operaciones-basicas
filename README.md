📄 README.md — Versión 1.0
📘 Generador de Operaciones Matemáticas

Aplicación web en HTML + CSS + JavaScript que genera operaciones matemáticas básicas (suma, resta, multiplicación y división) con números creados aleatoriamente según parámetros definidos por el usuario.

Los resultados completos se guardan en LocalStorage en formato JSON, permitiendo que las operaciones persistan aunque se refresque la página.

🚀 Características

✔ Generación automática de:

Sumas

Restas

Multiplicaciones

Divisiones (con cociente y residuo)

✔ Parámetros configurables:

Cantidad de elementos

Cantidad de cifras por número

Longitud del dividendo y divisor

Longitud del multiplicando y multiplicador

✔ Dos paneles principales:

Parámetros (con selectores del 1 al 10)

Operaciones generadas

✔ Las operaciones se guardan en:
localStorage["operaciones_math"]

✔ Se puede:

Generar nuevas operaciones

Recargar las operaciones guardadas desde JSON

Revisar el JSON en consola

🧱 Tecnologías

HTML5

CSS3

JavaScript Vanilla

LocalStorage para persistencia

📂 Estructura del proyecto
/
├── index.html   # Contiene toda la app (HTML, CSS y JS)
└── README.md    # Documentación del proyecto

🧩 Funcionamiento
🔹 Generación de números aleatorios

Cada número se genera con exactamente la cantidad de cifras indicada usando:

function randomNumero(digits) {
  const min = Math.pow(10, digits - 1);
  const max = Math.pow(10, digits) - 1;
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

🔹 Almacenamiento en JSON

Las operaciones se guardan así:

localStorage.setItem("operaciones_math", JSON.stringify(data));


Puedes ver el JSON en consola con:

JSON generado: [...]

▶️ Cómo usar
1. Descargar o clonar repositorio
git clone https://github.com/TU_USUARIO/TU_REPO.git

2. Abrir la aplicación

Solo abre index.html en tu navegador.
No requiere servidor ni dependencias.

🔮 Posibles mejoras futuras

Marcar operaciones como resueltas desde la interfaz

Historial de sesiones

Exportación del JSON

Modo oscuro

Validación avanzada en parámetros

Panel para revisar resultados detallados