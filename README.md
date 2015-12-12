# CheeseJS
CheeseJS is a javascript library to generate Japanese map

## Usage
```javascript
		var japan = new Cheese("#canvas");
		for (var i = 1; i <= 47; i++) {
			japan.setColor(i, '#' + (Math.random() * 0xFFFFFF << 0).toString(16));
		}
		japan.setColor("kyoto", "#000000");
		japan.setColor(["fukuoka", 47, "kyoto"], "#000000");

		japan.hover(["kagoshima", "hiroshima"]);
		japan.click(["tokyo", "kanagawa"], function(where) {
			console.log("You clicked " + where);
		});
```

### Method
* Cheese(String, Object)
* Cheese.setColor(String/Number/Array, String)
* Cheese.hover(String/Number/Array)
* Cheese.unhover(String/Number/Array)
* Cheese.click(String/Number/Array, callback)
* Cheese.unclick(String/Number/Array);

## Attributions
CheeseJS uses the map data from [this site](http://aoki2.si.gunma-u.ac.jp/R/map.html)

## TODO
* README整理
* 未実装の部分の実装
* 構造最適化
