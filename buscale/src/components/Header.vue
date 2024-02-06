<template>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
            <RouterLink to="/" class="navbar-brand">Buscale</RouterLink>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <RouterLink to="/" class="nav-link" :class="{ 'active': isActive('/') }">Início</RouterLink>
                    </li>
                    <li class="nav-item">
                        <RouterLink to="/product" class="nav-link" :class="{ 'active': isActive('/product') }">Produto</RouterLink>
                    </li>
                    <li class="nav-item">
                        <RouterLink to="/about" class="nav-link" :class="{ 'active': isActive('/about') }">Sobre</RouterLink>
                    </li>
                </ul>
                <form class="d-flex" role="search">
                    <input class="form-control me-2" type="Pesquisar" placeholder="Pesquisar" aria-label="Pesquisar">
                    <button class="btn btn-outline-secondary" type="submit">Pesquisar</button>
                </form>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
  methods: {
    isActive(route) {
      return this.$route.path === route;
    }
  }
}
</script>
