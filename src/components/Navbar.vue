<template>
    <div>
        <div class="soto">
            <div class="logo">
                
            </div>
            <div class="searchBox">
                <div class="topLine">
                    <label for="search">
                        <i class="fas fa-search"></i>
                        <input type="text" id="search" size="34" placeholder="搜尋活動">
                    </label>
                </div>
                <div class="botLine">

                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.soto {
    width: 100%;
    height: 92px;
    background-color: #7828b4;
    display: flex;
}
.soto .logo {
    background-image: url('../assets/logo.png');
    width: 157px;
    height: 44px;
    background-repeat: no-repeat;
    background-position-y: 8px;
    margin-top: 24px;
    margin-left: 6.5%;
}
.searchBox {
    width: 388px;
    height: 30.5px;
    margin-left: 12.1%;
    margin-top: 37px;
    margin-bottom: 24.5px;
}
.topLine {
    width: 388px;
}
label {
    display: flex;
}
i {
    font-size: 20px;
    color: #fff;
}
input {
    height: 24px;
    font-size: 20px;
    background-color: #7828b4;
    border: none;
    margin-left: 1.7%;
    color: #fff;
    outline: none;
}
input::placeholder {
    color: rgba(255, 255, 255, .5);
}
.botLine {
    width: 388px;
    border-bottom: 1px solid #fff;
    margin-top: 4.5px;
}
</style>