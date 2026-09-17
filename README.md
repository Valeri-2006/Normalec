# NormaLec

Plataforma de automatización y apoyo al diseño de instalaciones eléctricas — validación
normativa asistida por un sistema multiagente de IA.

Proyecto de grado (cuatro semestres), desarrollado en colaboración con **Ingelecol**, firma de
ingeniería eléctrica en Bogotá dedicada al diseño de instalaciones residenciales para radicación
ante Enel-Codensa bajo las normas **RETIE** y **NTC 2050**.

## Problema

El diagnóstico inicial con el equipo de Ingelecol mostró que:

- El 100% de los ingenieros reporta reproceso costoso y ciclos de corrección frecuentes.
- El 100% depende de un único ingeniero senior como autoridad normativa.
- El 0% cuenta con un checklist formal que cubra todo el proceso.

NormaLec busca distribuir ese conocimiento normativo tácito sin eliminar la supervisión humana:
**la IA nunca aprueba, solo sugiere**.

## Arquitectura (estado actual)

- **Plataforma**: dashboard web con arquitectura limpia/hexagonal (Ports & Adapters).
- **Núcleo**: motor de reglas de negocio determinístico y versionado (el aporte de ingeniería
  principal del proyecto).
- **Integración BIM**: extracción de parámetros vía Dynamo desde Revit (sin API de Revit como
  alcance principal, sin Design Automation API en la nube).
- **Capa de IA**: sistema multiagente compuesto por un agente RAG normativo con citación
  verificable, un agente de verificación determinística de reglas, un agente de interpretación de
  ambigüedades y un orquestador.

### Los cinco miniproyectos

1. Modelado del dominio normativo y motor de reglas versionado.
2. Dashboard web hexagonal.
3. Adaptador de extracción de datos BIM vía Dynamo.
4. Agente RAG normativo con citación verificable.
5. Orquestación multiagente con seguridad transversal.

## Tecnologías

- HTML5 semántico + CSS3 (Flexbox, diseño responsivo)
- (Por definir en próximos semestres: stack del dashboard, motor de reglas y agentes de IA)

## Estructura del repositorio

```
normalec/
├── index.html
├── estilos.css
├── screenshots/       # Capturas responsive (mobile, tablet, desktop)
├── validation/        # Reportes de validación W3C y WAVE
└── README.md
```

## Estado

En construcción — landing page inicial del proyecto. La secuenciación por semestre contempla
checklists determinísticos y motor de reglas en semestres 1–2, agente normativo basado en RAG en
el semestre 3, y recomendaciones basadas en ML (condicionadas a datos propietarios suficientes)
en el semestre 4.
