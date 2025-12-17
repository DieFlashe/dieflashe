# Signatur

Es können eigene öffentliche Signatur-Keys verwendet werden.
Dazu müssen im Verzeichnis `%LocalAppData%\DieFlashe\data\` je eine `*.pub`-Datei erstellt werden.
Solch eine Datei hat in der 1. Zeile 258 Zeichen und in der 2. Zeile 6 Zeichen.
Diese Dateien werden beim Programmstart von der DieFlashe geladen und in der Log aufgelistet.
Später bei der Firmware-Prüfung wird der Dateiname in der Statusbar angezeigt.

 - Von Geräten die noch nicht der DieFlashe bekannt sind
   befindet sich der Key auf dem Gerät in `/etc/avm_firmware_public_key1`
   und auf dem Build-System in `freetz-ng/build/original/filesystem/etc/avm_firmware_public_key1`.

 - Von Intern- und Inhaus-Firmware die mit einem anderen Key signiert sind
   befindet sich der Key in der Datei `avm_firmware_public_key4`,
   außer wenn das Gerät keine Dect-Hardware hat, dann heißt die Datei `avm_firmware_public_key3`.

 - Von selbst signierten Freetz-NG Firmware
   befindet sich der Key auf dem Gerät in `/etc/avm_firmware_public_key8`
   und auf dem Build-System in `freetz-ng/.signature/pub`.

Fehlende Signatur-Schlüssel können gerne inklusive Firmware-Name reported werden.

