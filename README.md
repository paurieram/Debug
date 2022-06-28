# Debug

## JS

### Ajax

>- #### Empty response
>
>> SyntaxError: JSON.parse: unexpected character at line 1 column 1 of the JSON data
>
>>Not working
>>```js
>>$.ajax({
>>    type: "get",
>>    url: "/url",
>>    dataType: "json",
>>    success: function (response) {
>>    }
>>});
>>```
>
>>Working
>>```js
>>$.ajax({
>>    type: "get",
>>    url: "/url",
>>    dataType: "text",
>>    success: function (response) {
>>    }
>>});
>>```

>- #### View response errors
>> Working
>>```js
>>$.ajax({
>>    type: "get",
>>    url: "/url",
>>    dataType: "text",
>>    success: function (response) {
>>    },
>>    error: function(jqXHR, textStatus, errorThrown){
>>        alert(errorThrown);
>>    }
>>});
>>```

## PHP

### Laravel


>- #### Error: Empty querry
>
>> Argument 1 passed to Symfony\\Component\\HttpFoundation\\Response::setContent() must be of the type string or null, object given, called in C:\\laragon\\www\\Ginepop\\vendor\\laravel\\framework\\src\\Illuminate\\Http\\Response.php on line 72"
>
>>Not working
>>```php
>>return categories::where('state', '0');
>>```
>
>>Working
>>```php
>>return categories::where('state', '0')->get();
>>```

>- #### Error: Not getting relationships
>
>>Not working
>>```php
>>return items::all();
>>```
>
>>Working
>>```php
>>return items::with('imatges')->get();
>>```