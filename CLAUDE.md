# CLAUDE.md

## Proyecto

- **Nombre:** road-damage-detection (detección de daños en vías).
- **Objetivo:** construir un dataset propio de imágenes de vías con baches/daños etiquetados y entrenar un modelo de visión computacional que los detecte y clasifique.
- **Repo:** github.com/Juanmelo73/road-damage-detection (público, licencia MIT).
- Proyecto de portafolio, sin producto final obligatorio. Debe ser completo pero no complejo: hay poco tiempo.

## Enfoque de desarrollo

- Notebooks como columna vertebral, numerados por fase en `notebooks/`.
- `src/` solo se crea cuando una función se repite entre notebooks.
- Las carpetas se agregan a medida que el proyecto avanza, no por adelantado.
- Datos y pesos de modelos **no** se versionan en git (dataset en Kaggle; modelos en Kaggle/Hugging Face).

### Fases

1. **Dataset:** imágenes propias (pocas, en Google Drive) + posiblemente un dataset público (RDD2022 u otro de baches; revisar licencia). Definir clases, etiquetar, dividir train/val/test y publicar en Kaggle con la cuenta del usuario para accederlo vía código.
2. **EDA.**
3. **Modelo base:** fine-tuning de un detector preentrenado (candidato: YOLO de Ultralytics), entrenando en Kaggle o Colab con GPU.
4. **Evaluación:** mAP, precisión, recall por clase, matriz de confusión y análisis de errores (prioridad: imágenes locales de Cali).
5. **Demo (opcional):** Gradio o Streamlit, posiblemente en Hugging Face Spaces.

## Estado actual

- Estructura: `data/raw`, `data/processed`, `notebooks/` (vacías con `.gitkeep`), `README.md`, `LICENSE`, `.gitignore`, `pyproject.toml`, `uv.lock`, `.python-version`.
- Python 3.13.
- **Siguiente paso:** Fase 1 (construcción del dataset). Pendiente: contar las imágenes disponibles en Drive y definir las clases.
- Dependencias: numpy, pandas, matplotlib, pillow; ipykernel en el grupo dev. Regeneradas con `uv add` / `uv add --dev` (versiones estables más recientes a la fecha).

## Herramientas y convenciones

- Editor: VS Code. Gestión de entorno y paquetes: uv.
- Dependencias **siempre** con `uv add` / `uv remove` (`uv add --dev` para desarrollo). Nunca escribir versiones a mano en `pyproject.toml`.
- Para cambiar de rama en git usar `git switch`, nunca `git checkout`.
- Mensajes de commit en inglés.

## Forma de trabajo

- El proyecto lo llevan el usuario (Juan), Claude Code y Claude (chat).
- No agregar archivos, carpetas, dependencias ni configuraciones que el usuario no haya pedido explícitamente. Ante la duda, preguntar primero.
- No inventar datos, versiones ni resultados; verificar antes de afirmar.
- Mantener este CLAUDE.md actualizado cuando cambie el estado del proyecto o se tome una decisión importante.
