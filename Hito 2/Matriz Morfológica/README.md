<img width="1920" height="1080" alt="7" src="https://github.com/user-attachments/assets/f3a75583-2600-473d-b569-157c2768920e" />
<img width="1920" height="1080" alt="8" src="https://github.com/user-attachments/assets/54ab980b-b379-41fe-ad29-e95ab25382eb" />
<img width="1920" height="1080" alt="9" src="https://github.com/user-attachments/assets/8275566b-3cc9-47a4-95cf-ba01eda065e8" />
<img width="1920" height="1080" alt="10" src="https://github.com/user-attachments/assets/3fc571e9-697d-48cb-8b41-de7266ee1eb5" />
<img width="1920" height="1080" alt="11" src="https://github.com/user-attachments/assets/2ece9530-de10-4dfc-b742-1f9a0a9e435a" />

## I. Proteger el sistema:
Regulador de voltaje: transforma un voltaje de entrada directo continuo e inestable en una salida constante y perfectamente regulada de 5V DC. Garantiza un suministro eléctrico seguro y libre de fluctuaciones para las etapas lógicas, sensores y el microcontrolador del dispositivo, pero disipa el excedente de tensión en forma de calor, lo que demanda un diseño con disipación térmica adecuada si la corriente de trabajo es elevada.

Capacitores de desacoplo: Componentes pasivos almacenadores de energía colocados en paralelo que actúan como filtros locales para suprimir el rizado de baja frecuencia y el ruido transitorio de alta frecuencia en la línea de alimentación. Aseguran la estabilidad operativa del regulador de voltaje y evitar reinicios inesperados en el sistema lógico, pero exigen una disposición física estricta en el PCB, debiendo soldarse lo más cerca posible a los pines del circuito integrado para no perder su efectividad.

Filtro pasivo: Una red eléctrica RC en cascada diseñada para atenuar de forma selectiva las interferencias electromagnéticas y ruidos falsos de alta frecuencia presentes en la etapa de acondicionamiento. Permite purificar y estabilizar la señal de manera muy económica y sencilla sin necesidad de alimentación externa, pero introduce una ligera atenuación en la amplitud y requiere un cálculo matemático preciso de su frecuencia de corte para evitar el desfase o la pérdida de datos en la banda de interés.

## II. Almacenar Energía del Sistema:
Batería de Litio: Celda electroquímica recargable de alta densidad energética y bajo peso, que mantiene un suministro de voltaje muy estable durante la mayor parte de su operación y soporta cientos de ciclos de uso. Ofrece una excelente autonomía en un formato compacto ideal para sistemas portátiles, pero requiere obligatoriamente un circuito de protección (BMS) para evitar sobrecargas, descargas profundas o riesgos de inestabilidad térmica.
Batería Recargable:
Batería alcalina: Una fuente de energía química primaria no recargable que utiliza una reacción de zinc y dióxido de manganeso para entregar un voltaje nominal directo listo para su uso inmediato en el circuito. Sin embargo, posee una densidad energética muy baja frente a consumos moderados-altos, lo que provoca una caída de voltaje progresiva durante su uso, un costo operativo elevado a largo plazo y un fuerte impacto ambiental debido a la necesidad de desechar y reemplazar constantemente el componente.

## III. Permitir/Impedir Energía al Sistema:

Interruptor pulsador led: Una variante que integra retroalimentación luminosa en el mismo cuerpo del botón, ofreciendo una confirmación visual inmediata del estado de encendido (ON/OFF) del dispositivo, incluso en entornos con poca luz. Aunque requiere un cableado adicional para la alimentación del LED.

Interruptor pulsador: Un mecanismo de activación por presión directa que destaca por su diseño compacto y plano, lo que simplifica su integración y facilita la desinfección de la superficie. Sin embargo, carece de una señal visual evidente sobre su estado mecánico a simple vista.

Interruptor basculante: Un interruptor físico de palanca que ofrece la opción más intuitiva, con un estado visible de ON/OFF que minimiza los errores de operación del personal. Pero demanda cuidar la estanqueidad de la ranura y un plan de limpieza más meticuloso.

## IV. Iniciación/Finalización de Fases:

Interruptor pulsador led: Una variante que integra retroalimentación luminosa en el mismo cuerpo del botón, ofreciendo una confirmación visual inmediata del estado de encendido (ON/OFF) del dispositivo, incluso en entornos con poca luz. Aunque requiere un cableado adicional para la alimentación del LED.

Interruptor pulsador: Un mecanismo de activación por presión directa que destaca por su diseño compacto y plano, lo que simplifica su integración y facilita la desinfección de la superficie. Sin embargo, carece de una señal visual evidente sobre su estado mecánico a simple vista.

Interruptor basculante: Un interruptor físico de palanca que ofrece la opción más intuitiva, con un estado visible de ON/OFF que minimiza los errores de operación del personal. Pero demanda cuidar la estanqueidad de la ranura y un plan de limpieza más meticuloso.

## V. Medir Señal Eléctrica del Músculo: 
Microcontrolador con electrodos externos: Conexión mediante cables largos. Permite medir cualquier músculo por más lejano que esté, pero los cables captan mucho ruido e interferencias por movimiento.
Microcontrolador con electrodos internos: Electrodos acoplados directo a la placa. Elimina el ruido por cables y es muy compacto, pero obliga a colocar todo el circuito sobre un solo músculo.

## VI. Medir Rotación y Aceleración de la Extremidad:
Sensor IMU 3 ejes: Módulo que mide la aceleración lineal tridimensional. Es muy económico y eficiente para inclinaciones o movimientos simples, pero es incapaz de registrar la velocidad de rotación angular.
Sensor IMU 6 Ejes: Chip que integra acelerómetro y giroscopio tridimensionales. Ofrece un seguimiento de movimiento completo y preciso en tiempo real, pero es más costoso y complejo de programar.

## VII. Filtración de Datos:
Filtro Notch: Atenúa una frecuencia muy estrecha . Elimina por completo el ruido de la red eléctrica sin alterar la señal, pero es inútil contra interferencias fuera de ese punto exacto.

Filtro pass-band Butterworth: Deja pasar solo el rango de frecuencias útiles del músculo. Aísla la señal limpia eliminando ruidos bajos y altos a la vez, pero requiere circuitos más complejos de diseñar.

## VIII. Transmisión/Recepción de Datos:
Módulo Bluetooth: Transmisión inalámbrica de datos. Ofrece total movilidad y conectividad sin cables, pero consume más energía y es propenso a interferencias.
Módulo HUB I2C Qwiic: Expansión de puertos plug-and-play. Conecta múltiples sensores en cadena rápida y sin soldaduras, pero añade hardware y espacio al diseño.
I2C: Protocolo de comunicación por bus a dos líneas de datos. Permite controlar decenas de dispositivos usando solo dos pines, pero es lento y limitado a distancias cortas.

## IX. Medir Frecuencia Mecánica:
Vibración por contacto: Sensor que detecta oscilaciones mecánicas por contacto físico directo con la superficie. Ofrece una respuesta digital rápida y económica ante movimientos, pero no cuantifica la magnitud exacta ni la frecuencia de la señal.

Vibración por choque/resorte: Interruptor electromecánico que cierra el circuito cuando un resorte interno se mueve por un impacto. Es sumamente barato y simple de implementar como activador, pero es muy impreciso y sufre de rebote mecánico.

Acelerómetro:Sensor digital MEMS que mide la aceleración tridimensional en los ejes X, Y y Z. Permite calcular con alta precisión matemática la frecuencia y la fuerza real del movimiento, pero exige un procesamiento lógico de datos más complejo.

## X. Determinar Tiempo de Vibración:

Codificador Rotatorio: Sensor digital de giro infinito que entrega pulsos lógicos. Permite ajustar tiempos con precisión exacta y sin derivaciones analógicas, pero requiere una programación más compleja por código.

Potenciómetro: Resistencia variable analógica que modifica el voltaje según su giro de perilla. Es muy barato y fácil de leer mediante un pin ADC, pero tiene un giro limitado y sufre desgaste mecánico.

## XI. Generar Frecuencia Mecánica:

Sistema Basado en Chip: Plataforma potente con conectividad inalámbrica nativa. Ofrece procesamiento rápido y control preciso de señales, pero consume más energía y su programación es más compleja.

Tarjeta Basada en Microcontrolador: Placa de desarrollo con pines accesibles y reguladores integrados. Facilita un prototipado rápido y robusto sin soldaduras, pero su tamaño físico es muy voluminoso.

Microcontrolador: Chip de formato mínimo dedicado a control lógico básico. Brinda tamaño ultra reducido y consumo mínimo ideal para portabilidad, pero tiene menos pines disponibles.

## XII. Inicio/Fin Temporizador:
Sistema Basado en Chip: Plataforma potente con conectividad inalámbrica nativa. Ofrece procesamiento rápido y control preciso de señales, pero consume más energía y su programación es más compleja.

Tarjeta Basada en Microcontrolador: Placa de desarrollo con pines accesibles y reguladores integrados. Facilita un prototipado rápido y robusto sin soldaduras, pero su tamaño físico es muy voluminoso.

Microcontrolador: Chip de formato mínimo dedicado a control lógico básico. Brinda tamaño ultra reducido y consumo mínimo ideal para portabilidad, pero tiene menos pines disponibles.

## XIII. Emitir frecuencia mecánica:
Motores LRA: Actuador magnético que vibra linealmente mediante una masa y un resorte. Ofrece una respuesta háptica ultra rápida, precisa y de bajo consumo, pero trabaja eficientemente solo en su frecuencia de resonancia fija y requiere un chip driver especial.
Actuador piezoeléctrico: Elemento cerámico que se deforma mecánicamente al aplicarle un campo eléctrico. Brinda la velocidad de respuesta más rápida y un control de frecuencia ultra preciso, pero requiere voltajes de activación elevados y su desplazamiento físico es microscópico.
Motor de vibración ERM: Motor DC tradicional con una masa excéntrica acoplada a su eje. Es sumamente barato, comercial y fácil de activar con simple voltaje continuo, pero la frecuencia y la fuerza están ligadas.

## XIV. Análisis de datos:

Sistema Basado en Chip: Plataforma potente con conectividad inalámbrica nativa. Ofrece procesamiento rápido y control preciso de señales, pero consume más energía y su programación es más compleja.

Tarjeta Basada en Microcontrolador: Placa de desarrollo con pines accesibles y reguladores integrados. Facilita un prototipado rápido y robusto sin soldaduras, pero su tamaño físico es muy voluminoso.

Microcontrolador: Chip de formato mínimo dedicado a control lógico básico. Brinda tamaño ultra reducido y consumo mínimo ideal para portabilidad, pero tiene menos pines disponibles.

## XV. Visualización de Datos:

Pantalla OLED: Módulo gráfico de alta nitidez y bajo consumo. Permite mostrar gráficos avanzados en poco espacio, pero es pequeña y sufre desgaste de píxeles.
Aplicación, Creación Propia: Interfaz de software en móvil o PC. Ofrece funciones interactivas infinitas y registro de datos, pero depende de un equipo externo y programación compleja.

Pantalla LCD: Pantalla tradicional para caracteres básicos. Es muy barata, robusta y fácil de usar, pero es voluminosa y está limitada sólo a texto estático.

# XVI. Mostrar Inicio/Fin Fase:

Interruptor pulsador led: Una variante que integra retroalimentación luminosa en el mismo cuerpo del botón, ofreciendo una confirmación visual inmediata del estado de encendido (ON/OFF) del dispositivo, incluso en entornos con poca luz. Aunque requiere un cableado adicional para la alimentación del LED.

Interruptor pulsador: Un mecanismo de activación por presión directa que destaca por su diseño compacto y plano, lo que simplifica su integración y facilita la desinfección de la superficie. Sin embargo, carece de una señal visual evidente sobre su estado mecánico a simple vista.

Interruptor basculante: Un interruptor físico de palanca que ofrece la opción más intuitiva, con un estado visible de ON/OFF que minimiza los errores de operación del personal. Pero demanda cuidar la estanqueidad de la ranura y un plan de limpieza más meticuloso.


