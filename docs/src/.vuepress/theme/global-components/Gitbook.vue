<template>
  <div class="gitbook-links">
    <div class="single-link" v-for="glink,idx in $frontmatter.gitbook">
      <a :href="glink.link" target="_blank">
        {{glink.title}}
      </a>
    </div>
  </div>
</template>

<style lang="scss">
@import '../styles/variables';

.gitbook-links {
  width: 35%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  .single-link {
    padding: 10px 30px;
    background: $dark-blue;
    border-radius: 30px;
    border: 2px solid $dark-blue;
    a, a:visited {
      color: $white;
      font-weight: 700;
      font-size: 28px;
    }
    &:hover {
      background: $white;
      a, a:visited {
        color: $dark-blue;
      }
    }
  }
}
</style>
