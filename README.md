<div align="center">

![Estud-IA Logo](../Estud-IA_Logo.png)

# **Campus Estud-IA**

# Ejercicio #2 Segmentación de Clientes - Machine Learning No Supervisado

### Proyecto de la Universidad Estud-IA
**Ejercicio #2 - Clustering No Supervisado**

</div>

## 📋 Tabla de Contenidos
1. [Descripción del Proyecto](#descripción-del-proyecto)
2. [¿Qué se quiere conseguir?](#qué-se-quiere-conseguir)
3. [Requisitos Previos](#requisitos-previos)
4. [Configuración del Entorno Virtual](#configuración-del-entorno-virtual)
5. [Instalación de Dependencias](#instalación-de-dependencias)
6. [Cómo ejecutar el Proyecto](#cómo-ejecutar-el-proyecto)
7. [Entendiendo el Código](#entendiendo-el-código)

---

## 📚 Descripción del Proyecto

Este proyecto implementa un **modelo de Machine Learning no supervisado usando clustering K-means** para segmentación de clientes.

El objetivo es **agrupar clientes en diferentes segmentos** basándose en su comportamiento de compra como:
- Gasto mensual promedio
- Frecuencia de compras
- Antigüedad como cliente
- Recencia de la última compra

---

## 🎯 ¿Qué se quiere conseguir?

Este proyecto cumple con los siguientes objetivos educativos:

✅ **Aprender Clustering**: Entender cómo funcionan los algoritmos no supervisados

✅ **Generación de datos sintéticos**: Crear datos realistas de clientes

✅ **Preprocesamiento**: Escalar y preparar datos para clustering

✅ **Optimización de clusters**: Encontrar el número óptimo de grupos

✅ **Visualización**: Crear gráficos para entender los clusters

✅ **Análisis de segmentos**: Interpretar y nombrar los grupos de clientes

✅ **Predicción**: Asignar nuevos clientes a segmentos existentes

---

## 🔧 Requisitos Previos

Antes de comenzar, necesitas tener instalado en tu computadora:

### Python
- **Python 3.8 o superior**
- Puedes descargarlo desde: https://www.python.org/downloads/

**¿Cómo verificar si tienes Python?**
```bash
python --version
```

Si ves algo como `Python 3.10.5`, significa que ya tienes Python instalado.

---

## 🚀 Configuración del Entorno Virtual

Un **entorno virtual** es como una carpeta especial que guarda todas las librerías de tu proyecto, separadas del resto de tu computadora. Esto es muy importante para no contaminar tu sistema.

### Paso 1: Abre la terminal/CMD

**En Windows:**
- Presiona `Win + R`
- Escribe `cmd` y presiona Enter

**En Mac/Linux:**
- Abre la Terminal (busca en Aplicaciones)

### Paso 2: Navega a la carpeta del proyecto

```bash
cd ruta/a/tu/proyecto
```

Por ejemplo:
```bash
cd /home/mendozalz/Escritorio/StudiaIA/Stud-IA-Developer/Clustering
```

### Paso 3: Crea el entorno virtual

**En Windows:**
```bash
python -m venv venv
```

**En Mac/Linux:**
```bash
python3 -m venv venv
```

Este comando crea una carpeta llamada `venv` (es como un "mini Python" solo para tu proyecto).

### Paso 4: Activa el entorno virtual

**En Windows:**
```bash
venv\Scripts\activate
```

**En Mac/Linux:**
```bash
source venv/bin/activate
```

**¿Funcionó?** Si ves algo como esto en tu terminal, significa que los pasos anteriores fueron correctos:
```bash
(venv) $
```

Nota que ahora tu terminal muestra `(venv)` al inicio. Eso significa que estás dentro del entorno virtual.

---

## 📦 Instalación de Dependencias

Las **dependencias** son librerías externas (código escrito por otros colaboradores) que nuestro proyecto necesita para funcionar.

### Paso 1: Asegúrate de tener el archivo `requirements.txt`

El archivo `requirements.txt` debe estar en la carpeta de tu proyecto junto a `app.py`.

### Paso 2: Instala todas las dependencias

Con el entorno virtual activado (recuerda que debe mostrar `(venv)` en tu terminal), ejecuta:

```bash
pip install -r requirements.txt
```

### ¿Qué hace este comando?

- `pip` = el gestor de paquetes de Python (es como un "instalador" de librerías)
- `install` = instalar
- `-r requirements.txt` = lee el archivo requirements.txt y instala todo lo que dice

**Espera un momento** mientras todas las librerías se descargan e instalan. Verás algo como:
```
Successfully installed numpy-1.24.0 pandas-2.0.0 ...
```

### Actualizar una dependencia (opcional)

Si en el futuro necesitas actualizar una librería específica:

```bash
pip install --upgrade nombre_libreria
```

Por ejemplo:
```bash
pip install --upgrade pandas
```

---

## ▶️ Cómo ejecutar el Proyecto

### Paso 1: Asegúrate de estar en el entorno virtual

Tu terminal debe mostrar `(venv)` al inicio:
```bash
(venv) $
```

### Paso 2: Ejecuta el archivo principal

```bash
python app.py
```

### ¿Qué pasará?

El programa hará esto automáticamente:

1. � **Genera datos sintéticos** - Crea 300 clientes con características realistas
2. � **Visualiza datos originales** - Muestra gráficos para entender la distribución
3. 🔧 **Preprocesa datos** - Escala las características para el clustering
4. 🎯 **Encuentra clusters óptimos** - Usa métodos del codo, silhouette y Davies-Bouldin
5. 🏗️ **Construye modelo K-means** - Entrena el clustering con el número óptimo de grupos
6. 📈 **Visualiza clusters** - Muestra los grupos formados con PCA
7. 🏷️ **Analiza segmentos** - Interpreta y nombra cada tipo de cliente
8. 🔮 **Predice nuevos clientes** - Asigna clientes nuevos a los segmentos existentes

Deberías ver algo como:
```
============================================================
👥 DEMOSTRACIÓN: CLUSTERING NO SUPERVISADO - CLIENTES
============================================================
👥 Generando datos sintéticos de clientes...
✅ Datos generados: 300 clientes, 4 características

📋 Características:
   Gasto_Mensual
   Frecuencia_Compra
   Antiguedad_Meses
   Recencia_Dias

📈 Estadísticas descriptivas:
       Gasto_Mensual  Frecuencia_Compra  Antiguedad_Meses  Recencia_Dias
count    300.000000         300.000000        300.000000   300.000000
mean      45.123456           6.678904          7.654321     7.321098
std       24.567890           5.432109          4.876543     3.210987
...
🎯 Número óptimo de clusters: 3
📊 Silhouette score máximo: 0.6543
✅ Demostración completada
🎯 Se encontraron 3 clusters de clientes
```

---

## 💡 Entendiendo el Código

### Estructura del Proyecto

```
Clustering/
│
├── app.py                  # Archivo principal (código del segmentador)
├── requirements.txt        # Lista de dependencias
└── README.md              # Este archivo (instrucciones)
```

### Las Librerías Explicadas

| Librería | Para qué sirve |
|----------|---|
| **numpy** | Trabajo con números y arrays (listas de números) |
| **pandas** | Manejo de datos en tablas (como Excel en Python) |
| **matplotlib** | Crear gráficos y visualizaciones |
| **seaborn** | Gráficos más bonitos y complejos que matplotlib |
| **scikit-learn** | Algoritmos de clustering y métricas de evaluación |
| **plotly** | Gráficos interactivos para visualización avanzada |
| **jupyter** | Soporte para notebooks de desarrollo |

### Flujo del Programa

```
1. Generar datos sintéticos de clientes (300 clientes)
           ↓
2. Visualizar datos originales (distribución y relaciones)
           ↓
3. Preprocesar datos (escalar características)
           ↓
4. Encontrar número óptimo de clusters (codo, silhouette, Davies-Bouldin)
           ↓
5. Construir y entrenar modelo K-means
           ↓
6. Visualizar clusters (PCA 2D y características originales)
           ↓
7. Analizar y nombrar segmentos de clientes
           ↓
8. Predecir clusters para nuevos clientes
```

---

## 🆘 Solución de Problemas

### Problema: "Python no se reconoce"

**Solución:** Python no está en el PATH de tu sistema. Reinstálalo asegurándote de marcar la opción "Add Python to PATH".

### Problema: "No existe el archivo requirements.txt"

**Solución:** Asegúrate de que el archivo `requirements.txt` está en la misma carpeta que `app.py`.

### Problema: "ModuleNotFoundError: No module named 'sklearn'"

**Solución:** Las dependencias no se instalaron correctamente. Intenta:
```bash
pip install scikit-learn pandas numpy matplotlib seaborn
```

### Problema: "No puedo activar el entorno virtual"

**Solución:** Verifica que estés en la carpeta correcta del proyecto y usa el comando correcto para tu sistema operativo.

---

## 📖 Recursos Adicionales

- [Documentación oficial de scikit-learn - Clustering](https://scikit-learn.org/stable/modules/clustering.html)
- [Documentación de pandas](https://pandas.pydata.org/)
- [Tutorial de K-means](https://www.datacamp.com/tutorial/k-means-clustering-python)
- [Segmentación de clientes con Python](https://towardsdatascience.com/customer-segmentation-using-k-means-clustering-d5cba4188e6c)
- [Métricas de evaluación de clustering](https://scikit-learn.org/stable/modules/clustering.html#clustering-evaluation)

---

## 📝 Lo que Aprendiste

Después de completar este proyecto, ahora sabes:

✅ Cómo crear datos sintéticos realistas
✅ Cómo preprocesar datos para clustering
✅ Cómo encontrar el número óptimo de clusters
✅ Cómo implementar el algoritmo K-means
✅ Cómo evaluar la calidad de los clusters
✅ Cómo visualizar clusters en 2D con PCA
✅ Cómo interpretar y nombrar segmentos
✅ Cómo asignar nuevos datos a clusters existentes

¡Felicidades! 🎉 Ya has completado tu primer proyecto de clustering no supervisado.

---

**Última actualización:** 19 de febrero de 2026