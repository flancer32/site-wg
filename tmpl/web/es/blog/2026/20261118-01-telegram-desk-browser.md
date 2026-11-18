---
title: "PDE v3: Telegram Desk ya funciona en el navegador"
description: "He probado Telegram Desk para PDE v3 con mi propia cuenta. ChatGPT ha podido leer conversaciones y enviar mensajes. La aplicación, que funciona en el navegador, ofrece 11 operaciones de texto."
summary: "He probado Telegram Desk para PDE v3 con mi propia cuenta. ChatGPT ha podido leer conversaciones y enviar mensajes. La aplicación, que funciona en el navegador, ofrece 11 operaciones de texto."
image: "/img/brand/pde-icon.png"
date: 2026-11-18
display_date: "18 de noviembre de 2026"
relations:
  - pde
---

# PDE v3: Telegram Desk ya funciona en el navegador

A finales de octubre conté que estaba preparando PDE v3 para las primeras pruebas. El 18 de noviembre pude comprobarlo con algo más que mensajes de prueba: utilicé ChatGPT para acceder a mi propia cuenta de Telegram a través de PDE v3.

Busqué un contacto, leí los últimos 50 mensajes de nuestra conversación y envié un mensaje privado. También publiqué entradas en mis canales de Telegram desde la misma conexión. Por ejemplo, [esta publicación](https://t.me/alexgusev_lab_es/97) salió directamente de ChatGPT.

## Telegram sin montar tu propio servidor

Telegram Desk es una aplicación independiente que funciona en el navegador. Se conecta directamente a Telegram, guarda las credenciales y la sesión en el navegador del usuario y ejecuta las operaciones autorizadas.

Otra aplicación de navegador, Browser Office, conecta el Desk con la infraestructura de PDE. ChatGPT accede a ella mediante MCP.

No hace falta montar un servidor propio ni contratar un VPS. Basta con un navegador en el ordenador. Las credenciales de Telegram se quedan en el navegador y no se envían al Gate de PDE, aunque las solicitudes y sus resultados sí pasan por él.

## Qué funciona por ahora

Telegram Desk dispone de **11 operaciones de texto**:

- **7 de lectura:** consultar la cuenta y los contactos, listar conversaciones, obtener historiales y mensajes concretos, y buscar mensajes.
- **4 que modifican el estado de Telegram:** enviar, editar y reenviar mensajes de texto, además de marcar conversaciones como leídas.

He probado las siete operaciones de lectura con mi propia cuenta. De las cuatro que modifican el estado, he comprobado el envío de mensajes, incluidas las publicaciones en canales. Las otras tres están implementadas, pero todavía no las he probado con mi cuenta real.

El propietario de la cuenta decide qué operaciones puede utilizar cada cliente de IA mediante los permisos configurados en el Desk.

Por ahora, el Desk solo trabaja con texto. No devuelve fotografías, vídeos, mensajes de voz ni archivos. Puede indicar que un mensaje contiene elementos que no son texto, pero no permite acceder a ese contenido mediante las operaciones actuales.

Tampoco tengo claro en qué casos un LLM necesita recibir el archivo original y cuándo bastaría con un texto extraído, la descripción de una imagen u otro resultado procesado. Prefiero comprobar primero hasta dónde podemos llegar con las operaciones de texto.

## Busco gente que quiera probarlo

Telegram Desk ya funciona en mi entorno de pruebas, pero PDE v3 sigue en desarrollo. Ahora quiero comprobar cómo se comporta con otros usuarios, navegadores y clientes de IA.

Si te apetece probar cómo ChatGPT u otro cliente MCP puede trabajar con tu Telegram, sigue [mi canal de Telegram](https://t.me/alexgusev_lab_es) y [escríbeme por privado](https://t.me/wiredgeese).

Cuéntame qué asistente de IA utilizas y qué te gustaría probar. Por ahora, el acceso al Gate de pruebas es por invitación. Ayudaré a los primeros participantes a configurarlo.

Seguramente aparecerán errores y limitaciones que todavía no conozco. Para eso sirven estas pruebas.

Más información sobre el proyecto en [pde.network](https://pde.network/).
