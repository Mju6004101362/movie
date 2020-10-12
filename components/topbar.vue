<template>
<div class="topbar">
    <img src="~/assets/img/logo.png" alt="">
    <ul>
        <li class="menu">หน้าแรก</li>
        <li class="menu">โรงภาพยนตร์</li>
        <li class="menu">ภาพยนตร์</li>
        <li>
            <input type="text" placeholder="ค้นหาภาพยนตร์">
            <button>ค้นหา</button>
        </li>
    </ul>
</div>
</template>

<script>
export default {}
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.topbar {
    width: 100%;
    height: auto;
    background-color: rgb(255, 217, 0);
}

.topbar img {
    width: 6%;
    display: block;
    margin: auto;
}

.topbar ul {
    display: flex;
    justify-content: space-between;
    height: 40px;
    background-color: rgb(95, 95, 95);
}

.topbar ul li {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    font-size: 16px;
    font-weight: 500;
    color: #fff;
    cursor: pointer;
    transition: 0.3s;
}

.topbar ul .menu:hover {
    background-color: rgb(73, 73, 73);
}

.topbar input {
    border-radius: 4px;
    border: none;
    padding: 0 12px;
    margin-right: 8px;
}

.topbar button {
    width: 60px;
    background-color: rgb(255, 217, 0);
    border-radius: 4px;
    border: none;
}
</style>
