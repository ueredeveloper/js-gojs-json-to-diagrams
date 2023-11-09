# GoJS Sample Objects and Diagrams

This repository showcases GoJS objects and diagrams for various use cases. You can use the HTML and JavaScript in these samples as a starting point for your GoJS applications.

Javascript Object example to convert to gojs: 

Tabelas 
```
Tabela Documento_Tipo
let documento_tipo = {dt_id: 1, dt_descricao: "Requerimento"}
	
// Tabela Endereço
let endereco = {end_id: 1, end_logradouro: "Rua dos Feijões"}

// Tabela Documento
let documento = {
    doc_id: 1, 
    doc_numero: 123456,
    doc_tipo: documento_tipo,
    doc_endereco: endereco

		}
```

## Real Time Diagram

This diagram represents a real-time data visualization with nodes and links:

``` Real Time JSON
[
    {
        "key": 1,
        "c": "#b496b5",
        "text": 123456
    },
    {
        "key": 2,
        "c": "#50cf6f",
        "parent": 1,
        "text": "Requerimento"
    },
    {
        "key": 3,
        "c": "#1ea07f",
        "parent": 1,
        "text": "Rua dos Feijões"
    }
]
```
CheckBox Tree
```
[
    {
        "key": 1,
        "parent": 1
    },
    {
        "key": 2,
        "parent": 1
    },
    {
        "key": 3,
        "parent": 1
    }
]
```

MultiArrow Tree 1
```
[
    {
        "key": 1,
        "text": 123456,
        "color": "lightyellow"
    },
    {
        "key": 2,
        "text": "Requerimento",
        "color": "orange"
    },
    {
        "key": 3,
        "text": "Rua dos Feijões",
        "color": "pink"
    }
]
````
MultiArrow Tree 2
```
[
    {
        "from": 1,
        "to": 2,
        "color": "red"
    },
    {
        "from": 1,
        "to": 3,
        "color": "red"
    }
]
```
Entity Relation 1
```
[
    {
        "key": "Documento",
        "visibility": true,
        "location": {
            "x": 300,
            "y": 250
        },
        "items": [
            {
                "name": "doc_id",
                "iskey": true,
                "figure": "Decision",
                "color": "purple"
            },
            {
                "name": "doc_numero",
                "iskey": false,
                "figure": "Hexagon",
                "color": "blue"
            }
        ],
        "inheriteditems": [
            {
                "name": "dt_id",
                "iskey": true,
                "figure": "Decision",
                "color": "purple"
            },
            {
                "name": "dt_descricao",
                "iskey": false,
                "figure": "Hexagon",
                "color": "blue"
            }
        ]
    },
    {
        "key": "Tipo de Documento",
        "visibility": true,
        "location": {
            "x": 300,
            "y": 30
        },
        "items": [
            {
                "name": "dt_id",
                "iskey": true,
                "figure": "Decision",
                "color": "purple"
            },
            {
                "name": "dt_descricao",
                "iskey": false,
                "figure": "Hexagon",
                "color": "blue"
            }
        ]
    }
]
```
Entity Relation 2
```
{
    "from": "Documento",
    "to": "Tipo de Documento",
    "text": "0..N",
    "toText": "1"
}
```




