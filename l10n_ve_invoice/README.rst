====================
Binaural Facturación
====================

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/licence-LGPL--3-blue.png
    :target: http://www.gnu.org/licenses/lgpl-3.0-standalone.html
    :alt: License: LGPL-3

|badge1|

Este modulo agrega funcionalidades que permiten manejar la facturación en Venezuela utilizando
moneda extranjera.


Campos agregados a modelos existentes
"""""""""""""""""""""""""""""""""""""

* Asiento Contable / Factura (account.move).

  * correlative: Correlativo.
  * invoice_reception_date: Fecha de recepción.
  * last_payment_date: Fecha de último pago.

* Diario Contable (account.journal).

  * series_correlative_sequence_id: Número de control para series.

Configuraciones
"""""""""""""""
* Compañía (res.company).

  * max_product_invoice: Cantidad máxima de productos en la factura.
  * group_sales_invoicing_series: Grupo para series de ventas.

Registros agregados
"""""""""""""""""""

* Secuencia (ir.sequence).

  * invoice_correlative: "Número de control de facturas" (código: invoice.correlative).

  * series_invoicing_correlative: "Número de control de facturas para series" (código: series.invoice.correlative).

* Regla de acceso (ir.rule).

  * invoice_correlative_rule: "Restricted Record: multi-company sequence".

Funcionalidades
"""""""""""""""

* El correlativo se genera automáticamente al validar la factura en el caso de las facturas de venta, utilizando la secuencia con el código "invoice.correlative".
* Las secuencias son por compañía.

Validaciones
""""""""""""

* No poder agregar más líneas que las seleccionadas en la configuración de la compañía.

Reportes
""""""""

* Forma libre.
* Nota de venta.
* Libro de ventas.
* Libro de compras.



**Tabla de Contenidos**

.. contents::
   :local:

Créditos
========

Autor/es
~~~~~~~~

* Binauraldev

Mantenedor/es
~~~~~~~~~~~~~

Este módulo es mantenido por Binaural.

.. image:: https://binauraldev.com/wp-content/uploads/2022/01/logo-binaural.png
   :alt: Binaural dev
   :target: https://binauraldev.com/