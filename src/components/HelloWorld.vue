<template>
  <div class="hello">
    {{ hello }}
    {{ 1+1 }}
    {{ "哈哈" }}
    {{ 0>10 ? '对的' : '错的' }}
    <p v-html="hello"></p>
    <p v-text="hello"></p>
    <span v-bind:class="haha1">我要888</span>
    <div>
      <template v-if="show">
        <span>我是if为true看见的</span>
        <a href="www.baidu.com">世界</a>
        <i>灭害</i>
      </template>
      <template v-else>我是if为false看见的</template>
    </div>
    <div class="list">
      <!-- <ul>
        <li v-for="(name,index) in names" v-bind:key="index">{{ name }}-{{ index }}</li>
      </ul>
      <ul>
        <li v-for="item in user">
          <span>{{ item.name }}</span>
          <span>{{ item.age }}</span>
        </li>
      </ul> -->
      <button v-on:click="handlerClick">按钮</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      hello: "<p>Hello Vue</p>",
      haha: "haha",
      haha1: "haha1",
      show:true,
      names:['tom','loch','lina'],
      user:[{
        id:0,
        name:'niadf',
        age:90
      },
      {
        id:1,
        name:'sdfg',
        age:90
      },
      {
        id:2,
        name:'ytri',
        age:90
      }]
    }
  },
  methods:{
    handlerClick(){
      this.show = !this.show
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .haha{
  color:red;
  }
  .haha1{
  color:blue;
  }
</style>
