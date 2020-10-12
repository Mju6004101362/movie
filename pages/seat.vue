<template>
<div>
    <h3>เลือกที่นั่ง</h3>
    <div class="seat-grid">
        <label>A</label>
        <div class="seat" v-for="index in 5" :key="index">
            {{index}}
        </div>
        <label>B</label>
        <div class="seat" v-for="index in 5" :key="index">
            {{index+5}}
        </div>
        <label>C</label>
        <div class="seat" v-for="index in 5" :key="index">
            {{index+10}}
        </div>
        <label>D</label>
        <div class="seat" v-for="index in 5" :key="index">
            {{index+15}}
        </div>
        <label>E</label>
        <div class="seat" v-for="index in 5" :key="index">
            {{index+20}}
        </div>
        <label>F</label>
        <div class="seat" v-for="index in 5" :key="index">
            {{index+25}}
        </div>
    </div>
</div>
</template>

<script>
export default {
    layout: 'main'
}
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

h3 {
    text-align: center;
}

.seat-grid {
    width: 500px;
    margin: auto;
    display: grid;
    grid-template-columns: auto auto auto auto auto auto;
    grid-gap: 16px;
    justify-content: center;
}

.seat-grid .seat {
    width: 40px;
    height: 40px;
    border-radius: 4px;
    background-color: yellowgreen;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    transition: 0.3s;
}

.seat-grid .seat:hover {
    background-color: rgb(135, 180, 44);
}
</style>
