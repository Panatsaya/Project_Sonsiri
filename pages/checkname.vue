<template>
  <div class="bg">
    <div class="container">
      <div class="head">
        <v-app-bar
          absolute
          color="#66806A"
          flat
          height="100%"
          width="100%"
        >
          <v-toolbar-title class="text-center">
            <h3>ระบบเช็คชื่อนักศึกษาวิชาทหาร</h3>
          </v-toolbar-title>
        </v-app-bar>
      </div>
      <div class="row1">
        <v-row>
          <v-btn
            block
            height="80px"
            color="#E9E5D6"
            href="year1"
          >
            <p>นักศึกษาวิชาทหาร ชั้นปีที่ 1</p>
          </v-btn>
        </v-row>
      </div>
      <div class="row2">
        <v-row>
          <v-btn
            block
            height="80px"
            color="#E9E5D6"
          >
            <p>นักศึกษาวิชาทหาร ชั้นปีที่ 2</p>
          </v-btn>
        </v-row>
      </div>
      <div class="row2">
        <v-row>
          <v-btn
            block
            height="80px"
            color="#E9E5D6"
          >
            <p>นักศึกษาวิชาทหาร ชั้นปีที่ 3</p>
          </v-btn>
        </v-row>
      </div>
      <div class="row2">
        <v-row>
          <v-btn
            block
            height="80px"
            color="#E9E5D6"
          >
            <p>นักศึกษาวิชาทหาร ชั้นปีที่ 4</p>
          </v-btn>
        </v-row>
      </div>
      <div class="row2">
        <v-row>
          <v-btn
            block
            height="80px"
            color="#E9E5D6"
          >
            <p>นักศึกษาวิชาทหาร ชั้นปีที่ 5</p>
          </v-btn>
        </v-row>
      </div>
    </div>
    <v-bottom-navigation
      :value="value"
      color="white"
      background-color="#66806A"
      absolute
    >
      <v-btn>
        <span>หน้าแรก</span>

        <v-icon>mdi-home</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </div>
</template>
<script>
export default {
  data: () => ({ value: 1 })
}
</script>
<style>
.bg{
    background-color: #ACB992;
}
</style>

<style>
.head{
    border-radius: 0px 0px 50px 50px;
}
.row1{
    margin-top: 8rem;
    padding: 12px 18px;
}
.row2{
    margin-top: 1rem;
    padding: 12px 18px;
}
.v-btn{
    box-shadow: 4px 4px 2px#535238;
}
.v-btn p{
    color: #535238;
    padding: 12px 18px;
    font-size: 18px;
}
</style>
