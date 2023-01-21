<template>
    <section class="forms-modal">
        <div class="container">
            <div class="row">
<!--                <div class="col-md-4">-->
<!--                    <Login></Login>-->
<!--                </div>-->

<!--                <div class="col-md-4">-->
<!--                    <CompanyLogin></CompanyLogin>-->
<!--                </div>-->

                <div class="col-md-4">
                    <RegisterMain></RegisterMain>
                </div>

            </div>
        </div>
    </section>

<!--<side-navigation></side-navigation>-->



</template>

<script>
// import CompanyLogin from "./components/Forms/CompanyLogin.vue";
// import Login from "./components/Forms/Login.vue";
import SideNavigation from "./components/SideNavigation.vue";
import RegisterMain from "./components/Forms/RegisterMain.vue";
export default {
    name: "App.vue",
    components:{
        RegisterMain
    }
}
</script>

