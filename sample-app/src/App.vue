<template>
  <div id="app">


    aaa
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>

    <wj-flex-grid :itemsSource="gridData">
        <wj-flex-grid-column header="ID" binding="id" :width="60"></wj-flex-grid-column>
        <wj-flex-grid-column header="商品名" binding="product" :width="200"></wj-flex-grid-column>
        <wj-flex-grid-column header="受注日" binding="date" :width="120"></wj-flex-grid-column>
        <wj-flex-grid-column header="金額" binding="amount" :width="100" format="c"></wj-flex-grid-column>
    </wj-flex-grid>

  </div>
</template>

<script>
   

    import '@grapecity/wijmo.vue2.grid';
    import '@grapecity/wijmo.cultures/wijmo.culture.ja';
    import '@grapecity/wijmo.styles/wijmo.css';
    export default {
        name: 'app',
        data: function () {
            return {
                gridData: [
                    { id: 15, product: 'ピュアデミグラスソース', date: '2017/01/10', amount: 6000 },
                    { id: 17, product: 'だしこんぶ', date: '2017/01/08', amount: 14500 },
                    { id: 18, product: 'ピリカラタバスコ', date: '2017/01/12', amount: 4000 },
                    { id: 84, product: 'なまわさび', date: '2017/01/21', amount: 8000 }
                ]
            }
        },
        components: {
        }
    }

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
