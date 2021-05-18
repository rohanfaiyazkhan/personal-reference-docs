# Window.location

## Getting pathname (without search params)

```

// URL: www.site.com/page?param=1  

let pathname = window.pathname // www.site.com/page

```

## Getting search params

```
// URL: www.site.com/page?param=1  

let searchParamsString = window.location.search // page=1  
let searchParams = new URLSearchParams(searchParamsString)
