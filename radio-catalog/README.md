# iRMP radio-catalog

Složku radio-catalog nahrajte do kořene repozitáře angelexit/Radio, větev main. Aplikace načítá catalog.json. Název složky: radio-catalog.

Formát: schemaVersion: 1 a pole radios. Každé rádio má name, stream_url (HTTPS), country (název země), languages (pole názvů jazyků). Volitelné: id, logo_url, bitrate, format, genre, description. Jedno rádio může mít více jazyků.

Výchozí katalog obsahuje osm českých stanic ze stávající aplikace. Přidávejte další stanice do radios; nabídky zemí a jazyků se vytvářejí automaticky. Nedostupný GitHub nevymaže uložený katalog. Přidání do aplikace zachová původní seznam, přehrávanou stanici i oblíbené. Duplicitní streamy se přeskočí.

Moderní iRMP 1.0.12 zobrazuje známé země a jazyky podle jazyka rozhraní (cs, de, en). Přijímá názvy i běžné kódy; například Německo / DE a Němčina / de se v němčině zobrazí jako Deutschland a Deutsch. Uložený katalog se při přepnutí jazyka nemění. Další jazyky rozhraní lze později doplnit.

## Záložní streamy (Modern od 1.0.13)

`stream_url` zůstává hlavní adresa. Volitelné `backup_streams` je pole dalších HTTPS adres stejné stanice. Starší seznamy s jedinou adresou jsou kompatibilní. Legacy a Xiaomi zatím automatické přepínání nepodporují.

```json
{
  "id": "example",
  "name": "Ukázková stanice",
  "stream_url": "https://primary.example/radio.mp3",
  "backup_streams": ["https://backup.example/radio.mp3"]
}
```

Adresy v příkladu jsou ilustrační. Při chybě a při 30 sekundách načítání s dostupným internetem se postupně zkoušejí další adresy, stále pod stejným rádiem. Po vyčerpání všech adres se přehrávání zastaví a zobrazí chybu. Ruční spuštění začíná znovu od hlavní adresy. Záložní vysílání ideálně volte na jiném serveru. Katalogový editor 1.1 obsahuje pole Záložní streamy, jednu adresu na řádek.
