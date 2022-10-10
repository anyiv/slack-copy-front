<template>
    <div class="card transparent">
    <div class="card-image">
        <figure class="image is-4by3">
        <img :src='url'/>
        </figure>
    </div>
    <div class="card-content">
        <div class="media">
            <div class="media-content">
                <p class="title is-4">{{name}}</p>
            </div>
        </div>

        <div class="content">
        {{description}}
        <br>

        </div>
    </div>
    </div>
</template>

<script>

export default{
    name: 'ClientCard',
    props: [ 'name', 'url', 'description'],
    data() {
            return {
               
            }
        }
}
</script>

<style scoped>

.title{
    margin-top: 5%;
    font-size: 1.5em;
    font-weight: 700;
    text-align: left;
}

.description{
    text-align: left;
}

.price{
    font-size: 1.5em;
    font-weight: 600;
    text-align: center;
}  

.transparent{
    max-width: 100%;
    background-color: transparent;
}
</style>
