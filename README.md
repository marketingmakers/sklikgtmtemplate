# sklikgtmtemplate
Sklik template pro Google Tag Manager

Zatím v první alfa verzi. 

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
Jedná se o první verzi. 

Prosím, pište všechny chyby a poznámky na michal@marketingmakers.net
