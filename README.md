# Metodika pro správu metadatových profilů
Metodika pro správu metadatových profilů.

Tvořena je v nástroji [MkDocs](https://www.mkdocs.org/) s pluginy [`mkdocs-material`](https://squidfunk.github.io/mkdocs-material/) a [`mkdocs-static-i18n`](https://github.com/ultrabug/mkdocs-static-i18n).

Pro lokální vvývoj je tedy třeba:
1. Mít nainstalovaný Python alespoň 3.11, `pip` a `venv`.
2. Naklonovat repozitář `git clone git@github.com:LIBCAS/Metodika-Dataspecer.git`
3. `cd Metodika-Dataspecer`
4. Vytvořit virtuální prostředí `python3 -m venv .venv`
5. Aktivovat virtuální prostředí `source .venv/bin/activate`
6. Nainstalovat MkDocs: `pip install mkdocs`
7. Nainstalovat `mkdocs-material`: `pip install mkdocs-material`
8. Nainstalovat `mkdocs-static-i18n`: `pip install mkdocs-static-i18n`
9. Spustit `mkdocs serve` pro vvojové prostředí
10. Spustit `mkdocs gh-deploy` pro publikaci do branche `gh-pages` a tedy na web

# Acknowledgments

<p align="left">
  <img src="https://webcentrum.muni.cz/media/3831863/seda_eosc.png" alt="EOSC CZ Logo" height="90">
</p>

---
This project output was developed with financial contributions from the [EOSC CZ](https://www.eosc.cz/projekty/narodni-podpora-pro-eosc) initiative through the project **National Repository Platform for Research Data** (CZ.02.01.01/00/23_014/0008787) founded by Programme Johannes Amos Comenius (P JAC) of the Ministry of Education, Youth and Sports of the Czech Republic (MEYS).

---

<p align="left">
  <img src="https://webcentrum.muni.cz/media/3832168/seda_eu-msmt_eng.png" alt="EU and MŠMT Logos" height="90">
</p>
