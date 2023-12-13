<template>
  <div class="container my-2 py-2">
    <h1 class="text-center" id="showcase">Showcase</h1>
    <div id="mainCarousel" class="carousel slide" data-bs-ride="carousel">
      <!-- Images from https://www.publicdomainpictures.net/ -->
      <div class="carousel-indicators">
        <button
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide-to="0"
          class="active"
          aria-current="true"
          aria-label="Image 1"
        ></button>
        <button
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide-to="1"
          aria-label="Image 2"
        ></button>
        <button
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide-to="2"
          aria-label="Image 3"
        ></button>
      </div>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img
            src="https://th.bing.com/th/id/R.c88dd4fbd5c12929a3ecc016008be200?rik=98IOO%2fv7GEO53g&riu=http%3a%2f%2fwww.publicdomainpictures.net%2fpictures%2f80000%2fvelka%2fsmall-flowers-in-black-and-white.jpg&ehk=L5e2mYywYnmHgBn1YVddfHvJaouT1rnLnOBKBmc8EFQ%3d&risl=&pid=ImgRaw&r=0"
            class="d-block w-100"
            alt="Lake Landscape Photo"
          />
        </div>
        <div class="carousel-item">
          <img
            src="https://th.bing.com/th/id/R.1665a15269fa8a5103d60a276b55e774?rik=othITY9IluvH%2fA&riu=http%3a%2f%2feskipaper.com%2fimages%2fblack-and-white-flowers-4.jpg&ehk=RFKz0eDxBryY8zhE7TBvv9sCFRgI4wi7TzAnUehzRUA%3d&risl=&pid=ImgRaw&r=0"
            class="d-block w-100"
            alt="Tree Landscape Photo"
          />
        </div>
        <div class="carousel-item">
          <img
            src="https://th.bing.com/th/id/R.1665a15269fa8a5103d60a276b55e774?rik=othITY9IluvH%2fA&riu=http%3a%2f%2feskipaper.com%2fimages%2fblack-and-white-flowers-4.jpg&ehk=RFKz0eDxBryY8zhE7TBvv9sCFRgI4wi7TzAnUehzRUA%3d&risl=&pid=ImgRaw&r=0"
            class="d-block w-100"
            alt="Railroad Landscape Photo"
          />
        </div>
      </div>
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#mainCarousel"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Back</span>
      </button>
      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#mainCarousel"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Comp3',
  props: {
    msg: String,
  },
};
</script>

<style scoped>
body {
  background-color: #e8eddf;
}
div {
  background-color: #e8eddf;
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
img {
  max-width: 100%;
  max-height: 100%;
}
</style>
