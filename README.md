# Lectura RFID entrada
_El proyecto tiene como fin crear un control de acceso a las oficinas de una empresa mediante la lectura de tarjetas RFID que serán previamente entregadas a los funcionarios para permitir su entrada al predio._
### Docentes:
- Lic. Ricardo Fabio
- Ing. Isaura Flores
### Grupo 1: 

- **Marcos Ibañez** - [MarcScript](https://github.com/MarcScript) 
- **Matias Berni** - [Bernimo](https://github.com/Bernimo) 
- **Franco Maidana** - [FrancoMaidana](https://github.com/FrancoMaidana)
- **Sebastián Chaparro** - [sebaschapa](https://github.com/sebaschapa)
### Entrega 09/04/2021
Se presentan el código básico de interacción con el sensor RFID en conjunto con el repositorio del proyecto en Github.
El funcionamiendo del codigo es el siguiente:<br />
El codigo primeramente importa una directiva para que el terminal interprete que se trata del script de python, seguidamente se importan la librerias:<br />
- GPIO<br />
- mcrf522<br />
- SimpleMCRF522<br />
La libreria GPIO es utilizada para manejar la interaccion de los pines del Raspberry Pi con el modulo RFID. Las librerias mcrf522 y SimpleMCRF522 son utilizadas para las funciones de comunicacion del RFID con el arduino.<br />
Seguidamente el codigo crea el objeto "usuario" al que utilizara para almacenar los parametros de lectura del tag.<br />
Luego el bloque try del script se encarga de ejecutar la secuencia de lectura para capturar la informacion que rebica del tag en caso de que éste se presente, y sino, se encarga de manejar las excepciones que puedan ocurrir.<br />
La lectura del objeto usuario se guarda en la variable UUID y se imprime.<br />
La instruccion "finally" se encarga de manejar que la situacion de la secuencia posterior de codigo se ejecute por defecto, ocurra o no la excepcion del bloque try.<br />
Finalmente se limpian el registro de entradas/salidas de por la instruccion GPIO.cleanup() para prevenir posibles errores que se ocasionen por la ejecucion de otros scripts.<br />
### Construido con 🛠️
* [Python](https://www.python.org/downloads/windows/) - Lenguaje de programación para interacción con la BD y sensores.
* [Raspbian](https://www.raspberrypi.org/software/operating-systems/) - Sistema Operativo del Raspberry.
* [PostgreSQL](https://www.postgresql.org/) - Gestor de la BD.

