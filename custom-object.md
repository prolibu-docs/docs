PROLIBU CUSTOM OBJECT
======

Los Custom Objects en Prolibu son objetos que parten desde cero y permiten cubrir las necesidades particulares de su negocio. Por ejemplo se puede crear un Custom Object llamado CustomObjectCRM y conectar su cuenta Prolibu con las oportunidades generadas dentro de su sistema o recepcionar datos de sus leads que provengan de un tráfico web y enviarles una cotización si así lo desea, también puede generar informes a detalle del estado de su cuenta y mucho más. Prolibu expone estos Custom Objects mediante un web service o web services que es una tecnología que utiliza un conjunto de protocolos y estándares que sirven para intercambiar datos entre aplicaciones; y mediante el uso de REST (Representational State Transfer) la arquitectura que, haciendo uso del protocolo HTTP, proporciona una API que utiliza cada uno de sus métodos (GET, POST, PUT, DELETE, etcétera) para poder realizar diferentes operaciones entre la aplicación que ofrece el servicio web y el cliente.

Estos Custom Objects son implementados dentro de su cuenta Prolibu por uno de nuestros expertos de TI mediante un contrato de datos en el cual se acuerdan que campos y comportamientos debe tener este nuevo objeto dentro de la plataforma. A continuación veremos un ejemplo de un contrato de datos.

```json
{
    "uuid": "090392-T90",
    "lead": {
        "firtsName": "Jane",
        "lastName": "Doe",  
        "email": "janed@prolibu.com",
        "mobile": "+57 3128932934",
        "metadata": {
            "source": "Facebook"
        }
    },
    "agent": {
        "firtsName": "John",
        "lastName": "Doe",  
        "email": "jdoe@prolibu.com",
        "mobile": "+57 3128932934"
    },
    "data": {
        "title": "Get now!",
        "expirationDate": "2021-03-30",
        "metadata": {
            "commercialTerms": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam egestas eu risus nec tristique.",
            "relatedInformationTable": "<table><thead><tr><th>one</th></tr></thead><tbody><tr><td>description</td></tr></tbody></table>",
            "financinglPlan": {
                "start": 2000,
                "monthlyPayment": 200,
                "interestRate": 1.5
            }
        },
        "products": [
            {
                "sku": "992DNUW92UE",
                "quantity": 1,
                "discountRate": 10,
                "currency": "USD",
                "metadata": {
                    "images": [
                        "https://s3.amazonaws.com/cdn.prolibu.com/rest-api-doc-images/Profile-menu.png",
                        "https://s3.amazonaws.com/cdn.prolibu.com/rest-api-doc-images/Profile-menu.png"
                    ]
                }    
            }
        ] 
    }
}
```

## Información adicional: 
* Para más información sobre el campo *lead por favor visite el siguiente [link](https://prolibu-docs.github.io/docs/#/reference-lead).
* Para más información sobre el campo *agent por favor visite el siguiente [link](https://prolibu-docs.github.io/docs/#/reference-user).
* Para más información sobre el campo *data por favor visite el siguiente [link](https://prolibu-docs.github.io/docs/#/reference-proposal).
* Los campos *metada para todos los modelos son abiertos por lo que usted es libre de agregar la información que considere importante a la hora de crear un registro. 
* La respuesta de un Custom Object puede variar de uno  a otro dependiendo su finalidad, pero principalmente regresa la misma estructura con los elementos generados. Por ejemplo en caso de que tengamos un Custom Object para generar cotizaciones a parte de devolver la estructura inicial procesada se anexarán 2 campos mas de tipo URL, uno con una url limpia para que el agente comercial pueda visualizar la propuesta y otra (un short link) afinada para ser compartida con el lead.


## Artículos Relacionados
* Para conectarse con a un web service Prolibu visite el siguiente [link](https://prolibu-docs.github.io/docs/#/guide).
* Para generar un Api Key Prolibu visite el siguiente [link](https://github.com/prolibu-docs/docs/blob/main/api-key.md).


---------------
© 2020 PROLIBU TECH SAS, ALL RIGHTS RESERVED.
