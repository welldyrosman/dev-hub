<template>
    <div class="container">
        <div class="center">
            <div class="col-7">
                <input type="text" v-model="form.userid" placeholder="ERP ID" class="form-control">
                <br>
                <input type="password" v-model="form.password" placeholder="ERP PASSWORD" class="form-control">
                <em><p class="notif tprimary">WRONG ID OR PASSWORD</p></em>
            </div>
            <div class="col-btn">
                <div v-on:click="login" class="btn-login" :class="btncolor">
                    <ion-icon class="icon-btn" :name="btnname"></ion-icon>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            form:{
                userid:"",
                password:""
            },
            isloginoke:"",
            btnname:"arrow-forward-outline",
            btncolor:"primary"
        }
    },
    methods:{
        login(){
            if(this.form.userid=="admin"&&this.form.userid=="123"){
                this.btnname="checkmark-outline"
                this.btncolor="success"
            }else{
                this.btnname="close-outline"
                this.btncolor="danger"
            }
        }
    }
}
</script>
<style scoped>
.notif{
    text-align: right;
}
.container {
  display: flex;
  justify-content: center;
  position: relative;
}
.icon-btn{
    margin-top:25%;
    font-size: 3rem;
}
.tprimary{
    color: rgb(79, 170, 255);
}
.tdanger{
    color: rgb(231, 58, 58);
}
.primary{
    background: rgb(79, 170, 255);
}
.danger{
    background: rgb(231, 58, 58);
}
.success{
    background: rgb(38, 212, 204);
}
.btn-login{
    width: 100px;
    height: 100px;
    border-radius: 100%;
    border: none;
    color: antiquewhite;
    margin-left: 1rem;
    margin-top: 20%;
    text-align: center;
    cursor: pointer;
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