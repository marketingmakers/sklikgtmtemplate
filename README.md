# Šablona pro Sklik retargeting a konverze do Google Tag Manager

Short description in English: This template is dedicated to PPC platform Sklik from Seznam.cz that is popular mainly in the Czech republic. By this template you are able to send both retargeting and conversion data. Other description follows in Czech language.

Umí kompletní strukturu tagů od Sklik, konkrétně dokáže nastavit kompletně tyto tagy: 

``` HTML
<!-- Měřicí kód Sklik.cz pro konverze -->
<script type="text/javascript">
var seznam_cId = X;
var seznam_value = Y;
</script>
<script type="text/javascript" src="https://www.seznam.cz/rs/static/rc.js" async></script>

<!-- Měřící kód Sklik pro retargeting -->
<script type="text/javascript">
	/* <![CDATA[ */
	      var seznam_retargeting_id = xxxx;
        var seznam_itemId = "id";
        var seznamPagetype = "offerdetail";
        var seznam_category = "název_kategorie";
	/* ]]> */
</script>
<script type="text/javascript" src="//c.imedia.cz/js/retargeting.js"></script>
```
## Postup nasazení
Při výběru tagu zvolte "Discover more tag types in the Community Template Gallery", vyhledejte tag Sklik a povolte nezbytná oprávnění. Takto přidaný tag vám bude nabízet i možnost aktualizací při úpravách. 

Dokud tag nebude schválen v template gallery, je nutné stáhnout soubor template.tpl, v GTM zvolte Šablony a vytvořte novou šablonu. V pravém horním rohu rozklikněte tři tečky a zvolte Import.

![Ukázka Sklik tagu](https://resources.marketingmakers.net/sklikgtmtemplate/template_preview.png)

## Důležité upozornění
Jedná se o první verzi, která byla testována jen na několika projektech.

Prosím, pište všechny chyby a poznámky na michal@marketingmakers.net
