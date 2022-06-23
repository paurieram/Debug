# Debug

## JS

### Ajax

empty response
> 
```js
$.ajax({},
error: function(jqXHR, textStatus, errorThrown){
    alert(errorThrown);
});
```

## PHP

### Laravel


> empty querry
> 
```php
return categories::where('state', '0')->get();
```