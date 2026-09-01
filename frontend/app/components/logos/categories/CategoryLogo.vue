<script lang="ts" setup>
import { Category } from "#shared/types/backend";

withDefaults(
  defineProps<{
    category: Category;
    size?: number;
  }>(),
  {
    size: 72,
  }
);
</script>
<template>
  <icon-mdi-shield-crown v-if="category === Category.OfficialPlugins" v-bind="$attrs" :width="size" :height="size" />
  <icon-mdi-paw v-else-if="category === Category.Ability" v-bind="$attrs" :width="size" :height="size" />
  <icon-mdi-puzzle v-else-if="category === Category.SidePlugin" v-bind="$attrs" :width="size" :height="size" />
  <icon-mdi-file-document-multiple v-else-if="category === Category.AbilityPack" v-bind="$attrs" :width="size" :height="size" />
  <icon-mdi-package-variant-closed v-else-if="category === Category.DataPack" v-bind="$attrs" :width="size" :height="size" />
  <icon-mdi-texture-box v-else-if="category === Category.ResourcePack" v-bind="$attrs" :width="size" :height="size" />
  <icon-mdi-earth v-else-if="category === Category.WorldBuild" v-bind="$attrs" :width="size" :height="size" />
  <icon-mdi-cog v-else-if="category === Category.ConfigFile" v-bind="$attrs" :width="size" :height="size" />
  <icon-mdi-help-box v-else-if="category === Category.Other" v-bind="$attrs" :width="size" :height="size" />
</template>
