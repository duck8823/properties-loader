# Properties Loader

The `properties` loader return JSON object.  
  
## Usage
[USING LOADERS](http://webpack.github.io/docs/using-loaders.html)  
```javascript
require("properties!application.properties");
// => returns JSON object of application.properties

require("properties?regex=pattern!application.properties");
// => returns JSON object of application.properties that matched pattern
``` 

## Examples
`application.properties`
```properties
app.foo=Foo
app.bar=Bar
hoge=Hoge
```
  
```javascript
require("properties!application.properties");
// => returns {'app.foo':'Foo','app.bar':'Bar','hoge':'Hoge'}

require("properties?regex=^app\\..*!application.properties");
// => returns {'app.foo':'Foo','app.bar':'Bar'}
```
  
## install
```
npm install --save-dev https://github.com/duck8823/properties-loader.git
```
  
## License
MIT (http://www.opensource.org/licenses/mit-license.php)