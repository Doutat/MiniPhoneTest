<!--<template>
  <f7-page name="about">
    <f7-navbar title="About" back-link="Back"></f7-navbar>
    <f7-block-title>About My App</f7-block-title>
    <f7-block strong>
      <p>Fugiat perspiciatis excepturi, soluta quod non ullam deleniti. Nobis sint nemo consequuntur, fugiat. Eius perferendis animi autem incidunt vel quod tenetur nostrum, voluptate omnis quasi quidem illum consequuntur, a, quisquam.</p>
      <p>Laudantium neque magnam vitae nemo quam commodi, in cum dolore obcaecati laborum, excepturi harum, optio qui, consequuntur? Obcaecati dolor sequi nesciunt culpa quia perspiciatis, reiciendis ex debitis, ut tenetur alias.</p>
    </f7-block>
    <f7-block>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magni molestiae laudantium dignissimos est nobis delectus nemo ea alias voluptatum architecto, amet similique, saepe iste consectetur in repellat ut minus quibusdam!</p>
      <p>Molestias et distinctio porro nesciunt ratione similique, magni doloribus, rerum nobis, aliquam quae reiciendis quasi modi. Nam a recusandae, fugiat in ea voluptates fuga eius, velit corrupti reprehenderit dignissimos consequatur!</p>
      <p>Blanditiis, cumque quo adipisci. Molestiae, dolores dolorum quos doloremque ipsa ullam eligendi commodi deserunt doloribus inventore magni? Ea mollitia veniam nostrum nihil, iusto doloribus a at! Ea molestiae ullam delectus!</p>
    </f7-block>


  </f7-page>
</template>-->
<template>
  <f7-page name="home">
    <!-- Top Navbar -->
  <f7-navbar>
    <f7-appbar :inner="false">
      <f7-searchbar
        search-container=".search-list"
        search-in=".item-title"
        placeholder="Saisir nom,téléphone"
        :disable-button="!$theme.aurora"
      >
       <f7-link popover-open=".popover-menu" icon-f7="mic_fill"></f7-link>
       <f7-link popover-open=".popover-menu" icon-f7="more_vertical"></f7-link>
      
      </f7-searchbar>
    </f7-appbar>
  </f7-navbar>
    <f7-popover class="popover-menu">
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
    <f7-toolbar tabbar labels top>
      <f7-link tab-link="#view-homecall" tab-link-active icon-ios="f7:star" icon-aurora="f7:star" icon-md="material:star" text=" "></f7-link>
      <f7-link tab-link="#view-catalog" icon-ios="f7:access_time" icon-aurora="f7:access_time" icon-md="material:access_time" text=" "></f7-link>
      <f7-link tab-link="#view-settings" icon-ios="f7:people" icon-aurora="f7:people" icon-md="material:people" text=" "></f7-link>
     
    </f7-toolbar>
 <f7-views  tabs class="safe-areas">
    <!-- Your main view/tab, should have "view-main" class. It also has "tab-active" class -->
    <f7-view  id="view-homecall" main tab tab-active url="/homecall/"></f7-view>

    <!-- Catalog View -->
    <f7-view id="view-catalog" name="catalog" tab url="#"></f7-view>

    <!-- Settings View -->
    <f7-view id="view-settings" name="settings" tab url="#"></f7-view>

   
  </f7-views>

   
 
    
  </f7-page>
</template>
