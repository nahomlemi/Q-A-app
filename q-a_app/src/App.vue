<template>
  <div class = "container">
    <h1>Q&A App</h1>
    <label>Question - {{number+1}}</label>
    <p>{{questions[number].q}}</p>
    <p>{{questions[number].answer}}</p>
    <div class = "buttons">
      <button @click = "back">back</button>
      <button @click = "show" id="show">show answer</button>
      <button @click = "next">next</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  },
  data(){
    return{
      number:0,
      questions:[
        {q:"who was the first president of the United State?",answer:"George Washington",A:"Abraham Lincoln",B:"George Washington",C:"Franklin D. Roosevelt",D:"Theodore Roosevelt"},
        {q:"which currency is used in Spain?", answer:"Euro", A:"USD",B:"Franc",C:"GBP",D:"Euro"},
        {q:"How many stars are on the flag of the United States?", answer:50, A:52, B:13, C:50, D:48},
        {q:"How many Harry Potter books are there?",answer:7, A:7, B:8, C:9, D:10},
        {q:"In which city can you find the Colosseum?", answer:"Rome",A:"Madrid", B:"Lisbon", C:"Rome", D:"Malta"},
        {q:"What was Prince Phillip title?", answer:"Duke of Edinburgh", A:"Duke of Edinburgh",B:"Prince of Wales",C:"Earl of Wessex",D:"Duke of York"},
        {q:"Who wrote Charlie and the Chocolate Factor?", answer:"Roald Dahl", A:"George Orwell", B:"JK Rowling",C:"JRR Tolkien",D:"Ronald Dahl"}
      ]
    }
  },
  methods:{
    back(){
      if (this.number>0){
        this.number -=1 
      }
    },
    show(){
    },
    next(){
      if(this.number<this.questions.length-1){
      this.number +=1
      }
    }
  }
}
</script>

<style>
h1{
  display:flex;
  justify-content:center;
}
.buttons{
  display:flex;
  justify-content:space-between;
  margin-top:40vh;
}
button{
  width:30vw;
  padding:10px 40px;
  border:0;
  border-radius:20px;
}
#show{
  
}
</style>
