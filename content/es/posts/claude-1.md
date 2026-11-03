---
title: "Tutorial de Cloudflare: 10 funciones esenciales para principiantes"
slug: claude
date: 2026-11-03
draft: false
---


# Tutorial de Cloudflare: 10 funciones esenciales para principiantes

Cloudflare es una de las plataformas más populares para optimizar el rendimiento de sitios web, administrar DNS y mejorar la seguridad en Internet. Tanto si tienes un blog personal, un sitio web empresarial o un proyecto online, Cloudflare ofrece herramientas que pueden ayudarte a mejorar la velocidad de carga, proteger tu servidor y simplificar la administración de tu sitio web.

Para los principiantes, Cloudflare puede parecer complicado porque ofrece muchas funciones diferentes, como DNS, CDN, SSL/TLS, WAF, Workers y Pages. Sin embargo, no necesitas aprenderlo todo de una sola vez.

En esta guía aprenderás a utilizar Cloudflare paso a paso y conocerás las 10 funciones esenciales que todo principiante debería conocer.

Si también utilizas servicios online internacionales, puedes conocer soluciones de pago como CoinePay, que ofrece servicios de tarjetas virtuales para pagos online. Para los usuarios que realizan transacciones frecuentes en la red TRON, TRXAPI ofrece un servicio de alquiler de energía TRON. Ambos son servicios independientes de terceros y no están afiliados oficialmente a Cloudflare.

## 1. ¿Qué es Cloudflare?

Cloudflare es una plataforma de infraestructura y seguridad de Internet que ofrece servicios como:

- Administración de DNS.
- Red de distribución de contenido (CDN).
- Cifrado SSL/TLS.
- Protección contra ataques DDoS.
- Firewall de aplicaciones web (WAF).
- Almacenamiento en caché de sitios web.
- Análisis del tráfico.
- Desarrollo de aplicaciones sin servidor.
- Alojamiento de sitios web estáticos.

En términos sencillos, Cloudflare puede funcionar como intermediario entre los visitantes de tu sitio web y tu servidor de origen.

Cuando conectas un sitio web a Cloudflare, el tráfico web compatible puede pasar primero por la red global de Cloudflare antes de llegar a tu servidor.

Según la configuración, esto puede ayudarte a:

- Mejorar la velocidad de carga del sitio web.
- Reducir las solicitudes repetidas al servidor de origen.
- Proteger el sitio frente a determinados tipos de tráfico malicioso.
- Activar conexiones HTTPS.
- Administrar los registros DNS del dominio.
- Supervisar el tráfico y los eventos de seguridad.

Cloudflare ofrece planes gratuitos y de pago. Los principiantes pueden comenzar con el plan gratuito y actualizarlo cuando necesiten funciones adicionales.

Sitio web oficial:

[https://www.cloudflare.com/](https://www.cloudflare.com/)

Documentación oficial:

[https://developers.cloudflare.com/](https://developers.cloudflare.com/)

## 2. Cómo registrarse en Cloudflare y añadir un dominio

Antes de utilizar la mayoría de las funciones de Cloudflare, necesitas crear una cuenta y conectar tu dominio.

### Paso 1: Crear una cuenta de Cloudflare

Visita la página oficial de registro:

[https://dash.cloudflare.com/sign-up](https://dash.cloudflare.com/sign-up)

Introduce tu dirección de correo electrónico y una contraseña. Después, sigue las instrucciones para completar el registro.

Una vez creada la cuenta, inicia sesión en el panel de control de Cloudflare.

### Paso 2: Añadir tu dominio

Busca la opción para añadir un sitio web o dominio.

Introduce el nombre del dominio que ya tienes registrado. Por ejemplo:

`example.com`

Normalmente debes introducir el dominio raíz, no la dirección completa de una página web.

Por ejemplo:

- Correcto: `example.com`
- No es necesario: `https://www.example.com/article`

Sigue las instrucciones y selecciona un plan adecuado. Si estás empezando, puedes elegir el plan gratuito.

### Paso 3: Revisar los registros DNS

Cloudflare puede analizar automáticamente los registros DNS existentes e intentar importarlos.

Los tipos de registros DNS más habituales son:

- **A:** Apunta un dominio a una dirección IPv4.
- **AAAA:** Apunta un dominio a una dirección IPv6.
- **CNAME:** Apunta un nombre de dominio a otro.
- **MX:** Define los servidores de correo electrónico.
- **TXT:** Se utiliza para verificar dominios y configurar la autenticación del correo electrónico, como SPF y DKIM.

Comprueba que los registros del sitio web, del correo electrónico y de otros servicios estén correctamente configurados.

### Paso 4: Cambiar los Nameservers del dominio

Después de añadir el dominio, Cloudflare te proporcionará dos servidores de nombres (Nameservers).

Inicia sesión en el panel de tu registrador de dominios y busca la configuración de DNS o Nameservers.

Sustituye los servidores de nombres actuales por las dos direcciones proporcionadas por Cloudflare.

Ten en cuenta lo siguiente:

- Utiliza siempre los Nameservers asignados específicamente a tu dominio.
- No copies los Nameservers de otros sitios web.
- Guarda una copia de la configuración DNS original antes de realizar cambios.
- La propagación DNS puede tardar un tiempo, dependiendo del registrador y de la caché DNS.

Regresa al panel de Cloudflare y espera hasta que el estado del dominio aparezca como Active.

Cuando el dominio esté activo, podrás empezar a configurar las funciones disponibles.

## 3. Las 10 funciones esenciales de Cloudflare que todo principiante debe conocer

A continuación, veremos las funciones más útiles de Cloudflare para los propietarios de sitios web.

## Función 1: Administración de DNS

El DNS es una de las funciones más importantes de Cloudflare.

DNS significa Domain Name System o Sistema de Nombres de Dominio. Su función es traducir los nombres de dominio en direcciones IP o dirigirlos hacia otros servicios de red.

Por ejemplo, cuando alguien visita:

`www.example.com`

El sistema DNS ayuda al navegador a encontrar el destino correspondiente.

### Cómo configurar los registros DNS

Sigue estos pasos:

1. Inicia sesión en Cloudflare.
2. Selecciona tu dominio.
3. Abre la sección DNS.
4. Entra en Records.
5. Haz clic en Add record.
6. Selecciona el tipo de registro.
7. Introduce el nombre y la dirección de destino.
8. Guarda los cambios.

Por ejemplo, si tu sitio web utiliza una dirección IPv4, puedes crear un registro A:

- Type: A
- Name: @
- IPv4 address: La dirección IP de tu servidor.
- TTL: Auto

También puedes crear un registro CNAME para el subdominio www si tu proveedor de alojamiento lo requiere.

### ¿Qué significan las nubes naranja y gris?

Los registros DNS de Cloudflare pueden mostrar dos estados de proxy diferentes.

**Nube naranja: Proxied**

El tráfico HTTP y HTTPS compatible pasa por el proxy de Cloudflare. Esto permite utilizar las funciones CDN y de seguridad correspondientes.

**Nube gris: DNS Only**

Cloudflare proporciona la resolución DNS, pero el tráfico no pasa por el proxy HTTP de Cloudflare.

No todos los registros DNS deben utilizar el proxy. Los registros de correo electrónico y determinados registros de verificación o servicios deben configurarse según su finalidad.

## Función 2: Aceleración del sitio web mediante CDN

CDN significa Content Delivery Network, o red de distribución de contenido.

La CDN de Cloudflare ayuda a distribuir el contenido del sitio web mediante su red global. Cuando determinados recursos están almacenados en caché, los visitantes pueden obtenerlos desde una ubicación de Cloudflare cercana en lugar de solicitar el mismo contenido al servidor de origen cada vez.

### ¿Qué contenido puede almacenar una CDN en caché?

Algunos ejemplos habituales son:

- Imágenes.
- Archivos CSS.
- Archivos JavaScript.
- Fuentes.
- Otros recursos estáticos compatibles.

### Cómo activar la CDN de Cloudflare

En muchas configuraciones habituales, puedes activar el proxy de Cloudflare siguiendo estos pasos:

1. Inicia sesión en Cloudflare.
2. Selecciona tu dominio.
3. Abre la configuración DNS.
4. Busca el registro A o CNAME de tu sitio web.
5. Comprueba que el registro admite el uso del proxy.
6. Cambia el estado a Proxied mediante el icono de la nube naranja.

Una vez configurado, las solicitudes HTTP y HTTPS compatibles podrán pasar por la red de Cloudflare.

Ten en cuenta que activar el proxy no significa que todas las páginas dinámicas se almacenen automáticamente en caché. Las reglas de caché, las cabeceras de respuesta y los tipos de recursos influyen en el comportamiento.

## Función 3: SSL/TLS y cifrado HTTPS

SSL/TLS es una función importante para proteger la comunicación entre los sitios web y sus visitantes.

Cuando HTTPS está configurado correctamente, los datos transmitidos entre el navegador y el sitio web pueden cifrarse, lo que ayuda a reducir el riesgo de interceptación o modificación.

### ¿Para qué sirve Cloudflare SSL/TLS?

Permite:

- Habilitar el acceso HTTPS.
- Cifrar la conexión entre los visitantes y Cloudflare.
- Cifrar la conexión entre Cloudflare y el servidor de origen.
- Mejorar la seguridad de las comunicaciones del sitio web.

### Cómo configurar SSL/TLS

Sigue estos pasos:

1. Inicia sesión en Cloudflare.
2. Selecciona tu dominio.
3. Abre SSL/TLS.
4. Entra en Overview.
5. Comprueba el modo de cifrado actual.
6. Selecciona un modo adecuado según la configuración del certificado de tu servidor de origen.

Los modos SSL/TLS más habituales son:

**Off:** Cloudflare no utiliza cifrado SSL/TLS para la conexión del sitio web.

**Flexible:** La conexión entre el visitante y Cloudflare utiliza HTTPS, pero la conexión entre Cloudflare y el servidor de origen utiliza HTTP.

**Full:** Ambas conexiones utilizan HTTPS, pero Cloudflare no valida estrictamente el certificado del servidor de origen.

**Full (strict):** Ambas conexiones utilizan HTTPS y Cloudflare valida el certificado del servidor de origen.

Si tu servidor de origen tiene un certificado SSL válido, normalmente se recomienda utilizar Full (strict).

No cambies a Full (strict) sin comprobar primero la configuración HTTPS de tu servidor. Una configuración incorrecta puede provocar errores como 525 o 526.

## Función 4: Almacenamiento en caché y Cache Rules

La función de caché de Cloudflare puede reducir las solicitudes repetidas al servidor de origen y mejorar el rendimiento del sitio web.

Por ejemplo, si tu sitio contiene muchas imágenes, archivos CSS y JavaScript, Cloudflare puede almacenar en caché los recursos compatibles y servirlos a los visitantes sin solicitar el mismo contenido al servidor de origen cada vez.

### Cómo borrar la caché de Cloudflare

Si actualizas una imagen o una página web, pero los visitantes siguen viendo la versión anterior, es posible que necesites borrar la caché.

Pasos:

1. Inicia sesión en Cloudflare.
2. Selecciona tu dominio.
3. Abre Caching.
4. Entra en Configuration.
5. Busca Purge Cache.
6. Selecciona si deseas borrar toda la caché o únicamente determinadas URL.

### ¿Qué son las Cache Rules?

Las Cache Rules permiten controlar el comportamiento de la caché según las URL y otras condiciones de las solicitudes.

Por ejemplo, puedes crear reglas de caché para directorios de imágenes.

Sin embargo, debes tener cuidado con las páginas que contienen información personal o que cambia con frecuencia, como:

- Páginas de inicio de sesión.
- Carritos de compra.
- Paneles de usuario.
- Páginas de pago.
- Información de cuentas personales.

Una configuración incorrecta puede mostrar contenido desactualizado o exponer información que debería permanecer privada.

## Función 5: Protección DDoS y seguridad del sitio web

Los ataques DDoS son una amenaza de seguridad habitual para los sitios web.

Los atacantes pueden enviar grandes cantidades de tráfico para consumir los recursos del servidor e impedir que los usuarios legítimos accedan al sitio.

Cloudflare ofrece capacidades de protección a nivel de red y de aplicación que pueden ayudar a mitigar determinados tipos de tráfico malicioso.

### ¿Qué puede hacer la protección DDoS de Cloudflare?

Dependiendo del servicio y de la configuración, puede ayudar a:

- Mitigar determinados ataques de tráfico a gran escala.
- Proteger la disponibilidad del sitio web.
- Reducir el tráfico malicioso que llega al servidor de origen.
- Complementar otras reglas de seguridad.

### Cómo utilizar las funciones de seguridad de Cloudflare

1. Inicia sesión en Cloudflare.
2. Selecciona tu dominio.
3. Abre la sección Security.
4. Revisa las opciones de seguridad disponibles.
5. Configura las opciones de protección adecuadas.
6. Consulta Security Events para revisar las solicitudes que han activado reglas de seguridad.

Las funciones de protección disponibles pueden variar según el plan y el producto.

Recuerda que utilizar Cloudflare no garantiza una protección completa frente a todos los ataques posibles. Tu servidor de origen también necesita una configuración de seguridad adecuada.

## Función 6: WAF (Web Application Firewall)

WAF significa Web Application Firewall, o firewall de aplicaciones web.

Esta herramienta examina las solicitudes HTTP entrantes y aplica reglas de seguridad para identificar y gestionar el tráfico potencialmente malicioso.

Cloudflare WAF puede ayudar a proteger los sitios web frente a determinadas amenazas habituales a nivel de aplicación.

### ¿Contra qué puede ayudar a proteger WAF?

Algunos ejemplos son:

- Determinados intentos de inyección SQL.
- Determinados ataques de Cross-Site Scripting (XSS).
- Solicitudes HTTP sospechosas.
- Tráfico automatizado malicioso.
- Solicitudes inusuales dirigidas a rutas específicas del sitio web.

### Cómo configurar Cloudflare WAF

Sigue estos pasos:

1. Inicia sesión en Cloudflare.
2. Selecciona tu dominio.
3. Abre Security.
4. Busca WAF.
5. Revisa las opciones Managed Rules y Custom Rules disponibles.
6. Configura las reglas según las necesidades de tu sitio web.

Cloudflare permite crear reglas personalizadas utilizando condiciones como direcciones IP, rutas URL y cabeceras de solicitudes.

Por ejemplo, puedes establecer restricciones adicionales para una dirección de administración que no debería ser accesible públicamente.

Ten cuidado al crear reglas demasiado estrictas. Una configuración incorrecta puede bloquear visitantes legítimos. Revisa los eventos de seguridad y ajusta las reglas gradualmente.

## Función 7: Redirect Rules y redirecciones de URL

Redirect Rules es una función muy útil para administrar las direcciones de un sitio web.

Permite enviar automáticamente a los visitantes de una URL a otra.

Por ejemplo:

`http://example.com`

Puede redirigirse a:

`https://example.com`

También puedes redirigir páginas antiguas a nuevas direcciones después de modificar la estructura de tu sitio web.

### Cómo configurar Redirect Rules

1. Inicia sesión en Cloudflare.
2. Selecciona tu dominio.
3. Abre Rules.
4. Busca Redirect Rules.
5. Crea una nueva regla de redirección.
6. Configura las condiciones de coincidencia.
7. Introduce la URL de destino.
8. Selecciona el código de estado adecuado.
9. Guarda la regla.

Los códigos de redirección más habituales son:

- **301:** Redirección permanente.
- **302:** Redirección temporal.

Si una página se ha trasladado definitivamente, puedes utilizar una redirección 301. Para cambios temporales, puedes considerar una redirección 302.

Después de crear la regla, prueba tanto la URL original como la de destino para comprobar que la redirección funciona correctamente.

## Función 8: Analytics y supervisión del tráfico web

Cloudflare Analytics ayuda a los propietarios de sitios web a comprender los patrones de tráfico y el rendimiento de la red.

Para los administradores de blogs, sitios empresariales y páginas de contenido, estas estadísticas pueden ayudar a identificar actividades inusuales y supervisar el rendimiento del sitio.

### ¿Qué puedes supervisar con Analytics?

Según el producto y el plan, las métricas disponibles pueden incluir:

- Número de solicitudes.
- Transferencia de datos.
- Rendimiento de la caché.
- Eventos de seguridad.
- Estadísticas relacionadas con los visitantes.
- Solicitudes al servidor de origen.
- Indicadores de rendimiento de red.

### Cómo consultar las estadísticas del sitio web

1. Inicia sesión en Cloudflare.
2. Selecciona tu dominio.
3. Abre Analytics.
4. Elige la categoría de datos que deseas consultar.
5. Configura el intervalo de tiempo.
6. Examina la información de tráfico y seguridad.

Puedes utilizar estos datos para identificar aumentos repentinos del tráfico, revisar el rendimiento de la caché e investigar solicitudes inusuales.

Ten en cuenta que Cloudflare Analytics y Google Analytics utilizan métodos de medición diferentes. Por eso, las cifras de tráfico de ambas plataformas pueden no coincidir.

## Función 9: Cloudflare Workers

Cloudflare Workers es una plataforma para desarrolladores que permite ejecutar código en la red de Cloudflare.

En términos sencillos, ayuda a los desarrolladores a implementar determinadas aplicaciones y funciones de backend sin tener que administrar un servidor tradicional.

### ¿Qué puedes crear con Workers?

Algunos usos habituales incluyen:

- Crear endpoints de API.
- Procesar solicitudes HTTP.
- Ejecutar funciones de procesamiento de datos.
- Desarrollar funciones dinámicas para sitios web.
- Conectarse a bases de datos y servicios externos.
- Implementar aplicaciones web ligeras.

### Cómo crear un Cloudflare Worker

1. Inicia sesión en Cloudflare.
2. Abre Workers & Pages.
3. Selecciona la opción para crear una aplicación o Worker.
4. Sigue las instrucciones de configuración.
5. Escribe o importa tu código.
6. Implementa el proyecto.
7. Prueba la aplicación utilizando la URL asignada.

Workers es especialmente útil para desarrolladores que tienen algunos conocimientos de programación.

Si solo quieres configurar DNS y CDN para un sitio web normal, no necesitas aprender Workers inmediatamente.

Los límites de uso, los recursos disponibles y las funciones avanzadas pueden variar según el plan. Consulta la documentación oficial antes de implementar aplicaciones en producción.

## Función 10: Cloudflare Pages para alojar sitios web estáticos

Cloudflare Pages es una plataforma para implementar sitios web estáticos y proyectos frontend.

Si administras el código de tu sitio web en GitHub, puedes conectar tu repositorio a Cloudflare Pages y automatizar las implementaciones.

### ¿Qué tipos de sitios web pueden utilizar Pages?

Algunos ejemplos son:

- Blogs personales.
- Sitios web empresariales.
- Páginas de presentación de productos.
- Sitios web de documentación.
- Proyectos de páginas estáticas.
- Aplicaciones frontend.

### Cómo implementar un sitio web con Cloudflare Pages

1. Inicia sesión en Cloudflare.
2. Abre Workers & Pages.
3. Selecciona la opción para crear una aplicación.
4. Elige el flujo de implementación de Pages.
5. Conecta tu repositorio de GitHub.
6. Selecciona el repositorio que deseas implementar.
7. Configura el comando de compilación y el directorio de salida.
8. Inicia la implementación.

Después de completar la implementación correctamente, Cloudflare proporcionará una URL desde la que los visitantes podrán acceder a tu sitio web.

Si tienes un dominio propio, también puedes seguir las instrucciones para conectarlo a tu proyecto de Pages.

El comando de compilación y el directorio de salida necesarios dependen del framework frontend y de la estructura de tu proyecto.

## 4. Configuración recomendada de Cloudflare para principiantes

Si acabas de crear una cuenta de Cloudflare, no necesitas activar todas las funciones inmediatamente.

Para un blog personal, un sitio web empresarial o una página de contenidos, el siguiente orden de configuración es un buen punto de partida.

### Paso 1: Conectar tu dominio

Añade tu dominio a Cloudflare, revisa los registros DNS y actualiza los Nameservers desde tu registrador de dominios.

### Paso 2: Comprobar la resolución DNS

Asegúrate de que el dominio principal y el subdominio www se resuelven correctamente.

Si el sitio web no se carga, comprueba primero los registros DNS y el servidor de origen.

### Paso 3: Configurar HTTPS

Selecciona un modo SSL/TLS que coincida con la configuración del certificado de tu servidor de origen.

Si tu servidor tiene un certificado válido, normalmente se recomienda Full (strict).

### Paso 4: Activar el proxy CDN

Configura los registros DNS adecuados del sitio web como Proxied utilizando el icono de la nube naranja.

Después de comprobar que el sitio funciona correctamente, supervisa el rendimiento y la caché.

### Paso 5: Configurar las reglas de caché

Establece políticas de caché según los tipos de recursos del sitio web.

Los recursos estáticos, como imágenes, CSS y JavaScript, suelen poder almacenarse en caché. Ten cuidado con las páginas de inicio de sesión, de pago y de información personal.

### Paso 6: Revisar la configuración de seguridad

Consulta Security Events y las reglas de protección disponibles.

Si identificas tráfico sospechoso, considera configurar WAF u otros controles de seguridad.

### Paso 7: Supervisar Analytics

Utiliza Analytics para revisar el tráfico, la caché y la seguridad del sitio web. Investiga las actividades inusuales cuando sea necesario.

## 5. Problemas habituales de Cloudflare y cómo solucionarlos

Incluso después de configurar Cloudflare correctamente, puedes encontrar algunos errores. Estos son algunos problemas frecuentes y sus posibles soluciones.

### 1. Mi sitio web no funciona después de conectarlo a Cloudflare

Entre las posibles causas se encuentran:

- Registros DNS incorrectos.
- Los cambios de Nameservers todavía no han surtido efecto.
- El servidor de origen no está disponible.
- La configuración SSL/TLS es incorrecta.
- El firewall del servidor está bloqueando las conexiones de Cloudflare.

Empieza comprobando la resolución DNS y la disponibilidad del servidor de origen. Después, revisa la configuración SSL/TLS.

### 2. Cómo solucionar el error 522 de Cloudflare

El error 522 suele indicar que Cloudflare ha agotado el tiempo de espera al intentar establecer una conexión con el servidor de origen.

Comprueba lo siguiente:

- ¿El servidor de origen está funcionando?
- ¿El firewall permite el tráfico de Cloudflare?
- ¿El servidor está sobrecargado?
- ¿El registro DNS apunta a la dirección IP correcta?
- ¿Existen problemas de conectividad de red?

### 3. Cómo solucionar el error 525 de Cloudflare

El error 525 suele indicar que ha fallado el protocolo de enlace SSL entre Cloudflare y el servidor de origen.

Puedes comprobar:

- Si HTTPS funciona correctamente en el servidor de origen.
- Si el servidor tiene instalado correctamente un certificado SSL.
- Si el servidor admite la configuración TLS necesaria.
- Si el modo SSL/TLS coincide con la configuración del servidor de origen.

### 4. Las imágenes no se actualizan después de activar Cloudflare

Esto puede ocurrir porque Cloudflare o tu navegador siguen utilizando una versión antigua almacenada en caché.

Prueba lo siguiente:

1. Inicia sesión en Cloudflare.
2. Selecciona tu dominio.
3. Abre Caching.
4. Utiliza Purge Cache para borrar la caché correspondiente.
5. Actualiza el navegador.

Si el problema continúa, comprueba si los archivos se han actualizado correctamente en el servidor de origen.

### 5. ¿El plan gratuito de Cloudflare es suficiente para principiantes?

Para blogs personales, pequeños sitios empresariales y páginas de contenido normales, el plan gratuito suele ser un buen punto de partida.

Si tu sitio web necesita funciones WAF más avanzadas, controles de seguridad adicionales, herramientas de rendimiento o servicios de nivel empresarial, puedes considerar un plan de pago.

Consulta siempre los precios y la documentación actual de Cloudflare, ya que las funciones y los límites pueden cambiar.

## 6. Recursos oficiales y documentación de Cloudflare

Si quieres aprender más sobre Cloudflare, los siguientes recursos oficiales pueden resultarte útiles.

**Sitio web oficial de Cloudflare**

[https://www.cloudflare.com/](https://www.cloudflare.com/)

**Panel de control de Cloudflare**

[https://dash.cloudflare.com/](https://dash.cloudflare.com/)

**Documentación de Cloudflare**

[https://developers.cloudflare.com/](https://developers.cloudflare.com/)

**Documentación de Cloudflare DNS**

[https://developers.cloudflare.com/dns/](https://developers.cloudflare.com/dns/)

**Documentación de Cloudflare SSL/TLS**

[https://developers.cloudflare.com/ssl/](https://developers.cloudflare.com/ssl/)

**Documentación de Cloudflare WAF**

[https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)

**Documentación de Cloudflare Workers**

[https://developers.cloudflare.com/workers/](https://developers.cloudflare.com/workers/)

**Documentación de Cloudflare Pages**

[https://developers.cloudflare.com/pages/](https://developers.cloudflare.com/pages/)

## 7. Conclusión: ¿Qué funciones de Cloudflare deberían aprender primero los principiantes?

Cloudflare ofrece numerosas herramientas, pero los principiantes deberían centrarse primero en conectar el sitio web y configurar las funciones básicas antes de explorar las opciones avanzadas.

Las 10 funciones esenciales explicadas en esta guía son:

1. **DNS:** Administrar la resolución de nombres de dominio.
2. **CDN:** Mejorar el acceso a los recursos estáticos del sitio web.
3. **SSL/TLS:** Configurar el cifrado HTTPS.
4. **Cache Rules:** Administrar la caché del sitio web.
5. **DDoS Protection:** Ayudar a mitigar ataques de tráfico malicioso.
6. **WAF:** Filtrar solicitudes sospechosas al sitio web.
7. **Redirect Rules:** Configurar redirecciones de URL.
8. **Analytics:** Supervisar el tráfico y los datos de seguridad.
9. **Workers:** Implementar aplicaciones de red y código de backend.
10. **Pages:** Publicar sitios web estáticos y proyectos frontend.

Para la mayoría de los propietarios de sitios web, DNS, CDN, SSL/TLS, caché y protección básica de seguridad son las mejores funciones que conviene aprender primero.

Si estás creando un blog personal, un sitio empresarial o una plataforma de contenidos, empieza con el plan gratuito de Cloudflare y configura las funciones esenciales. A medida que crezca tu sitio web, podrás explorar herramientas más avanzadas.

Recuerda revisar periódicamente los registros DNS, la configuración SSL/TLS y las reglas de caché. Una configuración incorrecta puede provocar problemas de acceso o comportamientos inesperados.

Cloudflare es mucho más que un proveedor de CDN. Es una plataforma que combina administración DNS, seguridad web, optimización del rendimiento y herramientas para desarrolladores. Aprender estas funciones esenciales puede ayudarte a administrar tu sitio web de forma más eficaz.

Si también buscas servicios de tarjetas virtuales para realizar pagos online, puedes conocer más sobre CoinePay:

[https://www.coinepay.net/login?referrer=7PFFZMCH](https://www.coinepay.net/login?referrer=7PFFZMCH)

Para los usuarios que realizan transferencias frecuentes de USDT TRC20 en la red TRON, TRXAPI también ofrece un servicio de alquiler de energía TRON:

[https://www.trxapi.io/energy.html?lang=zh-TW](https://www.trxapi.io/energy.html?lang=zh-TW)

Código de invitación de TRXAPI: 57YQDGFU

Estos servicios de terceros son independientes de Cloudflare y no están afiliados oficialmente con esta plataforma. Consulta sus respectivas condiciones antes de utilizarlos.

## Referencias

- Sitio web oficial de Cloudflare: [https://www.cloudflare.com/](https://www.cloudflare.com/)
- Documentación de Cloudflare: [https://developers.cloudflare.com/](https://developers.cloudflare.com/)
- Productos de Cloudflare: [https://www.cloudflare.com/products/](https://www.cloudflare.com/products/)
- Documentación de Cloudflare WAF: [https://developers.cloudflare.com/waf/](https://developers.cloudflare.com/waf/)
- Documentación de Cloudflare Analytics: [https://developers.cloudflare.com/analytics/](https://developers.cloudflare.com/analytics/)

