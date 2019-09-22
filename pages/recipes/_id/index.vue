<template>
   <section class="single-recipe">
       <h1>{{ $route.params.id }}</h1>
       <div>
           <img src="" alt="">
       </div>
       <p>The recipe description</p>
   </section>
</template> 

<script>
export default {
    asyncData() {
        return new promise(resolve, reject) => {
            setTimeout(() => {
                resolve ({
                recipes: [
                    {
                    id: "1",
                    title: "Keto Pizza",
                    previewText: "Awesome Pizza",
                    thumbnail= "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQBCFzE28rH8avelfjheWIXKZf7_mewoU6aj6uEeeTcqcg2tXvc"                 }]
            },
                {
                    id: "2",
                    title: "Keto Pizza",
                    previewText: "Awesome Pizza",
                    thumbnail= "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQBCFzE28rH8avelfjheWIXKZf7_mewoU6aj6uEeeTcqcg2tXvc"                 }]
            }
            ].find(el => el.id === context.params.id)
            })
        }, 1500)
        })
    }
 
}
},

</script>

<style scoped>
.single-recipe {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-flow: column;
    padding: 30px;
}

</style>