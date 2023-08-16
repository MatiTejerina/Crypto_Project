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

Te sitúas en el puesto de Analista de Datos en una empresa de servicios financieros que se ha interesado en el mercado de criptomonedas debido a su crecimiento exponencial y el potencial de oportunidades de inversión para los clientes. La empresa te ha asignado la tarea de realizar un análisis exhaustivo utilizando datos de la API CoinGecko para entender mejor el mercado de criptomonedas y presentar tus hallazgos y recomendaciones en un informe detallado.

La fuente de información entregada por la empresa posee un conjunto de aproximadamente 4000 monedas y el tiempo estipulado para obtener tus análisis es corto, por lo que se te ha solicitado que acotes tu trabajo en al menos 10 criptomonedas, y en base a estas presentes tus análisis y recomendaciones.

Considera además que la elección de estas monedas queda a tu criterio, pero debes dejar claro el porqué de tu elección y el sustento de ésta. Por ejemplo, podrías seleccionar las criptomonedas con mayor capitalización de mercado, aquellas que han experimentado un mayor crecimiento reciente, o incluso algunas que son innovadoras en términos de tecnología o caso de uso.

Por último, asegúrate de destacar el impacto y las recomendaciones basadas en los resultados del análisis. Estos podrían incluir posibles estrategias u oportunidades de inversión, la gestión del riesgo, optimización de la cartera, sugerencias sobre cómo seguir monitoreando el mercado de criptomonedas, entre otros.


## **Propuesta de trabajo -mínimos entregables-**

`EDA` (Exploratory Data Analysis)

Debes realizar un análisis exploratorio de los datos en un notebook. Tienen que estar tus pasos documentados con claridad, con las conclusiones correspondientes en cada gráfico empleado y análisis de lo que vas observando, utilizando celdas Markdown para tal fin. La prolijidad del notebook será un aspecto a evaluar. Es importante que tengas en cuenta que, en muchas oportunidades y trabajos, un EDA constituye un entregable en sí mismo.

En esta línea, hay varios aspectos indispensables que **deben** ser abordados en cualquier Análisis Exploratorio de Datos y tomaremos como punto de partida para evaluar tu performance en este apartado. Entre estos aspectos destacados se encuentran: *búsqueda de valores faltantes, valores atípicos/extremos u outliers y registros duplicados*. Asimismo, la utilización de gráficos coherentes según la tipología de variable que corresponda resulta esencial.

***En caso de hacer uso de librerías como pandas_profiling, es indispensable acompañar los gráficos con análisis propios.***

`Dashboard`

Debe ser funcional y coherente con el storytelling. El dasbhoard tiene que incluir **filtros**, permitiendo explorar detalladamente los datos con la selección de cada uno de ellos. Es decir, es indispensable que sea **interactivo**. También, se espera que el diseño que implementen facilite la interpretación de la información y su análisis, siendo importante, para ello, la claridad en la presentación de los datos, aspectos inherentes a la esteticidad, elección coherente de los gráficos según las variables a visualizar, entre otros ítems. 

`Análisis` :warning:

No se considerará solamente la producción de gráficos con datos -dashboard-, sino también los análisis y conclusiones que puedan extraer a partir de ellos.

`KPIs`

Debes sugerir 3 KPIs y deben estar adecuadamente representados de forma visual en el dashboard. Tén presente que deben tener relación con la historia que estás contando. Asimismo, se espera que en la presentación se explique el análisis y la funcionalidad de los KPIs sugeridos.

`MUY IMPORTANTE` repasar qué es un KPI y cómo se diferencia de una métrica convencional. En el material de apoyo tienen lectura que puede ser de ayuda.</small>

`Repositorio de GitHub`

El repositorio debe contener un **Readme** principal donde presenten, en una primera instancia, de forma general **su proyecto** y detallen qué hay en cada archivo/carpeta del propio repositorio. Este Readme no puede ser el mismo de la consigna que nosotros les entregamos.
A su vez, el Readme debe incluir un **reporte de análisis con base en sus dashboards**, así como el análisis y la funcionalidad de los KPIs sugeridos.

### _**Desafíate y no te quedes siendo Junior, sé Junior Advanced**_

Pensando en alcanzar tu Boom, te recomendamos incorporar los siguientes desafíos para tener un portfolio mucho más completo y competitivo:

- Crear una base de datos en un motor SQL, ingestar el csv procesado y utilizarla como fuente de datos de su dashboard en Power BI (o la herramienta de visualización que utilice).
- Ejecutar scripts de Python en la herramienta de visualización de datos escogida.
- Cruce de datos con datasets complementarios, ya sea para obtener información nueva o poder comparar la información disponible para todas las plataformas. 

<sub> Nota: la realización de uno o más de estos ítems no es intercambiable con los requerimientos mínimos establecidos en la sección anterior "Propuesta de trabajo". Empiece con esta sección una vez haya cumplido con los requerimientos mínimos, a modo de desafiarse a usted mismo y destacar frente al resto.</sub>

## Fuente de datos
**Obligatorio:**

- [API CoinGecko](https://www.coingecko.com/es/api/documentation): Ten en cuenta que se verificará que los datos sean traidos desde la API

**Complementarios:**
- Cualquier dataset de búsqueda propia que complemente y mejore el análisis. 
- [API Binance](https://binance-docs.github.io/apidocs/spot/en/#general-api-information)
