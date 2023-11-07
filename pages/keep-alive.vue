<template>
  <div class="keep-alive">
    <div>
      <button @click="handleVisibleCheckboxChange">ChangeComponent</button>
      <component :is="isActiveComponent" />
    </div>
    <div>
      <button @click="handleVisibleCheckboxChange">
        ChangeComponent && keep-alive
      </button>
      <keep-alive>
        <component :is="isActiveComponent" />
      </keep-alive>
    </div>
  </div>
</template>

<script setup lang="ts">
import UiCheckbox from "../components/ui/UiCheckbox.vue";
import UiInput from "../components/ui/UiInput.vue";

const isVisibleCheckbox = ref(true);

const isActiveComponent = computed(() => {
  if (isVisibleCheckbox.value) return UiCheckbox;

  return UiInput;
});
const handleVisibleCheckboxChange = () => {
  isVisibleCheckbox.value = !isVisibleCheckbox.value;
};
</script>

<style scoped lang="scss">
.keep-alive {
  margin-top: 20px;
  display: flex;
  justify-content: space-around;
}
</style>
