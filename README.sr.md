<a href="https://autoset.rs/"><img src="media/cover.jpg" alt="AutoSet Niš, naslovna strana na laptopu i telefonu" width="100%"></a>

# AutoSet Niš

Sajt auto-staklarske radnje u Nišu sa stranom za svaku uslugu i privatnim panelom za lager od preko 700 stavki, uvezenih iz knjigovodstva.

**[autoset.rs](https://autoset.rs/)** · [Studija slučaja](https://svilenkovic.rs/radovi/autoset-nis) · [English](README.md)

> [!NOTE]
> Klijentski projekat. Izvorni kod pripada klijentu i čuva se u privatnom repozitorijumu. Ova stranica opisuje šta sam uradio i kako.

<table>
  <tr><td><b>Klijent</b></td><td>AutoSet</td></tr>
  <tr><td><b>Delatnost</b></td><td>Auto stakla: prodaja, ugradnja, zamena i reparacija</td></tr>
  <tr><td><b>Lokacija</b></td><td>Niš</td></tr>
  <tr><td><b>Vrsta</b></td><td>Sajt sa više strana i panelom za lager</td></tr>
  <tr><td><b>Moj deo posla</b></td><td>Dizajn, izrada, SEO, hosting i održavanje</td></tr>
  <tr><td><b>Tehnologije</b></td><td>HTML, PHP 8.3, nginx, PHPMailer, MariaDB (panel)</td></tr>
</table>

## O projektu

AutoSet od 2005. prodaje i ugrađuje auto stakla u Nišu, od vetrobrana i bočnih stakala do stakala za kombije, kamione i autobuse. U staklarsku radnju niko ne ide po planu: kamen udari u vetrobran, vozač ukuca uslugu i grad i zove prvi sajt koji se učita. Zato svaka glavna usluga ima svoju stranu za takvu pretragu, a broj telefona se zove jednim dodirom.

Veći posao je stigao kasnije: privatni panel za pult, sa lagerom od preko 700 stavki i kalendarom zakazivanja. Knjigovodstveni program nema dokumentovan API, samo izvoz u tabelu. Panel zato uvozi XLSX u tri koraka (otpremanje, mapiranje kolona sa automatskim prepoznavanjem i pregled novih i izmenjenih redova) i pre svakog upisa pravi kopiju celog lagera. Najviše muke bilo je sa podacima: ista šifra postoji pod dva proizvođača, pa se redovi spajaju po šifri zajedno sa proizvođačem, a 94 reda su imala šifru bez naziva.

## Šta sam uradio

- Strana za svaku glavnu uslugu, pisana za pretragu tipa zamena vetrobrana Niš, sa svojim postupkom i čestim pitanjima
- Adrese bez nastavka preko try_files, pa strana može da pređe iz HTML-a u PHP, a da joj adresa ostane ista
- XLSX se proverava pre čitanja, po prijavljenoj veličini i odnosu sažimanja, pošto se fajl od 1,84 MB u memoriji raspakovao na 529 MB
- Popravka prozora za izmenu koji je zaokružene cene čitao nazad iz tabele i upisivao ih, pa su decimale tiho nestajale
- Testiranje pravim klikom miša, koje je našlo dugme Dalje 189 px ispod ivice ekrana na laptopu od 1366 px i lebdeću oznaku koja je gutala klikove
- Testovi koje panel nosi sa sobom: 129 provera nad podacima i 43 preko mreže, uključujući namerno napravljenu zip bombu

## Merenja

| | Performanse | Pristupačnost | Dobre prakse | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Telefon | 100 | 100 | 100 | 100 |
| Desktop | 100 | 100 | 100 | 100 |

PageSpeed Insights, laboratorijsko merenje živog sajta, septembar 2026. Sigurnosna zaglavlja: 6 od 6. HTML validator: bez grešaka. axe provera pristupačnosti: bez prekršaja. Strukturisani podaci: `AutoPartsStore`, `AutoRepair`.

## Snimci ekrana

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="AutoSet Niš, naslovna strana na ekranu širine 1440 px"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="AutoSet Niš, naslovna strana na telefonu"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="Sekcija &quot;Zašto AutoSet&quot;: šest kartica sa uslovima koje firma navodi">
<sub>Sekcija "Zašto AutoSet": šest kartica sa uslovima koje firma navodi</sub>

<img src="media/inner-2.webp" alt="Preporuke, pa kontakt blok sa adresom sedišta i formom">
<sub>Preporuke, pa kontakt blok sa adresom sedišta i formom</sub>

---

<sub>Izrada: [D. Svilenković](https://svilenkovic.rs).</sub>
