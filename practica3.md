Laboratorio de Comunicaciones
## Universidad Industrial de Santander

# Práctica 5. Modulaciones lineales

### Integrantes
- **Duban Andretti Gutierrez Leon** - 2220396
- **Juan José De la Rosa Medina** - 2202810

Escuela de Ingenierías Eléctrica, Electrónica y de Telecomunicaciones  
Universidad Industrial de Santander

  
### 1. Primera fase:  

---

| Casos         | Potencia de la señal portadora (nW) | Potencia de la banda lateral superior (nW) | Potencia de la banda lateral inferior (nW) | Índice de modulación | Frecuencia del mensaje (kHz) | Relación señal a ruido (dB) |
|---------------|-------------------------------------|--------------------------------------------|--------------------------------------------|------------------------|-------------------------------|------------------------------|
| ka*Ac = 1     | 55.67                              | 16.12                                     | 16.12                                     | 0.846                 | 11.7                          | 60.3                         |
| Ka*Ac < 1     | 47.23                              | 255.47                                    | 255.47                                    | 0.29                  | 11.7                          | 55.4                         |
| Ka*Ac > 1     | 45.37                              | 1.01                                      | 1.01                                      | 3.89                  | 11.7                          | 58.8                         |

---

## MEDICIONES  

### 1. Caso 1: KaAc = 1: (Modulación)

**Fig. 1. Simulación caso 1.**  

<img src="https://github.com/user-attachments/assets/9404d6da-4569-45bb-973c-0609cf7895bd" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

**Fig. 2. Espectro visto en el analizador de espectros.**  

<img src="https://github.com/user-attachments/assets/3499f2de-b518-495e-9124-78e02c170d5d" title="Simulación" alt="Texto alternativo" width="600" height="400"/>


En esta configuración se observa una modulación balanceada, donde la potencia de la portadora (55.67 nW) es comparable a la suma de las bandas laterales (16.12 + 16.12 = 32.24 nW). El índice de modulación de 0.846 indica una modulación cercana a la ideal (AM estándar). En el dominio de la frecuencia se distinguen claramente las tres componentes (portadora y dos bandas laterales) y en el dominio del tiempo se visualiza una señal modulada simétrica. La relación señal a ruido es alta (60.3 dB), lo que evidencia buena calidad de transmisión sin distorsión significativa.

- Potencias laterales: Dentro de nuestro informe se pudo observar unas potencias laterales iguales, esto se espera dentro de una modulación balanceada.  
- Índice ≈ 0.85 indica una modulación muy cercana al ideal de 1, pero aún segura. Por eso, en ese caso se obtuvo la mayor relación señal a ruido (60.3 dB) y una distribución de potencia equilibrada entre portadora y bandas laterales.  
- Se alcanza la mejor relación señal a ruido del experimento (60.3 dB), lo que implica una señal limpia y de alta calidad.

---

### 2. Caso 2: KaAc < 1: (Modulación crítica)

- El índice de modulación es muy bajo (0.29), indicando submodulación, lo que puede llevar a una señal con muy poca variación en la envolvente y una mala representación del mensaje.  
- Las potencias de las bandas laterales (255.47 nW cada una) son mucho mayores que la de la portadora (47.23 nW), lo cual no es característico de AM convencional. Esto puede indicar una anomalía o un comportamiento no lineal.  
- La relación señal a ruido disminuye a 55.4 dB, sugiriendo que, aunque hay mucha energía en las bandas laterales, no se traduce en una señal eficiente ni limpia.

**Fig. 3. Simulación caso 2.**  

<img src="https://github.com/user-attachments/assets/ea35819e-b3f6-4261-890d-0500d7ef510a" title="Simulación" alt="Texto alternativo" width="600" height="400"/>


**Fig. 4. Espectro visto en el analizador de espectros.**  

<img src="https://github.com/user-attachments/assets/e5b2d9ff-ce8d-4f68-a0e5-90b65d6bb11f" title="Simulación" alt="Texto alternativo" width="600" height="400"/>


---

### 3. Caso 3: KaAc > 1: (Sobre-modulación)

- El índice de modulación es muy superior a 1 (3.89), lo que implica sobremodulación, generando distorsión en la envolvente. Esto impide la correcta demodulación por envolvente.  
- Las bandas laterales tienen potencia extremadamente baja (1.01 nW cada una), lo que indica una pérdida de información útil, a pesar del índice alto.  
- Aunque el SNR se mantiene relativamente alto (58.8 dB), la calidad de la señal se ve afectada por la distorsión, y puede no representar fielmente el mensaje original.

**Fig. 5. Simulación caso 3.**  
<img src="https://github.com/user-attachments/assets/dd8ba434-acc2-48d0-8af4-99a17508e8c3" title="Simulación" alt="Texto alternativo" width="600" height="400"/>


**Fig. 6. Espectro visto en el analizador de espectros.**  
<img src="https://github.com/user-attachments/assets/fc6cc915-9f4e-4a8d-a94b-114d832b5080" title="Simulación" alt="Texto alternativo" width="600" height="400"/>


---

En este caso, el índice de modulación es 3.89, indicando sobremodulación, donde la señal del mensaje supera a la portadora. La portadora (45.37 nW) sigue siendo la mayor componente, pero las bandas laterales han caído considerablemente (1.01 nW cada una), mostrando que la señal está distorsionada. El espectro muestra una forma más achatada y desbalanceada, lo que suele dificultar la demodulación. A pesar de esto, la relación señal a ruido es de 58.8 dB.


# Fase 2

En esta fase se buscó analizar los tipos de modulación de una señal variando los valores del coeficiente Ka y la amplitud del mensaje, hasta obtener una señal modulada, una sobre-modulada y otra modulada al 100%.  

---

### Tabla 1. Valores Obtenidos para cada caso

| Ka\*Am | Amplitud De La Señal Portadora [V] | Amplitud Del Mensaje [V] | Potencia De La Señal [W] | índice De Modulación | Frecuencia Del Mensaje [Hz] |
|--------|-------------------------------------|----------------------------|----------------------------|------------------------|------------------------------|
| 1      | 0.22                                | 1                          | 0.041                      | -6.021                 | 952.38                       |
| 4      | 0.11                                | 2                          | 0.03                       | 4.082                  | 990.09                       |
| 0.25   | 0.3                                 | 0.5                        | 0.041                      | -7.96                  | 980.39                       |

---

## Caso 1: ka\*ma = 1

Para obtener el valor de la condición dada donde se genera una modulación al 100%, se estableció un valor de ka =1 y ma=1, con esto se logra ver en la simulación del flujograma y en el osciloscopio como la señal queda envuelta en su totalidad por la señal moduladora.

**Figura 1. Simulación de la señal modulada al 100%.**  
<img src="https://github.com/user-attachments/assets/3d63dacb-b67f-4857-9442-4075ccf56663" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

**Figura 2. Señal modulada al 100% obtenida en el osciloscopio.**  
<img src="https://github.com/user-attachments/assets/29ca098a-7459-48a9-a3ef-525937f185d2" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

De los datos obtenidos en el osciloscopio y en la tabla se aproxima a una modulación del 100% (m = 1). Sin embargo, el índice de modulación expresado en dB nos dice que no se logra alcanzar dicho valor de manera adecuada. Una modulación del 100% debería poseer un valor de 0 dB, pero para este caso de estudio no ocurre esto.

---

## Caso 2: ka\*ma > 1

Para obtener el valor de la condición dada donde se genera una sobre-modulación, se estableció un valor de ka =2 y ma=2, con esto se logra ver en la simulación del flujograma y en el osciloscopio como la señal queda distorsionada en sus picos.

**Figura 3. Simulación de una señal sobre-modulada.**  
<img src="https://github.com/user-attachments/assets/b6405bdd-4842-42e8-8593-4a9f285d8621" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

**Figura 4. Señal sobre-modulada obtenida en el osciloscopio.**  
<img src="https://github.com/user-attachments/assets/c36073dd-f607-40df-97e1-413c3d6074e9" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

Para el caso de la sobre-modulación, índice de modulación es mayor al de una modulación al 100%, debido a que esté es mayor que 1, lo cual se refleja en un valor positivo obtenido en la tabla en dB. Se observa como en el osciloscopio la señal pierde información, la envolvente se deforma y se genera una saturación en ambos picos.

---

## Caso 3: ka\*ma < 1

Para obtener el valor de la condición dada donde se genera una modulación, se estableció un valor de ka =0.5 y ma=0.5, con esto se logra ver en la simulación del flujograma y en el osciloscopio como la señal se reduce y comprime a lo largo del tiempo.

**Figura 5. Simulación para una señal modulada.**  
<img src="https://github.com/user-attachments/assets/26ca9941-421e-4f2d-9b4a-d486f00118bc" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

**Figura 6. Señal modulada obtenida en el osciloscopio.**  
<img src="https://github.com/user-attachments/assets/7703b693-22f9-4753-8311-361aa99a6bda" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

En este caso se generó una modulación con un índice menor a 1, el valor en dB indica un m aproximado de 0.4. En este tipo de modulaciones predomina la señal portadora y la envolvente casi no la modula, así como se puede observar en el osciloscopio. Para este tipo de modulaciones se desperdicia mucha potencia en la portadora y se transmite muy poca información.

---


# Fase 3

## Laboratorio comunicaciones  
### Tercera fase

---

● Caso 1:  
Parámetros asignados: 

● Índice de modulación: 75%  
● Frecuencia de portadora: 100 MHz  
● Ganancia TX: 10 dB  
● Muestras por símbolo: 10  

Comportamiento esperado: Cuando el índice de modulación m = 0.75, la 
envolvente de la señal modulada no debe tocar el eje cero. Eso significa que la 
portadora sigue predominando y que la señal modulada no presenta 
sobre-modulación.  
Nuestra simulación nos confirmó que la señal fue correctamente escalada y 
centrada para producir una modulación AM con índice 0.75. No hubo pérdida de 
información, y la señal modulada mantuvo su forma bien definida. El uso de una 
portadora de 100 MHz asegura que la modulación está en una banda alta.

<img src="https://github.com/user-attachments/assets/65f0fdb8-875d-4c40-806a-b288c45c638e" title="Simulación" alt="Texto alternativo" width="600" height="400"/>


De la grafica inferior (Dominio de la frecuencia) se pudo observar que este espectro 
concuerda perfectamente con una modulación AM con índice de 0.75. La presencia 
de lóbulos simétricos indicó una señal de doble banda lateral (DSB-AM), y la 
proporción entre los lóbulos y la portadora confirma que la información del mensaje 
está correctamente distribuida en frecuencia. 

<img src="https://github.com/user-attachments/assets/018d23d6-9784-45bf-a145-2d93203f05ff" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

Este comportamiento indicó una modulación AM correctamente implementada, sin 
saturación ni pérdida de información. La ganancia TX de 10 dB es adecuada para 
mantener la forma de la señal sin introducir distorsiones no lineales.  

Para verificar el índice de modulación se utilizó la siguiente fórmula:  
𝑚 = 𝐴𝑚á𝑥 − 𝐴𝑚í𝑛 / 𝐴𝑚á𝑥 + 𝐴𝑚í𝑛  
𝑚 = 141.8 − 8.594 / 141.8 + 8.594 = 0.886

Aunque el valor teórico asignado era del 75%, al usar los datos medidos 
directamente por el osciloscopio, el índice real está ligeramente por encima, esto no 
representa sobre-modulación entonces la señal siguió siendo válida. 

---

● Caso 2:  

Parámetros asignados:  

● Índice de modulación: 100%  
● Frecuencia de portadora: 250 MHz  
● Ganancia TX: 15 dB  
● Muestras por símbolo: 5  

<img src="https://github.com/user-attachments/assets/43f1ecd5-6f52-43ea-a61b-bf8f9c679a9a" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

En esta imagen se observó una señal modulada en amplitud cuya envolvente 
variaba significativamente, lo cual coincidió con un coeficiente de modulación de ka 
igual a 1. La amplitud de la señal modulada fluctuó entre valores cercanos a cero y 
un máximo aproximado de 0.25, tal como se esperaba teóricamente considerando 
una amplitud de portadora de 0.125. En la parte superior del gráfico, la señal digital 
moduladora alteró directamente la envolvente de la portadora, generando 
segmentos donde la señal prácticamente desaparecía, lo que indicó una modulación 
profunda. En el dominio de frecuencia, se identificó una portadora clara centrada en 
250 MHz y bandas laterales bien definidas, características de una modulación en 
doble banda lateral. 

<img src="https://github.com/user-attachments/assets/65e91ebe-20a9-4276-81c0-76fd97d9a7bb" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

Se confirmó visualmente el comportamiento esperado de la señal modulada. Se 
identificaron zonas donde la envolvente se acercaba al eje horizontal, indicando los 
valores mínimos de la señal moduladora, y por lo tanto, una casi anulación de la 
portadora. En contraste, los segmentos de mayor grosor representaron los valores 
máximos de modulación, con amplitudes cercanas a los 141.8 milivoltios. Esta 
variación, que osciló desde 8.6 milivoltios hasta 141.8 milivoltios, evidenció una 
modulación con alta profundidad y concordancia entre el comportamiento físico 
observado y el análisis teórico.  

---

● Caso 3:  

Parámetros asignados:  

● Índice de modulación: 150%  
● Frecuencia de portadora: 150 MHz  
● Ganancia TX: 20 dB  
● Muestras por símbolo: 20  

<img src="https://github.com/user-attachments/assets/69e04ef1-7f1c-4a8e-aaed-9293edcb4753" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

Se utilizó un coeficiente de modulación ka de 1.5, una frecuencia portadora de 150 
MHz, una ganancia de transmisión de 20.0, y se definieron 20 muestras por 
símbolo. Estos parámetros provocaron una modulación en amplitud más intensa que 
en los casos anteriores, lo cual se reflejó en la envolvente de la señal. La amplitud 
portadora se mantuvo en 0.125, y como resultado, la amplitud modulada osciló entre 
aproximadamente ±0.3. El espectro en frecuencia mostró una mayor densidad de 
componentes, con lóbulos laterales claramente visibles debido a la alta cantidad de 
muestras por símbolo y el mayor valor de ka, lo que generó un mayor contenido 
armónico alrededor de la portadora.

<img src="https://github.com/user-attachments/assets/161aaae0-6f5c-4b04-9bab-dba1b50b4b68" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

En el osciloscopio se midió una señal con una amplitud máxima de 
aproximadamente 357.72 mV y mínima de -622 mV, lo que resultó en un valor pico a 
pico de 396.04 mV, el mayor entre los tres casos. El tiempo base fue de 50 µs/div, y 
la resolución temporal permitió observar una forma de onda bien definida, con 
cambios bruscos entre niveles altos y bajos. El aumento del valor de ka y la 
ganancia TX produjo una señal más extensa en el dominio del voltaje, lo que facilitó 
su visualización y análisis. Además, los datos del osciloscopio reflejaron una 
modulación más profunda y simétrica, indicando un uso más eficiente del rango 
dinámico del canal de transmisión  

<img src="https://github.com/user-attachments/assets/df1ac80a-1de7-424c-8b02-2bd3d5ba1509" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

Se observó un pico principal en 0 dBm, correspondiente a la frecuencia portadora, y 
lóbulos laterales que decrecieron hasta aproximadamente -80 dBm, lo que indicó 
una modulación en amplitud leve debido al bajo coeficiente de modulación ka y una 
amplitud portadora pequeña. Esto confirmó que la señal transmitida tenía un 
contenido espectral concentrado y una modulación poco profunda.  

<img src="https://github.com/user-attachments/assets/e0a84713-471a-47f9-8863-55085506667e" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

El pico principal de la señal alcanzó los 0 dBm, y se evidenció un espectro más 
amplio y con lóbulos laterales más marcados que en el caso anterior. Esto se debió 
a un coeficiente de modulación Ka más alto y una mayor amplitud portadora, lo cual 
generó una señal más modulada y con mayor dispersión de energía en frecuencia.  


El ancho de banda ocupado se extendió de aproximadamente 249 MHz a 251 MHz, 
lo que confirmó una modulación en amplitud más intensa. Los lóbulos laterales se 
distribuyeron con simetría y se atenuaron progresivamente hasta valores cercanos a 
-80 dBm. En comparación con el caso 1, esta configuración resultó en una señal con 
mayor contenido espectral, lo que indicó una mayor eficiencia en la transmisión de 
información, aunque también con mayor posibilidad de interferencia.  

<img src="https://github.com/user-attachments/assets/df50769e-f057-4b14-8b4f-73c99dd5c129" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

La imagen del analizador de espectro mostró una señal centrada en los 150 MHz 
con un span de 2 MHz. El pico de la señal se mantuvo en 0 dBm, pero a diferencia 
de los casos anteriores, el espectro presentó un patrón más simétrico y denso, con 
lóbulos laterales claramente definidos y una mayor concentración de energía en 
torno a la frecuencia central. La caída de los lóbulos se observó más gradual, 
descendiendo hasta cerca de -90 dBm, lo que indicó una buena eficiencia espectral 
y una menor dispersión fuera de banda.  

El comportamiento de esta señal se atribuyó a un coeficiente Ka intermedio (1.5), 
una amplitud portadora baja (0.1250) y una frecuencia de 150 MHz. Estos 
parámetros provocaron una modulación en amplitud que mantuvo la potencia 
centrada, pero con una leve expansión del espectro respecto al caso 1. En 
comparación, la señal fue más robusta y estable, con un balance adecuado entre 
eficiencia y control del ancho de banda ocupado, lo que la hizo óptima para 
transmisión sin interferencias excesivas.  

---

## FASE 4


En esta fase se busca analizar el comportamiento de una señal portadora ante diferentes tipos de modulaciones, a continuación, se estudia cada caso y su comportamiento en el osciloscopio como en el analizador de espectros.

---

### Caso 1: Genere una Señal modulada en 60 %; Frecuencia de portadora 200 MHz, Ganancia de TX = 20 dB.

**Figura 1. Simulación para el caso 1.**  
<img src="https://github.com/user-attachments/assets/470abe53-bbc5-47f3-8f99-0b97a937fdc1" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

**Figura 2. Señal obtenida en el osciloscopio para el caso 1.**  
<img src="https://github.com/user-attachments/assets/d9299e32-8e3d-4c5d-8c7f-7045a0867b86" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

**Figura 3. Señal obtenida en el analizador de espectros para el caso 1.**  
<img src="https://github.com/user-attachments/assets/4ae1395a-5a30-4dc5-85a8-9467af5e2c6b" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

---

Osciloscopio: se puede apreciar como la envolvente no toca el eje cero, por lo cual se cumple la condición de una modulación, se puede apreciar que debido a que su índice de modulación es bastante cercano a la de una modulación al 100%, no se presentan grandes pérdidas de la señal.

Analizador de espectros: Se puede observar como en el analizador de espectros se presenta un valor máximo en su frecuencia central y con prácticamente ningún armónico de un valor significativo.

Este caso muestra una transmisión eficiente y estable sin distorsión. La modulación al 60% permite una buena recuperación de la señal y un consumo razonable de ancho de banda. Ideal para aplicaciones donde se prioriza la integridad de la señal sobre la eficiencia espectral.

---

### Caso 2: Genere una Señal modulada en 100 %; Frecuencia de portadora 250 MHz, Ganancia de TX = 25 dB.

**Figura 1. Simulación para el caso 2.**  
<img src="https://github.com/user-attachments/assets/13b55ce8-d0b3-4b56-8b0c-87fc257b3a20" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

**Figura 2. Señal obtenida en el osciloscopio para el caso 2.**  
<img src="https://github.com/user-attachments/assets/c6eda459-21f4-4718-b6fd-55dc9f724e5d" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

**Figura 3. Señal obtenida en el analizador de espectros para el caso 2.**  
<img src="https://github.com/user-attachments/assets/2489d231-e92a-4775-95c6-1fc956afb0d9" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

---

Osciloscopio: Se puede apreciar como la envolvente de la señal toca el eje cero justo en los valles de la señal portadora, lo que indica la modulación al 100%, esta condición nos garantiza una eficiencia máxima con el menor número de pérdidas.

Analizador de espectros: No se distinguen ninguna banda además de la banda ubicada en la frecuencia central de 250 MHz, por lo que esa es la única componente relevante para su potencia, además se puede observar como no existe ningún armónico no deseado.

Este es el mejor escenario en términos de eficiencia y fidelidad. Se aprovecha la amplitud total de la portadora sin sobrepasarla, asegurando una demodulación sin pérdida de información ni generación de distorsiones.

---

### Caso 3: Genere una Señal modulada en 120 %; Frecuencia de portadora 150 MHz, Ganancia de TX = 30 dB.

**Figura 1. Simulación para el caso 3.**  
<img src="https://github.com/user-attachments/assets/2eff5a35-ce56-4131-8621-578f015e6f2a" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

**Figura 2. Señal obtenida en el osciloscopio para el caso 3.**  
<img src="https://github.com/user-attachments/assets/b2c330bb-dbc6-408c-8718-170dfb556436" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

**Figura 3. Señal obtenida en el analizador de espectros para el caso 3.**  
<img src="https://github.com/user-attachments/assets/2c36f4bd-b176-43cf-a9d1-ac9c1c24383e" title="Simulación" alt="Texto alternativo" width="600" height="400"/>

---

Osciloscopio: Se puede observar como la señal en el osciloscopio presenta una saturación y una sobrecarga, lo que distorsiona de gran manera la señal vista por dicho instrumento de medición, esta distorsión se manifiesta como una pérdida en la información de la señal obtenida.

Analizador de espectros: En este caso se evidenció lo mismo que para los otros casos, en donde solo se presenta un armónico en su frecuencia central y no aparece ningún tipo de armónico indeseado.

La sobre-modulación no es recomendable en aplicaciones de alta fidelidad. Aunque la señal pueda parecer más potente, la inversión de la envolvente genera errores al demodular. El espectro también se contamina con componentes indeseadas, lo que reduce la eficiencia espectral y puede causar interferencias.
