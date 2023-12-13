<template>
  <header class="container-fluid  parallax parallax-img bg-danger-subtle">
  <nav class="navbar navbar-expand-md bg-danger-subtle">
      <div class="container-fluid py-2" >
          <ul class="navbar-nav"id="navBar" >
              <li class="nav-item">
                  <a class="navbar-brand" href="index.html"><img src="https://freepngimg.com/thumb/graphic/53536-5-abstract-shape-free-transparent-image-hq.png" alt="logo" style="width: 40px;" class="rounded-pill"></a>
              <li class="nav-item">
                  <a class="nav-link" href="index.html">Home</a> 
              </li>
              <li class="nav-item">
                  <a class="nav-link" href="#about">About Us</a>
              </li>
              <li class="nav-item">
                  <a class="nav-link" href="#showcase">Showcase</a>
              </li>
              <li class="nav-item">
                  <a class="nav-link" href="#account">Account</a>
              </li>
              <li class="nav-item">
                  <a class="nav-link" href="#contact">Contact Us</a>
              </li>
              
      </div>
  </nav>
</header>

      
</template>

<script>
export default {
  name: 'Comp1',
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body{
  background-color: #E8EDDF;
}
div{
  background-color: #E8EDDF;
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
a:hover {
  background-color: #CFDBD5;
  }
#navBar{
  background-color: #E8EDDF
}
.parallax {
  min-height: 50vh;
  background-attachment: fixed;
  background-size: cover;
  background-position: 50% 50%;

}

.parallax-img {
  background-image: linear-gradient(to bottom, rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url("https://th.bing.com/th/id/OIP.mLKZ5WMBt4318vZPGjIHiwHaE8?rs=1&pid=ImgDetMain");
}

</style>
