<template>
  <div class="home">
    <div class="myContainer">
      <ul>
        <li><h1>{{domande[4].domanda}}</h1></li>
        <li v-for="(risp,index) in domande[4].risposte" v-on:click="getStatus()" :class="{'green': risp.status && val == true,'red': !risp.status && val == true}" >{{risp.name}}</li>
      </ul>
    </div>
  </div>
</template>
      
<script>
// @ is an alias to /src

export default {
  name: "Home",
  data: function () {
    return {
      domande: [
        {
          domanda : 'Chi è il più bello del mondo?',
          risposte : {
            0: {
              name: 'Matthew',
              status: true,
              },
            1: {
              name: 'Sara',
              status: false,
              },
            2: {
              name: 'Brian',
              status: false,
              },
            3: {
              name: 'Kevin',
              status: false,
              },
          }
        },
        {
          domanda : 'Chi è il più forte del mondo?',
          risposte : {
            0: {
              name: 'Matthew',
              status: true,
              },
            1: {
              name: 'Sara',
              status: false,
              },
            2: {
              name: 'Brian',
              status: false,
              },
            3: {
              name: 'Kevin',
              status: false,
              },
          }
        },
        {
          domanda : 'Chi è il più effemminato del mondo?',
          risposte : {
            0: {
              name: 'Matthew',
              status: true,
              },
            1: {
              name: 'Simone',
              status: false,
              },
            2: {
              name: 'Mirko',
              status: false,
              },
            3: {
              name: 'Alfonso',
              status: false,
              },
          }
        },
        {
          domanda : 'Chi è il più forte a Macchiavelli?',
          risposte : {
            0: {
              name: 'Matthew',
              status: true,
              },
            1: {
              name: 'Matthew',
              status: true,
              },
            2: {
              name: 'Matthew',
              status: true,
              },
            3: {
              name: 'Matthew',
              status: true,
              },
          }
        },
        {
          domanda : 'Chi è il più grasso del mondo?',
          risposte : {
            0: {
              name: 'Lori',
              status: true,
              },
            1: {
              name: 'Sara',
              status: false,
              },
            2: {
              name: 'Michela',
              status: false,
              },
            3: {
              name: 'Broni',
              status: false,
              },
          }
        },
      ],
      val: false,
     
    }
  },
  methods: {
    getStatus: function () {
      this.val = !this.val;
    }
  }
};
</script>
      
      
  
     
      
      
        
     

    
