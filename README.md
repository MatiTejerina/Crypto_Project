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


### **Rol a desarrollar**

A traves de las API de Coingecko y Binance se crearan datasets de temporalidad de 1 dia de las 10 criptomonedas que mayor capitalizacion de mercado registran actualmente. Se excluirán de esa lista las monedas que no existian antes del 2019 por motivos de muestreo y a las stablecoins ya que no presentan volatilidad y su analisis se acota demasiado.
Una vez obtenidos los dataframes de partida se unira a traves de una funcion merge un dato proveniente del perfil de volumen de cada intervalo de 1 dia y se realizara una diferencia porcentual de todos los valores para cumplir criterio de estacionariedad. Este dato es el POC (Point of Control) que es el nivel de precio que mayor volumen de negociacion registró en el dia. Como se verá en los analisis posteriores este dato es clave para hacer una comparacion con el cierre de cada intervalo y asi poder definir una conducta (compra o venta) para el siguiente intervalo y definir la rentabilidad del periodo.

`EDA` (Exploratory Data Analysis)

Debes realizar un análisis exploratorio de los datos en un notebook. Tienen que estar tus pasos documentados con claridad, con las conclusiones correspondientes en cada gráfico empleado y análisis de lo que vas observando, utilizando celdas Markdown para tal fin. La prolijidad del notebook será un aspecto a evaluar. Es importante que tengas en cuenta que, en muchas oportunidades y trabajos, un EDA constituye un entregable en sí mismo.

En esta línea, hay varios aspectos indispensables que **deben** ser abordados en cualquier Análisis Exploratorio de Datos y tomaremos como punto de partida para evaluar tu performance en este apartado. Entre estos aspectos destacados se encuentran: *búsqueda de valores faltantes, valores atípicos/extremos u outliers y registros duplicados*. Asimismo, la utilización de gráficos coherentes según la tipología de variable que corresponda resulta esencial.

`Reporte`
 

`KPIs`

Debes sugerir 3 KPIs y deben estar adecuadamente representados de forma visual en el dashboard. Tén presente que deben tener relación con la historia que estás contando. Asimismo, se espera que en la presentación se explique el análisis y la funcionalidad de los KPIs sugeridos.


## Fuente de datos

- [API CoinGecko](https://www.coingecko.com/es/api/documentation)

**Complementarios:**
- Dataset propios
- [API Binance](https://binance-docs.github.io/apidocs/spot/en/#general-api-information)
