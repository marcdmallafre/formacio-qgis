# Formació inicial de QGIS – Esqueleta del curs

# Part Teòrica

## 1. Introducció a QGIS i conceptes bàsics
- Què és QGIS i per a què serveix
- Tipus de dades GIS: vectorial vs ràster
- Projectes QGIS (`.qgz`)

### Obrim un projecte nou
- Sistema de coordenades (CRS): concepte bàsic (projecte vs capa)
- 

---

## 2. Interfície de QGIS
- Panells principals:
  - Panell de capes
  - Canvas del mapa
  - Panell navegador
- Barres d'eines bàsiques
- Caixa d'eines
- Guardar i recuperar projectes

---

## 3. Gestió d'informació
- Afegir capes:
  - Vectorials (Shapefile, GeoPackage)
  - Ràster
- Incorporar i treure capes
- Ordre de dibuix
- Visibilitat i zoom a capa
- Eliminar capes (projecte vs fitxer)

### 3.1. Adreçes i plugins d'interès
- OpenICGC
- Open Coordinator
- WFS ICGC: https://geoserveis.icgc.cat/servei/catalunya/divisions-administratives/wfs


---

## 4. Plantilla de treball del servei de prevenció urbanística

V:\Urbanisme_IRP\DOCUMENTACIO\Plantilla_GIS_mapes --> plantilla_qgis_20260902

# 4.1 Estructura de la plantilla QGIS
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
- Identificar elements - openicgc
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
- Carregar un geopakage: V:\Urbanisme_IRP\DOCUMENTACIO\Plantilla_GIS_mapes\bd_cartografia\topografia-territorial-v1r0-2023.gpkg

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

[[https://pau.cat/parentpage/poum/](https://seu-e.cat/documents/1408847/20199799/PLANOL+ORDENACIO.pdf/55a0de2c-f9bb-4f6b-979d-fe3ab9b89111) ](https://seu-e.cat/documents/1408847/20199799/PLANOL+ORDENACIO.pdf/55a0de2c-f9bb-4f6b-979d-fe3ab9b89111) Pàgina 11
 
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

| codi | nom | x_utm | y_utm |
|------|------|------:|------:|
| 2 | Borda de Bailivell | 330340 | 4690428 |
| 5 | Borda de Pau | 330350 | 4690413 |
| 6 | Borda de Perutxo | 330183 | 4690318 |
| 7 | La Masia | 330913 | 4689072 |
| 8 | Borda Badia | 331460 | 4688789 |
| 10 | Borda de Casatnou | 330724 | 4688844 |
| 11 | Masia de Beneta | 330790 | 4689900 |
| 12 | Borda de Ribera | 331128 | 4688505 |
| 13 | Borda de Metge | 332404 | 4690121 |
| 14 | Borda del Rei | 332137 | 4690589 |
| 15 | Borda Martí | 331103 | 4688342 |
| 16 | La Mola | 331798 | 4689979 |
| 18 | Borda de Senterada | 334092 | 4691764 |
| 21 | Borda de l’Alberto | 333893 | 4691618 |
| 24 | Borda del Botiguer d’Envall | 333300 | 4690404 |
| 25 | Borda Miquel | 333954 | 4691428 |
| 26 | Borda de Batalla | 332438 | 4692510 |
| 27 | Borda de Guem | 332259 | 4692184 |
| 28 | Borda de Parire | 332139 | 4692526 |
| 29 | Borda Tomas | 332388 | 4692609 |
| 30 | Borda de Nadalet | 332233 | 4694274 |
| 32 | Borda de Canià | 331419 | 4693680 |
| 33 | Borda de Quartal | 331846 | 4692775 |
| 34 | Borda d’Escales | 331585 | 4693065 |
| 35 | Borda Santallaria | 331730 | 4692833 |
| 38 | Borda de Gallego | 331378 | 4695323 |
| 39 | Borda de Vells | 330247 | 4694993 |
| 40 | Borda de Viles | 331067 | 4694328 |
| 41 | Borda Isidro | 331707 | 4694123 |
| 42 | Borda de la Cai | 331002 | 4694584 |
| 49 | Borda de Cansat | 332730 | 4695547 |
| 50 | Borda del Ferrer | 332331 | 4698045 |
| 51 | Borda de Jaumet | 332828 | 4696221 |
| 52 | Borda d’en Roc | 331500 | 4697445 |
| 53 | Borda de Cortal | 331603 | 4695515 |
| 54 | Borda la Casera | 330712 | 4695443 |
| 55 | Borda de la Collada | 329657 | 4695051 |
| 56 | Borda la Macana | 331465 | 4695455 |
| 57 | La Bordeta | 330792 | 4696188 |
| 58 | Borda de la Plana | 331299 | 4696803 |
| 59 | Borda de Pedro | 330846 | 4696271 |
| 60 | Borda del Ferre | 331630 | 4696881 |
| 64 | Borda de Batalla | 333310 | 4696357 |
| 65 | Borda de Bernatxo | 333307 | 4696106 |
| 68 | Borda de Palau | 332979 | 4695670 |
| 71 | Borda d’Arnau | 334386 | 4696973 |
| 73 | Borda de Gaspar | 333514 | 4696525 |
| 74 | Borda de Gravat | 335108 | 4696793 |
| 75 | Borda de Jancuill | 335213 | 4696966 |
| 79 | Borda de Masa | 335319 | 4696952 |
| 80 | Borda de Ramon | 335253 | 4696943 |
| 89 | Les Cases d’en Pep | 334384 | 4694277 |
| 90 | Masia del Batlle | 333367 | 4694219 |
| 91 | Borda Agulló | 333652 | 4696509 |
| 96 | Borda Comes d’Aimà | 335310 | 4696250 |
| 97 | Borda de Gavatx | 335402 | 4696376 |
| 98 | Borda de Mestrepe | 334560 | 4695810 |
| 100 | Borda Toni | 334326 | 4696258 |
| 103 | Borda de Rascars | 334212 | 4694809 |
| 104 | Casa Font dels Pous | 335468 | 4696076 |
| 106 | Borda de Jaume | 334394 | 4695973 |
| 107 | Borda de Raons | 333804 | 4697723 |
| 108 | Borda de Teixidor | 333679 | 4697659 |
| 109 | Borda de Xiquet | 333614 | 4695817 |
| 114 | Borda de Pallis | 334523 | 4702358 |
| 117 | Refugi de Filla | 331501 | 4702591 |
| 120 | Borda del Prat del Pont | 334936 | 4704106 |
| 121 | Borda del Prat d’en Font | 335309 | 4705626 |
| 124 | La Mola | 334559 | 4704386 |
| 128 | Antic Hotel de FECSA | 335931 | 4708058 |
| 131 | Casa El Mestres | 334576 | 4695953 |

 
---
 
## Pràctica 5. Elaboració d'una figura d'informe a partir d'una referència cadastral
 
A partir d'una referència cadastral facilitada, incorporar l'àmbit corresponent al projecte i visualitzar-lo dins la plantilla corporativa. Preparar una composició cartogràfica específica per a informes, utilitzant la plantilla en format horitzontal i mostrant l'emplaçament de la finca sense activar les capes de riscos de protecció civil.


A partir d'aquest anunciat possible en una comissió d'urbanisme:

10.	Riudoms
AAA / 00112233 / M	26/07/2026
Pla especial urbanístic per a la creació d'un circuit de motocròs amb un centre de serveis i allotjament turístic, al polígon 43, parcel·la 72.

### Productes finals
- Àmbit de la referència cadastral incorporat al projecte.
- Composició cartogràfica d'informe en format horitzontal.
- Figura preparada per a la seva inclusió en documents tècnics.
- Exportació de la figura en PDF i/o imatge.
 
---
 
## Pràctica 6. Selecció i explotació d'informació urbanística

### Part 1
A partir de la capa d'equipaments municipals, identificar tots els equipaments situats al municipi de Riudoms en el marc d'una modificació puntual del planejament. Aplicar eines de selecció i filtratge, revisar els resultats obtinguts i generar una capa específica amb els elements afectats.

### Part 2
Resulta que un equipament, el del carrer Joan Miró, Doctor Flèming i Carrer de la sardana es modifica i inclou també el parc dels gegants. Edita el polígon afegint tota la illa.

### Productes finals
- Selecció dels equipaments del municipi de Riudoms.
- Capa derivada amb els elements seleccionats.
- Exportació de la informació per a la seva utilització en expedients urbanístics.

Resultat
"CODI_QUAL_MUC" = 'SE'
AND
"CODI_INE" = 43129
