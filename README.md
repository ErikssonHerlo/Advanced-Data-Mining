# Minería de Datos Avanzada

Este repositorio corresponde al curso de **Minería de Datos Avanzada** y está organizado como un **monorepo académico**, en el cual se incluirán todas las tareas, notebooks, datasets, resultados y documentos entregables desarrollados durante el curso.

La finalidad de este repositorio es mantener una estructura ordenada y reutilizable, utilizando un solo entorno virtual de Python (`.venv`) para ejecutar todas las actividades del curso sin tener que crear un ambiente diferente por cada tarea.

---

## Estructura del repositorio

La estructura sugerida del proyecto es la siguiente:

```text
Advanced-Data-Mining/
├── .venv/
├── .gitignore
├── README.md
├── requirements.txt
├── Tarea_02/
│   ├── data/
│   │   └── dataset_diabetes.csv
│   ├── notebooks/
│   │   └── clasificacion_diabetes.ipynb
│   └── outputs/
│       ├── resultados.csv
│       └── reporte.pdf
├── Tarea_02/
│   ├── data/
│   ├── notebooks/
│   └── outputs/
└── Tarea_03/
    ├── data/
    ├── notebooks/
    └── outputs/
````

Cada carpeta de tarea puede contener:

* `data/`: datasets utilizados en la actividad.
* `notebooks/`: notebooks desarrollados en clase o modificados para la entrega.
* `outputs/`: resultados generados, tablas, gráficas, reportes o archivos finales.

---

## Creación del entorno virtual

Desde la raíz del repositorio, crear el entorno virtual con:

```bash
python3 -m venv .venv
```

Esto generará una carpeta llamada `.venv`, la cual será utilizada por todas las tareas del curso.

---

## Activación del entorno virtual

En Linux o macOS:

```bash
source .venv/bin/activate
```

En Windows:

```bash
.venv\Scripts\activate
```

Cuando el entorno esté activo, debería aparecer algo similar a esto en la terminal:

```bash
(.venv)
```

---

## Instalación de dependencias

Una vez activado el entorno virtual, instalar las dependencias con:

```bash
pip install -r requirements.txt
```

El archivo `requirements.txt` debe contener las librerías necesarias para ejecutar los notebooks del curso, por ejemplo:

```txt
pandas
numpy
matplotlib
scikit-learn
jupyter
ipykernel
tensorflow
keras
```

---

## Registrar el entorno como kernel de Jupyter

Para que los notebooks puedan utilizar el entorno virtual, se debe registrar como kernel de Jupyter:

```bash
python -m ipykernel install --user --name Advanced-Data-Mining --display-name "Minería de Datos Avanzada"
```

Luego, dentro de Jupyter Notebook o JupyterLab, seleccionar el kernel:

```text
Minería de Datos Avanzada
```

---

## Ejecución de notebooks

Para abrir Jupyter Notebook:

```bash
jupyter notebook
```

O, si se utiliza JupyterLab:

```bash
jupyter lab
```

Luego se debe navegar a la carpeta correspondiente de la tarea y ejecutar el notebook deseado.

Ejemplo:

```text
tarea_01_diabetes/notebooks/clasificacion_diabetes.ipynb
```

---

## Uso del mismo `.venv` para todas las tareas

Todas las tareas del curso utilizarán el mismo entorno virtual ubicado en la raíz del repositorio:

```text
Advanced-Data-Mining/.venv
```

Esto evita duplicar dependencias y facilita la administración del proyecto.

Cuando una nueva tarea requiera una librería adicional, se debe instalar dentro del mismo entorno:

```bash
pip install nombre_libreria
```

Después, actualizar el archivo `requirements.txt` con:

```bash
pip freeze > requirements.txt
```

De esta forma, cualquier persona podrá replicar el entorno de trabajo instalando las mismas dependencias.

---

## Archivos que no deben subirse al repositorio

Se recomienda excluir del repositorio archivos temporales, entornos virtuales y salidas generadas automáticamente.

Ejemplo de `.gitignore`:

```gitignore
# Entorno virtual
.venv/

# Caché de Python
__pycache__/
*.pyc

# Jupyter
.ipynb_checkpoints/

# Archivos temporales
.DS_Store

# Salidas generadas
outputs/

# Datasets pesados o privados
*.csv
*.xlsx
*.zip
```

Si algún dataset debe incluirse como parte de la entrega, puede colocarse dentro de la carpeta `data/` de la tarea correspondiente.

---

## Replicación del proyecto

Para replicar este repositorio en otra computadora, seguir estos pasos:

1. Clonar el repositorio:

```bash
git clone <url-del-repositorio>
```

2. Entrar a la carpeta del proyecto:

```bash
cd Advanced-Data-Mining
```

3. Crear el entorno virtual:

```bash
python3 -m venv .venv
```

4. Activar el entorno virtual:

```bash
source .venv/bin/activate
```

5. Instalar dependencias:

```bash
pip install -r requirements.txt
```

6. Registrar el kernel de Jupyter:

```bash
python -m ipykernel install --user --name Advanced-Data-Mining --display-name "Minería de Datos Avanzada"
```

7. Ejecutar Jupyter:

```bash
jupyter notebook
```

---

## Convención para nuevas tareas

Cada nueva tarea debe agregarse en una carpeta independiente siguiendo una numeración ordenada:

```text
tarea_01_diabetes/
tarea_02_clustering/
tarea_03_regresion/
tarea_04_redes_neuronales/
```

Esto permite mantener el repositorio limpio, organizado y fácil de consultar.

---

## Autor

Estudiante: **Ing. Eriksson Hernandez**

Curso: **Minería de Datos Avanzada**

