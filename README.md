# Road Damage Detection

Detección y clasificación de daños en vías (baches) usando visión computacional.

> 🚧 Proyecto en desarrollo.

## Objetivo

Construir un dataset de imágenes de vías con daños etiquetados y entrenar un modelo de detección de objetos capaz de localizar y clasificar baches en imágenes.

## Fases

1. **Dataset**: recolección, etiquetado y publicación del dataset en Kaggle.
2. **Exploración (EDA)**: análisis de clases, tamaños y distribución de los daños.
3. **Modelo base**: *fine-tuning* de un modelo de detección preentrenado.
4. **Evaluación**: métricas (mAP, precisión, recall) y análisis de errores.
5. **Demo** (opcional): interfaz sencilla para probar el modelo con imágenes nuevas.

## Estructura

```
road-damage-detection/
├── data/              # datos locales (no se versionan; el dataset vive en Kaggle)
│   ├── raw/           # imágenes originales
│   └── processed/     # dataset final
├── notebooks/         # notebooks numerados por fase
├── pyproject.toml     # dependencias (gestionadas con uv)
└── README.md
```

## Configuración

El proyecto usa [uv](https://docs.astral.sh/uv/) para gestionar el entorno y las dependencias.

```bash
git clone https://github.com/Juanmelo73/road-damage-detection.git
cd road-damage-detection
uv sync
```

En VS Code, selecciona como kernel el intérprete de `.venv` para ejecutar los notebooks.

## Dataset

_Próximamente en Kaggle._

## Licencia

[MIT](LICENSE)
