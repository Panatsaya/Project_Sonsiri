<template>
  <div class="bg">
    <div class="head">
      <v-app-bar
        absolute
        color="#66806A"
        flat
        height="100%"
        width="100%"
      >
        <v-toolbar-title class="text-center">
          <h3>นักศึกษาวิชาทหารชั้นปีที่ 1</h3>
        </v-toolbar-title>
      </v-app-bar>
    </div>
    <div class="tablename">
      <v-simple-table
        fixed-header
        height="500px"
      >
        <template #default>
          <thead>
            <tr>
              <th class="text-center">
                ชื่อ-นามสกุล
              </th>
              <th class="text-center">
                ขาด
              </th>
              <th class="text-center">
                ลา
              </th>
              <th class="text-center">
                มาสาย
              </th>
            </tr>
          </thead>
          <tbody>
            <tr
              v-for="item in desserts"
              :key="item.name"
            >
              <td>{{ item.name }}</td>
              <td>
                <v-checkbox
                  v-model="ex4"
                  color="error"
                  value="error"
                  hide-details
                />
              </td>
              <td>
                <v-checkbox
                  v-model="ex4"
                  color="secondary"
                  value="secondary"
                  hide-details
                />
              </td>
              <td>
                <v-checkbox
                  v-model="ex4"
                  color="indigo"
                  value="indigo"
                  hide-details
                />
              </td>
            </tr>
          </tbody>
        </template>
      </v-simple-table>
    </div>
    <v-bottom-navigation
      :value="value"
      color="white"
      background-color="#66806A"
      absolute
    >
      <v-btn href="checkname">
        <span>หน้าแรก</span>

        <v-icon>mdi-home</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </div>
</template>
<script>
export default {
  data () {
    return {
      ex4: ['red', 'indigo', 'orange', 'primary', 'secondary', 'success', 'info',
        'warning', 'error', 'red darken-3', 'indigo darken-3', 'orange darken-3'],
      desserts: [
        {
          name: 'นายพันธการ',
          calories: 159
        },
        {
          name: 'นายสรณ์สิริ',
          calories: 237
        },
        {
          name: 'นายภัทรนิธิ์',
          calories: 262
        },
        {
          name: 'นายธีรพงษ์',
          calories: 305
        },
        {
          name: 'นายอธิวัฒน์',
          calories: 356
        },
        {
          name: 'นายพงศกร',
          calories: 375
        },
        {
          name: 'นางสาวสุภา',
          calories: 392
        },
        {
          name: 'นายแดงดี',
          calories: 408
        },
        {
          name: 'นางสาวหมูหวาน',
          calories: 452
        },
        {
          name: 'นางสาวธีร่า',
          calories: 518
        },
        {
          name: 'นางสาวธีร่า',
          calories: 518
        },
        {
          name: 'นางสาวธีร่า',
          calories: 518
        }
      ]
    }
  }
}
</script>
<style>
.bg{
    background-color: #ACB992;;
}
.tablename{
    margin-top: 6rem;
}
</style>
