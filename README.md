# SubSect — An Interactive Itemset Visualization 

SubSect is an interactive visualization for itemsets and association rules. This repository only includes the source code, for a detailed description of the visualization, refer to:
> De Pauw, Joey, Sandy Moens, and Bart Goethals. "SubSect—An Interactive Itemset Visualization."

Find a running example here: <https://joeydp.github.io/SubSect/>.

### Usage

Since this is only a way to visualize itemsets and association rules, not mine them, it is best used in conjunction with a data mining tool. It has already been integrated in [SNIPER](https://bitbucket.org/sandymoens/sniper/), a web-based tool for pattern mining with a main focus on facilitating data exploration.

Otherwise you can load the `circular.css` and `circular.js` files and call the visualization manually as follows:
```javascript
var body = d3.select("body");

circular(
  body,
  {
      "items": [
          {"id": "A", "label": "Apples", "icon": "plane"},
          {"id": "B", "label": "Pears", "icon": "bicycle"},
          {"id": "C", "label": "Oranges", "icon": "car"}
      ],
      "itemsets": [
          {
              "items": ["C"],
              "support": 0.4830097087378641
          },
          {
              "items": ["A", "B"],
              "support": 0.5339805825242718
          },
          {
              "items": ["C", "A"],
              "support": 0.4029126213592233
          },
          {
              "items": ["B"],
              "support": 0.6650485436893204
          },
          {
              "items": ["C", "A", "B"],
              "support": 0.25
          },
          {
              "items": ["C", "B"],
              "support": 0.30339805825242716
          },
          {
              "items": ["A"],
              "support": 0.8009708737864077
          }
      ]
  },
  800,        // size
  true       // use context circle
);
```
The full example can be seen [here](example.html).
