<template>
<div>
   <div>
    <el-checkbox style="margin-right: 20px" v-model="checked1" label="扣除信用分" border></el-checkbox>
    <el-input-number v-model="num" @change="handleChange" :min="1" :max="10" ></el-input-number>分
  </div>
  <div style="margin-top: 20px">
    <el-checkbox  style="margin-right: 20px" v-model="checked3" label="禁用账户" border size="medium"></el-checkbox> 
    <el-input-number v-model="num" @change="handleChange" :min="1" :max="10" ></el-input-number>天
  </div>
  <div style="margin-top: 20px">
    <el-checkbox v-model="checked3" label="封停账户" border size="medium"></el-checkbox>
  </div>

</div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
       tableData: [ {
          id: 3,
          date: '河南省',
          name: '无',
         name1: '无',
         name2: '无',
          children: [{
              id: 31,
              date: '洛阳市',
              name: '无',
            name1: '无',
            name2: '无',
            }, {
              id: 32,
              date: '老城区',
              name: '无',
              name1: '无',
              name2: '无',
          }]
        }]
    };
  },
  methods: {
    handleBtn() {
      this.dialogVisible = true;
    },
    handleClose() {
      this.dialogVisible = false;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.hello{
  width: 600px;
  display: flex;
  flex-wrap: wrap;
  line-height: 30px;
  text-align: left;
  /* border: 1px solid red; */
}
.item{
  width: 300px;
}
</style>
