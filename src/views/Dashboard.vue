<template>
    <div class="columns margin">
         <div class="column">
            <div class="container block">
                <div class="columns">
                    <div class="column is-one-quarter block"  v-for="item in servicesPlanList" :key="item.id">
                        <cards :title=item.name :price=item.price :description=item.description 
                                :benefits=item.benefits />
                    </div>
                </div>
            </div>
            <br>
            <div class="title">You're in good company</div>
            <div class="container block">
                <div class="columns">
                    <div class="column is-one-quarter block"  v-for="item in clientsList" :key="item.id">
                        <client-card :name=item.name :description=item.description 
                                :url=item.url />
                    </div>
                </div>
            </div> 
        </div>
    </div>
</template>


<script>
import axios from 'axios';
import Cards from '@/components/PlanCard.vue'
import ClientCard from '@/components/ClientCard.vue'
export default{
    name: 'Dashboard',
    props: [],
    components:{
        Cards,
        ClientCard
    },
    data() {
        return {
            servicesPlanList: [],
            clientsList: []
        }

    },
    async mounted() {
    await this.getClients()
    await this.getServicesPlan()
    },
    methods:{
        async getServicesPlan(){
            try {
                await axios.get("https://slack-copy-back.herokuapp.com/service_plans")
                .then(response=>{
                    this.servicesPlanList = response.data
                })
            } catch (error) {
                console.log(error)
            }
        },
        
        async getClients(){
            try {
                await axios.get("https://slack-copy-back.herokuapp.com/clients")
                .then(response=>{
                    this.clientsList = response.data
                })
            } catch (error) {
                console.log(error)
            }
        },
        open() {
                const loadingComponent = this.$buefy.loading.open({
                    container: this.isFullPage ? null : this.$refs.element.$el
                })
                setTimeout(() => loadingComponent.close(),4 * 1000)
            }
    }
}
</script>

<style scoped>
.margin{
    margin-top: 2em;
    margin-right: 2em;
    margin-bottom: 2em;
    margin-left: 2em;
}

/* nuevos css */
.container{
    background-color: #fefefe;
    width: 100%;
}

</style>
