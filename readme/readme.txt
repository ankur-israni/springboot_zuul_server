1) URLs
--------------------------
A) Zuul Server URI: http://localhost:8111

B) Zuul Client #1 (inventory) URIs:
-------------------------------------
Swagger: http://localhost:7500/swagger-ui.html

GET request - No request body - No header
-----------------------------------------------------------------------------------------------
URI: http://localhost:7500/services/inventory/all
Request: http://localhost:8111/services/inventory/all
Response:
{
    "items": [
        {
            "id": 1,
            "name": "Laptop",
            "price": 99.67,
            "info": {
                "manufacturedBy": "Apple",
                "description": "16' macbook pro"
            }
        },
        {
            "id": 2,
            "name": "Phone",
            "price": 100.33,
            "info": {
                "manufacturedBy": "Samsung",
                "description": "Android phone"
            }
        },
        {
            "id": 3,
            "name": "Brown Lamp",
            "price": 65.99,
            "info": {
                "manufacturedBy": "Costco",
                "description": "Teak lamp - brown color"
            }
        },
        {
            "id": 4,
            "name": "Alladin's Lamp",
            "price": 67.99,
            "info": {
                "manufacturedBy": "Genie",
                "description": "Magic lamp with 3 wishes"
            }
        }
    ]
}


POST request - Request body required - header required
--------------------------------------------------------------------------------------------------------------
URI: http://localhost:8111/services/inventory/allC
Request:
{
  "password": "ankur",
  "username": "ankur"
}

Response:
{
    "items": [
        {
            "id": 1,
            "name": "Laptop",
            "price": 99.67,
            "info": {
                "manufacturedBy": "Apple",
                "description": "16' macbook pro"
            }
        },
        {
            "id": 2,
            "name": "Phone",
            "price": 100.33,
            "info": {
                "manufacturedBy": "Samsung",
                "description": "Android phone"
            }
        },
        {
            "id": 3,
            "name": "Brown Lamp",
            "price": 65.99,
            "info": {
                "manufacturedBy": "Costco",
                "description": "Teak lamp - brown color"
            }
        },
        {
            "id": 4,
            "name": "Alladin's Lamp",
            "price": 67.99,
            "info": {
                "manufacturedBy": "Genie",
                "description": "Magic lamp with 3 wishes"
            }
        }
    ]
}

C) Zuul Client #1 (employee) URIs:
-------------------------------------
Swagger: http://localhost:7600/swagger-ui.html

GET request - No request body - No header
-----------------------------------------------------------------------------------------------
URI: http://localhost:8111/services/employee/all
Request: http://localhost:8111/services/employee/all
Response:
{
    "employees": [
        {
            "id": 1,
            "firstName": "ankur",
            "lastName": "israni"
        },
        {
            "id": 2,
            "firstName": "barack",
            "lastName": "obama"
        },
        {
            "id": 3,
            "firstName": "ravi",
            "lastName": "shastri"
        },
        {
            "id": 4,
            "firstName": "pamela",
            "lastName": "anderson"
        }
    ]
}



Request body required - header required
--------------------------------------------------------------------------------------------------------------
URI: http://localhost:8111/services/employee/allC
Request:
{
  "password": "ankur",
  "username": "ankur"
}

Response:
{
    "employees": [
        {
            "id": 1,
            "firstName": "ankur",
            "lastName": "israni"
        },
        {
            "id": 2,
            "firstName": "barack",
            "lastName": "obama"
        },
        {
            "id": 3,
            "firstName": "ravi",
            "lastName": "shastri"
        },
        {
            "id": 4,
            "firstName": "pamela",
            "lastName": "anderson"
        }
    ]
}
