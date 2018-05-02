<template>
  <div class="body">
    <header class="header">
      <div class="container">
        Header
      </div>
    </header>

    <div class="content">
      <div class="container">
        <main id="main">

        <nuxt/>

        </main>
        <aside class="right-sidebar">
          right
        </aside>
      </div>
    </div>

    <footer class="footer">
      <div class="container">
        Footer
      </div>
    </footer>
  </div>
</template>

<style lang="scss">

  @mixin grid($col) {
    padding: 0 15px;
    float: left;
    
    @if $col == 1 {
      width: 8.33333333333%;
    } @else if $col == 2{
      width: 16.6666666667%;
    }@else if $col == 3{
      width: 25%;
    }@else if $col == 4{
      width: 33.3333333333%;
    }@else if $col == 5{
      width: 41.6666666667%;
    }@else if $col == 6{
      width: 50%;
    }@else if $col == 7{
      width: 58.3333333333%;
    }@else if $col == 8{
      width: 66.6666666666%;
    }@else if $col == 9{
      width: 75%;
    }@else if $col == 10{
      width: 83.3333333333%;
    }@else if $col == 11{
      width: 91.6666666666%;
    } @else if $col == 12 {
      width: 100%;
    }
  
  }
  $footerBg: rgb(34, 34, 34);
  $colorLink: rgb(34, 34, 34);
  $colorLinkHover: rgb(127, 63, 129);

  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  html,
  .body {
    margin: 0;
    padding: 0;
    height: 100%;
    color: #121E27;
    font-size: 13px;
    font-family: 'Open Sans', sans-serif;
  }
  body{
    margin: 0;
    padding: 0;
  }
  html {
    margin: 0;
    padding: 0;
    line-height: normal;
  }

  i[class*="ico-"] {
    display: inline-block;
    vertical-align: middle;
    //background: url("../images/sprite.png");
  }

  i.ico-time {
    width: 15px;
    height: 15px;
    background-position: 0 0;
  }

a {
  cursor: pointer;
  color: $colorLink;
}

.clearfix::after {
  content: '';
  display: table;
  clear: both;
}

.container {
  max-width: 73.125em;
  min-width: 15.000em;
  margin: 0 auto;
}

.body {
  display: table;
  height: 100vh;
  width: 100%;
}
.content {
  display: table-row;
  height: 100%;
}

  ul li{
    list-style: none;
  }
  h1{
    font-size: 20px;
  }
  h2{
    font-size: 18px; 
  }
  h3{
    font-size: 16px;
  }
  h4{
    font-size: 15px;
  }

  .footer{
    margin-top: 20px;
    background-color: $footerBg;
  }

.header{
  margin-bottom: 20px;
  background-color: #957aad;
   -webkit-box-shadow: 0 2px 2px 0 rgba(0,0,0,0.14), 0 1px 5px 0 rgba(0,0,0,0.12), 0 3px 1px -2px rgba(0,0,0,0.2);
    box-shadow: 0 2px 2px 0 rgba(0,0,0,0.14), 0 1px 5px 0 rgba(0,0,0,0.12), 0 3px 1px -2px rgba(0,0,0,0.2);
}

#main{
  height: 100%;
  outline: 1px solid #222;
  @include grid(8);
}

.right-sidebar{
  @include grid(4);
  background: #fff;
  border: 1px solid #d7d7d7;
}
</style>
