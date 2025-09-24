# 🌿 NDVI Analysis Project Worksheet  (Jaydon, Sano, La'a)

This worksheet will guide you through the process of designing and carrying out an NDVI-based analysis in R. Fill in the prompts for your chosen research question, location, time period, data sources, and methods.  

---

## 1. Framing the Question  

**What environmental or social issue will you explore?**  
*Write your thoughts here:*  Amazon Rainforest Deforestation over time

---

**Why is NDVI an appropriate tool for this question?**  
*Write your thoughts here:*  The Amazon Rainforest is very massive and full or greenery and the deforestation has been very prominent over the years so I feel that it would be easy to map it using NDVI.

---

**Who might find your results meaningful or useful?**  
*Write your thoughts here:*  Environmental scientists, conservation organizations, and policy makers could use the results to track the pace and extent of deforestation in the Amazon. Local and Indigenous communities may also find the information valuable since deforestation directly affects their lands, resources, and cultural practices. In addition, educators and the general public could use the findings to better understand how quickly the rainforest is changing and why protecting it matters on a global scale.

---

## 2. Choosing a Place and Time  

**What geographic area will you focus on?**  
*Write your thoughts here:*  Para (a state in Brazil) Pará is one of the largest states in Brazil and has experienced some of the highest rates of deforestation in the Amazon. Its forests are under pressure from logging, cattle ranching, soybean farming, and the expansion of road networks

---

**What time frame makes sense for your question?**  
(e.g., single date, multiple years, seasonal patterns)  
*Write your thoughts here:*  2000-2024

---

**How will you define the scope of your analysis?**  
*Write your thoughts here:*  The analysis will focus on the state of Pará, Brazil, which is one of the Amazon’s major deforestation frontiers. I will use satellite-derived NDVI data to track changes in forest greenery as a proxy for vegetation loss.

---

## 3. Finding Data  

**Where could you get satellite imagery or NDVI data?**  
*Write your thoughts here:*  Landsat (2000–2024) for the long-term NDVI trend or Sentinel-2 (2015–2024) for high-resolution recent deforestation mapping.




---

**What resolution and frequency are appropriate?**  
*Write your thoughts here:*  

---

**Will you download data manually or use an R package? Which one?**  
*Write your thoughts here:*  Manual Download

---

## 4. Bringing Data into R  

**What R packages can help you work with spatial data?**  
*Write your thoughts here:*  sf, terra, stars

---

**How will you handle projections, boundaries, or missing data?**  
*Write your thoughts here:*  Projections: Landsat, Sentinel, and MODIS all come in different coordinate reference systems (CRS). To compare them or overlay with Pará’s boundary shapefile, everything needs to be in the same CRS. ChatGPT explained the solution would be, "Reproject all rasters and vector data to a common projection before analysis. For regional studies in Pará, a projected CRS like UTM Zone 21S (EPSG:32721) or WGS84 / UTM works well because it minimizes distortion locally." Boundaries: We only want NDVI data within Pará, not the entire Amazon Basin or Brazil. The solution would be to import Pará’s state boundary shapefile (from IBGE or GADM) Missing Data: The Amazon has heavy cloud cover, and satellites often produce NDVI values of NA in cloudy/shadowed areas. The solution would be to apply cloud masks, and use temporal compositing.

---

**What file formats will you be working with?**  
*Write your thoughts here:*  raster, jp2, 

---

## 5. Calculating NDVI  

**What is the NDVI formula?**  
*Write your formula here:*  NDVI=(NIR+Red)/(NIR−Red)​

---

**Which spectral bands are needed?**  
*Write your thoughts here:*  Band 4 and 8 (sentinel) and Band 5 and 4 (Landsat)

---

**How will you apply this formula in R?**  
*Write your thoughts here:*  

---

## 6. Exploring and Visualizing Data  

**How will you summarize NDVI values?**  
(maps, plots, tables)  
*Write your thoughts here:*  

---

**Will you compare locations, beofre and after events, look at seasonal patterns, or study long-term trends?**  
*Write your thoughts here:*  

---

**How will you make your visualizations clear and interpretable?**  
*Write your thoughts here:*  

---

## 7. Interpreting Results  

**What patterns or relationships do you expect to see?**  
*Write your thoughts here:*  

---

**How do they relate to your research question?**  
*Write your thoughts here:*  

---

**What uncertainties or data limitations should you acknowledge?**  
*Write your thoughts here:*  

---

## 8. Reflecting on Impact  


**Could your results inform decisions, policies, or further research?**  
*Write your thoughts here:*  

---

**What new questions emerge from your findings?**  
*Write your thoughts here:*  
