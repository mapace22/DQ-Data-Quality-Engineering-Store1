# 🛠️ Data Quality & Engineering Pipeline: Store 1 Customer Data

## 🎯 Visión General
Este proyecto establece un **Framework de Calidad de Datos** para "Store 1", enfocado en la transformación de datos brutos e inconsistentes en un formato estandarizado y "listo para el análisis". El objetivo central fue construir un pipeline robusto que garantice la integridad de los datos mediante protocolos automatizados de validación.

## 🧱 Implementación Técnica
El pipeline aborda problemas críticos de calidad de datos utilizando **Python**, con un enfoque en la escalabilidad y la resiliencia ante errores.

### Funcionalidades de Ingeniería:
* **Normalización Automatizada:** Implementación de algoritmos de manipulación de cadenas (`strip`, `replace`, `split`) para eliminar ruido y estandarizar identificadores de usuario y categorías de productos.
* **Integridad de Tipos de Datos:** Conversión sistemática de tipos de datos (ej. flotantes a enteros para métricas de edad) para asegurar la consistencia matemática en procesos posteriores.
* **Manejo Robustos de Errores:** Integración de bloques `try-except` para gestionar anomalías en los inputs de datos brutos, evitando fallos del pipeline durante el procesamiento por lotes.
* **Procesamiento por Lotes (Batch Processing):** Desarrollo de lógica iterativa para aplicar estándares de limpieza de forma eficiente en todo el dataset de clientes.

## 📊 Lógica del Pipeline (ETL)
1.  **Evaluación (Assessment):** Identificación de inconsistencias estructurales en `user_id`, `user_name`, y `user_age`.
2.  **Limpieza (Cleaning):** Eliminación de artefactos de formato y normalización de capitalización (case normalization) para datos categóricos.
3.  **Validación:** Aplicación de lógica de negocio para asegurar que los valores numéricos se encuentren dentro de los rangos operativos esperados.
4.  **Síntesis:** Generación de métricas clave (gasto total, mínimo y máximo) por perfil de usuario.

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python 3.12.1
* **Lógica Central:** Estructuras de datos dinámicas, manejo de excepciones y métodos avanzados de strings.
* **Entorno:** Jupyter Notebook / VS Code.

## 💡 Impacto de Datos
Mediante la implementación de este pipeline, se logró transicionar de datos fragmentados a una **"Única Fuente de Verdad" (Single Source of Truth)**. Esto garantiza que cualquier modelo predictivo o reporte financiero posterior se base en datos de alta fidelidad, eliminando sesgos operativos.
