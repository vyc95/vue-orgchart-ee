## Features
- For now, just static organization chart

# Installation
```
npm install vyc95/vue-orgchart-ee
```

# Usage
```html
<template>
  <div>
    <organization-chart :datasource="ds"></organization-chart>
  </div>
</template>

<script>
  import Vue from 'vue'
  import OrganizationChart from 'vue-organization-chart'
  import 'vue-organization-chart/dist/orgchart.css'

  export default {
    components: {
      OrganizationChart
    },
    data () {
      return {
        ds: {
          'id': '1',
          'name': 'Lao Lao',
          'title': 'general manager',
          'image': 'https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg',
          'children': [
            { 
              'id': '2', 
              'name': 'Bo Miao', 
              'title': 'department manager',
              'image': 'https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg',
            },
            { 
              'id': '3', 
              'name': 'Su Miao', 
              'title': 'department manager',
              'image': 'https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg',
              'children': [
                { 
                  'id': '4',
                  'name': 'Tie Hua',
                  'title': 'senior engineer',
                  'image': 'https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg', 
                },
                { 
                  'id': '5',
                  'name': 'Hei Hei',
                  'title': 'senior engineer',
                  'image': 'https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg',
                  'children': [
                    { 
                      'id': '6', 
                      'name': 'Pang Pang', 
                      'title': 'engineer',
                      'image': 'https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg', 
                    },
                    { 
                      'id': '7', 
                      'name': 'Xiang Xiang', 
                      'title': 'UE engineer',
                      'image': 'https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg', 
                    }
                  ]
                 }
               ]
             },
            { 
              'id': '8', 
              'name': 'Hong Miao', 
              'title': 'department manager',
              'image': 'https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg', 
            },
            { 
              'id': '9', 
              'name': 'Chun Miao', 
              'title': 'department manager',
              'image': 'https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg', 
            }
          ]
        }
      }
    }
  }
</script>
```

# Attributes
<table>
  <thead>
    <tr><th>Name</th><th>Type</th><th>Required</th><th>Default</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr>
      <td>datasource</td><td>json</td><td>yes</td><td></td><td>datasource usded to build out structure of orgchart. It could be a json object.</td>
    </tr>
    <tr>
      <td>pan</td><td>boolean</td><td>no</td><td>false</td><td>Users could pan the orgchart by mouse drag&drop if they enable this attribute.</td>
    </tr>
    <tr>
      <td>zoom</td><td>boolean</td><td>no</td><td>false</td><td>Users could zoomin/zoomout the orgchart by mouse wheel if they enable this attribute.</td>
    </tr>
    <tr>
      <td>zoomin-limit</td><td>number</td><td>no</td><td>7</td><td>Users are allowed to set a zoom-in limit.</td>
    </tr>
    <tr>
      <td>zoomout-limit</td><td>number</td><td>no</td><td>0.5</td><td>Users are allowed to set a zoom-out limit.</td>
    </tr>
  </tbody>
</table>

# Events
<table>
  <thead>
    <tr><th>Name</th><th>Parameters</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr>
      <td>node-click</td><td>node data</td><td>triggers when user clicks the node.</td>
    </tr>
  </tbody>
</table>

# Scoped Slots
```html
<template slot-scope="{ nodeData }">
  <!-- feel free to customize the internal structure of node -->
</template>
```
