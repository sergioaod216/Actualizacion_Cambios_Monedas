# Actualización de cambios diarios de monedas

**Examen 4 - Programación Declarativa**

Proyecto desarrollado en PostgreSQL para registrar y actualizar las cotizaciones diarias de cuatro monedas durante los últimos dos meses.

## Monedas utilizadas

- COP - Peso colombiano
- EUR - Euro
- GBP - Libra esterlina
- BTC - Bitcoin

**Período:** 17 de septiembre al 16 de noviembre de 2026.

Las cotizaciones se expresan tomando como referencia el dólar estadounidense (USD).

## Instrucciones de ejecución

1. Crear una base de datos llamada `Monedas` en PostgreSQL.
2. Abrir `DDL - Moneda.sql`, comentar la instrucción `CREATE DATABASE Monedas;` y ejecutar el resto del archivo dentro de la base creada.
3. Ejecutar `DML - Monedas.sql` para cargar los datos iniciales.
4. Ejecutar `DDL - Moneda - Secuencias.sql` para actualizar las secuencias.
5. Ejecutar `Actualizacion_Cambios_Monedas.sql` para registrar los cambios de las cuatro monedas.

## Funcionamiento

El script verifica si las monedas existen en la base de datos. Si alguna no existe, la agrega.

Después registra los cambios correspondientes a cada fecha. Si el cambio ya existe, actualiza su valor utilizando `ON CONFLICT`.

El código puede ejecutarse varias veces sin duplicar las cotizaciones.

## Resultados esperados

Se registran 61 días de cotizaciones para cada moneda, con un total de 244 registros correspondientes al período indicado.

La criptomoneda Bitcoin permite comprobar la inserción de una moneda que no estaba registrada inicialmente.

**Fuente de cotizaciones:** https://github.com/fawazahmed0/exchange-api
