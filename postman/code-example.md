# Code examples

**Author:** Christine Joyce

## cURL example

Requesting a Pepsi branded soda.

### cURL command

```shell
 curl http://localhost:3000/Pepsi_Sodas
```

### cURL response

```shell
{
    "Name": "Crush",
    "Color": "various",
    "Flavor profile": "fruity",
    "Calories per serving": "160",
    "id": 1
  }
```

## Postman example

Requesting a Coke branded soda.

### Request

**Method**:

```shell
{{base_url}}Coke_Sodas
```

### Postman response

```shell
 {
        "Name": "Sprite",
        "Color": "clear",
        "Flavor profile": "fruity",
        "Calories per serving": "140",
        "id": 1
    }
```
