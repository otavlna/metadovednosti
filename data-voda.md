# Téma 1 – úniky vody z vodovodů: ověřená data

Zdroj (hlavní): MZe – *Vodovody, kanalizace ČR 2024* (Praha 2025), kap. 2 a 5
https://mze.gov.cz/public/portal/mze/-a83602---ZT_TAmq0/vodovody-kanalizace-cr-2024.-ekonomika-ceny-informace

## ČR 2024
| Ukazatel | Hodnota | Kde |
|---|---|---|
| Voda vyrobená určená k realizaci | 593,5 mil. m³ | tab. 5.1.3 |
| Nefakturovaná voda | 104,7 mil. m³ (17,6 %) | tab. 5.1.3 |
| z toho ztráty v trubní síti | **89,6 mil. m³ (15,1 %)** | tab. 5.1.3 |
| Ztráty na 1 km sítě | 2 918 l/km/den (1 065 m³/km/rok) | tab. 5.1.3, 5.1.4 |
| Ztráty na obyvatele | 23,6 l/os/den | tab. 5.1.3 |
| Délka vodovodní sítě | 83 867 km | tab. 5.1.4 |
| Obnoveno v roce 2024 | 332 km = **0,40 % sítě** | kap. 2.2 |
| Průměrná cena vodného (skupina 50) | 59,78 Kč/m³ bez DPH | tab. 3.2.4 |

Trend: ztráty 2015 → 2024: 16,8 % → 15,1 % (minimum 14,5 % v 2019), od 2023 opět mírně rostou.

## Odvozené (náš výpočet – v prezentaci označit jako odhad)
- 89,6 mil. m³ × 59,78 Kč ≈ **5,4 mld. Kč/rok** v prodejní ceně vody (horní odhad – skutečné náklady vodáren na ztracenou vodu jsou nižší, viz pozn.).
- Obnova 0,40 % sítě ročně → celá síť by se vyměnila za **~250 let**. → nelze měnit vše, je nutné **cíleně vybrat nejhorší úseky** = prostor pro predikci (AI).
- 89,6 mil. m³ ≈ roční fakturovaná spotřeba ~2,8 mil. obyvatel (89,6 mil. m³ / 88,3 l/os/den domácnosti) – dobré do videa.

## Pozor (pro Monitory / obhajobu)
- MZe samo píše, že náklady na vodu jsou převážně fixní, takže ztráty se do ceny promítají „pouze v řádech procent“ a razantní preventivní zásahy můžou cenu vodného i zvýšit. → ROI stavět hlavně na **cílené obnově a méně haváriích**, ne jen na ceně ušetřené vody.
- Od 2024 jsou data z MZe místo ČSÚ → meziroční srovnání 2023/2024 může mít statistické odchylky.

## Regulace – směrnice EU o pitné vodě 2020/2184, čl. 4 odst. 3 (ověřeno v textu)
- státy musí posoudit úniky vody metodou **ILI** (Infrastructure Leakage Index) aspoň u dodavatelů ≥ 10 000 m³/den nebo ≥ 50 000 obyvatel
- výsledky poslat Komisi **do 12. 1. 2026** (už proběhlo)
- Komise **do 12. 1. 2028** stanoví unijní **práh úniků**; kdo ho překročí, musí do 2 let předložit **akční plán** na snížení
- → vodárny budou v příštích letech pod tlakem úniky měřit a snižovat = „proč teď“ do videa
- zdroj: https://gesetze.legal/eu/rl_2020_2184_eu/4 (text směrnice; oficiálně EUR-Lex 32020L2184)

## Havárie a jejich náklady (jen jednotlivé případy, celostátní průměr neexistuje veřejně)
- Praha (PVK): 5 208 poruch na vodovodní síti za rok (~2018) – https://www.tzb-info.cz/124488-sucho-zapricinilo-narust-poctu-havarii-na-vodovodni-siti-ztraty-vody-na-minimu
- Kraslice: jedna havárie, >1 200 obyvatel bez vody, opravy >300 tis. Kč – https://www.kmssro.cz/poruchy-a-odstavky/havarie-na-vodovodu-kanalizaci/havarie-vodovodu-v-kraslicich-dusledky-opravy-a-budouci-prace-81cs.html
- Turnov (VHS, 2022): havarijní oprava 393 tis. Kč (údaj z PDF, nejistý) – https://www.vhsturnov.cz/wp-content/uploads/2023/10/rocni-zprava-vhs-2022-1.pdf
- Plzeň 2026: výměna 200 m potrubí kvůli **opakovaným** haváriím ~12 mil. Kč – https://www.plzen.cz/vodarna_v_plzni_vymeni_pres_200_metru_potrubi_oprava_za_12_milionu_ma_zabranit_dalsim_havariim
- → do prezentace: „jedna havárie stojí řádově stovky tisíc Kč“ (s uvedením, že jde o příklady)

## Existující řešení / konkurence (důležité pro inovativnost!)
- **Praha už používá satelit:** PVK + izraelská firma **Utilis** (dnes Asterra), radar SAR z družice JAXA. 2020: 45 podezřelých míst, **26 potvrzených úniků**; 2021: 207 míst na 111 km z ~1 000 km skenované sítě. Ztráty PVK 2020: 12,91 % (před 20 lety přes 1/3). – https://energozrouti.cz/clanek/prazske-vodovody-kontroluji-ztraty-pitne-vody-za-pomoci-satelitu
- PVK používá i **SmartBall** (akustická koule v potrubí), data se vyhodnocují v zahraničí ~4 týdny – https://www.seznamzpravy.cz/clanek/pod-prahou-se-prohani-chytra-koule-monitoruje-potrubi-a-hleda-uniky-156575
- Zahraniční firmy: Gutermann (ZONESCAN AI nad akustickými loggery), Sewerin (SePem – únik do 3 dnů), Xylem/Sensus, Ovarro, TaKaDu, Electro Scan (SaaS na AWS).
- Akustický logger pokrývá cca okruh 150 m (Yorkshire Water) – https://www.waterindustryjournal.co.uk/?p=6174
- Ceny: veřejně **nejsou** (jen nabídky na míru). Marketingový údaj USA: pilot od 100 USD/logger + instalace – https://www.wateronline.com/doc/leak-detection-pilot-program-0001 → v unit economics pracovat s **předpoklady** a označit je.
- Protiargument: srovnání v Atlantě uvádí, že klasická akustická detekce vyšla nákladově lépe než AI satelit (netto přínos 2,4 mil. USD / 3 roky) – zdroj neověřen přímo (MDPI Smart Cities 8/4/122, přístup 403).

## Co z toho plyne pro náš návrh
- Velké vodárny (Praha) technologie mají → **cílit na malé a střední vodárny a obce**, které si drahé zahraniční řešení nekoupí. V ČR je **8 689 vlastníků a 3 211 provozovatelů** vodovodů a kanalizací (MZe 2024, tab. 2.1.1) = velký trh.
- Odlišení: kombinace **otevřených/levných dat** (satelit, data z vodoměrů a tlaků, stáří a materiál potrubí z majetkové evidence, počasí/mráz, doprava) → **AI predikce, které úseky obnovit nejdřív** (ne jen hledat existující úniky).
- Pomoc s povinným **reportingem ILI** pro EU jako vedlejší služba.

## Další zdroje
- ČSÚ – Domácnosti vodou nadále šetří (data 2023: ztráty 85,1 mil. m³, 14,8 %): https://csu.gov.cz/produkty/domacnosti-vodou-nadale-setri-v-prumyslu-jeji-spotreba-mirne-roste
- ČSÚ – regionální data 2024 (např. Liberecký kraj 19,6 % ztrát): https://csu.gov.cz/lbk/vodovody-a-kanalizace-v-libereckem-kraji-v-roce-2024
- MZe – Modrá zpráva 2024: https://mze.gov.cz/public/portal/mze/-a83826---x6C71AZZ/modra-zprava-2024
- EEA – drinking water distribution losses (srovnání EU): https://www.eea.europa.eu/en/analysis/maps-and-charts/drinking-water-distribution-losses
- Směrnice EU o pitné vodě: státy musí do 1/2026 vyhodnotit úniky a reportovat EK (regulační tlak = příležitost) – ověřit v textu směrnice 2020/2184.
