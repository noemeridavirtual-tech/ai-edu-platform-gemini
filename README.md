# AI Education Platform - Plataforma Educativa Inteligente

[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104-green.svg)](https://fastapi.tiangolo.com/)
[![Google Gemini AI](https://img.shields.io/badge/Google_Gemini-API-red.svg)](https://ai.google.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Descripción

AI Education Platform es una plataforma educativa avanzada construida con **Google Gemini AI** y **FastAPI**, diseñada específicamente para educadores de méxico. Esta herramienta revoluciona la enseñanza primaria mediante:

- **Generación Inteligente de Contenido**: Crea material educativo personalizado automáticamente
- **Gamificación**: Transforma el aprendizaje en experiencias interactivas y divertidas
- **Análisis de Aprendizaje**: Monitorea el progreso de cada estudiante en tiempo real
- **Soporte Multilingüe**: Funciona completamente en español mexicano

## Características Principales

### 🔬 Generación de Contenido
- Genera explicaciones claras y adaptadas al nivel de comprensión
- Crea ejemplos prácticos contextualizados
- Produce ejercicios personalizados
- Generapreguntas de evaluación

### 🎮 Gamificación
- Sistema de puntos y logros
- Desafíos educativos progresivos
- Competencias entre estudiantes
- Recompensas y reconocimientos

### 📊 Análisis de Datos
- Seguimiento del progreso estudiantil
- Identificación de áreas de mejora
- Reportes detallados por estudiante
- Estadísticas de desempeño

## Requisitos Previos

- Python 3.9 o superior
- pip (administrador de paquetes de Python)
- Cuenta de Google Cloud con acceso a Gemini API
- Git para control de versiones

## Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/noemeridavirtual-tech/ai-edu-platform-gemini.git
cd ai-edu-platform-gemini
```

### 2. Crear ambiente virtual

```bash
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 4. Configurar variables de entorno

```bash
cp .env.example .env
```

Edita el archivo `.env` y agrega tus credenciales:

```env
GEMINI_API_KEY=tu_clave_api_aqui
GEMINI_MODEL=gemini-2.0-flash-exp
PLATFORM_ENV=development
```

## Uso

### Iniciar el servidor

```bash
python app/main.py
```

La aplicación estará disponible en `http://localhost:8000`

### Endpoints Disponibles

#### Generar Contenido Educativo

```bash
curl -X POST "http://localhost:8000/generate-content" \
  -H "Content-Type: application/json" \
  -d '{
    "topic": "Fracciones",
    "level": "primaria",
    "language": "es"
  }'
```

#### Generar Quiz

```bash
curl -X POST "http://localhost:8000/generate-quiz" \
  -H "Content-Type: application/json" \
  -d '{
    "topic": "Sumas y Restas",
    "num_questions": 5,
    "difficulty": "medium"
  }'
```

## Estructura del Proyecto

```
ai-edu-platform-gemini/
├── app/
│   ├── main.py              # Aplicación principal FastAPI
│   ├── models/              # Modelos de datos
│   ├── routers/             # Rutas de API
│   ├── services/            # Lógica de negocios
│   ├── schemas/             # Esquemas Pydantic
│   ├── utils/               # Utilidades generales
│   ├── config.py            # Configuración de la app
│   ├── database.py          # Conexión a base de datos
└── requirements.txt       # Dependencias del proyecto
└── .env.example           # Variables de entorno ejemplo
└── README.md              # Este archivo
```

## Documentación de API

Una vez que el servidor está en ejecución, accede a la documentación interactiva:

- **Swagger UI**: http://localhost:8000/docs
- **ReDoc**: http://localhost:8000/redoc

## Deployment

### Google Cloud Run

Ver `Dockerfile` para instrucciones de deployement en Google Cloud Run.

## Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo LICENSE para detalles.

## Soporte

Para soporte, contacta a: noemeridavirtual@gmail.com

## Autor

**Noe Merída** - Educador y Desarrollador
- GitHub: [@noemeridavirtual-tech](https://github.com/noemeridavirtual-tech)
- Twitter: [@noemeridavirtual](https://twitter.com/noemeridavirtual)

---

**Hecho con ❤️ para los educadores de México**
