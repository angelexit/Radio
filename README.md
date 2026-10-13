# iRMP — Internet Radio Metadata Player

- [Xiaomi Android 10 1.0.6](https://github.com/angelexit/Radio/releases/tag/v1.0.6-xiaomi)

- [Moderní Android 1.0.14](https://github.com/angelexit/Radio/releases/tag/v1.0.14)
- [Legacy Android 4.1–4.4 1.0.16](https://github.com/angelexit/Radio/releases/tag/v1.0.16-legacy)

APK správné edice instalujte přes dosavadní verzi bez odinstalace. Moderní a Legacy jsou odlišné aplikace.

## Aktualizace

Nové verze se kontrolují při otevření aplikace, nejvýš jednou denně. Ruční kontrola je v O aplikaci; v Legacy tlačítkem Aktualizace. První přechod na výše uvedené verze je nutné udělat ručně — starší verze kontrolu ještě nemají.

Legacy na Androidu 4.1–4.4 stahuje aktualizaci přímo na autorádiu přes ověřené HTTPS a kontroluje soubor a podpis. Android vyžaduje potvrzení instalace a povolení neznámých zdrojů. Přenos přes Windows a jeho Odblokovat není pro tento postup potřeba.

Podklady pro vydávání: [updates/README.md](updates/README.md). Metadata nové verze zveřejněte až po nahrání její APK do Releases.

## Katalog rádií

Sdílená složka se jmenuje **radio-catalog**. Výběr je podle země nebo jazyka, stanice se přidávají do stávajícího seznamu bez změny přehrávání. [Formát katalogu](radio-catalog/README.md).

Sestavení a podpisy ověřeny. Nový postup aktualizace Legacy zatím nebyl vyzkoušen na fyzickém autorádiu.

Xiaomi a Modern sdílejí Android identitu a podpis, instalují se jako alternativní edice téže aplikace. Jejich kontroly aktualizací čtou samostatná metadata; Xiaomi nepřebírá Modern aktualizace. První přechod Xiaomi 1.0.5 → 1.0.6 vyžaduje ruční instalaci.

Záložní streamy podporují Modern 1.0.13+, Xiaomi 1.0.6+ a Legacy 1.0.16+. V Upravit rádio/stanici vložte další HTTPS adresy stejné stanice, jednu na řádek. Po vyčerpání všech adres se přehrávání zastaví s chybou.
