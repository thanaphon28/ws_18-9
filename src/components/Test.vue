<template>
<div id="test" class="temp">
    v-model

    <div class="input-group input-group-sm mb-3">
        <span class="input-group-text" id="inputGroup-sizing-sm">user</span>
        <input type="text" class="form-control" aria-label="Sizing example input" v-model="userName">
   </div>

<div class="input-group mb-3">
  <span class="input-group-text" id="inputGroup-sizing-sm">password</span>
  <input type="text" class="form-control" aria-label="Sizing example input" v-model="usrPass">
</div>


<div>
    shown: <br>
    user : {{userName}}<br>
    password : {{usrPass}}
</div>


<div class="container">

 <div class="input-group input-group-sm mb-3">
        <span class="input-group-text" id="inputGroup-sizing-sm">Color</span>
        <input type="text" class="form-control" aria-label="Sizing example input" v-model="background">
   </div>
</div>
    <div v-bind:style="{'background-color' : background}">
    color: {{background}}
    </div>

<div>
</div>




<!-- <div class="card">
        <div class="class-header">
            ชื่อ : {{myInfo.myName}}
            <button type="button" class="btn btn-success" @click="myShownInfo">{{labelBotton}}</button>
        </div>
    <div class="class-body" :hidden="!hideShown">
        myNickName: {{myInfo.myNickName}}
        myStudentID: {{myInfo.myStudentID}}
    </div>

    </div> -->
    





    <!-- v-on
    v-bind -->

    <!-- <button type="button" class="btn btn-primary" v-on:click="alertMsg('D', 'F', $event)">Click</button>
    <button type="button" class="btn btn-secondary" @click="alertMsg">Click</button>
   <button type="button" class="btn btn-success" v-on:dblclick="alertMsgDB">Click</button> -->




     <!-- <p> HelloWorld </p>
     <img v-bind:src=url
     width="5%" height="5%" />
       <p> fName : {{fName}} </p>

        <span/> celsius : {{celsius}}
        <span/> fahrenheit : {{fahrenheit}}
        <p> {{show}}</p> -->




  </div>
  
</template>

<script>
export default {
    name : "test",
    data(){
        return{
              fName : "thanaphon",
            imgName: "ฉัน",
            url: "https://scontent.futp1-1.fna.fbcdn.net/v/t1.6435-9/110055989_3261730180559614_1653728825861650048_n.jpg?_nc_cat=107&ccb=1-5&_nc_sid=09cbfe&_nc_eui2=AeF7Tk78rM5868zCavmTm9_MCFu5G42aHmYIW7kbjZoeZg0vzqBtCHoD7oOSU8OAWovmE0VgsxOO9LJ4mhCHMYfy&_nc_ohc=CstA7T60RfEAX-lqbKa&_nc_ht=scontent.futp1-1.fna&oh=d7c84d6f35b6e84db9b49f3d750d1fa6&oe=616C2ACD"
            ,color : "test",
            celsius : 30,
            dataPumu: ["หัว","ก้อย"],
            text: "click",

            myInfo:{
                myName: "A B",
                myNickName: "C",
                myStudentID: "6130"
            },
            hideShown : true,

            userName: null,
            usrPass: null,
            background:null,


        }
    },
        computed: {
            fahrenheit() {
                 let result = this.celsius *1.8 +32 ;
                return result;
            },
            random(){
                return Math.random() >0.5 ? 1 : 0;
            },
            show(){
                return this.dataPumu[this.random];
            },
            labelBotton(){
                return this.hideShown ? "Hide" : "Shown";
            }

        },
        methods:{
            alertMsg(p1, p2, e){
                 alert(`You ${e.type} the button at ${e.clientX}, ${e.clientV}`);
                 alert(`parameter ${p1}, ${p2}`);
            },
            alertMsgDB(){
                console.log("Thanaphon Jedsadalak");
            },
            myShownInfo(){
                this.hideShown = !this.hideShown;
            }

        }


  };
    
</script>

<style>
 .temp{
        background-color: deepskyblue;
    }
    .test{
        color: cornsilk;
    }

</style>