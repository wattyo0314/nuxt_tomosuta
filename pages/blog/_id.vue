<template>
  <div>
    <h2>blog detail</h2>
    <p>これは{{ $route.params.id }}のエントリーです。</p>
  </div>
</template>

<script>
export default {
  validate({ params }) {
    return /^\d+$/.test(params.id);
  }
};
</script>
