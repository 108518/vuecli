<template>
  <div id="zujian">
    <h1>这里是zujian组件内的文本内容</h1>
    <a> 作者： {{ author }} </a>
    <p>{{ zujianmsg }}</p>

    <!-- `greet` 是在下面定义的方法名 -->
  <button v-on:click="greet">点击弹出提示</button>

  <button v-on:click="say('你好')">显示 你好</button>
  <button v-on:click="say('传递内容')">显示 传递内容</button>

  <input v-model="author" placeholder="请编辑内容">
<p>文本框输入内容是: {{ author }}</p>


<input type="checkbox" id="checkbox" v-model="checked">
<label for="checkbox">{{ checked }}</label>
<br>


  <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
  <label for="jack">Jack</label>
  <input type="checkbox" id="john" value="John" v-model="checkedNames">
  <label for="john">John</label>
  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
  <label for="mike">Mike</label>
  <br>
  <span>Checked names: {{ checkedNames }}</span>
<br>

  <input type="radio" id="one" value="One" v-model="picked">
  <label for="one">One</label>
  <br>
  <input type="radio" id="two" value="Two" v-model="picked">
  <label for="two">Two</label>
  <br>
  <span>Picked: {{ picked }}</span>


  <div id="example-5">
  <select v-model="selected">
    <option disabled value="">请选择</option>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <span>Selected: {{ selected }}</span>
</div>





<select v-model="selectedv">
  <option v-for="option in options" v-bind:value="option.value" :key="option.value">
    {{ option.text }}
  </option>
</select>
<span>Selected: {{ selectedv }}</span>



<div id="example-3">
  <button @click="show = !show">
    Toggle render
  </button>
  <transition
    name="custom-classes-transition"
    enter-active-class="animated tada"
    leave-active-class="animated bounceOutRight"
  >
    <p v-if="show">hello</p>
  </transition>
</div>


  </div>
</template>
 


<script>
export default {
  name: 'zujian',
  props: {
    zujianmsg: String
  },
  data(){
    return{
      author: "组件作者昵称 lfq",
      checked: "显示复选框状态",
      checkedNames: [],
      picked:"",
      selected: '',
      selectedv: 'A',
    options: [
      { text: 'One', value: 'A' },
      { text: 'Two', value: 'B' },
      { text: 'Three', value: 'C' }
      ],
      show: true
    }
  },
  // 在 `methods` 对象中定义方法
  methods: {
    greet: function (event) {
      // `this` 在方法里指向当前 Vue 实例
      alert('Hello ' + this.author + '!')
      // `event` 是原生 DOM 事件
      if (event) {
        alert(event.target.tagName)
      }
    },
    say: function (message) {
      alert(message)
    }
  }
}
</script>
 
<style>
</style>


