<template>
    <div class="container">
        <div class="center">
            <div class="col-7">
                <input type="text" placeholder="ERP ID" class="form-control">
                <br>
                <input type="password" placeholder="ERP PASSWORD" class="form-control">
            </div>
            <div class="col-btn">
                <div class="btn-login">
                    <ion-icon class="icon-btn" name="checkmark-outline"></ion-icon>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
.container {
  display: flex;
  justify-content: center;
  position: relative;
}
.icon-btn{
    margin-top:25%;
    font-size: 3rem;
}
.btn-login{
    width: 100px;
    height: 100px;
    border-radius: 100%;
    border: none;
    background: rgb(79, 170, 255);
    color: antiquewhite;
    margin-left: 1rem;
    margin-top: 20%;
    text-align: center;
}
.center {
  width: 50%; 
  padding: 10px;
  display: flex;
  margin-top: 25%;
}
.col-7{
    width: 70%;
}
input{
    width: 100%;
    font-size: 2rem;
    font-family: 'Roboto Condensed', sans-serif;
    margin-bottom: 1em;
    border-top-style: hidden;
    border-right-style: hidden;
    border-left-style: hidden;
    border-bottom-style: groove  grey;
}
textarea:focus, input:focus{
    outline: none;
}
</style>