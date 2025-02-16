---
title: 'Detalles de diseño: estructura de motor de registro'
description: La interfaz de registro utiliza funciones de motor de registro para preparar e insertar movimientos de contabilidad y registros de movimientos de IVA.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-posting-engine-structure" />Detalles de diseño: estructura de motor de registro
La interfaz de registro y otras funciones en la codeunit 12 utilizan funciones de motor de registro para preparar e insertar movimientos de contabilidad y registros de movimientos de IVA. El motor de registro también es responsable de la creación del registro de contabilidad.  
  
 Las funciones en la tabla siguiente proporcionan un marco estándar para diseñar procedimientos de registro (como Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry y Reverse) y acceso exclusivo a la tabla 17, Mov. C/G.  
  
|Routine|Description|  
|-------------|---------------------------------------|  
|StartPosting|Inicializa el búfer de registro TempGLEntryBuf, bloquea las tablas de movimientos de contabilidad y de IVA e inicializa el periodo contable, el registro de contabilidad y el tipo de cambio. Si se le llama solo una vez, NextEntryNo es 0.|  
|ContinuePosting|Comprueba y registra el IVA no realizado para el incremento NextTransactionNo de la transacción anterior y prepara el registro de la línea siguiente.|  
|FinishPosting|Finaliza el registro insertando los movimientos de contabilidad desde el búfer temporal a la tabla de la base de datos. Se utiliza siempre con StartPosting. Comprueba la presencia de inconsistencias.|  
|InitGLEntry|Se utiliza para inicializar un nuevo movimiento de contabilidad para la línea de diario general. Devuelve GLEntry como parámetro.|  
|InitGLEntryVAT|Igual que InitGLEntry, pero también asigna Cta. contrapartida y SummarizeVAT.|  
|InitGLEntryVATCopy|Similar a InitGLEntryVAT, pero también copia datos de grupos de registro desde movimientos de IVA antes de SummarizeVAT.|  
|InsertGLEntry|La única función que inserta el movimiento de contabilidad general en la tabla global TempGLEntryBuf. Utilice siempre esta función para insertar.|  
|CreateGLEntry|Lleva a cabo una acción InitGLEntry, asigna un importe adicional de divisa y realiza una acción InsertGLEntry. Reemplaza varias líneas de código con una sola llamada a función.|  
|CreateGLEntryBalAcc|Igual que CreateGLEntry, pero también asigna Tipo contrapartida y Cta. contrapartida.|  
|CreateGLEntryVAT|Igual que CreateGLEntry, pero con procesamiento adicional para grupos de registro y guardado en búfer temporal de IVA:<br /><br /> `GLEntry.CopyPostingGroupsFromDtldCVBuf(DtldCVLedgEntryBuf,GenJnlLine."Gen. Posting Type");`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryVATCollectAdj|Igual que CreateGLEntry, pero con recopilación adicional de ajustes y guardado en búfer temporal de IVA:<br /><br /> `CollectAdjustment(AdjAmount,GLEntry.Amount,GLEntry."Additional-Currency Amount",OriginalDateSet);`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryFromVATEntry|Igual que CreateGLEntry, pero también copia grupos de registro desde movimientos de IVA.|  
  
## <a name="see-also" />Consulte también
 [Detalles de diseño: estructura de interfaz de registro](design-details-posting-interface-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
