# Quiniela Mundial 2026 — Camilo vs Sofía 🏆

Tablero en vivo de nuestra quiniela de la Copa del Mundo 2026. Lee los datos directo de un Google Sheet y se actualiza solo cada minuto. Pensado para mobile.

**En vivo:** https://camotoya.github.io/quiniela-mundial-2026/

## Cómo funciona
- Toda la data vive en un Google Sheet (fixture de los 104 partidos, predicciones y resultados).
- El tablero lee el sheet vía el endpoint público `gviz/tq?tqx=out:csv` (solo lectura, sin claves).
- Las predicciones y los marcadores se cargan **a mano desde el celular en el Sheet**; los puntos se calculan con fórmulas. El tablero solo muestra.

## Secciones
1. **Marcador global** — duelo Camilo (cian) vs Sofía (magenta).
2. **Próximos** — lo que viene, con cuenta regresiva y las predicciones de cada uno.
3. **Resultados** — partidos jugados, con marcador real, predicciones y puntos ganados.

## Configurar otro sheet
Editar al inicio del `<script>` en `index.html`:
```js
const SHEET_ID = "...";   // id del Google Sheet
const GID = "...";        // id de la pestaña con la data
```
El sheet debe estar compartido como **"Cualquiera con el enlace · Lector"**.

## Sistema de puntaje
| Criterio | Grupos | Eliminatorias |
|---|---|---|
| Acertar ganador/empate | 5 | 10 |
| Goles del local | 2 | 4 |
| Goles del visitante | 2 | 4 |
| Diferencia de goles | 1 | 2 |
| **Máximo por partido** | **10** | **20** |
