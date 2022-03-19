<template>


  <div class ="menu">
    <a>Home</a>
    <a>Products</a>
    <a>About</a>
    <a v-for="작명 in 3" :key="작명">Home2</a>
    <a v-for="menu in menus" :key="menu">{{menu}}</a>
    // 가장 일반적
    <a v-for="(a,i) in menus" :key="i">{{a}}</a>
  </div>
  <div>
    logo
    <h4 class="red" :style=sty>{{ products[0] }}</h4>
    <p>{{ price1 }} 만원 </p>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p> {{ price2 }} 만원 </p>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p> {{ price2 }} 만원 </p>
  </div>
  <div v-for="(a,i) in products" :key="a">
    <h4>{{ a }}</h4>
    <p> {{ moneys[i] }}</p>
    <button @click="increase">허위매물 신고</button> <span> 신고수 : {{신고수[i]}} </span>
  </div>
</template>

<script>

document.getElementById

export default {
  name: 'App',
  data(){
    return {
      price1 : 620,
      price2 : 70,
      logo : 'one Room',
      sty : 'color : skyblue',
      products : ['yeoksam','gwangjin','mapo'],
      menus : ['hooome','shop','news'],
      moneys : ['60만원', '70만원','80만원' ],
      신고수 : [0,0,0]
    }
  },

  methods : {
    increase(){
      this.신고수 += 1;
    }
  },

  components: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
  }
.menu a {
  color: white;
  padding: 10px;
}

</style>
