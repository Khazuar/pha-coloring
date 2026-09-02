# Modell: Färbung und Klärung von tPHA mit Krapp

Zusammenstellung der bisherigen Erkenntnisse als Nachschlagewerk, nicht als
Versuchsprotokoll. Gültig für gesättigtes Färbebad mit Feststoffvorrat,
F�rbe-pH 5, ausreichende Nachlieferrate. Plättchen: 28 mm Ø, 1 mm stark,
13,2 cm² Oberfläche, 0,616 cm³, ~0,74 g. Temperaturen in °C, Zeiten in
Sekunden, sofern nicht anders angegeben. Versuchsbezeichnungen (V3, V4 …)
dienen nur als Belegverweis, nicht als Gliederung.

---

## 1. Schichtdicke (Färbung)

$$d(T,t) = 80\,\mu\text{m} \cdot \sqrt{\frac{t}{1800\,\text{s}}} \cdot \exp\left[-\frac{E_a}{2R}\left(\frac{1}{T+273{,}15} - \frac{1}{358{,}15}\right)\right]$$

mit **Ea = 66,8 kJ/mol** — bestimmt aus zwei Schnittkantenmessungen
(34,5 µm bei 60 °C, 80 µm bei 85 °C, je 30 min), unabhängig bestätigt durch
die aus der Colorimetrie bestimmte Ea von 72,9 kJ/mol (Abschnitt 5).

| T | 30 min | 60 min |
|---|---|---|
| 60 °C | 34,5 µm | 48,8 µm |
| 70 °C | 48,9 µm | 69,2 µm |
| 80 °C | 68,2 µm | 96,4 µm |
| 85 °C | 80,0 µm | 113 µm |
| **90 °C** | **93,4 µm** | 132 µm |

Die 90-°C-Zeile ist eine bestätigte Extrapolation (Abschnitt 5), nicht
Kalibrierung. Der früh gemessene Wert von 300 µm für die Sättigungsfärbung
(10 h/68 °C) ist mit diesem Modell auf ~205 µm zu korrigieren — die damalige
Ablesung nutzte bei viel höherer Farbstoffkonzentration eine andere
Sichtbarkeitsschwelle.

---

## 2. Chelatisierungsgrad während der Färbung

$$\theta_{30}(T) = 0{,}01847 \cdot T - 1{,}0936 \qquad (r = 0{,}990)$$

$$\theta(T,t) = \theta_{30}(T)\cdot\sqrt{\frac{t}{1800\,\text{s}}}, \quad \text{begrenzt auf } [0;1]$$

| T | θ nach 30 min |
|---|---|
| 60 °C | 1,4 % |
| 70 °C | 19,9 % |
| 80 °C | 38,4 % |
| 85 °C | 47,6 % |
| **90 °C** | **56,8 %** |

Gilt für Färbung bei **pH 5**. Bei anderem Färbe-pH ist dieser Verlauf nicht
belegt (offener Punkt, siehe Abschnitt 8).

**Der Zeitterm ist die schwächste Stelle.** Er stützt sich auf einen
einzigen Punkt (10 h/68 °C ergab θ = 0,677 statt der von der 30-min-Gerade
vorhergesagten 0,162; das ergibt einen Zeitexponenten von 0,477, also
näherungsweise √t — plausibel, aber nicht durch eine echte Zeitreihe belegt).

Bei langer Färbezeit (10 h) wird ein erheblicher Teil der Chelatisierung
bereits während des Färbens erreicht (θ bis 0,84 gemessen) — das Färbebad
wirkt dann selbst wie eine langsame Klärung. Bei kurzer, heißer Färbung
(Zielszenario dieses Projekts) bleibt θ dagegen niedrig (5–57 % je nach
Temperatur), und die Klärung (Abschnitt 4) übernimmt den Rest.

---

## 3. Farbe aus Menge und Chelatgrad

Zweikomponentenmodell aus freiem Alizarin (h = 70,4°, gemessen an nPHA ohne
TiO₂) und Ti-Chelat (h = 29,8°, gemessen an vollständig geklärtem tPHA).

Optisch wirksame Farbstoffmenge:

$$A(d) = 15{,}62 \cdot \left(1 - e^{-d/32{,}4\,\mu\text{m}}\right)$$

$$a^* = A\left[(1-\theta) + 2{,}504\,\theta\right]$$
$$b^* = A\left[2{,}807(1-\theta) + 1{,}434\,\theta\right]$$

(2,807 = tan 70,4°; 1,434 = 2,504 · tan 29,8°)

$$L^* = 100 \cdot e^{-a^*/88{,}19}$$
$$C^* = \sqrt{a^{*2}+b^{*2}}, \qquad h = \arctan(b^*/a^*)$$

Der Faktor **2,504** ist die relative Farbstärke des Chelats gegenüber
freiem Alizarin — es färbt gut zweieinhalbfach kräftiger. Das erklärt, warum
schon 47–57 % chelatisierter Anteil den Farbeindruck dominieren, obwohl
mehr als die Hälfte der Substanz noch frei vorliegt.

Die Sättigungslänge d0 = 32,4 µm entspricht einer **optischen Sondiertiefe
von ~90–100 µm** (bei 93 µm sind 94 % von A_max erreicht). Unabhängig
bestätigt durch lineare Extrapolation von a\* gegen gemessene Schichtdicke
(r = 0,986): Der Sättigungswert a\* = 30,5 wird danach schon bei ~93 µm
erreicht, obwohl die zugehörige Färbung (10 h/68 °C) tatsächlich ~205 µm
tief reichte. Jenseits von ~100 µm trägt zusätzliche Tiefe optisch praktisch
nichts mehr bei.

---

## 4. Klärung (Nachbehandlung)

### 4.1 Mechanismus: Umwandlung ist nicht Entfernung

Beim Klären laufen zwei Dinge gleichzeitig ab: freies Alizarin wird
chelatisiert (Fortschritt p, wandelt θ weiter Richtung 1) und ein Teil der
optisch wirksamen Menge A geht scheinbar verloren (sichtbar am C\*-Abfall
über das hinaus, was die reine Umwandlung erklärt).

**Der Massenausgleichsversuch zeigt: Dieser scheinbare Verlust ist
überwiegend keine Entfernung, sondern Umverteilung in die Tiefe.** Ein
ungefärbtes Plättchen als Senke neben einem gefärbten im selben Klärbad
(90 °C, dest. Wasser) nahm nur ~1–3 % der im gefärbten Plättchen
enthaltenen Farbstoffmenge auf — bei einem gemessenen A-Verlust am
gefärbten Plättchen von 13–16 %. Der überwiegende Teil des „verlorenen"
Farbstoffs bleibt also im Objekt, nur außerhalb der optisch wirksamen
Randzone.

**Sicherheitsrelevant:** Klären macht den Farbstoff überwiegend unsichtbar,
nicht überwiegend mobil-frei entfernt. Ob der ins Innere verlagerte Anteil
dort gebunden oder weiterhin migrationsfähig ist, ist ungeklärt (siehe
Ausblick, Eisenvitriol-Test am Vollquerschnitt).

### 4.2 Formeln

$$p(T,t) = 1 - \exp\left[-k(T)\cdot t \cdot f\right], \qquad k(T) = 4{,}561\cdot10^{-4}\,\text{s}^{-1}\cdot\exp\left[-\frac{E_{a,\text{Klär}}}{R}\left(\frac{1}{T+273{,}15}-\frac{1}{348{,}15}\right)\right]$$

$$\theta_{\text{nachher}} = \theta + (1-\theta)\cdot p$$

mit **Ea,Klär = 53,7 kJ/mol** — direkt aus zwei Temperaturen bestimmt
(75 °C und 90 °C, beide in destilliertem Wasser gemessen), erkennbar
niedriger als die Diffusions-Ea der Färbung (66,8 kJ/mol). Plausibel: die
Klärung ist teils reaktionslimitiert (Deprotonierung, Protonenabtransport),
nicht rein diffusionslimitiert.

f skaliert die Rate nach Klärmedium (Abschnitt 4.3). Referenzwerte für
destilliertes Wasser (f = 1):

| T | p nach 30 min | p nach 60 min |
|---|---|---|
| 60 °C | 30 % | 51 % |
| 70 °C | 47 % | 71 % |
| 75 °C | 56 % | 81 % |
| 80 °C | 66 % | 88 % |
| 85 °C | 75 % | 94 % |
| **90 °C** | **83 %** | **97 %** |

**Kein Kapazitätsplateau.** Ein früher Fit an drei Zeitpunkten (15/25/40 min
bei 90 °C, dest. Wasser) legte fälschlich eine harte Sättigungsgrenze bei
p ≈ 83 % nahe — Ursache war eine zu hoch angesetzte Ea (zunächst von der
F�rbe-Diffusion übernommen, keine eigene Messung). Ein vierter Punkt bei
100 min widerlegte das eindeutig: p = 95 %, h = 30,6° — nur 0,8° vom
reinen Chelat-Endwert entfernt. TiO₂ ist im relevanten Konzentrationsbereich
also nicht die begrenzende Ressource. **Lehre für künftige Kinetikfits:**
eine übernommene statt selbst gemessene Aktivierungsenergie ist eine
Annahme; ein scheinbares Plateau aus wenigen Punkten auf engem Zeitfenster
ist von einer schlicht zu langsam angesetzten Kinetik kaum zu unterscheiden.

### 4.3 Klärmedien im Vergleich

| Medium | f (rel. Rate) | A-Verlust | Status |
|---|---|---|---|
| **kein Medium** (trocken, nur Restfeuchte im Polymer) | 0,29 | ~5 % | funktioniert, langsam |
| **destilliertes Wasser** | 1,0 (Referenz) | 13–16 % (überwiegend Umverteilung, s. 4.1) | funktioniert, gut charakterisiert |
| **Leitungswasser** | ~1,3–1,4 | 13–16 % (kein Unterschied zu dest.) | funktioniert schneller, nicht reproduzierbar |
| **IPA, kalt (~20 °C)** | ≪ 0,1 | vernachlässigbar | praktisch wirkungslos |
| **IPA, heiß (~75 °C)** | — | — | **ausgeschlossen: erweicht das Material** |
| gepufferte Lösung (Acetat, drei pH-Stufen) | ~1,0 (kein Unterschied zu dest.) | nicht separat gemessen | **getestet, widerlegt** — kein Vorteil gegenüber dest. Wasser |
| Zitronensäure | — | — | spekulativ, könnte Chelat lösen statt bilden |

**Kein Medium (trocken).** Auch ohne äußeres Wasser läuft Klärung ab — die
~1 % Restfeuchte im Polymer reicht für die nötige Deprotonierung, nur
deutlich langsamer (Faktor 0,29 gegenüber destilliertem Wasser; 75 °C/30 min
ergab p = 21 % statt 56 %).

**Destilliertes Wasser** ist das am besten charakterisierte Medium
(Abschnitt 4.2). Frühere Unterscheidung in „feucht" (Tropfen, dünner Film)
und „nass" (volles Bad) erwies sich als unnötig: Beide liefern
ununterscheidbare Ergebnisse in Umwandlung und A-Verlust — konsistent mit
4.1, wonach ohnehin kaum Substanz das Objekt verlässt, sodass die
Lösekapazität des Mediums kaum ins Gewicht fällt. „Dämpfen" (nur
Wasserdampf, kein flüssiges Wasser) dürfte sich chemisch kaum von einer
dünnen Benetzung unterscheiden; praktisch ist ein trockener Dampfkontakt
zudem kaum herstellbar, da ein kaltes Plättchen beim Aufheizen von selbst
einen vergleichbaren Kondensatfilm ansetzt (~26 µm beim Aufheizen auf
90 °C).

**Leitungswasser** klärt bei gleicher Temperatur und Zeit deutlich schneller
als destilliertes Wasser (90 °C/25 min: p = 89,5 % gegenüber modelliert
77,1 % für destilliert, gleicher Ausgangsbatch), bei **statistisch
identischem A-Verlust** (15,4 % vs. 15,7 %). Als Rezeptzutat ungeeignet —
Härtegrad und Ca-Belagsbildung schwanken mit dem Wohnort des Anwenders und
sind nicht reproduzierbar vorhersagbar (frühere Versuche zeigten teils
abwischbare violette Beläge, in anderen Läufen keine; vermutlich temperatur-
und zeitabhängig).

Die naheliegende Erklärung — Bicarbonat/Carbonat puffert das bei der
Chelatisierung freiwerdende Proton ab — ist **durch einen direkten Test
widerlegt** (siehe „Gepufferte Lösungen" unten). Was den Effekt tatsächlich
verursacht, ist damit wieder offen; **Calcium selbst** (nicht als Puffer,
sondern z. B. als eigenständiges Ca-Alizarin-Chelat oder als Katalysator der
Ti-Chelatisierung) ist der derzeit naheliegendste Kandidat. Ein Hinweis
darauf: stark geklärte Plättchen wirken zunehmend pinkstichig statt
rot-orange, was auf eine dritte Farbspezies neben freiem Alizarin und
Ti-Chelat hindeuten könnte. Ungeklärt, ob diese dritte Spezies TiO₂ benötigt
(ternärer Ti–Ca–Alizarin-Komplex) oder auch ohne TiO₂ entsteht — ein
Parallelversuch an nPHA (kein TiO₂, damit isoliert testbar) läuft.

**IPA, kalt.** Bei Raumtemperatur (~18–25 °C) praktisch wirkungslos: über
32 min kumulativ kein messbarer Effekt, auch nach ~10 h nur geringe
Veränderung, teils mit Anzeichen physikalischer Materialschädigung
(erhöhte NIR-Streuung bei nPHA, vermutlich Mikrorisse durch Quellung) ohne
nennenswerten Klärnutzen. Quantitativ erklärbar: D bei 20 °C liegt rund
Faktor 20 unter D bei 90 °C, sodass 10 h bei Raumtemperatur nur der
Wirkung von rund 2 h bei 90 °C entsprechen — und selbst das unterschätzt
die Diskrepanz, weil die Chelatisierungs-Ea nochmal niedriger ist als die
Diffusions-Ea.

**IPA, heiß.** Bei ~75 °C erweichte das behandelte Plättchen sichtbar
(Quellung/Spannungsrissbildung, IPA-Siedepunkt 82 °C). **Als Klärmedium
ausgeschlossen**, unabhängig von der Kinetik.

**Gepufferte Lösungen — Pufferhypothese getestet und weitgehend widerlegt.**
Drei Acetatpuffer (pH 4,2 / 5,0 / 5,8, Konzentration jeweils auf gleiche
Pufferkapazität wie der pH-5-Ansatz gebracht: 0,137 / 0,100 / 0,303 mol/L),
90 °C, 25 min, identischer Ausgangsbatch wie der Leitungswasser-Vergleich:

| Medium | p |
|---|---|
| destilliertes Wasser | 76,9 % |
| Puffer pH 4,2 | 75,9 % |
| Puffer pH 5,0 | 78,3 % |
| Puffer pH 5,8 | 78,5 % |
| **Leitungswasser** | **89,5 %** |

Alle drei gepufferten Ansätze liegen auf dem Niveau von reinem destilliertem
Wasser, unabhängig von pH und Kapazität — und deutlich unter Leitungswasser.
Weder der pH-Wert noch die Pufferkapazität von Acetat erklären die
Beschleunigung durch Leitungswasser. **Acetatpuffer bringt gegenüber
destilliertem Wasser keinen messbaren Vorteil** und ist als Rezeptzutat
damit ohne Nutzen — es verkompliziert das Rezept, ohne einen Effekt zu
liefern. Für die tatsächliche Ursache siehe die Ca-Diskussion oben.

**Zitronensäure** (Ausblick, spekulativ). Als starker Ti-Komplexbildner
könnte sie das Ti-Alizarin-Chelat kompetitiv aufbrechen statt Klärung zu
beschleunigen — also eher ein Werkzeug zur gezielten Entfärbung/Farbton-
Korrektur als ein Klärmedium. Ungetestet.

---

## 5. Validierung

| Versuch | L\* mod | L\* ist | a\* mod | a\* ist | b\* mod | b\* ist | h mod | h ist |
|---|---|---|---|---|---|---|---|---|
| 60 °C/30 min | 88,8 | 89,3 | 10,46 | 10,11 | 28,53 | 25,98 | 69,9° | 68,7° |
| 70 °C/30 min | 83,6 | 84,3 | 15,83 | 16,27 | 30,86 | 32,47 | 62,8° | 63,4° |
| 75 °C/30 min | 80,9 | 83,7 | 18,72 | 19,09 | 31,32 | 32,30 | 59,1° | 59,4° |
| 80 °C/30 min | 78,2 | 83,1 | 21,64 | 20,42 | 31,29 | 29,49 | 55,3° | 55,3° |
| 85 °C/30 min (×2) | 75,7 | 75,0 / 77,0 | 24,54 | 26,61 / 25,65 | 30,79 | 33,07 / 30,18 | 51,4° | 51,2° / 49,6° |
| 68 °C/10 h (Sättigung) | 69,1 | 61,9 | 32,62 | 30,50 | 28,23 | 28,32 | 40,9° | 42,9° |
| 75 °C/30 min Klärung, dest., ×3 | 74,5–83,5 | 76,0–87,1 | 15,9–25,9 | 15,1–26,9 | 17,4–21,0 | 17,1–21,9 | 39–48° | 38–49° |
| 75 °C/30 min Klärung, trocken | 74,1 | 72,6 | 26,42 | 27,67 | 28,07 | 29,39 | 46,7° | 46,7° |
| **90 °C/30 min (bestätigte Extrapolation)** | 73,3 | 76,5 | 27,36 | **28,73** | 29,88 | **29,90** | 47,5° | **46,1°** |

**RMS über alle Kalibrier- und Validierungspunkte: h ≈ 1,0°, a\* ≈ 1,4,
b\* ≈ 1,5, L\* ≈ 3,1.** Der Hue ist die belastbarste Größe. L\* ist am
schwächsten — größter Ausreißer ist die Sättigungsfärbung (10 h), die
außerhalb des Kalibrierbereichs liegt und zudem oberhalb der optischen
Sondiertiefe (Abschnitt 3) gefärbt wurde.

Die 90-°C-Zeile ist die schärfste Prüfung: eine vor der Messung fixierte
Vorhersage außerhalb des ursprünglichen Kalibrierbereichs (60–85 °C), die
mit einer unabhängigen Wiederholung bestätigt wurde. Ein erster Lauf bei
90 °C war durch kaltes Aufheizen und Luftblasen verfälscht (effektiv nur
~85 °C erreicht, ~17 % der Fläche maskiert) — beide Ursachen ließen sich
rechnerisch trennen (Temperaturfehler am Hue, Maskierung an der Amplitude)
und methodisch beheben (Glas mit Inhalt vollständig vorheizen, dann erst
Plättchen einhängen).

---

## 6. Vorhersagen

| Prozess | d | L\* | a\* | b\* | C\* | h |
|---|---|---|---|---|---|---|
| 90 °C/30 min, ohne Klärung | 93 µm | 73,3 | 27,36 | 29,88 | 40,51 | 47,5° |
| 90 °C/30 min + Klärung 90 °C/30 min, dest. | 93 µm | 73,7 | 26,92 | 17,27 | 31,98 | **32,7°** |
| 85 °C/30 min + Klärung 85 °C/60 min, dest. | 80 µm | 74,7 | 25,69 | 15,49 | 30,00 | 31,1° |
| 85 °C/40 min + Klärung 90 °C/30 min, dest. | 92 µm | 73,8 | 26,82 | 17,29 | 31,91 | 32,8° |

Alle drei Klärvarianten landen nahe beieinander bei h ≈ 31–33°, deutlich
näher am Chelat-Endwert (29,8°) als am ungeklärten Zustand. Für **nahezu
vollständige** Umwandlung (h < 31°) sind nach heutigem Stand eher 60–100 min
nötig (bestätigt: 100 min bei 90 °C erreichten h = 30,6°). Eine halbe bis
eine Stunde Klärung bei 85–90 °C deckt aber bereits den Großteil der
möglichen Verschiebung ab.

---

## 7. Alizarinmenge und Farbstoffbedarf

### Sättigungsbeladung

Rückgerechnet aus der Sättigungsfärbung (68 °C/10 h): ein Plättchen
(0,616 cm³) nahm rund 5 mg Alizarin auf.

$$c_s \approx 8\,\text{mg/cm}^3 \;\hat{=}\; 0{,}7\ \text{Gew.-\%}$$

Größenordnungsabschätzung, nicht gravimetrisch gemessen (Faktor 1,5 nach
oben oder unten wäre nicht überraschend).

### Bedarf je Flächeneinheit

Das Konzentrationsprofil folgt einer erfc-Front; das Flächenintegral
darunter beträgt nur 1,128/2,32 = 0,486 des Rechtecks aus
Randkonzentration mal Eindringtiefe:

$$m_A(T,t) = 0{,}486 \cdot c_s \cdot d(T,t) = 3{,}94\cdot10^{-4}\ \frac{\text{mg}}{\text{cm}^2\cdot\mu\text{m}} \cdot d(T,t)$$

| T | 10 min | 20 min | 30 min | 60 min |
|---|---|---|---|---|
| 60 °C | 0,0078 | 0,0111 | 0,0136 | 0,0192 |
| 75 °C | 0,0132 | 0,0186 | 0,0228 | 0,0323 |
| 85 °C | 0,0182 | 0,0257 | 0,0315 | 0,0446 |
| **90 °C** | 0,0212 | 0,0300 | **0,0368** | 0,0520 |

(mg Alizarin je cm² Objektoberfläche)

### Praxisformel für den Wurzelbedarf

Bei 2 % Anthrachinongehalt der Wurzel und 50 % Ausnutzung, für 90 °C/30 min:

$$m_{\text{Wurzel}}[\text{g}] \approx 4{,}0\cdot10^{-5}\cdot d[\mu\text{m}]\cdot A[\text{cm}^2] \;+\; 0{,}006\cdot V[\text{ml}]$$

Merkregel: **1 g Wurzel je 100 ml Flotte, plus 0,4 g je 100 cm² Oberfläche**
(bei ~93 µm Färbetiefe; proportional weniger bei dünnerer Färbung).

| Fall | Objekt | Flotte | Flottenanteil |
|---|---|---|---|
| Plättchen im Glas (13 cm², 200 ml) | 0,05 g | 1,20 g | **96 %** |
| kleiner Druck, enges Gefäß (50 cm², 150 ml) | 0,18 g | 0,90 g | 83 % |
| mittleres Objekt (200 cm², 500 ml) | 0,74 g | 3,00 g | 80 % |
| großes Objekt (800 cm², 1500 ml) | 2,94 g | 9,00 g | 75 % |

**Der Flottenterm dominiert den Verbrauch vollständig** — ein Fehler von
Faktor 2 in der Oberfläche ändert den Gesamtbedarf um unter 10 %.
Konsequenz: Flottenvolumen minimieren (Füllkörper, enges Gefäß) oder den
Sud mehrfach verwenden.

### Oberfläche abschätzen

Flotte direkt messen (Objekt ins Gefäß, mit Wasser bedecken, abgießen,
wiegen) statt zu rechnen. Für die Oberfläche genügt aus dem Slicer-Volumen:

$$A \approx k \cdot V^{2/3}, \qquad k = 6\text{–}7 \text{ (kompakt)},\ 8\text{–}12 \text{ (typisch)},\ 12\text{–}20 \text{ (flach/verzweigt)}$$

**Layer Lines:** Die Diffusion glättet laterale Strukturen; eine periodische
Störung der Wellenlänge λ klingt mit exp[−(2π√(Dt)/λ)²] ab. Bis 0,2 mm
Schichthöhe ist die Front bei typischen Prozesszeiten praktisch eben (unter
90 °C/30 min bleiben 0,2 % bis 21 % Restwelligkeit je nach Schichthöhe) —
es zählt die projizierte Fläche ohne Zuschlag. Ab 0,3 mm folgt die Farbfront
den Rillen; dann Zuschlag von 30–50 % und ungleichmäßigere Färbung.

### Vorbehalte

- c_s ist geschätzt, nicht gemessen.
- Der Anthrachinongehalt der Wurzel (hier 2 %) und die Ausnutzung (hier
  50 %) schwanken zwischen Chargen erheblich.
- A ist die **benetzte** Oberfläche. Bei nicht wasserdicht gedruckten
  Objekten kommt die Infill-Oberfläche hinzu — potenziell das Fünf- bis
  Zehnfache der Außenhülle.

---

## 8. Offene Punkte

1. **Zeitabhängigkeit von θ beim Färben** stützt sich auf einen Datenpunkt
   (10 h/68 °C). Eine echte Zeitreihe bei konstanter Temperatur steht aus.
2. **In der Temperaturreihe sind T und d korreliert** (alle 30 min); die
   Trennung beider Einflüsse hängt an einem einzigen abweichenden Punkt.
3. **Keine pH-Abhängigkeit beim Färben modelliert.** Abschnitt 2 gilt nur
   für pH 5. Ob und wie stark höherer Färbe-pH die Chelatisierung während
   des Färbens erhöht (auf Kosten der Aufnahmemenge), ist offen — geplanter
   Versuch mit Acetat/Essigsäure-Pufferreihe.
4. **Ob der beim Klären ins Volumen verlagerte Farbstoff (Abschnitt 4.1)
   dort gebunden oder mobil bleibt, ist ungeklärt** — sicherheitsrelevant,
   zu prüfen z. B. über einen Farbreaktionstest (Eisen(II)) am
   Vollquerschnitt eines geklärten Plättchens.
5. **Der Substanzverlust beim Klären** ist nur bei 75 °C kalibriert und
   dürfte von der Schichtdicke abhängen (dünne Schichten verlieren relativ
   mehr) — mit den vorliegenden Daten nicht von der Regime-Abhängigkeit
   trennbar.
6. **Die Ursache der Leitungswasser-Beschleunigung ist ungeklärt.** Die
   Pufferhypothese ist getestet und widerlegt (siehe 4.3). Calcium ist der
   naheliegendste verbliebene Kandidat — offen ist, ob es als eigenständiges
   Ca-Alizarin-Chelat, als ternärer Ti–Ca–Alizarin-Komplex (nur mit TiO₂
   möglich) oder als reiner Katalysator ohne Einbau ins Endprodukt wirkt.
   Für das Rezept praktisch nachrangig — destilliertes Wasser klärt
   zuverlässig, nur langsamer (siehe 4.2) — aber mechanistisch offen.
7. **Gültigkeitsbereich:** Färbung 60–90 °C (bis 90 °C durch Wiederholung
   abgesichert), Klärung 75–90 °C (zwei Temperaturen direkt gestützt,
   60–70 °C und 80 °C Interpolation). Für dünn gefärbte Proben (< 90 µm)
   ist das Farbmodell nicht separat geprüft.
8. **Oberhalb ~100 µm Schichtdicke verliert das Modell an Aussagekraft für
   die Farbe** (optische Sondiertiefe erreicht) — die Schichtdickenformel
   gilt weiter, a\*/b\*/L\* reagieren aber kaum noch auf zusätzliche Tiefe.
