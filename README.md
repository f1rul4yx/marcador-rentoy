# marcador-rentoy

Marcador de puntos para el juego de cartas Rentoy.

## Qué es

Aplicación web estática para llevar la puntuación en partidas de Rentoy. Dos jugadores, puntos objetivo configurables, historial de hasta 50 partidas guardado en localStorage y detección automática de ganador con animación de confeti.

## Instalación

```bash
git clone https://github.com/f1rul4yx/marcador-rentoy.git
cd marcador-rentoy
```

No requiere configuración adicional.

## Uso

```bash
docker compose up -d
```

Accede a `http://TU_IP`. La aplicación se sirve en el puerto 80.

```bash
docker compose down       # Parar
docker compose restart    # Reiniciar
```

## Build

```bash
docker build -t f1rul4yx/marcador-rentoy:latest ./build
docker push f1rul4yx/marcador-rentoy:latest
```
