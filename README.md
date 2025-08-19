[# activacion-de-Conceptos-y-Regresion-lineal

Proyecto educativo para **activar conceptos de Machine Learning** aplicando un flujo completo de **Regresión Lineal** sobre el dataset `Credit.csv`.  
El objetivo es practicar **EDA**, **preprocesamiento**, **entrenamiento**, **evaluación** y **validación de supuestos** del modelo.

---

## 📌 Tabla de contenido
- [Objetivos de aprendizaje](#-objetivos-de-aprendizaje)
- [Estructura del proyecto](#-estructura-del-proyecto)
- [Dataset](#-dataset)
- [Requisitos](#-requisitos)
- [Cómo ejecutar](#-cómo-ejecutar)
  - [Google Colab](#google-colab)
  - [Local (Jupyter/VSCode)](#local-jupytervscode)
- [Métricas y validaciones](#-métricas-y-validaciones)
- [Próximos pasos (roadmap)](#-próximos-pasos-roadmap)
- [Buenas prácticas de reproducibilidad](#-buenas-prácticas-de-reproducibilidad)
- [Contribuciones](#-contribuciones)
- [Licencia](#-licencia)
- [Autor](#-autor)

---

## 🎯 Objetivos de aprendizaje
- Repasar el **pipeline** de ML: EDA - limpieza - ingeniería de variables - partición de datos - modelado - evaluación.
- Entrenar y evaluar un modelo de **Regresión Lineal**.
- Interpretar métricas (**R2**, **MAE**, **MSE/RMSE**) y validar supuestos del modelo.
- Dejar un notebook reproducible para futuras iteraciones (regularización, comparación de modelos, etc.).

____________________________________________________

> Si `Credit.csv` está por ahora en la raíz del repo, puedes moverlo a `data/` o actualizar la ruta usada en el notebook (variable `DATA_PATH`).

---

## 🧠 Dataset
`Credit.csv` contiene variables financieras/demográficas de clientes (ej.: ingresos, uso de crédito, edad, estado civil, etc.).  
La **variable objetivo** es continua (ej.: `Balance`), adecuada para regresión.

- **Fuente**: material docente/ejercicio (indicar si existe una URL o autor específico).
- **Campos**: documentar brevemente las variables más relevantes cuando se usen en el notebook.

---

## 🛠️ Requisitos
- **Python** 3.10+
- Paquetes:
  - `pandas`, `numpy`
  - `scikit-learn`
  - `matplotlib` y/o `plotly`
  - `seaborn` (opcional para EDA)

Instalación rápida:
```bash
pip install -U pandas numpy scikit-learn matplotlib seaborn
# o, si existe:
pip install -r requirements.txt
________________________________________________

Cómo ejecutar
Google Colab

Abre el notebook en notebooks/Proyecto_6_ActivaciondeConceptosyRegresionLineal.ipynb.

Asegúrate de que data/Credit.csv esté disponible (subiéndolo o montando Google Drive).

Ejecuta las celdas en orden: EDA - preprocesamiento - entrenamiento - evaluación - validación de supuestos.

(Opcional) Guarda figuras en outputs/figuras/ y el modelo en outputs/modelos/.
_______________________________________________

Local (Jupyter/VSCode)

git clone https://github.com/cabarcn/activacion-de-Conceptos-y-Regresion-lineal.git
cd activacion-de-Conceptos-y-Regresion-lineal

# (opcional) crear entorno virtual
python -m venv .venv

# Windows:
.venv\Scripts\activate

# Linux/Mac:
source .venv/bin/activate

pip install -r requirements.txt  # si está disponible
# o instala paquetes mínimos:

pip install -U pandas numpy scikit-learn matplotlib seaborn
# Abre el notebook con Jupyter o VS Code y ejecútalo

__________________________________________________

Métricas y validaciones

Se reportan (como mínimo):

R² (coeficiente de determinación)

MAE (Mean Absolute Error)

MSE / RMSE (Root Mean Squared Error)

Validaciones visuales sugeridas:

Real vs. Predicho

Distribución de residuos

QQ-plot (normalidad de residuos)

Residuos vs. predicciones (homocedasticidad)

VIF o correlaciones (para multicolinealidad), si aplica

Incluye al final del notebook una celda que imprima las métricas y guarde gráficos en outputs/figuras/
____________________________________________________________

Próximos pasos (roadmap)

 Regularización: Ridge / Lasso / ElasticNet y comparación de resultados.

 Ingeniería de variables (interacciones, transformaciones).

 Selección de características (RFE, importancia, VIF).

 Validación cruzada y curvas de aprendizaje.

 Comparar con baselines: KNN, Árboles, Random Forest.

 Exportar el modelo (joblib) a outputs/modelos/.

 ____________________________________________
 🔬 Buenas prácticas de reproducibilidad

Fijar random_state en train_test_split y en los modelos.

Mantener y versionar requirements.txt.

Documentar supuestos y decisiones del preprocesamiento en el notebook.

Evitar subir datos sensibles o archivos >100 MB (usar Git LFS o almacenamiento externo).

🤝 Contribuciones

Las mejoras son bienvenidas. Abre un Issue o un Pull Request con propuestas (nuevos gráficos, comparaciones de modelos, refactor del pipeline, etc.).

📄 Licencia

Uso académico/educativo. Ajusta a la licencia que prefieras (por ejemplo, MIT).

✍️ Autor

Cristopher Abarca
Desarrollador / Estudiante de Ingeniería Informática
