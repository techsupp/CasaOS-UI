<!--
 * @Author: JerryK
 * @Date: 2021-11-10 17:50:18
 * @LastEditors: Jerryk jerry@icewhale.org
 * @LastEditTime: 2022-07-14 10:48:52
 * @Description:
 * @FilePath: \CasaOS-UI\src\components\CoreService.vue
-->
<template>
  <div class=" home-section has-text-left mt-1 mb-2rem">
    <div class="columns is-variable is-2 is-multiline suggestion-list">
      <template v-if="!isLoading">
        <Sync-block></Sync-block>
        <smart-block></smart-block>
      </template>
      <b-loading v-model="isLoading" :is-full-page="false"></b-loading>
    </div>
  </div>

</template>

<script>
import SmartBlock from './smartHome/SmartBlock.vue'
import SyncBlock from './syncthing/SyncBlock.vue'
import StorageBlock from "@/components/Storage/StorageBlock";

export default {
  components: {SyncBlock, SmartBlock, StorageBlock},
  name: "core-service",
  data() {
    return {
      isLoading: false,
    }
  },

}
</script>

<style>

</style>
