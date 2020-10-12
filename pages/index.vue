<template>
<div>
    <div class="searhBar">
        <input type="text" placeholder="ค้นหาภาพยนตร์">
        <select name="" id="">
            <option value="">เลือกโรงภาพยนตร์</option>
            <option value="เซนเฟส">เซนเฟส</option>
            <option value="แอร์พอร์ต">แอร์พอร์ต</option>
        </select>
    </div>
    <div style="padding: 32px 0">
        <div class="movieList">
            <div v-for="(i,index) in movieList" :key="index">
                <hr>
                <div class="movieCard">
                    <div>
                        <p>Theatre</p>
                        <h1>{{index+1}}</h1>
                    </div>
                    <img :src="i.img" alt="">
                    <div style="padding:0 16px;">
                        <h3>{{i.title_en}}</h3>
                        <p>{{i.title_th}}</p>
                        <div style="padding:16px 0;">
                          <button>{{i.available}}</button>
                        </div>
                    </div>
                </div>
                <hr>
            </div>
        </div>
    </div>

</div>
</template>

<script>
export default {
    layout: 'main',
    data() {
        return {
            movieList: [{
                title_en: 'Vanguard',
                title_th: 'หน่วยพิทักษ์ฟัดข้ามโลก',
                time: '107 นาที',
                category: 'แอ็คชัน',
                img: 'https://cdn.majorcineplex.com/uploads/movie/2903/thumb_2903.jpg',
                available : '20.00'
            }, {
                title_en: 'Greenland',
                title_th: 'นาทีระทึก..วันสิ้นโลก',
                time: '120 นาที',
                category: 'แอ็คชัน, ระทึกขวัญ',
                img: 'https://cdn.majorcineplex.com/uploads/movie/3068/thumb_3068.jpg',
                available : '21.00'
            }, {
                title_en: 'Bille',
                title_th: 'บิลลี่ ฮอลิเดย์ แจ๊ส เปลี่ยนโลก',
                time: '98 นาที',
                category: 'ชีวิต',
                img: 'https://cdn.majorcineplex.com/uploads/movie/3052/thumb_3052.jpg',
                available : '21.30'
            }, {
                title_en: 'Tesla',
                title_th: 'เทสลา คนล่าอนาคต',
                time: '96 นาที',
                category: 'ชีวิต',
                img: 'https://cdn.majorcineplex.com/uploads/movie/3028/thumb_3028.jpg',
                available : '20.30'
            }]
        }
    }
}
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.searhBar {
    height: 120px;
    display: grid;
    grid-template-columns: auto auto;
    grid-gap: 8px;
    justify-content: center;
    align-items: center;
    background-color: rgb(73, 73, 73);
}

.searhBar input,
.searhBar select {
    width: 200px;
    height: 40px;
    border-radius: 4px;
    border: none;
    padding: 0 12px;
}

.movieList {
    width: 1000px;
    margin: auto;
    padding: 32px 16px;
    background-color: rgb(73, 73, 73);
    border-radius: 4px;
}

.movieCard {
    width: 100%;
    height: 200px;
    border-radius: 4px;
    padding: 17px;
    display: grid;
    grid-template-columns: 10% auto auto;
    justify-content: flex-start;
}

.movieCard img {
    width: 109px;
    border-radius: 4px;
    object-fit: cover;
}

.movieCard .movieText {
    white-space: nowrap;
    width: 100%;
    overflow: hidden;
    text-overflow: ellipsis;
    text-align: center;
    color: #fff;
}

.movieCard button{
  width: 60px;
  border: none;
  border-radius: 4px;
  background-color: rgb(255, 238, 0);
  transition: 0.3s;
}

.movieCard h1,.movieCard h3, .movieCard p{
  color: #fff;
}

.movieCard button:hover{
  filter: brightness(0.8);
}
</style>
