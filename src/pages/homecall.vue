<template>
  <f7-page :page-content="false" name="homecall">
   
   
    
        <f7-block class="margeinterieure">

          <f7-block-title>Test</f7-block-title>
<f7-list >
  <f7-list-item-row >
    <f7-list-item-cell class="marge">
           <f7-link  popover-open=".popover-menuAppel" color="white"> <b-card img-src="https://picsum.photos/400/400/?image=41" img-alt="Image" overlay>
                <b-card-title class="myStyle">   <f7-link raised sheet-open=".demo-sheet" icon-f7="more_vertical_fill" icon-color="white"></f7-link></b-card-title>
                <b-card-text >
                  <center><h1>M</h1></center>
                </b-card-text>
                <b-card-text class="">Marie</b-card-text>
            </b-card>
           </f7-link>
  </f7-list-item-cell>
   <f7-list-item-cell class="marge">
           <f7-link  popover-open=".popover-menuAppel" color="white">  <b-card img-src="https://picsum.photos/400/400/?image=41" img-alt="Image" overlay>
                <b-card-title class="myStyle"> <f7-link raised sheet-open=".demo-sheet" icon-f7="more_vertical_fill" icon-color="white"></f7-link></b-card-title>
                <b-card-text>
                 <center><h1>N</h1></center>
                </b-card-text>
                <b-card-text class="">Nina</b-card-text>
            </b-card>
            </f7-link>
  </f7-list-item-cell>
 
  </f7-list-item-row>
  
  <f7-list-item-row >
    <f7-list-item-cell class="marge">
           <f7-link  popover-open=".popover-menuAppel" color="white"> <b-card img-src="https://picsum.photos/400/400/?image=41" img-alt="Image" overlay>
                <b-card-title class="myStyle">   <f7-link raised sheet-open=".demo-sheet" icon-f7="more_vertical_fill" icon-color="white"></f7-link></b-card-title>
                <b-card-text >
                  <center><h1>M</h1></center>
                </b-card-text>
                <b-card-text class="">Marie</b-card-text>
            </b-card>
           </f7-link>
  </f7-list-item-cell>
   <f7-list-item-cell class="marge">
           <f7-link  popover-open=".popover-menuAppel" color="white">  <b-card img-src="https://picsum.photos/400/400/?image=41" img-alt="Image" overlay>
                <b-card-title class="myStyle"> <f7-link raised sheet-open=".demo-sheet" icon-f7="more_vertical_fill" icon-color="white"></f7-link></b-card-title>
                <b-card-text>
                 <center><h1>N</h1></center>
                </b-card-text>
                <b-card-text class="">Nina</b-card-text>
            </b-card>
            </f7-link>
  </f7-list-item-cell>
 
  </f7-list-item-row>
  <f7-list-item-row >
    <f7-list-item-cell class="marge">
           <f7-link  popover-open=".popover-menuAppel" color="white"> <b-card img-src="https://picsum.photos/400/400/?image=41" img-alt="Image" overlay>
                <b-card-title class="myStyle">   <f7-link raised sheet-open=".demo-sheet" icon-f7="more_vertical_fill" icon-color="white"></f7-link></b-card-title>
                <b-card-text >
                  <center><h1>M</h1></center>
                </b-card-text>
                <b-card-text class="">Marie</b-card-text>
            </b-card>
           </f7-link>
  </f7-list-item-cell>
   <f7-list-item-cell class="marge">
           <f7-link  popover-open=".popover-menuAppel" color="white">  <b-card img-src="https://picsum.photos/400/400/?image=41" img-alt="Image" overlay>
                <b-card-title class="myStyle"> <f7-link raised sheet-open=".demo-sheet" icon-f7="more_vertical_fill" icon-color="white"></f7-link></b-card-title>
                <b-card-text>
                 <center><h1>N</h1></center>
                </b-card-text>
                <b-card-text class="">Nina</b-card-text>
            </b-card>
            </f7-link>
  </f7-list-item-cell>
 
  </f7-list-item-row>
  
</f7-list>

 

            
            
        </f7-block>
            <f7-popover class="popover-menuAppel">
              <f7-list>
                <f7-list-item no-chevron link="#" popover-close title="SIM 1"></f7-list-item>
              <f7-list-item no-chevron link="#" popover-close title="SIM 2" ></f7-list-item>
              </f7-list>
            </f7-popover>

        <f7-sheet class="demo-sheet" :opened="sheetOpened" @sheet:closed="sheetOpened = false">
      <f7-toolbar>
        <div class="left"></div>
        <div class="right">
          <f7-link sheet-close>Close</f7-link>
        </div>
      </f7-toolbar>
      <!-- Scrollable sheet content -->
      <f7-page-content>
        <f7-block>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quae ducimus dolorum ipsa aliquid accusamus perferendis laboriosam delectus numquam minima animi, libero illo in tempora harum sequi corporis alias ex adipisci...</p>
          <!-- ... -->
        </f7-block>
      </f7-page-content>
    </f7-sheet>

  <f7-fab position="center-bottom" slot="fixed" text="" color="blue">
    <f7-icon ios="f7:dialpad" aurora="f7:dialpad" md="material:dialpad" color="white"></f7-icon>
  </f7-fab>

  </f7-page>
</template>
<script>
export default {
  data(){
    return{
 sheetOpened:false,
    };

  },
}
</script>


<style>
.myStyle
{
  float:right;
}
.margeinterieure
{
  padding: 0%;
}

.marge
{
 
}

</style>
