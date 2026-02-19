# 🛠️ Herramientas de IA por CLI - Guía Completa

## ¿Por qué CLI en lugar de Web?

| Aspecto | Web (ChatGPT, Claude.ai) | CLI (Claude Code, aider) |
|---------|--------------------------|--------------------------|
| **Acceso a archivos** | ❌ Copy-paste manual | ✅ Lee directo del disco |
| **Tamaño de contexto** | Limitado por ventana | Puede leer proyectos enteros |
| **Automatización** | ❌ No scripteable | ✅ Integrable en pipelines |
| **Edición de código** | Copy-paste de vuelta | ✅ Edita archivos directo |
| **Historial de Git** | ❌ Manual | ✅ Commits automáticos |
| **Privacidad** | Datos van a la nube | Algunas opciones locales |

---

## 🔍 Tabla Comparativa

| Herramienta | Proveedor | Precio | Ideal Para | Dificultad |
|-------------|-----------|--------|------------|------------|
| **Claude Code** | Anthropic | API ($) | Coding, editar archivos | ⭐ Fácil |
| **Gemini CLI** | Google | 🆓 ¡GRATIS! | Aprender, presupuesto bajo | ⭐ Fácil |
| **GitHub Copilot CLI** | GitHub | $10-19/mes | Comandos shell, Git | ⭐ Fácil |
| **aider** | Open Source | API ($) | Pair programming | ⭐⭐ Medio |
| **OpenClaw** | Open Source | API ($) | Automatización, integraciones | ⭐⭐ Medio |
| **Cursor** | Cursor Inc | $20/mes | Experiencia IDE completa | ⭐ Fácil |

---

## 1️⃣ Gemini CLI (Google) 🆓 ¡GRATIS!

### ¿Por qué Gemini?
- **Tier gratuito:** 15 requests/minuto, 1M tokens/día
- Perfecto para aprender sin gastar
- Calidad competitiva con GPT-4

### Cómo Empezar

```bash
# Obtener API key GRATIS en:
# https://aistudio.google.com/app/apikey

# Instalar aider
pip install aider-chat

# Configurar key
export GOOGLE_API_KEY="AIza..."

# Usar con Gemini (¡gratis!)
aider --model gemini/gemini-1.5-flash
```

### Precios
| Tier | Costo | Límites |
|------|-------|---------|
| Gratis | $0 | 15 req/min, 1M tokens/día |
| Pago | ~$0.075/1M tokens | Límites mayores |

---

## 2️⃣ Claude Code (Anthropic)

### Web vs CLI

| Claude.ai (Web) | Claude Code (CLI) |
|-----------------|-------------------|
| Interfaz de chat | Interfaz de terminal |
| Subir archivos uno por uno | Leer directorios enteros |
| Copy-paste código de vuelta | Edita archivos directo |
| Contexto limitado | Contexto extendido |
| Sin acceso a shell | Puede ejecutar comandos |

### Cómo Empezar

```bash
# Instalar
npm install -g @anthropic-ai/claude-code

# Configurar API key
export ANTHROPIC_API_KEY="sk-ant-..."

# Ejecutar
claude
```

### Precios
- Pago por token (uso de API)
- ~$3 por 1M tokens de entrada (Claude 3.5 Sonnet)
- ~$15 por 1M tokens de salida

---

## 3️⃣ aider (Open Source)

### ¿Qué lo Hace Especial?
- Aware de Git: hace commits automáticos
- Edición multi-archivo
- Funciona con CUALQUIER modelo (OpenAI, Anthropic, Gemini, local)

### Cómo Empezar

```bash
# Instalar
pip install aider-chat

# Usar con OpenAI
export OPENAI_API_KEY="sk-..."
aider

# Usar con Claude
export ANTHROPIC_API_KEY="sk-ant-..."
aider --model claude-3-5-sonnet-20241022

# Usar con Gemini (¡GRATIS!)
export GOOGLE_API_KEY="AIza..."
aider --model gemini/gemini-1.5-flash

# Especificar archivos a editar
aider app.py utils.py tests/
```

### Comandos Clave (dentro de aider)
```
/add archivo.py    # Agregar archivo al contexto
/drop archivo.py   # Quitar del contexto
/diff              # Ver cambios pendientes
/commit            # Commitear cambios
/undo              # Deshacer último cambio
/help              # Todos los comandos
```

---

## 4️⃣ GitHub Copilot CLI

### Qué Hace
- Sugiere comandos de shell desde lenguaje natural
- Explica comandos complejos
- Integrado con `gh` CLI

### Cómo Empezar

```bash
# Requiere suscripción a GitHub Copilot ($10/mes)

# Instalar extensión
gh extension install github/gh-copilot

# Sugerir un comando
gh copilot suggest "encontrar todos los archivos .log mayores a 100MB"

# Explicar un comando
gh copilot explain "tar -xzvf archivo.tar.gz"
```

---

## 5️⃣ OpenClaw (Gateway Auto-hospedado)

### ¿Qué lo Hace Especial?
- Conecta a WhatsApp, Telegram, Discord, Slack
- Memoria persistente entre sesiones
- Acceso completo al sistema (archivos, shell, browser)
- Corre 24/7 como servicio

### Cómo Empezar

```bash
# Instalar
npm install -g openclaw

# Asistente de configuración
openclaw onboard --install-daemon

# Abrir interfaz de chat
openclaw tui
```

---

## 🎯 Guía Rápida de Decisión

### "Quiero probar GRATIS"
→ **Gemini** con aider
```bash
pip install aider-chat
export GOOGLE_API_KEY="tu-key-gratis"
aider --model gemini/gemini-1.5-flash
```

### "Quiero la mejor calidad"
→ **Claude Code** o **aider con Claude**
```bash
npm install -g @anthropic-ai/claude-code
claude
```

### "Solo quiero ayuda con comandos de shell"
→ **GitHub Copilot CLI**
```bash
gh copilot suggest "tu tarea"
```

### "Quiero un asistente personal de IA"
→ **OpenClaw**
```bash
openclaw onboard --install-daemon
```

### "No quiero salir de mi IDE"
→ **Cursor** o **Continue**

---

## 💰 Comparación de Costos (Uso Típico)

| Herramienta | Uso Leve (1hr/día) | Uso Intenso (8hr/día) |
|-------------|--------------------|-----------------------|
| Gemini | 🆓 Gratis | 🆓 Gratis |
| Claude Code | ~$5-10/mes | ~$30-50/mes |
| aider + GPT-4 | ~$10-20/mes | ~$50-100/mes |
| GitHub Copilot | $10/mes fijo | $10/mes fijo |
| Cursor | $20/mes fijo | $20/mes fijo |

---

## 📚 Recursos

| Herramienta | Documentación | API Keys |
|-------------|---------------|----------|
| Gemini | ai.google.dev | aistudio.google.com/app/apikey |
| Claude Code | anthropic.com/claude-code | console.anthropic.com |
| aider | aider.chat | (usa otros proveedores) |
| Copilot CLI | docs.github.com/copilot | github.com/settings/copilot |
| OpenClaw | docs.openclaw.ai | (usa otros proveedores) |

---

*Workshop por Juan Torres - Atenea Conocimientos 2026*
