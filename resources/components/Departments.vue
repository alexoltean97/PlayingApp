<template>
    <div class="departments">
        <span>
              <i @click="listTrigger()" v-if="opened" class="fa-solid fa-minus"></i>
              <i @click="listTrigger()" v-else class="fa-solid fa-plus"></i>
                <a href="#">
                     Departments
                </a>
            <i class="fa-solid fa-diagram-project"></i>
        </span>

        <ul :class="[{open: opened, close: !opened}]">
            <li><a href="#">It </a></li>
            <li><a href="#">Human Resources</a></li>
            <li><a href="#">Public Relations</a></li>
            <li><a href="#">Whatever</a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "Projects",
    data(){
        return{
            opened:true
        }
    },
    methods:{
        listTrigger(){
            this.opened = !this.opened
        }
    }
}
</script>

<style scoped>
span{
    display: block;
    font-family: Roboto,sans-serif;
    color: #fff;
}

.open{
    display: block;
}

.close{
    display: none;
    visibility: hidden;
}

</style>
