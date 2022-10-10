<template>
    <b-navbar class="color">
        <template #brand>
            <b-navbar-item >
                <img class="sizes"
                    src="https://i.imgur.com/HJMecvu.png"
                    alt="Some logo i guess"
                >
            </b-navbar-item>
        </template>
        <template #start>
            <b-navbar-dropdown label="Products">
                <b-navbar-item href="#">
                    Functions
                </b-navbar-item>
                <b-navbar-item href="#">
                    Canals
                </b-navbar-item>
            </b-navbar-dropdown>
            <b-navbar-item href="#">
                Solutions
            </b-navbar-item>
            <b-navbar-item href="#">
                Enterprice
            </b-navbar-item>
            <b-navbar-item href="#">
                Resources
            </b-navbar-item>
            <b-navbar-item href="#">
                Pricing
            </b-navbar-item>
        </template>

        <template #end>
             <b-navbar-item href="#">
                <b-icon
                    icon="Search"
                    size="is-small">
                </b-icon>
            </b-navbar-item>
            <b-navbar-item href="#">
                Sign in
            </b-navbar-item>
            <b-navbar-item tag="div">
                <div class="buttons">
                    <a class="button outlined">
                        TALK TO SALES
                    </a>
                    <a class="button button-color">
                        <strong>TRY FOR FREES</strong>
                    </a>
                </div>
            </b-navbar-item>
        </template>
    </b-navbar>
</template>

<script>

export default {
    name: 'TopBar'
}
</script>

<style scoped>
.button-color{
    background-color: #67236F;
    color: #fefefe;
}
.sizes{
    height: 150px;
    width: 150px;
}
.color{
  background-color: #F9F0FA;
}
</style>