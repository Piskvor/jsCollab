# testovací repozitář na hraní s Javascriptem

Chyby skriptu v aktuálním souboru: 
- Firefoxí [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console/Opening_the_Web_Console) - vypisuje chyby skriptu (`Ctrl+Shift+K`)
- Chromácká [DevTools Console](https://developers.google.com/web/tools/chrome-devtools/console/) dělá totéž, ale v Chromu (`Ctrl+Shift+J`)
- IE není browser, to je monstrum s chapadly, ale prý to má někde v Developer Tools (`F12`)  

Příklad:

`unreachable code after return statement sermirsky-metronom.html:13:16`

První kousek je typ chyby, druhý je název souboru (`sermirsky-metronom.html`), třetí je řádka a sloupec (`13:16`).
Kouknu a vidím:

    12            nahodne = noveNahodne;
    13        return nahodne;
    14        if (nahodne == "1") {
    15            alert("Prima!");
    16        }

Mám tam return na řádce 13 - za ním by se ještě něco mělo dít, ale nebude, protože tím returnem vyskočím z funkce ven.
