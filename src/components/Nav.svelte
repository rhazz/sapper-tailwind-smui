<script>
  export let segment;
</script>

<style type="text/scss">
  nav {
    border-bottom: 1px solid rgba(255, 62, 0, 0.1) !important;
    font-weight: 300 !important;
    padding: 0 1em !important;
  }

  ul {
    margin: 0 !important;
    padding: 0 !important;
  }

  /* clearfix */
  ul::after {
    content: "";
    display: block;
    clear: both;
  }

  li {
    display: block;
    float: left;
  }

  [aria-current] {
    position: relative;
    display: inline-block;
  }

  [aria-current]::after {
    position: absolute;
    content: "";
    width: calc(100% - 1em);
    height: 2px;
    background-color: rgb(255, 62, 0);
    display: block;
    bottom: -1px;
  }

  a {
    text-decoration: none;
    padding: 1em 0.5em;
    display: block;
  }
</style>

<nav>
  <ul>
    <li>
      <a aria-current={segment === undefined ? 'page' : undefined} href=".">
        home
      </a>
    </li>
    <li>
      <a aria-current={segment === 'about' ? 'page' : undefined} href="about">
        about
      </a>
    </li>

    <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
    <li>
      <a
        rel="prefetch"
        aria-current={segment === 'blog' ? 'page' : undefined}
        href="blog">
        blog
      </a>
    </li>
    <li>
      <a
        rel="prefetch"
        aria-current={segment === 'smui' ? 'page' : undefined}
        href="smui">
        smui exemplo
      </a>
    </li>
  </ul>
</nav>
