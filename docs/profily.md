## Vytvoření nového aplikačního profilu
Než začneme v Dataseceru vytvářet samotný aplikační profil pro náš repozitář, je nutné se podrobně seznámit s výchozím metadatovým modelem. [Czech core metadata model](https://eosc-cz.github.io/CCMM/cs/)
1. Zjistíme si jaké prvky výchozí metadatový model obsahuje.

2. Rozmyslíme si co jaké prvky z výchozího metadového převezmeme a jakým způsobem je budeme používat, upravovat, Nastavíme pravidla jak je budeme používat (zda budou povinné v metadatovém popisu, kardinalitu apod.)

3. V případě, že potřebujeme podrobnější metadatový popis než umožňuje si výchozí metadatový model, musíme si nadefinovat nové prvky ve slovníku. 


![Výběr typu projektu – Aplikační profil](img/vytvorit_aplikacniprofil.png)

V hlavním menu zvolte možnost „Průvodce projektem“ – Vytvořit aplikační profil.

1. Zadejte **název projektu** (např. „CCMM AP“).

2. Vložte **URL specifikaci** modelu, ze kterého chcete aplikační profil vytvořit.  
   Pokud vytváříte aplikační profil pro CCMM, vložte link na něj:  
   [https://eosc-cz.github.io/CCMM/cs/](https://eosc-cz.github.io/CCMM/cs/)


3. Vyplňte **Base IRI** – základní IRI (Internationalized Resource Identifier),  
   pod kterým budou identifikovány prvky vašeho profilu:  

   **Poznámka:** Doporučujeme promyslet předem; lze jej však později upravit.
Záložka *profile* obsahuje všechny slovniky použité ve výchozím metadatovém modelu.
Mohu si zobrazit co obsahuje zvolený slovník.

   [https://example.com/profile/mujprofil/](https://example.com/profile/mujprofil/)


![Slovniky](img/slovniky.png)



![Zobrazeni](img/zobrazenimodel.png)
![Vizuální model](img/vizualni_model.png)


## ▶️ Definice tříd zahrnutých do aplikačního profilu

Po vytvoření nového aplikačního profilu se nám otevře editor aplikačního profilu.

Záložka *profile* obsahuje všechny prvky použité ve výchozím metadatovém modelu.

Zvolím položku, kterou chci přidat do mého aplikačního profilu (např. Agent).  
Klikneme na **Create new profile** (symbol podkovy).

Rozhodneme se, zda chceme třídu převzít tak, jak je definována ve výchozím metadatovém modelu, nebo ji budeme upravovat.

**Name:** Pojmenování třídy.

**IRI** *(International Resource Identifier)* Identifikátor třídy.

**Specialization:** Zda se jedná o specializaci jiné třídy.

**Definition:** Stručný popis dané třídy. Možné uvést i v několika jazycích.  
**Příklad:** Agent: Any entity carrying out actions with respect to the entities Catalogue and the Catalogued Resources.*

**Usage note:** Poznámka k použití dané třídy. Př. "V tomto profilu se dataset pooužívá pro XYZ."

**External documentation:** Odkaz na externí dokumentaci popisující danou třídu.

**Role:** Určím se zda bude role hlavní (main) nebo podpůrná (supportive). Hlavní role jsou důležité prvky metadatového profilu př. dataset, katalog. Podpůrná zahrnuje méně důležité např. téma. Role se nedědí mezi profily.

Vlevo vidím katalog - třídy v aplikačním profiu. Přidané jsou vybarvené zeleně. Vpravo je vizuální model.
![Zobrazení třídy](img/katalog_vizualni.png)

## ▶️ Přidání atributů
U tříd je následně třeba přidat atributy.
1. Atribut přidám symbolem plus. 

2. Nadefinujte si pro z čeho vycházíte **Profile of** a pro jakou třídu atribut definujete **Domain**

![Atribut](img/atribut.png)

## ▶️ Přidání vztahů mezi třídami
Nyní si přidáme do svého profilu další třídu (funding reference).
V části relationsh přidám vztah mezi těmito třídami (has funding reference).
![Relationship](img/relationship_profile.png)
1. Atribut přidám symbolem plus.

2. Nadefinujte si pro z čeho vycházíte **Profile of** a pro jakou třídu atribut definujete **Domain**


![Atribut](img/atribut.png)

## ▶️ Nadefinování vlastních pojmů ve Slovníku

V případě, že chci do aplikačního profilu přidat vlastní prvky které nejsou součástí CCMM, nadefinuji si je ve slovníku. 

![Slovnik](img/slovnik_novy.png)

Můžu využít často používaných slovníků (well known vocabularies), importovat slovník prostřednictvím url (vocabulary from url), případně si nadefinovat vlastní.

![Pridat](img/add_vocabulary.png)

Vytvořím si nový slovník a přidám nové pojmy (symbol plus). Musím vyplnit název, IRI a definici. 
Následně se nadefinované pojmy přidám do aplikačního profilu.

![Slovnik](img/slovnik_class.png)






