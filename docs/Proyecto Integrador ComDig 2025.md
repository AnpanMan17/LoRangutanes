---
title: Proyecto Integrador ComDig 2025

---

# Diseño del Codificador-Decodificador

Utilizando una Jupyter Notebook, implementar el codificador de la ecuación 1 propuesto en el paper de Vangelista y su correspondiente decodificador. El diseño debe permitir enviar una cantidad de bits múltiplo del Spreading Factor (SF). Estos bits tienen que ser aleatorios con una función de distribución de probabilidad uniforme. El script debe permitir imprimir una parte de los bits transmitidos y los bits decodificados. A la salida del decodificador se debe calcular e imprimir la probabilidad de error de bit (BER), entendiendose como la relación entre la cantidad de bits errados sobre la cantidad de bits enviados.

Utilizar una celda de la Jupyter Notebook para desarrollar la matematica y/o lógica utilizada en el algoritmo propuesto por ud.

**Test:** Si el codificador y decodificador se encuentran bien diseñados, bajo esta condición de funcionamiento debe dar un BER=0, cualquiera sea la cantidad de bits generados.


![Diseño del Codificador-Decodificador](images/design_encoder_decoder.png)

# Diseño del Waveform Former - n-Tuple former

Agregar a la Jupyter Notebook utilizada anteriormente, la implementación del waveform Former propuesto en la ecuación 2 del paper de Vangelista y su correspondiente n-Tuple Former descripto en la sección III. Con el agregado de esta etapa el diseño debe permitir enviar una cantidad de bits múltiplo del Spreading Factor (SF). El script debe permitir imprimir una parte de los símbolos transmitidos y los símbolos decodificados. A la salida del n-Tuple former se debe calcular e imprimir la probabilidad de error de símbolo (SER), entendiéndose como la relación entre la cantidad de símbolos errados sobre la cantidad de símbolos enviados. 

Utilizar una celda de la Jupyter Notebook para desarrollar la matematica y/o lógica utilizada en el algoritmo propuesto por ud.

**Test:** Si el Waveform Former y el n-Tuple Former se encuentran bien diseñados, bajo esta condición de funcionamiento debe dar un SER=0, cualquiera sea la cantidad de bits generados. 

![Diseño del Waveform Former - n-Tuple former](images/WaveformFormerDesign_nTupleFormer.png)

# Implementación del ruido del Canal

Incorporar en la Jupyter Notebook previamente utilizada la implementación del ruido AWGN (ruido aditivo blanco gaussiano) que introduce el canal de comunicaciones en la señal transmitida. Este ruido debe ser generado aleatoriamente con una distribución de probabilidad gaussiana de media cero y varianza $\sigma^2$.

La varianza $\sigma^2$ debe ser determinada a partir de la relación señal-ruido (SNR) expresada en decibeles ($SNR_{dB}$) seleccionada.

La notebook resultante debe ser capaz de reproducir la curva de BER correspondiente al escenario **Flat FSCM**, cuyos parámetros se detallan en la **Sección IV** del paper de referencia. Realizar también la curva de SER correspondiente.

Utilizar ademas una celda de la Jupyter Notebook para desarrollar la matematica, conceptualizar la teoría y/o lógica utilizada en el algoritmo propuesto por ud.

![Implementación del ruido del Canal](images/Channel_Noise_Implementation.png)

# Implementación de un canal selectivo en frecuencia

Incorporar en la Jupyter Notebook previamente utilizada la implementación del canal selectivo en frecuencia $h(nT) = \sqrt{0.8}\delta(nT) + \sqrt{0.2}\delta(nT - T)$ propuesto por Vangelista en el paper de referencia.

La notebook resultante debe ser capaz de reproducir la curva de BER correspondiente al escenario **Freq Sel FSCM**, cuyos parámetros se detallan en la **Sección IV** del paper de referencia. Realizar también la curva de SER correspondiente.

Utilizar ademas una celda de la Jupyter Notebook para desarrollar la matematica, conceptualizar la teoría y/o lógica utilizada en el algoritmo propuesto por ud.

![Implementación de un canal selectivo en frecuencia](images/Implementation_of_a_frequency_selective_channel.png)

# Implementación del sistema LoRa en el SDR

A partir del Paper de referencia "From Demodulation to Decoding: Toward Complete LoRa PHY Understanding and Implementation" implementar la transmisión de tramas LoRa en el transmisor

![Implementación del sistema LoRa en el SDR](images/Implementation_of_the_LoRa_system_in_the_SDR.png)

y las etapas de Dechirping, Window Alignment, Peak Merging y clock Recovery en el receptor 

![Implementación del sistema LoRa en el SDR](images/LoRa_demodulation_stages.png)

Probar el sistema futilizando en los SDRs para el envío de mensajes cortos.

Utilizar ademas una celda de la Jupyter Notebook para desarrollar la matematica, conceptualizar la teoría y/o lógica utilizada en el algoritmo propuesto por ud.

### **Nota:** Para optimizar el rendimiento de las etapas a diseñar utilizar los recursos brindados por la biblioteca numpy, evitando utilizar listas.