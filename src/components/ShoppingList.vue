<style>
.container {
  background-color: aqua;
  width: 40%;
  margin: 20px auto 0px auto;
}

.removed label {
  text-decoration: line-through;
}

ul li {
  list-style-type: none;
}

ul li span {
  margin-left: 5px;
}

.footer {
  font-size: 0.7em;
  margin-top: 20vh;
}
</style>

<template>
  <div class="container">
    <h2>{{ title }}</h2>
    
    <add-item-component v-on:add="addItem"></add-item-component>
    <items-component :items="items"></items-component>

    <div class="footer">
      <hr>
        <change-title-component v-model="title"></change-title-component>
    </div>
   
    
  </div>
</template>
<script>

    import AddItemComponent from './shopping-list/AddItemComponent'
    import ItemsComponent from './shopping-list/ItemsComponent'
    import ChangeTitleComponent from './shopping-list/ChangeTitleComponent'

export default {
  data() {
    return {
      title: "Shopping List!",
      items: [
        { text: "Bananas", checked: true },
        { text: "Apples", checked: false }
      ]
    };
  },
  methods: {
    addItem(text){
      this.items.push({
        text: text,
        checked: false
      })
    }
  },
  components : {
    AddItemComponent,
    ItemsComponent,
    ChangeTitleComponent
  }
};
</script>