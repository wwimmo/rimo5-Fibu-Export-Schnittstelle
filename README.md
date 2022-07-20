# rimo5-Fibu-Export-Schnittstelle

<!--ts-->
Table of contents
   * [Eingabemaske für den Fibuexport (Bewegungsdaten)](#Eingabemaske-für-den-Fibuexport-Bewegungsdaten)
   * [Felddefinition](#Felddefinition)
   * [Musterdatei](#Musterdatei)
   * [Export](#Export)

# Eingabemaske für den Fibuexport (Bewegungsdaten)
Die Schnittstelle MIS-Export exportiert Daten aus Tabellen oder Views, aus Rimo in CSV-Files ins lokale Dateisystem.
![DataRelationship](/_grafiken/Funktionsaufruf.png)

Wir wählen Verwaltung, Fibu, Fibujahr und Bis Buchdat. gemäss unseren Wünschen bzw. Vorgaben.

Gegenkonto: Hier wird das Gegenkonto der Buchungen in der Finanzbuchhaltung eingegeben.

Exp. Eröffnungsbuchungen: Wenn die Eröffnungsbuchungen aus Rimo R4 ebenfalls exportiert werden sollen, setzen wir hier das Flag.

Pfad: Hier wählen wir über den Drei-Punkte-Button den Pfad aus, unter dem Rimo R4 die Export-Datei abspeichern soll. Dateiname und Endung werden von Rimo R4 automatisch vergeben und sollten nicht geändert werden.

Modus: Hier wählen wir die Art und Weise, wie Rimo R4 die Buchungssätze exportiert. Bei „Kumuliert pro Monat“ werden die Buchungen in der Finanzbuchhaltung jeweils zum Monatsletzten verbucht.

Mit der Bestätigung durch „OK“ erscheint ein Journal, das wir ausdrucken können. Damit ist der Export Rimo-seitig abgeschlossen; das File kann von seinem Speicherort abgeholt werden und gemäss Anleitung in die Finanzbuchhaltung eingelesen werden

# Felddefinition
| Pos | Typ | Grösse | Bezeichnung | Bemerkung | Zwingend | Mustereintrag |
|---: |:---:| ------:| :---------- | :-------- | -------: | :------------ |
| 1 | N | 8 | Zähler | Fortlaufende Nummer | Ja | 1 |
| 2 | A | 1 | Version | Immer ‚I’  | Ja | I |
| 3 | D | 10 | Datum | Buchungsdatum: TT/MM/JJJJ | Ja | 01.01.2003 |
| 4 | N | 11 | Konto/Kart | Konto oder Kostenart (max. 11 Stellen) | Ja | 1100 |
| 5 | N | 11 | Gkto/Gkart | Gegenkonto oder Gegenkostenart | Ja | 3000 |
| 6 | A | 30 | Buchungstext1 | Buchungstext 1. Textzeile (in Hochkommassetzen) | Nein | “ Buchtext 1“ |
| 7 | N | 12.2 | Betrag | Buchungsbetrag | Ja | 10000 |
| 8 | A | 30 | Buchungstext2 | Buchungstext 2. Textzeile (in Hochkommas setzen) | Nein | “ Buchtext 2“ |
| 9 | A | 1 | Soll/Haben | Soll/Haben-CodeMuss ‚S’ oder ‚H’ enthalten | Ja | S |
| 10 | N | 11 | Kostenstelle | Exportkostenstelle, wenn bei Position 4 eine Kostenart mitgegeben wird | Ja* |   |
| 11 |  |  |  |  |  | Leer |
| 12 | (N) | 6 | Belegnummer | Belegnummer (alphanumerisch) | Nein | “111111“ |
| 13 |  |  |  |  |  | Leer |
| 14 |  |  |  |  |  | Leer |
| 15 |  |  |  |  |  | Leer |
| 16 |  |  |  |  |  | Leer |
| 17 |  |  |  |  |  | Leer |
| 18 |  |  |  |  |  | Leer |
| 19 |  |  |  |  |  | Leer |
| 20 | D | 10 | Valutadatum | Buchungsdatum: TT/MM/JJJJ | Nein | 11.02.2002 |
| 21 |  |  |  |  |  | Leer |
| 22 |  |  |  |  |  | Leer |
| 23 |  |  |  |  |  | Leer |
| 24 | A | 3 | ISO-Code Konto | 3 stelliger ISO-Code für Kontowährung. Immer CHF | Ja | CHF |
| 25 | A | 3 | ISO-Code GKonto | 3 stelliger ISO-Code für Kontowährung. Immer CHF | Ja | CHF |
| 26 |  |  |  |  |  | Leer |
| 27 |  |  |  |  |  | Leer |
| 28 |  |  |  |  |  | Leer |
| 29 |  |  |  |  |  | Leer |
| 30 |  |  |  |  |  | Leer |
| 31 |  |  |  |  |  | Leer |
| 32 |  |  |  |  |  | Leer |
| 33 |  |  |  |  |  | Leer |
| 34 |  |  |  |  |  | Leer |
| 35 | A | 1 | Codefeld | Alphanumerisches Feld 1 Stelle R für Rimo | Nein | R  |
| 36 | A | 3 | MWSTCODE | Code gemäss MWST-Tabelle des Mandanten | Nein | 311 |
| 37 | N | 3.2 | MWSTSATZ | MWST Satz | Nein | 7.6 |
| 38 |  |  |  |  |  | Leer |
| 39 |  |  |  |  |  | Leer |
| 40 |  |  |  |  |  | Leer |
| 41 | N | 3.2 | MWSTKOEFF | MWST-Anteilvorsteuer | Nein | 100 |
| 42 |  |  |  |  |  | Leer |
| 43 |  |  |  |  |  | Leer |
| 44 |  |  |  |  |  | Leer |
| 45 |  |  |  |  |  | Leer |
| 46 |  |  |  |  |  | Leer |
| 47 |  |  |  |  |  | Leer |
| 48 |  |  |  |  |  | Leer |
| 49 |  |  |  |  |  | Leer |
| 50 |  |  |  |  |  | Leer |
| 51 |  |  |  |  |  | Leer |
| 52 |  |  |  |  |  | Leer |
| 53 |  |  |  |  |  | Leer |
| 54 |  |  |  |  |  | Leer |
| 55 |  |  |  |  |  | Leer |
| 56 |  |  |  |  |  | Leer |
| 57 |  |  |  |  |  | Leer |
| 58 |  |  |  |  |  | Leer |
| 59 |  |  |  |  |  | Leer |
| 60 |  |  |  |  |  | Leer |
| 61 |  |  |  |  |  | Leer |
| 62 |  |  |  |  |  | Leer |
| 63 | A | 1 | Konstante | ‚E’ | Ja | E |

# Musterdatei
Eine Beispieldatei findet man hier: [Fibuexp_Muster.txt](Fibuexp_Muster.txt)

# Export
Exportiert werden die Daten nun in der Schnittstelle Fibu, per: KUNDENADMINISTRATION / EXPORT/IMPORT / FIBU-EXPORT

Hier müssen nun die entsprechenden Finanzbuchhaltungen selektiert werden. Pro Fibu, sprich pro Geschäftsbereich muss ein separater Export erfolgen. Dabei muss unter Mandanten für jede Fibu der entsprechende Geschäftsbereich angewählt werden. Achtung: Rimo prüft hier nichts – als Kunde muss man beim Export also darauf achten, dass man für die jeweilige Fibu den korrekten Mandanten anwählt.

Die Information welches Gegenkonto zu verwenden ist, muss der Kunde liefern. Bei Abacus ist dies in der Regel Konto «9999».

Zum Schluss den gewünschten _Pfad_ angeben und Rimo exportiert die Daten. Achtung: Der Dateiname kann nicht beeinflusst werden. Das heisst Rimo exportiert die Datei immer mit demselben Namen. Deshalb die Datei nach Export zuerst umbenennen bzw. wegkopieren, da sie ansonsten überschrieben wird.

Ein Export kann unter _Fibu-Export wiederholen_ nochmals ausgeführt werden.
Rimo schreibt auf jede Buchung ein Export-Datum, damit diese nicht doppelt exportiert werden.
