<template>
  <div class="home">
    <div class="myContainer">
      <ul>
        <li><h1>{{domande[1].domanda}}</h1></li>
        <li v-for="risp in domande[1].risposte" v-on:click="getStatus(risp)" :style="val">{{risp.name}}</li>
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
            1: {
              name: 'Matthew',
              status: true,
              },
            2: {
              name: 'Sara',
              status: false,
              },
            3: {
              name: 'Brian',
              status: false,
              },
            4: {
              name: 'Kevin',
              status: false,
              },
          }
        },
        {
          domanda : 'Chi è il più forte del mondo?',
          risposte : {
            1: {
              name: 'Matthew',
              status: true,
              },
            2: {
              name: 'Sara',
              status: false,
              },
            3: {
              name: 'Brian',
              status: false,
              },
            4: {
              name: 'Kevin',
              status: false,
              },
          }
        },
        {
          domanda : 'Chi è il più effemminato del mondo?',
          risposte : {
            1: {
              name: 'Matthew',
              status: true,
              },
            2: {
              name: 'Simone',
              status: false,
              },
            3: {
              name: 'Mirko',
              status: false,
              },
            4: {
              name: 'Alfonso',
              status: false,
              },
          }
        },
        {
          domanda : 'Chi è il più forte a Macchiavelli?',
          risposte : {
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
            4: {
              name: 'Matthew',
              status: true,
              },
          }
        },
        {
          domanda : 'Chi è il più grasso del mondo?',
          risposte : {
            1: {
              name: 'Lori',
              status: true,
              },
            2: {
              name: 'Sara',
              status: false,
              },
            3: {
              name: 'Michela',
              status: false,
              },
            4: {
              name: 'Broni',
              status: false,
              },
          }
        },
      ],
      val: ''
    }
  },
  methods: {
    getStatus: function (risp) {
      let status = risp.status;
      if (status) {
        this.val = 'background-color:green;'
      } else {
        this.val = 'background-color:red;'
      }
    }
  }
};
</script>
     

    
