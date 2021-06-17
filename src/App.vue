<template>
  <span
    v-for="item in nums"
    :key="item"
    v-bind:title="message"
    @click="onClick"
  >
    测试绑定属性
  </span>
  <div v-once>
    父级数据 {{ count }}
    <div>
      子集数据 {{count}}
    </div>
  </div>
  <div>
    同级数据 {{ count }}
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      message: '鼠标悬浮效果',
      nums: [1, 2, 3],
      count: 0,
    }
  },
  mounted() {
    
  },
  methods: {
    onClick() {
      alert(123);
    }
  }
}
</script>

