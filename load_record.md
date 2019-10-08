- Se necesita importar el modulo N/record
- Se debe tener el id del registro que se quiere cargar
- No se debe utilizar para actualizar un registro, para actualizar se debe usar (record.submitFields)

~~~
var objOpportunity = record.load({
    type: 'opportunity', id: id_opportunity
});

// forma de obtener un valor del registro
var opportunityType = objOpportunity.getValue({ fieldId: "custbody_ifx_opp_type" });
var quoteID = objOpportunity.getValue({ fieldId: 'custbody_ifx_opp_quoteid' }) || 0;
var itemsCount = objOpportunity.getLineCount({ sublistId: 'item' });
var id_currency = objOpportunity.getValue({ fieldId: 'currency' });
~~~
