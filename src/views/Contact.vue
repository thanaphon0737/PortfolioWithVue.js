<template>
  <div id="contact">
    <h1>Contact</h1>
    <ul>
      <li>Thanaphon.thanusan@gmail.com</li>
      <li>Facebook.com/T.Thanusan</li>
      <li>Github.com/Thanaphon0737</li>
      <li>41 BandonKeaw Moo.9 Pongyangkhok Hangchat Lampang 52190, Thailand</li>
    </ul>
    <label for="fname">Contact Me</label>
    <div>
      <input type="text" v-model="user.name" placeholder="Name" /><br /><br />
      <input
        type="text"
        v-model="user.email"
        placeholder="Email"
      /><br /><br />
      <input
        type="text"
        v-model="user.subject"
        placeholder="Subject"
      /><br /><br />
      <input
        type="textarea"
        v-model="user.message"
        placeholder="Message"
      /><br /><br />
      <button @click="addUser">Submit</button>
    </div>
    <div class="showdata">
      <li v-for="(user, index) in Dusers" :key="index">
        {{ user.name }}, Email {{ user.email}}, Subject {{user.subject}}, Message {{user.message}}
        <button @click="removeUser(index)">X</button>
      </li>
    </div>
  </div>
</template>

<script>
export default {
  name: "contact",
  mounted() {
    if(localStorage.getItem('Dusers')){
      this.Dusers = JSON.parse(localStorage.getItem('Dusers'));
    }
  },
  methods: {
    addUser(){
      this.Dusers.push(this.user)
      this.user = {name:"", email:"", subject:"", message:""}
      localStorage.setItem('Dusers', JSON.stringify(this.Dusers))
      console.log(this.Dusers)
    },
    removeUser(index){
      this.Dusers.splice(index,1)
      localStorage.setItem('Dusers', JSON.stringify(this.Dusers))
    }
  },
  data() {
    return {
      user:{name:"",email:""},
      Dusers: [],
    };
  },
};
</script>

<style></style>
