## Paths
### error403
```
GET /errores/403
```

#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|ModelAndView|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json

#### Produces

* */*

#### Tags

* error-controller

### error404
```
GET /errores/404
```

#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|ModelAndView|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json

#### Produces

* */*

#### Tags

* error-controller

### setExtraInformationError
```
POST /exception/error
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|QueryParameter|errorId|errorId|true|string||
|QueryParameter|message|message|true|string||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json

#### Produces

* */*

#### Tags

* base-exception-controller

### getError
```
GET /exception/error
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|QueryParameter|exception|exception|false|string||
|QueryParameter|message|message|false|string||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|object|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json

#### Produces

* */*

#### Tags

* base-exception-controller

### Create a new Foo entity.
```
POST /foos
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|entity|entity|true|Foo||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|201|Created|Foo|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json;charset=UTF-8

#### Produces

* application/json;charset=UTF-8

#### Tags

* foo-controller

### Return a GridWrapper object with a Foo collection.
```
GET /foos
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|QueryParameter|filters|Filters over Foo entity|false|string||
|QueryParameter|fetchs|Fetchs required|false|string||
|QueryParameter|page|Page to show|false|integer (int32)||
|QueryParameter|rows|Records per page|false|integer (int32)||
|QueryParameter|sidx|Order By|false|string||
|QueryParameter|sord|Order mode (ASC or DESC)|false|string||
|QueryParameter|searchField|Search field|false|string||
|QueryParameter|searchOper|Search operator|false|string||
|QueryParameter|searchString|Search data|false|string||
|BodyParameter|dummy|Dummy param for generics discovery|false|Foo||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|Foo|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json

#### Produces

* application/json;charset=UTF-8

#### Tags

* foo-controller

### Multipart + json example
```
POST /foos/file
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|QueryParameter|foo|Entidad|true|string||
|FormDataParameter|file|Archivo|true|file||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|string|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* multipart/form-data

#### Produces

* */*

#### Tags

* foo-controller

### Create a new Bar entity in to Foo's collection.
```
POST /foos/{fooId}/bars
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|fooId|Foo entity Id|true|integer (int32)||
|BodyParameter|entity|Bar entity|true|Bar||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|201|Created|Bar|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json;charset=UTF-8

#### Produces

* application/json;charset=UTF-8

#### Tags

* bar-controller

### Return a GridWrapper object with the Bar collection.
```
GET /foos/{fooId}/bars
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|fooId|Foo entity Id|true|integer (int32)||
|QueryParameter|filters|Filters over Bar entity|false|string||
|QueryParameter|fetchs|Fetchs required|false|string||
|QueryParameter|page|Page to show|false|integer (int32)||
|QueryParameter|rows|Records per page|false|integer (int32)||
|QueryParameter|sidx|Order By|false|string||
|QueryParameter|sord|Order mode (ASC or DESC)|false|string||
|QueryParameter|searchField|Search field|false|string||
|QueryParameter|searchOper|Search operator|false|string||
|QueryParameter|searchString|Search data|false|string||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|Bar|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json

#### Produces

* application/json;charset=UTF-8

#### Tags

* bar-controller

### Delete a Bars entity from de Foo's colleción.
```
DELETE /foos/{fooId}/bars/{id}
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|fooId|Foo entity Id|true|integer (int32)||
|PathParameter|id|Bar entity Id|true|integer (int32)||
|QueryParameter|version|Bar entity version|true|integer (int32)||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|Bar|
|204|No Content|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|


#### Consumes

* application/json

#### Produces

* */*

#### Tags

* bar-controller

### Return a Bar entity by Id 
```
GET /foos/{fooId}/bars/{id}
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|fooId|Foo entity Id|true|integer (int32)||
|PathParameter|id|Bar entity Id|true|integer (int32)||
|QueryParameter|fetchs|Fetchs required|false|string||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|Bar|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json

#### Produces

* application/json;charset=UTF-8

#### Tags

* bar-controller

### Update a Bar entity.
```
PUT /foos/{fooId}/bars/{id}
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|fooId|Foo entity Id|true|integer (int32)||
|BodyParameter|entity|Bar entity|true|Bar||
|PathParameter|id|Bar Id|true|integer (int32)||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|Bar|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json;charset=UTF-8

#### Produces

* application/json;charset=UTF-8

#### Tags

* bar-controller

### Delete a Foo entity.
```
DELETE /foos/{id}
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|id|id|true|integer (int32)||
|QueryParameter|version|version|true|integer (int32)||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|Foo|
|204|No Content|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|


#### Consumes

* application/json

#### Produces

* */*

#### Tags

* foo-controller

### Return a Foo entity by Id 
```
GET /foos/{id}
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|PathParameter|id|Foo entity Id|true|integer (int32)||
|QueryParameter|fetchs|Fetchs required|false|string||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|Foo|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json

#### Produces

* application/json;charset=UTF-8

#### Tags

* foo-controller

### Update a Foo entity.
```
PUT /foos/{id}
```

#### Parameters
|Type|Name|Description|Required|Schema|Default|
|----|----|----|----|----|----|
|BodyParameter|entity|entity|true|Foo||
|PathParameter|id|id|true|integer (int32)||


#### Responses
|HTTP Code|Description|Schema|
|----|----|----|
|200|OK|Foo|
|201|Created|No Content|
|401|Unauthorized|No Content|
|403|Forbidden|No Content|
|404|Not Found|No Content|


#### Consumes

* application/json;charset=UTF-8

#### Produces

* application/json;charset=UTF-8

#### Tags

* foo-controller

