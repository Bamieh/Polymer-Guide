javascript is not loose, but it has implicit coercion thats why you can easily make a Boolean and set it as a string later on(implicit coercion happens).
Polymer asks you to define the type for its attribute deserialisation. Here is a brief explanation:


## type: String
it will deserialize camel-case:
```
userName: String
<my-component use-name="ahmad"></...
```
Deserialization occurs both at create time, and at runtime (for example, when the attribute is changed using setAttribute). However, it is encouraged that attributes only be used for configuring properties in static markup, and instead that properties are set directly for changes at runtime.

## type: Boolean,
Boolean properties are set based on the presence of the attribute: if the attribute exists at all, the property is set to true, regardless of the attribute value. If the attribute is absent, the property gets its default value.

## type: Object or Array
you can pass an object or array in JSON format:
```
<my-element book='{ "title": "Persuasion", "author": "Austen" }'></my-element>
<!-- Note that JSON requires double quotes, as shown above. -->
```

### A note worth mentioning for setting value to property:
When initializing a property to an object or array value, use a function to ensure that each element gets its own copy of the value, rather than having an object or array shared across all instances of the element.
If you provide a function, Polymer calls the function once per element instance.

```
data: {
      type: Object,
      notify: true,
      value: function() { return {}; }
}
```


source*: https://www.polymer-project.org/1.0/docs/devguide/properties.html#attribute-deserialization