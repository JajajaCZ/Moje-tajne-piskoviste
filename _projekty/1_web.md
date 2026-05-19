---
layout: post
title: "Webové stránky"
date: 2026-05-19
---
## Poslední změny

1. Odstranění chyb a čistka
Vyřešení složky Archív: Zjistili jsme, že Jekyll padal kvůli chybějící složce/diakritice, a ujasnili si, jak soubory archivovat nebo ignorovat v konfiguraci.

Kompletní likvidace původní patičky: Trápili jsme se s defaultní patičkou tématu Minima (která tam tvrdohlavě cpala ikonu GitHubu a nadpisy). Vyřešili jsme to tím, že jsme vytvořili vlastní čistý soubor _includes/footer.html, který tu starou patičku stoprocentně přemazal.

2. Vlastní design a Dark Mode
Černo-bílý styl: Nastavili jsme hluboké tmavé pozadí pomocí tvé barvy #0A0A0A v souboru assets/main.scss. K tomu jsme přebarvili texty na příjemnou šedou a nadpisy na čistě bílou, aby netahaly oči.

Bílá dělicí čára: Upravili jsme styl hlavičky, aby pod menu svítila ostrá bílá linka oddělující menu od obsahu.

3. Nové logo (Panda červená)
Nasazení loga: Nahradili jsme textový název webu parádním kulatým steampunkovým logem s pandou červenou.

Struktura složek: Obrázek jsme čistě uklidili do nově vytvořené složky img/panda.png.

Vychytaný Hover efekt: Do CSS jsme přidali kód, díky kterému panda při najetí myší plynule o 5 % povyskočí a o 20 % se rozjasní.

4. Inteligentní menu a struktura webu
Automatické meníčko: Upravili jsme šablonu _includes/header.html tak, aby se odkazy perfektně výškově vycentrovaly na střed k novému logu. Zároveň menu zase funguje automaticky – samo přidá každou novou podstránku vytvořenou v kořenu webu a umí je řadit podle parametru order.

Rozdělení na Články a Projekty: Navrhli jsme pokročilé řešení pro _config.yml, kde rušíme staré _posts a budujeme dvě samostatné složky: _clanky a _projekty. Tím zajistíme, že se ti věci nebudou míchat, ale hlavní stránka (index.md) si dokáže plynule cucat data z obou složek naráz, sloučit je a seřadit podle data s ikonkami (🛠️ / 📝).

Zjednodušení datování: Aktivovali jsme v konfiguraci funkci, díky které nemusíš psát dlouhé datum do názvu souboru (Jekyll si ho vytáhne přímo z hlavičky uvnitř článku).

Co máme v plánu dál?
Naposledy jsme připravili krátký text o pandě červené.