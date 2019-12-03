<template>
  <div id="shittypanel">
    <header>{{ title}}</header>
    <div class="shittylist">
      <input id="inputField" @keypress.13="addtoshittylist"/>
      <button @click="addtoshittylist">Add</button>
      <ul>
        <li v-for="(item, index) in items">
          <button class="delete" @click="deleteItems(index)"><i class="ion-close"></i></button>{{ item.list }}
        </li>
      </ul>
    </div>
  </div>

</template>

<script>
    export default {
      data () {
        return {
          title: 'shitTodo',
          items: [
            {list: 'shit1'},
            {list: 'shit2'},
            {list: 'shit3'},
            {list: 'shi5123'},
            {list: 'suchshitmuchwow'}
          ]
        }
      },
      methods: {
        addtoshittylist: function() {
          var field = document.getElementById('inputField');
          if (field !== '') {
            this.items.push({
              list: field.value
            })
            field.value=''
          }
        },
        deleteItems: function(index) {
          this.items.splice(index, 1);
        }
      },
    }
</script>




