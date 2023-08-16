# Arrow Functions

### Syntax

(param1, param2) ⇒ { statements }

(param1, param2) ⇒ expression

(param1, param2) ⇒ { return expression; }

(singleParam) ⇒ { statements }

singleParam ⇒ { statements }

() ⇒ { statements }

() ⇒ expression

() ⇒ { return expression; }

(param1, param2, paramN) ⇒ expression

## Normal Function

var multiply = (x,y) {

return x * y;

}

## Arrow Function

var multiply = (x, y) ⇒ { return x * y };

or

var multiply = (x, y) ⇒ x*y;

### Example:

var materials = [ 'Hydrogen', 'Helium', 'Lithium', 'Berryllium' ];

//Using Normal Function

var materialsLength1 = materials.map(function(material) {

return material.length;

});

//Using Arrow Function

var materialsLength2 = materials.map((material) ⇒ {

return material.length;

});

or,

var materialsLength3 = materials.map((material) ⇒ material.length);

[Code](Arrow%20Functions%20de3d4274323a4cc8b46644b1eb923aa6/Code%2099875fb2183a4bdea425e3cd23fd36e2.md)