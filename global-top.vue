<template>
  <div
    class="deck-progress"
    :style="{ width: ($slidev.nav.total > 1 ? ($slidev.nav.currentPage - 1) / ($slidev.nav.total - 1) * 100 : 0) + '%' }"
  />
  <div v-if="$slidev.nav.currentPage > 1" class="deck-counter">
    {{ String($slidev.nav.currentPage).padStart(2, '0') }} / {{ String($slidev.nav.total).padStart(2, '0') }}
  </div>
</template>

<style scoped>
.deck-progress {
  position: fixed; top: 0; left: 0; height: 3px;
  background: var(--teal, #0F9B9B); z-index: 200;
  transition: width .5s cubic-bezier(.22, 1, .36, 1);
  border-radius: 0 2px 2px 0;
}
.deck-counter {
  position: fixed; top: 1.1rem; right: 1.4rem;
  font-size: .8rem; font-weight: 600;
  color: var(--ink-muted, #8A8E96); z-index: 200;
  font-variant-numeric: tabular-nums;
}
</style>
