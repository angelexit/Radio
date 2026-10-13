# Aktualizace moderního iRMP

Nahrajte složku updates do kořene repozitáře angelexit/Radio ve větvi main. Aplikace čte updates/modern.json.

Pro vydání nejprve vytvořte GitHub Release (např. v1.0.11) a připojte APK iRMP_1.0.11_Final_GitHub_Updates.apk. Až APK existuje, zveřejněte modern.json s jejím skutečným downloadUrl. Neoznamujte verzi dřív, než lze APK stáhnout.

Při další verzi změňte versionCode na vyšší číslo (Android build), versionName, downloadUrl a notes. applicationId a edition zachovejte. Stejný nebo nižší versionCode nevyvolá oznámení. Aktualizační APK musí mít stejný podpis, aby zachovala data při instalaci přes starou verzi.

Automatická kontrola probíhá při otevření/návratu, nejvýš jednou za 24 hodin po úspěšné kontrole. Při chybě automatický pokus opakuje nejdříve za hodinu; ruční tlačítko lze použít kdykoli. Stažení a instalace vyžadují akci uživatele. Upozornění lze skrýt do další verze.

První verze s kontrolou je 1.0.11 (build 32). Starší instalace ji samy neohlásí; první aktualizaci je nutné předat ručně.

## Legacy

Legacy čte updates/legacy.json. Zachovejte applicationId exit.angel.irmplegacy, edition legacy. První verze s aktualizacemi je 1.0.15-legacy (build 16). U nových verzí zvyšte versionCode, zveřejněte APK ve vlastní GitHub Release a aktualizujte versionName, downloadUrl, sha256 a notes. sha256 je SHA-256 přesného finálního APK souboru. APK musí mít původní podpis a stejnou identitu aplikace.

Na Androidu 4.1–4.4 aplikace stáhne APK sama přes ověřené HTTPS, ověří SHA-256, identitu, vyšší build a podpis a otevře instalátor Androidu. Není potřeba Windows ani Odblokovat. Android stále vyžaduje povolení instalace z neznámých zdrojů a potvrzení instalace. Na Androidu 7+ Legacy otevře stažení v prohlížeči. Moderní a Legacy vydávejte odděleně.

Xiaomi má vlastní metadata xiaomi.json s edition=xiaomi. Modern a Xiaomi sdílejí applicationId exit.angel.irmpalpha, proto používejte rostoucí kódy napříč oběma edicemi (aktuálně Xiaomi 35, Modern 36; další vydání alespoň 37). Legacy má samostatnou identitu a aktuální kód 17.
