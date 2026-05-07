<img width="11520" height="3456" alt="Banner Proyectos" src="https://github.com/user-attachments/assets/407d4b1a-84ae-415a-b874-95f3d3558075" />

# 📊 Proyecto - Automatización MySQL → Python → Excel

## 📝 Descripción del proyecto

Este proyecto automatiza la extracción y análisis de datos de la base de datos SQL usando Python, generando varios archivos CSV que se conectan automáticamente a un libro de Excel. 

**Enfoque híbrido:** Automatización del flujo y carga de datos + diseño manual en Excel. La actualización de datos es automática, pero conservas total libertad creativa para el diseño del dashboard.

## 🎯 Objetivos concretos

- Automatizar la extracción de datos desde MySQL hacia Excel
- Generar 3 o más datasets en formato CSV pre-procesados para análisis
- Crear un flujo de trabajo simple: Python genera → Excel visualiza
- Documentar y estructurar el proyecto para fácil mantenimiento

## 🗄️ Base de datos utilizada

Para este proyecto, trabajaremos con la base de datos Sakila, una base de datos de ejemplo que simula el sistema de una tienda de alquiler de películas. 

- **Base de datos**: Sakila (MySQL)
- **Contenido**: Datos de clientes, direcciones, países, ciudades, alquileres y pagos.
- El estudiante podrá utilizar otra base de datos que prefiera 

## 📊 Análisis objetivo

Para el caso de la base de datos Sakila, el proyecto se enfocará en analizar:

- Comportamiento de clientes y patrones de consumo
- Distribución geográfica de ingresos (países y ciudades)
- Tendencias temporales de alquileres y pagos
- Identificación de clientes VIP y mercados clave

## 🧰 Tecnologías

- **Python** 
- **Base de datos**: MySQL
- **Librerías principales**:
  - `pandas` - Manipulación y análisis de datos
  - `sqlalchemy` - Conexión a base de datos
  - `mysql-connector-python` - Driver MySQL
  - `openpyxl` - Generación y manipulación de archivos Excel
  - `python-dotenv` - Gestión de variables de entorno
- **Excel** - Diseño de dashboards y visualizaciones
- **Control de versiones**: Git & github

## 📦 Condiciones de entrega

**El proyecto es en grupos.**

- Repositorio en Github
- Archivo Excel con conexion a Datos, Tablas dinámicas, y un Dashboard
- **Documentación completa**:
  - README con instrucciones de instalación y uso
  - Documentación del proceso de automatización completo

## ⏳ Plazo de Entrega

**1 semana**

## 🏗️ Estructura del proyecto

```
proyecto-sakila-automation/
│
├── main.py                    ⭐ EJECUTAR ESTE (punto de entrada)
│
├── src/                       📦 Código fuente (procesamiento)
│   ├── __init__.py
│   ├── sakila_ETL.py         (extracción y transformación de datos)
│   └── config.py              (configuración desde .env)
│
├── queries/                   📜 Consultas SQL organizadas
│   ├── Clientes_sakila.sql
│   ├── movies.sql
│   ├── casting.sql
│   └── top_peliculas.sql
│
├── output/                    📂 Datos procesados (CSVs)
│   ├── Clientes_sakila.csv    (desde queries)
│   ├── movies.csv             (desde queries)
│   ├── casting.csv            (desde queries)
│   ├── top_peliculas.csv      (desde queries)
│
├── dashboard/                 📊 Visualización (Excel)
│   ├── README.md              (guía del dashboard)
│   └── Sakila_Dashboard.xlsx  
│
├── .venv/                     🐍 Entorno virtual Python (ignorado por Git)
│
├── requirements.txt           (dependencias Python)
├── .env                       🔒 Credenciales (configurado ✓)
├── .env.example               (plantilla)
├── .gitignore                 (protección Git)
└── README.md                  (guía principal del proyecto)
```

**Organización clara:**
- **src/** = Procesamiento automatizado (Python)
- **output/** = CSVs con datos de pre-procesados
- **dashboard/** = Documento xlsx de visualización final (Excel)

**🔒 IMPORTANTE:** El archivo `.env` contiene tus credenciales y NO se sube a Git (está en `.gitignore`)

## ✅ Checklist de desarrollo

### Configuración inicial

- [ ] Instalar y configurar MySQL con base de datos Sakila
- [ ] Crear entorno virtual de Python
- [ ] Instalar dependencias del proyecto
- [ ] Configurar variables de entorno para conexión DB

### Desarrollo del pipeline de datos

- [ ] Implementar conexión a base de datos
- [ ] Crear consultas SQL optimizadas para extracción de datos
- [ ] Implementar generación de dataset
- [ ] Crear sistema de exportación automática

### Integración con Excel

- [ ] Desarrollar generador automático de archivos CSV estructurados
- [ ] Implementar formateo de datos compatible con Excel
- [ ] Crear estructura de datos para dashboard
- [ ] Agregar manejo de archivos y rutas
- [ ] Documentar proceso de conexión Excel-CSV

### Automatización y calidad

- [ ] Crear script principal de ejecución (main.py)
- [ ] Implementar manejo de errores

## 🧪 Criterios de evaluación
- Configurar y automatizar su entorno de trabajo.
- Gestionar equipos técnicos
- Evaluar Conjuntos de datos
- Desarrollar interfaces dinámicas
