## BLAX BOX
<img width="1077" height="611" alt="Caja negra" src="https://github.com/user-attachments/assets/f764e7cd-c532-4c73-b477-6cbe55b68834" />


## SECUENCIA DE OPERACIONES

### Fase de Inicialización 
Conecte el cable de alimentación a un tomacorriente. Verifique que la señal visual de activación esté encendida en el chasis del dispositivo.
Presione el interruptor físico. Este comando dispara la rutina de autodiagnóstico y establece el enlace con la estación de control (PC).
El sistema ejecutará una toma de datos iniciales para registrar la actividad bioeléctrica basal y el ángulo articular en flexión y extensión durante 10 segundos antes de la estimulación.
La aplicación notificará al terapeuta/usuario que el sistema ha alcanzado las condiciones óptimas para iniciar la Fase 1.
### Fase 1: Terapia de Neuromodulación
Coloque el cabezal de tratamiento sobre el Bíceps braquial.
Presione el interruptor de activación para dar inicio a la emisión de estímulos. El prototipo comenzará a vibrar a una frecuencia constante de 40 Hz, durante 20 minutos.
Una vez transcurrido el tiempo programado, se activará una señal visual de indicador de fin de terapia. En este instante, el sistema desenergizará automáticamente los actuadores de vibración por seguridad.
### Fase 2: Evaluación Post-Terapia y Análisis
Tras un breve lapso de reposo posterior al apagado de los estímulos, el sistema iniciará automáticamente la Fase 2.
El usuario deberá flexionar y extender el brazo para la toma de datos finales. Los sensores capturarán la respuesta dinámica post-estimulación para cuantificar la mejora en el rango de movimiento y la reducción de la espasticidad.
La información recolectada (sEMG e inercial) será transmitida en tiempo real hacia la PC para su almacenamiento en la base de datos local.
Los registros guardados serán procesados mediante algoritmos de Machine Learning
### Apagado y Mantenimiento
Una vez confirmada la carga de datos, desconecte el equipo del tomacorriente.
Limpie el cabezal de contacto con un paño humedecido en alcohol isopropílico.



## ESTRUCTURA DE FUNCIONES
<img width="3449" height="1523" alt="Esquema de funciones" src="https://github.com/user-attachments/assets/aa5da035-1881-491f-807f-b20aae2c4be1" />
