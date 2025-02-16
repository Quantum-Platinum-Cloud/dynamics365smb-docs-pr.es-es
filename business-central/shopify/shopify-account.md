---
title: Crear y configurar una cuenta de Shopify
description: Aprenda a obtener una cuenta de Shopify para que pueda demostrar el flujo de trabajo para integrar Shopify y Business Central.
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# Crear y configurar una cuenta de Shopify

Si está considerando utilizar Shopify como su solución de comercio electrónico y necesita una cuenta Shopify para validar el flujo de trabajo integrado, tiene las siguientes opciones:

- Obtenga una versión de prueba. Este es el punto de partida típico para los usuarios finales.  
- Crear tiendas de desarrollo. Este enfoque es para socios que realizan demostraciones recurrentes, capacitaciones y brindan soporte.

## Prueba (usuario final)

Vaya al [sitio web de Shopify](https://www.shopify.com) y use su cuenta de correo electrónico como cuenta de administrador para registrarse para una prueba gratuita. Para obtener más información sobre cómo crear y personalizar su tienda en línea, consulte el [Centro de ayuda de Shopify](https://help.shopify.com/).

En el **Administrador de Shopify** de la tienda creada, aplique la siguiente **Configuración**:

- Desactive **Archivar automáticamente el pedido** en la sección **Procesamiento de pedidos** de los ajustes de [**Finalizar compra**](https://www.shopify.com/admin/settings/checkout) del **Administrador de Shopify**.
- Considere habilitar *Mostrar enlace de inicio de sesión en la tienda y pagar* en la sección **Configuración de la cuenta del cliente** de la configuración de pago.
- Considere seleccionar la opción *Nombre de la empresa - Opcional* en la sección **Información del cliente** de la configuración de pago.
- Habilite la opción **Mostrar opciones de propinas al finalizar la compra** en la sección **Propinas** de la configuración de la finalización de la compra, si planea demostrar propinas
- Activa los pagos de prueba. Tiene dos opciones. Comience yendo a la configuración de [**Pagos**](https://www.shopify.com/admin/settings/payments):  
  1. *(para probar) Bogus Gateway*. Para obtener más información, consulte [Activar Bogus Gateway para realizar pruebas](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* en modo de prueba. Para obtener más información, consulte [Probar Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Seleccione un plan en la configuración de [**Plan**](https://www.shopify.com/admin/settings/plan) para poder probar el proceso de pago.

> [!Important]  
> Para evitar pagos, recuerda cancelar su prueba de Shopify.

## Tienda de desarrollo

Comience por unirse al [Programa de socios de Shopify](https://help.shopify.com/partners/about). Luego, use el **panel de socios** para crear la tienda en desarrollo. Más información en [Crear tiendas de desarrollo](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Después de crear la tienda, en el **Administrador de Shopify** de la tienda creada, aplique la siguiente **Configuración**:

- Desactive **Archivar automáticamente el pedido** en la sección **Procesamiento de pedidos** de los ajustes de [**Finalizar compra**](https://www.shopify.com/admin/settings/checkout) del **Administrador de Shopify**.
- Considere habilitar *Mostrar enlace de inicio de sesión en la tienda y pagar* en la sección **Configuración de la cuenta del cliente** de la configuración de pago.
- Considere seleccionar la opción *Nombre de la empresa - Opcional* en la sección **Información del cliente** de la configuración de pago.
- Si tiene previsto demostrar las propinas, habilite la opción **Mostrar opciones de propinas al finalizar la compra** en la sección **Propinas** de la configuración de la finalización de la compra.
- Activa los pagos de prueba. Tiene dos opciones. Comience yendo a la configuración de [**Pagos**](https://www.shopify.com/admin/settings/payments):  
  1. *(para probar) Bogus Gateway*. Para obtener más información, consulte [Activar Bogus Gateway para realizar pruebas](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify Payments* en modo de prueba. Obtenga más información en [Probar Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

> [!Note]  
> Las tiendas de desarrollo suelen estar protegidas con contraseña. Cuando intenta abrir una página específica en su tienda en línea desde [!INCLUDE [prod_short](../includes/prod_short.md)], por ejemplo, para ir a un producto o pedido específico, deberá ingresar su contraseña. Mientras realiza la prueba, para evitar tener que ingresar su contraseña, inicie sesión en su administrador de Shopify y abra su tienda desde allí. No necesitará ingresar la contraseña de la tienda hasta que cierre el navegador o la sesión expire.  

## Consulte también

[Comenzar a usar el conector Shopify](get-started.md)  
[Tutorial: Configurar y usar el Shopify Connector](walkthrough-setting-up-and-using-shopify.md)
