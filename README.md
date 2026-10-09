DÚR·KROS — Duelo de Arcanos
===========================

Un juego de cartas, tablero hexagonal y magia táctica — en un solo archivo HTML,
y también como APK para Android.

Eres un mago del Collegium de Amsalor. Forja tu arcano, elige tu rama, construye tu mazo
y baja al Círculo: un tablero de 37 hexágonos donde cada decisión —dónde te mueves, cuándo
gastas tu Kros, qué hechizo lanzas— pesa.

Qué es
------

- Duelo 1v1 por turnos sobre un tablero hexagonal concéntrico (Centro · Interior · Exterior · Borde).
  Puedes ganar bajando la Vitalidad del rival a 0 **o empujándolo fuera del Círculo**.
- Motor de recursos a doble filo: el **Kros** (maná) se recupera despacio; gastar de más te
  empuja por debajo de tu **línea roja de sobrecalentamiento** y tus hechizos pueden corromperse.
  El **ψ** (sintonía) es una ventana móvil: quien la abandona, se desangra.
- Roguelike "Las Sendas": cuatro travesías (`El Peregrino`, `Los Faros`, `Nocturnis`, `La Ceniza`)
  con mapas que se bifurcan, criaturas, élites, eventos de rol con tiradas 2d6, mercaderes,
  cofres con reliquias y un jefe final por lugar. La Vitalidad **persiste** entre combates.
- Coleccionismo: 200+ cartas repartidas en 7 ramas, con rarezas, cajas, sobres, polvo y forja.
- Campeones: sistema gacha con fragmentos, niveles y estilos de IA propios.
- Multijugador en línea P2P por WebRTC (código de sala, partida rápida, emparejamiento
  clasificatorio por Elo), **dos jugadores en el mismo dispositivo** y torneos.
- Perfil y credencial: XP, rangos, logros, epítetos, sellos y una credencial PNG que
  **lleva tu progreso dentro** (comprimido y con suma de verificación) para respaldarlo.

Qué lo hace raro
----------------

- Todo en un solo `index.html`: HTML, CSS, JS, arte vectorial, música y efectos
  **sintetizados en Web Audio** (no hay ni un archivo externo). Cero dependencias, cero build.
- Pensado para el teléfono: diseño *mobile-first*, sin scroll horizontal, sin *overflow*,
  sin repintados innecesarios. Modo rendimiento automático en equipos modestos.
- Cero servidores propios: la señalización en línea usa PeerJS; el resto va directo
  entre jugadores. La clasificatoria es local, el estado se sincroniza por WebRTC.
- Arte generado: cada carta tiene una ilustración SVG determinista (por su código),
  con paleta de rama, motivo de familia y capas de atmósfera.

Cómo jugar
----------

No hay que compilar nada. Abre `index.html` en un navegador moderno (Chrome, Firefox, Safari
o Edge) y ya está.

```bash
git clone https://github.com/tu-usuario/durkros.git
cd durkros
# Abre index.html directamente, o sirve la carpeta con:
python3 -m http.server 8080
