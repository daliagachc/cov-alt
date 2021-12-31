# Razón de mortandad vs elevación

## Descripción

### Países Andinos

(version [pdf]('reg_alt_alt.pdf'))  
Razón de excesos de mortandad ($R_m$) vs elevación para regiones administrativas (nivel 1) de ciertos países de Latinoamérica. 
La línea base de mortandad (denominador) se tomó utilizando el año 2019. 
El numerador son los datos de mortandad disponibles desde marzo 2020. 
El área de cada circulo es proporcional a la población de la región.  
Las líneas discontinuas marcan el promedio ponderado para cada país (y para la región).
La línea punteada marca la regresión lineal (no ponderada) de la razón de mortandad (y) vs la elevación (x). 
La elevación de cada región se obtuvo mediante el promedio ponderado (por población) de sus ciudades constituyentes.


```python
from IPython import display; display.Image("reg_alt_alt.png")
```




    
![png](README_files/README_4_0.png)
    



### Países sudamericanos


```python
display.Image("reg_alt.png")
```




    
![png](README_files/README_6_0.png)
    



(version [pdf]('reg_alt.pdf'))  
Similar al anterior pero con Paraguay, Brasil, Chile y Uruguay incluídos. Probablemente el resultado de la regresión es un caso de "falacia ecológica" 

## Países andinos individuales

Individualmente la pendiente de la regresión es negativa para los países andinos, sin embargo en el rango 0.025-.975 dan valores positivos y negativos para todos


```python
display.Image("reg_alt_altPeru.png")
```




    
![png](README_files/README_10_0.png)
    




```python
display.Image("reg_alt_altBolivia.png")
```




    
![png](README_files/README_11_0.png)
    




```python
display.Image("reg_alt_altEcuador.png")
```




    
![png](README_files/README_12_0.png)
    




```python
display.Image("reg_alt_altColombia.png")
```




    
![png](README_files/README_13_0.png)
    



## Países andinos "normalizados"

Si a la razón de mortandad le sustraemos el promedio de cada país obtenemos un aproximado que toma en cuenta los diferencias de cada país y se enfoca en la pendiente como función de la altura. El resultado es $m=-0.02(-0.06,0.01)$. Esto nos indica que por cada kilometro que se sube en altura, la razón de exceso de mortandad reduce un aprox. de 2%. La variación es mínima y además dentro del rango acotado se encuentran valores positivos y negativos 


```python
display.Image("reg_alt_alt_corr.png")
```




    
![png](README_files/README_16_0.png)
    



### normalizando la elevación

Finalmente, con el objetivo de reducir la "falacica ecológica" también podemos sustrar el promedio de altura de cada país


```python
display.Image("reg_alt_alt_corr_corr.png")
```




    
![png](README_files/README_19_0.png)
    



## Comentarios
1. Desde el principios de 2020 los habitantes de Lima han casi triplicado sus probabilidades de morir.
1. Uruguay es un caso excepcional en que las probabilidades han disminuido con la pandemia
1. La regresión para la segunda figura es "ingenua" en el sentido que no toma en cuenta que los países que han afrontado mejor la pandemia (e.g. Uruguay, Chile) tienen sus regiones a casi nivel del mar
1. Por ende, si tomamos en cuenta solo países con regions altas y bajas (Perú, Bolivia, Ecuador, Colombia) tenemos una mejor idea (primera figura)

# Chances de mortandad el 2021 comparadas a 2019 


```python
display.Image("scatter_pais.png")
```




    
![png](README_files/README_22_0.png)
    



## Fuentes
datos de covid obtenidos del gran trabajo de:
  - https://github.com/pr0nstar
      - https://github.com/pr0nstar/covid19-data
        - https://github.com/pr0nstar/covid19-data/blob/master/raw/mortality/south.america.subnational.mortality.csv  

información demográfica obtenidad de wolfram alpha

## Extra 


```python
!jupyter-nbconvert --to markdown README.ipynb
```

    [NbConvertApp] Converting notebook README.ipynb to markdown
    [NbConvertApp] Support files will be in README_files/
    [NbConvertApp] Making directory README_files
    [NbConvertApp] Making directory README_files
    [NbConvertApp] Making directory README_files
    [NbConvertApp] Making directory README_files
    [NbConvertApp] Making directory README_files
    [NbConvertApp] Making directory README_files
    [NbConvertApp] Making directory README_files
    [NbConvertApp] Making directory README_files
    [NbConvertApp] Writing 5663 bytes to README.md



```python
!echo 'gsh'; git add .; git commit -m'from mac'; git push
```

    gsh
    fatal: unable to stat '.~region_alt-Copy1.ipynb': No such file or directory
    On branch master
    Your branch is up to date with 'origin/master'.
    
    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
    	[31mmodified:   README.ipynb[m
    	[31mmodified:   README.md[m
    	[31mmodified:   reg_alt.pdf[m
    	[31mmodified:   reg_alt.png[m
    	[31mmodified:   reg_alt_alt.pdf[m
    	[31mmodified:   reg_alt_alt.png[m
    	[31mmodified:   reg_alt_altBolivia.pdf[m
    	[31mmodified:   reg_alt_altBolivia.png[m
    	[31mmodified:   reg_alt_altColombia.pdf[m
    	[31mmodified:   reg_alt_altColombia.png[m
    	[31mmodified:   reg_alt_altEcuador.pdf[m
    	[31mmodified:   reg_alt_altEcuador.png[m
    	[31mmodified:   reg_alt_altPeru.pdf[m
    	[31mmodified:   reg_alt_altPeru.png[m
    	[31mmodified:   reg_alt_alt_corr.pdf[m
    	[31mmodified:   reg_alt_alt_corr.png[m
    	[31mmodified:   reg_alt_alt_corr_corr.pdf[m
    	[31mmodified:   reg_alt_alt_corr_corr.png[m
    	[31mmodified:   region.ipynb[m
    	[31mmodified:   region_alt-Copy1.ipynb[m
    	[31mmodified:   region_alt.ipynb[m
    	[31mmodified:   region_alt_corr_country-Copy1.ipynb[m
    	[31mmodified:   region_alt_corr_country.ipynb[m
    
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
    	[31mUntitled-Copy1.ipynb[m
    	[31mUntitled.ipynb[m
    	[31mdata/ortiz-prado_2021.xlsx[m
    
    no changes added to commit (use "git add" and/or "git commit -a")
    Everything up-to-date



```python

```


```python

```


```python

```


```python

```
