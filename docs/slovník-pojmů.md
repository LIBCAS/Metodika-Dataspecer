Slovník pojmů obsahuje přehled základních pojmů používaných při datovém modelování v [nástroji Dataspecer](dataspecer.md).

## Aplikační profil
V metadatovém modelování je aplikační profil (application profile) specializovaný soubor pravidel a specifikací, který upravuje používání existujících metadatových schémat nebo standardů pro konkrétní účel, doménu nebo organizaci. Nejedná se tedy o nový metadatový standard, ale o kombinaci a úpravu již existujících prvků tak, aby vyhovovaly specifickým potřebám.

## Atribut (attribute)
V datovém modelování představuje atribut konkrétní vlastnost třídy (entity), která popisuje určitý detail nebo aspekt její instance. Každý atribut má určený název, datový typ a může mít i další pravidla, jako je povinnost vyplnění nebo opakovatelnost. Například ve třídě Address (adresa) mohou být atributy jako full address (úplná adresa), post code (poštovní směrovací číslo), post name (název pošty), locator designator (číselné označení, např. číslo popisné), nebo locator name (název ulice). Atribut latitude (zeměpisná šířka) a longitude (zeměpisná délka) zase patří ke třídě Geometry a slouží k prostorovému určení adresy. Každý z těchto atributů zachycuje konkrétní informaci o adrese a společně tvoří strukturovaný popis dat, který lze jednoznačně interpretovat a strojově zpracovávat. Například konkrétní adresa může mít post code = „110 00“, locator name = „Národní“ a latitude = „50.087“ – každý z těchto údajů je hodnotou přiřazenou ke svému atributu.

## International resource identifier (IRI)
Jednoznačný identifikátor sloužící k označení zdrojů na webu, který na rozdíl od URI (Uniform Resource Identifier) umožňuje použití znaků z plné znakové sady Unicode – tedy i písmen s diakritikou, cyrilice, čínských znaků apod.
IRI se používá zejména v prostředí sémantického webu, RDF, ontologií a metadatových modelů, kde zajišťuje globálně unikátní a čitelnou identifikaci pojmů, tříd nebo instancí.
Př. `https://data.město.cz/osoby/Jiří_Černý`

##  Cross-Origin Resource Sharing (CORS)  
**Cross-Origin Resource Sharing (CORS)** je bezpečnostní mechanismus využívající HTTP hlavičky, který umožňuje webovým aplikacím přistupovat ke zdrojům (např. API nebo datovým sadám) na jiných doménách, než na kterých byly načteny. Standardně prohlížeče takové přeshraniční požadavky omezují kvůli ochraně uživatelských dat, ale pomocí CORS může server výslovně povolit přístup z jiných důvěryhodných domén. Tento mechanismus je důležitý zejména při zpřístupňování otevřených dat pro koncové uživatele nebo frontendové aplikace. Chování CORS je popsáno ve [specifikaci Fetch Standard (WHATWG)](https://fetch.spec.whatwg.org/#http-cors-protocol) a praktické vysvětlení i příklady najdete na [Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CORS).

## Kardinalita
Kardinalita v datovém modelování určuje, kolikrát může nebo musí být určitý vztah nebo vlastnost mezi dvěma třídami použit. Jinak řečeno, popisuje počet výskytů, které jsou povolené nebo požadované mezi objekty.

Například pokud má datová sada (Dataset) vlastnost title, kardinalita 1..1 znamená, že musí mít právě jeden název. Pokud by byla kardinalita 0..*, může mít žádný, jeden nebo více názvů.

Kardinalita se často zapisuje ve formátu:

0..1 – nejvýše jeden výskyt (nepovinný),

1..1 – právě jeden výskyt (povinný),

0..* – libovolný počet výskytů (včetně nuly),

1..* – alespoň jeden výskyt.

## RDF
(Resource Description Framework) je standard pro reprezentaci dat, který slouží k popisu informací pomocí trojic ve tvaru subjekt–predikát–objekt. Každá trojice vyjadřuje jedno tvrzení o nějakém zdroji, přičemž všechny prvky mohou být jednoznačně identifikovány pomocí URI. RDF se často používá k propojování dat z různých zdrojů a tvoří základ sémantického webu. Například trojice <http://example.org/JanNovak> <http://schema.org/jobTitle> "analytik" říká, že Jan Novák má pracovní pozici analytik. RDF se často zapisuje ve formátu TTL (Turtle). Například zápis ex:JanNovak schema:jobTitle "analytik" říká, že Jan Novák má pracovní pozici „analytik“. 

## Sémantické datové specifikace
Sémantická datová specifikace je formální popis datové struktury, který kromě technické definice dat (např. typy, atributy, vztahy) zahrnuje také význam těchto dat v konkrétním doménovém kontextu. Cílem je zajistit jednoznačnou interpretaci a správné porozumění datům napříč různými systémy, organizacemi i uživateli. Taková specifikace často využívá standardy jako ontologie, datové slovníky nebo modely typu RDF/OWL, které umožňují propojení dat s jejich sémantikou a tím podporují interoperabilitu, validaci a automatizované zpracování.

## Slovník
Slovník je kolekce formálně definovaných pojmů (např. tříd, atributů a vztahů), které slouží pro popis datových struktur a metadat. Slovník obsahuje konkrétní sémantické prvky, které lze znovu používat napříč různými datovými modely. Ve slovníku jsou pojmy jednoznačně identifikovány (např. URI) a často vycházejí z existujících standardů (např. DCAT, Dublin Core, DataCite, FOAF).

## Třída (class)
Třída v datovém modelování označuje typ objektů, které sdílejí stejné vlastnosti a význam. Používá se k popisu kategorií dat, jako jsou např. osoby, adresy, dokumenty nebo distribuční soubory. Každý konkrétní objekt v datech je instancí nějaké třídy. Třídy mohou být hierarchicky uspořádány (např. podtřídy) a mohou mít přiřazené atributy a vztahy.


## Vztah
Popisuje vztahy mezi 2 třídami aplikačního profilu. 
Př. Dataset has funding reference. 