# Formació inicial de QGIS

## Aplicació al servei de prevenció urbanística de la Direcció General de Protecció Civil

**Document de treball --- proposta revisada**

------------------------------------------------------------------------

## 1. Objectiu del curs

Proporcionar als tècnics els coneixements necessaris per treballar amb
informació geogràfica a QGIS, consultar i editar dades, fer anàlisis
espacials bàsiques i elaborar cartografia tècnica mitjançant la
plantilla corporativa del servei.

El curs parteix de situacions habituals del treball d'urbanisme i
Protecció Civil. No té com a objectiu formar especialistes en SIG, sinó
capacitar els participants per gestionar amb autonomia les tasques
cartogràfiques més freqüents.

## 2. Estructura i progressió

El curs s'organitza en tres blocs:

1.  **Fonaments i eines bàsiques de QGIS:** entendre el projecte, les
    capes, els sistemes de coordenades i les operacions habituals.
2.  **Gestió i anàlisi de dades:** consultar, seleccionar, editar,
    transformar i creuar informació geogràfica.
3.  **Aplicació al servei:** treballar amb la plantilla corporativa, la
    informació de Protecció Civil, el Mapa Urbanístic de Catalunya i les
    bases cartogràfiques de l'ICGC.

La part pràctica acompanya els continguts teòrics i culmina amb un
exercici d'anàlisi espacial aplicat a un cas urbanístic.

# PART TEÒRICA

## 1. Introducció als SIG i a QGIS

-   Què és un Sistema d'Informació Geogràfica (SIG).
-   Què és QGIS i per a què serveix.
-   Aplicacions dels SIG en l'àmbit de l'urbanisme i la Protecció Civil.
-   Tipus de dades geogràfiques:
    -   Dades vectorials: punts, línies i polígons.
    -   Dades ràster: ortofotos, models digitals del terreny i altres
        imatges.
-   Diferència entre dades geogràfiques i dades alfanumèriques.
-   Projectes QGIS (`.qgz`) i fonts de dades.

### Obrir i crear un projecte

-   Crear un projecte nou.
-   Obrir i desar projectes.
-   Configuració inicial del projecte.
-   Diferència entre projecte i capes de dades.

## 2. Interfície i entorn de treball

-   Panells principals:
    -   Panell de capes.
    -   Canvas o visualitzador del mapa.
    -   Panell navegador.
    -   Caixa d'eines de processos.
-   Barres d'eines i personalització bàsica de l'entorn.
-   Cerca d'eines i algoritmes.
-   Activar, desactivar i reorganitzar panells.
-   Guardar i recuperar la configuració de treball.

## 3. Sistemes de coordenades i projeccions

-   Què és un sistema de referència de coordenades (CRS).
-   Diferència entre coordenades geogràfiques i projectades.
-   CRS del projecte i CRS de les capes.
-   ETRS89 / UTM fus 31N (EPSG:25831).
-   Identificació del sistema de coordenades d'una capa.
-   Assignació d'un CRS i reprojecció d'una capa: diferències.
-   Reprojectar i exportar dades.
-   Problemes habituals de desplaçament o incompatibilitat entre capes.

## 4. Incorporació i gestió de dades geogràfiques

### 4.1. Formats de dades

-   Formats vectorials: Shapefile, GeoPackage i GeoJSON.
-   Formats ràster: GeoTIFF i altres imatges georeferenciades.
-   Taules externes: CSV i fulls de càlcul.
-   Diferència entre afegir una capa al projecte i modificar el fitxer
    d'origen.

### 4.2. Incorporació de capes

-   Afegir capes vectorials i ràster.
-   Incorporar taules amb coordenades.
-   Eliminar capes del projecte sense eliminar els fitxers.
-   Ordre de dibuix i visibilitat.
-   Zoom a l'extensió d'una capa.
-   Identificar l'origen i les propietats d'una capa.

### 4.3. Serveis i fonts cartogràfiques

-   Connexió a serveis WMS i WMTS.
-   Connexió a serveis WFS.
-   Diferències bàsiques entre serveis de visualització i serveis de
    dades.
-   Incorporació de serveis de l'ICGC.
-   Complements d'interès:
    -   OpenICGC.
    -   Open Coordinator.
-   Servei WFS de divisions administratives de l'ICGC:
    https://geoserveis.icgc.cat/servei/catalunya/divisions-administratives/wfs

## 5. Navegació, identificació i consulta

-   Zoom i desplaçament pel mapa.
-   Zoom a l'extensió del projecte i de les capes.
-   Identificar elements i consultar-ne els atributs.
-   Consultar informació mitjançant eines i complements disponibles.
-   Mesurar distàncies i superfícies.
-   Consultar les propietats i la informació de les capes.

## 6. Selecció, filtratge i expressions

-   Selecció d'elements:
    -   Per clic.
    -   Per rectangle i polígon.
    -   Per atributs.
    -   Per expressió.
-   Invertir, afegir i eliminar elements de la selecció.
-   Diferència entre seleccionar i filtrar.
-   Filtres de capes.
-   Introducció a les expressions de QGIS:
    -   Operadors de comparació.
    -   Operadors lògics `AND`, `OR` i `NOT`.
    -   Condicions amb text, nombres i valors nuls.
    -   Combinació de diverses condicions.
-   Exportació dels elements seleccionats o filtrats.

Exemple d'expressió:

``` sql
"CODI_QUAL_MUC" = 'SE'
AND
"CODI_INE" = 43129
```

## 7. Taula d'atributs i gestió de camps

-   Obrir i interpretar la taula d'atributs.
-   Registres i camps.
-   Tipus de camps: text, enter, decimal, data i altres.
-   Ordenar i filtrar registres.
-   Edició de valors.
-   Afegir, eliminar i modificar camps.
-   Unir taules mitjançant un camp comú.
-   Exportar taules i resultats.

## 8. Edició de dades vectorials i digitalització

-   Mode d'edició.
-   Crear capes de punts, línies i polígons.
-   Crear nous elements.
-   Modificar, moure i eliminar geometries.
-   Eines de vèrtexs.
-   Snapping o ajustament a geometries existents.
-   Configuració bàsica de toleràncies i capes d'ajust.
-   Desar o cancel·lar edicions.
-   Comprovacions bàsiques de geometries.

## 9. Calculadora de camps

-   Funcionament de la calculadora de camps.
-   Crear camps nous i actualitzar camps existents.
-   Tipus de dades i expressions.
-   Operacions aritmètiques.
-   Còpia i combinació de valors.
-   Càlcul d'àrees i longituds.
-   Ús de funcions bàsiques.
-   Diferència entre camps virtuals i camps guardats.
-   Consideracions sobre les unitats i el sistema de coordenades.

## 10. Geoprocessament i anàlisi espacial

-   Concepte de geoprocessament.
-   Caixa d'eines de processos.
-   Capes d'entrada i paràmetres dels algoritmes.
-   Eines bàsiques:
    -   Retallar (*Clip*).
    -   Intersecció (*Intersection*).
    -   Dissoldre (*Dissolve*).
    -   Buffer o àrea d'influència.
    -   Diferència (*Difference*).
    -   Unió espacial per localització.
-   Diferència entre operacions sobre atributs i operacions sobre
    geometries.
-   Desar i revisar els resultats.
-   Comprovació de geometries i resultats inesperats.

L'objectiu és entendre per a què serveix cada operació i saber escollir
l'eina adequada per a una necessitat concreta. No es pretén aprofundir
en anàlisis avançades.

## 11. Simbologia i etiquetatge

### 11.1. Simbologia

-   Simbologia simple.
-   Canvi de color, gruix, contorn i transparència.
-   Simbologia categòrica per camps.
-   Simbologia graduada.
-   Simbologia basada en regles: introducció.
-   Copiar i enganxar estils entre capes.
-   Desar i reutilitzar estils.

### 11.2. Etiquetatge

-   Etiquetatge a partir d'un camp.
-   Expressions per construir etiquetes.
-   Configuració de mida, color, contorn i posició.
-   Prioritats i conflictes entre etiquetes.
-   Etiquetatge condicionat: introducció.

## 12. GeoPackage i organització de les dades

-   Què és un GeoPackage.
-   Avantatges respecte del Shapefile.
-   Crear un GeoPackage.
-   Afegir-hi múltiples capes.
-   Exportar capes a un GeoPackage.
-   Consultar i gestionar les capes que conté.
-   Bones pràctiques:
    -   Noms clars i coherents.
    -   Evitar duplicats.
    -   Controlar els sistemes de coordenades.
    -   Centralitzar les dades del projecte.
    -   Mantenir una estructura de carpetes ordenada.
-   Diferència entre desar el projecte i desar les dades.
-   Rutes relatives i absolutes.
-   Recuperació de projectes amb fonts de dades no disponibles.

Fitxer de treball de referència:

`V:\Urbanisme_IRP\DOCUMENTACIO\Plantilla_GIS_mapes\bd_cartografia\topografia-territorial-v1r0-2023.gpkg`

## 13. Composició cartogràfica

-   Introducció al Disseny d'impressió.
-   Crear i configurar un disseny.
-   Afegir i configurar elements:
    -   Mapa.
    -   Llegenda.
    -   Escala gràfica.
    -   Fletxa del nord.
    -   Títol i textos.
    -   Imatges i altres elements gràfics.
-   Configuració de pàgina i orientació.
-   Escales i extensió del mapa.
-   Mapes principals i detalls ampliats.
-   Exportar a PDF i imatge.

## 14. Plantilla corporativa i informació del servei

Aquest bloc aplica els coneixements generals a l'entorn de treball del
servei de prevenció urbanística.

### 14.1. Estructura de la plantilla QGIS

Ubicació:

`V:\Urbanisme_IRP\DOCUMENTACIO\Plantilla_GIS_mapes\plantilla_qgis_20260902`

-   Obrir i desar la plantilla.
-   Organització dels grups de capes.
-   Convencions de noms.
-   Simbologia predefinida.
-   Fonts de dades utilitzades.
-   Servidor cartogràfic de la DGPC.
-   Activació i desactivació de capes.
-   Incorporació de noves dades sense alterar l'estructura original.
-   Bones pràctiques per mantenir la plantilla.

### 14.2. Informació de Protecció Civil

-   Risc d'inundació i les seves diferents capes.
-   Risc químic en establiments industrials.
-   Risc químic pel transport de mercaderies perilloses.
-   Risc nuclear.
-   Interpretació cartogràfica bàsica de les zones de risc.
-   Consulta i identificació d'afectacions.
-   Consultes habituals en expedients urbanístics.

### 14.3. Mapa Urbanístic de Catalunya (MUC)

-   Classificació del sòl.
-   Qualificació urbanística.
-   Desenvolupaments urbanístics.
-   Consulta d'informació urbanística.
-   Identificació de sectors i claus urbanístiques.
-   Consulta dels atributs i codis del MUC.
-   Selecció i extracció d'informació municipal.

### 14.4. Bases cartogràfiques de l'ICGC

-   Ortofoto.
-   Cartografia topogràfica.
-   Cartografia 1:5.000.
-   Ombres del terreny.
-   Models digitals del terreny.
-   Serveis WMS i WMTS.
-   Incorporació de bases cartogràfiques com a suport dels informes.

# PART PRÀCTICA

Les pràctiques segueixen una seqüència acumulativa: els resultats
d'alguns exercicis es reutilitzen en els següents. Es recomana treballar
amb un mateix projecte i un GeoPackage per anar incorporant les capes
generades.

## Pràctica 1. Georeferenciació d'un plànol de planejament urbanístic

### Objectiu

Georeferenciar un plànol de planejament a partir d'un document PDF i
situar-lo correctament sobre la cartografia de referència.

### Desenvolupament

1.  Obrir el document PDF corresponent al POUM.
2.  Identificar la pàgina que conté el plànol objecte de treball.
3.  Extreure la pàgina i convertir-la a format imatge.
4.  Obrir l'eina de georeferenciació de QGIS.
5.  Incorporar punts de control sobre elements identificables tant al
    plànol com a la cartografia de referència.
6.  Configurar el sistema de coordenades EPSG:25831.
7.  Executar la georeferenciació.
8.  Comprovar visualment l'ajust del plànol sobre l'ortofoto i la
    cartografia de suport.
9.  Revisar l'error dels punts de control i detectar possibles
    desajustos.

### Document de referència

[Plànol d'ordenació del POUM --- pàgina
11](https://seu-e.cat/documents/1408847/20199799/PLANOL+ORDENACIO.pdf/55a0de2c-f9bb-4f6b-979d-fe3ab9b89111)

### Productes finals

-   Imatge del plànol extreta del PDF.
-   Ràster georeferenciat en EPSG:25831.
-   Projecte QGIS amb el plànol correctament posicionat.

## Pràctica 2. Digitalització d'àmbits urbanístics

### Objectiu

Crear una capa de polígons a partir del plànol georeferenciat i
incorporar-hi informació identificativa.

### Desenvolupament

1.  Crear una nova capa vectorial de polígons.
2.  Configurar el sistema de coordenades EPSG:25831.
3.  Crear els camps necessaris per identificar els àmbits.
4.  Digitalitzar els quatre àmbits representats al plànol.
5.  Revisar i corregir les geometries.
6.  Introduir la informació identificativa a la taula d'atributs.
7.  Configurar el simbolisme i l'etiquetatge.
8.  Desar la capa dins del GeoPackage del projecte.

### Productes finals

-   Capa de polígons amb els quatre àmbits digitalitzats.
-   Taula d'atributs amb el nom de cada àmbit.
-   Etiquetatge configurat.
-   Capa guardada dins d'un GeoPackage.

## Pràctica 3. Elaboració de plànols amb la plantilla corporativa

### Objectiu

Incorporar les dades generades a les pràctiques anteriors a la plantilla
corporativa i elaborar composicions cartogràfiques.

### Desenvolupament

1.  Obrir la plantilla corporativa.
2.  Incorporar el plànol georeferenciat.
3.  Incorporar la capa dels àmbits digitalitzats.
4.  Organitzar les capes i configurar-ne la visibilitat.
5.  Revisar la simbologia i l'etiquetatge.
6.  Crear un disseny d'impressió en format horitzontal.
7.  Crear un segon disseny en format vertical.
8.  Incorporar un detall ampliat d'un dels àmbits de dimensions
    reduïdes.
9.  Exportar les composicions.

### Productes finals

-   Plànol en format horitzontal.
-   Plànol en format vertical.
-   Detall ampliat d'un àmbit de petites dimensions.
-   Exportació dels plànols en PDF.

## Pràctica 4. Incorporació de masos a partir de coordenades UTM

### Objectiu

Crear una capa de punts a partir d'una taula de coordenades UTM ETRS89
fus 31N (EPSG:25831).

### Desenvolupament

1.  Obrir la taula de masos facilitada en format CSV o full de càlcul.
2.  Identificar els camps corresponents al codi, nom, coordenada X i
    coordenada Y.
3.  Incorporar la taula a QGIS.
4.  Crear una capa de punts a partir de les coordenades.
5.  Assignar el sistema de coordenades EPSG:25831.
6.  Comprovar la ubicació dels punts sobre l'ortofoto.
7.  Revisar possibles errors de coordenades o d'importació.
8.  Desar la capa dins del GeoPackage del projecte.

### Productes finals

-   Capa de punts amb la localització dels masos.
-   Taula d'atributs amb el codi i el nom.
-   Verificació de la ubicació sobre ortofoto.
-   Capa incorporada al GeoPackage del projecte.

**Dades d'entrada:** utilitzar la taula completa de masos amb els camps
`codi`, `nom`, `x_utm` i `y_utm` inclosa en el document original del
curs.

## Pràctica 5. Elaboració d'una figura d'informe a partir d'una referència cadastral

### Objectiu

Incorporar una finca al projecte QGIS a partir de la seva referència
cadastral i elaborar una figura cartogràfica per a un informe
urbanístic.

### Enunciat de referència

A partir d'un possible assumpte tractat en una comissió d'urbanisme:

**10. Villalonga del camp --- 26/07/2026**

AAA / 00112233 / M

Pla especial urbanístic per a la creació d'un circuit de motocròs amb un
centre de serveis i allotjament turístic, al polígon 4, parcel·la 144.

### Desenvolupament

1.  Localitzar la finca a partir de la referència cadastral facilitada.
2.  Obtenir la geometria cadastral mitjançant la font de dades
    disponible.
3.  Incorporar la geometria al projecte.
4.  Comprovar-ne la ubicació sobre l'ortofoto.
5.  Obrir la plantilla corporativa.
6.  Preparar una composició cartogràfica específica per a informes.
7.  Utilitzar el format horitzontal.
8.  Mostrar l'emplaçament de la finca sense activar les capes de riscos
    de Protecció Civil.
9.  Exportar la figura.

### Productes finals

-   Àmbit de la referència cadastral incorporat al projecte.
-   Composició cartogràfica d'informe en format horitzontal.
-   Figura preparada per a la seva inclusió en documents tècnics.
-   Exportació en PDF i/o imatge.

## Pràctica 6. Selecció i explotació d'informació urbanística

### Objectiu

Utilitzar les eines de selecció, filtratge i exportació per obtenir
informació urbanística d'un municipi.

### Part 1. Identificació d'equipaments municipals

A partir de la capa d'equipaments municipals, identificar tots els
equipaments situats al municipi de Riudoms en el marc d'una modificació
puntual del planejament.

1.  Obrir la capa d'equipaments municipals.
2.  Consultar-ne la taula d'atributs.
3.  Identificar els camps que permeten distingir el tipus de
    qualificació i el municipi.
4.  Aplicar una selecció per expressió.
5.  Revisar els elements seleccionats.
6.  Exportar els resultats a una capa específica.

Expressió de referència:

``` sql
"CODI_QUAL_MUC" = 'SE'
AND
"CODI_INE" = 43129
```

### Part 2. Modificació d'un àmbit

Un dels equipaments, situat a l'entorn dels carrers Joan Miró, Doctor
Fleming i de la Sardana, es modifica per incorporar també el parc dels
Gegants.

1.  Localitzar el polígon de l'equipament.
2.  Activar el mode d'edició.
3.  Modificar la geometria per incorporar tota l'illa.
4.  Comprovar la continuïtat i la correcció del polígon.
5.  Desar els canvis.

### Productes finals

-   Selecció dels equipaments del municipi de Riudoms.
-   Capa derivada amb els elements seleccionats.
-   Polígon modificat amb la incorporació del parc dels Gegants.
-   Exportació de la informació per a la seva utilització en expedients
    urbanístics.

## Pràctica 7. Anàlisi espacial de riscos i planejament urbanístic

### Objectiu

Aplicar eines de geoprocessament per identificar i quantificar la
coincidència entre zones de risc i classificació urbanística.

### Enunciat

En el marc d'una consulta urbanística, es vol identificar quines
categories de sòl del MUC queden afectades per una determinada zona de
risc d'inundació i quantificar-ne la superfície.

### Desenvolupament

1.  Obrir la plantilla corporativa.
2.  Identificar i activar la capa de risc d'inundació que correspongui a
    l'exercici.
3.  Incorporar o activar la informació del MUC.
4.  Comprovar que les capes utilitzades tenen sistemes de coordenades
    compatibles.
5.  Executar una intersecció entre la zona de risc i la classificació
    urbanística.
6.  Revisar la taula d'atributs del resultat.
7.  Calcular la superfície afectada mitjançant la calculadora de camps.
8.  Agrupar o resumir les superfícies per classificació del sòl.
9.  Revisar els resultats i comprovar que no hi ha errors geomètrics o
    de càlcul.
10. Elaborar una composició cartogràfica amb la plantilla corporativa.

### Productes finals

-   Capa resultant de la intersecció entre risc i classificació
    urbanística.
-   Taula d'atributs amb les superfícies afectades.
-   Resum de superfícies per categoria de sòl.
-   Composició cartogràfica amb els resultats de l'anàlisi.

**Nota:** la pràctica s'ha de plantejar amb una capa de risc i un àmbit
de treball concrets, facilitats prèviament pel formador. La
interpretació normativa del risc no forma part de l'objectiu d'aquest
exercici; l'objectiu és aprendre a tractar i analitzar les dades
cartogràfiques.

# RESULTATS D'APRENENTATGE

En acabar el curs, els participants haurien de poder:

1.  Obrir, configurar i desar un projecte QGIS.
2.  Incorporar capes vectorials, ràster, taules i serveis cartogràfics.
3.  Identificar i gestionar els sistemes de coordenades.
4.  Consultar la informació gràfica i alfanumèrica de les capes.
5.  Seleccionar i filtrar elements mitjançant atributs i expressions.
6.  Crear i modificar geometries.
7.  Calcular i actualitzar camps de dades.
8.  Executar operacions bàsiques de geoprocessament.
9.  Configurar simbologia i etiquetatge.
10. Organitzar la informació en GeoPackage.
11. Utilitzar la plantilla corporativa i les fonts cartogràfiques del
    servei.
12. Elaborar i exportar composicions cartogràfiques per a informes.

# CONSIDERACIONS PER A LA IMPARTICIÓ

-   Prioritzar les demostracions pràctiques davant les explicacions
    teòriques extenses.
-   Utilitzar sempre que sigui possible dades i exemples del servei.
-   Facilitar als participants un conjunt de dades preparat per a cada
    pràctica.
-   Treballar amb EPSG:25831 com a sistema de referència habitual dels
    exercicis a Catalunya.
-   Fer que les pràctiques siguin acumulatives quan tingui sentit.
-   Reservar temps per resoldre incidències habituals: capes
    desconnectades, CRS incorrectes, geometries invàlides i errors
    d'exportació.
-   Diferenciar clarament les operacions que modifiquen les dades
    originals de les que generen capes noves.
-   Mantenir la plantilla corporativa original sense sobreescriure-la
    durant els exercicis.

# CONTINGUTS COMPLEMENTARIS I FORA DE L'ABAST INICIAL

Per mantenir el curs en un nivell inicial, deixaria per a una formació
posterior:

-   Modelatge i automatització amb el Modelador gràfic.
-   Introducció a PyQGIS i scripts Python.
-   Anàlisis ràster avançades.
-   Geoprocessament complex i anàlisi de xarxes.
-   Bases de dades espacials PostGIS.
-   Creació de formularis avançats i controls de qualitat automatitzats.

Aquests continguts poden constituir una segona formació, un cop els
participants dominin les operacions bàsiques del curs.
