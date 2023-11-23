REST Countries
=======

Get information about countries via a RESTful API https://restcountries.eu

API Endpoints
=======

Below are described the REST endpoints available that you can use to search for countries

All
---------------

``` html
https://restcountries.eu/rest/v2/all
```

Name
---------------

Search by country name. It can be the native name or partial name

``` javascript
https://restcountries.eu/rest/v2/name/{name}
```

``` html
https://restcountries.eu/rest/v2/name/eesti
```

``` html
https://restcountries.eu/rest/v2/name/united
```

Full Name
---------------

Search by country full name

``` javascript
https://restcountries.eu/rest/v2/name/{name}?fullText=true
```

``` html
https://restcountries.eu/rest/v2/name/aruba?fullText=true
```

Code
---------------

Search by ISO 3166-1 2-letter or 3-letter country code

``` javascript
https://restcountries.eu/rest/v2/alpha/{code}
```

``` html
https://restcountries.eu/rest/v2/alpha/co
```

``` html
https://restcountries.eu/rest/v2/alpha/col
```

List of codes
---------------

Search by list of ISO 3166-1 2-letter or 3-letter country codes

``` javascript
https://restcountries.eu/rest/v2/alpha?codes={code};{code};{code}
```

``` html
https://restcountries.eu/rest/v2/alpha?codes=col;no;ee
```

Currency
---------------

Search by ISO 4217 currency code

``` javascript
https://restcountries.eu/rest/v2/currency/{currency}
```
``` html
https://restcountries.eu/rest/v2/currency/cop
```

Language
---------------

Search by ISO 639-1 language code

``` javascript
https://restcountries.eu/rest/v2/lang/{et}
```
``` html
https://restcountries.eu/rest/v2/lang/es
```

Capital city
---------------

Search by capital city

``` javascript
https://restcountries.eu/rest/v2/capital/{capital}
```
``` html
https://restcountries.eu/rest/v2/capital/tallinn
```

Calling code
---------------

Search by calling code

``` javascript
https://restcountries.eu/rest/v2/callingcode/{callingcode}
```
``` html
https://restcountries.eu/rest/v2/callingcode/372
```

Region
---------------

Search by region: Africa, Americas, Asia, Europe, Oceania

``` javascript
https://restcountries.eu/rest/v2/region/{region}
```
``` html
https://restcountries.eu/rest/v2/region/europe
```

Regional Bloc
---------------

Search by regional bloc:

- EU (European Union)
- EFTA (European Free Trade Association)
- CARICOM (Caribbean Community)
- PA (Pacific Alliance)
- AU (African Union)
- USAN (Union of South American Nations)
- EEU (Eurasian Economic Union)
- AL (Arab League)
- ASEAN (Association of Southeast Asian Nations)
- CAIS (Central American Integration System)
- CEFTA (Central European Free Trade Agreement)
- NAFTA (North American Free Trade Agreement)
- SAARC (South Asian Association for Regional Cooperation)

``` javascript
https://restcountries.eu/rest/v2/regionalbloc/{regionalbloc}
```
``` html
https://restcountries.eu/rest/v2/regionalbloc/eu
```

Response Example
---------------

``` html
https://restcountries.eu/rest/v2/alpha/col
```

``` json
[[{
	"name": "Colombia",
	"topLevelDomain": [".co"],
	"alpha2Code": "CO",
	"alpha3Code": "COL",
	"callingCodes": ["57"],
	"capital": "Bogotá",
	"altSpellings": ["CO", "Republic of Colombia", "República de Colombia"],
	"region": "Americas",
	"subregion": "South America",
	"population": 48759958,
	"latlng": [4.0, -72.0],
	"demonym": "Colombian",
	"area": 1141748.0,
	"gini": 55.9,
	"timezones": ["UTC-05:00"],
	"borders": ["BRA", "ECU", "PAN", "PER", "VEN"],
	"nativeName": "Colombia",
	"numericCode": "170",
	"currencies": [{
		"code": "COP",
		"name": "Colombian peso",
		"symbol": "$"
	}],
	"languages": [{
		"iso639_1": "es",
		"iso639_2": "spa",
		"name": "Spanish",
		"nativeName": "Español"
	}],
	"translations": {
		"de": "Kolumbien",
		"es": "Colombia",
		"fr": "Colombie",
		"ja": "コロンビア",
		"it": "Colombia",
		"br": "Colômbia",
		"pt": "Colômbia"
	},
	"flag": "https://restcountries.eu/data/col.svg",
	"regionalBlocs": [{
		"acronym": "PA",
		"name": "Pacific Alliance",
		"otherAcronyms": [],
		"otherNames": ["Alianza del Pacífico"]
	}, {
		"acronym": "USAN",
		"name": "Union of South American Nations",
		"otherAcronyms": ["UNASUR", "UNASUL", "UZAN"],
		"otherNames": ["Unión de Naciones Suramericanas", "União de Nações Sul-Americanas", "Unie van Zuid-Amerikaanse Naties", "South American Union"]
	}]
}]
```

Filter Response
=======

You can filter the output of your request to include only the specified fields.

``` javascript
https://restcountries.eu/rest/v2/{service}?fields={field};{field};{field}
```
``` html
https://restcountries.eu/rest/v2/all?fields=name;capital;currencies
```

Sources
=======
* [@mledoze]
* [List of countries]
* [Languages]
* [Currencies]
* [Area]

Similar projects
=======
* [Countries of the world]
* [REST Countries Node.js]
* [REST Countries Ruby]
* [REST Countries Go]
* [REST Countries Python]
* [world-currencies]
* [REST Countries C#](https://github.com/egbakou/RESTCountries.NET)

License
=======
[Mozilla Public License] MPL 2.0

[dist]: https://github.com/fayder/restcountries/
