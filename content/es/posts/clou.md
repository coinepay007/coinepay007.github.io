---
title: Cómo configurar Cloudflare CDN (Guía 2027)
slug: clou
date: 2026-11-24
draft: false
---
Cómo configurar Cloudflare CDN (Guía 2027)

Cloudflare CDN es una solución popular para mejorar el rendimiento de los sitios web, reducir los tiempos de carga y añadir una capa adicional de seguridad. Al distribuir el tráfico a través de la red global de Cloudflare, los propietarios de sitios web pueden almacenar contenido estático en caché, proteger sus servidores y optimizar el acceso de los visitantes desde diferentes regiones.

Tanto si tienes un blog de WordPress, un sitio web empresarial, una tienda online o una página alojada en un VPS, configurar Cloudflare CDN puede ser un paso útil para mejorar el rendimiento de tu sitio.

En esta guía aprenderás cómo configurar Cloudflare CDN en 2027, conectar tu dominio, configurar los registros DNS, activar el proxy, ajustar las opciones de caché y solucionar los problemas más habituales.

Si también utilizas herramientas de pago online para servicios internacionales, puedes conocer CoinePay como una alternativa para realizar pagos online.

👉 **CoinePay 官方入口：**  
[https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

Si también utilizas la red TRON para transferir USDT, puedes conocer el servicio de alquiler de energía TRON de TRXAPI, que puede ayudar a reducir el consumo de recursos TRX en determinadas transacciones compatibles.

👉 **TRXAPI 官方入口：**  
[https://login.trxapi.io/energy](https://login.trxapi.io/energy)

## **¿Qué es Cloudflare CDN?**

Cloudflare CDN es una red de distribución de contenido que ayuda a entregar los contenidos de un sitio web a través de una red global de servidores. En lugar de que cada visitante se conecte directamente al servidor de origen, Cloudflare puede servir contenido almacenado en caché desde una ubicación más cercana al visitante.

Cloudflare también ofrece servicios adicionales, como gestión de DNS, protección contra ataques DDoS, filtrado de tráfico, compatibilidad con SSL/TLS y opciones de almacenamiento en caché.

Las principales ventajas de Cloudflare CDN incluyen:

- Mayor velocidad de carga del sitio web para visitantes de diferentes regiones.
- Reducción del consumo de ancho de banda del servidor de origen.
- Protección adicional contra determinados tipos de tráfico malicioso y ataques DDoS.
- Compatibilidad con cifrado SSL/TLS.
- Gestión flexible de DNS.
- Funciones de caché y optimización del sitio web.

Cloudflare ofrece planes gratuitos y de pago. Muchas de las funciones básicas de CDN se pueden configurar utilizando el plan Free.

## **Qué necesitas antes de configurar Cloudflare CDN**

Antes de conectar tu sitio web a Cloudflare, asegúrate de disponer de lo siguiente:

- Un nombre de dominio registrado.
- Un sitio web o servidor de alojamiento que ya esté funcionando.
- Acceso al panel de administración de tu registrador de dominios.
- Acceso a los registros DNS de tu dominio.
- La dirección IP de tu servidor de alojamiento, si es necesaria.

Si tu dominio ya está conectado a un sitio web, revisa la configuración DNS existente antes de realizar cambios. Los registros DNS incorrectos pueden provocar que el sitio web, el correo electrónico u otros servicios dejen de funcionar.

## **Paso 1: Crear una cuenta de Cloudflare**

Primero, visita el sitio web oficial de Cloudflare:

[https://www.cloudflare.com/](https://www.cloudflare.com/)

Registra una cuenta utilizando tu dirección de correo electrónico y una contraseña.

Después de registrarte, inicia sesión en el panel de Cloudflare. Desde allí podrás añadir tu dominio y configurar DNS, seguridad, caché y otros ajustes del sitio web.

## **Paso 2: Añadir tu dominio a Cloudflare**

Después de iniciar sesión:

1. Abre el panel de Cloudflare.
2. Selecciona la opción para añadir o incorporar un dominio.
3. Introduce tu nombre de dominio, por ejemplo, [example.com](http://example.com).
4. Continúa con el siguiente paso.
5. Selecciona un plan.

Para la mayoría de los sitios personales, blogs y páginas pequeñas, el plan Free es un buen punto de partida.

Cloudflare intentará escanear los registros DNS existentes e importarlos a su interfaz de gestión DNS.

## **Paso 3: Revisar los registros DNS**

Antes de activar Cloudflare, revisa cuidadosamente tus registros DNS.

Los registros DNS más comunes incluyen:

- Registro A: apunta un dominio o subdominio a una dirección IPv4.
- Registro AAAA: apunta un dominio o subdominio a una dirección IPv6.
- Registro CNAME: apunta un dominio o subdominio a otro nombre de host.
- Registro MX: define los servidores de correo electrónico del dominio.
- Registro TXT: se utiliza para verificaciones, SPF, DKIM, DMARC y otras configuraciones.

Asegúrate de que los registros principales de tu sitio web sean correctos.

Por ejemplo:

Registro A

Nombre: @

Contenido: dirección IP de tu servidor

Registro CNAME

Nombre: www

Contenido: tu dominio principal o el nombre de host proporcionado por tu proveedor de alojamiento.

Los registros exactos dependerán de la configuración de tu alojamiento web.

Si utilizas correo electrónico asociado a tu dominio, asegúrate de que los registros MX, TXT y otros registros relacionados con el correo electrónico permanezcan correctamente configurados. El proxy de Cloudflare no gestiona el tráfico de correo electrónico convencional y, por lo general, los registros de correo deben permanecer en modo DNS Only.

## **Paso 4: Activar el proxy de Cloudflare**

Uno de los pasos más importantes para configurar Cloudflare CDN es activar su servicio de proxy.

En la sección de gestión DNS encontrarás una opción de estado del proxy para los registros compatibles.

Proxied — Nube naranja

Cuando la nube naranja está activada, el tráfico de los registros compatibles pasa a través de Cloudflare. Esto permite utilizar las funciones correspondientes de CDN, seguridad y proxy.

DNS Only — Nube gris

Cuando la nube gris está activada, Cloudflare proporciona resolución DNS, pero no enruta el tráfico a través de su red de proxy.

Para los registros principales de tu sitio web, como el registro A del dominio y el registro A o CNAME de www, activa Proxied si tu configuración web lo permite.

No actives el proxy automáticamente para todos los registros DNS. Algunos servicios, como el correo electrónico y ciertos registros de verificación o servicios de terceros, necesitan permanecer en DNS Only.

## **Paso 5: Cambiar los nameservers de tu dominio**

Después de revisar los registros DNS, Cloudflare te proporcionará dos nameservers.

Debes sustituir los nameservers actuales de tu dominio por los que te asigna Cloudflare.

El proceso suele ser el siguiente:

1. Inicia sesión en tu registrador de dominios.
2. Abre la página de administración de tu dominio.
3. Busca la configuración de nameservers.
4. Sustituye los nameservers actuales por los dos nameservers de Cloudflare.
5. Guarda los cambios.

Los cambios de nameservers pueden tardar un tiempo en propagarse.

Durante este proceso, la resolución DNS puede variar dependiendo de la red y de la caché DNS. Evita realizar cambios innecesarios mientras se completa la activación.

Si tienes DNSSEC activado, revisa la configuración antes de cambiar los nameservers. Una configuración DNSSEC incorrecta puede impedir que tu dominio se resuelva correctamente.

## **Paso 6: Configurar SSL/TLS**

SSL/TLS es importante para proteger las conexiones del sitio web y evitar advertencias de seguridad en el navegador.

En el panel de Cloudflare:

1. Selecciona tu dominio.
2. Abre la sección SSL/TLS.
3. Revisa el modo de cifrado.
4. Selecciona el modo que corresponda a la configuración SSL de tu servidor de origen.

Cloudflare ofrece habitualmente los siguientes modos SSL/TLS:

Flexible

Flexible cifra la conexión entre los visitantes y Cloudflare, pero la conexión entre Cloudflare y tu servidor de origen no está cifrada.

Este modo puede utilizarse cuando el servidor de origen no dispone de un certificado SSL, aunque generalmente no es la configuración recomendada a largo plazo.

Full

Full cifra la conexión entre Cloudflare y el servidor de origen. Tu servidor debe admitir HTTPS, aunque el certificado no necesariamente tiene que ser de una autoridad pública de confianza.

Full (Strict)

Full (Strict) cifra la conexión y valida el certificado del servidor de origen. Tu servidor debe disponer de un certificado válido que cumpla los requisitos de Cloudflare.

Se recomienda utilizar Full (Strict) en la mayoría de los sitios web que ya tienen HTTPS correctamente configurado.

Antes de activar Full (Strict), asegúrate de que tu servidor de origen tenga un certificado SSL válido.

## **Paso 7: Configurar la caché de Cloudflare**

La caché de Cloudflare permite almacenar determinados recursos del sitio web en su red, de modo que puedan entregarse sin tener que obtenerlos repetidamente desde el servidor de origen.

Para configurar la caché:

1. Abre tu dominio en el panel de Cloudflare.
2. Accede a la sección de configuración de caché.
3. Revisa las opciones disponibles.
4. Ajusta el comportamiento de la caché según las necesidades de tu sitio web.

Los recursos estáticos que normalmente se pueden almacenar en caché incluyen:

- Imágenes.
- Archivos CSS.
- Archivos JavaScript.
- Fuentes.
- Páginas HTML estáticas, cuando corresponda.

El contenido dinámico, las páginas de inicio de sesión, los carritos de compra, los paneles de administración y el contenido personalizado requieren una configuración más cuidadosa.

En sitios web de WordPress, evita almacenar indiscriminadamente en caché páginas que contengan información de inicio de sesión, datos personalizados de usuarios, información del carrito de compra o funciones administrativas.

Puedes utilizar Cache Rules de Cloudflare para definir qué URLs deben almacenarse en caché y cómo debe aplicarse el comportamiento de caché.

## **Paso 8: Configurar Cache Rules**

Cache Rules permite controlar el comportamiento de la caché para URLs específicas o determinadas condiciones.

Por ejemplo, puedes:

- Almacenar archivos estáticos en caché durante períodos más largos.
- Excluir páginas administrativas de la caché.
- Evitar almacenar páginas de inicio de sesión.
- Aplicar diferentes configuraciones de caché a determinados subdominios.
- Controlar el comportamiento de la caché para determinados tipos de contenido.

Si utilizas WordPress, considera excluir las siguientes rutas de la caché cuando corresponda:

- /wp-admin/
- /wp-login.php

Dependiendo de la configuración de tu sitio, también puede ser necesario excluir páginas dinámicas, páginas de pago o contenido personalizado.

Prueba siempre tu sitio web después de modificar Cache Rules.

## **Paso 9: Vaciar la caché de Cloudflare**

Cuando actualizas tu sitio web, pero los visitantes siguen viendo contenido antiguo, el problema puede estar relacionado con la caché.

Puedes limpiar la caché desde Cloudflare.

1. Abre el panel de Cloudflare.
2. Selecciona tu dominio.
3. Accede a la sección de caché.
4. Busca la opción para purgar la caché.
5. Selecciona el método de limpieza adecuado.

Cloudflare permite diferentes opciones para eliminar contenido almacenado en caché. Según tus necesidades, puedes purgar URLs específicas o limpiar una parte más amplia de la caché.

Para actualizaciones habituales del sitio web, suele ser preferible purgar únicamente las URLs afectadas en lugar de eliminar toda la caché.

## **Paso 10: Probar Cloudflare CDN**

Después de configurar Cloudflare, comprueba que tu sitio web funciona correctamente.

Revisa los siguientes aspectos:

- Tu sitio web se abre normalmente.
- HTTPS funciona sin advertencias del navegador.
- Los registros DNS se resuelven correctamente.
- Las versiones www y sin www funcionan como esperas.
- Los servicios de correo electrónico siguen funcionando.
- Los recursos estáticos se almacenan en caché cuando corresponde.

También puedes comprobar las cabeceras HTTP de respuesta.

Por ejemplo, puede aparecer la siguiente cabecera:

cf-cache-status

Los valores más comunes incluyen:

- HIT: el recurso solicitado se ha servido desde la caché.
- MISS: el recurso no estaba en caché y se ha obtenido desde el servidor de origen.
- BYPASS: se ha omitido la caché.
- DYNAMIC: el recurso no se considera apto para el almacenamiento en caché convencional.
- EXPIRED: el recurso almacenado en caché ha caducado.

No todas las solicitudes deben devolver HIT. Las páginas dinámicas y los recursos que no están almacenados en caché pueden devolver legítimamente otros estados.

También puedes utilizar herramientas de pruebas de rendimiento como PageSpeed Insights, GTmetrix o WebPageTest para evaluar la velocidad de carga y el rendimiento de tu sitio web.

## **Problemas comunes de Cloudflare CDN**

### **Error 521 de Cloudflare**

El error 521 generalmente indica que Cloudflare no puede establecer una conexión con el servidor de origen porque este está rechazando la conexión.

Posibles soluciones:

- Comprueba si el servidor está funcionando.
- Verifica que el firewall del servidor permita el tráfico de Cloudflare.
- Comprueba el servicio web del servidor de origen.
- Revisa las reglas del firewall y del software de seguridad.

### **Error 522 de Cloudflare**

El error 522 indica que se ha producido un tiempo de espera en la conexión entre Cloudflare y el servidor de origen.

Las posibles causas incluyen:

- El servidor de origen está sobrecargado.
- Las reglas del firewall están bloqueando Cloudflare.
- Problemas de conectividad de red.
- Retrasos en la respuesta del servidor.

Comprueba el servidor de alojamiento y la configuración de red.

### **Errores de certificados SSL**

Los errores SSL pueden producirse cuando la configuración SSL/TLS de Cloudflare no coincide con la configuración del certificado del servidor de origen.

Comprueba lo siguiente:

- El certificado SSL del servidor de origen es válido.
- El modo SSL/TLS seleccionado es adecuado.
- HTTPS está configurado correctamente en el servidor de origen.
- No existen reglas de redirección incompatibles.

### **El contenido del sitio web no se actualiza**

Si tu sitio web muestra contenido antiguo:

- Purga la caché correspondiente de Cloudflare.
- Limpia la caché del navegador.
- Revisa Cache Rules.
- Comprueba si el plugin de caché de tu sitio web está causando el problema.

## **¿Cloudflare CDN es gratuito?**

Cloudflare ofrece un plan Free que incluye diversas funciones de DNS, proxy, seguridad y caché.

Para muchos sitios web personales, blogs y pequeñas empresas, el plan Free es suficiente para empezar.

Los planes de pago ofrecen funciones y servicios adicionales, dependiendo del plan y de la disponibilidad actual de cada producto.

El plan más adecuado dependerá del tráfico de tu sitio web, los requisitos de seguridad, las necesidades de rendimiento y el presupuesto.

## **Lista de verificación para configurar Cloudflare CDN**

Antes de terminar la configuración, comprueba lo siguiente:

- Tu dominio se ha añadido a Cloudflare.
- Los registros DNS se han revisado.
- Los registros principales del sitio web están correctamente configurados.
- El proxy está activado para los registros web compatibles.
- Los nameservers se han actualizado.
- SSL/TLS está correctamente configurado.
- Los ajustes de caché se han revisado.
- Las páginas dinámicas no se almacenan en caché de forma incorrecta.
- El sitio web se carga correctamente mediante HTTPS.
- Los registros DNS del correo electrónico siguen siendo correctos.
- Se ha comprobado el rendimiento del sitio web.

## **Conclusión**

Configurar Cloudflare CDN es una forma práctica de mejorar la entrega de contenido de tu sitio web, gestionar DNS y añadir una capa adicional de protección.

El proceso básico consiste en añadir tu dominio a Cloudflare, revisar los registros DNS, activar el proxy, actualizar los nameservers, configurar SSL/TLS y ajustar las reglas de caché.

Aunque Cloudflare ofrece muchas funciones avanzadas, los principiantes pueden comenzar con una configuración básica y optimizar su sitio web gradualmente.

Al configurar correctamente DNS, el proxy, SSL/TLS y la caché, puedes crear una infraestructura web más eficiente y mejorar la experiencia de los visitantes desde diferentes regiones.

Recursos oficiales de Cloudflare:

Configuración de dominios de Cloudflare:  
[https://developers.cloudflare.com/fundamentals/manage-domains/add-site/](https://developers.cloudflare.com/fundamentals/manage-domains/add-site/)

Estado del proxy de Cloudflare:  
[https://developers.cloudflare.com/dns/proxy-status/](https://developers.cloudflare.com/dns/proxy-status/)

Cache Rules de Cloudflare:  
[https://developers.cloudflare.com/cache/how-to/cache-rules/](https://developers.cloudflare.com/cache/how-to/cache-rules/)

Purga de caché de Cloudflare:  
[https://developers.cloudflare.com/cache/how-to/purge-cache/](https://developers.cloudflare.com/cache/how-to/purge-cache/)