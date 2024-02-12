# Šablona pro Sklik a Zboží retargeting a konverze do Google Tag Manager

Short description in English: This template is dedicated to PPC platform Sklik and comparison shopping engine Zbozi.cz from Seznam that is popular mainly in the Czech republic. By this template you are able to send both retargeting and conversion data. Other description follows in Czech language.

S touto šablonou nastavíte tagy pro retargeting i konverze. Není tedy nutné kopírovat a vkládat kódy, které vygeneruje Sklik, vše je možné dělat v příjemném uživatelském rozhraní.  

Šablona podporuje verzi sledovacího kódu publikovanou 12. února 2024. 

``` HTML
<script type="text/javascript" src="https://c.seznam.cz/js/rc.js"></script>
<script>
// Nastavení objektu identity
	window.sznIVA.IS.updateIdentities({  
		eid: "hodnota emailu", // Email či zahashovaný email
		aid: {
			"a1": "stát", // Vyplňte stát
			"a2": "město", // Vyplňte město
			"a3": "ulice", // Vyplňte ulici
			"a4": "číslo popisné", // Vyplňte číslo popisné
			"a5": "PSČ", // Vyplňte poštovní směrovací číslo
		},
		tid: "hodnota telefonního čísla" // Hodnota telefonního čísla
	});

var conversionConf = {
  id: 10000000, /* identifikátor konverze Sklik*/
  value: 199.9, /* hodnota objednávky v Kč*/
  orderId: 123456, /* identifikátor objednávky Zboží.cz*/
  zboziType: “standard”, /* “standard” (standardní měření), “limited” (omezené měření), nebo “sandbox” měření konverzí Zboží.cz */
  zboziId: “QQQQ”,  /* ID provozovny Zboží.cz*/
  consent: 1 /* souhlas od návštěvníka na odeslání konverzního hitu, povolené hodnoty: 0 (není souhlas) nebo 1 (je souhlas) */
};
 // Ujistěte se, že metoda existuje, předtím než ji zavoláte
 if (window.rc && window.rc.conversionHit) {
   window.rc.conversionHit(conversionConf);
 }
</script>


<!-- Měřící kód Sklik pro retargeting -->
<script type="text/javascript" src="https://c.seznam.cz/js/rc.js"></script>
<script>
// Nastavení objektu identity
	window.sznIVA.IS.updateIdentities({  
		eid: "hodnota emailu", // Email či zahashovaný email
		aid: {
			"a1": "stát", // Vyplňte stát
			"a2": "město", // Vyplňte město
			"a3": "ulice", // Vyplňte ulici
			"a4": "číslo popisné", // Vyplňte číslo popisné
			"a5": "PSČ", // Vyplňte poštovní směrovací číslo
		},
		tid: "hodnota telefonního čísla" // Hodnota telefonního čísla
	});

var retargetingConf = {
  rtgId: 123456, /* identifikátor retargeting */
  itemId: "67890", /* identifikátor nabídky */
  category: "Zahrada | Stínící technika | Zahradní slunečníky", /* kategorie eshopu */
  pageType: "offerdetail", /* typ stránky - offerdetail, category */
  rtgUrl: "https://example.com?hello=world", /*  */
  consent: 1, /* souhlas od návštěvníka na odeslání retargetingového hitu, povolené hodnoty: 0 (není souhlas) nebo 1 (je souhlas) */
};
 // Ujistěte se, že metoda existuje, předtím než ji zavoláte
 if (window.rc && window.rc.retargetingHit) {
   window.rc.retargetingHit(retargetingConf);
 }
</script>
```

![Ukázka Sklik tagu](https://resources.marketingmakers.net/sklikgtmtemplate/ukazka_sklik_tagu.JPG)

## Postup nasazení
Při výběru tagu zvolte "Discover more tag types in the Community Template Gallery", vyhledejte tag Sklik & Zbozi.cz a povolte nezbytná oprávnění. Takto přidaný tag vám bude nabízet i možnost aktualizací při úpravách. 

[![Návod k nasazení tagu na YouTube](https://resources.marketingmakers.net/sklikgtmtemplate/sklik_template_ytb.png)](https://youtu.be/bcmNIpcvzl0 "Návod k nasazení tagu na YouTube")

## Jak číst souhlas z proměnné a spouštět Sklik tag se správným oprávněním?
Pokud chcete pouštět Sklik tag se správnou úrovní souhlasu, je více cest, jak toho dosáhnout. V políčku souhlas můžete zvolit následující možnosti:
- **Poskytnut** - Skliku se odešle hodnota 1, tedy že uživatel souhlasí, 
- **Neposkytnut** - Skliku se odešle hodnota 0, tedy že uživatel nesouhlasí,
- **Dle souhlasu v analytics_storage** - Při spuštění tagu přečte tag hodnotu z aktuálního stavu souhlasu s analytickým úložištěm dle Google Consent Mode
- **Dle souhlasu v ad_storage** - Při spuštění tagu přečte tag hodnotu z aktuálního stavu souhlasu s reklamním úložištěm dle Google Consent Mode
- **{{výběr proměnné}}** - můžete poslat i jakoukoliv vlastní proměnnou, ve které musí být hodnota 1 nebo 0 (ať již číslem či textem)
- **Od poslední aktualizace není možné vybrat Neurčeno. Nezadáte-li tedy souhlas, je považováno, že souhlas nemáte. **

V rámci čtení souhlasu s analytics_storage a ad_storage nepracuje tag s wait_for_update ani nespouštím znovu tag v případě změny souhlasu. Toto musíte ohlídat správnými triggery u tagu. Můžete také využít konkurenční šablonu, Sklik (červené logo), která ošetřuje i tuto možnost. 

## Problémy a podpora
Veškeré problémy nebo i podezření na problém prosím hlaste na michal@marketingmakers.net nebo vytvořte issue zde na GitHubu. 
