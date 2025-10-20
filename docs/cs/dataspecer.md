# Nástroj pro správu metadatových profilů: Dataspecer
Dataspecer je nástroj pro tvorbu, správu a vizualizaci sémantických datových specifikací, tj. slovníků a aplikačních profilů.
Na jejich základě je možné také odvozovat další technické artefakty, zejména datová schémata (XML, JSON, CSV).

## Možnosti spuštění

Aplikaci můžete vyzkoušet na [demo instanci](https://demo.dataspecer.com/).

- Kdokoli může Dataspecer otestovat lokálně pomocí Dockeru.
- Pomocí Dockeru je možné Dataspecer nasadit lokálně na serveru.

Podrobnější informace o spuštění pomocí Dockeru naleznete na
[GitHubu Dataspeceru](https://github.com/dataspecer/dataspecer?tab=readme-ov-file#docker-container).

## Správce projektů
V rozhraní Dataspecer se specifikaci říká projekt.
![Správce projektů](../assets/images/manager.webp)

Základním rozhraním je správce projektů.
Každý slovník a každý aplikační profil je samostatným projektem.
Projekt lze rozkliknout a vidět jeho vnitřní strukturu, to však nebudeme potřebovat.

## Možnosti projektu

![Možnosti projektu](../assets/images/další_možnosti.webp)

- **Exportovat specifikaci** stáhne specifikaci vytvořeného slovníku/aplikačního profilu ve formě zip archivu k publikaci na webu, např. na [GitHub Pages](https://pages.github.com).
- **Zobrazit dokumentaci (cs/en)** zobrazí náhled dokumentace k vytvořené specifikaci v angličtině či češtině, viz [generovaná dokumentace](#generovana-dokumentace).
- **Upravit šablonu dokumentace** Otevře se HTML editor, kde lze editovat vzhled šablony vytvářené dokumentace. Ta využívá systém [ReSpec](https://respec.org/docs/).
- **Importovat z URL** umožní přidat existující slovník či aplikační profil vytvořený v Dataspeceru do aktuální specifikace.
- **Zálohovat do souboru** stáhne zálohu projektu ve formě ZIP archivu, který lze na libovolné Dataspecer instanci opět nahrát pomocí tlačítka Import. Nelze však takto nahrát zálohu na instanci, kde již importovaný projekt existuje.
- **Duplikovat** Vytvoří kopii projektu.   
- **Rename** přejmenuje projekt.  
- **Upravit data modelu** slouží pro debugování, nebudeme potřebovat.
- **Odstranit** vymaže projekt.

## Nová specifikace
Pro vytvoření nové specifikace klikneme na tlačítko Průvodce projektem.
![Nový projekt](../assets/images/nový_projekt.webp)

A zvolíme jednu z možností:
![Průvodce projektem](../assets/images/průvodce_projektem.webp)

Jak slovník, tak aplikační profil je tvořen v [**editoru modelu**](editor-modelu.md).

[**Slovník**](slovníky.md) vytváříme v případě, že potřebujeme definovat nové pojmy - třídy a vlastnosti.

[**Aplikační profil**](aplikační-profily.md) vytváříme, pokud chceme specifikovat použití částí jiných specifikací v našem konkrétním kontextu. Například pokud vytváříme aplikační profil CCMM pro konkrétní doménový repozitář.

**Datové schéma** slouží pro tvrobu datových struktur přímo na základě existujících slovníků. Tuto volbu nebudeme používat.

## Generovaná dokumentace
![Dokumentace](../assets/images/dokumentace.webp)
Generovaná dokumentace používá systém [ReSpec](https://respec.org/docs/) tak, jako běžné webové specifikace.
Obsahuje dokumentaci slovníku či aplikačního profilu, včetně odkazů na jednotlivé koncepty v přepoužitých slovnících a aplikačních profilech.
Dále obsahuje přílohy se strojově čitelnou reprezentací specifikace, případně s technickými artefakty.
Dokumentace je připravena k publikaci na webu, např. na [GitHub Pages](https://pages.github.com).