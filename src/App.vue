<template>
  <div id="app">

    <div class="header"></div>
    <!-- <div class="header"></div> -->

    

    <div v-if="step == 1">
      <h1>Who is More Qualified?</h1>
      <div class="row">
        <div class="col-xs-6">
          <img src="../img/hilary.png" @click="alertme()" class="image-select">
          <ul>
            <li>bullet</li>
            <li>bullet</li>
            <li>bullet</li>
          </ul>    
        </div>
        
        <div class="col-xs-6"> 
          <img src="../img/trump.jpg" @click="alertme()" class="image-select">
          <ul>
            <li>bullet</li>
            <li>bullet</li>
            <li>bullet</li>
          </ul>  
        </div>
        
      </div>
    </div>

    <div v-if="step == 2">
      <h1>Which Side?</h1>
      <div class="row">
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
                
            <button type="button" id="submit" name="submit" class="btn btn-primary pull-right">See Results</button>
            </form>
        </div>
      </div>
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
  }
}



</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.header{
  height: 50px;
  width:100%;
  background-color:red;
  margin-bottom: 40px;
}
.centered{
  margin:0 auto;
}
.btn-primary{
  background-color:red;
  font-weight: 1em;
}
img {
  max-width: 200px;
}

h1, h2 {
  font-weight: normal;
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
