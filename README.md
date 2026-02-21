# LLM Embeddings and Data Pipeline Implementation  

## Descripción del Proyecto

Este proyecto reproduce e implementa los componentes principales del Capítulo 2 del libro *Build a Large Language Model (From Scratch)* de Sebastian Raschka. El objetivo es comprender cómo se construye el pipeline de preparación de datos necesario para entrenar un modelo de lenguaje (LLM).  

En el notebook embeddings.ipynb se desarrolla paso a paso el proceso completo que permite transformar texto crudo en representaciones numéricas que pueden ser procesadas por una red neuronal. Esto incluye la tokenización, la construcción del vocabulario, el manejo de tokens desconocidos, la generación de datasets usando ventanas deslizantes (max_length y stride), y la implementación de embeddings de tokens y embeddings posicionales utilizando PyTorch.  

Además, se incluye un pequeño experimento donde se modifican los valores de max_length y stride para analizar cómo cambia el número de muestras generadas y por qué el uso de ventanas superpuestas (overlap) resulta beneficioso para tareas de predicción del siguiente token.

---

## Getting Started

Estas instrucciones permiten ejecutar el proyecto localmente y correr el notebook de principio a fin sin errores.  

El proyecto está implementado en Python utilizando PyTorch y tiktoken, y se ejecuta completamente dentro de un Jupyter Notebook embeddings

---

## Prerrequisitos

Se requiere tener instalado:

- Python 3.9 o superior  
- pip  
- Jupyter Notebook o VSCode  
- PyTorch  
- tiktoken  

Puedes verificar tu versión de Python con:

python --version

---

## Instalación

### 1. Crear un entorno virtual (recomendado)

python -m venv venv

Activarlo:
venv\Scripts\activate


---

### 2. Instalar las librerías necesarias

pip install torch  
pip install tiktoken   

---

### 3. Descargar los archivos necesarios


O clonar el repositorio completo:

git clone https://github.com/rasbt/LLMs-from-scratch.git  

---

### 4. Ejecutar el notebook

Iniciar Jupyter:

jupyter notebook  

Abrir:

embeddings.ipynb  

Al ejecutarlo correctamente se deben observar:

- Resultados de tokenización  
- Construcción del vocabulario  
- Muestras generadas por el dataset  
- Impresiones de formas (shapes) de los embeddings  
- Conteo de muestras al cambiar max_length y stride  

---

## Verificación y Pruebas

Se debe verificar que:
  
- La tokenización genera IDs consistentes.  
- El dataset produce pares (inputs, targets).  
- La capa de embeddings retorna tensores con forma (batch_size, max_length, embedding_dim).  
 
---

## Construido con

- Python  
- PyTorch (framework de redes neuronales)  
- tiktoken (tokenizador GPT-2)  
- Jupyter Notebook  