# 📽️ Teleprompter

Jednoduchý teleprompter, ktorý beží priamo v prehliadači – bez inštalácie, funguje na počítači aj mobile. Umožňuje čítať text na obrazovke počas nahrávania videa cez prednú alebo zadnú kameru.

## Funkcie

- **Vlastný text** – vlož alebo napíš text, ktorý sa má posúvať
- **Nastaviteľná rýchlosť posúvania a veľkosť písma**
- **Zrkadlový režim** – pre použitie so sklom teleprompteru
- **Čiara na čítanie** – vodiaca čiara uprostred obrazovky
- **Kamera na pozadí** – prepínanie medzi prednou a zadnou kamerou
- **Nahrávanie videa** – s možnosťou pozastaviť, pokračovať, zrušiť alebo uložiť nahrávku (video sa stiahne priamo do zariadenia ako `.webm`/`.mp4`)
- Funguje na mobile aj desktope, prispôsobené dotykovému ovládaniu

## Použitie

1. Otvor `index.html` v prehliadači (alebo použi live odkaz cez GitHub Pages).
2. Vlož text, nastav rýchlosť, veľkosť písma a prípadne zapni zrkadlový režim.
3. Klikni na **Spustiť**.
4. Prehliadač si vyžiada povolenie na kameru a mikrofón – potvrď ho.
5. Ovládanie počas čítania:
   - **Medzerník** – štart/pauza posúvania textu
   - **Šípky ▲ ▼** – rýchlejšie/pomalšie
   - **🔄 Kamera** – prepnutie predná/zadná
   - **⏺ Nahrávať** – spustenie nahrávania (⏸ pozastaví, ▶ pokračuje)
   - **🗑 Zrušiť** – zahodí rozohratú nahrávku
   - **💾 Uložiť** – ukončí nahrávanie a stiahne súbor
   - **Esc** – návrat na úvodnú obrazovku

## Spustenie cez GitHub Pages

Kamera a mikrofón fungujú v prehliadačoch len cez HTTPS (alebo localhost). GitHub Pages toto spĺňa automaticky, takže po nasadení appka funguje bez ďalšieho nastavovania – vrátane mobilných zariadení.

1. V nastaveniach repozitára choď do **Settings → Pages**.
2. Pri **Source** vyber vetvu `main` a priečinok `/(root)`.
3. Ulož – appka bude dostupná na `https://tvoje-meno.github.io/nazov-repozitara/`.

## Kompatibilita

- Odporúčané prehliadače: Chrome, Edge, Firefox (Android aj desktop)
- Safari na iOS podporuje nahrávanie videa od verzie iOS 14.3+; formát výstupu sa môže líšiť (`.mp4` namiesto `.webm`)
- Bez pripojenej kamery appka funguje aj naďalej ako klasický teleprompter (bez nahrávania)

## Technológie

Čistý HTML, CSS a JavaScript – žiadne závislosti, žiadny build proces. Používa štandardné webové API: `getUserMedia` (kamera/mikrofón) a `MediaRecorder` (nahrávanie).
