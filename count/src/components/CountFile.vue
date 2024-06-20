<template>
  <div id="app" class="container">
    <div class="card">
      <button @click="incrementCount">Press me!</button>
      <p>Total Count: {{ count }}</p>
    </div>
    </div>
      <div id="app" class="container2">
        <div class="card2">
          <label for="" class="list">last visit</label><br>
          <input type="text" class="Visit" v-model="visit" placeholder="last visit"><br>
          <button @click="saveVisit">Done!</button>
        </div>
      </div>
      <div id="app" class="container3">
        <div class="card3">
          <label for="notes" class="Notes">Instant Notes</label><br>
          <textarea id="notes" v-model="note" placeholder="Write your notes here..."></textarea><br>
          <button @click="saveNote">Done!</button>
        </div>
      </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      where:null,
      count: 0,
      note: localStorage.getItem('note') || '',
      visit: localStorage.getItem('visit') || '',
    };
  },
  methods: {
    incrementCount() {
      this.count++;
    },
    // notetaken() {
    //       console.log(this.note);
    //     },
    saveNote() {
      localStorage.setItem('note', this.note);
      // alert('Note saved!');
        },
    saveVisit() {
      localStorage.setItem('visit', this.visit);
      // alert('visit saved!');
        },
  }
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f0f0f0;
  margin: 0;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 10vh;
  gap:20px;
}

.card {
  background: #74c8fc;
  padding: 50px;
  border-radius: 8px;
  box-shadow: 0 10px 18px rgba(0, 0, 0, 0.1);
  text-align: center;
  margin-top: -100%;
}
.container2 {
  display: flex;
  margin-left: -190%;
  margin-top: -150%;
  height: 10vh;
}
.card2 {
  background: #74c8fc;
  padding: 30px;
  border-radius: 8px;
  box-shadow: 0 10px 18px rgba(0, 0, 0, 0.1);
  text-align: center;
  margin-top: -20%;

}
.card2 button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 10px;
}
.card2 button:hover {
  background-color: #0056b3;
}

.container3 {
  display: flex;
  justify-content: center;
  align-items:end ;
}
.card3 {
  background: #74c8fc;
  padding: 50px;
  border-radius: 8px;
  box-shadow: 0 10px 18px rgba(0, 0, 0, 0.1);
  text-align: center;
  gap: 20px;
  height: 23vh;
  max-height: 200px;
  margin-top: -210%  ;
  margin-right: -350%;
}
.card3 button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 0px;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 10px;
}
.card button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 10px;
}

.card button:hover {
  background-color: #0056b3;
}

.card p {
  font-size: 18px;
  margin-top: 20px;
}
body{
  background-image: url(@/assets/nice.png);
}



.notes {
  width: auto;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  font-size: 16px;
}
.Notes  {
  font-size: 18px;
  margin-bottom: 10px;
}
.card3 button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;
  margin-top: 10px;
}
.card3 button:hover {
  background-color: #0056b3;
}
.list {
  font-size: 18px;
  margin-bottom: 10px;
}
</style>
