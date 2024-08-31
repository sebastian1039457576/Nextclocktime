# Nextclocktime
// Función para mostrar la hora actual en tiempo real
function mostrarHora() {
    const fecha = new Date();
    const hora = fecha.getHours();
    const minutos = fecha.getMinutes();
    const segundos = fecha.getSeconds();
    const reloj = document.getElementById("reloj");

    reloj.textContent = `${hora}:${minutos}:${segundos}`;
}

// Función para validar el formulario de inicio de sesión
function validarFormulario() {
    const usuario = document.querySelector('input[name="usuario"]').value;
    const password = document.querySelector('input[name="password"]').value;

    if (usuario === "" || password === "") {
        alert("Por favor, completa todos los campos.");
        return false;
    }

    return true;
}

// Función para resaltar el menú activo
function resaltarMenu() {
    const secciones = document.querySelectorAll('nav ul li a');
    secciones.forEach((seccion) => {
        seccion.addEventListener('click', function() {
            secciones.forEach((item) => item.classList.remove('activo'));
            this.classList.add('activo');
        });
    });
}

// Función principal (main)
function main() {
    // Mostrar hora en tiempo real
    setInterval(mostrarHora, 1000);

    // Validar formulario de inicio de sesión
    const formulario = document.querySelector('form');
    formulario.addEventListener('submit', function(event) {
        if (!validarFormulario()) {
            event.preventDefault(); // Evita que el formulario se envíe si hay campos vacíos
        }
    });

    // Resaltar menú activo
    resaltarMenu();
}

// Ejecutar la función principal cuando el DOM esté listo
document.addEventListener('DOMContentLoaded', main);
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    
}
.registro-container {
    display: flex;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    width: 800px;
    max-width: 100%;
}
.registro-container img {
    width: 50%;
    height: auto;
    display: block;

}


.container p{
    text-align: justify;
}

.formulario {
    padding: 20px;
    width: 50%;
}
.formulario h2 {
    margin-bottom: 20px;
}
.formulario input[type="text"], .formulario input[type="email"], .formulario input[type="password"] {
    width: calc(100% - 20px);
    padding: 10px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}
.formulario input[type="submit"] {
    width: 100%;
    padding: 10px;
    background-color: #333;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
}
.formulario input[type="submit"]:hover {
    background-color: #555;
}


  
        
        .registro-container {
            display: flex;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            width: 800px;
            max-width: 100%;
        }
        .registro-container img {
            width: 50%;
            height: auto;
            display: block;
        }
        .formulario {
            padding: 20px;
            width: 50%;
        }
        .formulario h2 {
            margin-bottom: 20px;
        }
        .formulario input[type="text"], .formulario input[type="email"], .formulario input[type="password"] {
            width: calc(100% - 20px);
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .formulario input[type="submit"] {
            width: 100%;
            padding: 10px;
            background-color: #333;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        .formulario input[type="submit"]:hover {
            background-color: #555;
        }

    <div class="registro-container">
        <img src="tu-imagen.jpg" alt="Descripción de la imagen">
        <div class="formulario">
            <h2>Registro</h2>
            <form action="submit.php" method="post">
                <input type="text" name="nombre" placeholder="Nombre" required>
                <input type="email" name="email" placeholder="Email" required>
                <input type="password" name="password" placeholder="Contraseña" required>
                <input type="submit" value="Registrarse">
            </form>
        </div>
    </div>
</body>
</html>

<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>next clock time</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            display: grid;
            grid-template-columns: 1fr 1fr;
            grid-template-rows: auto 1fr auto;
            min-height: 100vh;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 10px;
            text-align: center;
            grid-column: 1 / -1;
        }
        nav {
            background-color: #555;
            padding: 10px;
            text-align: center;
            grid-column: 1 / -1;
        }
        nav ul {
            list-style-type: none;
            margin: 0;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin-right: 20px;
        }
        nav ul li a {
            color: #fff;
            text-decoration: none;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        img {
            max-width: 100%;
            height: auto;
            display: block;
            margin: auto;
            border-radius: 5px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
        }
        p {
            color: #555;
            line-height: 1.5;
        }
        footer {
            background-color: #333;
            color: #fff;
            padding: 10px;
            text-align: center;
            grid-column: 1 / -1;
        }
    </style>
</head>
<body>
    <header>
        <h1><b>Next Clock Time</b></h1>
        
  
    </header>
    <nav>
        <ul>
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#resumen">Ubicacion De Paquete </a></li>
            <li><a href="#opinion">Servicios</a></li>
            <li><a href="#detalles">Acerca de nosotros</a></li>
        </ul>
        
    </nav>
    <div id="inicio" class="container">
        <h2>Inicio</h2>
        <img src="gps8.avif" alt="next clock time">
        <p>Cómo rastrear un envío por número de pedido
            Los paquetes entregados por varias compañías de transporte privadas también pueden rastrearse por número de pedido. Un ejemplo es la tienda ASOS, que envía sus mercancías a los compradores mediante los servicios de paquetería wnDirect, TRAKPAK, SkyNet y otros.
            
            Sin embargo, todos los envíos se siguen principalmente con número de rastreo. Si usted no lo conoce, encuentre el pedido de su interés por número en su cuenta personal de la tienda en línea; a menudo ahí se indica el rastreo postal. Las tiendas pequeñas suelen enviarlo en un correo electrónico donde notifican sobre el envío de un pedido listo.
            
            Si no puede encontrar el número de rastreo, simplemente escriba y solicítelo al servicio de atención de la tienda, indicando el número de pedido.</p>
        
        <p>Bienvenido a la página de información del Next clock time.</p>
        <img src="gps22.jpg" alt="next clock time">
        <p> importancia de los sistemas de rastreo GPS para las empresas de transporte
empresas de logística en Valencia, La importancia de los sistemas de rastreo GPS para las empresas de transporte, docksdelevante
16 Mar La importancia de los sistemas de rastreo GPS para las empresas de transporte
PUBLICADO EN 11:15H IN BLOG BY ADMINISTADOR 0 COMENTARIOS
Como una de las empresas de logística en Valencia de mayor trayectoria a nivel nacional, somos conscientes de la importancia de implementar tecnología punta de rastreo de rutas. Y es que la excelencia siempre ha sido una prioridad para nosotros. En este sentido, los sistemas GPS de rastreo para empresas de transporte, como los ofrecidos por Docks de Levante, han contribuido tremendamente a mejorar la seguridad de la mercancía, así como los tiempos de entrega. 

¿Cómo ayudan los últimos sistemas de rastreo GPS a nuestra actividad?
Un sistema GPS de rastreo para empresas de transporte es un dispositivo electrónico que se instala en los vehículos para realizar seguimientos, a tiempo real, de su ubicación, velocidad, dirección, tiempo de recorrido y otros datos importantes. Esto permite monitorear las rutas en todo momento, lo que significa que pueden tomar decisiones informadas sobre la seguridad y el rendimiento de los vehículos. Pero hay más.

Máximo control de la mercancía
Además de mejorar el rendimiento del vehículo de carga y descarga de mercancía, los sistemas GPS de rastreo mejoran el control de los productos que se transportan. En definitiva, los errores en cualquiera de las fases que intervienen en las entregas, un lujo que ninguna empresa de logística y transporte se puede permitir, disminuyen al máximo. 

Fidelización de clientes
Al monitorear la ubicación de los vehículos, así como el estado de la carga, reduce los tiempos de entrega, lo que se traduce en un verdadero aumento de la satisfacción en la experiencia de usuario. Esto supone una auténtica ventaja competitiva. Y es que no hay nada como mantener la cartera de clientes intacta. 

Mejora de la eficiencia general de la empresa
El rastreo digital también mejora la eficiencia general de la empresa. Esto se debe a que los dispositivos permiten que los técnicos puedan controlar la ubicación de sus vehículos y cargas, así como la planificación al detalle cada ruta, lo que se traduce en una reducción de costes en términos de combustible y tiempos de trabajo. 


En conclusión, los sistemas GPS de rastreo para empresas de transporte son una herramienta esencial para mejorar la seguridad, el monitoreo de las rutas, el control de la mercancía, la eficiencia general, la mejora de los tiempos de entrega y, en definitiva, el servicio. 

¿Buscas la máxima calidad, eficacia y sostenibilidad en este tipo de trabajos? Contacta con Docks de Levante, una de las mejores empresas de logística en Valencia, y consulta nuestra carta de servicios online.</p>


        </div>
    <div class="container">
        <!-- Formulario de Iniciar Sesión -->
        <div class="form-container">
            <h2>Iniciar Sesión</h2>
            <form action="login.php" method="post">
                <input type="text" name="usuario" placeholder="Nombre de Usuario" required>
                <input type="password" name="password" placeholder="Contraseña" required>
                <div class="checkbox-container">
                    <label>
                        <input type="checkbox" name="remember">
                        Recuérdame
                    </label>
                    <div class="forgot-password">
                        <a href="#">¿Olvidaste tu contraseña?</a>
                    </div>
                </div>
    
                <input type="submit" value="Enviar">
            </form>
        </div>
    <div class="container">       
        </div>
    <div id="resumen" class="container">
        <h2>Asesor</h2>
        <img src="gps11.jfif" alt="next clock time">
        <p><strong>Autor:</strong> Sebastian mesa ortega</p>
        <p><strong>Género:</strong> Hombre</p>
        <p><strong>Fecha de Publicación:</strong> 13/08/24</p>
        <p><strong>Editorial:</strong> La editorial mis dos</p>
        <p><strong>Resumen:</strong> Un libro en el que ves la humanidad tanto lo bueno como lo malo.</p>
    </div>
    <div id="opinion" class="container">
        <h2>sobre nosotros</h2>
        <img src="gps3.jpg" alt="next clock time">
        <p>
            Gps:El mapa del tesoro: geolocalización, la herramienta de logística que todo CEO debe conocer
            La logística moderna se enfrenta a desafíos constantes, especialmente en un entorno impulsado por el comercio electrónico. En este contexto, la geolocalización se ha convertido en una herramienta fundamental para mejorar la experiencia del cliente y optimizar los procesos logísticos en tiempo real. En este artículo, exploraremos los beneficios y las tecnologías detrás de la geolocalización, destacando cómo puede impulsar la productividad y la seguridad en la industria logística.
            en el solistica trabajamos para brindar soluciones tecnologuicas que poteciar el exito y competitividad de nuestros  clientes 
            Gracias a los sistemas geolocalizador (GPS),Tenemos el control  de la trama se ata de manera magistral, ofreciendo una conclusión que te dejará pensando mucho tiempo después de haber cerrado el libro.</p>
   
    <footer>
        <p>Comunicate linea +13043642487</p>
    </footer>
    
</body>
</html>
