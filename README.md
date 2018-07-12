# \<polymer-two-temp\>


This is another repo to experiment with Polymer, this time with Polymer 2.

## Concepts

* Reusable components
* One-way data binding
* Shared-styles with Bootstrap

## Reusable component template

Below is a snippet of how to create a component in Polymer 2:

```html
<link rel="import" href="../../../bower_components/polymer/polymer-element.html">
<link rel="import" href="../shared-styles.html">

<dom-module id="my-element">
  <template>
    <style include="shared-styles">
      .My-element {}
    </style>
    <div class="My-element"></div>
  </template>
  <script>
    class MyElement extends Polymer.Element {
      static get is() { return 'my-element'; }
      static get properties() { return {} }
    }

    window.customElements.define(MyElement.is, MyElement);
  </script>
</dom-module>
```

Once a component is created it can be used throughout the application.  If different data is used, one-way or two-way data binding can be used.  Below is an example of HTML used within the various feature sections in this repo:

```html
<div class="Collaborate">
  <headline-element headline=[[headline]]></headline-element>
  <div class="container">
    <h3>Congratulations here's your links!</h3>
  </div>
</div>
```

---
