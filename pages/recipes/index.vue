<template>
    <section class="recipes">
             <Recipe
             v-for="recipe in recipes"
             :key="recipe.id"
             :humbnail= "recipe.thumbnail"
             :title="recipe.title"
             :id="recipe.id"
             :previewText="recipe.previewText" />
             <Recipe
             :thumbnail= "recipe.thumbnail"
             :title="recipe.title"
             :id="recipe.id"
             :previewText="recipe.previewText" />

            <div class="thumbnail" style="background-image: url(https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQBCFzE28rH8avelfjheWIXKZf7_mewoU6aj6uEeeTcqcg2tXvc)"></div>
            <h1>Keto Foods</h1>
            <p>So… it’s super duper common for this dish to be served appetizer-style with a mountain of tortilla chips or a fresh fluffy baguette</p>
    </section>
</template>

<script>
import Recipe from '@/components/Recipe'
export default {
    components: {
        Recipe
    },
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
            ]
            })
        }, 1500)
        })
    }
 
}
</script>

<style scoped>
.recipes{
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-content: center;

}

</style>