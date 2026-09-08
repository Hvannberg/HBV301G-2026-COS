# 📄 Software Requirements Specification (SRS)
Cafeteria Ordering System 

## 1. Inngangur
### 1.1 Tilgangur
Meginmarkmið COS kerfisins er að með nýjum sjálfvirkum ferlum megi gera pantanir skilvirkari (hraðvirkari og með minni mannafla), og
villufrírri. Markmið kerfisins er að veita notendum þjónustu til að panta 24/7 í staðinn fyrir frá 8-16. Í núverandi kerfi eyða starfmenn umtalsverðum tíma
í að fara í mötuneytið, velja, panta, bíða eftir matnum og greiða fyrir hann. Að meðaltali tekur það um 65 mínútur. Sumir starfsmenn hringja inn pöntun í síma. Umtalsverðar birgðir fara til spillis.
Þegar starfsmenn borða út í bæ tekur það allt að 90 mínútur.

### 1.2 Umfang og mörk kerfisins

**Innan umfangs (scope):**
Þróun kerfisins nær til þess að gera starfsmönnum kleift að senda inn
pantanir í mötuneyti og styðja starfsfólk mötuneytis við að afgreiða
pantanir og senda beiðnir um afhendingu og útbúa matseðla.

**Utan umfangs (scope):
Í þessari útgáfu nær þróunin ekki til pantana frá utanaðkomandi
veitingastöðum eða greiðslu með greiðslukorti.

** Samhengi og mörk kerfisins: (context og system boundary)
COS hefur samskipti við birgðakerfi og launakerfi. Aðrir þættir í
samhengi kerfisins sem hafa áhrif á kröfur eru leiðbeiningar um
næringargildi málsverða, kjarasamningar um niðurgreiðslu fæðis
á vinnustöðum og ferli sem lýsa afhendingu pantana.




### 1.3 Skilgreiningar
| Hugtak | Skýring |
|--------|---------|
| SRS | Software Requirements Specification|
|        |         |


### 1.4 Tilvísanir
- ISO/IEC/IEEE International Standard - Systems and software engineering -- Life cycle processes -- Requirements engineering," in ISO/IEC/IEEE 29148:2018(E) , vol., no., pp.1-104, 30 Nov. 2018, doi: 10.1109/IEEESTD.2018.8559686.ISO/IEC/IEEE 29

---

## 2. Almenn lýsing
### 2.1 Notendahópar
-  Starfsmenn velja af matseðli og panta matinn. Kerfið kannar hvort starfsmaður hafi heimilað frádrátt kostnaðar frá launum. Starfsmaður fær síðan matinn afhentan. Pöntunin fer fram á innra netinu. Stundum pantar starfsfólk mat fyrir viðburði fyrir
   hópa starfsmanna og eða gesti
-  Starfsfólk í mötuneyti afgreiðir pöntun úr kerfinu, eldar matinn, pakkar honum inn og sendir inn beiðni um afhendingu
-  Sendlar fá beiðni um að afhenda pantanir. Sendlar ná í matinn úr mötuneyti og afhenda starfsmönnum
-  Matreiðslufólk útbýr matseðla  og bjóða einnig upp á rétt dagsins. Ekki verður hægt að bjóða upp á alla rétti til að borða utan mötuneytis (take a way)


### 2.2 Viðskiptaávinningur
- Starfsmenn eyða minni tíma í að panta mat,greiða fyrir hann og fá hann afhentan.
- Starfsfólk í mötuneyti eyðir minni tíma í að taka við pöntunum, t.d. í síma.
- Minni sóun á matarbirgðum
- Sendlar geta stytt tímann með því að safna saman pöntunum á deildir eða byggingar fyrirtækisins.

---

## 3. Kröfur fyrir kerfið

### 3.1 Viðskiptakröfur
| ID                                        | Titill                                                                  |
|-------------------------------------------|-------------------------------------------------------------------------|
| [BREQ-1](business_requirements.md#breq-1) | Lækka rýrnun matarbirgða í mötuneyti um 40% innan 6 mánaða              |
| [BREQ-2](business_requirements.md#breq-2) | Auka meðal raunvinnutíma starfsmanns sem notar mötuneytið um 15 mínútur |

### 3.2 Kerfiskrafa
| ID                              | Titill                 |
|---------------------------------|------------------------|
| [SR-1](system_requirement.md#sr-1) | Rafrænt pöntunar- og afgreiðsluferli máltíða |

### 3.3 Eiginleikar (Features)
| ID                    | Titill                                                  |
|-----------------------|---------------------------------------------------------|
| [F-1](feature.md#f-1) | Panta og greiða fyrir máltíðir frá matseðli í mötuneyti |
| [F-2](feature.md#f-2) | Búa til og skoða matseðla                               |
| [F-3](feature.md#f-3) | Aðgangur að COS                                         |

### 3.4 Notendakröfur
| ID                               | Titill                         | Eiginleiki            |
|----------------------------------|--------------------------------|-----------------------|
| [UR-1](user_requirement.md#ur-1) | Panta máltíð til afhendingar   | [F-1](feature.md#f-1) |
| [UR-2](user_requirement.md#ur-2) | Breyta eða hætta við pöntun    | [F-1](feature.md#f-1) |
| [UR-3](user_requirement.md#ur-3) | Skoða matseðil                 | [F-2](feature.md#f-2) |
| [UR-4](user_requirement.md#ur-4) | Búa til matseðil               | [F-2](feature.md#f-2) |
| [UR-5](user_requirement.md#ur-5) | Aðgangur að COS á innraneti    | [F-3](feature.md#f-3) |
| [UR-6](user_requirement.md#ur-6) | Aðgangur að COS af Internetinu | [F-3](feature.md#f-3) |

### 3.5 Virknikröfur
| ID                                       | Titill                                | Notendakrafa                     |
|------------------------------------------|---------------------------------------|----------------------------------|
| [FR-1](functional_requirement.md#fr-1)   | Velja máltíð                          | [UR-1](user_requirement.md#ur-1) |
| [FR-2](functional_requirement.md#fr-2)   | Velja afhendingu                      | [UR-1](user_requirement.md#ur-1) |
| [FR-3](functional_requirement.md#fr-3)   | Staðfesta pöntun                      | [UR-1](user_requirement.md#ur-1) |
| [FR-4](functional_requirement.md#fr-4)   | Breyta pöntun                         | [UR-2](user_requirement.md#ur-2) |
| [FR-5](functional_requirement.md#fr-5)   | Hætta við pöntun                      | [UR-2](user_requirement.md#ur-2) |
| [FR-6](functional_requirement.md#fr-6)   | Takmarka breytingar á útbúinni pöntun | [UR-2](user_requirement.md#ur-2) |
| [FR-7](functional_requirement.md#fr-7)   | [Virkni]                              | UR-3                             |
| [FR-8](functional_requirement.md#fr-8)   | [Virkni]                              | UR-3                             |
| [FR-9](functional_requirement.md#fr-9)   | [Virkni]                              | UR-3                             |
| [FR-10](functional_requirement.md#fr-10) | [Virkni]                              | UR-4                             |
| [FR-11](functional_requirement.md#fr-11) | [Virkni]                              | UR-4                             |
| [FR-12](functional_requirement.md#fr-12) | [Virkni]                              | UR-4                             |
| [FR-13](functional_requirement.md#fr-13) | [Virkni]                              | UR-5                             |
| [FR-14](functional_requirement.md#fr-14) | [Virkni]                              | UR-5                             |
| [FR-15](functional_requirement.md#fr-15) | [Virkni]                              | UR-5                             |
| [FR-16](functional_requirement.md#fr-16) | [Virkni]                              | UR-6                             |
| [FR-17](functional_requirement.md#fr-17) | [Virkni]                              | UR-6                             |
| [FR-18](functional_requirement.md#fr-18) | [Virkni]                              | UR-6                             |

### 3.6 Viðskiptareglur
| ID                              | Titill                         |
|---------------------------------|--------------------------------|
| [BRG-1](business_rule.md#brg-1) | Verð pöntunar                  |
| [BRG-2](business_rule.md#brg-2) | Afhendingagluggi er 15 mínútur |

### 3.7 Gæðaeiginleikar
| ID                                | Titill                                     |
|-----------------------------------|--------------------------------------------|
| [QA-1](quality_attribute.md#qa-1) | Öryggi við meðhöndlun viðkvæmra upplýsinga |
| [QA-2](quality_attribute.md#qa-2) | Nothæfi                                    |

### 3.8 Takmarkanir
| ID                       | Titill                  |
|--------------------------|-------------------------|
| [C-1](constraint.md#c-1) | HTML 5.0 staðall        |
| [C-2](constraint.md#c-2) | C-2 Oracle gagnagrunnur |

### 3.9 Ytri skil (Interfaces)
| ID                                 | Titill                                |
|------------------------------------|---------------------------------------|
| [EI-1](external_interface.md#ei-1) | Tenging við launakerfi                |
| [EI-2](external_interface.md#ei-2) | Tenging við birgðakerfi mötuneytisins |

---

## 4. Viðaukar
### 4.1 Orðalisti
- Skilgreina lykilhugtök.

  | Hugtak | Skilgreining |
  |--------|--------------|
  |        |              |
  |        |              |

### 4.2 Samþykktir
- Kennari: ____________________  
- Nemandi: ____________________
