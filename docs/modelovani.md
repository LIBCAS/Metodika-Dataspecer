# Problematika modelování dat
<<<<<<< HEAD
## Slovník pojmů
###▶️ Aplikační profil
Aplikační profil je
###▶️ Atribut
###▶️ Číselník
###▶️ Datové schéma
###▶️ IRI
###▶️ Slovník
###▶️ Vizuální model
###▶️ Vztah




=======

## Základy modelování dat

Představme si velkou doručovací společnost, která pracuje se zákazníky a jejich objednávkami. Interně potřebuje společnost sledovat své pracovníky, sklady a vozidla, která zajišťují doručení zboží. I když se jedná o zjednodušený scénář, můžeme již vytvořit jednoduchý diagram popisující vztahy mezi zmíněnými entitami – tzv. doménovou ontologii.

Vývojáři softwaru používají tento popis spolu s dalšími informacemi k vytvoření databází a interních systémů, které slouží k provozu společnosti, vytváření objednávek a distribuci zboží mezi různá doručovací vozidla.

Obvykle se vytváří více menších systémů, jako například webová stránka pro zákazníky, systém pro pracovníky ve skladech, mobilní aplikace pro doručovatele atd. Aby tyto aplikace, weby a další systémy společnosti mohly mezi sebou sdílet informace, musí se obě strany dohodnout na společném formátu a technologii. Nejčastěji používané technologie pro výměnu dat jsou **XML**, **JSON**, **RDF** nebo **CSV**.

Formát, nebo technicky řečeno **schéma**, specifikuje, jak by měla být data strukturována – popisuje názvy polí, datové typy, pořadí entit atd.

---

## Příklady serializačních technologií a různých schémat

### Ukázková data o zákazníkovi ve formátu **JSON**

```json
{
  "name": "John",
  "surname": "Doe",
  "age": 35
}
>>>>>>> origin
