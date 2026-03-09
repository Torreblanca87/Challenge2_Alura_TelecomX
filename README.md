# Challenge2_Alura_TelecomX

# Proyecto de Análisis de Datos

# Telecom X – Análisis de Deserción de Clientes (Churn)

**Rol:** Asistente de Análisis de Datos
**Dataset:** 7,032 registros de clientes
**Variables analizadas:** 23 características

---

# 1. Contexto del proyecto

En industrias de servicios como telecomunicaciones, la retención de clientes representa uno de los factores más importantes para la estabilidad financiera de la empresa. Adquirir nuevos clientes suele ser significativamente más costoso que mantener a los actuales, por lo que comprender las causas de la deserción se vuelve una prioridad estratégica.

El presente análisis explora el comportamiento de los clientes de **Telecom X**, con el objetivo de identificar patrones asociados al abandono del servicio (churn). Para ello se realiza un **análisis exploratorio de datos (EDA)** que permite examinar las características demográficas, contractuales y de uso del servicio.

El propósito final es generar conocimiento que permita diseñar estrategias de retención más efectivas y, en etapas posteriores, construir modelos predictivos que anticipen el riesgo de churn.

---

# 2. Objetivos del análisis

Este estudio tiene como meta principal **comprender los factores que influyen en la deserción de clientes** dentro de la base de datos analizada.

Los objetivos específicos son:

* Analizar la distribución y características de la base de clientes.
* Identificar variables que presentan una relación significativa con el churn.
* Detectar segmentos de clientes con mayor probabilidad de abandono.
* Generar insights que puedan ser utilizados en estrategias de retención.
* Definir variables relevantes para futuros modelos de predicción de churn.

---

# 3. Panorama general del dataset

La base de datos contiene información de **7,032 clientes**, incluyendo variables demográficas, detalles contractuales, servicios contratados y variables de facturación.

Entre las características más relevantes se encuentran:

* Información demográfica (género, edad, estado civil).
* Antigüedad del cliente en la empresa.
* Tipo de contrato.
* Servicios de telecomunicaciones contratados.
* Métodos de pago y facturación.
* Variables de facturación mensual y total.

El análisis inicial revela que **la tasa general de deserción es de aproximadamente 26.6%**, lo que indica que más de una cuarta parte de los clientes en la base han cancelado su servicio.

Desde una perspectiva de negocio, este nivel de churn representa una señal importante que justifica un análisis detallado de sus causas.

---

# 4. Perfil de los clientes

Antes de analizar la deserción, es importante comprender la estructura general de la base de clientes.

## 4.1 Características demográficas

La distribución de clientes por género es prácticamente equilibrada, con una proporción cercana al 50% entre hombres y mujeres. Esto sugiere que la base de clientes no presenta sesgos importantes en este aspecto.

En cuanto al grupo de **adultos mayores**, estos representan aproximadamente **16% del total de clientes**. Sin embargo, su comportamiento frente al churn es diferente al del resto de la población.

Por otra parte, el análisis de convivencia muestra que existe una ligera mayoría de clientes **sin pareja**, representando aproximadamente **52% de la base**.

Estas variables permiten establecer un primer panorama del tipo de clientes que componen la cartera de Telecom X.

---

## 4.2 Antigüedad del cliente

La antigüedad es una de las variables más importantes dentro del análisis de churn.

En la base analizada se observa que:

* La **mediana de antigüedad** es de aproximadamente **29 meses**.
* Existe una amplia dispersión en los datos.
* El primer cuartil se ubica alrededor de **10 meses**, mientras que el tercer cuartil se sitúa cerca de **55 meses**.

La distribución presenta una forma **bimodal**, lo que sugiere la coexistencia de dos grandes grupos dentro de la base: clientes relativamente nuevos y clientes con relaciones de largo plazo.

Este comportamiento puede tener implicaciones directas en la probabilidad de abandono.

---

## 4.3 Cargos mensuales

El análisis de los cargos mensuales revela una distribución heterogénea.

Se identifican tres segmentos principales dentro de la base:

* Clientes con cargos relativamente bajos.
* Clientes con cargos intermedios.
* Clientes con cargos mensuales elevados.

La distribución presenta una **asimetría hacia valores más altos**, lo que indica que existe un grupo relevante de clientes con servicios de mayor valor económico.

---

# 5. Factores asociados a la deserción

El análisis exploratorio permite identificar varias variables con una relación clara respecto al churn.

---

# 5.1 Antigüedad y abandono

La antigüedad del cliente muestra una relación inversa con la probabilidad de deserción.

En promedio:

* Los clientes que abandonan el servicio presentan una **antigüedad media de 18 meses**.
* En contraste, la base total de clientes tiene una antigüedad media cercana a **32 meses**.
* La **mediana de antigüedad de los desertores es de aproximadamente 10 meses**.

Este comportamiento evidencia una **correlación negativa moderada entre antigüedad y churn**, lo que indica que a medida que aumenta el tiempo de permanencia del cliente, disminuye su probabilidad de cancelar el servicio.

Al segmentar la antigüedad por periodos se observan diferencias importantes.

| Antigüedad     | Tasa de churn |
| -------------- | ------------- |
| 0 – 6 meses    | 53%           |
| 7 – 12 meses   | 36%           |
| 13 – 24 meses  | 29%           |
| 48 meses o más | < 10%         |

Esto sugiere que **los primeros meses de relación con el cliente constituyen la etapa más crítica para la retención**.

---

# 5.2 Variables sociodemográficas

El análisis de variables personales muestra resultados interesantes.

**Género**

No se observan diferencias relevantes en la tasa de deserción entre hombres y mujeres, lo que indica que esta variable no tiene un peso significativo en el comportamiento de churn.

**Adultos mayores**

Este grupo presenta una tasa de abandono cercana al **41.7%**, considerablemente superior al promedio general.

**Estado de pareja**

Los clientes que no tienen pareja muestran una tasa de churn cercana al **33%**, mientras que aquellos que viven con pareja presentan un nivel significativamente menor (**19.7%**).

Esto podría sugerir que los hogares con mayor estabilidad familiar tienden a mantener el servicio por más tiempo.

---

# 5.3 Tipo de contrato

El tipo de contrato emerge como uno de los factores más influyentes en la probabilidad de abandono.

| Tipo de contrato   | Tasa de churn |
| ------------------ | ------------- |
| Mensual            | 42.7%         |
| Contrato de 1 año  | 11.3%         |
| Contrato de 2 años | 2.8%          |

Los contratos mensuales presentan un nivel de churn considerablemente mayor, lo cual es consistente con la menor barrera de salida que ofrecen.

Por el contrario, los contratos de mayor duración funcionan como un mecanismo de retención natural al generar compromisos de permanencia.

Sin embargo, se observa que algunos clientes abandonan el servicio cerca del momento de renovación contractual, lo que abre oportunidades para estrategias de fidelización anticipada.

---

# 5.4 Método de pago

El método de pago también parece estar relacionado con la probabilidad de churn.

Los clientes que utilizan **cheque electrónico** presentan una tasa de abandono cercana al **45.3%**, significativamente superior a la de otros métodos.

En contraste, los métodos automáticos de pago, como tarjetas de crédito o transferencias bancarias, muestran menores niveles de deserción.

Esto podría reflejar diferencias en el nivel de compromiso del cliente o en la facilidad del proceso de pago.

---

# 5.5 Servicios contratados

## Servicio de internet

El tipo de conexión a internet presenta diferencias importantes en la tasa de abandono.

| Servicio                 | Tasa de churn |
| ------------------------ | ------------- |
| Fibra óptica             | 41.9%         |
| DSL                      | 19.0%         |
| Sin servicio de internet | 7.4%          |

El servicio de **fibra óptica** combina dos características relevantes: cargos mensuales más altos y una tasa de deserción elevada.

El análisis temporal sugiere que la mayoría de estas cancelaciones ocurre durante los primeros meses del servicio.

Esto apunta a posibles problemas en la experiencia inicial del cliente, como instalación, expectativas del servicio o soporte técnico.

---

## Servicios adicionales

El soporte técnico aparece como un factor importante de retención.

Los clientes que **no cuentan con soporte técnico** presentan una tasa de abandono **2.7 veces mayor** que aquellos que sí lo tienen.

Esto sugiere que los servicios complementarios pueden fortalecer la relación del cliente con la empresa y reducir la probabilidad de cancelación.

---

# 6. Impacto financiero del churn

El análisis de las variables de facturación permite comprender el impacto económico de la deserción.

**Cargo mensual**

* Clientes que abandonan: mediana cercana a **80**
* Clientes que permanecen: mediana cercana a **63**

Esto indica que el churn afecta en mayor medida a clientes con planes de mayor valor.

**Cargo total**

La relación observada entre cargo total y churn es negativa, lo cual se explica principalmente por la menor antigüedad de los clientes que abandonan.

---

# 7. Principales hallazgos del análisis

A partir del análisis exploratorio se identifican varios patrones relevantes:

1. La deserción se concentra principalmente en etapas tempranas de la relación con el cliente.
2. Los primeros seis meses representan el periodo más crítico para la retención.
3. Los contratos mensuales presentan el mayor riesgo de abandono.
4. El servicio de fibra óptica muestra una combinación de alto valor económico y alta tasa de churn.
5. Los servicios adicionales, particularmente el soporte técnico, contribuyen a mejorar la retención.
6. Los clientes con cargos mensuales más elevados presentan mayor probabilidad de abandono.

---

# 8. Recomendaciones estratégicas

## Acciones operativas inmediatas

* Implementar programas de **acompañamiento para nuevos clientes durante los primeros 90 días**.
* Fortalecer el **seguimiento a clientes que contratan fibra óptica**.
* Incentivar la migración hacia **contratos de mayor duración**.
* Promover el uso de **métodos de pago automáticos**.

---

## Estrategias de retención

Se recomienda implementar sistemas de monitoreo que identifiquen clientes con características de alto riesgo, tales como:

* Antigüedad inferior a 6 meses
* Cargos mensuales elevados
* Ausencia de soporte técnico
* Contratos mensuales

Asimismo, podrían desarrollarse campañas de renovación anticipada antes del vencimiento de contratos.

---

# 9. Conclusión

El análisis muestra que la deserción de clientes en Telecom X no ocurre de manera aleatoria. Por el contrario, está asociada a patrones identificables relacionados con la antigüedad del cliente, el tipo de contrato y los servicios contratados.

En particular, los **primeros meses de experiencia del cliente con la empresa** representan la etapa más determinante para su permanencia.

Desde una perspectiva estratégica, mejorar la experiencia inicial del cliente —especialmente en servicios de alto valor como la fibra óptica— representa una de las oportunidades más importantes para reducir el churn y fortalecer la estabilidad de ingresos de la empresa.

