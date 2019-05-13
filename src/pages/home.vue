<template>
  <f7-page name="home" hide-navbar-on-scroll>
    <!-- Top Navbar -->
 
<f7-navbar>
    <f7-appbar :inner="false">
      <f7-searchbar
        search-container=".search-list"
        search-in=".item-title"
        placeholder="Saisir nom,téléphone"
        :disable-button="!$theme.aurora"
      >
       <f7-link  icon-f7="mic_fill"></f7-link>
       <f7-link popover-open=".popover-menu" icon-f7="more_vertical"></f7-link>
      
      </f7-searchbar>
    </f7-appbar>
  </f7-navbar>
    <f7-popover :backdrop="false" class="popover-menu">
      <f7-list>
        <f7-list-item link="#" popover-close title="Dialog"></f7-list-item>
        <f7-list-item link="#"  popover-close title="Appeler"></f7-list-item>
        <f7-list-item link="#" popover-close title="Rechercher" class="searchbar-enable" data-searchbar=".searchbar-demo1"></f7-list-item>
        <f7-list-item link="#" popover-close title="Form Inputs"></f7-list-item>
         <f7-list-item link="#" popover-close class="popover-open"  data-popover=".popover-about" title="About"></f7-list-item>
      </f7-list>
    </f7-popover>

<!-- Views/Tabs container -->
 
    <!-- Tabbar for switching views-tabs -->
    <f7-toolbar tabbar labels top >
      <f7-link tab-link="#view-homecall" tab-link-active icon-ios="f7:star" icon-aurora="f7:star" icon-md="material:star" text=" " @click="isHomePage=true"></f7-link>
      <f7-link tab-link="#view-catalog" icon-ios="f7:access_time" icon-aurora="f7:access_time" icon-md="material:access_time" text=" " @click="isHomePage=false"></f7-link>
      <f7-link tab-link="#view-settings" icon-ios="f7:people" icon-aurora="f7:people" icon-md="material:people" text=" " @click="isHomePage=false"></f7-link>
     
    </f7-toolbar>
 <f7-views  tabs class="safe-areas ">
    <!-- Your main view/tab, should have "view-main" class. It also has "tab-active" class -->
    <f7-view class="page-content" id="view-homecall" main tab tab-active url="/homecall/" ></f7-view>

    <!-- Catalog View -->
    <f7-view class="page-content" id="view-catalog" name="catalog" tab url="#"></f7-view>

    <!-- Settings View -->
    <f7-view class="page-content" id="view-settings" name="settings" tab url="#"></f7-view>

   
  </f7-views>

   <f7-fab v-if="isHomePage" position="center-bottom" slot="fixed" text="" color="blue">
    <f7-icon ios="f7:dialpad" aurora="f7:dialpad" md="material:dialpad" color="white"></f7-icon>
  </f7-fab>
 
    
  </f7-page>
</template>
<script>
export default {
  data(){
    return{
      isHomePage:true
    }
  }
}
</script>

