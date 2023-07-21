<template>
  <div id="app">
    <org-chart :datasource="ds" @node-click="selectNode">
    </org-chart>
  </div>
</template>

<script>
import OrgChart from "./components/OrganizationChartContainer.vue";

export default {
  name: "app",
  components: {
    OrgChart,
  },
  data() {
    return {
      ds: {
        id: "1",
        name: "Lao Lao",
        title: "general manager",
        image:
          "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
        children: [
          {
            id: "2",
            name: "Bo Miao",
            title: "department manager",
            image:
              "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
          },
          {
            id: "3",
            name: "Su Miao",
            title: "department manager",
            image:
              "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
            children: [
              {
                id: "4",
                name: "Tie Hua",
                title: "senior engineer",
                image:
                  "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
              },
              {
                id: "5",
                name: "Hei Hei",
                title: "senior engineer",
                image:
                  "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
                children: [
                  {
                    id: "6",
                    name: "Pang Pang",
                    title: "engineer",
                    image:
                      "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
                  },
                  {
                    id: "7",
                    name: "Xiang Xiang",
                    title: "UE engineer",
                    image:
                      "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
                    children: [
                      {
                        id: "10",
                        name: "Wei Wei",
                        title: "engineer",
                        image:
                          "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
                        children:[{
                           id: "11",
                        name: "Cheng Cheng",
                        title: "engineer",
                        image:
                          "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
                        }]
                      },
                    ],
                  },
                ],
              },
            ],
          },
          {
            id: "8",
            name: "Hong Miao",
            title: "department manager",
            image:
              "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
          },
          {
            id: "9",
            name: "Chun Miao",
            title: "department manager",
            image:
              "https://upload.wikimedia.org/wikipedia/commons/3/34/Elon_Musk_Royal_Society_%28crop2%29.jpg",
          },
        ],
      },
    };
  },
  methods: {
    selectNode(nodeData) {
      alert("node " + nodeData.name + " is selected");
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
