<template>
  <hr :style="styleToString(styleDefault)" />
</template>

<script lang="ts" setup>
import { styleToString } from '../utils';
import type { CSSProperties, HTMLAttributes } from 'vue';

interface Props extends Omit<HTMLAttributes, 'style'> {
  style?: CSSProperties;
}

const props = defineProps<Props>();

const styleDefault = {
  width: '100%',
  border: 'none',
  borderTop: '1px solid #eaeaea',
  ...props.style,
};
</script>
