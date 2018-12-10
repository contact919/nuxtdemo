<template>
  <div>
    <el-row>
      <el-col :span="8" v-for="(o, index) in 1" :key="o" :offset="index > 0 ? 2 : 0">
        <el-card :body-style="{ padding: '0px' }">
          <div style="padding: 14px;">
            <span>id: {{ $route.params.id }}</span>
            <div class="bottom clearfix">
              <time class="time">{{num}}</time>
              <el-button type="text" class="button">操作按钮</el-button>
            </div>
          </div>
        </el-card>
      </el-col>
    </el-row>
  </div>      
</template>
    
<style>
  .time {
    font-size: 13px;
    color: #999;
  }
  
  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }

  .button {
    padding: 0;
    float: right;
  }

  .image {
    width: 100%;
    display: block;
  }

  .clearfix:before,
  .clearfix:after {
      display: table;
      content: "";
  }
  
  .clearfix:after {
      clear: both
  }
</style>

<script>
export default {
  data() {
    return {
      currentDate: new Date(),
      num: 100
    };
  },
  validate ({params}){    
    console.log(params); 
    return /^\d+$/.test(params.id)      //正则比较
  },
  asyncData(ctx) {
    let num2 = ctx.route.params.id
    console.log(ctx.route.params.id)
    return {num: num2}
  },
  mounted() {
        console.log(this.num)

  },
}
</script>
