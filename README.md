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

## 🔗 Este proyecto continúa el Proyecto III

En el Proyecto III vuestro equipo extrajo un dataset analítico de Olist **a mano**: escribisteis la consulta, la ejecutasteis una vez y exportasteis un CSV.

Aquí convertís eso en un **proceso que se ejecuta solo**. Misma base, mismos equipos, mismo grano — pero ahora es código que cualquiera puede correr y obtener datos frescos.

De vuestra entrega del Proyecto III necesitáis tres cosas:

| Lo que traéis de P3 | Para qué sirve aquí |
| :--- | :--- |
| **El grano declarado** | El ETL debe respetarlo en cada ejecución |
| **La consulta SQL final** | Es el punto de partida de `queries/` |
| **Los KPIs definidos** | Son las tablas dinámicas del dashboard |

## 🗄️ Base de datos utilizada

- **Base de datos**: **Olist** (MySQL), la misma del Proyecto III
- **Contenido**: 99.441 pedidos reales de un marketplace brasileño (2016-2018): clientes, pedidos, artículos, pagos, reseñas, productos, vendedores y geolocalización
- **Instalación**: si aún no la tenéis cargada, el volcado está en la [carpeta de formación en Drive](https://drive.google.com/drive/folders/1apSXjn6eQ5o9RdutbD4skSjvH6ytvR06?usp=sharing) (`olist.sql.gz`)

> [!NOTE]
> Como siempre, el equipo puede traer **otra base de datos** si tiene una idea mejor. Pero entonces tiene que arrastrarla también al Proyecto V, porque los tres están encadenados.

## 📊 Análisis objetivo

Para la base de datos Olist, el proyecto se enfocará en analizar:

- Comportamiento de clientes y patrones de compra
- Distribución geográfica de ingresos (estados y ciudades de Brasil)
- Tendencias temporales de pedidos, pagos y tiempos de entrega
- Identificación de vendedores y categorías clave

> [!WARNING]
> Recordad la trampa del grano del Proyecto III: un `JOIN` de `orders` con `order_items`, `order_payments` y `order_reviews` sin agregar antes infla la facturación un **26%**. En un ETL automatizado ese error se repite en **cada ejecución** y nadie lo revisa. Aquí es donde más caro sale.

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

## 👥 Equipos

**Equipos de 3 o 4 personas**, los mismos que en el Proyecto III y que seguiréis en el Proyecto V.

## 📦 Condiciones de entrega

- Repositorio en Github
- Archivo Excel con conexion a Datos, Tablas dinámicas, y un Dashboard
- **Documentación completa**:
  - README con instrucciones de instalación y uso
  - Documentación del proceso de automatización completo

## ⏳ Plazo de Entrega

**1 semana**

## 🏗️ Estructura del proyecto

```
proyecto-olist-automation/
│
├── main.py                    ⭐ EJECUTAR ESTE (punto de entrada)
│
├── src/                       📦 Código fuente (procesamiento)
│   ├── __init__.py
│   ├── olist_ETL.py          (extracción y transformación de datos)
│   └── config.py              (configuración desde .env)
│
├── queries/                   📜 Consultas SQL organizadas
│   ├── clientes_actividad.sql
│   ├── catalogo_productos.sql
│   ├── vendedores.sql
│   └── entregas_retrasos.sql
│
├── output/                    📂 Datos procesados (CSVs)
│   ├── clientes_actividad.csv (desde queries)
│   ├── catalogo_productos.csv (desde queries)
│   ├── vendedores.csv         (desde queries)
│   ├── entregas_retrasos.csv  (desde queries)
│
├── dashboard/                 📊 Visualización (Excel)
│   ├── README.md              (guía del dashboard)
│   └── Olist_Dashboard.xlsx   
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

- [ ] Instalar y configurar MySQL con la base de datos Olist
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

## 🔜 Qué pasa al Proyecto V

Los CSV que genere vuestro ETL son la fuente del **Proyecto V (Power BI)**. Allí rehacéis este mismo dashboard con una herramienta profesional: modelo en estrella, medidas DAX e interactividad real.

Merece la pena que mientras montáis el Excel anotéis **qué querríais hacer y no podéis**. Esa lista es el guion del siguiente proyecto.

## 🧪 Criterios de evaluación
- Configurar y automatizar su entorno de trabajo.
- Gestionar equipos técnicos
- Evaluar Conjuntos de datos
- Desarrollar interfaces dinámicas
