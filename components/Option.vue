<script setup lang="ts">
import { Gender, Popularity, Length } from "~~/data";

interface OptionProps {
  option: {
    title: string;
    categorie: string;
    buttons: Gender[] | Popularity[] | Length[];
  };
  options: {
    gender: Gender;
    popularity: Popularity;
    length: Length;
  };
}

const props = defineProps<OptionProps>();
</script>

<template>
  <div class="option-container">
    <h4>{{ option.title }}</h4>
    <div class="option-buttons">
      <button
        v-for="value in option.buttons"
        :key="value"
        :class="options[option.categorie] === value && 'option-active'"
        class="option option-left"
        @click="options[option.categorie] = value"
      >
        {{ value }}
      </button>
    </div>
  </div>
</template>
