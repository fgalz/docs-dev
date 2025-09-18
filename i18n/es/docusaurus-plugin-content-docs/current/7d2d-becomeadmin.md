---
id: 7d2d-becomeadmin
title: "7 Days to Die: Cómo convertirse en administrador de 7 Days to Die"
description: Cómo convertirse en administrador de los servidores del juego 7 Days to Die - Documentación de ZAP-Hosting.com 
sidebar_label: Convertirse en administrador
services:
  - gameserver-7d2d
---

import InlineVoucher from '@site/src/components/InlineVoucher';

## Introducción
La asignación de permisos de administrador te permite una administración sencilla y completa con control total de tu servidor. Como administrador, tienes la opción de utilizar todas las opciones y funciones disponibles proporcionadas por el juego directamente en el juego. Todos los pasos que necesitas seguir para asignar permisos de administrador a tu servidor se describirán a continuación. 
<InlineVoucher />

## Configuración
Agregar un administrador se hace a través de la configuración **serveradmin.xml**, que puedes encontrar en la interfaz web bajo Configs.

![](https://screensaver01.zap-hosting.com/index.php/s/wXpLL2qyZE2zCYa/preview)

Puedes encontrar tu SteamID64 yendo a tu perfil de Steam y haciendo clic derecho en cualquier lugar de él. Allí luego haces clic en **Copiar URL de Steam**. 

![](https://screensaver01.zap-hosting.com/index.php/s/Q9WJ8GwbHCmTRPx/preview)

Después abre una de las siguientes páginas y pega la URL de tu perfil allí: 

- https://steamrep.com/
- https://steamidfinder.com/
- https://steamid.io/

Esto te proporcionará información general así como la ID de Steam de tu cuenta. En este caso solo necesitamos el SteamID64. El SteamID64 se especifica entonces bajo ``<admins>...</admins>``. Esto se verá así:

```
 <users>
    <user steamID="76561198021925107" name="Pista de quién es este usuario" permission_level="0" />
  </users>
```

:::danger ¿El registro de administrador no es reconocido? 
Asegúrate de eliminar los caracteres de comentario `<!--` y `-->` para hacer válida la línea. De lo contrario, la línea permanece solo como un comentario y no se aplicará. Simplemente elimina los caracteres al principio y al final de la línea para activarla.
:::

El juego ofrece la posibilidad de definir diferentes niveles de permisos para los permisos de administrador. Esto significa que es posible definir diferentes grupos de administradores con diferentes permisos. El nivel se define por la opción ``permission_level``. Esto puede ser configurado de 0 a 1000. Dependiendo de cómo esté configurado, los administradores tendrán acceso a los permisos asignados. Una vez hecho esto, los permisos de administrador se han asignado con éxito. 



## Permisos

Los permisos para todos los comandos de administrador se pueden definir bajo ``permissions``. Para esto, el ``permission_level`` debe ser ajustado, al igual que cuando se añaden administradores. Esto se verá así:

```
<permissions>
	<permission cmd="dm" permission_level="0" ></permission>
	<permission cmd="kick" permission_level="1" ></permission>
	<permission cmd="say" permission_level="1000" ></permission>
    <permission cmd="chunkcache" permission_level="1000" ></permission>
    <permission cmd="debugshot" permission_level="1000" ></permission>
    <permission cmd="debugweather" permission_level="1000" ></permission>
    <permission cmd="getgamepref" permission_level="1000" ></permission>
</permissions>
```

Un nivel de permiso es un valor entre 0 y 1000 y determina qué permisos tiene un jugador. 1000 es el más bajo (sin permisos) y 0 es el más alto (permisos completos de administrador). Dependiendo de cómo deben ser los permisos en este aspecto, esto debe ser ajustado en consecuencia. 


## Conclusión

Felicidades, has configurado con éxito los permisos de administrador. Para más preguntas o asistencia, ¡no dudes en contactar a nuestro equipo de soporte, que está disponible diariamente para ayudarte! 🙂

<InlineVoucher />