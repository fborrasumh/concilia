# ConcilIA — Consejo de Consciencia

Aplicación web de un solo fichero que reproduce, sobre la API de OpenAI, la arquitectura de
deliberación multiperspectiva del skill [`consciousness-council`](https://github.com/K-Dense-AI/scientific-agent-skills/tree/main/skills/consciousness-council)
(AHK Strategies, licencia MIT).

**App:** https://fborrasumh.github.io/concilia/

## Qué hace

Doce arquetipos de pensamiento —la Arquitecta, el Contrario, la Empirista, la Ética, el
Futurista, la Pragmática, el Historiador, la Empática, el Forastero, la Estratega, el
Minimalista y la Creadora— deliberan sobre una pregunta con incertidumbre real, y la
fricción entre ellos se convierte en criterio de decisión.

El proceso tiene tres fases:

1. **Convocatoria.** El modelo compone una mesa de 3, 5 o 6 miembros cuyas perspectivas
   vayan a chocar de verdad, partiendo de plantillas por tipo de pregunta (negocio,
   arquitectura técnica, dilema personal, reto creativo, cuestión ética, estrategia,
   crisis, personas, inversión). Si la pregunta es trivial, lo advierte y ofrece un
   contraste rápido de dos perspectivas.
2. **Deliberación.** Cada miembro interviene desde su lente con posición, razonamiento,
   riesgo que ve, insight inesperado y un desacuerdo sustantivo con otro miembro
   concreto. Un auditor detecta posiciones redundantes y obliga a reformularlas: si todos
   coinciden, el consejo ha fallado.
3. **Síntesis.** Puntos de convergencia, tensión central, punto ciego que nadie abordó,
   camino recomendado que respeta la tensión, nivel de confianza y una pregunta con la que
   quedarse.

## Configuraciones

- Consejo rápido (3), estándar (5) o deliberación profunda (6 miembros).
- Selección automática o manual de los arquetipos.
- Modo rondas: réplica cruzada y posición revisada.
- Abogado del diablo: todos argumentan contra lo intuitivo.
- Consejo anónimo, con revelación de identidades tras la síntesis.
- Consejo silencioso: solo la síntesis.
- Arquetipos propios definidos por el usuario (lente, pregunta firma, punto ciego).
- Council Quality Score: diversidad, tensión, punto ciego y accionabilidad,
  con CQS = 0,25·D + 0,30·T + 0,25·PC + 0,20·A.
- Dossier de evidencia web opcional vía Tavily, citado como [F1], [F2]… en la deliberación.

## Uso

Abre la app, pega tu clave de OpenAI en «Claves API» y convoca. La clave se guarda solo en
el `localStorage` del navegador y las llamadas van directamente de tu equipo a la API; no
hay servidor intermedio. Modelo por defecto: `gpt-4o-mini`. Las sesiones se guardan en
IndexedDB y se pueden exportar a Markdown o JSON.

## Créditos

Arquitectura del consejo basada en el skill `consciousness-council` de AHK Strategies
(MIT). Implementación web: Fernando Borrás Rocher, Universidad Miguel Hernández de Elche.
Parte del catálogo [Herramientas IA para la academia](https://fborrasumh.github.io/ia/).

## Licencia

MIT
