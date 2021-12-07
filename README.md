# Šablona pro Sklik a Zboží retargeting a konverze do Google Tag Manager

Short description in English: This template is dedicated to PPC platform Sklik from Seznam.cz that is popular mainly in the Czech republic. By this template you are able to send both retargeting and conversion data. Other description follows in Czech language.

S touto šablonou nastavíte tagy pro retargeting i konverze. Není tedy nutné kopírovat a vkládat kódy, které vygeneruje Sklik, vše je možné dělat v příjemném uživatelském rozhraní.  

Šablona podporuje verzi sledovacího kódu publikovanou 23. listopadu 2021. 

``` HTML
<script type="text/javascript" src="https://c.seznam.cz/js/rc.js"></script>
<script>
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

![Ukázka Sklik tagu](https://resources.marketingmakers.net/sklikgtmtemplate/template_preview.png)

## Postup nasazení
Při výběru tagu zvolte "Discover more tag types in the Community Template Gallery", vyhledejte tag Sklik a povolte nezbytná oprávnění. Takto přidaný tag vám bude nabízet i možnost aktualizací při úpravách. 

[![Návod k nasazení tagu na YouTube](https://resources.marketingmakers.net/sklikgtmtemplate/sklik_template_ytb.png)](https://youtu.be/bcmNIpcvzl0 "Návod k nasazení tagu na YouTube")

## Jak číst souhlas z proměnné a spouštět Sklik tag se správným oprávněním?
Pokud chcete pouštět Sklik tag se správnou úrovní souhlasu, je více cest, jak toho dosáhnout. Jednu s využitím Tag Manageru ukazujeme zde:

[![Jak číst souhlas z proměnné a spouštět Sklik tag se správným oprávněním](https://resources.marketingmakers.net/sklikgtmtemplate/cteni_souhlasu2.JPG)](https://youtu.be/B8RaDx4reCg "Návod k čtení souhlasu z proměnné")



## Problémy a podpora
Veškeré problémy nebo i podezření na problém prosím hlaste na michal@marketingmakers.net nebo vytvořte issue zde na GitHubu. 

## Další rozvoj
Aktuálně plánuji přidat podporu Consent Managementu pro tento tag. Zatím můžete nezbytné souhlasy upravovat přímo v tagu. 
