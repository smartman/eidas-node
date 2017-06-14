---
title: Ülevaade
permalink: Autentimisteenused
---

## Ülevaade

Käesolev dokument esitab RIAs arendatavate autentimisteenuste, nii siseriiklike kui ka piiriüleste,  teenuseprofiilid (teatmelised lühikirjeldused).

Kõigepealt esitatakse tabelisse koondatult iga teenuse kohta: identifikaator (koodnimetus), lühi- ja täispikk nimetus, võimalikud  alternatiivnimetused, sihtrühma lühikirjeldus ja MUST/NICE TO HAVE atribuut.

Seejärel esitatakse iga teenuse kohta eraldi: teenuse kasutusvoo ülevaatlik kirjeldus, kasutatavate standardite ja tehnoloogiate loetelu ja kõrgvaateline arhitektuurijoonis.

_Märkus._ Seadmata kahtluse alla teenuste kombineerimise (ingl _bundling_) otstarbekust, kas tehnilise teostuse või marketingi eesmärgil, on käesoleva liigituse aluseks siiski võetud teenuste fokusseerimine sihtrühmadele.  (Põhimõte, et teenusel ei saa olla mitut erinevat sihtrühma). Liigituse eesmärk on ka loodetavasti teha sammuke teenuste nimetusi arusaadavamaks tegemise suunas. "eIDAS Node" ei ole teenusenimetusena päris hea, sest selles sees on kolm erinevat, täiesti erinevatele sihtrühmadele pakutavat (osa)teenust. "Isikutuvastusportaal" on hea üldmõistena, kuid tuleb silmas pidada, et ka selle kaudu on kavas pakkuda kolmele erinevale sihtrühmale kolme erinevat teenust. See ei tähenda, et "eIDAS Node" ja "Isikutuvastusportaal" terminitena kasutuskõlblikud oleksid. Lihtsalt tuleks lisada selgitus, millise sihtrühma millist teenusekasutusvoogu  või -voogusid silmas peetakse. "Selgemad" nimetused on allolevas tabelis märgendatud punasega. Teenusenimede kujundamine on pikk protsess. Käesolev dokument ei sea eesmärgiks nimetusi fikseerida. - Priit P 

Arhitektuurijooniste juures tasub meeles pidada, et sõnumivahetused (v.a pärimine Äriregistrist üle X-tee) teostatakse kasutaja veebisirvija ümbersuunamiste (_redirect_), aga ka OpenID Connect _backend_-päringute abil. Tähistused: `EE` - Eesti, `SE` - Rootsi (välisriigi näitena).

| Id | lühinimetus | nimetus | alternatiiv-nimetused | sihtrühm | MUST/NICE |
|:---:|:---------:|:-----------:|:-------:|:--------:|
|  1   | eIDAS väljaminev | <span class='Q'>eIDAS autentimispäringute vahendusteenus välisriikidesse</span> | RIA eIDAS Node | Eesti asutus, kes tahab e-teenust pakkuda välisriigi eID kasutajale | eIDAS MUST |
|  2   | eIDAS sissetulev | <span class='Q'>välisriikidest saabuvate eIDAS autentimispäringute täitmise teenus</span> | RIA eIDAS Node, isikutuvastusportaal, elektrooniline isikutuvastusportaal | välisriigi asutus, kes soovib Eesti eID kasutajale osutada e-teenust, välisriigi eIDAS konnektorteenuse kaudu | eIDAS MUST |
|  3   | eIDAS konnektorteenus | <span class='Q'>eIDAS konnektorteenus Eesti asutusele</span> | RIA eIDAS Node, isikutuvastusportaal, elektrooniline isikutuvastusportaal | välis-eID kasutajaid teenindav Eesti asutus, kes eelistab Eesti eIDAS konnektorteenusega liidestuda otse (nt RIK) | eIDAS mugavus |
|  4   | <span class='Q'>SSO teenus</span> | <span class='Q'>Ühekordse sisselogimise teenus</span> |  | Eesti e-teenuse osutaja, kes soovib, et teabeväravast eesti.ee suunatakse kasutaja e-teenusesse autenditult; Eesti asutused, kes soovivad födereerunult pakkuda Eesti eID kasutajale SSO kasutajakogemust | MUST (Eesti) |
|  5   | <span class='Q'>Siseriiklik autentimisteenus</span> | Eesti e-teenust Eesti eID-ga kasutava inimese autentimise teenus | isikutuvastusportaal, elektrooniline isikutuvastusportaal, eesti.ee autentimisteenus, RIA autentimisteenus | e-teenust pakkuv Eesti asutus, kes Eesti eID kasutaja autentimist eelistab teenusena sisse osta |  mugavus (Eesti) |

