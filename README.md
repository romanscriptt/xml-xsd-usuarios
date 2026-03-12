# Validación XML con XSD

**Módulo:** Lenguaje de Marcas — 1º DAM  
**RA 4:** Establece mecanismos de validación para documentos XML  
**Autor:** Álvaro López De San Román

---

## Archivos del proyecto

| Archivo | Descripción |
|---|---|
| `usuarios.xml` | Documento XML con 3 usuarios de ejemplo |
| `usuarios.xsd` | Esquema XSD que valida el XML |

---

## Estructura del XML

Elemento raíz `<usuarios>` con varios `<usuario>`, cada uno con:

- Atributo `id` obligatorio con formato `U001`, `U002`, `U003`...
- `<nombreUsuario>` → nombre de usuario
- `<contrasena>` → contraseña
- `<email>` → correo electrónico
- `<telefono>` → teléfono
- `<codigoPostal>` → código postal

---

## Expresiones regulares y estándares

| Campo | Regex | Estándar |
|---|---|---|
| `email` | `[a-zA-Z0-9._%+\-]+@[a-zA-Z0-9.\-]+\.[a-zA-Z]{2,6}` | RFC 5322 |
| `telefono` | `\+34 [6-9][0-9]{2} [0-9]{3} [0-9]{3}` | CNMC España |
| `codigoPostal` | `(0[1-9]\|[1-4][0-9]\|5[0-2])[0-9]{3}` | Correos España |
| `nombreUsuario` | `[a-z][a-z0-9_]{2,19}` | POSIX IEEE 1003.1 |
| `contrasena` | `[a-zA-Z0-9@#$%!&*+\-_]{8,}` | NIST SP 800-63B |

---

## Demostración de validación

[![Ver en YouTube](https://img.shields.io/badge/YouTube-Ver%20vídeo-red?logo=youtube)](https://youtu.be/--l4bVfmJ0E)

Validado con **VSCode** + extensión **XML (Red Hat)** → 0 errores.

---

## Opinión

Me ha gustado mucho la actividad. Me ha servido para estructurar mejor el XML
y para utilizar expresiones regulares en el XSD. Veo que esta parte es crucial
entenderla al 100% para el futuro, ya que le exigimos al usuario formatos
preestablecidos que garantizan la integridad de los datos.
