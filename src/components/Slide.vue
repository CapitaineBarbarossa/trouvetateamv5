<template>
    <div v-if="id === 1" class="carousel-item active">
        <img :src="require(`@/assets/${image}`)" class="d-block w-100" alt="...">
        <div class="carousel-caption d-none d-md-block">
        </div>
    </div>
    <div v-else class="carousel-item">
        <img :src="require(`@/assets/${image}`)" class="d-block w-100" alt="...">
        <div class="carousel-caption d-none d-md-block">
        </div>
    </div>
</template>

<script>
export default {
  name: 'Slides',
  props: {
    id: Number,
    titre:String,
    image:String,
  }
}
</script>