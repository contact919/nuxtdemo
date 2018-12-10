<template>
  <section class="container">
    <div>
      <logo/>
      <el-row>
        <nuxt-link :to="{path: 'edit', query: {editId: 10011}}">
          <el-button type="primary" icon="el-icon-edit">编辑1</el-button>
        </nuxt-link>
        <nuxt-link to="newsList">
          <el-button type="warning" icon="el-icon-star-off">新闻</el-button>
        </nuxt-link>
      </el-row>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.links {
  padding-top: 15px;
}
</style>
