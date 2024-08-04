<!-- <script setup>
import { ref } from 'vue'
const toods = ref([
  {
    id:0,
    name:"代辦事項名稱",
    dueDate:"到期日",
    completed:"是否已完成",
  },
  {
    id: 1,
    name: '購買雜貨',
    dueDate: '2024-07-30',
    completed: true
  },
  {
    id: 2,
    name: '完成報告',
    dueDate: '2024-08-01',
    completed: false
  },
  {
    id: 3,
    name: '清理房間',
    dueDate: '2024-07-28',
    completed: true
  }
])
</script>

const toods = ref([ // { // id:0, // name:"代辦事項名稱", // dueDate:"到期日", //
completed:"是否已完成", // }, { id: 1, name: '購買雜貨', dueDate: '2024-07-30', completed: true }, {
id: 2, name: '完成報告', dueDate: '2024-08-01', completed: false }, { id: 3, name: '清理房間',
dueDate: '2024-07-28', completed: true } ])
<table>
    <thead>
      <tr>
        <th>代辦事項名稱</th>
        <th>到期日</th>
        <th>是否已完成</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="tood in toods" :key="tood.id">
        <td>{{ tood.name }}</td>
        <td>{{ tood.dueDate }}</td>
        <td>{{ tood.completed ? '是' : '否' }}</td>
      </tr>
    </tbody>
  </table> -->

<!-- 
  const meals = ref([
  {
    id: 1,
    name: '珍珠奶茶',
    describe: '香濃奶茶搭配QQ珍珠',
    price: 50,
    inStock: 20
  },
  {
    id: 2,
    name: '冬瓜檸檬',
    describe: '清新冬瓜配上新鮮檸檬',
    price: 50,
    inStock: 18
  },
  {
    id: 3,
    name: '翡翠檸檬',
    describe: '綠茶與檸檬的完美結合',
    price: 55,
    inStock: 34
  },
  {
    id: 4,
    name: '四季春茶',
    describe: '香醇四季春茶，回甘無比',
    price: 45,
    inStock: 10
  },
  {
    id: 5,
    name: '阿薩姆奶茶',
    describe: '阿薩姆紅茶搭配香醇鮮奶',
    price: 50,
    inStock: 25
  },
  {
    id: 6,
    name: '檸檬冰茶',
    describe: '檸檬與冰茶的清新組合',
    price: 45,
    inStock: 20
  },
  {
    id: 7,
    name: '芒果綠茶',
    describe: '果與綠茶的獨特風味',
    price: 55,
    inStock: 18
  },
  {
    id: 8,
    name: '抹茶拿鐵',
    describe: '抹茶與鮮奶的絕配',
    price: 60,
    inStock: 20
  }
])

//console.log(meals.value[0].inStock)
</script> -->

<template>
  <!-- <h1>目前是app.vue</h1> -->
  <!-- <VueComm></VueComm> -->
  <!-- <h2>{{ text2 }}</h2>
  <input type="text" v-model="text2" /> -->
  <h1>VueWeek1 餐點管理工具</h1>
  <table cellpadding="0" cellspacing="0" border="0" class="meals_table">
    <thead>
      <tr>
        <th scope="col">品項</th>
        <th scope="col">描述</th>
        <th scope="col">價格</th>
        <th scope="col">庫存</th>
      </tr>
    </thead>
    <tbody>
      <!-- <tr v-for="meal in meals" :key="meal.id">
        <td>{{ meal.name }}</td>
        <td>
          <small>{{ meal.describe }}</small>
        </td>
        <td>{{ meal.price }}</td>
        <td>
          <button class="reduce">-</button>
          {{ meal.inStock }}
          <button class="add" @click="stockUp(meal.id)">+</button>
        </td>
      </tr> -->
    </tbody>
  </table>
</template>

<style>
h1 {
  text-align: center;
  font-size: 20px;
  line-height: 1;
  padding: 0;
  margin: 0 0 15px;
  display: block;
}

.meals_table {
  width: 100%;
  min-width: 500px;
  margin: 0 auto;
  overflow: hidden;
  box-sizing: border-box;
}

.meals_table th,
.meals_table td {
  text-align: center;
  vertical-align: middle;
  font-size: 15px;
  line-height: 1.5;
  padding: 8px 5px;
}

.meals_table th {
  color: #fff;
  border-top: solid 1px #d6d6d6;
  border-right: solid 1px #d6d6d6;
  border-bottom: solid 1px #d6d6d6;
  background-color: #949494;
}
.meals_table th:first-child {
  border-left: solid 1px #d6d6d6;
}
.meals_table td {
  border-bottom: solid 1px #d6d6d6;
  border-right: solid 1px #d6d6d6;
  background-color: #f8f8f8;
}
.meals_table tr:nth-of-type(2n + 0) td {
  background-color: #ffffff;
}
.meals_table td:first-of-type {
  border-left: solid 1px #d6d6d6;
}

/* 表格_按鈕 */
.meals_table button {
  background: #c1bbbb;
  color: #fff;
  border: none;
  line-height: normal;
  box-sizing: border-box;
  padding: 0 0px;
  font-size: 14px;
  border-radius: 4px;
  width: 20px;
  height: 20px;
  margin: 3px;
  cursor: pointer;
}
.meals_table button:hover {
  opacity: 0.5;
}
</style>
