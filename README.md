A layer ontop of [wallop](https://github.com/peduarte/wallop) which enables you to use multiple independent wallops in a page, without worrying about renaming the special classes

dependent on wallop JS and wallop CSS files as per normal wallop

###Class

```javascript
JWallop (wallopID, [wallopOptions, usePaginationDots, onChangefunction]
```

#Usage

read and understand the basics of wallop:
the html needs to be set up the same, but give the outer "Wallop" an id.


Html:
```html
<div class="Wallop" id="wallop1">
  ...all the wallops stuff here...
</div>
```

Basic:
```javascript

wallopID = "wallop1";

wallop1 = new JWallop(wallopID);

```

Advanced:
```javascript
var h2OnChange = function(event){
    var selector = "#" + event.detail.wallopEl.getAttribute("id") + " h2";
    TweenMax.fromTo(selector, 2,{color: "#fff"}, {color: "#00f"});
    console.log(selector);
}

wallop1 = new JWallop("wallop1", {}, true, h2OnChange);
```
