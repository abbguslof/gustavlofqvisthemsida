<template>
<div>
    <img :src="item.image" alt="simning image" class="h-80 w-64 object-cover border-4" >
    <h3 class="font-semibold hover:underline">{{item.title}} | <span class="text-sm font-light"> {{item.date}} </span> </h3>
    <p>{{item.description}}</p>
</div>
</template>

<script>
export default {
    props:['item'],
    data() {
        return {

        }
    }
}
</script>