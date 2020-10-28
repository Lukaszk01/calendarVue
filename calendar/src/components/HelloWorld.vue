<template>
<div class="flex flex-col min-h-full overflow-y-auto">
    <Navbar v-if="shouldShowNavbar" @toggle-sidebar="toggleSidebar" />
    <div
      class="flex-grow relative flex w-full max-w-5xl mx-auto text-gray-700 mt-12 md:mt-16 overflow-hidden"
      @touchstart="onTouchStart"
      @touchend="onTouchEnd"
    >
      <!--Sidebar mask-->
      <div
        v-if="isSidebarOpen"
        class="md:hidden fixed inset-0 w-screen h-full z-10 bg-black opacity-75"
        @click="toggleSidebar(false)"
        @scroll.stop.prevent
      ></div>
      <!--Mobile sidebar-->
      <div
        class="md:hidden z-10"
        :class="[isSidebarOpen ? 'absolute' : 'hidden']"
      >
        <Sidebar
          :items="sidebarItems"
          @toggle-sidebar="toggleSidebar"
          show-nav-links
        >
          <template name="sidebar-top" #top>
            <slot name="sidebar-top" />
          </template>
          <template #bottom>
            <slot name="sidebar-bottom" />
          </template>
        </Sidebar>
      </div>
      <!--Desktop sidebar-->
      <div
        class="flex-shrink-0 hidden md:block md:relative z-10 w-72 overflow-y-auto"
      >
        <Sidebar :items="sidebarItems" @toggle-sidebar="toggleSidebar" show-ads>
          <template name="sidebar-top">
            <slot name="sidebar-top" />
          </template>
          <template name="sidebar-bottom">
            <slot name="sidebar-bottom" />
          </template>
        </Sidebar>
      </div>
      <!--Main page-->
      <div class="flex-grow">
        <!--Home page-->
        <Home v-if="$page.frontmatter.home" />
        <!--Other pages-->
        <Page v-else :sidebar-items="sidebarItems">
          <template #top>
            <slot name="page-top" />
          </template>
          <template #bottom>
            <slot name="page-bottom" />
          </template>
        </Page>
        <!--Bottom page navigation-->
        <PageNav v-bind="{ sidebarItems }" />
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
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
</style>
