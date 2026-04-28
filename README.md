# 🎯 Marcador Rentoy

Marcador de puntos para el juego de cartas Rentoy.

## Uso

```bash
docker compose up -d
```

Accede a `http://TU_IP`.

## Construcción de la imagen

```bash
docker build -t f1rul4yx/marcador-rentoy:latest ./build
docker push f1rul4yx/marcador-rentoy:latest
```

## Comandos útiles

```bash
docker compose up -d      # Arrancar
docker compose down       # Parar
docker compose restart    # Reiniciar
```

## Funcionalidades

- Tablero de puntuación para dos jugadores
- Puntos objetivo configurables
- Botones +1, +3, -1, -3
- Undo/Redo con Ctrl+Z / Ctrl+Y
- Detección automática de ganador con confeti
- Historial de partidas (máximo 50) guardado en localStorage
- Diseño responsive

## Stack

HTML, CSS, JavaScript, Docker, Apache
