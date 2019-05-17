<template>
  <f7-page :page-content="false"  name="homecall">
 
          <f7-block class="">

            <f7-row class="" >
          
              <f7-col v-for="personCall in dataPerson" :key="personCall.id" class="margin-bottom "  width="50" tablet-width="25" :style="{backgroundImage:'url('+personCall.image+')'}" >
                  <f7-link color="white"  class="display-block " popover-open=".popover-menuAppel" > 
                    <f7-card class="bg-color-none no-margin">
                        <f7-card-content>
                          <p><f7-link  class="float-right" popover-close=".popover-menuAppel" raised sheet-open=".demo-sheet" icon-f7="more_vertical_fill" icon-color="white"></f7-link></p>
                          <h1 class="text-align-center">{{personCall.nom.charAt(0).toUpperCase()}}</h1>
                          <p>{{personCall.nom}}</p>
                          {{personCall.typeContact}}
                        </f7-card-content>
                       
                      </f7-card>
                    </f7-link>
              </f7-col>
            </f7-row>
          
          </f7-block>
       
       
            <f7-popover class="popover-menuAppel">
              <f7-list>
                <f7-list-item no-chevron link="#" popover-close title="SIM 1"></f7-list-item>
              <f7-list-item no-chevron link="#" popover-close title="SIM 2" ></f7-list-item>
              </f7-list>
            </f7-popover>

    <f7-sheet   class="demo-sheet" :opened="sheetOpened" @sheet:closed="sheetOpened = false">
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

  

  </f7-page>
</template>
<script>
export default {
  data(){
    return{
 sheetOpened:false,

 //Mes donnees
   dataPerson:[
        {
          id:'1',
          nom:'Marie Justine',
          image:'../static/img/img_avatar2.png',
          typeContact:'mobile'
        },
         {
          id:'2',
          nom:'Nelly',
          image:'../static/img/img_avatar.png',
          typeContact:'telephone'
        },
         {
          id:'3',
          nom:'Marie Grace ',
          image:'../static/img/img_avatar2.png',
          typeContact:'mobile'
        },
         {
          id:'4',
          nom:'Elsa',
          image:'../static/img/img_avatar.png',
          typeContact:'mtn'
        },
         {
          id:'5',
          nom:'Arlette',
          image:'../static/img/img_avatar.png',
          typeContact:'mobile'
        },
         {
          id:'6',
          nom:'sheila',
          image:'../static/img/img_avatar2.png',
          typeContact:'orange'
        },
         {
          id:'7',
          nom:'Leslie',
          image:'../static/img/img_avatar.png',
          typeContact:'mobile'
        },
         {
          id:'8',
          nom:'Erika Michelle',
          image:'../static/img/img_avatar2.png',
          typeContact:'mobile'
        },
         {
          id:'9',
          nom:'Anaelle',
          image:'../static/img/img_avatar.png',
          typeContact:'mobile'
        }
      ]
    };

  },
}
</script>


