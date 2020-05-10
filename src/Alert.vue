<template>
    <div>
        <transition name="fade">
        <div class="ui message success" v-if="visible">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Qui quis nesciunt repellat architecto? Labore praesentium quidem esse incidunt voluptatum! Aut sapiente beatae quisquam itaque natus voluptatum aliquid commodi temporibus alias.
        </div>
          </transition>
        <button @click="toggle">Toggle</button>
      
    </div>
</template>

<script>
export default {
    data() {
        return {
            visible: true
        }
    },
    methods: {
        toggle: function() {
            this.visible = !this.visible
        }
    }
}
</script>
<style>
    .fade-enter-active, .fade-leave-active {
        transition: opacity 1s, transform 1s; 
    }
    .fade-enter, .fade-leave-active {
        opacity: 0;
        transform: translateX(20px);
    }
</style>





