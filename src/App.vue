<template>
  <div id="app">

    <div class="header">
      <img src="../img/logo.jpg" style="float:left;max-width:200px;padding:1em;">
    </div>
    <!-- <div class="header"></div> -->

    <div v-if="step == 1">

      <div class="row" style="margin-bottom:2em;">
        <h1>Who is More Qualified?</h1>
        <h3>Select One To Cast Your Vote</h3>
      </div>
      
      <div class="row">
        <div class="col-xs-12 col-sm-6">
          <button @click="alertme()">
          <img src="./img/hilary.png"  class="image-select-blue">
          </button>
        </div>
        
        <div class="col-xs-12 col-sm-6"> 
          <img src="./img/trump.jpg" @click="alertme()" class="image-select-red">
        </div>
      </div>
      <button class="btn btn-lg btn-primary" @click="alertme()">Neither</button>
    </div>

    <div v-if="step == 2">
      <h1>Which Side?</h1>
      <div class="row">
        <div>Donald</div>
        <div class="col-xs-6"><img src="../img/republican.png" @click="alertme()" class="image-select"></div>
        <div class="col-xs-6"> <img src="../img/democrat.png" @click="alertme()" class="image-select"></div>
      </div>
    </div>

    <div v-if="step == 3">
       <div class="container center-block">
      <div class="col-xs-6 center-block">
        <div class="form-area">  
            <form role="form">
            <br style="clear:both">
                        <h3 style="margin-bottom: 25px; text-align: center;">Contat Information</h3>
                <div class="form-group">
                <input type="text" class="form-control" id="name" name="name" placeholder="Name" required>
              </div>
              <div class="form-group">
                <input type="text" class="form-control" id="email" name="email" placeholder="Email" required>
              </div>
              <div class="form-group">
                <input type="text" class="form-control" id="mobile" name="mobile" placeholder="Mobile Number" required>
              </div>
              <div class="form-group">
                <input type="text" class="form-control" id="subject" name="subject" placeholder="Subject" required>
              </div>
                <div class="form-group">
                <textarea class="form-control" type="textarea" id="message" placeholder="Message" maxlength="140" rows="7"></textarea>
                    <span class="help-block"><p id="characterLeft" class="help-block ">You have reached the limit</p></span>                    
                </div>  
            <button type="button" id="submit" name="submit" class="btn btn-primary pull-right" @click="sendData()">See Results</button>
            </form>
        </div>
      </div>
    </div>
    </div>

    <div v-if="step == 4">
      <h1>Results Page</h1>
      <div class="row">
        <div>This may use chart.js to grab data</div>
      </div>
    </div>
   
    <!-- <h1>{{ msg }}</h1>
    <h2>Essential Links</h2> -->
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      step: 1
    }
  },
  methods: { 
    alertme(){
      this.step++;
    },
    sendData(){
      alert("Send Results to DataBase");
      this.step++;
    }
  }
}



</script>

<style scoped>
#app {
  font-family:Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.header{
  height: 50px;
  width:100%;
  -webkit-box-shadow: 0 10px 6px -6px lightgrey;
	-moz-box-shadow: 0 10px 6px -6px lightgrey;
	box-shadow: 0 10px 6px -6px lightgrey;
  margin-bottom: 40px;
}
.centered{
  margin:0 auto;
}
.btn-primary{
  background-color:black;
  font-weight: 1em;
  padding:0.5em 3em;
  font-size:1.7em;
}
.image-select-red{
  border:20px solid #EE385F;;
  border-radius: 5px;
  box-shadow: 2px 2px grey;
}
.image-select-blue{
  border:20px solid #528EFA;
  border-radius: 5px;
  box-shadow: 2px 2px grey;
}
img {
  max-width: 200px;
}

h1, h2 {
  font-weight: 600;
}
h3{
  color:grey;
  margin:0;
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
