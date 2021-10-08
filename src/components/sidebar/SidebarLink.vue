<template>
    <router-link :to="to" class="link" :class="{ active: isActive }">
    <i class="icon" :class="icon" />
    <transition name="fade">
      <span v-if="!collapsed">
        <slot />
      </span>
    </transition>
  </router-link>
  
</template>

<script>import { computed } from "@vue/reactivity"
import { useRoute } from "vue-router"
import { collapsed } from './state'

export default {
    props: {
        to: { type: String, required: true},
        icon: { type: String, required: true }
    },

    setup(props) {
        const route = useRoute()
        const isActive = computed (() => route.path === props.to)
        return { isActive, collapsed}
    }

}
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.1s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
.link {
  display: flex;
  align-items: center;
  cursor: pointer;
  position: relative;
  font-weight: 400;
  user-select: none;
  margin: 0.5em 0;
  padding: 0.3em;
  border-radius: 0.25em;
  height: 2,5em;
  color: black;
  text-decoration: none;
}
.link:hover {
  background-color: var(--sidebar-item-hover);
  color: white;
}
.link.active {
  background-color: var(--sidebar-item-active);
  color: white;
}
.link .icon {
  flex-shrink: 0;
  width: 25px;
  margin-right: 10px;
}

</style>