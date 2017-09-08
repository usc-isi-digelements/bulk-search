# bulk-search

A Polymer element that allows multiple searches simultaneously.

### Example

```js
var searchFields = [{
  color: "cyan",
  dateProperties: {},
  facetTransform: transFunc(),
  facets: true,
  field:"knowledge_graph.caliber_gauge.key",
  icon:"maps:local-offer",
  key:"caliber_gauge",
  link:"entity",
  queryField:"knowledge_graph.caliber_gauge.value",
  result:"header",
  search:true,
  sort: {
    sortId:1,
    sortType:"entity"
  },
  styleClass:"entity-cyan",
  title:"Caliber or Gauge",
  titlePlural:"Calibers or Gauges",
  type:"string",
},
{
  color: "pink",
  dateProperties: {},
  facetTransform: transFunc(),
  facets: true,
  field:"knowledge_graph.city.key",
  icon:"maps:place",
  key:"city",
  link:"entity",
  queryField:"knowledge_graph.city.value",
  result:"header",
  search:true,
  sort: {
    sortId:1,
    sortType:"entity"
  },
  styleClass:"entity-pink",
  title:"City",
  titlePlural:"Cities",
  type:"location",
}];
```

```html
<bulk-search
  search-fields="[[searchFields]]"
  parameter-key="[[searchFields.0.key]]"
  search-parameters="{{searchParameters}}"
  process-request="{{processRequest}}">
</bulk-search>
```

### Dependencies

Dependencies are installed using [Bower](http://bower.io/):

    npm install -g bower
    bower install

### Testing

Tests are run using [web-component-tester](https://github.com/Polymer/web-component-tester):

    npm install -g web-component-tester
    wct

### Demonstration & Documentation

Demonstration and documentation are viewed using [polyserve](https://github.com/PolymerLabs/polyserve):

    npm install -g polyserve
    polyserve