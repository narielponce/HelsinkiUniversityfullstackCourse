# Comunicación HTTP usando el método POST

Este documento describe el flujo de comunicación cuando se envía un formulario desde el front-end al back-end usando el método POST.

```mermaid
sequenceDiagram
    participant Usuario
    participant Navegador
    participant Servidor

    Usuario ->> Navegador: Llena el formulario y presiona "Enviar"
    Note right of Usuario: El navegador prepara una solicitud HTTP POST
    
    Navegador ->> Servidor: Envía la solicitud HTTP POST con los datos del formulario
    Note right of Navegador: La solicitud incluye la URL, cabeceras y el cuerpo con los datos del formulario
    
    Servidor ->> Servidor: Procesa los datos del formulario
    Note right of Servidor: Validación, almacenamiento en base de datos, etc.
    
    Servidor ->> Navegador: Envía la respuesta HTTP
    Note right of Servidor: La respuesta incluye el código de estado y el cuerpo de la respuesta
    
    Navegador ->> Usuario: Muestra la respuesta al usuario
    Note right of Navegador: Puede ser una página de confirmación, un mensaje de éxito, etc.
```
