<template>
  <div class="home">
    <h3 v-if="listNumber">{{ listNumber }} Items In List</h3>
    <h3 v-else>Please Add Items</h3>
    <form>
      <input v-model="item" type="text" placeholder="Enter Item" />
      <button class="btn-add" @click="addItem">Add</button>
    </form>
    <ul>
      <li v-for="(item, i) in itemList" :key="i">
        <span>{{ item }}</span
        ><button class="btn-remove" @click="() => removeItem(i)">Remove</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      item: "",
      itemList: [],
      listNumber: "",
    };
  },
  methods: {
    addItem() {
      this.itemList.push(this.item);
      this.listNumber = this.itemList.length;
      this.item = "";
    },
    removeItem(i) {
      this.itemList.splice(i, 1);
    },
  },
};
</script>

<style>
.home {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
h3 {
  margin-top: 30px;
}
form {
  width: 458px;
  height: 109px;
  background: #ffffff;
  box-shadow: 0px 5px 20px rgba(0, 0, 0, 0.25);
  border-radius: 24px;
  margin-top: 30px;
  display: flex;
  align-items: center;
}
input {
  width: 249px;
  padding: 5px;
  border: none;
  border-bottom: 1px solid black;
  margin-left: 34px;
}
input:focus {
  outline: none;
}
::placeholder {
  font-size: 16px;
}
.btn-add {
  width: 115px;
  height: 47px;
  background-color: #81559b;
  color: #ffffff;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 10px;
  outline: none;
  border: none;
  margin-left: 24px;
  margin-top: -15px;
  cursor: pointer;
}
ul {
  width: 600px;
  height: 596px;
  margin-top: 30px;
  background: #ffffff;
  box-shadow: 0px 5px 20px rgba(0, 0, 0, 0.25);
  border-radius: 32px;
  padding: 38px;
  padding-top: 0;
  list-style: none;
}
li {
  width: 530px;
  height: 116px;
  background-color: #b2ef9b;
  border-radius: 10px;
  padding-left: 54px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 18px;
  font-weight: bold;
  margin-top: 37px;
}
.btn-remove {
  margin-right: 38px;
  width: 163px;
  height: 47px;
  color: white;
  background: #8c86aa;
  border-radius: 10px;
  border: none;
  outline: none;
  cursor: pointer;
  font-size: 18px;
}
</style>
