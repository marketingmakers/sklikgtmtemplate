# Šablona pro Sklik retargeting a konverze do Google Tag Manager

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
Dokud nebude šablona na oficiálním repository (nebude kompletně protestována), tak je nutné šablonu nasadit ručně. 

1. Stáhněte si soubor template.tpl
2. V menu v Google Tag Manager zvolte Templates (Šablony)
3. Vytvořte novou šablonu.
4. V pravém horním rohu rozklikněte tři tečky a zvolte Import.
5. A je to. Nyní můžete tvořit kompletní Sklik tagy:

![Ukázka Sklik tagu](https://resources.marketingmakers.net/sklikgtmtemplate/template_preview.png)

## Důležité upozornění
Jedná se o první verzi, která byla testována jen na několika projektech.

Prosím, pište všechny chyby a poznámky na michal@marketingmakers.net
