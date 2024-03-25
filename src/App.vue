<template>
<div class="app">
  <Header title="the Anime Quoter"></Header>
<Quote :quote="quote"></Quote>

  <button  @click="getQuote">generate</button>
  <!-- {{this.quotes}} -->
</div>

</template>

<script>
import Header from "./components/headerHeader.vue";
import Quote from "./components/quote-Quote.vue";
export default {
  name: 'App',
  components: {
    Header,
    Quote
  },
 data(){
  return{
    quote:{
      content:'content goes here',
      anime:'naruto',
      character:'madara'
    },
    quotes:[]
  }
 },
 methods:{
  async getQuote(){
    
    if (this.quote.content) {
      this.quotes=[...this.quotes,this.quote]
    }
    const  data= await (fetch('https://jsonplaceholder.typicode.com/todos/1')
    .then(response => response.json())
    .then(quote => console.log(quote)))

    this.quote={
      content:data.content,
      anime:data.anime,
      character:data.character
    }
    

  }
 },
 created(){
  this.getQuote()
 }
}
</script>

<style lang='scss'>
:root{
  --primary: #D81E5B
  --secondary: #8A4FFF
  --tertiary:#32CBFF
  --dark:#131A26
  --light:#EEE
  --gray:#848484
}

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

button{
  display: flex;
  justify-content: center;
  height: 50px;
  align-items: center;
  cursor: pointer;
  font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  font-size: 20px;
  color: aliceblue;
  border-radius: 22px;
   padding: 0px 32px;
  margin: 64px auto;
  border: none;
  outline: none;
  background-color: rgb(234, 120, 120);
  &:hover{
    background-color: rgb(236, 64, 64);
  }
}
</style>
