# Análisis de mercado para la apertura de centros especializados de Halterofilia - *Lift & Lead*

## 📊 Descripción del proyecto
Este repositorio contiene un análisis de datos de los Campeonatos Europeos de Halterofilia para validar la hipótesis de que la popularidad del CrossFit está impulsando el interés por la halterofilia en Europa. El análisis apoya la estrategia de negocio de ***Lift & Lead***, una startup que busca abrir centros de entrenamiento especializados en halterofilia.

## 🔍 Estructura del análisis
El análisis se ha realizado en dos fases:

### Fase 1
Análisis de datos de los campeonatos europeos de halterofilia de 2019 y 2020, incluyendo:
- Limpieza y estructuración de datos
- Creación de un dataframe unificado
- Extracción de información relevante sobre atletas, países, categorías y resultados

### Fase 2
Ampliación del análisis incluyendo datos de 2019 a 2024, mediante:
- Web scraping de datos adicionales de Wikipedia (2021-2024)
- Integración con el análisis previo
- Análisis comparativo entre periodos

## 🛠️ Tecnologías utilizadas

### Procesamiento y análisis de datos
- **pandas**: Manipulación y análisis de dataframes
- **numpy**: Operaciones numéricas y manejo de arrays

### Visualización de datos
- **matplotlib**: Creación de gráficos estáticos
- **seaborn**: Visualizaciones estadísticas avanzadas
- **plotly.express**: Gráficos interactivos

### Web scraping y extracción de datos

- **requests**: Realización de solicitudes HTTP.
- **BeautifulSoup**: Parsing y extracción de datos HTML estructurados.

### Análisis exploratorio
- **missingno**: Visualización de datos faltantes

### Procesamiento de texto y coincidencia de cadenas
- **re**: Expresiones regulares para procesamiento de texto
- **fuzzywuzzy**: Coincidencia de cadenas mediante lógica difusa

## 📋 Metodología
1. **Preparación de datos**:
   - Concatenación de datasets de diferentes años
   - Extracción de información estructurada de columnas con datos combinados
   - Limpieza de caracteres extraños
   - Creación de nuevas columnas: Medalla, Atleta, Fecha, Nombre, Apellido, País, Resultados, etc.
   - Conversión de tipos de datos para análisis

2. **Análisis exploratorio (EDA)**:
   - Detección de outliers
   - Visualización mediante boxplots y gráficos de barras
   - Análisis de distribución de medallas por país y género
   - Evaluación de equidad en resultados por género

3. **Web Scraping y extracción de datos**:
    - Identificación y selección de URLs de Wikipedia con resultados oficiales de campeonatos (2021-2024)
   - Utilización de requests para obtener el contenido HTML completo de cada página
   - Implementación de BeautifulSoup para parsear y navegar por la estructura DOM
   - Localización de tablas de resultados mediante selectores CSS específicos y atributos de clase
   - Filtrado de tablas relevantes según encabezados y contenido para distinguir entre diferentes categorías y eventos
   - Transformación de datos tabulares HTML a estructuras de pandas mediante pd.read_html() combinado con procesamiento     personalizado
    - Homogeneización de formatos de datos entre diferentes años para mantener consistencia con el dataset original
    - Tratamiento específico para variaciones en nomenclatura de países.
  
## 🏆 Principales hallazgos
- Distribución de medallas por país (oro, plata y bronce)
- Identificación de países con mayor equidad en términos de éxito entre atletas femeninos y masculinos:
  - Los países más equitativos: Azerbaiyán, Alemania y Moldavia
  - Los países menos equitativos: Reino Unido, Suecia, Albania, Polonia, España, Bélgica, Austria, Georgia
- Países con menor diferencia entre puntuaciones promedio por género
- Cambios significativos en la distribución de medallas a lo largo del tiempo, incluyendo el impacto de eventos como la exclusión de Rusia y Bielorrusia a partir de 2022

## ⚠️ Consideraciones especiales
- El campeonato de 2020 se celebró en 2021 debido a la pandemia de COVID-19
- En 2022, los atletas de Rusia y Bielorrusia fueron excluidos debido a la invasión rusa de Ucrania
- En 2024, los deportistas bielorrusos participaron bajo la denominación "Atletas Independientes Neutrales"

## 💡 Conclusiones relevantes para el negocio
El análisis proporciona insights valiosos para ***Lift & Lead*** sobre:
- Mercados potenciales basados en el éxito y popularidad por países
- Tendencias en la participación y rendimiento por género
- Evolución del interés por la halterofilia en diferentes regiones europeas
- Cambios en el panorama competitivo que podrían indicar oportunidades de mercado

---

*Este repositorio contiene todo el código y análisis detallado que respalda estas conclusiones*