/* eslint-disable */
<template>
     <button @click="toggle">
    {{label}}
    </button>
      <div class="columns">
        <transition name="collapse" mode="in-out">
          <div v-if="view" class="column">
            <slot>

            </slot>
          </div>
        </transition>
      </div>
  </template>

<script setup lang="ts">
  import { defineEmits } from 'vue'
  defineProps({
    view:{
      type:Boolean,
      default:false,
      required:true
    },
    label:{
      type:String,
      default:'',
    }
  })
       
    const emit = defineEmits(['toggle'])

       const toggle = () => {
          emit('toggle')
       
        }
    </script>
    
    <style lang="scss" scoped>
    
    
  
    
    .column {
      overflow:hidden;
      transition:flex 0.5s ease-out; 
      height:auto;
      flex:1;
      background-color: transparent;
    
     
    }
    
    .collapse {
      &-enter,
      &-leave-to {
        flex: 0;
      }
    }
    </style>