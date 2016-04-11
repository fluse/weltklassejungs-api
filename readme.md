#Weltklassejungs API

##Location

###request

```javascript
{
    URL: 'api.weltklassejungs.de/v1/location/',
    headers: {
        Authorization: 'Basic {token}'
    },
    query: {
        search: String
    }
    Method: 'GET'
}
```

###response

```javascript
{
    error: null,
    result: [{
        city: String
        country: String
        countryCode: String,
        latitude: Number,
        longitude: Number,
        state: String,
        zip: String
    }, {location}, {location}]
}
```

##Search

###request

```javascript
{
    URL: 'api.weltklassejungs.de/v1/search/',
    headers: {
        Authorization: 'Basic {token}'
    },
    Method: 'POST',
    body: {
        location: String,
        date: Date,
        time: {
            from: Date,
            to: Date
        },
        eventType: String,
        technic: String,
        age: Number,
        misc: String
    }
}
```

###response

**error**

```javascript
{
    error: {
        location: 'isEmpty',
        date: 'isInvalid',
        time: 'isInvalid',
        eventType: 'isEmpty'
    },
    result: null
}
```

**success**
