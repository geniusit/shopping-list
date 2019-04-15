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
    <div class="input-group">
      <input
        v-model="data.newItem"
        @keyup.enter="addItem"
        placeholder="add shopping list item"
        type="text"
        class="form-control"
      >
      <span class="input-group-btn">
        <button @click="addItem" class="btn btn-default" type="button">Add!</button>
      </span>
    </div>

    <ul>
      <li :key="item.title" v-for="item in data.items" :class="{ 'removed': item.checked }">
        <div class="checkbox">
          <label>
            <input type="checkbox" v-model="item.checked">
            {{ item.text }}
          </label>
        </div>
      </li>
    </ul>
    <div class="footer">
      <hr>
      <em>Change the title of your shopping list here</em>
      <input v-model="title">
    </div>
  </div>
</template>


<script>
var data = {
  items: [
    { text: "Bananas", checked: true },
    { text: "Apples", checked: false }
  ],
  title: "My Shopping List",
  newItem: ""
};

export default {
  data() {
    return {
      title: "Shopping List!",
      data: data
    };
  },
  methods: {
    addItem: function() {
      var text;

      text = this.data.newItem.trim();
      if (text) {
        this.data.items.push({
          text: text,
          checked: false
        });
        this.data.newItem = "";
      }
    }
  }
};
</script>