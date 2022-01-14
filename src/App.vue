<template>
  <v-container>

    <v-row>
      <v-col cols="12" lg="6" md="" sm="">
        <v-data-table
          :headers="tableHeaders"
          :items="itemsWithIndex"
          hide-default-footer
          
        >
        </v-data-table>
      </v-col>


    </v-row>
  </v-container>
</template>
<script>

export default {
  data() {
    return {

   
      tableHeaders: [
  
        {
          text: "S.NO",
          align: "start",
          sortable: false,
          value: 'index'
        },
        {
          text: "Name",
          align: "start",
          sortable: false,
          value: "serialNumber",
        },
        
        {
          text: "Calories",
          align: "start",
          sortable: false,
          value: "Number",
        },
        
      ],
      items: [
        {
          serialNumber: "Frozen Yogurt",
          Number: 150,
          align: "start",

          
        },
        {
          serialNumber: "Frozen Yogurt",
          Number: 200,
          align: "start",
         
        },
        {
          serialNumber: "Frozen Yogurt",
          Number: 159,
          align: "start",

        },
      ],
    };
  },

  computed: {
    itemsWithIndex() {
      return this.items.map(
        (items, index) => ({
          ...items,
          index: index + 1
        }))
    }
  },

};
</script>

<style scoped>

</style>
