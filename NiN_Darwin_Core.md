
# Habitat- og livsmediumvariabler fra NiN i Darwin Core 

#### Artsdatabanken 2021-03-24

Dette notatet er et forslag til enhetlig navnsetting og formatering av variabler som beskriver natursystem og livsmedium etter NiN i datastandarden Darwin Core. Slik standardisering er blant annet viktig for at data skal bli vist riktig i Artskart.

Artsdatabanken foreslår at variablene som beskriver natursystem og livsmedium blir lagt i Darwin Core-feltet _dynamicProperties_. Feltet tar data av typen _key:value_ som betyr av vi kan definere egne nøkkelord for bestemt variabler og knytte en verdi til hvert nøkkelord. For eksempel kan vi lagre natursystemdata for en observasjon i hovedtypen “Sanddynemark”, kartleggingsenhet “forstrand og primærdyner” som {"habitatNiN":"NA-T21-C-1""}. Oppslag i Artsdatabankens kode-API vil da peke på [https://nin-kode-api.artsdatabanken.no/v2.2/koder/hentkode/NA_T21-C-1](https://nin-kode-api.artsdatabanken.no/v2.2/koder/hentkode/NA_T21-C-1)

Feltnavn i Darwin Core er engelskspråklige, og vi foreslår å bruke nøkkelord for lagring av NiN variabler som også er på engelsk. Data vil slik være tilgjengelig for flere – særlig i forskingsmiljøene og internasjonalt. I de fleste tilfeller vil likevel NiN-kodene være på norsk, men det samme er situasjonen også for andre variabler i Artskart. Etter hvert er det mulig at Artsdatabanken kan tilby kodelister for NiN slik at samme datasett kan presenteres både på norsk eller engelsk.  

Nøkkelordene som vi foreslår å bruke er hentet fra presentasjonen av NiN i artikkelen av Halvorsen et al. (2020) publisert i Global Ecology and Biogeography og tilgjengelig her: [https://doi.org/10.1111/geb.13164](https://doi.org/10.1111/geb.13164).

Tabellen nedenfor gir en oversikt over variabler i NiN og nøkkelord for bruk i _dynamicProperties_ i Darwin Core. For generell informasjon om formatering av feltet _dynamicProperties_ referer vi til Darwin Core Quick Reference Guide: [https://dwc.tdwg.org/terms/#dwc:dynamicProperties](https://dwc.tdwg.org/terms/#dwc:dynamicProperties)

Darwin Core har allerede feltet _habitat_, og dette vil bli lest av Artskart som fritekst dersom variabelen _habitatRemark_ er tom.

Nye versjoner av NiN kan føre til endringer i kodene som blir brukt for eksempel for natursystem. Det er derfor nødvendig å ha informasjonen om hvilken versjon av NiN dataene referer til. Informasjon om NiN-versjon er derfor lagt til som en egen variabel. Slik situasjonen er akkurat nå refererer livsmedium strengt tatt til en eldre versjon av NiN, men Artsdatabanken vil arbeide for at alle deler av NiN skal ha samme versjonsnummer. Informasjon om versjonsnummer spesifikt for livsmedium er derfor utelatt fra oppsettet nedenfor.

_Tabell med oversikt over nøkkelord for bruk i feltet dynamicProperties i Darwin Core. Nøkkelord merket * er nødt til å ha verdier som samsvarer med kodeliste for NiN for å bli lest inn i Artskart._



|**Variabel**|**Nøkkelord dynamicProperties**|
|:---|:---|
|natursystem|habitatNiN *|
|NiN versjonsnummer|versionNiN|
|natursystem fritekst|habitatRemark|
|||
|substrat art|substrateSpecies|
|substrat artsID|substrateSpeciesID 1|
|substrat art fritekst|substrateSpeciesRemark|
|||
|livsmedium|microhabitatNiN *|
|livsmedium fritekst|microhabitatRemark|

<br>
<br>

------------------------------------------------
<sup>1</sup> artsID blir automatisk lagt til av Artsdatabanken dersom artsnavnet er et gyldig navn i Artsnavnebase

