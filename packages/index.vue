<template>
  <div class="list">
    <template v-for="item in list" :key="item.id">
      <div class="label">{{ item.label }}</div>
      <div class="nav-list">
        <div class="nav-list-item" v-for="sitem in list.list" :key="sitem.id">
          {{ sitem.label }}
        </div>
      </div>
    </template>
  </div>
</template>
<script>
export default {
  name: "NavList",
};
</script>
<script setup>
const list = [
  {
    label: "语言识别",
    id: 1,
    list: [
      {
        label: "微信语音",
        id: "1-1",
      },
      {
        label: "qq语音",
        id: "1-2",
      },
    ],
  },
];
</script>
<style>
.list {
  display: flex;
  flex-direction: column;
}

.label {
  font-size: 16px;
  color: #121212;
  font-weight: bold;
}

.nav-list {
  display: flex;
  flex-direction: column;
  margin-left: 14px;
}

.nav-list-item {
  font-size: 14px;
  color: #121212;
}
</style>
