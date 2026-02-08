# 🛒🚨Alerta de Triple Confirmación de Compra

## 📌Descripción del proyecto

Este proyecto implementa una alerta SQL de triple confirmación de compra, diseñada para detectar operaciones potencialmente riesgosas o anómalas en sistemas transaccionales.

La alerta se activa cuando una compra cumple tres condiciones de confirmación simultáneas, lo que permite reducir falsos positivos y focalizar el análisis en eventos con mayor probabilidad de fraude o error operativo.

## 🎯Objetivos del proyecto

- Detectar compras con comportamiento atípico.
- Combinar múltiples señales en una única alerta robusta.
- Reducir ruido operativo generado por alertas simples.
- Mejorar el control transaccional mediante SQL.
- Facilitar auditorías y análisis de riesgo.

## 🏦Contexto de negocio

En entornos de banca, fintech y e-commerce:
- Una sola señal puede ser insuficiente para disparar una alerta.
- El exceso de alertas genera fatiga operativa.
- La combinación de señales reduce falsos positivos y mejora la eficiencia del monitoreo.

📌 La triple confirmación permite validar una compra desde distintos ángulos antes de alertar.

## 🧠Lógica de la triple confirmación

La consulta SQL evalúa una compra y dispara la alerta solo si se cumplen tres criterios simultáneos, por ejemplo:
- Monto inusual
- Superior a un umbral definido o fuera del comportamiento histórico del cliente.
- Frecuencia o repetición anómala
- Múltiples compras en un corto período de tiempo.
- Condición contextual sospechosa
- Cambio de ubicación, dispositivo, canal o medio de pago.
- Diferencia respecto al patrón habitual.

📌 Los criterios son configurables según el negocio.

## 🧪Ejemplos de uso

- Compras de alto monto repetidas en minutos.
- Transacciones desde una región no habitual del cliente.
- Operaciones consecutivas con distintos medios de pago.
- Combinación de volumen, frecuencia y contexto.

## 🛠️Tecnologías utilizadas

SQL

Compatible con:
- PostgreSQL
- SQL Server
- BigQuery
- Oracle
- MySQL (con ajustes menores)

## 📁Estructura del proyecto

├── alerta_triple_confirmacion_de_compra.sql
└── README.md
## ▶️Cómo utilizar la alerta

Abrir el archivo alerta_triple_confirmacion_de_compra.sql.

Configurar:
- Tabla de transacciones
- Ventana temporal
- Umbrales de monto y frecuencia
- Dimensiones de contexto (canal, ubicación, medio de pago)
- Ejecutar la consulta en el motor SQL.

Integrar la salida con:
- Sistemas de alertas
- Dashboards de fraude
- Flujos de revisión manual

## 🚀Posibles extensiones

- Ponderar las señales con un score de riesgo.
- Agregar historial del cliente (behavioral profiling).
- Clasificar alertas por severidad.
- Integrar con modelos de Machine Learning.
- Registrar alertas en una tabla histórica.

## 👤Autora

Flavia Hepp
Proyecto de SQL aplicado a detección de fraude y control transaccional.
