# iRMP radio-catalog

Složku radio-catalog nahrajte do kořene repozitáře angelexit/Radio, větev main. Aplikace načítá catalog.json. Název složky: radio-catalog.

Formát: schemaVersion: 1 a pole radios. Každé rádio má name, stream_url (HTTPS), country (název země), languages (pole názvů jazyků). Volitelné: id, logo_url, bitrate, format, genre, description. Jedno rádio může mít více jazyků.

Výchozí katalog obsahuje osm českých stanic ze stávající aplikace. Přidávejte další stanice do radios; nabídky zemí a jazyků se vytvářejí automaticky. Nedostupný GitHub nevymaže uložený katalog. Přidání do aplikace zachová původní seznam, přehrávanou stanici i oblíbené. Duplicitní streamy se přeskočí.

Moderní iRMP 1.0.12 zobrazuje známé země a jazyky podle jazyka rozhraní (cs, de, en). Přijímá názvy i běžné kódy; například Německo / DE a Němčina / de se v němčině zobrazí jako Deutschland a Deutsch. Uložený katalog se při přepnutí jazyka nemění. Další jazyky rozhraní lze později doplnit.
