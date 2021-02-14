<template>
  <b-container>
    <b-button @click="filter">toggle</b-button>
    <create-modal @create-emit='abc'/>
    <b-table striped hover :items="dummy_items"></b-table>
  </b-container>
</template>

<script>
import CreateModal from '@/components/widget/CreateModal'
export default {
  components: { CreateModal },
  data() {
    return {
      dummy_items: [
        {
          age: 40,
          toggle: false,
          first_name: "Dickerson",
          last_name: "Macdonald"
        },
        { age: 21, toggle: false, first_name: "Larsen", last_name: "Shaw" },
        { age: 89, toggle: true, first_name: "Geneva", last_name: "Wilson" },
        { age: 38, toggle: false, first_name: "Jami", last_name: "Carney" }
      ],
      isToggle: false,
      items:[
                  {
          age: 40,
          toggle: false,
          first_name: "Dickerson",
          last_name: "Macdonald"
        },
        { age: 21, toggle: false, first_name: "Larsen", last_name: "Shaw" },
        { age: 89, toggle: true, first_name: "Geneva", last_name: "Wilson" },
        { age: 38, toggle: false, first_name: "Jami", last_name: "Carney" }
      ]
    };
  },
  methods: {
    filter() {
        console.log("a");
      this.isToggle = !this.isToggle;
      return (this.dummy_items = this.items.filter(
        item => item.toggle === this.isToggle
      ));
    },
    abc(form){
        
        alert(JSON.stringify(form))
        this.dummy_items.push({ age: 21, toggle: false, first_name: "Larsen", last_name: "Shaw" })
    }
  },
};
</script>
