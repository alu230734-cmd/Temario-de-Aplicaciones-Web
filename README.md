# Temario-de-Aplicaciones-Web

Propósito de Aprendizaje 1: Comprender los fundamentos del desarrollo de aplicaciones web.
#  1.-Introducción al desarrollo web  #
##  Tipos de aplicaciones web  ##
## Aplicaciones web estáticas  ##
### Descripción: ###
Son páginas que muestran información fija, creada generalmente en HTML y CSS. El contenido no cambia hasta que se edita manualmente.  
Ejemplo:  
Portafolios, páginas de información básica.  
## Aplicaciones web dinámicas  ##
###  Descripción:  ###
El contenido puede cambiar en función de la interacción del usuario o la información extraída de una base de datos. Utilizan lenguajes como PHP, Python, Ruby, Node.js.  
Ejemplo:  
Blogs, tiendas en línea, sistemas de gestión de contenido (CMS).  
##  SPA (Single Page Application)  ##
###  Descripción:  ###
Toda la aplicación se carga en una sola página web. La navegación y las actualizaciones de contenido se realizan sin recargar la página, normalmente usando frameworks como React, Angular, o Vue.js.  
Ventajas:  
Experiencia de usuario fluida y rápida.  
Ejemplo:  
Gmail, Facebook, Twitter.  
## PWA (Progressive Web Application)  ##  
###  Descripción:  ###
Son aplicaciones web avanzadas que se comportan como aplicaciones nativas en dispositivos móviles. Usan tecnologías como Service Workers para funcionar offline y pueden instalarse en el dispositivo.  
Ventajas:  
Acceso offline, notificaciones push, instalación en el escritorio/móvil.  
Ejemplo:  
Twitter Lite, Pinterest.  


# 2.Arquitectura de aplicaciones web  #
1. Cliente-Servidor  
La arquitectura cliente-servidor es el modelo más básico de las aplicaciones web.  

###  Cliente:  ###
Es quien realiza las solicitudes (por ejemplo, un navegador web o una app móvil).  
### Servidor:  ###
Es quien recibe esas solicitudes, las procesa y envía una respuesta (por ejemplo, una página web, datos en formato JSON, etc.).  
Características:  

Separación de responsabilidades: el cliente se encarga de la interfaz y el servidor de la lógica y almacenamiento.
Comunicación mediante protocolos como HTTP/HTTPS.  
Ejemplo:  
Un usuario accede a www.ejemplo.com desde su navegador. El navegador (cliente) solicita la página; el servidor la envía.  

2. Arquitectura de tres capas  
En aplicaciones web modernas, se suele usar la arquitectura de tres capas:  

Capa de Presentación: Interfaz de usuario, lo que ve el usuario (HTML, CSS, JS).  
Capa de Lógica de Negocio: Procesa reglas, operaciones y la lógica de la aplicación (por ejemplo, el backend en Node.js, Java, Python).  
Capa de Datos: Gestiona el almacenamiento y recuperación de datos (base de datos como MySQL, MongoDB).  
Ventajas:  

Permite escalabilidad y mantenimiento.  
Separación clara de responsabilidades.  
Ejemplo:  
Un usuario registra su cuenta:  

Presentación: Formulario de registro (cliente).  
Lógica: Valida datos y crea usuario (servidor).  
Datos: Guarda usuario en la base de datos.  
3. REST y API-first design  
REST (Representational State Transfer):  

Es un estilo de arquitectura para diseñar servicios web.  
Utiliza HTTP y recursos identificados con URLs.  
Opera con métodos estándar (GET, POST, PUT, DELETE).  
Principios:  

Stateless (sin estado): Cada solicitud es independiente.  
Recursos: Todo se modela como recursos accesibles por URL.  
API-first design:  

Consiste en diseñar primero la API (Interfaz de Programación de Aplicaciones) antes de implementar el backend y frontend.  
Se define cómo será la comunicación entre cliente y servidor (formatos, endpoints, etc.).  
Facilita el trabajo paralelo de equipos y la integración con terceros.  
Ejemplo:  
Antes de crear la lógica para usuarios, se define el endpoint /api/users, qué datos acepta y devuelve, y cómo se comporta.  
#  3. -Lenguajes y tecnologías fundamentales  #
###  HTML (HyperText Markup Language)  ###
Es el lenguaje de marcado base para crear páginas web.  
Define la estructura y el contenido (texto, imágenes, enlaces, formularios, etc.).  
No es un lenguaje de programación, sino de estructuración.  
Ejemplo:

HTML  
<!DOCTYPE html>  
<html>  
  <head><title>Mi página</title></head>  
  <body>  
    <h1>Bienvenido</h1>  
    <p>Este es un párrafo de ejemplo.</p>  
  </body>  
</html>

### CSS (Cascading Style Sheets)  ### 
Es el lenguaje para definir la presentación y el diseño de las páginas web.  
Permite controlar colores, fuentes, posiciones, tamaños, animaciones, etc.  
Se puede incluir en el mismo archivo HTML o en archivos separados.  
Ejemplo:  

CSS  
body {  
  background-color: #f5f5f5;  
  font-family: Arial, sans-serif;  
}  

h1 {  
  color: blue;  
}  
### JavaScript  ###
Es el lenguaje de programación principal para la web.  
Permite añadir interactividad y dinamismo (validaciones, animaciones, interacción con APIs, etc.).  
Se ejecuta en el navegador del usuario (cliente).  
Ejemplo:  

JavaScript  
document.getElementById("miBoton").onclick = function() {  
  alert("¡Has hecho clic en el botón!");  
};  
###  PHP  ###  
Es un lenguaje de programación de propósito general, muy usado en el desarrollo web del lado del servidor (backend).  
Permite generar contenido dinámico, manejar formularios, sesiones, interactuar con bases de datos, etc.  
Se ejecuta en el servidor y genera HTML para el cliente.  
Ejemplo:  

PHP  
<?php  
echo "¡Hola, mundo!";  
?>  
###  MySQL  ##  
Es un sistema de gestión de bases de datos relacional.  
Permite almacenar, consultar y manipular datos de forma eficiente.  
Se usa comúnmente junto con PHP para crear aplicaciones web dinámicas (ejemplo: blogs, tiendas online, foros).  
Ejemplo de consulta SQL:  

SQL  
SELECT nombre, email FROM usuarios WHERE activo = 1;  

#  4.-Control de versiones  #

##  Git y GitHub  ##  
Git: Sistema de control de versiones distribuido para gestionar cambios en archivos de código.  
GitHub: Plataforma basada en Git para alojar repositorios, colaborar y compartir proyectos.  
Branching, Merge, Pull Requests:  
Branching: Crear ramas para desarrollar nuevas características sin afectar el código principal.  
Merge: Unir cambios de ramas al principal.  
Pull Request: Solicitud para revisar y fusionar cambios en GitHub, facilita la colaboración y revisión de código.  

<img width="309" height="163" alt="image" src="https://github.com/user-attachments/assets/e6cb248d-fc77-4e2e-9195-cec49ed39488" />

Propósito de Aprendizaje 2: Desarrollar componentes y funcionalidades de una aplicación web  
#  1.-Diseño e implementación del frontend  #
Maquetación/Wireframe/Mockup  
Herramientas y técnicas para planificar la interfaz antes de programar (Figma, Sketch, papel).  
Maquetación: Estructura visual con HTML/CSS.  
Wireframe: Boceto básico.  
Mockup: Diseño visual detallado.  
API  
El frontend consume APIs para obtener y mostrar datos dinámicos.  

#  2.-Diseño e implementación del backend  #
Servidor  
Software que recibe y procesa solicitudes del cliente (Node.js, PHP, Python).  
Manejo de peticiones y respuestas HTTP: Controla cómo se reciben (request) y responden (response) las solicitudes web.  
Conexión a bases de datos: Integración con sistemas como MySQL, PostgreSQL, MongoDB para almacenar y consultar datos.  
#  3.-Bases de datos  #
Modelado de datos y relaciones  
Diseño de tablas, campos y relaciones entre entidades (ej. usuarios y posts).  
ORM (Object Relational Mapping)  
Herramientas que permiten interactuar con bases de datos usando código orientado a objetos (ej. Sequelize, TypeORM, Doctrine).  
CRUD desde el backend  
Crear, Leer, Actualizar y Eliminar datos mediante el backend y la base de datos.  

#  4.-Seguridad básica en aplicaciones web  #
Validación de formularios  
Verificar datos del usuario antes de procesarlos para evitar errores y ataques.  
Autenticación y autorización  
Autenticación: Confirmar identidad del usuario (login).  
Autorización: Permitir o denegar acceso a recursos según el rol del usuario.  

<img width="275" height="183" alt="image" src="https://github.com/user-attachments/assets/3d472637-42e0-433e-b2c6-4e28158ab225" />

Propósito de Aprendizaje 3: Implementar y desplegar una aplicación web funcional  
#  1. -Integración de frontend y backend  #
Interfaz de usuario Frontend  
El frontend es la parte visual e interactiva de la aplicación (HTML, CSS, JavaScript, frameworks como React, Angular, Vue).  
Su propósito es permitir al usuario interactuar con la aplicación, visualizar datos y enviar acciones.  
Ejemplo: Formularios para registro/login, dashboards, listados de productos.  
Manejo de API  
El frontend se comunica con el backend mediante APIs (REST, GraphQL).  
Se usan métodos HTTP para enviar/recibir datos:  
GET para obtener datos  
POST para crear  
PUT/PATCH para actualizar  
DELETE para eliminar  
Ejemplo:  
JavaScript  
fetch("https://api.misitio.com/productos")  
  .then(res => res.json())  
  .then(data => mostrarProductos(data));  
Se recomienda validar datos antes de enviarlos y manejar errores (mensajes claros para el usuario).  
Proceso de Solicitud y Respuesta de Backend  
El backend recibe las solicitudes del frontend, procesa la lógica, accede a la base de datos y envía respuestas.  
Flujo típico:  
Usuario envía formulario desde frontend.  
Frontend envía datos a la API.  
Backend valida, procesa y responde (éxito o error).  
Buenas prácticas:  
Estructurar las respuestas de la API (ejemplo: {success: true, data: {...}}).  
Manejar excepciones y enviar mensajes claros.  

#  2.- Almacenamiento en Servidor
Tipos de servidores  
Servidor físico/dedicado: Hardware exclusivo, más caro pero mayor control.  
Servidor compartido: Recursos compartidos entre varias apps, más económico pero menos flexible.  
Servidor virtual (VPS): Simulación de servidor dedicado sobre hardware compartido, buen balance de precio y control.  
Cloud (nube): Recursos escalables, pago por uso (AWS, Azure, Google Cloud).  
Servicios de hosting  
Espacio donde se publica la aplicación web.  
Ejemplos populares:  
Heroku (fácil despliegue y escalabilidad)  
Vercel, Netlify (ideal para frontend y JAMstack)  
DigitalOcean, AWS EC2 (más control y potencia)  
Recomendaciones:  
Analiza necesidades de tráfico, seguridad y presupuesto antes de elegir.  
Proveedores de Servicios de Almacenamiento  
Ofrecen almacenamiento para archivos, bases de datos, backups.  
Ejemplo:  
Amazon S3 (archivos estáticos, imágenes)  
Firebase Storage  
Google Cloud Storage  

#  3.-Optimización y rendimiento  #
Optimización de recursos  
Imágenes: Comprimir y servir en formatos modernos (WebP).  
Scripts/CSS: Minificar y combinar archivos para reducir el tamaño.  
Carga asíncrona: Cargar recursos según se necesiten (lazy loading).  
CDN: Usar redes de distribución de contenido para servir recursos de forma global y rápida.  
Despliegue de aplicaciones web  
Publicar la app en Internet, configurando servidores, dominios y certificados SSL.  
Pasos básicos:  
Build/compilar la app  
Subir archivos al servidor/hosting  
Configurar el entorno (variables, base de datos, seguridad)  
Probar funcionamiento   
CI/CD básico  
Integración Continua (CI): Automatizar pruebas y revisiones de código cada vez que se suben cambios.  
Despliegue Continuo (CD): Automatizar el proceso de publicación de la app en servidores.  
Herramientas: GitHub Actions, GitLab CI, Travis CI.  
Ventajas:  
Menos errores humanos  
Despliegues rápidos y confiables  
Documentación del proyecto  
Escribir documentación clara y completa para que otros puedan instalar, usar y contribuir al proyecto.  
Incluye:  
Instrucciones de instalación y despliegue  
Uso de la API  
Estructura del proyecto  
Ejemplos de código  
Descripción de tecnologías empleadas  

<img width="950" height="534" alt="image" src="https://github.com/user-attachments/assets/1d922069-fdd8-4482-b68b-11b5fe86fc7a" />

