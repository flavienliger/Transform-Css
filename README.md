Transform-Css
=============

Transform Css to Object, with manipulation of translate/ scale/ rotate.
No deps required.


- for use this library, you need add Css to $.css or el.style. If you add in css file, el.style return matrice element.

- to use :
```
new Transform(obj);
```

- input avalaible :
```
var obj = document.getElementById('test'); // dom classic
var obj = $('#test'); // jQuery
var obj = { translateX: '10px', translateY: 10 }; // object
var obj = 'transform: translateX(10px) translateY(10px)'; // string
```

- method :
```
var transfo = new Transform({ translateX: 10, rotateZ: 10 });

transfo.get(); // return { translateX: 10, rotateZ: 10 }
transfo.getCssFormat(); // return 'translateX(10px) rotateZ(10deg)'

transfo.add({ translateX: 10 }); // add to previous transfo, translateX: 20
transfo.add( 'translateX(10px)' );

transfo.set(name, val, add);
transfo.set('translateX', 10, true); // translateX: 20

transfo.translate(x, y, z); // add X or Y or Z

transfo.rotate(x, y, z); // rotate to X Y Z
transfo.rotate(z); // rotate to Z only

transfo.scale(x, y); // scale X and Y
transfo.scale(x); // ratio 1 scale(x, x)
```

- default unit are PX and DEG