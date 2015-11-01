# Polymer Guide
*v0.01*
![Polymer Logo][polymer-logo]

## Table of Contents
1. [Basics](#basics)
1. [References](#references)
1. [Contributors](#contributors)
1. [License](#license)

##Basics
- [1.1](#1.1) <a name="1.1"></a> **Styling**: Overriding Styles.

- [1.2](#1.2) <a name="1.2"></a> **Attributes**: Default and Custom attributes.

```HTML
<link rel="import" href="../bower_components/polymer/polymer.html">
<polymer-element name="hello-world" attributes="name">
	<template>
	<style>
		h1 {
			text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
		}
	</style>
		<h1>Hello {{name}}</h1>
	</template>
	<script>
		Polymer({
			name: 'World'
		})
	</script>
</polymer-element>
```

```HTML
<hello-world name="Bamieh"></hello-world> <!-- Hello Bamieh -->
<hello-world></hello-world> <!-- Hello World -->
```
- [1.3](#1.3) <a name="1.3"></a> **Itteration**

```HTML
<link rel="import" href="../bower_components/polymer/polymer.html">
<polymer-element name="hello-world" attributes="name">
	<template>
	<ul>
		<template repeat="{{item in names}}">
			<li>Hello {{item.name}}</li>
		</template>
	</ul>
	</template>
	<script>
		Polymer({
			ready:function() {
				this.names = [
					{ name: 'World'},
					{ name: 'Bamieh'},
					{ name: 'Ahmad'}
				]
			}
		})
	</script>
</polymer-element>
```
- [1.4](#1.4) <a name="1.4"></a> **Data Binding**

```HTML
<link rel="import" href="../bower_components/polymer/polymer.html">
<polymer-element name="hello-world" attributes="name">
	<template>
	<h1>Hello {{name}}</h1>
	<input type="text" value="{{name}}">
	</template>
	<script>
		Polymer({
			ready:function() {
				this.name = 'Bamieh'
			}
		})
	</script>
</polymer-element>
```

- [1.5](#1.5) <a name="1.5"></a> **Polymer Data Binding Vs Angular Data Binding**



**[⬆ back to top](#table-of-contents)**

##References
1. [The Polymer Summit 2015](https://www.youtube.com/watch?v=ZDjiUmx51y8&list=PLNYkxOF6rcICdISJclfQhj2S8QZGjXV8J&index=3)
2. [LEVELup tuts](http://leveluptuts.com/tutorials/polymer-tutorials/){:target="_blank"}

##Contributors

- [View Contributors](https://github.com/Bamieh/Polymer-Guide/graphs/contributors)

**[⬆ back to top](#table-of-contents)**

##License

The MIT License (MIT)

Copyright (c) 2015 Ahmad Bamieh

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

**[⬆ back to top](#table-of-contents)**

[polymer-logo]: http://www.bacancytechnology.com/wp-content/themes/twentyfourteen/images/polymerjs.png "Polymer Logo"