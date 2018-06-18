<template>
    <div>
        <div class="bg">
            <div class="row">
                <div class="col-lg-2 left">
                    <div class="leftBox">
                        <div class="firstList list">
                            <div class="title">
                                地點
                            </div>
                            <select id="contry">
                                <option value="" class="opt">Taiwan</option>
                            </select>
                        </div>
                        <div class="secondList list">
                            <div class="title">
                                日期
                            </div>
                            <label for="firstDate">
                                <p>from</p>
                                <input type="date" id="firstDate" class="date">
                            </label>
                            <label for="secondDate">
                                <p>to</p>
                                <input type="date" id="secondDate" class="date">
                            </label>
                        </div>
                        <div class="thirdList list">
                            <div class="title">
                                標籤
                            </div>
                            <label class="check checkClass">
                                全部
                                <input type="checkbox">
                                <span class="checkmark"></span>
                            </label>
                            <label class="check checkClass">
                                娛樂
                                <input type="checkbox">
                                <span class="checkmark"></span>
                            </label>
                            <label class="check checkClass">
                                食物
                                <input type="checkbox">
                                <span class="checkmark"></span>
                            </label>
                            <label class="check checkClass">
                                學習
                                <input type="checkbox">
                                <span class="checkmark"></span>
                            </label>
                            <label class="check checkClass">
                                戶外
                                <input type="checkbox">
                                <span class="checkmark"></span>
                            </label>
                        </div>
                    </div>
                </div>
                <div class="col-lg-10 right">
                    <div class="topSide">
                        <div class="msg">
                            找到<div class="purple">{{ datas.length }}</div>個搜尋結果...
                        </div>
                        <div class="tag">
                            <label for="txt">
                                娛樂
                                <i class="far fa-times-circle" id="txt"></i>
                            </label>
                        </div>
                    </div>
                    <div class="botSide">
                        <ul v-for="(data, id) in datas" :key="data.id">
                            <li>
                                <div class="img">

                                </div>
                                <div class="info">
                                    <div class="infoTitle">
                                        {{ data.title }}
                                    </div>
                                    <div class="infoContent">
                                        {{ data.content }}
                                    </div>
                                    <div class="infoTagBox">
                                        <div class="infoTag">
                                            娛樂
                                        </div>
                                    </div>
                                    <div class="infoIcons">
                                        <div class="iconBox">
                                            <i class="fas fa-map-marker-alt"></i>
                                            <span>{{ data.location }}</span>
                                        </div>
                                        <div class="iconBox">
                                            <i class="far fa-calendar-alt"></i>
                                            <span>{{ data.startDate }} ~ {{ data.endDate }}</span>
                                        </div>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            datas: [
                {
                    title: '標題1',
                    content: '內容1',
                    startDate: '1995/03/29',
                    endDate: '2095/03/29',
                    location: 'Taiwan',
                },
                {
                    title: '標題2',
                    content: '內容2',
                    startDate: '1995/03/29',
                    endDate: '2095/03/29',
                    location: 'Taiwan',
                },
                {
                    title: '標題3',
                    content: '內容3',
                    startDate: '1995/03/29',
                    endDate: '2095/03/29',
                    location: 'Taiwan',
                },
            ],
        }
    },
}
</script>

<style scoped>
.bg {
    width: 100%;
    height: 100vh;
    background-color: #f2f2f2;
}
.leftBox {
    width: 100%;
    padding: 0px;
}
.list {
    background-color: #ebebeb;
    margin-left: 38px;
    border: 1px solid rgba(0, 0, 0, 0);
}
.firstList {
    width: 300px;
    height: 137px;
    border-bottom: 1px solid #d7d7d7;
}
.title {
    font-size: 20px;
    font-weight: bold;
    margin-left: 40px;
    margin-top: 24px;
}
.firstList select {
    width: 220px;
    height: 40px;
    font-size: 16px;
    border-radius: 2px;
    margin-left: 40px;
    margin-top: 15px;
}
.secondList {
    width: 300px;
    height: 197px;
    border-bottom: 1px solid #d7d7d7;
}
.secondList label {
    display: flex;
    justify-content: center;
    margin-top: 24px;
}
.secondList label:last-child {
    margin-top: 8px;
}
.secondList label p {
    width: 40px;
    height: 20px;
    font-size: 16px;
    margin-top: 5px;
    text-align: right;
}
.secondList label .date {
    width: 170px;
    height: 40px;
    border: none;
    border-radius: 2px;
    margin-left: 13px;
    padding-left: 11px;
}
.thirdList {
    width: 300px;
    height: 245px;
}
.checkClass {
    margin-left: 40px;
    margin-top: 8px;
}
.checkClass:first-child {
    margin-top: 24px;
}
.topSide {
    width: 95%;
    margin-top: 24px;
    margin-left: 60px;
    margin-bottom: 24px;
}
.msg {
    font-size: 24px;
    display: flex;
}
.msg .purple {
    color: #7828b4;
    margin-left: 8px;
    margin-right: 8px;
}
.tag {
    width: 128px;
    height: 35px;
    border: 1px solid #9013fe;
    border-radius: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #9013fe;
    padding-top: 5px;
    margin-top: 8px;
    cursor: pointer;
}
.tag label {
    cursor: pointer;
}
.botSide {
    width: 95%;
    height: 85vh;
    margin-left: 60px;
}
.botSide ul {
    width: 65%;
    height: 220px;
    list-style: none;
    margin-bottom: 24px;
}
.botSide ul li {
    width: 100%;
    height: 100%;
}
.botSide ul li .img {
    width: 220px;
    border: 1px solid;
    height: 220px;
    background-image: url('https://cw1.tw/CW/images/article/201707/article-5965b9d9abf26.jpg');
    background-repeat: no-repeat;
    background-size: 220px 220px;
    float: left;
}
.botSide ul li .info {
    background-color: #fff;
    width: 754px;
    height: 220px;
    float: left;
}
.infoTitle {
    width: 436px;
    height: 36px;
    font-size: 24px;
    color: #9013fe;
    display: flex;
    align-items: center;
    margin-top: 24px;
    margin-left: 20px;
}
.infoContent {
    width: 520px;
    height: 50px;
    margin-top: 16px;
    margin-left: 20px;
}
.infoTagBox {
    width: 520px;
    height: 24px;
    margin-left: 20px;
    margin-top: 13px;
}
.infoTag {
    width: 131px;
    height: 24px;
    background-color: #d7d7d7;
    text-align: center;
    color: #fff;
    border-radius: 100px;
}
.infoIcons {
    display: flex;
    width: 520px;
    margin-left: 20px;
    margin-top: 16px;
}
.infoIcons span {
    color: #9b9b9b;
    margin-left: 7px;
}
.iconBox {
    margin-left: 20px;
}
.iconBox:first-child {
    margin-left: 0px;
}

/* 自製checkbox */
.check {
    display: block;
    position: relative;
    padding-left: 22px;
    cursor: pointer;
    font-size: 16px;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
}
.check input {
    position: absolute;
    opacity: 0;
    cursor: pointer;
}
.checkmark {
    position: absolute;
    top: 5px;
    left: 0;
    height: 16px;
    width: 16px;
    background-color: #fff;
}
.check:hover input ~ .checkmark {
    background-color: #f2f2f2;
}
.check input:checked ~ .checkmark {
    background-color: #fff;
}
.checkmark:after {
    content: "";
    position: absolute;
    display: none;
}
.check input:checked ~ .checkmark:after {
    display: block;
}
.check .checkmark:after {
    left: 4px;
    top: 0px;
    width: 8px;
    height: 14px;
    border: solid #2196F3;
    border-width: 0 3px 3px 0;
    -webkit-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    transform: rotate(45deg);
}
</style>
