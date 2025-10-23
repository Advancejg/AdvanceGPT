# AdvanceGPT - Plataforma de IA Avanzada

## 🚀 Descripción del Proyecto

AdvanceGPT es una plataforma de inteligencia artificial avanzada, profesional y modular que actúa como tu asistente personal 24/7. Diseñada para ejecutar tareas complejas, gestionar automatizaciones, aprender de tus interacciones y conectarse con tus cuentas y servicios favoritos.

## ✨ Características Principales

### 1. Chat Inteligente Multi-Modelo
- Integración con múltiples proveedores LLM (OpenAI, Google Gemini, Hugging Face, modelos locales)
- Selección dinámica del modelo según la tarea
- Contexto de conversación con memoria a largo plazo

### 2. Memoria Inteligente y Aprendizaje
- Sistema de memoria vectorial (ChromaDB/FAISS)
- Almacenamiento persistente de preferencias y contextos
- Aprendizaje continuo de patrones de usuario
- Recuperación de información relevante en conversaciones

### 3. Automatizaciones Avanzadas
- Workflows personalizables con n8n
- Integración con Google Drive, Gmail, redes sociales
- Ejecución programada de tareas
- Publicación automática de contenido
- Gestión de correos y archivos

### 4. Integraciones Reales
- **Google Workspace**: Drive, Gmail, Calendar
- **Redes Sociales**: Instagram, YouTube, Twitter/X
- **Servicios de IA**: OpenAI, Anthropic, Google AI
- **Almacenamiento**: S3, Cloudinary, local

### 5. Panel de Control Profesional
- Interfaz React moderna y responsive
- Dashboard con estadísticas y métricas
- Gestión de proyectos y tareas
- Visualización de logs y acciones
- PWA para uso en móvil y escritorio

### 6. Seguridad y Privacidad
- Autenticación OAuth2.0 segura
- Almacenamiento cifrado de credenciales
- Logs de auditoría profesionales
- Cumplimiento GDPR

## 📦 Estructura del Proyecto

```
AdvanceGPT/
├── backend/              # API Node.js/Fastify
│   ├── src/
│   │   ├── routes/        # Endpoints REST
│   │   ├── services/      # Lógica de negocio
│   │   ├── integrations/  # Conectores externos
│   │   ├── memory/        # Sistema de memoria
│   │   ├── automation/    # Workflows
│   │   └── utils/         # Utilidades
│   ├── config/
│   ├── package.json
│   └── Dockerfile
│
├── frontend/             # React PWA
│   ├── src/
│   │   ├── components/    # Componentes React
│   │   ├── pages/         # Páginas
│   │   ├── hooks/         # Custom hooks
│   │   ├── services/      # API calls
│   │   └── styles/        # Tailwind CSS
│   ├── public/
│   ├── package.json
│   └── vite.config.js
│
├── automation/           # Workflows n8n
│   ├── workflows/
│   └── templates/
│
├── docs/                 # Documentación
│   ├── setup/          # Guías de instalación
│   ├── api/            # Documentación API
│   └── tutorials/      # Tutoriales
│
├── docker-compose.yml
├── .env.example
└── README.md
```

## 🛠️ Stack Tecnológico

### Backend
- **Runtime**: Node.js 20+
- **Framework**: Fastify (alto rendimiento)
- **Base de Datos**: PostgreSQL + Redis
- **Memoria Vectorial**: ChromaDB / FAISS
- **Autenticación**: Passport.js (OAuth2.0)
- **Automatización**: n8n + Bull Queue

### Frontend
- **Framework**: React 18 + TypeScript
- **Build Tool**: Vite
- **Estilos**: Tailwind CSS
- **Estado**: Zustand
- **PWA**: Workbox
- **UI Components**: shadcn/ui

### DevOps
- **Contenedores**: Docker + Docker Compose
- **CI/CD**: GitHub Actions
- **Despliegue**: Vercel (frontend) + Railway (backend)
- **Monitoreo**: Sentry + Winston Logs

## 🚀 Instalación Rápida

### Requisitos Previos
- Node.js 20+ y npm/yarn
- Docker y Docker Compose (opcional)
- Cuenta de Google (para integraciones)
- API Keys de OpenAI/Gemini (opcional)

### Opción 1: Docker (Recomendado)

```bash
# Clonar el repositorio
git clone https://github.com/Advancejg/AdvanceGPT.git
cd AdvanceGPT

# Configurar variables de entorno
cp .env.example .env
# Editar .env con tus credenciales

# Levantar todos los servicios
docker-compose up -d

# Acceder a:
# - Frontend: http://localhost:3000
# - Backend API: http://localhost:8000
# - n8n: http://localhost:5678
```

### Opción 2: Instalación Manual

```bash
# Backend
cd backend
npm install
npm run dev

# Frontend (nueva terminal)
cd frontend
npm install
npm run dev
```

## 📚 Documentación Completa

Para más información detallada, consulta:

- [Guía de Instalación](docs/setup/installation.md)
- [Configuración de Integraciones](docs/setup/integrations.md)
- [Documentación de API](docs/api/README.md)
- [Tutoriales de Uso](docs/tutorials/README.md)
- [Desarrollo y Contribución](docs/CONTRIBUTING.md)

## 🎯 Casos de Uso

1. **Asistente Personal 24/7**
   - Gestión de correos y calendario
   - Recordatorios inteligentes
   - Resumen de información importante

2. **Automatización de Contenido**
   - Publicación automática en redes sociales
   - Generación de descripciones y hashtags
   - Procesamiento de vídeos y multimedia

3. **Gestión de Proyectos**
   - Seguimiento de tareas
   - Generación de informes
   - Coordinación de equipos

4. **Análisis y Reporting**
   - Extracción de datos de múltiples fuentes
   - Generación de informes personalizados
   - Visualización de métricas

## 🔐 Seguridad

- Todas las credenciales se almacenan cifradas
- OAuth2.0 para autenticación segura
- Tokens con expiración y renovación automática
- Logs de auditoría de todas las acciones
- Rate limiting y protección contra abusos

## 💰 Despliegue en Producción
### Vercel (Frontend)
```bash
vercel deploy
```

### Railway (Backend)
```bash
railway up
```

### VPS (Completo)
Ver [guía de despliegue VPS](docs/setup/vps-deployment.md)

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Licencia

MIT License - ver [LICENSE](LICENSE) para más detalles

## 👥 Autor

**Advancejg**
- GitHub: [@Advancejg](https://github.com/Advancejg)

## 🚀 Roadmap

- [x] Sistema de chat básico
- [x] Integración con múltiples LLMs
- [x] Memoria vectorial
- [ ] App móvil nativa (React Native)
- [ ] Integración con Telegram/WhatsApp
- [ ] Sistema de plugins
- [ ] Marketplace de automatizaciones
- [ ] Modo offline con modelos locales

## ❓ Soporte

Si tienes preguntas o necesitas ayuda:
- Abre un [Issue](https://github.com/Advancejg/AdvanceGPT/issues)
- Consulta la [documentación](docs/)
- Revisa las [FAQ](docs/FAQ.md)

---

**🌟 ¡Dale una estrella al proyecto si te resulta útil!**
