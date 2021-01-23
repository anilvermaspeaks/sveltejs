<script>
  export let meet;
  console.log(meet);
</script>

<article class="meetupItem">
  <header>
    <h3>{meet?.title}</h3>
    <h4>{meet?.subtitle}</h4>
  </header>
  <div class="content">
    <img src="https://picsum.photos/300/200" alt="" />
    <p>{meet?.description}</p>
  </div>
  <footer>
    <a href="mailto:{meet?.email}">Mail</a>
    <button>Show Details</button>
    <button>Favorite</button>
  </footer>
</article>

<style>
  .meetupItem {
    background-color: #fff;
    padding: 15px;
    border-radius: 6px;
  }
</style>
