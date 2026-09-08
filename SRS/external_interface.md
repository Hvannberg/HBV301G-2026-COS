

# Ytri tenging (External interface)

Lýsing á tengingu milli hugbúnaðarkerfisins og notanda, annars hugbúnaðar, vélbúnaðar eða samskiptakerfis.


<a id="EI-1"></a>
## EI-1 Tenging við SAP Payroll

## 🔌 Skil
COS skal tengjast SAP Payroll í gegnum REST API. Er nánari skilgreining en í COS skjölum

## 📥 Inntak / úttak
COS fær upplýsingar frá SAP Payroll um skráningu og heimild
starfsmanns til launadráttar og sendir greiðslubeiðnir vegna
keyptra máltíða.

## 📚 Samskipti og staðlar
REST API yfir HTTPS. Gögn eru send og móttekin á JSON-sniði.

 ## 📌 Tegund skila
- [ ] Notendaviðmót (User interface)
- [x] Hugbúnaðarviðmót (Software interface)
- [ ] Vélbúnaðarviðmót (Hardware interface)
- [ ] Samskiptaviðmót (Communications interface)


<a id="EI-2"></a>
## EI-2 Tenging við birgðakerfi mötuneytisins, CaféStock

## 🔌 Skil
COS skal hafa forritaskil við CaféStock. Hugbúnaðurinn er heimasmíðað kerfi fyrirtækisins sem heldur utan um birgðir mötuneytisins.

## 📥 Inntak / úttak
COS fær upplýsingar frá CaféStock um hvaða matvara er í boði og sendir upplýsingar um magn pantaðrar matvöru.

## 📚 Samskipti og staðlar
Ekki tilgreint í COS. Í þessari útfærslu er gert ráð fyrir HTTP og JSON.

 ## 📌 Tegund skila
- [ ] Notendaviðmót (User interface)
- [x] Hugbúnaðarviðmót (Software interface)
- [ ] Vélbúnaðarviðmót (Hardware interface)
- [ ] Samskiptaviðmót (Communications interface)
