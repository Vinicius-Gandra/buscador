<template>
  <nav
    class="navbar navbar-expand-md navbar-light fixed-top navbar-transparente">
    <div class="container">
        <div class="collapse navbar-collapse">
            <ul class="navbar-nav ml-auto nav nav-pills">
                <li v-for="rota in rotas" :key="rota">
                  
                    <router-link class="nav-link" :to="rota.path ? rota.path : '/'"> {{rota.titulo}}
                    </router-link>
                </li>
            </ul>
        </div>
    </div>
  </nav>
</template>


<script>
export default {
  props: {
    rotas: {
      type: Array,
      required: true,
    },
  },
};
</script>    

<style scoped>

nav.navbar-transparente {
    padding: 15px 0px;
    background: rgba(0,0,0,0.6);
}
.navbar-light .navbar-nav .nav-link {
    color: white;
}

.navbar-light .navbar-nav .nav-link:hover {
    color: #71c9ee;
}


.navbar-light .navbar-toggler {
    color: rgba(0,0,0,.5);
    border-color: rgba(255,255,255,0.7);
}

</style>