# Switch Button

HTML, CSS and jQuery template for switch button

## HTML
```html
<div class="btn-switch">
		<!-- button2 class for the active button by default -->
	    <div class="active-switch button2"></div>
	    <button data-btn="button1">
	        <strong>Button 1</strong><br>
	        <small>Button 1	description</small>
	    </button>
	    <button data-btn="button2">
	        <strong>Button 2</strong><br>
	        <small>Button 2	description</small>
	    </button>
	    
	</div>
```
## CSS
```css
/* The switch - the box around the slider */
.btn-switch {
  background-color: #e1dede;
  border-radius: 5rem;
  width: 300px;
  height: 64px;
  position: relative;
}
/* button style */
.btn-switch button {
  float: left;
  width: 150px;
  border:none;
  padding:1rem;
  color: #7b7b7b;
  background: transparent;
  border-radius: 5rem;
  position: relative;
}

/*Button switch animation*/
.btn-switch .active-switch.button2 {
  transition: all 0.2s ease-in-out;
  border-radius: 5rem;
  width: 50%;
  border: 1px solid #66cccc;
  background-color: #fff;
  height: 62px;
  position: absolute;
  top: 0;
  -webkit-transform: translateX(100%);
  -khtml-transform: translateX(100%);
  -moz-transform: translateX(100%);
  -ms-transform: translateX(100%);
  -o-transform: translateX(100%);
  transform: translateX(100%);
}
.btn-switch .active-switch.button1 {
  transition: all 0.2s ease-in-out;
  border-radius: 5rem;
  width: 50%;
  border: 1px solid #66cccc;
  background-color: #fff;
  height: 62px;
  position: absolute;
  top: 0;
  -webkit-transform: translateX(0%);
  -khtml-transform: translateX(0%);
  -moz-transform: translateX(0%);
  -ms-transform: translateX(0%);
  -o-transform: translateX(0%);
  transform: translateX(0%);
}
```

##jQuery/JavaScript
```javascript
/**
 * Button click event
 */
$(document).on('click','.btn-switch button', function(e){
    e.preventDefault();
    let btn = $(this).data('btn');
    $('.active-switch').removeClass('button1 button2').addClass(btn);
});
```

# eXWebDev

![](https://avatars.githubusercontent.com/u/27113334?s=400&u=52924d8cb1f9f6f28d7a5fe67c29f258f2e358a2&v=4)

