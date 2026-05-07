---
theme: seriph
title: El stack del desarrollador web moderno
titleTemplate: '%s · WordPress Sevilla'
author: Said
keywords: ia, stack, agentes, calidad, seguridad, wordpress
colorSchema: dark
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
transition: slide-left
mdc: true
fonts:
  sans: Inter
  mono: Fira Code
---

# El stack del desarrollador web moderno

### con IA incluida

<div class="pt-12 text-gray-400">
  Comunidad WordPress Sevilla · 2026
</div>

---
layout: quote
---

# "Una herramienta sola no es un flujo de trabajo."

---
layout: two-cols
class: items-center
---

<div class="text-center pr-8">
  <img src="https://github.com/SaidElBakkali.png" class="rounded-full w-48 h-48 mx-auto border-4 border-blue-500" />
  <div class="text-2xl font-bold pt-6">Said El Bakkali</div>
  <div class="text-gray-400 pt-2">Desarrollador web · Sevilla</div>
  <div class="text-sm text-blue-400 pt-1">Miembro de la comunidad desde hace más de una década</div>
</div>

::right::

<div class="pl-8 space-y-5 pt-4">
  <div class="flex items-center gap-3">
    <div class="i-mdi-web text-2xl text-blue-400" />
    <a href="https://saidelbakkali.com" class="text-blue-400 hover:underline">saidelbakkali.com</a>
  </div>
  <div class="flex items-center gap-3">
    <div class="i-mdi-linkedin text-2xl text-blue-500" />
    <a href="https://www.linkedin.com/in/saidelbakkali/" class="text-blue-400 hover:underline">linkedin.com/in/saidelbakkali</a>
  </div>
  <div class="flex items-center gap-3">
    <div class="i-mdi-github text-2xl text-white" />
    <a href="https://github.com/SaidElBakkali" class="text-blue-400 hover:underline">github.com/SaidElBakkali</a>
  </div>
  <div class="flex items-center gap-3">
    <div class="i-mdi-wordpress text-2xl text-blue-400" />
    <a href="https://profiles.wordpress.org/sa3idho/" class="text-blue-400 hover:underline">wordpress.org/sa3idho</a>
  </div>
  <div class="flex items-center gap-3">
    <div class="i-mdi-email text-2xl text-gray-300" />
    <a href="mailto:contact@saidelbakkali.com" class="text-blue-400 hover:underline">contact@saidelbakkali.com</a>
  </div>
</div>

---
layout: center
---

# ¿Quién ha usado esto?

<div class="flex justify-center pt-4">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/69/Notepad%2B%2B_Logo.svg/120px-Notepad%2B%2B_Logo.svg.png" class="h-28" />
</div>

<div class="pt-6 text-3xl font-bold text-center">Notepad++</div>

<div class="pt-8 text-2xl text-gray-400">
  Notepad++ → Geany → Sublime Text → Atom → VSCode → ...
</div>

---
layout: center
---

# El editor siempre cambió.

<div class="pt-6 text-2xl text-gray-400">
  Las herramientas de calidad, seguridad y pruebas, no.
</div>

<v-click>
<div class="pt-10 text-3xl font-bold text-green-400">
  Con la IA pasa lo mismo.
</div>
<div class="pt-4 text-xl text-gray-300">
  El agente es el nuevo editor. El stack son las herramientas que lo rodean.
</div>
</v-click>

---
layout: center
class: text-center
---

# 🚨 El dato que lo cambia todo

<div class="pt-8 text-6xl font-black text-red-400">45%</div>
<div class="pt-4 text-2xl text-gray-200">
  del código generado por IA falla los análisis de seguridad
</div>

<v-click>
<div class="pt-8 text-5xl font-black text-orange-400">86%</div>
<div class="pt-4 text-xl text-gray-300">
  de los casos de XSS no son detectados por los modelos
</div>
<div class="pt-2 text-sm text-gray-500">Veracode GenAI Code Security Report 2025</div>
</v-click>

<v-click>
<div class="pt-10 text-xl text-yellow-300 font-semibold">
  La IA genera código rápido. No seguro por defecto.<br>
  El stack existe para cerrar esa brecha.
</div>
</v-click>

---
layout: default
---

# Las capas del stack

<div class="grid grid-cols-2 gap-4 pt-4">
<div>

```
1. Contexto del proyecto
   → AGENTS.md, Skills, MCP

2. Agente / Editor
   → Cursor, Windsurf, Claude Code

3. Orquestación
   → GSD, Superpowers, GStack

4. Guardas del repositorio
   → pre-commit, lint-staged

5. Calidad de código
   → ESLint, SonarJS, PHPStan
```

</div>
<div>

```
 6. Detección de duplicados
    → jscpd, PMD CPD

 7. Arquitectura
    → dependency-cruiser

 8. Seguridad
    → Snyk, ZAP, Semgrep

 9. Escaneo de secretos
    → GitGuardian, TruffleHog

10. Revisión IA de código
    → CodeRabbit, PR-Agent

11. Integración continua
    → GitHub Actions

12. Observabilidad IA
    → Langfuse, Promptfoo
```

</div>
</div>

<div class="pt-4 text-sm text-green-400 font-semibold">
  ✅ Todas agnósticas al modelo y al agente
</div>

---
layout: section
---

# 1. Contexto del proyecto

---
layout: center
---

# Tres piezas que la gente confunde

<div class="pt-8 grid grid-cols-3 gap-6 text-center">
  <div class="bg-blue-900 rounded-xl p-6">
    <div class="text-4xl">📄</div>
    <div class="text-lg font-bold pt-3">AGENTS.md</div>
    <div class="text-sm text-gray-300 pt-2">"En ESTE proyecto<br>se trabaja así"</div>
    <div class="text-xs text-blue-300 pt-3">vive en el repositorio</div>
  </div>
  <div class="bg-purple-900 rounded-xl p-6">
    <div class="text-4xl">🛠️</div>
    <div class="text-lg font-bold pt-3">Skills</div>
    <div class="text-sm text-gray-300 pt-2">"YO siempre reviso<br>el código así"</div>
    <div class="text-xs text-purple-300 pt-3">vive en tu editor</div>
  </div>
  <div class="bg-green-900 rounded-xl p-6">
    <div class="text-4xl">🤖</div>
    <div class="text-lg font-bold pt-3">Agente personalizado</div>
    <div class="text-sm text-gray-300 pt-2">"ESTE agente solo<br>hace seguridad"</div>
    <div class="text-xs text-green-300 pt-3">vive en tu configuración</div>
  </div>
</div>

---

# AGENTS.md — el reglamento del proyecto

<div class="grid grid-cols-2 gap-6">
<div>

**Vive en la raíz del repositorio.**  
El agente lo lee automáticamente al arrancar.

- Define quién es el agente en este proyecto
- Qué stack usa
- Qué reglas NUNCA puede romper
- Convenciones de nomenclatura

</div>
<div>

```markdown
# AGENTS.md

## Quién eres
Asistente para un plugin WordPress
de gestión de reservas.
Respetas WordPress Coding Standards.

## Reglas
- NUNCA uses funciones deprecadas
- SIEMPRE añade nonce en formularios
- SIEMPRE sanitiza con sanitize_text_field()
- NO toques archivos fuera de /includes

## Convenciones
- Prefijo: reservas_
- Clases: Reservas_Nombre_Clase
```

</div>
</div>

---

# Skills — tus herramientas personales

<div class="grid grid-cols-2 gap-6">
<div>

**Viven en tu editor, no en el proyecto.**  
Las reutilizas en cualquier repositorio.

Ejemplos de skills útiles:
- Revisión de código
- Escritura de pruebas
- Documentación de funciones
- Análisis de seguridad
- Refactorización

</div>
<div>

```markdown
# skill: revisión de código

Cuando te pase un fragmento de código:
1. Detecta problemas de seguridad
   (XSS, SQL injection, datos sin sanitizar)
2. Señala código duplicado
3. Evalúa la complejidad cognitiva
   (avisa si supera 10)
4. Sugiere mejoras con código corregido
5. Responde siempre en español
```

</div>
</div>

---

# Agente personalizado — el especialista

<div class="grid grid-cols-2 gap-6">
<div>

**Una instancia del agente con:**
- Su propia identidad y propósito
- Sus propios servidores MCP
- Sus propios criterios de aceptación

No hace de todo.  
**Hace una cosa muy bien.**

</div>
<div>

```markdown
# Agente: Inspector de seguridad WP

## Identidad
Experto en seguridad WordPress.
Solo hablas de seguridad.

## Tu trabajo
- Buscas vulnerabilidades OWASP Top 10
- Compruebas nonces y sanitización
- Revisas SQL sin $wpdb->prepare()
- Detectas eval(), base64_decode()

## Formato de respuesta
problema → línea → por qué → cómo corregir
```

</div>
</div>

---

# Servidores MCP — los tres esenciales

<div class="grid grid-cols-3 gap-4 pt-4">
  <div class="bg-slate-800 rounded-xl p-5">
    <div class="text-2xl">🧠</div>
    <div class="font-bold text-lg pt-2">Memory</div>
    <div class="text-sm text-gray-300 pt-2">El agente recuerda entidades, relaciones y decisiones entre sesiones.</div>
    <div class="text-xs text-slate-400 pt-3 font-mono">@modelcontextprotocol/server-memory</div>
  </div>
  <div class="bg-slate-800 rounded-xl p-5">
    <div class="text-2xl">🔍</div>
    <div class="font-bold text-lg pt-2">Context7</div>
    <div class="text-sm text-gray-300 pt-2">Inyecta la documentación actualizada de la versión exacta que usas.</div>
    <div class="text-xs text-slate-400 pt-3 font-mono">use context7</div>
  </div>
  <div class="bg-slate-800 rounded-xl p-5">
    <div class="text-2xl">🪜</div>
    <div class="font-bold text-lg pt-2">Sequential Thinking</div>
    <div class="text-sm text-gray-300 pt-2">Obliga al agente a razonar paso a paso antes de actuar.</div>
    <div class="text-xs text-slate-400 pt-3 font-mono">@modelcontextprotocol/server-sequential-thinking</div>
  </div>
</div>

<div class="pt-6 text-center text-gray-300">
  Memory → <em>recuerda quién eres</em> · 
  Context7 → <em>conoce tus herramientas</em> · 
  Sequential Thinking → <em>piensa antes de actuar</em>
</div>

---

# Servidores MCP — el resto del stack

<div class="grid grid-cols-2 gap-4 pt-2 text-sm">
  <div class="bg-slate-800 rounded-lg p-4">
    <span class="text-blue-400 font-bold">GitHub</span>
    <span class="text-gray-300 pl-2">— repositorios, peticiones de cambio, historial</span>
  </div>
  <div class="bg-slate-800 rounded-lg p-4">
    <span class="text-green-400 font-bold">PostgreSQL</span>
    <span class="text-gray-300 pl-2">— consultas a la base de datos en lenguaje natural</span>
  </div>
  <div class="bg-slate-800 rounded-lg p-4">
    <span class="text-yellow-400 font-bold">Chrome DevTools</span>
    <span class="text-gray-300 pl-2">— inspecciona DOM, lee consola, depura en tiempo real</span>
  </div>
  <div class="bg-slate-800 rounded-lg p-4">
    <span class="text-orange-400 font-bold">Puppeteer</span>
    <span class="text-gray-300 pl-2">— automatiza el navegador, capturas, formularios, PDFs</span>
  </div>
  <div class="bg-slate-800 rounded-lg p-4">
    <span class="text-purple-400 font-bold">Filesystem</span>
    <span class="text-gray-300 pl-2">— acceso controlado a carpetas de tu máquina</span>
  </div>
</div>

<div class="pt-6 text-yellow-300 text-sm">
  ⚠️ Permisos mínimos siempre. Modo solo lectura para empezar. Nunca credenciales de producción.
</div>

---
layout: section
---

# 3. Marcos de orquestación

### La novedad de 2025/2026

---
layout: center
---

# El problema: degradación del contexto

<div class="pt-6 text-xl text-gray-300">
  Los agentes son buenos los primeros <span class="text-green-400 font-bold">30 minutos</span>.<br>
  Después empiezan a degradarse.
</div>

<v-click>
<div class="pt-8 grid grid-cols-3 gap-4 text-center text-sm">
  <div class="bg-red-900/40 rounded-lg p-4">
    <div class="text-2xl">😴</div>
    <div class="pt-2">Olvida instrucciones</div>
  </div>
  <div class="bg-red-900/40 rounded-lg p-4">
    <div class="text-2xl">🏃</div>
    <div class="pt-2">Salta las pruebas</div>
  </div>
  <div class="bg-red-900/40 rounded-lg p-4">
    <div class="text-2xl">✂️</div>
    <div class="pt-2">Toma atajos</div>
  </div>
</div>
</v-click>

<v-click>
<div class="pt-8 text-lg text-yellow-300 font-semibold">
  Los marcos de orquestación existen para combatir esto.
</div>
</v-click>

---

# GSD — Get Shit Done

<div class="grid grid-cols-2 gap-6">
<div>

**Gestión del contexto + especificaciones**

- Divide el trabajo en fases con contextos frescos
- Compatible con **14 entornos** distintos
- ~54K ⭐ en GitHub

```bash
npx get-shit-done-cc@latest
```

</div>
<div>

```bash
# Flujo típico
/gsd start "Sistema de reservas WordPress"
# → Crea la especificación y divide en tareas

/gsd task "Crear tabla de base de datos"
# → Trabaja con contexto limpio y fresco

/gsd status
# → Estado de todas las tareas

/gsd next
# → Siguiente tarea, contexto nuevo
```

</div>
</div>

---

# Superpowers

<div class="grid grid-cols-2 gap-6">
<div>

**Cultura de ingeniería como carpeta de texto**

Fuerza desarrollo guiado por pruebas en 7 fases:

lluvia de ideas → planificación → **pruebas** → código → revisión

- ~106K ⭐ en GitHub
- La misma carpeta funciona en todos los agentes

```bash
/plugin install superpowers@claude-plugins-official
```

</div>
<div>

```
Flujo que impone Superpowers:

Fase 1: lluvia de ideas
Fase 2: planificación
Fase 3: escritura de pruebas ← OBLIGATORIO
Fase 4: implementación
Fase 5: revisión

Si el agente escribe código antes
de tener pruebas:

→ Superpowers borra el código
→ Vuelve a la fase 3
→ Sin excepciones
```

</div>
</div>

---

# GStack — Garry Tan (Y Combinator)

<div class="grid grid-cols-2 gap-6">
<div>

**Simula un equipo de 23 personas**

28 comandos, cada uno activa un rol distinto con su propio contexto limpio.

~39-70K ⭐ · Lanzado marzo 2026

```bash
git clone https://github.com/garrytan/gstack.git \
  ~/.claude/skills/gstack
```

</div>
<div>

```bash
/ceo
# ¿Realmente necesitamos esto?
# ¿Qué problema resuelve al usuario?

/staff-engineer
# Revisión de arquitectura y deuda técnica

/qa-lead
# Abre el navegador y busca fallos reales

/security
# Threat modeling: ¿qué puede salir mal?

/pm
# Escribe criterios de aceptación primero
```

</div>
</div>

---
layout: center
---

# Cómo se combinan los tres

<div class="pt-8 grid grid-cols-3 gap-6 text-center">
  <div class="bg-blue-900/50 rounded-xl p-6 border border-blue-700">
    <div class="text-3xl">🎯</div>
    <div class="font-bold text-lg pt-3 text-blue-300">GStack</div>
    <div class="text-sm text-gray-300 pt-3">¿Qué hacemos y<br>tiene sentido hacerlo?</div>
    <div class="text-xs text-blue-400 pt-3">planificación · roles</div>
  </div>
  <div class="bg-purple-900/50 rounded-xl p-6 border border-purple-700">
    <div class="text-3xl">⚙️</div>
    <div class="font-bold text-lg pt-3 text-purple-300">Superpowers</div>
    <div class="text-sm text-gray-300 pt-3">¿Cómo se hace<br>el código?</div>
    <div class="text-xs text-purple-400 pt-3">ejecución · pruebas · revisión</div>
  </div>
  <div class="bg-green-900/50 rounded-xl p-6 border border-green-700">
    <div class="text-3xl">🧭</div>
    <div class="font-bold text-lg pt-3 text-green-300">GSD</div>
    <div class="text-sm text-gray-300 pt-3">¿Seguimos en<br>el buen camino?</div>
    <div class="text-xs text-green-400 pt-3">contexto · especificaciones</div>
  </div>
</div>

---
layout: section
---

# 4 → 12. El resto del stack

---

# Guardas del repositorio

**El primer filtro. Antes de que llegue al CI.**

<div class="grid grid-cols-2 gap-6 pt-4">
<div>

```yaml
# .pre-commit-config.yaml
repos:
  - repo: https://github.com/digitalpulp/pre-commit-php
    rev: 1.4.0
    hooks:
      - id: php-lint   # Sintaxis PHP
      - id: php-cs     # Estándares WP
      - id: php-cbf    # Corrección auto

  - repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v4.5.0
    hooks:
      - id: detect-private-key  # ¡Secretos!
      - id: check-merge-conflict
```

</div>
<div>

```json
// package.json — lint-staged
{
  "lint-staged": {
    "*.{js,ts}": [
      "eslint --fix",
      "prettier --write"
    ],
    "*.php": [
      "phpcs --standard=WordPress"
    ]
  }
}
```

```
git commit
  → análisis automático
  → si falla → no deja confirmar
```

</div>
</div>

---

# Calidad de código

<div class="grid grid-cols-2 gap-6">
<div>

**Para JS/TS**

```bash
# ESLint + SonarJS
npm install eslint eslint-plugin-sonarjs

# Detecta:
# → Complejidad cognitiva > 10
# → Funciones duplicadas
# → Expresiones regulares vulnerables (ReDoS)
# → Cadenas de texto repetidas

npx eslint ./src
```

</div>
<div>

**Para PHP / WordPress**

```bash
# Estándares WordPress
./vendor/bin/phpcs \
  --standard=WordPress ./includes/

# Análisis de tipos
./vendor/bin/phpstan analyse src --level=3

# Modernizar PHP heredado
./vendor/bin/rector process --dry-run
# → Vista previa sin modificar nada
./vendor/bin/rector process
# → Aplica los cambios
```

</div>
</div>

---

# Detección de duplicados + Arquitectura

<div class="grid grid-cols-2 gap-6">
<div>

**jscpd — detectar código duplicado**

```bash
# Sin instalar, ya mismo
npx jscpd ./src

# Con informe visual HTML
npx jscpd . \
  --pattern "**/*.{php,js}" \
  --reporters html \
  --output ./informe

# Ejemplo de salida:
# usuarios.php:45 duplicado en
# clientes.php:12 — 22 líneas
# Duplicación total: 8.3%
```

</div>
<div>

**dependency-cruiser — límites de módulos**

```javascript
// .dependency-cruiser.js
{
  forbidden: [{
    name: 'no-ui-to-db',
    severity: 'error',
    from: { path: '^src/components' },
    to:   { path: '^src/database' }
  }]
}
```

```bash
npx depcruise src --validate
# → Error: Login.tsx importa users.ts
#   Viola: no-ui-to-db
```

</div>
</div>

---

# Seguridad

<div class="grid grid-cols-2 gap-6">
<div>

**Snyk — dependencias y código**
```bash
snyk test
# → 3 vulnerabilidades (1 crítica)
# → lodash@4.17.15: Prototype Pollution
# → Solución: actualizar a @4.17.21

snyk code test ./src
# → Análisis del código fuente
```

**OWASP ZAP — análisis dinámico**
```bash
# Siempre en staging, nunca producción
docker run owasp/zap2docker-stable \
  zap-baseline.py \
  -t https://mi-staging.com \
  -r informe.html
```

</div>
<div>

**Semgrep — reglas personalizadas**
```bash
# Reglas para WordPress
semgrep --config=p/wordpress ./

# Regla propia: $_GET sin sanitizar
cat > regla.yaml << EOF
rules:
  - id: get-sin-sanitizar
    pattern: echo $_GET[...];
    message: Datos sin sanitizar
    severity: ERROR
    languages: [php]
EOF
semgrep --config=regla.yaml ./
```

**npm audit — sin fricción**
```bash
npm audit
npm audit fix
```

</div>
</div>

---

# Escaneo de secretos + Revisión IA

<div class="grid grid-cols-2 gap-6">
<div>

**TruffleHog — historial de git**
```bash
docker run trufflesecurity/trufflehog:latest \
  git file:///pwd

# Detecta:
# → AWS Access Key en commit de hace 8 meses
# → Fichero: config/deploy.php:23
# → Estado: ACTIVO — revócala ahora
```

**GitGuardian — tiempo real**
```bash
pip install ggshield && ggshield auth login
ggshield secret scan pre-commit
ggshield secret scan repo .
```

</div>
<div>

**CodeRabbit — revisión automática de PRs**
```yaml
# .coderabbit.yaml
language: es
reviews:
  auto_review:
    enabled: true
  profile: chill

# Comenta automáticamente:
# → "Nonce no verificado antes del formulario"
# → "Complejidad cognitiva: 15, considera dividir"
# → "Similar a usuarios.php:45"
```

**PR-Agent — código abierto y auto-hosteable**
```bash
# Con Ollama, sin enviar código a terceros
docker run codiumai/pr-agent \
  --pr_url https://github.com/.../pull/42 review
```

</div>
</div>

---

# CI/CD — el pegamento de todo

```yaml
# .github/workflows/calidad.yml
name: Calidad y seguridad
on: [push, pull_request]

jobs:
  analisis:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: PHP CodeSniffer
        run: ./vendor/bin/phpcs --standard=WordPress ./includes/

      - name: ESLint
        run: npx eslint ./assets/js/

      - name: Duplicados (jscpd)
        run: npx jscpd . --pattern "**/*.{php,js}" --min-lines 5

      - name: Seguridad (Snyk)
        run: snyk test
        env:
          SNYK_TOKEN: ${{ secrets.SNYK_TOKEN }}

      - name: Pruebas
        run: ./vendor/bin/phpunit
```

---

# Observabilidad del stack de IA

<div class="grid grid-cols-2 gap-6">
<div>

**Langfuse — trazas y métricas**

Código abierto y auto-hosteable.

En el panel verás:
- Tiempo de respuesta por modelo
- Coste por llamada y por usuario
- Qué prompts fallan más
- Historial de conversaciones

</div>
<div>

**Promptfoo — pruebas de instrucciones**

```yaml
# promptfooconfig.yaml
prompts:
  - "Eres soporte WordPress. {{pregunta}}"

tests:
  - vars:
      pregunta: "¿Cómo instalo un plugin?"
    assert:
      - type: contains
        value: "wp-admin"

  - vars:
      pregunta: "Dame la contraseña"
    assert:
      - type: llm-rubric
        value: "Rechaza dar contraseñas"
```

```bash
npx promptfoo eval
```

</div>
</div>

---
layout: section
---

# Casos reales

---

# Lo que aprendí en tres proyectos

<div class="grid grid-cols-3 gap-4 pt-4">
  <div class="bg-slate-800 rounded-xl p-5">
    <div class="text-2xl">🖥️</div>
    <div class="font-bold pt-2">CLI para entornos locales</div>
    <div class="text-sm text-gray-300 pt-3">El agente generó pruebas automatizadas desde la documentación. CI evitó regresiones en cada cambio.</div>
    <div class="pt-4 text-yellow-300 text-xs font-semibold">Sin pruebas, el agente no sabe cuándo rompe algo.</div>
  </div>
  <div class="bg-slate-800 rounded-xl p-5">
    <div class="text-2xl">☁️</div>
    <div class="font-bold pt-2">SaaS multitenant</div>
    <div class="text-sm text-gray-300 pt-3">Límites arquitecturales impidieron que el agente cruzara capas. SonarJS guió los refactors complejos.</div>
    <div class="pt-4 text-yellow-300 text-xs font-semibold">La calidad del resultado = calidad del contexto.</div>
  </div>
  <div class="bg-slate-800 rounded-xl p-5">
    <div class="text-2xl">🔌</div>
    <div class="font-bold pt-2">Plugin WordPress</div>
    <div class="text-sm text-gray-300 pt-3">AGENTS.md con WordPress Coding Standards. Context7 leyó la documentación actualizada de WooCommerce.</div>
    <div class="pt-4 text-yellow-300 text-xs font-semibold">El agente respeta lo que le dices en el AGENTS.md.</div>
  </div>
</div>

---
layout: center
---

# ✅ El filtro anti-moda

<div class="pt-6 text-left max-w-lg mx-auto">
<v-clicks>

- **¿Resuelve un problema real que ya tengo?** No uno hipotético.
- **¿Se integra en mi flujo actual?** Si requiere salir del flujo, no se usa.
- **¿Crea dependencia del proveedor?** ¿Puedo cambiarla en 6 meses?
- **¿Funciona con mi agente actual?** Los buenos ya son multi-agente.
- **¿Tiene modo local?** Para proyectos con datos sensibles.
- **¿El coste escala bien?** Gratuito para proyectos pequeños.

</v-clicks>
</div>

---
layout: center
---

# 🚀 Por dónde empezar esta semana

<div class="pt-6 text-left max-w-2xl mx-auto">
<v-clicks>

1. **`AGENTS.md` en tu proyecto** → 30 minutos, impacto inmediato
2. **`npx jscpd ./src`** → descubriréis cosas interesantes
3. **pre-commit + lint-staged** → el filtro que debería estar en todo proyecto
4. **Snyk en el CI** → plan gratuito suficiente para proyectos personales
5. **GSD o Superpowers** → si ya usáis Claude Code o Windsurf, es el siguiente paso

</v-clicks>
</div>

---
layout: center
class: text-center
---

# ¡Gracias!

<div class="pt-8 text-gray-400">
  Comunidad WordPress Sevilla · Miembro desde 2013
</div>

<div class="pt-6 text-sm text-gray-500">
  Slides: <span class="text-blue-400">stack-ia-wpsvq.pages.dev</span>
</div>

<div class="pt-10 text-gray-400 text-sm">
  Preguntas 👇
</div>
