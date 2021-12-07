<template>
  <div class="menu-container" @click="handleClick" :class="active">
    <div class="menu-content">
      {{ title }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'menuBox',
  props: ['title'],
  data() {
    return {
      active: { active: false }
    }
  },
  methods: {
    handleClick() {
      this.active.active = !this.active.active
      console.log('clicked', this.active.active)
    }
  }
}
</script>

<style scoped>
.menu-container {
  display: flex;
  border: 1px solid black;
  margin: 0.5%;
  flex-direction: column;
  align-items: center;
  z-index: 5;
  transition-duration: 1s;
  position: relative;
  background-color: transparent;
  width: 100%;
  height: 98%;
}

.menu-container::before {
  content: '';
  position: absolute;
  top: -50px;
  left: 0;
  width: 100%;
  height: calc(100% + 100px);
  clip-path: polygon(0% 0%, 100% 50px, 100% 100%, 0% calc(100% - 50px));
}

.menu-content {
  width: 100%;
  height: 100%;
  border: 1px dotted red;
  z-index: 4;
  display: flex;
  align-items: center;
  justify-content: center;
  background: white;
}

.menu-container.active {
  position: fixed;
  width: 99%;
  height: 98%;
  z-index: 10;
}
</style>