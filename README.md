# Poke-Randomizer

Generador de Pokémon aleatorio por generación. Consume la [PokéAPI](https://pokeapi.co/) para mostrar nombre, imagen, estadísticas base y grito de un Pokémon seleccionado al azar dentro del rango elegido.

🔗 **Demo en vivo:** [https://mackelf.github.io/Talento-digital/](https://mackelf.github.io/Talento-digital/)

---

## Características

- Generación aleatoria de Pokémon filtrada por generación (Gen I a Gen IX, o todas)
- Visualización de nombre, número y sprite oficial
- Tabla de estadísticas base con barras de progreso coloreadas por rango
- Reproductor de grito (cry) del Pokémon con animación de ondas
- Cache local con `localStorage` — evita peticiones repetidas a la API
- Carga inicial de los 1025 Pokémon en paralelo con indicador de progreso
- Diseño responsivo con Bootstrap 5

---

## Tecnologías

| Tecnología | Uso |
|---|---|
| Vue 3 (CDN) | Reactividad y lógica de la app |
| Bootstrap 5 | Estilos y layout |
| Bootstrap Icons | Icono del reproductor |
| PokéAPI | Fuente de datos |
| localStorage | Cache persistente entre sesiones |
| Vanilla CSS | Estilos custom (card Pokéball, barras, animaciones) |

---

## Estructura del proyecto

```
pkmnRandomizer/
└── index.html      # App completa (HTML + Vue + CSS)
```

---

## Instalación y uso local

```bash
# Clona el repositorio
git clone https://github.com/Mackelf/Talento-digital.git

# Entra a la carpeta
cd Talento-digital

# Abre index.html en el navegador
# No requiere npm ni servidor — funciona directo en el browser
```

---

## Cómo funciona el cache

En la primera visita, la app carga los datos de los 1025 Pokémon desde PokéAPI en paralelo y los guarda en `localStorage`. En visitas posteriores, lee directamente del cache sin hacer ninguna petición a la API.

Para forzar una recarga del cache, ejecuta en la consola del navegador:

```js
localStorage.removeItem('pokemonCache')
```

---

## Filtros de generación

| Botón | Rango de IDs |
|---|---|
| Gen I | 1 – 151 |
| Gen II | 152 – 251 |
| Gen III | 252 – 386 |
| Gen IV | 387 – 493 |
| Gen V | 494 – 649 |
| Gen VI | 650 – 721 |
| Gen VII | 722 – 809 |
| Gen VIII | 810 – 905 |
| Gen IX | 906 – 1025 |
| Todas | 1 – 1025 |

---

## Autor

**Mario** — [@Mackelf](https://github.com/Mackelf)  
Bootcamp Talento Digital / SENCE — Módulo Frontend
