

Herramienta visual para planificar claims de terreno en servidores geopolíticos de Minecraft usando Dynmap.

Este programa no automatiza el comando `/f claim`.
Su función es ayudar a planificar el área a claimear y generar coordenadas donde el jugador debe pararse para ejecutar el claim manualmente.

---

## Requisitos

- Servidor con Dynmap
- Plugin de claims tipo Factions (`/f claim` por chunk)
- Processing o ejecutable del programa

---

## Flujo básico de uso (recomendado)

1. Abrir el programa
2. Anotar(En papel o block de notas) coordenadas en las que se incluye el área a claimear, revisar el dynmap. (Recomendado no usar areas grandes)
3. Escribir en el programa las coordenadas. Utilizar teclas 1 y 2(Cada una para ingresar cada par de coordenadas x,z) 
4. Subir recorte del mapa, en el que esté lo más preciso posible el área entre las dos coordenadas que anotaste. Tecla I para subir la imagen como archivo
5. Trazar línea, es continua y debe cerrarse como un polígono al finalizar de claimear el área
6. Exportar las coordenadas a un archivo de texto. Usar tecla S para subir al archivo points.txt
7. (IMPORTANTE Guardar el archivo point.txt en otro lugar, con otro nombre, se sobreescribe al usar de nuevo el programa)
8. Usar esas coordenadas dentro del servidor para claimear 

---

## Controles del programa

### Mouse
- Arrastrar el mouse: dibuja el trazo del área a claimear

### Teclado
- **C**  
  Limpia el trazo actual y permite empezar de nuevo.

- **S**  
  Exporta las coordenadas generadas a un archivo `points.txt`.

---

## Información mostrada en pantalla

- Coordenadas del mouse en píxeles
- Coordenadas del mundo (X, Z) correspondientes a la posición del mouse
- Visualización del área marcada por el usuario

El área dibujada es solo una referencia visual.
Las coordenadas exportadas corresponden al sistema real de coordenadas, es necesario ajustarlo dentro del código si se planea usar en un servidor distinto para el que fue desarrollado.

---

## Archivo de salida

El archivo `points.txt` contiene una lista de coordenadas X Z.

Ejemplo: 

43015 -73720
43031 -73720
43047 -73720


Cada línea representa un pixel en el programa y un bloque del mapa, corresponde a las coordenadas (x, z) donde el jugador debe pararse en el servidor.

---

## Uso en el servidor

1. Copiar una coordenada del archivo `points.txt`
2. Ir a esa posición en el juego (por ejemplo con `/tp`)
3. Ejecutar `/f claim`
4. Repetir el proceso para cada coordenada

---

## Limitaciones conocidas

- El programa no ejecuta comandos en el servidor
- No verifica si un chunk ya está claimeado
- La precisión depende de la estimación visual del usuario

---

## Licencia

MIT License
Metropolitan---Geopoliticos-Unidos

Herramienta para planificar claims en servidores geopolíticos usando Dynmap o parecidos.
