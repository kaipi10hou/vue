<template>
  <div class="home">
    <div>대화명을 입력해 주세요!</div>
    <!-- <input type="text" v-model="usernick"> -->
    <input type="text" @keydown.enter="submit" @input="changedNick" class="" :class="usernick =='김의석'?'a':'b'">
    <button @click="submit">입장</button>
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
    
  },
  data(){
    return{
      usernick:"",
    }
  },
  watch:{
    'usernick':function(value){
      console.log(value);
    }
  },
  methods:{
    changedNick(e){
      this.usernick = e.target.value;
    },
    submit(){
      console.log("submit");
    }
  }
}
</script>
