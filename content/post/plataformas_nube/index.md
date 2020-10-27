---
title: "Plataformas en la nube que deberías usar en 2020"
date: 2020-04-18
tags: ["plataformas", "programar","código", "nube"]
categories: ["plataformas", "programación"]
description: "Plataformas en la nube que deberías usar"
draft: false
---
 
# 
Una plataforma en la nube es generalmente una solución llave en mano que puede facilitarle la vida y quitarle algo de complejidad a sus hombros.

Probablemente no pueda crear una aplicación completa y escalable sin utilizar al menos una plataforma en la nube.

Aquí está la lista:

1. Servicios web de Amazon
Incluso si no lo está utilizando en su trabajo actual, al menos debería familiarizarse con los componentes EC2 y S3.

No necesita inscribirse en un curso costoso para aprender lo esencial.

Flujos básicos para EC2:

Lanzar una instancia
Iniciar / reiniciar / detener una instancia
Crea una copia de seguridad
Restaurar desde una copia de seguridad
Configurar grupos de seguridad
Flujos básicos para S3:

Crea un cubo
Crear una carpeta
Subir archivos
Establecer permisos
Descargar archivos
Si bien es posible que desee usar la interfaz de usuario para manejar tareas no repetitivas en EC2, lo más probable es que use la CLI de AWS para manejar todas las operaciones en S3.

Recuerde, AWS tiene muchos componentes, casi cualquier cosa que se le ocurra en términos de computación en la nube y API.

2. Twilio
Twilio es una empresa de comunicación en la nube que permite a los usuarios utilizar lenguajes web estándar para crear aplicaciones de voz, VoIP y SMS a través de una API web.

Una funcionalidad para enviar mensajes de texto no es algo que desee crear desde cero.

Aquí hay un ejemplo de Python para enviar un SMS con Twilio:

```python
from twilio.rest import Client

account_sid = 'ACXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX'
auth_token = 'your_auth_token'
client = Client(account_sid, auth_token)

message = client.messages.create(
                              body='Hi there!',
                              from_='+15017122661',
                              to='+15558675310'
                          )

print(message.sid)
```
Puedes leer un breve tutorial [aquí](https://www.twilio.com/docs/sms/tutorials/how-to-send-sms-messages) .

3. SendGrid
SendGrid es una plataforma de entrega de correo electrónico basada en la nube, tanto para correos electrónicos transaccionales como de marketing.

Claro, puede enviar correos electrónicos sin SendGrid o cualquier otro proveedor externo, todo lo que necesita es un servidor.

Es tan simple como:

```php
<?php
$to = "somebody@example.com";
$subject = "My subject";
$txt = "Hello world!";
$headers = "From: webmaster@example.com" . "\r\n" .
"CC: somebodyelse@example.com";

mail($to,$subject,$txt,$headers);
?>
```
Pero es una mala idea usar su propio servidor de correo electrónico en lugar de SendGrid.

Este es el por qué:

Es posible que su servidor no pueda manejar el volumen de correos electrónicos que está enviando.
Los correos electrónicos enviados desde su servidor pueden aterrizar en la carpeta Spam debido a su baja reputación de [IP](https://sendgrid.com/blog/email-reputation-101-ip-reputation-vs-domain-reputation/) .
Tendrá que crear sus propias herramientas para monitorear la actividad del [correo electrónico](https://sendgrid.com/docs/ui/analytics-and-reporting/email-activity-feed/).
SendGrid no es solo para vendedores, sino que también proporciona una potente API web.

Aquí hay un ejemplo básico de Python para enviar un correo electrónico:

```python
import os
from sendgrid import SendGridAPIClient
from sendgrid.helpers.mail import Mail

message = Mail(
    from_email='from_email@example.com',
    to_emails='to@example.com',
    subject='Sending with SendGrid is Fun',
    html_content='<strong>and easy to do anywhere, even with Python</strong>')
try:
    sg = SendGridAPIClient(os.environ.get('SENDGRID_API_KEY'))
    response = sg.send(message)
    print(response.status_code)
    print(response.body)
    print(response.headers)
except Exception as e:
    print(e.message)
```

Como puede ver, también verificamos el código de estado en este ejemplo anterior.

4. Endtest
Endtest es una plataforma en la nube donde puede crear y ejecutar pruebas automatizadas para sus aplicaciones web y aplicaciones móviles

Ofrecer a sus usuarios una experiencia perfecta es de suma importancia.

Una buena manera de lograrlo es confiar en pruebas automatizadas y ser el primero en descubrir cuándo algo deja de funcionar.

Las pruebas unitarias y las solicitudes de API simplemente no son suficientes para verificar si su producto funciona como se espera para sus usuarios.

Endtest ofrece una manera fácil de crear pruebas automatizadas funcionales y ejecutarlas en su laboratorio de dispositivos móviles y en la nube entre navegadores.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--z9wn5vPz--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/sn1fk6jsd5kis5y40rpw.gif)

Y puede hacerlo sin tener que escribir una sola línea de código.

Hay una grabadora para Web [Tests](https://endtest.io/guides/docs/how-to-create-web-tests/) y una grabadora para Mobile [Tests](https://endtest.io/guides/docs/how-to-create-mobile-tests/) , ambas se basan en la identificación de elementos, no en el reconocimiento de imágenes o el OCR

![](https://res.cloudinary.com/practicaldev/image/fetch/s--ERWmrKgi--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/6wt3v13sfs0iv4nbvaf6.gif)

También ofrece una [API](https://endtest.io/guides/docs/how-to-use-the-endtest-api/) e integraciones con soluciones como Jenkins, Jira, Slack y otras.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--UV4wjQPF--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/p56rl7t8yjutjq5esqq2.gif)

¿Por qué deberías usar esta plataforma en la nube?

[Aquí](https://endtest.io/why-endtest) hay una buena respuesta.

5. Análisis de amplitud
Esta no es su solución de análisis habitual donde importa algo de JavaScript en sus páginas y comienza a rastrear a los visitantes.

Amplitude puede ayudarlo a rastrear eventos de usuarios y generar información increíblemente útil.

Por ejemplo, puede ver cuántos de los usuarios que se registraron hace 6 semanas siguen usando su producto, una métrica que se conoce como [retención](https://help.amplitude.com/hc/en-us/articles/230543327-Retention-Analysis).


![](https://res.cloudinary.com/practicaldev/image/fetch/s--uRvUlJ4p--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/aaoffpkqi6anl9w32it5.png)

El truco es utilizar las capacidades de seguimiento de eventos e integrarlas en su código.

Para cada acción realizada por un usuario, puede enviar una solicitud a la API de [Amplitude](https://help.amplitude.com/hc/en-us/articles/115000959052-For-Developers-Getting-Started) para almacenar un identificador para el usuario, el tipo de evento y cualquier otra cosa que necesite.

Aquí le mostramos cómo enviar un evento a Amplitude desde su código de Python:

```python
import amplitude    

# initialize amplitude logger
amplitude_logger = amplitude.AmplitudeLogger(api_key = "SOME_API_KEY_STRING")

# example event
event_args = {"device_id":"somedeviceid", "event_type":"justtesting", 
              "event_properties":{"property1":"somevalue", "propertyN":"anothervalue"}
event = amplitude_logger.create_event(**event_args)

# send event to amplitude
amplitude_logger.log_event(event)
```

Esto le permite generar cronogramas de eventos para todos sus usuarios y segmentos.

6. raya
Stripe es un conjunto de API de pago que impulsa el comercio para negocios en línea de todos los tamaños.

Manejar los pagos es otra cosa que no desea construir desde cero.

Stripe es conocido por ser amigable para el desarrollador y proporciona una [documentación](https://stripe.com/docs/api) detallada para sus API.

Y tener una página de pago impresionante realmente puede aumentar esas conversiones.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--sVyJKfCn--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/14b80ohq1p4h29lj2t1d.jpg)

El manejo de pagos no se trata solo de procesar un pago con tarjeta de crédito, hay otros aspectos importantes cubiertos por Stripe, como el fraude y el cumplimiento.

Aquí hay un ejemplo usando JavaScript:
```javascript
var stripe = Stripe('_____YOUR_STRIPE_PUBLISHABLE_KEY___');
var elements = stripe.elements();

// Create an instance of the card Element
var card = elements.create('card', {style: style});
// Add an instance of the card Element into the `card-element` <div>
card.mount('#card-element');

// Handle real-time validation errors from the card Element.
card.addEventListener('change', function(event) {
    var displayError = document.getElementById('card-errors');
if (event.error) {
        displayError.textContent = event.error.message;
    } else {
        displayError.textContent = '';
    }
});

// Handle form submission
var form = document.getElementById('payment-form');
form.addEventListener('submit', function(event) {
    event.preventDefault();
stripe.createToken(card).then(function(result) {
        if (result.error) {
            // Inform the user if there was an error
            var errorElement = document.getElementById('card-errors');
            errorElement.textContent = result.error.message;
        } else {
            stripeTokenHandler(result.token);
        }
    });
});
 
// Send Stripe Token to Server
function stripeTokenHandler(token) {
    // Insert the token ID into the form so it gets submitted to the server
    var form = document.getElementById('payment-form');
// Add Stripe Token to hidden input
    var hiddenInput = document.createElement('input');
    hiddenInput.setAttribute('type', 'hidden');
    hiddenInput.setAttribute('name', 'stripeToken');
    hiddenInput.setAttribute('value', token.id);
    form.appendChild(hiddenInput);
// Submit form
    form.submit();
}
```

¿Te gusto?  házmelo saber por redes sociales
Gracias Excelente día
