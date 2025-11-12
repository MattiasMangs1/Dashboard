# 📊 Dalarnas näringsliv 2019–2024  
Ett Power BI-projekt som analyserar hur företagen i Dalarna utvecklats i omsättning, tillväxt och finansiell hälsa mellan 2019 och 2024.


---

## 🎯 Syfte

Målet med projektet är att skapa en tydlig och interaktiv visualisering av hur Dalarnas företag har utvecklats under en period präglad av stora ekonomiska förändringar – från pandemin till energikris och räntehöjningar.

Analysen fokuserar på tre huvudområden:

- **Tillväxt:** Hur har omsättningen utvecklats över tid?  
- **Struktur:** Hur skiljer sig utvecklingen mellan branscher och kommuner?  
- **Finansiell hälsa:** Hur starka, likvida och lönsamma är företagen?

---

## 🧩 Databearbetning och modellering

Data hämtades ur årsredovisningar för företag med säte i Dalarna (sekundärdata).  
Bearbetningen utfördes i **Power Query**, där fokus låg på att bygga en **ren och enhetlig datamodell**.  
Arbetet omfattade bland annat:

- Sammanställning av data från flera årsflikar (2019–2024).  
- Rensning av symboler, tomma värden och oönskade kolumner.  
- Typkonvertering och trimning av textvärden.  
- Konvertering av procentvärden till decimaler (ex. 56 → 0,56).  
- Uppskalning av monetära värden (tkr → kr) för att möjliggöra presentation i **miljarder kronor (Mdr)** via DAX.  
- Tillägg av årskolumn och kombination till en samlad datatabell.  
- Skapande av en enkel stjärnmodell bestående av:
  - `Financials` (faktatabell)
  - `dimYear` (hjälptabell för tidsfiltrering)

Bearbetningen genomfördes uteslutande i Power Query för datarensning och Power BI för modellering och beräkningar.

---

## 🧮 Mått och nyckeltal i fokus

| Typ | Nyckeltal | Definition |
|------|------------|------------|
| **Tillväxt** | **Total omsättning (Mdr)** | Summering av företagens omsättning uttryckt i miljarder SEK (DAX: division med 1 000 000 000) |
| | **Omsättningstillväxt YoY (%)** | Årlig tillväxt jämfört med föregående år |
| | **Omsättning CAGR fr. 2019 (%)** | Genomsnittlig årlig tillväxt sedan 2019 |
| **Lönsamhet** | **Median rörelsemarginal (%)** | Rörelseresultat i relation till omsättning |
| **Finansiell styrka** | **Median soliditet (%)** | Andel eget kapital av totala tillgångar |
| **Likviditet** | **Median kassalikviditet (%)** | Kortsiktig betalningsförmåga |
| **Risk** | **Median skuldsättningsgrad (%)** | Skulder i relation till eget kapital |

---

## 💡 Övriga datafält (ej visualiserade)

Datasetet innehåller även kompletterande nyckeltal som:  
EBITDA, resultat efter finansnetto, årets resultat, omsättning per anställd och antal anställda.  
Dessa användes inte i visualiseringarna eftersom fokus låg på att analysera övergripande tillväxt och finansiell hälsa.  
De ger däremot möjligheter för vidareutveckling — t.ex. analyser av produktivitet eller marginalförändringar.

---

## 📊 Rapportens struktur

Rapporten består av fyra huvudsidor:

### 1️⃣ Dalarnas näringsliv 2019–2024  
!['Page 1'](/Project_Dalarna/bilder/Page1.png)

**Frågor som besvaras:**  
- Hur snabbt växer Dalarnas företag?  
- Hur har soliditet och lönsamhet förändrats över tid?  


---

### 2️⃣ Branschanalys 
!['Page 2'](/Project_Dalarna/bilder/Page2.png)


**Frågor som besvaras:**  
- Vilka branscher driver tillväxten?  
- Hur starka och lönsamma är de?  


---

### 3️⃣ Kommunanalys  
!['Page 3'](/Project_Dalarna/bilder/Page3.png)


**Frågor som besvaras:**  
- Vilka kommuner står för den största ekonomiska aktiviteten?  
- Var i Dalarna finns tillväxten och styrkan?  

---

### 4️⃣ Finansiell hälsa  
!['Page 4'](/Project_Dalarna/bilder/Page4.png)

**Frågor som besvaras:**  
- Har företagen blivit mer kapitalstarka?  
- Hur har skuldsättningen och likviditeten förändrats?  
- Hur hänger lönsamhet och soliditet ihop?  


---

## 🧰 Teknisk översikt

| Komponent | Verktyg / metod |
|------------|----------------|
| Databearbetning | Power Query (M-kod) |
| Modellstruktur | Enkel stjärnmodell: `Financials` ↔ `dimYear` |
| DAX-beräkningar | YoY, CAGR, medianmått, Mdr-omräkning |
| Visualiseringar | KPI-kort, kombinationsdiagram, bubbeldiagram, karta |
| Enheter | Miljarder SEK (Mdr) och procent (%) |
| Delning | `.pbix`-fil via GitHub |

---




## 🧑‍💻 Om projektet

Projektet är utvecklat av **Mattias Mångs**  
Syftet är att kombinera företagsekonomisk förståelse med datadrivna verktyg för att visualisera regionala ekonomiska mönster.

---

## 🔗 Länkar

- 📬 [LinkedIn – Mattias Mångs](https://www.linkedin.com/in/mattias-mangs/)  

