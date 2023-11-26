# Http Foxes (Front)
A simple project to document and demonstrate the use of an API

![image](https://github.com/SamuelsonPajeu/http-foxes-front/assets/79151331/abc8d569-715c-4f71-94c7-076da25cdf1e)

------------------------------------------------------------------------------------------
## Install
A simple .html file, just open it and you're ready to go.

## Usage
- ENDPOINT: https://http-foxes-api.onrender.com/foxes

#### Listing existing foxes as a JSON array

<details>
 <summary><code>GET</code> <code><b>/</b></code> <code>(gets all foxes in the DB)</code></summary>

##### Parameters

> None

##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `application/json;charset=UTF-8`        |  JSON array                                                    |

##### Example cURL

> ```javascript
>  curl -X GET "https://http-foxes-api.onrender.com/foxes" -H "Content-Type: application/json" -H "accept: */*"
> ```
</details>

<details>
  <summary><code>GET</code> <code><b>/code/{numeric_id}</b></code> <code>(Get by HTTP Status Code {numeric_id})</code></summary>

##### Parameters

> | name              |  type     | data type      | description                         |
> |-------------------|-----------|----------------|-------------------------------------|
> | `numeric_id` |  required | int ($int64)   | The specific http status numeric id        |

##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `application/json`        | JSON array        |
> | `404`         | `text/html;charset=utf-8`                | Fox not found                          |
> | `400 `         | `text/html;charset=utf-8`         | Invalid fox code                                                                |

##### Example cURL

> ```javascript
>  curl -X GET "https://http-foxes-api.onrender.com/foxes/code/100" -H "Content-Type: application/json" -H "accept: */*"
> ```

</details>

<details>
  <summary><code>GET</code> <code><b>/description/{string}</b></code> <code>(Search by HTTP Status description)</code></summary>

##### Parameters

> | name              |  type     | data type      | description                         |
> |-------------------|-----------|----------------|-------------------------------------|
> | `string` |  required | string | A word or prahse inside the HTTP description |

##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `application/json`        | JSON array        |
> | `404`         | `text/html;charset=utf-8`                | Fox not found                          |

##### Example cURL

> ```javascript
>  curl -X GET "https://http-foxes-api.onrender.com/foxes/description/Not" -H "Content-Type: application/json" -H "accept: */*"
> ```

</details>

------------------------------------------------------------------------------------------
## Adding a site
You can contribute by filling out the following form: https://forms.gle/296T7PwnNVwtjjmy9

These 2 properties are required:
```
{
   code*,
   image*
},
```

------------------------------------------------------------------------------------------
## Contributors

Thanks go to these wonderful people:
<table>
    <tr>
        <td align="center"><a href="https://github.com/HenriqueGomez"><img src="https://avatars.githubusercontent.com/u/11247187?v=4" width="100px;" alt=""/><br /><sub><b>Henrique Gomez</b></sub></a><br/>
        <a href="#" title="Js and CSS front-end">💻</a>
        </td>
        <td align="center"><a href="https://github.com/Felipejsr"><img src="https://avatars.githubusercontent.com/u/32332877?v=4" width="100px;" alt=""/><br /><sub><b>Felipe Rodrigues</b></sub></a><br/>
        <a href="#" title="Foxes: 101,203,204,205">🦊</a>
        </td>
    </tr>
</table>
