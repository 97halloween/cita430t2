<template>
  <nav class="uk-navbar-container uk-margin" uk-navbar>
    <div class="uk-navbar-center">

        <div class="uk-navbar-center-left">
          <div>
            <ul class="uk-navbar-nav">
              <router-link
               v-for="link in Links"
               :key="link.url"
               :to="link.url"
               :exact="link.exact"
               active-class="uk-active"
               tag="li"
               >
                <a href="#">{{link.name}}</a>
              </router-link>
            </ul>
        </div>
      </div>
      <!-- <router-link
      class="uk-navbar-item uk-logo"
      tag="a"
      to="/"
      >
      Team 1
      </router-link> -->
        <div class="uk-navbar-center-right">
          <div>
          <ul class="uk-navbar-nav">
            <li
             v-for="icon in Icons"
             :key="icon.url"
             >
              <a :href="icon.url" :uk-icon="icon.name" target="_blank"></a>
            </li>
          </ul>
        </div>
      </div>

    </div>
</nav>

</template>

<script>
  export default {
    data: () => ({
      Links: [
        {name: "home", url: "/", exact: true},
        {name: "about", url: "/about"}
      ],
      Icons: [
        {name: "icon: youtube", url: "https://www.youtube.com/watch?v=dQw4w9WgXcQ"},
        {name: "icon: instagram", url: "https://www.instagram.com/p/B25sLqSh834/"},
        {name: "icon: reddit", url: "https://www.youtube.com/watch?v=dQw4w9WgXcQ"},
        {name: "icon: facebook", url: "https://www.youtube.com/watch?v=dQw4w9WgXcQ"}
      ]
    })
  }
</script>
