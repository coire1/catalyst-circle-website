<template>
  <header class="site-header">
    <div class="pagewidth">
      <div class="logo">
        <img :src="$withBase(`images/catalyst.png`)" alt="Project Catalyst" />
      </div>
      <div class="nav-wrapper">
        <nav>
          <ul>
            <li v-for="item in $frontmatter.menu">
              <a :href="item.link">{{item.title}}</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<style lang="scss">
@import '../styles/variables';

header.site-header {
  position: fixed;
  background: $dark-blue;
  width: 100%;
  z-index: 100;
  height: 100px;
  .pagewidth {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 0;
    .logo {
      img {
        width: auto;
        height: 60px;
      }
    }
    .nav-wrapper {
      nav {
        ul {
          display: flex;
          li {
            &:not(:last-child) {
              margin-right: 30px;
            }
            a, a:visited {
              color: $white;
              font-weight: 700;
              &:hover {
                text-decoration: underline;
              }
            }
          }
        }
      }
    }
  }
}
</style>
