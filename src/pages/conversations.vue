<template>
<f7-page :page-content="false" name="conversations">
    
    <f7-block>
        <f7-block-title >Aujourd'hui</f7-block-title>
        <f7-list >

             <f7-list-item
               v-for="maListe in maListeDeContact"
                :key="maListe.id"
                :title="maListe.nom"
                :footer="maListe.typeContact"
                link="#"
                :after="maListe.heure"
                no-chevron
                data-popover=".popover-menuAppel1"
               class="popover-open" 
            >
            <!--<img slot="media" src="../img/img_avatar.png" width="50" alt="">-->
            <img class="radius-img" slot="media" :src="maListe.image" width="50" alt="">
            <f7-link @click="person()" class="text-color-gray"  popover-open=".popover-afficherInfo" ><f7-icon  ios="f7:keyboard_arrow_down" aurora="f7:keyboard_arrow_down" md="material:keyboard_arrow_down" ></f7-icon></f7-link>
            </f7-list-item>


       
        </f7-list>


    </f7-block>
    
             <f7-popover class="popover-menuAppel1">
              <f7-list>
                <f7-list-item no-chevron link="#" popover-close title="SIM 1"></f7-list-item>
              <f7-list-item no-chevron link="#" popover-close title="SIM 2" ></f7-list-item>
              </f7-list>
            </f7-popover>

            <f7-popover :backdrop="false" class="popover-afficherInfo">
              <f7-list>
                <f7-list-item no-chevron raised sheet-open=".demo-sheet-swipe-to-step"  link="#" popover-close title="Afficher infos appels"></f7-list-item>
                <f7-list-item no-chevron link="#" popover-close title="Envoyer Message" ></f7-list-item>
                <f7-list-item no-chevron link="#" popover-close title="Copier Numero" ></f7-list-item>
              </f7-list>
            </f7-popover>



     <f7-sheet
      class="demo-sheet-swipe-to-step"
      style="height:auto"
      swipe-to-close
      swipe-to-step
      backdrop
    >
      <!-- Initial swipe step sheet content -->
      <div class="sheet-modal-swipe-step" style="background-image:url(https://cdn.framework7.io/placeholder/nature-1000x600-3.jpg)">
        <div class="display-flex padding justify-content-space-between align-items-center">
          <div> <f7-link class="text-color-white" sheet-close><f7-icon  ios="f7:expand_more" aurora="f7:expand_more" md="material:expand_more" ></f7-icon></f7-link></div>
          <div>
            <f7-link sheet-close class="text-color-white"><f7-icon  ios="f7:star_border" aurora="f7:star_border" md="material:star_border" ></f7-icon></f7-link>
           <f7-link popover-open=".popover-menuPlusContact" class="text-color-white" icon-f7="more_vertical_fill"></f7-link>
          </div>
        </div>
        <div class="padding-horizontal padding-bottom">
          <div class="margin-top text-align-left text-color-white" strong><h1>Ribal Nelly</h1></div>
        </div>
      </div>
      <!-- Rest of the sheet content that will opened with swipe -->
          <f7-card >
            <f7-card-content :padding="false">
              <f7-list medial-list>
                <f7-list-item
                  title="676565366"
                  footer="Mobile Cameroun"
                >
                <f7-icon slot="media" ios="f7:phone" aurora="f7:phone" md="material:phone" ></f7-icon>
                <f7-icon ios="f7:message" aurora="f7:message" md="material:message" ></f7-icon>
                </f7-list-item>
              
              </f7-list>
            </f7-card-content>
          
          </f7-card>
           <f7-card >
            <f7-card-content :padding="false">
              <f7-list medial-list>
               
                <f7-list-item
                  title="Appel vocal au 676565366"
                  
                >
                  <img slot="media" src="https://cdn.framework7.io/placeholder/fashion-88x88-5.jpg" width="25"/>
                </f7-list-item>
                <f7-list-item
                   title="Appel video au 676565366"
               
                >
                  <img slot="media" src="https://cdn.framework7.io/placeholder/fashion-88x88-6.jpg" width="25"/>
                </f7-list-item>

                 <f7-list-item
                   title="Message au 676565366"
               
                >
                  <img slot="media" src="https://cdn.framework7.io/placeholder/fashion-88x88-6.jpg" width="25"/>
                </f7-list-item>

              </f7-list>
            </f7-card-content>
          
          </f7-card>

          <f7-card >
            <f7-card-content :padding="false">
              <f7-list medial-list>
               
                <f7-list-item
                  title="13:56"
                  footer="676565366"
                
                >
                   <span slot="after">  <f7-icon class="text-color-red" ios="f7:call_missed_outgoing" aurora="f7:call_missed_outgoing" md="material:call_missed_outgoing" ></f7-icon> manqué</span>
                </f7-list-item>
                <f7-list-item
                  title="11:55"
                  footer="676565366"
                  
                >
                  <span slot="after">  <f7-icon class="text-color-red" ios="f7:call_missed_outgoing" aurora="f7:call_missed_outgoing" md="material:call_missed_outgoing" ></f7-icon> manqué</span>
                </f7-list-item>
                 <f7-list-item
                  title="13:56"
                  footer="676565366"
                  after="7 min et 56 s"
                >
                 
                </f7-list-item>
                <f7-list-item
                  title="11:55"
                  footer="676565366"
                  after="2 min et 12 s"
                >
                 
                </f7-list-item>
                
              </f7-list>
            </f7-card-content>
              <f7-card-footer>
                <f7-link> Plus</f7-link>
              </f7-card-footer>
          </f7-card>
    </f7-sheet>

 <f7-popover :backdrop="false" class="popover-menuPlusContact">
              <f7-list>
                 <f7-list-item no-chevron link="#" popover-close title="partager"></f7-list-item>
                 <f7-list-item no-chevron link="#" popover-close title="Afficher les contacts associés" ></f7-list-item>
                 <f7-list-item no-chevron link="#" popover-close title="Supprimer" ></f7-list-item>
              </f7-list>
            </f7-popover>



     
   
</f7-page>
</template>
<script>
export default {
    data(){
        return{
            sheetOpened:false,
            maListeDeContact:[
                {
                    id:'1',
                    nom:'Edwige Princesse',
                    typeContact:'Mobile',
                    image:'../static/img/beach.jpg',
                    numero:'673554527',
                    heure:'17:16'
                },
                 {
                    id:'2',
                    nom:'Marie Ribal',
                    typeContact:'Mobile',
                    image:'../static/img/img_avatar2.png',
                    numero:'673554527',
                    heure:'17:00'
                },
                 {
                    id:'3',
                    nom:'Leroy ',
                    typeContact:'Mobile',
                    image:'../static/img/img_avatar.png',
                    numero:'673554527',
                    heure:'16:16'
                },
                 {
                    id:'4',
                    nom:'Elisabeth',
                    typeContact:'Mobile',
                    image:'../static/img/img_avatar2.png',
                    numero:'673554527',
                    heure:'15:16'
                },
                 {
                    id:'5',
                    nom:'Lovelyne Ribal',
                    typeContact:'Mobile',
                    image:'../static/img/img_avatar2.png',
                    numero:'673554527',
                    heure:'14:16'
                },
                 {
                    id:'6',
                    nom:'Jerome Lando',
                    typeContact:'Mobile',
                    image:'../static/img/user-male.png',
                    numero:'673554527',
                    heure:'14:16'

                },
                 {
                    id:'7',
                    nom:'Marie Ribal',
                    typeContact:'Mobile',
                    image:'../static/img/img_avatar2.png',
                    numero:'673554527',
                    heure:'13:16'
                },
                 {
                    id:'8',
                    nom:'Erika Monique',
                    typeContact:'Mobile',
                    image:'../static/img/img_avatar2.png',
                    numero:'673554527',
                    heure:'12:16'
                },
               
            ]
        }
    },
    methods:{
       person: function(){
           //var personId = this.$f7route.id;
       }
       
    }
}
</script>

<style scoped>
img.radius-img{
    border-radius:50%;
}
</style>
