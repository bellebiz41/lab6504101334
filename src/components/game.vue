<template>
    <div>
      <div class="player-container">
        <div>
          <h2 class="player1-name">Player[AI]</h2>
          <div>
            <img v-if="player1Choice === 'ค้อน'" src="./assets/3.png" :width="300" alt="ค้อน" />
            <img v-if="player1Choice === 'กระดาษ'" src="./assets/2.png" :width="300" alt="กระดาษ" />
            <img v-if="player1Choice === 'กรรไกร'" src="./assets/1.png" :width="300" alt="กรรไกร" />
          </div>
          
          
        </div>
  
        <div>
          <h2 class="player2-name">Player[bellaz]</h2>
          <div>
            <img v-if="player2Choice === 'ค้อน'" src="./assets/3.png" :width="300" alt="ค้อน" />
            <img v-if="player2Choice === 'กระดาษ'" src="./assets/2.png" :width="300" alt="กระดาษ" />
            <img v-if="player2Choice === 'กรรไกร'" src="./assets/1.png" :width="300" alt="กรรไกร" />
          </div>
          
          
        </div>
  
      </div>
  <br>
  <br>
      <div>
        <button @click="playRound" class="round-button">เป่ายิ้งฉุบบบบ</button>
        <button @click="resetGame" class="reset-button">เริ่มใหม่ ไม่ยอมแพ้หรอกกก</button>
      </div>
  <br>
      <div class="score-container"> 
      <h2 class="score-text">SCORE {{ player1Score }} : {{ player2Score }}</h2> </div>
    </div>
  </template>
  
  <style>
  
  </style>
  
  
  
  <script>
  import { ref } from 'vue';
  
  export default {
    data() {
      return {
        player1Score: 0,
        player2Score: 0,
        gameResult1: '',
        gameResult2: '',
        player1Choice: '', 
        player2Choice: '', 
        choices: ['ค้อน', 'กระดาษ', 'กรรไกร'],
      };
    },
    methods: {
      playRound() {
        const player1Index = Math.floor(Math.random() * this.choices.length);
        const player2Index = Math.floor(Math.random() * this.choices.length);
  
        const player1Choice = this.choices[player1Index];
        const player2Choice = this.choices[player2Index];
  
        if (player1Choice === player2Choice) {
          this.gameResult1 = 'เสมอ ';
          this.gameResult2 = 'เสมอ ';
        } else if (
          (player1Choice === 'ค้อน' && player2Choice === 'กรรไกร') ||
          (player1Choice === 'กระดาษ' && player2Choice === 'ค้อน') ||
          (player1Choice === 'กรรไกร' && player2Choice === 'กระดาษ')
        ) {
          this.gameResult1 = 'ชนะ ';
          this.gameResult2 = 'แพ้ ';
          this.player1Score++;
        } else {
          this.gameResult1 = 'แพ้ ';
          this.gameResult2 = 'ชนะ ';
          this.player2Score++;
        }
        this.player1Choice = player1Choice;
        this.player2Choice = player2Choice;
      },
      resetGame() {
        this.player1Score = 0;
        this.player2Score = 0;
        this.gameResult1 = '';
        this.gameResult2 = '';
        this.player1Choice = '';
        this.player2Choice = '';
      },
    },
  };
  
  </script>
  