<script>
  export let segment;
</script>

<style type="text/css">
  /* [aria-current] {
    position: relative;
    display: inline-block;
  } */
  /* 
  [aria-current]::after {
    position: absolute;
    content: "";
    width: calc(100% - 1em);
    height: 2px;
    display: block;
    bottom: -1px;
  } */
</style>

<nav>
  <div class="navigation">
    <a
      class="navItem"
      aria-current={segment === undefined ? 'page' : undefined}
      href=".">
      Home
    </a>

    <a
      class="navItem"
      aria-current={segment === 'stories' ? 'page' : undefined}
      target="_blank"
      href="https://shortstoriesbynidhi.home.blog/">
      Reader's Delight
    </a>

    <a
      class="navItem"
      aria-current={segment === 'cook' ? 'page' : undefined}
      target="_blank"
      href="https://vegetarianhealthy.food.blog/">
      Cook Book
    </a>

    <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->

    <a
      class="navItem"
      aria-current={segment === 'calculators' ? 'page' : undefined}
      href="calculator">
      Financial Calculators
    </a>
  </div>
</nav>
