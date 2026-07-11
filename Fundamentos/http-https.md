## 🌍 HTTP y HTTPS

**HTTP (HyperText Transfer Protocol)** y **HTTPS (HyperText Transfer Protocol Secure)** son los protocolos que permiten la comunicación entre un cliente (navegador) y un servidor web. 

La comunicación funciona bajo un esquema de:

```bash
 Solicitud (Request) → Respuesta (Response).
```

El cliente solicita recursos.
El servidor los procesa y responde.


## 🔓 HTTP

Es el protocolo base de la Web, utilizado para la transferencia de documentos hipertexto.

### Caracteristicas:

- Comunicación cliente-servidor
- Basado en solicitudes y respuestas
- No cifra la información
- Los datos viajan en texto plano
- vulnerable a interceptaciones
- No valida la identidad del servidor

Fue el estándar inicial para la transmisión de páginas web.

## 🔐 HTTPS

Es la versión segura de HTTP, diseñada para proteger la comunicación en la Web.

### Caracteristicas:

- Utiliza cifrado SSL/TLS
- Cifra los datos transmitidos
- Protege información sensible 
- Previene ataques de intermediarios (MITM)
- Verifica la identidad del servidor mediante certificados digitales

Actualmente es el estándar de seguridad en Internet.
