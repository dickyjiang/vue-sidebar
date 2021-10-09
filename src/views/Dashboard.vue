<template>
<div class="bg-white h-screen">
    <Navbar/>
      <div class="border-black">
          <div class="flex justify-between px-4 py-2 border-b border-black ">
            <div class="text-black text-3xl leading-tight font-semibold">
                <h1>Controlled</h1>
                <h1>Tab</h1>
            </div>
            <div class="">
              <h1 class="text-right">The sidebar is {{ collapsed ? 'closed' : 'open' }}</h1>
              <button class="float-right rounded-full px-3 py-2 text-xs font-semibold text-white bg-black " @click="toggleSidebar">Toggle Sidebar</button>
            </div>
          </div>
          <div class="text-sm flex min-h-screen ">
            <div class="divide-y divide-gray-100 flex-1">
                <Nav class="w-full">
                  <NavItem href="/featured" isActive>Featured</NavItem>
                  <NavItem href="/popular">Popular</NavItem>
                  <NavItem href="/recent">Recent</NavItem>
                </Nav>
                <List>
                  <ListItem v-for="recipe in recipes" :key="recipe.id" :recipe="recipe" />
                </List>
              </div>
            <div class="w-1/4 border-l border-black">
              <SidebarRight/>
            </div>
          </div>
      </div>

</div>
</template>

<script>
import { collapsed, toggleSidebar } from "../components/sidebar/state"
import Navbar from "../components/Navbar.vue"
import SidebarRight from '../components/sidebarRight/SidebarRight.vue'
import Nav from '../components/Nav.vue'
import NavItem from '../components/NavItem.vue'
import List from '../components/List.vue'
import ListItem from '../components/ListItem.vue'

export default {
  name: 'Dashboard',
  // props: ['recipes'],
  data() {
    return {
      recipes: [
        {title:'bacang', time:'60', difficulty:'mayan', servings:'2', author:'siujang', rating:'5'},
        {title:'lotek', time:'60', difficulty:'mayan', servings:'2', author:'siujang', rating:'5'},
        {title:'ambokue', time:'60', difficulty:'mayan', servings:'2', author:'siujang', rating:'5'},
        {title:'cakue', time:'60', difficulty:'mayan', servings:'2', author:'siujang', rating:'5'},

      ]
    }
    
    },
  
  
  components: { 
    Navbar,
    SidebarRight,
    Nav,
    NavItem,
    List,
    ListItem,
  },
    setup() {
        return { collapsed, toggleSidebar}
    }

}
</script>

<style>

</style>