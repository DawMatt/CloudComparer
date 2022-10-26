# TODO

## Automate yaml to JSON conversion

## Automate Azure data extraction

Extract all services supported by Azure

```jmespath
services[? length(service[? azure[0].name != null].azure | [][]) > to_number('0')].{
    "category": category ,
    "categoryurl": categoryurl ,
    "subcategory": subcategory ,
    "subcategoryurl": subcategoryurl ,
    "service": service[? azure[0].name != null].azure | [][]
}
```

Extract all service categories supported by Azure

```jmespath
services[? length(service[? azure[0].name != null].azure | [][]) > to_number('0')].{
    "category": category ,
    "categoryurl": categoryurl ,
    "subcategory": subcategory ,
    "subcategoryurl": subcategoryurl,
    "count": length(service[? azure[0].name != null].azure | [][])
}
```
