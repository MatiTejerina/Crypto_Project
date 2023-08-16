<p align="center"><img src="images/henry_logo.png"></p>

# <h1 align=center> Cohorte Data-FT13 -- Matias Tejerina </h1>

# <h1 align=center> **PROYECTO INDIVIDUAL Nº2** </h1>

# <h1 align=center>**`Cryptocurrencies market analysis project`**</h1>

<p align="center">
<img src="images/logosmonedas.jpg"  height=300>
</p>
<hr>

## **Descripción del problema -contexto y rol a desarrollar-**

### **Contexto**

En los últimos años, el mercado de las criptomonedas ha experimentado un crecimiento exponencial y una creciente adopción a nivel mundial. La aparición del Bitcoin en 2009 marcó el inicio de una revolución financiera que ha llevado a la creación de miles de criptomonedas diferentes con diversas funcionalidades y tecnologías subyacentes.

Con el aumento del interés en el mercado de criptomonedas, cada vez más inversores, empresas y entusiastas buscan comprender mejor el comportamiento y la evolución de estos activos digitales. Sin embargo, la naturaleza altamente volátil y compleja de las criptomonedas presenta desafíos significativos para aquellos que desean tomar decisiones informadas sobre inversiones o simplemente para comprender mejor cómo funcionan estos mercados emergentes.

El análisis y la exploración de datos desempeñan un papel crucial en la obtención de información valiosa dentro del vasto conjunto de datos disponibles sobre criptomonedas. En este contexto, es clave el uso de una valiosa fuente de datos actualizados que proporcionen información sobre una amplia variedad de criptomonedas, incluidos precios, volúmenes de negociación, capitalización de mercado, información histórica y más.

### **Objetivo principal del analisis**

Generar una estrategia de compra o venta (long/short) y comparar el rendimiento entre la curva de equidad de la estrategia y la del criptoactivo subyacente.

### **Construcción del dataset**

A traves de las API de Coingecko y Binance se crearan datasets de temporalidad de 1 dia de las 10 criptomonedas que mayor capitalizacion de mercado registran actualmente. Se excluirán de esa lista las monedas que no existian antes del 2019 por motivos de muestreo y a las stablecoins ya que no presentan volatilidad suficiente.
Una vez obtenidos los dataframes de partida se unira a traves de una funcion merge un dato proveniente del perfil de volumen de cada intervalo de 1 dia y se realizara una diferencia porcentual de todos los valores de precio y volumen para cumplir criterio de estacionariedad. Este nuevo dato es el POC (Point of Control) que es el nivel de precio que mayor volumen de negociacion registró en el dia. Como se verá en los analisis posteriores este dato es clave para hacer una comparacion con el cierre de cada intervalo y asi poder definir una conducta (compra o venta) para el siguiente intervalo y definir la rentabilidad del periodo.

**¿Que es el perfil de volumen?**
El perfil de volumen en series temporales financieras es una representación gráfica que muestra la cantidad de activos (monedas en este caso) negociados por nivel de precio en un mercado durante intervalos de tiempo específicos, como minutos, horas o días. Este perfil revela la distribución de la actividad de negociación a lo largo del tiempo, destacando los momentos de mayor y menor volumen de transacciones. En términos formales, el perfil de volumen permite analizar la liquidez, la participación del mercado y las tendencias de interés en función de la cantidad de activos negociados en diferentes períodos temporales.

**¿Que es el Point of Control?**
Es el nivel de precio en el que el volumen de transacciones es más alto, lo que indica un punto de mayor interés y actividad por parte de los participantes del mercado. El POC es un componente importante del perfil de volumen ya que puede brindar información sobre niveles de soporte y resistencia en el mercado. Los traders e inversores a menudo observan el POC para determinar dónde se encuentra el equilibrio entre la oferta y la demanda, lo que puede influir en las decisiones de compra y venta de activos financieros.

**¿Que es el Close?**
Es el precio de cierre de cada periodo.

**¿Por que se hace la diferencia porcentual de los precios para estudiar los retornos en las series temporales financieras?**
El estudio de los retornos de los precios en lugar del valor crudo del precio en una serie temporal financiera es una práctica común en el análisis financiero por varias razones:

-Normalización de datos: Los precios de los activos financieros pueden variar significativamente en magnitud a lo largo del tiempo. Al trabajar con los retornos, se elimina este efecto, lo que permite comparar y analizar más fácilmente las tendencias y patrones a lo largo del tiempo.

-Estacionariedad: Los retornos suelen ser más estacionarios que los precios crudos. La estacionariedad es una propiedad deseable en análisis de series temporales, ya que simplifica el modelado y las inferencias estadísticas.

-Eliminación de tendencias: Los precios crudos a menudo presentan tendencias a largo plazo. Al calcular los retornos, se elimina esta tendencia, lo que facilita la identificación de patrones más sutiles, como movimientos cíclicos o estacionales.

-Análisis de volatilidad: Los retornos son cruciales para el estudio de la volatilidad en los mercados financieros. La volatilidad es una medida de la variabilidad de los precios, y se calcula utilizando los cambios en los retornos.

-Modelado financiero: Muchos modelos financieros, como los modelos de valoración de activos y los modelos de riesgo, están diseñados para trabajar con retornos en lugar de precios. Estos modelos asumen que los retornos siguen ciertas distribuciones estadísticas y propiedades que hacen que el análisis sea más manejable.

-Comparabilidad entre activos: Al trabajar con retornos, es más fácil comparar el desempeño de diferentes activos financieros, incluso si tienen precios muy diferentes. Esto es especialmente útil para los inversores y analistas que desean comparar cómo diferentes activos se han comportado a lo largo del tiempo.

-Análisis de riesgo y rendimiento: Los retornos son fundamentales para evaluar el rendimiento histórico y el riesgo asociado con una inversión. Al calcular medidas como la tasa de rendimiento, la desviación estándar y la relación riesgo-rendimiento, se utilizan los retornos.

**Logica de entrada al mercado**
En este analisis se toma en cuenta el fenomeno de autocorrelacion que presentan las series temporales financieras (el valor anterior tiene una influencia sobre el valor siguiente). En el notebook donde se trabajó se define la columna 'Directional_bias' que indica una direccionalidad para el siguiente retorno basada en que si el Close del intervalo se encuentra por encima del POC el siguiente retorno tendra una tendencia a ser negativo (el POC de un periodo anterior suele actuar como un "imán" atrayendo al precio) y viceversa.

## **`EDA` (Exploratory Data Analysis)**

En el EDA se prosiguió de manera sistematica a explorar los siguientes apartados de cada moneda y explicar las particularidades de cada una:
-Informacion sobre las columnas.
-Busqueda de valores nulos y duplicados.
-Generacion de estadisticas descriptivas sobre las columnas.
-Grafico de la serie temporal de los retornos de la estrategia.
-Grafico de la distribucion de los retornos de la estrategia.
-Grafico de la volatilidad de los retornos de la estrategia.
-Grafico de autocorrelacion.
-Grafico de correlacion.

## **`KPIs`**

Para evaluar el comportamiento de la estrategia utilizamos los siguientes 4 KPIs (rendimiento del portafolio, alpha, win/loss ratio, tasa de acierto) y 2 metricas auxiliares (valor minimo del portafolio y valor maximo del portafolio) que asisten en el estudio de la volatilidad del portafolio:

KPIs:

-Rendimiento del Portafolio: Es la medida de cómo ha crecido o disminuido el valor total del portafolio durante un período determinado. Se calcula como el cambio porcentual en el valor del portafolio desde el inicio del período hasta el final.

-Alpha: Es una métrica que evalúa el rendimiento de la cartera en comparación con un índice de referencia. Representa el exceso de rendimiento logrado por encima del activo subyacente. Un alpha positivo indica que has superado al mercado.

-Ratio de Ganancia Promedio a Pérdida Promedio: También conocido como "ratio de ganancia-pérdida" (Win-Loss Ratio), este KPI mide la proporción entre las ganancias promedio obtenidas en las operaciones exitosas y las pérdidas promedio en las operaciones perdedoras. Un ratio mayor a 1 indica que las ganancias superan las pérdidas, lo que puede ser positivo.

-Tasa de Ganancia: Es la proporción de operaciones exitosas en comparación con el total de operaciones realizadas. Se expresa como un porcentaje y ayuda a evaluar la eficacia de la estrategia. Una alta tasa de ganancia no garantiza automáticamente un buen rendimiento si las pérdidas en las operaciones perdedoras son muy grandes.

Métricas:

-Valor Mínimo del Portafolio: Es el punto más bajo que ha alcanzado el valor de la cartera en un período determinado. Puede ser útil para entender la pérdida máxima potencial que puede haber experimentado el portafolio.

-Valor Máximo del Portafolio: Es el punto más alto que ha alcanzado el valor de tu cartera en un período determinado. Indica el máximo crecimiento potencial logrado.

## **`Reporte`**

Se reportan los KPIs y metricas de las 3 criptomonedas con mayor capitalizacion de mercado actualmente:

**Moneda: bitcoin**
-Rendimiento Total: 299.54%
-Alpha: 48.46%
-Ratio de Ganancia Promedio a Pérdida Promedio: 0.96
-Tasa de ganancia: 54.48%
-Valor minimo del portafolio: -10.74%
-Valor maximo del portafolio: 354.98%

**Moneda: ethereum**
Rendimiento Total: 291.12%
Alpha: -60.65%
Ratio de Ganancia Promedio a Pérdida Promedio: 0.96
Tasa de ganancia: 53.5%
Valor minimo del portafolio: -34.79%
Valor maximo del portafolio: 474.26%

**Moneda: binancecoin**
Rendimiento Total: 869.23%
Alpha: 348.16%
Ratio de Ganancia Promedio a Pérdida Promedio: 1.07
Tasa de ganancia: 55.5%
Valor minimo del portafolio: -1.58%
Valor maximo del portafolio: 896.38%

## Fuente de datos

- [API CoinGecko](https://www.coingecko.com/es/api/documentation)

**Complementarios:**
- Dataset propios
- [API Binance](https://binance-docs.github.io/apidocs/spot/en/#general-api-information)

## Conclusión
Los KPIs y metricas indican que en las criptomonedas de mayor capitalizacion de mercado esta logica de entradas en long o short tiende a generar un exceso de retorno en comparacion con el activo subyacente.
