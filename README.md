# Análisis de Desinformación en Redes Sociales en las Elecciones Presidenciales

## Autores: 

- Leonardo Ponce 202030531-5 (leonardo.ponde@usm.cl)
- Álvaro Pozo 202030535-8 (alvaro.pozo@usm.cl)

# Descripción del problema abordado

Este proyecto analiza la propagación de desinformación en redes sociales durante eventos políticos. Se construyen grafos de difusión para identificar comunidades, usuarios influyentes y patrones de amplificación de contenido. Además, se realiza procesamiento de texto (NLP) para comparar temas entre usuarios humanos y cuentas automatizadas.

En este proyecto encontrarás:

1. **Recolección y lectura de datos** de publicaciones (`Tweets_Elecciones2025_Chile.csv`) y clasificación de bots (`analisis_bots_mejorado.csv`).
2. **Reconstrucción de cascadas de difusión** (retuits, compartidos, menciones) para formar grafos de propagación.
3. **Cálculo de métricas de red** (grado, betweenness, closeness, etc.) para identificar cuentas con rol de amplificación.
4. **Visualización temporal y geográfica** de la propagación de contenido.
5. **Detección de comunidades** mediante el método **Louvain** (`python-louvain`) y generación de resúmenes por comunidad.
6. **Análisis textual**: limpieza, eliminación de stopwords (NLTK/spaCy), generación de n-gramas y nubes de palabras para comparar temáticas entre usuarios humanos y automatizados.
7. **Cruce con señales de automatización** para distinguir posibles bots a partir de patrones de actividad.


# Dependencias técnicas y librerias necesarias

### Dependencias principales

- pandas  
- numpy  
- matplotlib  
- seaborn  
- wordcloud  
- adjustText  
- networkx  
- python-louvain  
- scikit-learn  
- scipy  
- nltk  
- spacy (`es_core_news_sm`)  
- unidecode

### Instalación

```bash
pip install pandas numpy matplotlib seaborn wordcloud adjustText \
            networkx python-louvain scikit-learn scipy nltk spacy unidecode
python -m spacy download es_core_news_sm
```

# Instrucciones de ejecución

1. Clona el repositorio y coloca los datos en la carpeta data/:
data/
├─ Tweets_Elecciones2025_Chile.csv
└─ analisis_bots_mejorado.csv
2. Abre el notebook: *Analisis_desinformacion.ipynb*

3. Ejecuta todas las celdas en orden (Kernel → Restart & Run All).

4. Los resultados incluyen:

- Visualizaciones de redes y comunidades.

- Nubes de palabras.

- Tablas resumen con métricas de difusión.