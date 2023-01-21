<template>
    <nav :class="[{'side-nav': 'default', open: opened, closed: !opened }]">

        <button @click="closeSideNav()">
            <i class="fa-solid fa-bars"></i>
        </button>


        <div class="company">
            <div class="logo">
                <p>image</p>
            </div>

            <h3>
                Caesar's Corporation
            </h3>
        </div>

        <Departments></Departments>
        <Projects></Projects>

        <span>
            <a href="#">
                   Leaves
            </a>
              <i class="fa-solid fa-person"></i>
        </span>

        <span>
            <a href="#">
                People
            </a>
              <i class="fa-solid fa-people-group"></i>
        </span>

        <span>
            <a href="#">
               My Account
            </a>
             <i class="fa-solid fa-circle-user"></i>
        </span>

        <span>
            <a href="#">
                Settings
            </a>
            <i class="fa-solid fa-gear"></i>
        </span>


    </nav>

</template>

<script>
import Departments from "./Departments.vue";
import Projects from "./Projects.vue";
export default {
    name: "SideNavigation",
    components: {Projects, Departments},
    data(){
        return{
           opened: true,
        }
    },

    methods:{
        closeSideNav(){
            this.opened = !this.opened
        }
    }
}
</script>

<style scoped>
.side-nav{
    background-color: darkblue;
    height: 100vh;
}

.open{
    max-width: 20%;
}

.closed{
    max-width: 2%;
}

.closed span a{
    display: none;
    visibility: hidden;
}

.closed span .fa-plus{
    display: none;
    visibility: hidden;
}
.closed ul li{
    display: none;
    visibility: hidden;
}

.side-nav span{
    display: block;
    font-family: Roboto,sans-serif;
    color: #fff;
}

.side-nav ul li{
    font-family: Roboto,sans-serif;
    list-style-type: none;
    color: #fff;
}

.side-nav .company h3{
    color: #fff;
}
</style>
