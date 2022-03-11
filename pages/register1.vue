<template>
  <v-row justify="center">
    <div class="bg">
      <v-col cols="12" sm="8" md="6">
        <div class="glass">
          <div class="topic">
            <h3>Sign in</h3>
          </div>
          <div class="txt">
            <v-text-field
              label="ชื่อ-นามสกุล"
              single-line
              solo
              light
              background-color="#E8EAE6"
            />
          </div>
          <div class="txt1">
            <v-text-field
              label="E-mail"
              single-line
              solo
              light
              background-color="#E8EAE6"
            />
          </div>
          <div class="txt2">
            <v-text-field
              label="Password"
              single-line
              solo
              light
              background-color="#E8EAE6"
            />
          </div>
          <v-btn
            class="btn1"
            depressed
            @click="onSave"
          >
            sign up
          </v-btn>
        </div>
      </v-col>
    </div>
    <div class="back">
      <v-btn
        href="login1"
        class="btn2"
        dark
        left
      >
        <v-icon
          dark
          left
        >
          mdi-arrow-left
        </v-icon>Back
      </v-btn>
    </div>
  </v-row>
</template>

<script>
export default ({
  data: () => ({
    user: '',
    passwd: ''
  }),
  methods: {
    async onSave () {
      console.log('onSave')
      const res = await fetch('http://localhost:7001/list?user=63309010014&pass=123456')
      const data = await res.json()
      console.log('data=', data)
    }

  }
})
</script>

<style>
.pa-7{
  margin-top: 2rem;
}
.bg{
  background-color: #ACB992;
}
.glass{
  background-color: #fff;
  border-radius: 40px;
  box-shadow: 4px 4px 4px #455848;
  margin: 12px 10px;
  padding: 14px 10px 12px 12px;
  margin-top: 5rem;
}
.txt {
  margin: 8px 12px;
  width: 250px;
}
.txt1 {
  margin: 8px 12px;
  text-align: left;
  width: 250px;
}
.txt2 {
  margin: 8px 12px;
  text-align: left;
  width: 250px;
}
.v-text-field{
    border-radius: 20px;
    font-size: 16px;
    margin: 8px 0;
    padding: 12px 20px;
}
.v-text-field label{
  padding-left: 12px;
}
.topic{
  color: #7C9473;
  font-family: serif;
  font-size: 32px;
  padding: 12px 16px;
}
.btn1 {
  background: #415542 !important;;
  size: 30px;
  border-radius: 15px;
  box-shadow: 2px 2px 2px #a5a5a5;
}
.v-btn{
  margin-bottom: 1rem;
}
.back{
  position: fixed;
  left: 0;
  bottom: 0;
  margin-bottom: 5rem;
  margin-left: 2rem;
}
.btn2 {
  background: #A35638 !important;;
  size: 30px;
  border-radius: 15px;
  box-shadow: 2px 2px 2px #a5a5a5;
}
</style>
