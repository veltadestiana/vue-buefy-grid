<template>
  <section class="home">

    <!-- Header -->
    <div class="hero" style="background: #2872C7">
      <div class="hero-body">
        <div class="container has-text-centered">
          <h1 class="title-site is-size-2 ">
            Suche Coupons
          </h1>
          <div class="searchbox" onClick="onClick(event)">
            <input type="search" v-model="search" placeholder="Suchen..." />
            <button>
              <i class="fa fa-search" aria-hidden="true"></i>
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Content -->
    <div class="container">
      <div class="columns is-multiline">
        <div class="column is-one-third" v-for="list in filteredListing">
          <div class="card">
            <div class="card-image">
              <figure class="image">
                <img :src="list.header_img" >
              </figure>
              <div class="ribbon ribbon-top-right"><span>Bis Zu +{{list.upto}}%</span></div>
            </div>
          <div class="card-content">
            <div class="content">
              <p class="title is-size-5 has-text-centered" style="margin: 10px 0 10px 0">{{list.name}}</p>
                <div class="field is-grouped">
                  <p class="control">
                    <span class="button is-rounded is-static list-tags" v-for="(list, tags) in listing">{{list.tags}}</span>
                  </p>
                </div>
            </div>
          </div>
          <a class="button is-info is-fullwidth" style="margin-top: 0; border-radius: 0; letter-spacing: 1px"><strong>See Details →</strong></a>
        </div>
        </div>
      </div>
    </div>

  </section>
</template>

<script>
export default {
  data () {
    return {
      search: '',
      listing: [
        { id: '1', name: 'Amazon Gesusche', header_img: 'https://i.imgur.com/g6fJICX.png', tags: 'Elektronik', upto: '5' },
        { id: '2', name: 'Zalando Gutschein', header_img: 'https://i.imgur.com/FLwrcfD.png', tags: 'Haushalt', upto: '10' },
        { id: '3', name: 'Notebooksbilliger Gutschein', header_img: 'https://i.imgur.com/GeH8BEl.png', tags: 'Bücher', upto: '20' }
      ]};
    },
    computed:
    {
        filteredListing: function()
        {
        	 var self = this;
           return this.listing.filter(function(list){return list.name.toLowerCase().indexOf(self.search.toLowerCase())>=0;});
        }
    }
  }
</script>
