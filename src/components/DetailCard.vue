 <script>
 export default {
   props: {
    card: Object
   } 
 }
 </script>
 <template lang="">
    <div class="col-20" >
        <div class="card">
            <img :src="card.card_images[0].image_url" />
            <div class="card-body">
                <h3>{{card.name}}</h3>
            </div>
        </div>
    </div>
 </template>
 <style lang="scss" scoped>
 .card {
    background-color: #fff;
    margin: 10px;
    padding: 10px;
    
    
    img {
        max-width: 100%;
    }
}
 </style>
