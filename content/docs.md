---
Title: Docs
Description: Documentation regarding design
hidden: true
Template: docs 
---

# Dokumentation


## Färgpaletten:
------
Jag skulle påstå att färgschemat till det primära temat är ett **komplementärt** (alternativt ett **split-komplementärt**?) i och med att den färg som är genomgående bakgrundsfärg ligger mittemot accentfärgen. Dessa två färger kompletteras sedan av tre mer balanserade färger - en vit och en nästintill svart vilka används till text, samt en ljust orange som används till länkar. 

Den blågröna färgen har jag valt då jag anser att den känns rätt lugn men ändå lutar åt professionalism och lite modernitet i och med just kombinationen av blått och grönt.
Den orangea accentfärgen skulle jag säga utstrålar både värme och kreativitet utan att bli alltför stark i kontrast till bakgrundsfärgen - men samtidigt tillräcklig kontrast för att dra till sig blicken till elementen den sätts på vilka främst är knappar vilka leder till relevanta sidor.

### Färgschema och -hjul

![Bild på färghjul](image/wheel.png){.wheel}



| Variabelnamn       | Färg                   
|--------------------|------------------------------------|
| `$font-color`      | <span style="background-color:#fff; color:#000;  padding:5px 10px; display:inline-block; border:1px solid #ccc;">#fff</span>      
| `$font-alt-color`  | <span style="background-color:#333; color:#fff;  padding:5px 10px; display:inline-block; border:1px solid #ccc;">#333</span>  
| `$background-color`| <span style="background-color:#2c727f; color:#fff;   padding:5px 10px; display:inline-block; border:1px solid #ccc;">#2c727f</span>
| `$accent-color`    | <span style="background-color:#faac6c; color:#000;  padding:5px 10px; display:inline-block; border:1px solid #ccc;">#faac6c</span>
| `$link-color`      | <span style="background-color:#ffe5cf; color:#000;  padding:5px 10px; display:inline-block; border:1px solid #ccc;">#ffe5cf</span>


## Typografi:
------

Jag valde att till rubriker och interna länkar (till exempel navbaren) använda en font-familj som sticker ut och kontrasterar mycket från den som används till brödtexten. 

Fonten heter **Barrio** och känns lite lekfull och inbjudande och är satt att vara markant större än brödtexten som använder den simpla men omtyckta **Arial**  - dels för att skapa en hierarki mellan de olika texterna, men även för att den ska vara lättare att läsa.


## Designprinciper och -element:
------

Sidan har genomgående samma bakgrundsfärg, font-familj när det gäller rubriker, interna länkar samt brödtext vilket skapar en känsla av **enhetlighet** och **repetition**. **Hierarki** uppstår tydligt då rubriker och interna länkar dels har ett markant annorlunda typsnitt men även i storlek.

Jag har försökt arbeta med ganska mycket **white/negative-space** då bakgrundsfärgen är rätt stark och jag anser det vara än mer viktigt att då ge användaren rum för att ta in allt. Även **inramning** är något jag försökt tänka på, dels i highlights sidan där varje arbete är inramat, men även för de interna länkar på till exempel about-sidan där varje sådan drar till sig uppmärksamhet.
På about-sidan skulle jag även säga att det är en tydlig **symmetri**. Sidan består av dels en text men även länkar men med hjälp av ett gridsystem tar de upp lika mycket plats. 





## Känslan kunden vill förmedla:
------

Kunden vill ge en känsla av inbjudande lekfullhet och professionalism. Han kan leverera rustika produkter som inte för det behöver vara färglösa eller stela.


## Uppdelning av SASS:
------

Jag valde att arbeta med nya standarden @use istället för @import och har därmed skapat en folder med namnet variables vilken innehåller filerna **_variables** där jag definierat alla färger samt font-familjet som används och **_index**. 
Jag har min **style.scss** vilken “drar ihop” alla SCSS-filer jag vill att sidan skall använda.
**base.scss** består främst av grundläggande styling som används på i alla sidor som påverkar body, html, * och .main. I huvudsak handlar det om regler för placering vilken sätts med flex, line-height, en grundläggande font-size, box-sizing och overflow.

Jag valde sedan att dela upp mina filer på ett sätt som gör att namnet avspeglar vilket content som berörs. Jag velade om jag skulle göra så eller istället bryta upp i filer som till exempel links.scss, borders.scss, content.scss. Det känns som att alternativ två på ett sätt hade gjort det lite enklare att underhålla och återanvända - nu har jag istället flyttat en del återkommande styling/class:er till base.scss.

Som det är nu har jag alltså en scss-fil för varje typ av content/include, tex header.scss, highlights.scss, contact.scss och så vidare.
