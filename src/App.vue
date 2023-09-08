<template>
  <div id="app">
    <h1>Rock Paper Scissors game</h1>
    
    
    <GameComponent />
  </div>
</template>

<script>
import GameComponent from './components/game.vue';

export default {
  components: {
    GameComponent,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+Thai+Looped:wght@200;900&family=Noto+Sans:wght@500&family=Space+Mono:ital,wght@0,400;1,700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Mali:ital,wght@1,700&family=Noto+Sans+Thai+Looped:wght@200;900&family=Noto+Sans:wght@500&family=Space+Mono:ital,wght@0,400;1,700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Mali:ital,wght@1,700&family=Noto+Sans+Thai+Looped:wght@200;900&family=Noto+Sans:wght@500&family=Rubik+Iso&family=Space+Mono:ital,wght@0,400;1,700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap');
#app {
  text-align: center;
  color: #000000;
  margin-top: 0px;
  background-color: #FFF4C7;
  width: 70%; /* ความกว้างเต็มหน้าจอ */
  height: 110dvh; /* ความสูงเต็มหน้าจอ */
  display: flex;
  flex-direction: column;
}

h1 {
  font-size: 100px;
  font-family: 'Rubik Iso', cursive;
}
h2 {
  font-family: 'Share Tech Mono', monospace;
  font-size: 30px;
}
h3 {
  font-family: 'Mali', cursive;
  font-size: 50px;

}
.player1-name {
  font-size: 34px;
  color: #CD5C5C;
  font-family: 'Press Start 2P', cursive;
}


.player2-name {
  font-size: 34px;
  color: #CD5C5C; 
  font-family: 'Press Start 2P', cursive;
}


.player-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  
  border-radius: 50px; 
  
  
}

.reset-button {
  margin-left: 70px; 
  background-color: #FEB9D0; 
  color: #000000; 
  border-radius: 50px; 
  font-family: 'Mali', cursive;
  font-size: 30px;
}

.reset-button:hover {
  background-color: #ab96e5; 
}
.round-button:hover {
  background-color: #b4538fee; 
}

.round-button {
  
  background-color: #96CFCF; 
  color: #000000;
  border-radius: 50px; 
  font-family: 'Mali', cursive;
  font-size: 30px;
}

.score-container {
  background-color: #E57A72; 
  color: #000000; 
  padding: 3px; 
  margin-top: 15px; 
  text-align: center; 
  border-radius: 50px; 
  border: 2px solid #B19CD8; 
  max-width: 300px; 
  margin: 15px auto;
  font-family: 'Share Tech Mono', monospace;
}

.score-text {
  margin: 0; 
}
.player1-image img{
  width: 50px;
  height: 50px;
}
</style>



