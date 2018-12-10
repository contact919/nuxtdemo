<template>
  <div>
    <h1 class="edit">编辑页面 editId {{$route.query.editId}}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: this.$route.query.editId
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {hid: "keywords", name: "keywords", content: "乒乓球,乒乓球学习,桌球,table tennis,正手攻球,弧圈球"},
        {hid: "description", name: "description", content: "专注青少年学生乒乓球教学"}
      ]
    }
  }
}
</script>

<style>
.edit{
  color: rgb(81, 145, 230);
}
</style>
