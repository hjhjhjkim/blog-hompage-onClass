<script>
  import { Link } from "svelte-routing";
</script>

<style lang="scss">
  @import "../scss/_definition.scss";
  .container {
    width: 100%;
    min-height: 100%;
    @include custom-flex(center, center);
    p {
      font-size: 124px;
      font-weight: 900;
    }
  }
</style>

<div class="container">
  <p>메인페이지</p>
  <ul>
    <li>
      <Link to="/list">LIST</Link>
    </li>
    <li>
      <Link to="/detail">DETAIL</Link>
    </li>
    <li>
      <Link to="/write">WRITE</Link>
    </li>
  </ul>
</div>
