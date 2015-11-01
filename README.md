# Polymer Guide
![Polymer Logo][polymer-logo]

## Table of Contents
1. [Basics](#Basics)
1. [Contributors](#contributors)
1. [License](#license)

##Basics
- [1.1] (#1.1) <a name="1.1"></a> **Attributes**: Default and Custom attributes.

```HTML
	<hello-world name="Bamieh"></hello-world> <!-- Hello Bamieh -->
	<hello-world></hello-world> <!-- Hello World -->
```

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

##Contributors

##License

[polymer-logo]: http://www.bacancytechnology.com/wp-content/themes/twentyfourteen/images/polymerjs.png "Polymer Logo"