<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ADMISICOLIE - Sistema de Admisiones y Matrículas</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
            background-color: #eafafc;; /* Color de fondo azul claro */
            background-image: url('file:///C:/Users/giane/Desktop/1-%20SENA%20-%20ANALISIS%20Y%20DESARROLLO%20DE%20SOFWARE/7-%20IMAGENES/logo_empresa-removebg-preview.png'); /* URL de la imagen de destello (puedes reemplazarla con tu propia imagen) */
            background-repeat: no-repeat; /* No repetir la imagen de fondo */
            background-position: top left/* Posición de la imagen de fondo */
        }
        #header {
            padding: 20px;
            background-color: #fcfcf9;
            border-bottom: 1px solid #733333;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        #logo-colegio {
            width: 100px;
            margin-right: 10px;
        }
        h1#titulo {
            color: orange; /* Color de la letra ADMISICOLIE */
            text-shadow: 2px 2px 4px #000000; /* Sombra del texto para darle un aspecto tridimensional */
        }
        #nombre-colegio {
            color: #1a237e; /* Color de la letra del colegio */
        }
        #login-form {
            width: 300px;
            margin: 50px auto;
            padding: 20px;
            background-color: #9df7db;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: left; /* Alinea el texto dentro del formulario a la izquierda */
        }
        #login-form h2 {
            color: #333;
        }
        #login-form label {
            display: block;
            margin-bottom: 10px;
            color: #555;
        }
        #login-form input[type="text"],
        #login-form input[type="password"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
        #login-form button {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            border: none;
            border-radius: 4px;
            color: #fff;
            cursor: pointer;
        }
        #login-form button:hover {
            background-color: #0056b3;
        }
        .error-message {
            color: red;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <div id="header">
        <img src="file:///C:/Users/giane/Desktop/1-%20SENA%20-%20ANALISIS%20Y%20DESARROLLO%20DE%20SOFWARE/7-%20IMAGENES/Logo_admisicolie-removebg-preview.png" alt="Logo del proyecto" style="width:100px;margin-right:10px;">
        <h1 id="titulo">ADMISICOLIE</h1>
    </div>
    <img id="logo-colegio" src="file:///C:/Users/giane/Desktop/1-%20SENA%20-%20ANALISIS%20Y%20DESARROLLO%20DE%20SOFWARE/7-%20IMAGENES/ESCUDO_SANTA_M__DE_LA_PROVIDENCIA-removebg-preview.png" alt="Logo del colegio">
    <h2 id="nombre-colegio">Colegio Santa Maria de la Providencia</h2>
    <div id="login-form">
        <h2>Iniciar Sesión</h2>
        <form action="login.php" method="post" onsubmit="return validarFormulario()">
            <label for="login">Usuario:</label>
            <input type="text" id="login" name="login" required>
            <label for="password">Contraseña:</label>
            <input type="password" id="password" name="password" required>
            <button type="submit">Ingresar</button>
        </form>
        <p class="error-message" id="error-message" style="display:none;">Contraseña incorrecta</p>
    </div>
    <script>
        function validarFormulario() {
            var login = document.getElementById("login").value;
            var password = document.getElementById("password").value;
            
            // Aquí deberías implementar la lógica real para validar las credenciales del usuario en tu backend
            // Por ejemplo, podrías hacer una solicitud HTTP a tu servidor y verificar las credenciales allí
            
            // Si la contraseña no es correcta, muestra un mensaje de error
            if (password !== "contraseña_correcta") {
                document.getElementById("error-message").style.display = "block";
                return false; // Detiene el envío del formulario
            }
            return true; // Permite el envío del formulario si las credenciales son correctas
        }
    </script>
</body>
</html>

