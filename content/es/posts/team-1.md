---
title: "Cómo agregar miembros a Claude Team: guía de configuración y permisos"
slug: team
date: 2026-11-18
draft: false
---
# Cómo agregar miembros a Claude Team: guía de configuración y permisos

Claude Team está diseñado para empresas y organizaciones que desean utilizar Claude AI de forma colaborativa. Ofrece herramientas centralizadas para gestionar miembros, configurar permisos y administrar la facturación del equipo.

Tanto si estás creando un nuevo espacio de trabajo como si administras un equipo existente, saber cómo invitar usuarios y configurar sus permisos te ayudará a mantener la organización segura y ordenada.

Esta guía explica cómo agregar miembros, enviar invitaciones, administrar roles, compartir enlaces de invitación, eliminar usuarios y solucionar problemas habituales.

## 1. Qué necesitas antes de invitar miembros a Claude Team

Antes de agregar nuevos usuarios, asegúrate de que tu organización esté correctamente configurada.

### 1.1 Configurar una organización de Claude Team

Primero necesitas una organización activa de Claude Team.

Visita el sitio web oficial:

[https://claude.ai/](https://claude.ai/)

Inicia sesión con tu cuenta y asegúrate de acceder al espacio de trabajo correcto.

Si solo tienes una cuenta personal de Claude, es posible que necesites crear una organización o cambiar al plan Team antes de invitar a tus compañeros.

### 1.2 Preparar las direcciones de correo electrónico

Claude Team utiliza dominios de correo electrónico autorizados para controlar quién puede unirse al espacio de trabajo.

Antes de enviar invitaciones:

- Recopila las direcciones de correo electrónico de los miembros.
- Comprueba que no haya errores al escribirlas.
- Verifica que el dominio esté permitido por la organización.
- Asegúrate de que los destinatarios puedan acceder a sus buzones.

Si un dominio no está autorizado, la invitación o el proceso para unirse al equipo pueden fallar.

### 1.3 Comprobar las plazas disponibles

Claude Team utiliza plazas de pago para proporcionar acceso a los miembros del equipo.

Antes de invitar a nuevos usuarios, comprueba cuántas plazas están disponibles.

Un detalle importante es que las invitaciones pendientes reservan una plaza inmediatamente. No es necesario que el destinatario acepte la invitación para que esa plaza quede ocupada.

Si no hay suficientes plazas, un Owner o Primary Owner puede necesitar adquirir plazas adicionales.

## 2. Cómo invitar miembros a Claude Team

La forma habitual de agregar miembros es a través de la configuración de la organización.

### 2.1 Iniciar sesión en Claude Team

Accede a:

[https://claude.ai/](https://claude.ai/)

Inicia sesión con una cuenta que tenga permisos de Admin, Owner o Primary Owner.

Asegúrate de estar dentro de la organización correcta y no en tu cuenta personal de Claude.

### 2.2 Abrir la página de administración de miembros

Ve a:

**Organization settings → Members**

Desde esta página, los administradores autorizados pueden consultar los miembros existentes, revisar sus roles, gestionar invitaciones y agregar nuevos usuarios.

### 2.3 Hacer clic en Add member

En la página Members, selecciona:

**Add member**

Aparecerá una ventana donde podrás introducir los datos del nuevo integrante.

Sigue estos pasos:

1. Introduce la dirección de correo electrónico del miembro.
2. Selecciona el tipo de plaza correspondiente.
3. Elige el rol y los permisos adecuados.
4. Revisa que toda la información sea correcta.
5. Haz clic en **Add members** para enviar la invitación.

El sistema enviará un correo electrónico de invitación a la dirección indicada.

### 2.4 Aceptar la invitación

Después de recibir el correo, el nuevo miembro debe abrirlo y seguir las instrucciones para incorporarse a la organización.

Según la documentación de Anthropic, las invitaciones por correo electrónico caducan después de 21 días.

Si el destinatario no acepta la invitación dentro de ese plazo, un administrador tendrá que enviar otra.

## 3. Cómo invitar a varios miembros de Claude Team al mismo tiempo

Si tu empresa necesita incorporar a varios empleados, Claude Team ofrece una opción de invitación masiva.

Es especialmente útil al configurar un nuevo equipo o incorporar a varios trabajadores.

### 3.1 Utilizar la opción Bulk add

Accede a:

**Organization settings → Members → Add member**

Busca la opción **Bulk add**.

### 3.2 Introducir varias direcciones de correo

Puedes pegar varias direcciones de correo electrónico en el campo de invitación.

Separa las direcciones mediante comas o saltos de línea.

Por ejemplo:

```
user1@company.com
user2@company.com
user3@company.com
user4@company.com
```

Comprueba que todas las direcciones sean correctas y cumplan los requisitos de dominio de correo de tu organización.

### 3.3 Enviar las invitaciones

Después de introducir las direcciones:

1. Revisa la lista de miembros.
2. Selecciona los tipos de plaza adecuados.
3. Configura los roles y permisos.
4. Envía las invitaciones.

Una vez completado el proceso, vuelve a la página Members para comprobar el estado de cada invitación.

Si algún miembro no recibe el correo, verifica su dirección y consulta la sección Pending.

## 4. Cómo compartir un enlace de invitación de Claude Team

Además de enviar invitaciones individuales por correo electrónico, los administradores pueden compartir un enlace de invitación con sus compañeros.

Este método puede facilitar la incorporación de varios miembros a una misma organización.

### 4.1 Encontrar el enlace de invitación

Inicia sesión en Claude Team y accede a:

**Organization settings → Identity and access**

Busca la sección **Invite link** dentro de la configuración de acceso global.

Haz clic en el botón de copiar para obtener el enlace.

La disponibilidad de esta función depende del tipo de organización y de su configuración de seguridad. Por ejemplo, los enlaces de invitación están habilitados de forma predeterminada en las nuevas organizaciones Team, mientras que las organizaciones Enterprise que utilizan SSO no pueden utilizar este método.

### 4.2 Compartir el enlace con los miembros

Puedes distribuir el enlace mediante:

- Correo electrónico corporativo
- Canales de Slack
- Herramientas de comunicación internas
- Plataformas de colaboración
- Bases de conocimiento de la empresa

Los miembros pueden abrir el enlace, iniciar sesión o crear una cuenta y seguir las instrucciones para incorporarse al equipo.

### 4.3 Gestionar la seguridad del enlace

Los enlaces de invitación deben compartirse únicamente con compañeros autorizados.

Ten en cuenta estas recomendaciones:

- No publiques el enlace en sitios web públicos.
- Compártelo solo mediante canales internos de confianza.
- Comprueba si el enlace sigue activo.
- Desactívalo cuando ya no sea necesario.
- Genera uno nuevo si sospechas que el anterior se ha filtrado.

Según la documentación actual de Anthropic, los enlaces de invitación caducan automáticamente 90 días después de su creación.

Si desactivas o generas un nuevo enlace, el anterior deja de funcionar inmediatamente.

Los miembros que se incorporan mediante un enlace reciben el tipo de plaza disponible de menor nivel. Si no quedan plazas disponibles, puede ser necesario asignar plazas adicionales.

## 5. Roles y permisos de Claude Team

Después de invitar a los miembros, debes asignarles los roles adecuados según sus responsabilidades.

Claude Team ofrece cuatro roles principales:

- User
- Admin
- Owner
- Primary Owner

Cada uno dispone de permisos diferentes.

### 5.1 User: miembro estándar

El rol User está destinado a los empleados que utilizan Claude para sus tareas habituales.

Entre sus funciones habituales se encuentran:

- Crear y modificar conversaciones.
- Utilizar Projects.
- Acceder a las funciones disponibles para el equipo.
- Trabajar con recursos compartidos según la configuración de la organización.

Por lo general, los usuarios normales no pueden administrar miembros ni modificar la configuración de facturación.

### 5.2 Admin: administrador del equipo

Los administradores se encargan de la gestión diaria de la organización.

Sus permisos incluyen:

- Invitar nuevos miembros.
- Eliminar miembros del equipo.
- Cancelar invitaciones pendientes.
- Gestionar el acceso de los miembros dentro de sus permisos.

Sin embargo, los administradores no pueden realizar todas las acciones de gestión de la organización.

Por ejemplo, no tienen los mismos permisos de facturación ni pueden modificar los roles de los miembros como lo hacen los Owners.

### 5.3 Owner: propietario de la organización

Los Owners disponen de permisos de administración más amplios.

Según la configuración de la organización, pueden:

- Invitar y eliminar miembros.
- Administrar las asignaciones de Admin y Owner.
- Modificar los roles de los miembros.
- Consultar y pagar facturas.
- Agregar o modificar métodos de pago.
- Comprar plazas adicionales.

Los Owners desempeñan un papel importante en la gestión de las suscripciones y los miembros de la organización.

### 5.4 Primary Owner: propietario principal

El Primary Owner es el propietario principal de la organización Claude Team.

Este rol dispone de amplios permisos administrativos y de facturación.

Además de las funciones de gestión habituales, puede supervisar la asignación de plazas y transferir la responsabilidad de Primary Owner a otro miembro que cumpla los requisitos.

Cada organización solo puede tener un Primary Owner al mismo tiempo.

Por motivos de seguridad, este rol debe asignarse a la persona responsable de la gestión general de la cuenta de la organización.

## 6. Cómo cambiar el rol de un miembro de Claude Team

Si cambian las responsabilidades de un empleado, es posible que necesites actualizar sus permisos.

Solo los Owners y Primary Owners pueden modificar los roles de los miembros.

Sigue estos pasos:

1. Inicia sesión en tu organización Claude Team.
2. Abre **Organization settings**.
3. Selecciona **Members**.
4. Busca al miembro cuyo rol deseas cambiar.
5. Abre el menú desplegable del rol junto a su nombre.
6. Selecciona el nuevo rol.
7. Confirma el cambio.

Por ejemplo, si un empleado pasa a encargarse de incorporar nuevos miembros, un Owner puede cambiar su rol de User a Admin.

Si no encuentras la opción para modificar el rol, comprueba si tu cuenta tiene los permisos necesarios.

## 7. Cómo eliminar un miembro de Claude Team

Cuando un empleado deja la empresa o ya no necesita acceder al espacio de trabajo, puedes eliminarlo de la organización.

### 7.1 Abrir la página Members

Inicia sesión en Claude Team y accede a:

**Organization settings → Members**

Busca al miembro que deseas eliminar.

### 7.2 Eliminar al miembro

Haz clic en el botón de menú situado junto al nombre del miembro.

Selecciona:

**Remove from team**

Sigue las instrucciones de confirmación para completar el proceso.

### 7.3 Qué ocurre después de eliminar a un miembro

Cuando se elimina a un miembro:

- Pierde inmediatamente el acceso a la organización.
- La plaza que tenía asignada queda disponible para otro miembro.
- La plaza puede asignarse a otra persona.
- Si vuelve a incorporarse utilizando la misma dirección de correo electrónico, se conserva el historial de su cuenta.

Ten en cuenta que eliminar a un miembro no reduce automáticamente el número total de plazas contratadas por la organización.

Si deseas reducir el número de plazas de la suscripción, tendrás que gestionar esa configuración por separado.

Por lo general, un Owner o Primary Owner no puede eliminarse a sí mismo de la organización. Otro propietario con los permisos adecuados debe realizar esa acción.

## 8. Problemas habituales al invitar miembros a Claude Team

En ocasiones, las invitaciones pueden fallar o los miembros pueden tener dificultades para unirse a la organización. A continuación se explican algunos problemas frecuentes y sus posibles soluciones.

### 8.1 El dominio del correo electrónico no está permitido

Un problema habitual es que la dirección de correo no coincida con los dominios autorizados por la organización.

Posibles soluciones:

- Comprueba que la dirección esté escrita correctamente.
- Confirma que el dominio esté permitido.
- Pide al administrador que revise la configuración de dominios autorizados.
- Utiliza una dirección de correo corporativa válida si es necesario.

### 8.2 No hay suficientes plazas disponibles

Si todas las plazas están asignadas o reservadas por invitaciones pendientes, es posible que no puedas agregar más miembros.

Puedes intentar lo siguiente:

- Revisar la asignación actual de plazas.
- Comprobar si hay miembros que ya no necesitan acceso.
- Eliminar los miembros innecesarios para liberar plazas.
- Cancelar las invitaciones que no se utilizarán.
- Pedir a un Owner o Primary Owner que compre plazas adicionales si es necesario.

### 8.3 El miembro no recibe el correo de invitación

Si un miembro no encuentra el correo, comprueba lo siguiente:

- ¿La dirección de correo es correcta?
- ¿Se ha enviado correctamente la invitación?
- ¿El mensaje está en la carpeta de spam o correo no deseado?
- ¿La invitación sigue pendiente?
- ¿Ha caducado la invitación?

Para reenviar una invitación caducada:

1. Abre **Organization settings → Members**.
2. Selecciona la pestaña **Pending**.
3. Busca la dirección de correo correspondiente.
4. Selecciona la opción para reenviar la invitación.

### 8.4 No se pueden modificar los permisos

Si no puedes cambiar el rol de un miembro, es posible que tu cuenta no tenga permisos suficientes.

Según la documentación de Anthropic sobre roles y permisos, solo los Owners y Primary Owners pueden modificar los roles de los miembros.

Si necesitas permisos administrativos adicionales, ponte en contacto con un Owner.

### 8.5 El enlace de invitación no funciona

Un enlace puede dejar de funcionar si ha caducado, ha sido desactivado o se ha generado uno nuevo.

Pide al administrador que revise el enlace en:

**Organization settings → Identity and access**

Si es necesario, podrá generar un nuevo enlace y compartirlo con el equipo.

## 9. Buenas prácticas para administrar un espacio de trabajo Claude Team

Para las empresas y organizaciones con varios usuarios, una buena gestión de miembros ayuda a mantener la seguridad y controlar los costes de suscripción.

### 9.1 Asignar roles según las responsabilidades

Evita conceder permisos de Admin u Owner a todos los empleados.

Una distribución práctica puede ser:

- User: empleados habituales.
- Admin: personal responsable de gestionar el equipo.
- Owner: responsables de la organización y las suscripciones.
- Primary Owner: administrador principal de la cuenta de la organización.

Conceder únicamente los permisos necesarios ayuda a reducir los riesgos de acceso innecesario.

### 9.2 Revisar periódicamente la lista de miembros

Comprueba la página Members de forma regular.

Presta atención a:

- Empleados que ya no trabajan en la empresa.
- Miembros que ya no utilizan Claude.
- Invitaciones que todavía no se han aceptado.
- Cuentas con permisos administrativos innecesarios.

Eliminar las cuentas que ya no se utilizan también permite liberar plazas para nuevos empleados.

### 9.3 Planificar correctamente las plazas

Antes de invitar a nuevos usuarios, revisa el número y el tipo de plazas disponibles.

Claude Team ofrece diferentes tipos de plazas, incluidas Standard y Premium, con distintas funciones y límites de uso.

Asigna cada tipo de plaza según las necesidades reales de cada empleado, en lugar de elegir automáticamente la misma opción para todos.

### 9.4 Proteger los enlaces de invitación

Los enlaces de invitación pueden permitir el acceso directo a la organización.

Compártelos únicamente con compañeros de confianza. Si un enlace se expone accidentalmente, desactívalo o genera uno nuevo.

Si tu organización necesita un control de acceso más estricto, las invitaciones individuales por correo electrónico pueden ser una mejor alternativa, ya que permiten revisar las solicitudes antes de que los miembros se incorporen.

## 10. Gestión de pagos y suscripciones de Claude Team

Además de administrar los miembros del equipo, las organizaciones deben prestar atención a la facturación de la suscripción.

Las suscripciones de Claude Team pueden incluir cargos recurrentes, cambios en la asignación de plazas y diferentes requisitos de pago.

Antes de comprar plazas adicionales, comprueba:

- El plan de suscripción actual.
- El número de plazas asignadas.
- El precio aplicable a cada plaza.
- El ciclo de facturación.
- Los métodos de pago disponibles.

Si utilizas una tarjeta virtual para pagar servicios digitales internacionales, asegúrate de que el comercio acepte esa tarjeta y de que el saldo disponible sea suficiente.

CoinePay ofrece opciones de tarjetas virtuales para pagos en sitios web internacionales y suscripciones digitales. Puedes consultar sus servicios y condiciones de pago aquí:

[https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

Para los usuarios de la red TRON que también realizan transferencias de USDT, TRXAPI ofrece un servicio de alquiler de Energy que puede ayudar a gestionar los recursos de red necesarios para las transacciones on-chain.

Alquiler de Energy de TRXAPI:  
[https://login.trxapi.io/energy](https://login.trxapi.io/energy)

Código de invitación: **RT9G2YGH**

Antes de enviar USDT, verifica siempre la red, la dirección del destinatario y las comisiones de la transacción.

## 11. Conclusión

Invitar miembros y administrar permisos son tareas fundamentales para gestionar una organización de Claude Team.

Los administradores pueden agregar nuevos miembros, gestionar invitaciones pendientes y eliminar usuarios desde la página Members. Los Owners y Primary Owners disponen de permisos adicionales para administrar roles, facturación y asignación de plazas.

Si necesitas incorporar a varios empleados, las funciones Bulk add y los enlaces de invitación pueden facilitar el proceso.

Para mantener tu organización segura y bien organizada, recuerda:

- Asignar los roles según las responsabilidades.
- Comprobar las plazas disponibles antes de enviar invitaciones.
- Revisar periódicamente las invitaciones pendientes.
- Eliminar las cuentas que ya no se necesitan.
- Proteger los enlaces de invitación.
- Supervisar los costes de suscripción y la configuración de facturación.

Siguiendo estas recomendaciones, tu organización podrá gestionar los miembros de Claude Team de forma más eficiente y mantener un mejor control sobre el acceso al espacio de trabajo.

Para consultar las instrucciones más recientes y la disponibilidad de las funciones, revisa el Centro de ayuda oficial de Anthropic antes de realizar cambios en tu organización.

## Recursos oficiales de Claude Team

- Administrar miembros en los planes Team y Enterprise: [https://support.claude.com/en/articles/13133750-manage-members-on-team-and-enterprise-plans](https://support.claude.com/en/articles/13133750-manage-members-on-team-and-enterprise-plans)
- Roles y permisos: [https://support.claude.com/en/articles/9267276-roles-and-permissions](https://support.claude.com/en/articles/9267276-roles-and-permissions)
- Unirse a una organización mediante un enlace de invitación: [https://support.claude.com/en/articles/13776697-join-an-organization-via-invite-link](https://support.claude.com/en/articles/13776697-join-an-organization-via-invite-link)
- Comprar y administrar plazas en los planes Team: [https://support.claude.com/en/articles/12004354-purchase-and-manage-seats-on-team-plans](https://support.claude.com/en/articles/12004354-purchase-and-manage-seats-on-team-plans)

