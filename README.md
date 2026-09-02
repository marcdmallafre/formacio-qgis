# Formació inicial de QGIS – Esqueleta del curs

# Part Teòrica

## 1. Introducció a QGIS i conceptes bàsics
- Què és QGIS i per a què serveix
- Tipus de dades GIS: vectorial vs ràster
- Projectes QGIS (`.qgz`)
- Sistema de coordenades (CRS): concepte bàsic (projecte vs capa)

---

## 2. Interfície de QGIS
- Panells principals:
  - Panell de capes
  - Canvas del mapa
  - Panell navegador
- Barres d'eines bàsiques
- Guardar i recuperar projectes

---

## 3. Afegir i gestionar capes
- Afegir capes:
  - Vectorials (Shapefile, GeoPackage)
  - Ràster
- Incorporar i treure capes
- Ordre de dibuix
- Visibilitat i zoom a capa
- Eliminar capes (projecte vs fitxer)

---

## 4. Plantilla de treball del servei de prevenció urbanística

#4.1 Estructura de la plantilla QGIS
- Organització dels grups de capes
- Convencions de noms
- Simbologia predefinida
- Fonts de dades utilitzades
- Servidor cartografic de la DGPC

# 4.2 Informació de Protecció Civil
- Risc d'inundació (diferents capes)
- Risc químic en establiments industrials
- Risc químic pel transport de mercaderies perilloses
- Risc nuclear
- Interpretació bàsica de les zones de risc
- Consultes habituals en expedients urbanístics

# 4.3 Mapa Urbanístic de Catalunya (MUC)
- Classificació del sòl
- Qualificació urbanística
- Desenvolupaments urbanístics
- Consulta d'informació urbanística
- Identificació de sectors i claus urbanístiques

# 4.4 Bases cartogràfiques de l'ICGC
- Ortofoto
- Topogràfic
- Cartografia 1:5.000
- Ombres del terreny i model digital
- Serveis WMS i WMTS

## 5. Navegació i eines bàsiques
- Zoom i desplaçament
- Zoom a extensió del projecte / capa
- Identificar elements
- Mesurar distàncies i àrees

---

## 6. Selecció d'elements
- Selecció per clic
- Selecció per rectangle / polígon
- Selecció per atribut (introducció)
- Invertir i netejar seleccions
- Treballar amb elements seleccionats

---

## 7. Taula d'atributs
- Obrir i entendre la taula d'atributs
- Tipus de camps (text, enter, decimal)
- Ordenar i filtrar registres
- Edició bàsica de valors
- Afegir i eliminar camps (introducció)

---

## 8. Edició de dades vectorials (geometries)
- Mode d'edició
- Crear nous elements (punt, línia, polígon)
- Moure, modificar i esborrar geometries
- Snapping (concepte bàsic)
- Desar i cancel·lar edicions

---

## 9. Calculadora de camps (nivell inicial)
- Què és la calculadora de camps
- Crear camps nous
- Càlculs simples:
  - Còpia de valors
  - Operacions bàsiques (+, -, *, /)
  - Àrea i longitud (introducció)
- Camps temporals vs camps guardats

---

## 10. Estils i simbologia
- Simbologia simple
- Canvi de color, gruix i transparència
- Simbologia categòrica per camps
- Canvi ràpid d'estils
- Copiar i enganxar estils entre capes

---

## 11. Ús correcte de GeoPackage
- Què és un GeoPackage
- Avantatges respecte al Shapefile
- Crear un GeoPackage
- Afegir múltiples capes dins un mateix fitxer
- Bones pràctiques:
  - Noms clars de capes
  - Evitar duplicats
  - Centralitzar dades del projecte

---

## 12. Composició cartogràfica
- Introducció al Disseny d'impressió
- Crear un nou disseny
- Elements bàsics:
  - Mapa
  - Llegenda
  - Escala gràfica
  - Fletxa del nord
  - Títol i textos
- Exportar mapes a PDF i imatge

---

# Part pràctica

## Pràctica 1. Georeferenciació d'un plànol de planejament urbanístic
 
A partir d'un document PDF corresponent a un POUM, cal identificar la pàgina que conté el plànol objecte de treball i exportar-la a format imatge. Posteriorment, s'ha de georeferenciar aquesta imatge utilitzant punts de control sobre una base cartogràfica de referència. El resultat s'ha de validar visualment comprovant que el plànol s'ajusta correctament a l'ortofoto i a la cartografia de suport.
 
### Productes finals
- Imatge del plànol extreta del PDF.
- Ràster georeferenciat en EPSG:25831.
- Projecte QGIS amb el plànol correctament posicionat.
 
---
 
## Pràctica 2. Digitalització d'àmbits urbanístics
 
Utilitzant el plànol georeferenciat obtingut a la pràctica anterior, cal crear una capa de polígons i digitalitzar els quatre àmbits representats al document. Per a cada àmbit s'ha d'incorporar la informació identificativa corresponent i configurar l'etiquetatge perquè el nom de cada àmbit sigui visible sobre el mapa.
 
### Productes finals
- Capa de polígons amb els quatre àmbits digitalitzats.
- Taula d'atributs amb el nom de cada àmbit.
- Etiquetatge configurat amb els noms dels àmbits.
- Capa guardada dins d'un GeoPackage.
 
---
 
## Pràctica 3. Elaboració de plànols amb la plantilla corporativa
 
Incorporar a la plantilla corporativa de QGIS el plànol georeferenciat i els àmbits digitalitzats a les pràctiques anteriors. Mitjançant el Disseny d'Impressió, elaborar dues composicions cartogràfiques del mateix document: una en format horitzontal i una altra en format vertical. A més, cal crear un detall ampliat d'un dels àmbits afectats de dimensions reduïdes per millorar-ne la llegibilitat.
 
### Productes finals
- Plànol en format horitzontal.
- Plànol en format vertical.
- Detall ampliat (zoom) d'un àmbit de petites dimensions.
- Exportació dels plànols en format PDF.
 
---
 
## Pràctica 4. Incorporació de masos a partir de coordenades UTM
 
A partir d'una taula amb la relació de masos i les seves coordenades UTM ETRS89 fus 31N (EPSG:25831), crear una capa de punts a QGIS i verificar la correcta ubicació dels elements sobre la cartografia de referència. La informació generada s'ha d'emmagatzemar al GeoPackage del projecte.
 
### Productes finals
- Capa de punts amb la localització dels masos.
- Verificació de la seva ubicació sobre ortofoto.
- Capa incorporada al GeoPackage del projecte.
 
---
 
## Pràctica 5. Elaboració d'una figura d'informe a partir d'una referència cadastral
 
A partir d'una referència cadastral facilitada, incorporar l'àmbit corresponent al projecte i visualitzar-lo dins la plantilla corporativa. Preparar una composició cartogràfica específica per a informes, utilitzant la plantilla en format horitzontal i mostrant l'emplaçament de la finca sense activar les capes de riscos de protecció civil.
 
### Productes finals
- Àmbit de la referència cadastral incorporat al projecte.
- Composició cartogràfica d'informe en format horitzontal.
- Figura preparada per a la seva inclusió en documents tècnics.
- Exportació de la figura en PDF i/o imatge.
 
---
 
## Pràctica 6. Selecció i explotació d'informació urbanística
 
A partir de la capa d'equipaments municipals, identificar tots els equipaments situats al municipi de Riudoms en el marc d'una modificació puntual del planejament. Aplicar eines de selecció i filtratge, revisar els resultats obtinguts i generar una capa específica amb els elements afectats.
 
### Productes finals
- Selecció dels equipaments del municipi de Riudoms.
- Capa derivada amb els elements seleccionats.
- Exportació de la informació per a la seva utilització en expedients urbanístics.

