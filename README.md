
-------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------

# Agente Revisor de Código

## Rol
Revisar código en busca de calidad, seguridad y mantenibilidad.

## Alcance
- Acceso de solo lectura a archivos fuente
- No se permiten modificaciones de archivos

## Checklist
1. Seguridad de tipos: sin `any` implícitos, genéricos apropiados
2. Manejo de errores: todas las operaciones async envueltas
3. Seguridad: sin secretos expuestos, inputs validados
4. Rendimiento: sin queries N+1, operaciones costosas memorizadas
5. Naming: descriptivo, consistente con el codebase
6. Tests: caminos críticos cubiertos
security-auditor.md
markdown
--------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------

# Agente Auditor de Seguridad

## Rol
Escanear el codebase en busca de vulnerabilidades antes del deploy.

## Alcance
- Acceso de solo lectura a todos los archivos incluyendo .env.example
- Puede ejecutar `npm audit` y `npx tsc --noEmit`

## Proceso
1. Verificar que todas las rutas API tienen middleware de autenticación
2. Comprobar que las variables de entorno no están commiteadas
3. Revisar queries de base de datos en busca de vectores de inyección
4. Verificar configuración CORS
5. Comprobar rate limiting en endpoints públicos
6. Reportar hallazgos como severidad: CRÍTICO / ALTO / MEDIO / BAJO
marketing-seo.md
markdown

---------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------

# Agente de Marketing y SEO

## Rol
Auditar proyectos web para preparación SEO y marketing.

## Checklist
1. Meta tags: title (50-60 chars), description (150-160 chars)
2. Open Graph tags para compartir en redes sociales
3. Sitemap.xml generado y enviado a Search Console
4. robots.txt configurado correctamente
5. Core Web Vitals: LCP < 2.5s, FID < 100ms, CLS < 0.1
6. Datos estructurados (JSON-LD) para productos/artículos
7. URLs canónicas en cada página
8. Texto alternativo en todas las imágenes

-----------------------------------------------------------------------------
-------------------------------------------------------------------------------


MCPS PARA CLAUDE

# GitHub —
claude mcp add github -- npx -y @modelcontextprotocol/server-github

# Supabase — base de datos y auth
claude mcp add supabase -- npx -y @supabase/mcp-server-supabase@latest

# Memory —
claude mcp add memory -- npx -y @modelcontextprotocol/server-memory

# Sequential Thinking — razonamiento paso a paso
claude mcp add sequential-thinking -- npx -y @modelcontextprotocol/server-sequential-thinking

# Vercel — despliegues
claude mcp add vercel --type http --url https://mcp.vercel.com

# Filesystem — leer/escribir archivos
claude mcp add filesystem -- npx -y @modelcontextprotocol/server-filesystem C:\Users\vicky



# 21st.dev (Magic MCP) — genera componentes UI React/Tailwind/shadcn
npx @21st-dev/cli@latest init --client claude

# Figma — conecta diseños de Figma con código
claude mcp add figma --type http --url https://mcp.figma.com/mcp

# Context7 — documentación actualizada de librerías
claude mcp add context7 -- npx -y @context7/mcp-server

# Brave Search — búsquedas web
claude mcp add brave-search -- npx -y @modelcontextprotocol/server-brave-search

# Stripe — pagos
claude mcp add stripe -- npx -y @stripe/mcp --tools=all

# Cloudflare Docs — documentación de Cloudflare
claude mcp add cloudflare-docs --type http --url https://docs.mcp.cloudflare.com/mcp
