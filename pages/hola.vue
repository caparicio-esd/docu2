<template>
  <NotionRenderer :blockMap="blockMap" />
</template>

<script>
import { notionRouterId } from "./../content/notion-router";
const routeName = "hola";

export default {
  async asyncData({ $notion }) {
    const blockMap = await $notion.getPageBlocks(notionRouterId(routeName));
    return { blockMap };
  },
};
</script>

<style>
/* @import "vue-notion/src/styles.css"; */
</style>