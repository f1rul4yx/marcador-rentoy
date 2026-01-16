# Marcador Rentoy

Aplicación web para anotar los puntos del juego de cartas Rentoy.

## Características

- **Tablero de puntuación interactivo** para dos jugadores
- **Configuración flexible**: nombres de jugadores y puntos objetivo personalizables
- **Botones de puntuación**: +1, +3, -1, -3 puntos
- **Sistema Undo/Redo** con soporte para atajos de teclado (Ctrl+Z, Ctrl+Y)
- **Detección automática de ganador** con animación de confeti
- **Historial de partidas** guardado localmente (máximo 50 partidas)
- **Persistencia de datos**: auto-guarda al cambiar de pestaña o cerrar el navegador
- **Diseño responsive**: adaptado para móvil y desktop

## Tecnologías

- HTML5
- CSS3 (animaciones, gradientes, glassmorphism)
- JavaScript Vanilla (ES6+)
- Docker + Apache 2

## Estructura del Proyecto

```
marcador-rentoy/
├── build/
│   ├── Dockerfile
│   └── app/
│       └── index.html
├── docker-compose.yaml
└── README.md
```

## Instalación y Uso

### Opción 1: Ejecución directa

Abre el archivo `build/app/index.html` en tu navegador.

### Opción 2: Con Docker Compose (recomendado)

```bash
docker-compose up -d
```

La aplicación estará disponible en http://localhost

### Opción 3: Con Docker

```bash
# Usando la imagen de Docker Hub
docker run -d -p 80:80 f1rul4yx/marcador-rentoy:1.0

# O construir la imagen localmente
docker build -f build/Dockerfile -t marcador-rentoy build/
docker run -d -p 80:80 marcador-rentoy
```

## Uso de la Aplicación

1. **Pantalla de configuración**: Ingresa los nombres de los jugadores y los puntos necesarios para ganar
2. **Pantalla de juego**: Usa los botones para sumar o restar puntos a cada jugador
3. **Ganador**: Cuando un jugador alcanza los puntos objetivo, aparece la pantalla de victoria
4. **Historial**: Consulta las partidas anteriores desde el botón de historial

## Atajos de Teclado

| Atajo | Acción |
|-------|--------|
| `Ctrl+Z` | Deshacer último movimiento |
| `Ctrl+Y` | Rehacer movimiento |

## Almacenamiento Local

La aplicación guarda los datos en el navegador usando localStorage:

- `rentoy_gameState`: Estado actual de la partida
- `rentoy_matchHistory`: Historial de partidas

## Licencia

Este proyecto es de uso libre.
