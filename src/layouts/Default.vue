<template>
  <div class="layout">
    <header class="header">
      <nav class="nav"></nav>
    </header>
    <slot />
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<style>

</style>
