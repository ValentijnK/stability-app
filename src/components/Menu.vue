<template>
  <div id="nav" class="wrapper">
    <!-- Sidebar  -->
    <nav id="sidebar">
        <div class="sidebar-header">
            <h3>Ship Stability Calculator</h3>
        </div>
        <ul class="nav flex-column">
            <li class="nav-item">
                <router-link class="nav-link active" to="/momentenstelling">Momentenstelling</router-link>
            </li>
            <li class="nav-item">
                <router-link class="nav-link active" to="/about">Grain curve</router-link>
            </li>
            <li class="nav-item">
                <router-link class="nav-link active" to="/">Lifting and cranes</router-link>
            </li>
            <li class="nav-item">
                <router-link class="nav-link active" to="/hold-calculations">Hold Calculations</router-link>
            </li>
            <li class="nav-item">
              <a class="nav-link disabled">Disabled</a>
            </li>
          </ul>
    </nav>
</div>
</template>

<script>
export default {
  name: 'Menu',
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrapper {
    display: flex;
    align-items: stretch;
}

#sidebar {
    min-width: 250px;
    max-width: 250px;
    min-height: 100vh;
    background: #7386D5;
    color: #fff;
    transition: all 0.3s;
    text-align: center;
}

#sidebar .sidebar-header {
    padding: 20px;
    background: #6d7fcc;
}

#sidebar ul.components {
    padding: 20px 0;
    border-bottom: 1px solid #47748b;
}

#sidebar ul p {
    color: #fff;
    padding: 10px;
}

#sidebar ul li a {
    padding: 10px;
    font-size: 1.1em;
    display: block;
}
#sidebar ul li a:hover {
    color: #7386D5;
    background: #fff;
}

#sidebar ul li.active > a, a[aria-expanded="true"] {
    color: #fff;
    background: #6d7fcc;
}

ul ul a {
    font-size: 0.9em !important;
    padding-left: 30px !important;
    background: #6d7fcc;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #fff;
}
</style>
