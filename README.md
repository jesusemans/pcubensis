# pcubensis

A real-time 3D simulation of the *Psilocybe cubensis* lifecycle, from spore germination to full mycelial colonization and fruiting. Built entirely in a single HTML file with no build step required.

## What it does

The simulation runs through a staged timeline: spores appear and fall, hyphae grow outward using a Space Colonization Algorithm across a 3D spatial hash grid, and mushrooms emerge procedurally. Secondary fruiting bodies develop at offset positions once the main colony is established. Spores continuously release from under the caps and drift.

Everything is rendered with Three.js r170, post-processed with bloom (UnrealBloomPass), and can be orbited freely with the mouse.

## Technical details

- Mycelium growth: Space Colonization Algorithm with auxin flux canalization, up to 40,000 nodes, expanding and retracting wavefront glow
- Mushroom geometry: procedural LatheGeometry profile (stipe, shoulder, cap dome), 3D gill blades, annulus/veil, canvas-generated diffuse and bump textures
- Spore simulation: 800 particles spawned from under the cap gills, fall with initial downward velocity, then buoyancy and radial drift over an 8–18s lifetime
- Post-processing: EffectComposer + UnrealBloomPass (strength 0.9, radius 0.6, threshold 0.35) + OutputPass
- No dependencies beyond Three.js, loaded via importmap from CDN

## How to run

Download `psilocybe_cubensis.html` and open it in a modern browser. That's it.

Requires a browser with importmap support: Chrome 89+, Firefox 108+, Safari 16.4+.

---

# pcubensis (español)

Simulación 3D en tiempo real del ciclo de vida de *Psilocybe cubensis*, desde la germinación de esporas hasta la colonización micelial completa y la fructificación. Está construida en un único archivo HTML, no requiere instalación ni build.

## Qué hace

La simulación avanza por etapas cronológicas: las esporas aparecen y caen, las hifas crecen usando un Algoritmo de Colonización por Espacio sobre una grilla de hash espacial 3D, y los hongos emergen de forma procedural. Los cuerpos fructíferos secundarios se desarrollan en posiciones desplazadas una vez que la colonia principal está establecida. Las esporas se liberan continuamente desde debajo del sombrero y se dispersan.

Todo se renderiza con Three.js r170, se post-procesa con bloom (UnrealBloomPass), y se puede orbitar libremente con el mouse.

## Detalles técnicos

- Crecimiento del micelio: Algoritmo de Colonización por Espacio con canalización de flujo de auxinas, hasta 40.000 nodos, frente de onda expansivo y retractivo
- Geometría del hongo: perfil LatheGeometry procedural (estipe, hombro, cúpula del sombrero), láminas 3D, anillo/velo, texturas difusas y de relieve generadas en canvas
- Simulación de esporas: 800 partículas naciendo bajo las láminas del sombrero, con velocidad inicial descendente, luego flotabilidad y dispersión radial en un ciclo de vida de 8 a 18 segundos
- Post-procesado: EffectComposer + UnrealBloomPass (strength 0.9, radius 0.6, threshold 0.35) + OutputPass
- Sin dependencias más allá de Three.js, cargado vía importmap desde CDN

## Cómo ejecutarlo

Descargá `psilocybe_cubensis.html` y abrilo en un navegador moderno. Nada más.

Requiere soporte de importmap: Chrome 89+, Firefox 108+, Safari 16.4+.
