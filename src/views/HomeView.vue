<template>
  <div class="렉사이">
    <img src="@/assets/1.png" width= "500">
    <p>렉사이</p>
    승리  <button @click="winup(0)" style="color : red">증가</button>
    <button @click="windown(0)" style="color : blue">감소</button>  {{승리수[0]}}
    패배  <button @click="loseup(0)" style="color : red">증가</button>
    <button @click="losedown(0)" style="color : blue">감소</button>  {{패배수[0]}}
    <p>승률 : {{승리수[0]/(승리수[0]+패배수[0])*100}}</p>
  </div>
  <hr style="border: solid 10px red;">

  <div class="리신">
    <img src="@/assets/2.jpg" width= "500">
    <p>리신</p>
    승리  <button @click="winup(1)" style="color : red">증가</button>
    <button @click="windown(1)" style="color : blue">감소</button>  {{승리수[1]}}
    패배  <button @click="loseup(1)" style="color : red">증가</button>
    <button @click="losedown(1)" style="color : blue">감소</button>  {{패배수[1]}}
    <p>승률 : {{승리수[1]/(승리수[1]+패배수[1])*100}}</p>
  </div>
  <hr style="border: solid 10px red;">

   <div class="엘리스">
    <img src="@/assets/3.png" width= "500">
    <p>엘리스</p>
    승리  <button @click="winup(2)" style="color : red">증가</button>
    <button @click="windown(2)" style="color : blue">감소</button>  {{승리수[2]}}
    패배  <button @click="loseup(2)" style="color : red">증가</button>
    <button @click="losedown(2)" style="color : blue">감소</button>  {{패배수[2]}}
    <p>승률 : {{승리수[2]/(승리수[2]+패배수[2])*100}}</p>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
  components: {
  },
  data () {
    return {
      승리수: [0, 0, 0],
      패배수: [0, 0, 0]
    }
  },
  methods: {
    winup: function (value) {
      this.승리수[value]++
    },
    windown: function (value) {
      this.승리수[value]--
    },
    loseup: function (value) {
      this.패배수[value]++
    },
    losedown: function (value) {
      this.패배수[value]--
    }
  }
}
</script>
<style>

</style>
