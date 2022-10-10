<template>
    <div class="card transparent">
        <!-- <div class="card-header">
        </div> -->
        <div class="card-content">
            <h1 class="title"> {{title}}</h1>
            <h6 class="subtitle is-6">{{description}}</h6>
            <div class="price" v-if="title == 'Free'" > $0 USD /mo</div>
            <div class="price" v-else-if="title == 'Enterprise Grid'" ><br/> </div>
            <div class="price" v-else > ${{price}}USD /mo</div>
            <div class="buttons">
                <b-button size="is-medium" class="button-color"  expanded>GER STARTED</b-button>
            </div>
            <div v-for="item in benefits" :key=item.id>
                
                <p><b-icon
                    icon="check"
                    size="is-small">
                </b-icon> {{item.description}} </p>
            </div>
            <br>
            <a href="" class="center">Learn more</a>
        </div>
    </div>
</template>

<script>

export default{
    name: 'Cards',
    props: [ 'title', 'description', 'price', 'benefits'],
    data() {
            return {
               
            }
        }
}
</script>

<style scoped>
.button-color{
    background-color: #67236F;
    color: #fefefe;
}

.title{
    margin-top: 5%;
    font-size: 1.5em;
    font-weight: 700;
    text-align: left;
}

.center{
    align-content: center;
    text-align: center;
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
