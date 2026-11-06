# THE MACHINE · PROJECT FINCH 0.2

Mobilvennlig, gratis PWA for Safari på iPhone og PC. Denne prototypen er en **lokal regelbasert beslutningssimulator**, ikke en språkmodell eller AGI.

## Funksjoner

- Oppdrag med kategorier, begrunnede forslag og tydelig usikkerhet.
- Manuell godkjenning og korrigering.
- Enkel preferanselæring: hver kategori har to faste strategier, og godkjente strategier prioriteres etter historiske tilbakemeldinger med Laplace-utjevning.
- Beslutningslogg lagret lokalt, eksport/import av JSON og sletting.
- Mobilvennlig grensesnitt, grunnleggende tilgjengelighet og offline-støtte.
- Ingen API-nøkler, kontoer eller kostnader.

## Bruk og publisering

GitHub Pages: Settings → Pages → Deploy from a branch → main → /(root). Dette krever at pull requesten først er gjennomgått og slått sammen i main. Åpne deretter adressen i Safari og velg Del → Legg til på Hjem-skjerm.

Alternativt kan du åpne `index.html` via en lokal webserver. PWA-cache krever HTTPS eller localhost.

## Kontroller

Test på iPhone: velg kategori, skriv oppdrag, analyser, godkjenn eller korriger, åpne Hukommelse, eksporter, importer og test etter omlasting. Kontroller også offline etter første besøk.

## Sikkerhet og begrensninger

Ingenting sendes til en server av appens egen kode; all historikk lagres i nettleserens localStorage. GitHub Pages leverer nettstedet og har vanlig hosting-/tilgangslogging. Dette er **ikke kryptert eller synkronisert**, og egner seg ikke til sensitive opplysninger. Enhetens nettstedsdata kan slettes. En korrigering brukes bare som et negativt utfall for valgt strategi, ikke som generell læring av naturlig språk. Endring av kildekode eller handlinger i eksterne systemer krever senere separate, eksplisitte godkjenningsmekanismer.
