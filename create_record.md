- Se necesita importar el modulo N/record
- Al guardar el record obtenemos el nuevo id

~~~
var objRecord = record.create({
    type: 'customrecord_ifx_opp_solution_design',
    isDynamic: true
});

objRecord.setValue('custrecord_ifx_design_customer', id_customer);
objRecord.setValue('custrecord_ifx_design_oppid', id_opportunity);
objRecord.setValue('custrecord_ifx_desing_estimate_id', id_estimate);
objRecord.setValue('custrecord_ifx_design_presales', id_employee);
var id_record = objRecord.save();
~~~
