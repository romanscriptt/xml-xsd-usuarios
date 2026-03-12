Módulo: Lenguaje de Marcas — 1º DAM  
RA 4: Establece mecanismos de validación para documentos XML
Autor: Álvaro López De San Román
--------------------------------------------------------------

--> Archivos del proyecto

| Archivo | Descripción 

usuarios.xml | Documento XML con 3 usuarios de ejemplo 
usuarios.xsd | Esquema XSD que valida el XML 

--> Estructura del XML

Elemento raíz <usuarios> con varios <usuario>, cada uno con:
- Atributo id obligatorio en un formato que me gusta mucho para estos casos que es 001, 002, 003,...
- <nombreUsuario> → nombre de usuario
- <contrasena> → contraseña 
- <email> → correo electrónico
- <telefono> → teléfono 
- <codigoPostal> → código postal 

--> Expresiones regulares y estándares

| Campo | Regex | Estándar 

email | [a-zA-Z0-9._%+\-]+@[a-zA-Z0-9.\-]+\.[a-zA-Z]{2,6} | RFC 5322 |
telefono | \+34 [6-9][0-9]{2} [0-9]{3} [0-9]{3} | CNMC España |
codigoPostal | (0[1-9]\|[1-4][0-9]\|5[0-2])[0-9]{3} | Correos España |
nombreUsuario | [a-z][a-z0-9_]{2,19} | POSIX IEEE 1003.1 |
contrasena | [a-zA-Z0-9@#$%!&*+\-_]{8,} | NIST SP 800-63B |

--> Opinón 

Me ha gustado mucho la acatividad me ha servido a la hora de etsructurara mejor el xml 
y a la hora de utilizar el regstro regex en el xsd me ha gustado mucho ya que veo que esta 
parte es crucial entenderal al 100% para un fuuturo no tener problemas en difernetes casos de
tal forma que le exigimos al usuario casos que estan prestabelcidas 