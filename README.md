# Šablona pro Sklik retargeting a konverze do Google Tag Manager

Short description in English: This template is dedicated to PPC platform Sklik from Seznam.cz that is popular mainly in the Czech republic. By this template you are able to send both retargeting and conversion data. Other description follows in Czech language.

S touto šablonou nastavíte tag pro retargeting i konverze. Není tedy nutné kopírovat a vkládat tyto kódy, které vygeneruje Sklik, vše je možné dělat v příjemném uživatelském rozhraní.  

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

![Ukázka Sklik tagu](https://resources.marketingmakers.net/sklikgtmtemplate/template_preview.png)

## Postup nasazení
Při výběru tagu zvolte "Discover more tag types in the Community Template Gallery", vyhledejte tag Sklik a povolte nezbytná oprávnění. Takto přidaný tag vám bude nabízet i možnost aktualizací při úpravách. 

[![Návod k nasazení tagu na YouTube](https://resources.marketingmakers.net/sklikgtmtemplate/sklik_template_ytb.png)](https://youtu.be/bcmNIpcvzl0 "Návod k nasazení tagu na YouTube")


## Důležité upozornění
Jedná se o alfa verzi tagu, která je testována na cca 15ti projektech. Zatím bez jakýchkoliv problémů. I tak prosíme o obezřetnost a hlášení všeho nestandardního na michal@marketingmakers.net
