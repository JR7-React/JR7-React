<div align="center">

<img src="https://github.com/user-attachments/assets/e4580b89-87ea-4705-9ffe-89323fca769a" alt="JR7Dev" width="260"/>

# Javier Romero

**Desarrollador full-stack · React / TypeScript · Django · PostgreSQL · Honduras**

Construí y desplegué, como único desarrollador, dos sistemas que hoy usa una fundación de Honduras:
uno de monitoreo comunitario y otro de gestión médica, los dos capaces de trabajar sin conexión.

[LinkedIn](https://www.linkedin.com/in/javi-romero-85486833a/) · [Correo](mailto:javierromero181818@gmail.com)

</div>

---

## 🛠️ Tecnologías

<table>
<tr>
<td width="50%" valign="top">

#### 💻 **Frontend**
![React](https://img.shields.io/badge/React_18-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![TanStack Query](https://img.shields.io/badge/TanStack_Query_v5-FF4154?style=for-the-badge&logo=react-query&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Material UI](https://img.shields.io/badge/MUI_v5-0081CB?style=for-the-badge&logo=material-ui&logoColor=white)
![DnD Kit](https://img.shields.io/badge/@dnd--kit-Drag_&_Drop-555555?style=for-the-badge&logoColor=white)
![React Grid Layout](https://img.shields.io/badge/React_Grid_Layout-Modular_Board-222222?style=for-the-badge&logoColor=white)

#### 🤖 **IA y protocolos**
![Model Context Protocol](https://img.shields.io/badge/MCP_Server-8A2BE2?style=for-the-badge&logoColor=white)
![Claude](https://img.shields.io/badge/Claude_(MCP)-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![OAuth 2.1](https://img.shields.io/badge/OAuth_2.1_+_PKCE-2E9EF7?style=for-the-badge&logoColor=white)
![SQL AST Guard](https://img.shields.io/badge/SQL_AST_Guard-00FF66?style=for-the-badge&logoColor=black)

</td>
<td width="50%" valign="top">

#### ⚙️ **Backend y tareas asíncronas**
![Python](https://img.shields.io/badge/Python_3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django_5-092E20?style=for-the-badge&logo=django&logoColor=white)
![DRF](https://img.shields.io/badge/Django_REST_Framework-A30000?style=for-the-badge&logo=django&logoColor=white)
![Celery](https://img.shields.io/badge/Celery_5-37814A?style=for-the-badge&logo=celery&logoColor=white)
![Redis](https://img.shields.io/badge/Redis_7-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)

#### 🗄️ **Datos, GIS e infraestructura**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_16-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![PostGIS](https://img.shields.io/badge/PostGIS_3-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Dexie.js](https://img.shields.io/badge/Dexie.js_4_(IndexedDB)-2E9EF7?style=for-the-badge&logoColor=white)
![Cloudflare R2](https://img.shields.io/badge/Cloudflare_R2-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=for-the-badge&logo=railway&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)

</td>
</tr>
</table>

---

## Sistemas en producción

### SGC — Monitoreo comunitario sin conexión · [sgc.fundesur.org](https://sgc.fundesur.org/)

Plataforma web instalable (PWA) para que FUNDESUR diseñe formularios, levante encuestas en comunidades
sin señal, las revise y las convierta en indicadores por proyecto y territorio. Hice el análisis, la
arquitectura, el desarrollo, el despliegue y la capacitación.

- **Constructor de formularios** con arrastrar y soltar (@dnd-kit), versiones, lógica condicional,
  cálculos y validaciones, sin código para el usuario.
- **Captura sin conexión** con fotos, GPS y firmas, guardada en IndexedDB (Dexie) y sincronizada por
  lotes al recuperar señal, con resolución de conflictos.
- **Revisión de levantamientos:** solo lo aprobado cuenta en indicadores, exportaciones e IA.
- **Constructor de tableros** con cuadrícula reordenable (react-grid-layout) y gráficas en SVG.
- **Servidor MCP** para que analistas consulten los datos con Claude en lenguaje natural: OAuth,
  validación del SQL con `sqlparse`, rol de base de datos de solo lectura y registro de cada consulta.
- **Mapas y cobertura territorial** con PostGIS y MapLibre.
- **Seguridad:** 2FA, roles, auditoría y protección anti-bots en el inicio de sesión.

**Stack:** React 18 · TypeScript (estricto) · Vite · MUI 5 · TanStack Query · Dexie · Python 3.12 ·
Django 5 · DRF · Celery · Redis · PostgreSQL 16 + PostGIS · Cloudflare R2 · Docker · Railway

| Periodo | Commits | Funcionalidades especificadas | Archivos de pruebas | Servicios en producción |
|---|---|---|---|---|
| mar – sep 2026 | 2,809 | 123 | ~1,500 (backend y frontend) | 7, con CI en cada cambio |

<img src="https://raw.githubusercontent.com/JR7-React/JR7-React/main/assets/sgc/constructor-formularios-lienzo.jpg" alt="Constructor de formularios" width="100%"/>

<details>
<summary><b>Más capturas</b></summary>

<img src="https://raw.githubusercontent.com/JR7-React/JR7-React/main/assets/sgc/constructor-dashboard-personalizar.jpg" alt="Constructor de tableros" width="100%"/>
<img src="https://raw.githubusercontent.com/JR7-React/JR7-React/main/assets/sgc/conector-mcp-claude.jpg" alt="Consulta con Claude mediante MCP" width="100%"/>
<img src="https://raw.githubusercontent.com/JR7-React/JR7-React/main/assets/sgc/mapa-geoespacial.jpg" alt="Mapa de cobertura" width="100%"/>

</details>

---

### Salud para Vivir — Gestión médica e inventario · [saludparavivir.fundesur.org](https://saludparavivir.fundesur.org/)

Sistema para los centros de salud que apoya FUNDESUR: pacientes, atenciones, formatos clínicos de la
Secretaría de Salud, inventario y dispensación de medicamentos, con conectividad intermitente. Empezó
como mi proyecto de práctica profesional (UNAH) y luego lo amplié por contrato.

- **Expediente y atenciones:** signos vitales, diagnósticos CIE-10 y prescripciones.
- **Formatos clínicos imprimibles:** planificación familiar, control puerperal y AIEPI (niño menor de
  2 meses y de 2 meses a 4 años), con vista previa de impresión.
- **Inventario en dos niveles** (bodega general y cada centro): lotes, vencimientos, movimientos,
  ajustes, transferencias y pedidos.
- **Alertas automáticas** de vencimiento y existencias bajas, por correo y en el sistema.
- **Reportes PDF y Excel** (atenciones, morbilidad, consumo) y asistente de IA (Gemini) limitado por
  seguridad de filas al centro de quien pregunta.

**Stack:** React 18 · Vite · MUI 5 · React Hook Form + Zod · Dexie · react-virtuoso · Tailwind (formatos
imprimibles) · Django · DRF · Celery · Redis · PostgreSQL · Docker · Railway

| Periodo | Commits | Uso |
|---|---|---|
| jul 2025 – sep 2026 | 1,969 | Más de 1,500 atenciones en el primer centro; en expansión a 10 centros |

<img src="https://github.com/user-attachments/assets/d180c5b2-7669-4eb2-b17a-ea52563a08c9" alt="Formato de planificación familiar con vista previa de impresión" width="100%"/>

<details>
<summary><b>Más capturas</b></summary>

<img src="https://github.com/user-attachments/assets/1795c1ea-1f31-4517-adc7-d1455df82806" alt="Historial de atención AIEPI" width="100%"/>
<img src="https://github.com/user-attachments/assets/6bac3d26-744b-4580-bf92-eff649cca9bb" alt="Inventario por lotes" width="100%"/>
<img src="https://github.com/user-attachments/assets/d01f475d-0555-43c0-8889-074fb2e72514" alt="Comparativa de dispensación por centro" width="100%"/>

</details>

---

## Cómo trabajo

El sistema médico fue mi primer sistema completo y aprendí de sus errores: llegó a tener un archivo de
19,357 líneas y un mismo dato con varios nombres. En el SGC, un año después, el archivo más grande tiene
215 líneas (mediana de 62 en 3,658 archivos).

- Desarrollo guiado por especificaciones con Spec Kit: cada funcionalidad pasa por especificación,
  plan, tareas y verificación (123 especificaciones en el SGC).
- Reglas de calidad escritas: archivos pequeños, una responsabilidad por archivo, TypeScript estricto.
- Pruebas y CI antes de desplegar.
- Trabajo con agentes de IA (Claude Code) dentro de ese proceso, no en lugar de él, apoyado en un grafo
  de conocimiento del código (graphify) y memoria persistente entre sesiones (memanto).

---

## Otros proyectos

- [**merab-daemon**](https://github.com/JR7-React/merab-daemon) — Runtime local en Rust para agentes de
  IA: MCP, JSON-RPC, SQLite y ejecución de tareas en grafo.
- [**spec-kit-strict**](https://github.com/JR7-React/spec-kit-strict) — Extensión de Spec Kit con
  compuertas de calidad estrictas y commits por artefacto.
