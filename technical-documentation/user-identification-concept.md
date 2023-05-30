# User Identification Concept

User identification is relevant for claiming virtual funds. It ensures that users can claim their virtual funds only at a specific age, only with a German residence, and only once per person.

<!-- toc-start -->
<!-- GENERATED CONTENT -->
- [Overview]
- [Technical Building Blocks]
- [Technical Flow]
- [Background Information]
  - [eID / Electronic ID Card]
  - [ID Documents of German Residents]
  - [Proof of Residence]

[Overview]: #overview
[Technical Building Blocks]: #technical-building-blocks
[Technical Flow]: #technical-flow
[Background Information]: #background-information
[eID / Electronic ID Card]: #eid--electronic-id-card
[ID Documents of German Residents]: #id-documents-of-german-residents
[Proof of Residence]: #proof-of-residence
<!-- toc-end -->

## Overview

At the beginning, the KulturPass is going to support eID-compatible documents only. However, over time the scope of the solution will evolve, so later the users may identify with other documents as well.  The term "eID-compatible documents" for now covers regular German ID cards and resident permits.

For unique identification of a person verification of the identification document needs to be performed. As a first step, the technical **eID verification** will be implemented leveraging the eID service of the German Bundesdruckerei. This procedure performs the verification of eID-compatible documents on a NFC-capable mobile device. On desktop, the machine can be paired with an NFC-capable mobile device. The verification can be done by the user himself, the procedure does not require any human agent to be involved.

## Technical Building Blocks

The technical building blocks will be described in separate documents for each means of verification:

- for eID verification, see [User Identification with eID](./user-identification-with-eid.md#technical-building-blocks)

Other means of verification might be added in the future.

## Technical Flow

The technical flow will be described in separate documents for each means of verification.

## Background Information

### eID / Electronic ID Card

The eID (electronic ID card, DE: elektronischer Personalausweis) is an ID card that is NFC-capable. Users can share the content of their eID with authorized applications. This requires an NFC-capable device and knowledge of an eID-specific transport PIN (5 or 6 digits).

An eID can share the following information:

- first name, last name, alias, doctoral degree
- whether the person is of a certain age
- date of birth, place of birth
- address
- document type (see below)
- whether the person's address matches a given residence
- pseudonymous identifier (scoped per authorized application)

Since May 2017, the eID capability is activated by default on newly issued documents and cannot be deactivated anymore.

The following documents are eID-compatible:

| Name | Name (DE) | Audience | Example |
|---|---|---|---|
| German ID card | (neuer) Personalausweis (nPA) | German citizens (DE: Staatsbürger) | [example ⎆](https://de.wikipedia.org/wiki/Personalausweis_(Deutschland)#/media/Datei:Personalausweis_(2021).png) |
| electronic residence permit | elektronischer Aufenthaltstitel | non-EU/EEA citizens, refugees, etc. | [example ⎆](https://de.wikipedia.org/wiki/Elektronischer_Aufenthaltstitel#/media/Datei:Aufenthaltserlaubnis-Beschaeftigung.JPG) |
| eID card | eID-Karte | EU/EEA citizens | [example ⎆](https://de.wikipedia.org/wiki/EID-Karte#/media/Datei:EID-karte.png) |

The eID card was introduced in 2019 as a consequence of the online access act (DE: Onlinezugangsgesetz).

### ID Documents of German Residents

German residents may have different ID documents:

| Name /<br/>_Name (DE)_ | Contains<br/>residence | Distribution<br/>among users |
|---|---|---|
| German ID card<br/>_(neuer) Personalausweis_ | yes | • wide >=16 years<br/>• poor <16 years<br/>• only German citizens |
| Passport<br/>_Reisepass_ | no | • rather poor (DE citizens)<br/>• rather poor (EU/EEA citizens)<br/>• rather high (other citizens) |
| ID card (EU/EEA)<br/>_Ausweis (EU/EWR)_ | unreliable | • depending on the issuing country |
| electronic residence permit<br/>_elektronischer Aufenthaltstitel_ | yes | • wide (non-EU/EEA citizens)<br/>• age-independent |
| eID card<br/>_eID-Karte_ | yes | • rather very poor |
| student card<br/>_Schülerausweis_ | sometimes | • wide<br/>• age-independent |

Especially EU/EEA citizens do not necessarily have an eID-compatible ID card, as there are rather few services available that would motivate them to obtain an eID card at EUR 37.

Not all non-EU/EEA citizens necessarily have an electronic residence permit (e.g. some refugees from Ukraine).

This has the following consequences:

- producing a proof of identity under the age of 16 cannot be equally guaranteed, as it is not mandatory to have an ID card at that age
- eID-compatible ID cards must not be the only way to produce a proof of identity
- if the proof of identity is produced with a passport, an additional proof of residence must be produced (DE: Meldebescheinigung). The proof of residence is not digitally available in Germany.

### Proof of Residence

The proof of residence (DE: Meldebescheinigung) can be obtained from local authorities. It is not digitally available. The document must be scanned/photographed to digitize it. Accordingly, it cannot easily be verified automatically.

Back to [KulturPass DE - Technical Documentation](README.md)

Back to [KulturPass DE documentation](../README.md)
