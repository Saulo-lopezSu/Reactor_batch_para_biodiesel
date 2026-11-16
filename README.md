# Automatización de reactor batch para producción de biodiésel

Sistema de monitoreo y control basado en Arduino para un reactor batch de biodiésel. Desarrollado junto con alumnos de 6.º semestre de Ingeniería Química del TESJo.

<!--![Montaje del prototipo](imagenes/montaje.jpg)-->

## ¿Qué hace?
- Mide la temperatura del reactor y la muestra en una pantalla LCD.
- Controla la agitación mediante un driver de motor.
- Emite una alerta sonora con un buzzer [completar: ¿a qué temperatura o condición?].
- Envía los datos por puerto serial a Python, que grafica la temperatura en tiempo real.

## Hardware
| Componente | Uso |
|---|---|
| Arduino Uno | Control principal |
| Sensor de temperatura [modelo] | Medición de temperatura |
| Pantalla LCD 16x2 | Visualización local |
| Driver de motor [L298N u otro] | Control de agitación |
| Buzzer | Alertas |
| Costo aproximado | $3,000 MXN (electrónica y reactivos) |

## Software
- **Arduino (C++)**: lectura del sensor, control del motor, LCD y alarma. Carpeta `firmware/`.
- **Python**: lectura del puerto serial y gráfica en tiempo real con Matplotlib. Carpeta `python/`.

## Cómo usarlo
1. Arma el circuito según el esquema en `docs/esquema.png`.
2. Carga `firmware/reactor.ino` al Arduino desde el IDE.
3. Instala las dependencias: `pip install pyserial matplotlib`
4. Ejecuta `python python/temp.py` (ajusta el puerto COM en el script).

## Resultados
- [Completar: rango de temperatura alcanzado y estabilidad, ej. ± X °C]
- [Completar: número de lotes realizados y resultado obtenido]

<!--![Gráfica de temperatura en tiempo real](imagenes/grafica.jpg)-->

## Estructura del repositorio
```
├── firmware/    # Código Arduino
├── python/      # Script de monitoreo y gráfica
├── docs/        # Esquema del circuito
└── imagenes/    # Fotos y capturas
```

## Mi participación
Diseño del circuito, programación del firmware y script de monitoreo. Trabajo realizado junto con Pedro López.

## Autores
- Saulo González, [@Saulo-lopezSu](https://github.com/Saulo-lopezSu)
- Pedro López

## Licencia
[MIT](LICENSE)
