<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>Here are my musical keys</p>

    <div class="keys">
      <div data-key="90" class="key">
        <kbd>Z</kbd>
        <span class="sound">clap</span>
      </div>
      <div data-key="88" class="key">
        <kbd>X</kbd>
        <span class="sound">hihat</span>
      </div>
      <div data-key="67" class="key">
        <kbd>C</kbd>
        <span class="sound">kick</span>
      </div>
      <div data-key="86" class="key">
        <kbd>V</kbd>
        <span class="sound">openhat</span>
      </div>
      <div data-key="66" class="key">
        <kbd>B</kbd>
        <span class="sound">boom</span>
      </div>
      <div data-key="78" class="key">
        <kbd>N</kbd>
        <span class="sound">ride</span>
      </div>
      <div data-key="77" class="key">
        <kbd>M</kbd>
        <span class="sound">snare</span>
      </div>
    </div>

    <audio data-key="90" src="../sounds/clap.wav"></audio>
    <audio data-key="88" src="../sounds/hihat.wav"></audio>
    <audio data-key="67" src="../sounds/kick.wav"></audio>
    <audio data-key="86" src="../sounds/openhat.wav"></audio>
    <audio data-key="66" src="../sounds/boom.wav"></audio>
    <audio data-key="78" src="../sounds/ride.wav"></audio>
    <audio data-key="77" src="../sounds/snare.wav"></audio>
  </div>
</template>

<script>
export default {
  name: "Poushita",
  props: {
    msg: String
  },
  created: function() {
    window.addEventListener("keydown", this.playSound);
  },
  destroyed: function() {
    window.removeEventListener("keydown", this.playSound);
  },
  methods: {
    playSound: e => {
      const key = document.querySelector(`div[data-key="${e.keyCode}"]`);
      const soundName = key.querySelector(".sound").textContent;
      let audio = new Audio(require(`../sounds/${soundName}.wav`));
      audio.play();
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  font-size: 10px;
  background: url(http://i.imgur.com/b9r5sEL.jpg) bottom center;
  background-size: cover;
}
body,
html {
  margin: 0;
  padding: 0;
  font-family: sans-serif;
}
.keys {
  display: flex;
  flex: 1;
  min-height: 100vh;
  align-items: center;
  justify-content: center;
}
.key {
  border: 0.4rem solid black;
  border-radius: 0.5rem;
  margin: 1rem;
  font-size: 1.5rem;
  padding: 1rem 0.5rem;
  transition: all 0.07s ease;
  width: 10rem;
  text-align: center;
  color: white;
  background: rgba(0, 0, 0, 0.4);
  text-shadow: 0 0 0.5rem black;
}
.playing {
  transform: scale(1.1);
  border-color: #ffc600;
  box-shadow: 0 0 1rem #ffc600;
}
kbd {
  display: block;
  font-size: 4rem;
}
.sound {
  font-size: 1.2rem;
  text-transform: uppercase;
  letter-spacing: 0.1rem;
  color: #ffc600;
}
</style>
