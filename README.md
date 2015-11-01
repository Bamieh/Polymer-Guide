# Polymer Guide
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

**[⬆ back to top](#table-of-contents)**

##References
[leveluptuts polymer tutorial](http://leveluptuts.com/tutorials/polymer-tutorials/)

##Contributors
**[⬆ back to top](#table-of-contents)**

##License
**[⬆ back to top](#table-of-contents)**

[polymer-logo]: http://www.bacancytechnology.com/wp-content/themes/twentyfourteen/images/polymerjs.png "Polymer Logo"