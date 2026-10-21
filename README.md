# TP Integrador — Bases de Datos

## Descripción

Proyecto integrador de la materia Bases de Datos. El proyecto utiliza Python para conectarse con tres sistemas de bases de datos:

- **MongoDB Atlas:** base de datos documental.
- **Redis Cloud:** almacén de datos en memoria.
- **Neo4j AuraDB:** base de datos orientada a grafos.

Las conexiones se configuran mediante variables de entorno para mantener las credenciales fuera del código fuente y facilitar la ejecución del proyecto en distintas computadoras.

## Requisitos previos

- Python 3 instalado.
- Git.
- Acceso a las instancias online de MongoDB Atlas, Redis Cloud y Neo4j AuraDB.
- Credenciales y direcciones de conexión válidas para las tres bases de datos.

## Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/Joa-Ceq/TP-BB.DD.git
cd TP-BB.DD
```

Reemplazá los valores de ejemplo por la URL y el nombre reales del repositorio.

### 2. Crear un entorno virtual

En Windows, desde Git Bash:

```bash
py -m venv .venv
source .venv/Scripts/activate
```

### 3. Instalar las dependencias

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 4. Configurar las variables de entorno

Crear un archivo `.env` en la raíz del proyecto con las siguientes variables:

```dotenv
# MongoDB Atlas
MONGODB_HOST=
MONGODB_USER=
MONGODB_PASSWORD=
MONGODB_DATABASE=
MONGODB_URI=

# Redis Cloud
REDIS_URL=

# Neo4j AuraDB
NEO4J_URI=
NEO4J_USER=
NEO4J_PASSWORD=
```

Completar las variables con los datos de conexión correspondientes. No utilizar los valores de ejemplo como credenciales reales.

El archivo `.env` contiene información privada y no debe subirse a GitHub.

### 5. Ejecutar el proyecto

Abrir el notebook `TP_Integrador_BD (2).ipynb` en Visual Studio Code, seleccionar el intérprete de Python del entorno virtual `.venv` y ejecutar las celdas en el orden indicado.

## Estructura del proyecto

```text
.
├── TP_Integrador_BD (2).ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── .env                 # Configuración local, no versionada
```

Esta estructura representa los archivos principales; puede ampliarse si el proyecto incorpora otros módulos o recursos.

## Seguridad

- No publicar contraseñas, URI privadas ni archivos que contengan credenciales.
- Mantener `.env` excluido mediante `.gitignore`.
- No compartir credenciales personales en el código fuente.
- Verificar que las instancias online permitan las conexiones desde la red utilizada.

## Tecnologías utilizadas

- Python
- MongoDB Atlas
- Redis Cloud
- Neo4j AuraDB
- Jupyter Notebook