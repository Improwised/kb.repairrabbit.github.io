+++
title= "Api doc"
date= 2018-01-18T19:40:04+05:30
description = ""
draft= false
alwaysopen = true
+++

The documentation for phoneworld api is provided here in this file

### Get all stores.

```
Api: api/stores
Type: GET
```
**Response**
```
{
    "success": true,
    "status": 200,
    "data": {
        "stores": [
            {
                "store_id": 2,
                "address": "Ahmedabad",
                "image_url": null
            },
            {
                "store_id": 1,
                "address": "Rajkot",
                "image_url": "http://phoneworld.test/storage/images/store_map_images/138571214-hv.jpg"
            }
        ]
    },
    "message": [],
    "errors": []
}
```
**Response For store dosen't exists**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "Store Not Found",
    "errors": []
}
```

### Get store wise device categories.

```
Api: api/stores/{store_id}/device_categories
Type: GET
```
**Response**
```
{
    "success": true,
    "status": 200,
    "data": {
        "store_device_categories": [
            {
                "device_category_id": 1,
                "device_category": "iPhone",
                "image_url": "http://phoneworld.test/storage/images/device_category_images/138571214-3I.jpg"
            },
            {
                "device_category_id": 15,
                "device_category": "esdfa",
                "image_url": null
            }
        ]
    },
    "message": [],
    "errors": []
}
```
**Response at Validation Failed**
```
{
    "success": false,
    "status": 400,
    "data": [],
    "message": "Error while validating store_id",
    "errors": {
        "store_id": [
            "The store id must be a number."
        ]
    }
}
```
**Response if store dosen't exists**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "Store Not Found",
    "errors": []
}
```
**Response if device category dosen't exists**
```
{
    "success": true,
    "status": 404,
    "data": [],
    "message": "Device Category Not Found",
    "errors": []
}
```

### Get devices according to device category.

```
Api: api/device_categories/{device_category_id}/devices
Type: GET
```
**Response**
```
{
    "success": true,
    "status": 200,
    "data": {
        "store_devices": [
            {
                "device_id": 1,
                "device_name": "iPhone 5",
                "image_url": "http://example.com/storage/images/device_images/device.png"
            },
            {
                "device_id": 2,
                "device_name": "iPhone 5s",
                "image_url": "http://example.com/storage/images/device_images/device1.png"
            }
        ]
    },
    "message": [],
    "errors": []
}
```
**Response at Validation Failed**
```
{
    "success": false,
    "status": 400,
    "data": [],
    "message": "Error while validating device_category_id",
    "errors": {
        "device_category_id": [
            "The device category id must be a number."
        ]
    }
}
```
**Response if device category dosen't exists**
```
{
    "success": true,
    "status": 404,
    "data": [],
    "message": "Device Category Not Found",
    "errors": []
}
```
**Response if device dosen't exists**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "Device Not Found",
    "errors": []
}
```

### Get device products.

```
Api: api/devices/{device_id}/products
Type: GET
```
**Response**
```
{
    "success": true,
    "status": 200,
    "data": {
        "products": [
            {
                "product_id": 1,
                "product_name": "Display (LCD) damage, glass broken black",
                "sku": "A000210",
                "price": "69.90",
                "install_fee": "0",
                "image_url": "http://example.com/storage/images/product_images/product.png",
            }
        ]
    },
    "message": [],
    "errors": []
}
```
**Response at Validation Failed**
```
{
    "success": false,
    "status": 400,
    "data": [],
    "message": "Error while validating device_id",
    "errors": {
        "device_id": [
            "The device id must be a number."
        ]
    }
}
```
**Response if device dosen't exists**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "Device Not Found",
    "errors": []
}
```
**Response if product dosen't exists**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "Product Not Found",
    "errors": []
}
```

### Get available time slotes.

```
Api: api/time-slots
Type: GET
Request Form Data:
{
    "store_id": "40",
    "device_id": "67",
    "appointment_date": "2017-12-13"
}
```
**Response**
```
{
    "success": true,
    "status": 200,
    "data": {
        "timeslots": [
            {
                "1": "10:30 - 11:00",
                "2": "11:00 - 11:30",
                "3": "11:30 - 12:00",
                "4": "12:00 - 12:30"
            }
        ]
    },
    "message": [],
    "errors": []
}
```
**Response at device not found**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "Device Not Found",
    "errors": []
}
```
**Response at store not found**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "Store Not Found",
    "errors": []
}
```
**Response at Validation Failed**
```
{
    "success": false,
    "status": 400,
    "data": [],
    "message": "Error while validating data",
    "errors": {
        "store_id": [
            "The store id must be a number."
        ],
        "device_id": [
            "The device id must be a number."
        ],
        "appointment_date": [
            "The appointment date field is required."
        ]
    }
}
```
**Error Response**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "On the selected day are no times available (anymore)!",
    "errors": []
}
```

### Post appointment data.
```
Api: api/make-appointment
Type: POST
Request Form Data:
{
    "store_id": "40",
    "device_id": "67",
    "appointment_date": "22-11-2017",
    "time_slot": "10:30 - 11:00",
    "defectsSelected[0]": "2",
    "defectsSelected[1]": "3",
    "email": "bhumika++9012@improwised.com",
    "name": "bhumika",
    "phone": "12457862"
}
```
**Response**
```
{
    "success": true,
    "status": 200,
    "data": [],
    "message": "Appointment created successfully",
    "errors": []
}
```
**Response at device not found**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "Device Not Found",
    "errors": []
}
```
**Response at store not found**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "Store Not Found",
    "errors": []
}
```
**Response at product not found**
```
{
    "success": false,
    "status": 404,
    "data": [],
    "message": "Product Not Found",
    "errors": []
}
```
**Error Response**
```
{
    "success": false,
    "status": 400,
    "data": [],
    "message": "Error while validating data",
    "errors": {
        "defectsSelected": [
            "The defects selected field is required."
        ],
        "appointment_date": [
            "The appointment date field is required."
        ],
        "time_slot": [
            "The time slot field is required."
        ],
        "device_id": [
            "The device id field is required."
        ],
        "store_id": [
            "The store id field is required."
        ],
        "email": [
            "The email field is required."
        ],
        "name": [
            "The name field is required."
        ]
    }
}
```
