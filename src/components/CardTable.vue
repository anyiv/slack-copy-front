<template>
<div>
    <div class="card cards-blue">
        <div class="card-header">
            <div class="card-header-title ingress-title is-centered"> {{ title }}</div>
        </div>
        <div class="card-content">
            <b-table :data=data :columns=columns></b-table>
        </div>
    </div>
</div>
    
</template>

<script>
export default {
    name: 'CardTable',
    props: [ "title", "data", "columns"],
    data() {
            return {
                
            }
        }
}
</script>

<style scoped>
.list-card{
    margin-top: 2em;
    margin-bottom: 2em;
    border-style: solid;
    border-color: #E3A9A5;
}


.margin{
    margin-top: 2em;
    margin-right: 2em;
    margin-bottom: 2em;
    margin-left: 2em;
}

.side-margin{
    margin-left: 1em;
    margin-right: 1em;
}

.list-title{
    font-size: 1.5em;
}

.cards-blue{
    background-color: #D5E5E2;
    margin-top: 2em;
}
</style>