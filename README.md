# DIW_Maquetacio

Desarrollo de una web responsive para un restaurante usando HTML y CSS, con maquetación mediante Grid y Flexbox, secciones de carta, galería y reservas. Diseño adaptable, accesible y compatible con los principales navegadores.

# Pràctica 10 - HTML / CSS / RESPONSIVE

## MÒDUL

Disseny d’interfícies Web

## RA2

Crea interfícies web homogènies definint i aplicant estils.

## TIPUS D’ACTIVITAT

Activitat avaluable (30%)  
Desenvolupament individual

---

## OBJECTIUS

- Reconèixer les possibilitats de modificar les etiquetes HTML.
- Definir i associar estils globals a fulls externs.
- Redefinir estils utilitzant herència.
- Identificar les propietats de cada element.
- Crear classes d’estils reutilitzables.
- Aplicar disseny responsive.
- Utilitzar eines de validació CSS i accessibilitat.

---

## CONDICIONS D’ENTREGA

- Entrega via GitHub.
- Mateix repositori: `DIW_Maquetacio`
- Crear una nova branca obligatòria:

---

## CRITERIS D’ACCEPTACIÓ

- ❗ Només es pot modificar el CSS.
- ❗ S’ha d’utilitzar herència i reutilització d’estils (NO repetir CSS en media queries).
- ❗ Sense errors de codi (penalització fins a -2 punts).
- ❗ Comentaris al CSS i HTML (penalització -1 punt).
- ❗ Compatible amb navegadors principals.
- ❗ Sense scroll horitzontal.
- ❗ Ús obligatori de breakpoints:
- 768px (tablet)
- 576px (mòbil)
- ❗ Pàgina accessible (validació amb WAVE).
- ❗ No es poden usar tècniques no explicades a classe.
- ❗ S’ha de treballar en una nova branca.

---

## ESTRUCTURA DEL PROJECTE

La pàgina continua la pràctica anterior amb millores responsive:

- Menú fix superior
- Header amb imatge adaptativa
- Secció "Sobre nosaltres" amb grid responsive
- Carta amb layout grid
- Galeria amb flex responsive
- Formulari de reserva
- Footer adaptatiu

---

## BREAKPOINTS RESPONSIVE

### 📱 Mòbil (≤ 576px)

- Menú en columna
- Botons al 100% d’amplada
- Grid de "Sobre nosaltres" en una sola columna
- Carta adaptada a layout vertical
- Títol de Carta ocult
- Galeria en columna
- Imatges més grans i adaptades
- Footer centrat i sense logo

---

### 📱 Tablet (≤ 768px)

- Menú simplificat
- Grid de "Sobre nosaltres" reorganitzat
- Carta amb ajust de columnes
- Galeria flexible amb wrap
- Footer centrat, logo ocult

---

## TECNOLOGIES UTILITZADES

- HTML5 semàntic
- CSS3
- Flexbox
- CSS Grid
- Media Queries
- Variables CSS (`:root`)
- Google Material Symbols (icones)

---

## ACCESSIBILITAT

- Ús d’atributs `alt` a totes les imatges
- Estructura semàntica HTML
- Comprovació amb extensió WAVE

---

## RESPONSIVE DESIGN

El projecte s’adapta correctament a:

- Mòbils
- Tablets
- Escriptori

Sense scroll horitzontal i mantenint coherència visual.

---

## NOTES

- Es manté la tècnica original de maquetació (flex/grid).
- No es reescriuen estils innecessàriament.
- Es prioritza reutilització i herència CSS.
