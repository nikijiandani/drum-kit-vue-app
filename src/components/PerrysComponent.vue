<template>
  <div class="perry">
    <h1>{{ msg }}</h1>
    <p>This is Perry's Component. It wears glasses, too...</p>
  </div>
</template>

<script>
let sounds = {
    q: require('../sounds/boom.wav'),
    w: require('../sounds/clap.wav'),
    e: require('../sounds/hihat.wav'),
    r: require('../sounds/kick.wav'),
    t: require('../sounds/openhat.wav'),
    y: require('../sounds/ride.wav'),
    u: require('../sounds/snare.wav'),
    i: require('../sounds/tink.wav'),
    o: require('../sounds/tom.wav')
}



export default {
  name: 'PerrysComponent',
  props: {
    msg: String
  },
  methods: {
    playSound: (e) => {
        switch (e.keyCode) {
            case 81:
                let audioQ = new Audio(sounds.q);
                audioQ.play();
                break;
            case 87:
                let audioW = new Audio(sounds.w);
                audioW.play();
                break;
            case 69:
                let audioE = new Audio(sounds.e);
                audioE.play();
                break;
            case 82:
                let audioR = new Audio(sounds.r);
                audioR.play();
                break;
            case 84:
                let audioT = new Audio(sounds.t);
                audioT.play();
                break;
            case 89:
                let audioY = new Audio(sounds.y);
                audioY.play();
                break;
            case 85:
                let audioU = new Audio(sounds.u);
                audioU.play();
                break;
            case 73:
                let audioI = new Audio(sounds.i);
                audioI.play();
                break;
            case 79:
                let audioO = new Audio(sounds.o);
                audioO.play();
                break;
        }
    },
    // onKeyDown: (e) {
    //     switch (e.keyCode) {
    //         case 81: 
    //             this.playSound(sound1);
    //             break;
    //         default:
    //             console.log('error')
    //             break;
    //     }
    // }
  },
  created: function() {
      window.addEventListener('keydown', this.playSound);
  },
  destroyed: function() {
      window.removeEventListener('keydown', this.playSound);
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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



