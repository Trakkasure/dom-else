# What is this strange thing?
This is a Polymer Element providing the missing ELSE portion for the "DOM-IF" template.

## Install
```bash
bower install --save dom-else
```

## Example

```html
    <button onclick="clicked()">Toggle</button>
    <template id="domIf" is="dom-if" if>
      <div>1</div>
      <div>2</div>
      <div>3</div>
      Stuff
      <div>4</div>
      <template is="dom-else">
        <div>e1</div>
        <div>e2</div>
	More stuff
        <div>e3</div>
      </template>
    </template>

    <script>
       function clicked() {
           var t=document.querySelector('#domIf');
           t.set('if',!t.if);
       }
    </script>
```

## Basics
The dom-else element currently needs to be a direct child of the dom-if element.
