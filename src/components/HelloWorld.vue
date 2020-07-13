<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>{{ messages }}</p>
    <span v-bind:title="message">
    鼠标悬停几秒钟查看此处动态绑定的提示信息！
  </span>

  <p v-if="seen">现在你看到我了</p>

  <ol><li v-for="todo in todos" :key="todo.id">
      {{ todo.text }}
    </li>
  </ol>


<p>{{ message }}</p>
  <button v-on:click="reverseMessage">逆转消息</button>

  <p>{{ message }}</p>
  <input v-model="message">







  </div>


</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return{
      messages:'测试字符串内容',
      message: '页面加载于 ' + new Date().toLocaleString(),
      seen:true,
      todos: [
      { text: '学习 JavaScript' },
      { text: '学习 Vue' },
      { text: '整个牛项目' }
    ]
    }
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
