<template>
  <div class="items">
    <div
      v-for="(item, index) in items"
      :key="index"
      class="item"
    >
      <p class="title">{{ item.name }}</p>
      <p class="category">{{ item.category }}</p>
      <p class="price">${{ item.price }}</p>
      <a
        :href="item.url"
        target="_blank"
      >
        View Item
      </a>
      <div
        class="misc"
        v-html="item.misc" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Homepage',
  data () {
    return {
      items: [
        {
          name: 'De Los Muertos Shirt',
          category: 'clothes',
          price: '25.00',
          url: 'https://github.myshopify.com/collections/shirts/products/los-muertos-tee',
          misc: 'Men\'s - Medium'
        },
        {
          name: 'Grim Repo Shirt',
          category: 'clothes',
          price: '25.00',
          url: 'https://github.myshopify.com/collections/shirts/products/grim-repo-tees',
          misc: 'Men\'s - Medium'
        },
        {
          name: 'Recursion by Blake Crouch',
          category: 'audiobooks',
          price: '19.60',
          url: 'https://www.audible.com/pd/Recursion-Audiobook/1984886878',
          misc: ''
        },
        {
          name: 'Ready Player Two by Ernest Cline',
          category: 'audiobooks',
          price: '24.50',
          url: 'https://www.audible.com/pd/Ready-Player-Two-Audiobook/0593396960',
          misc: ''
        },
        {
          name: 'Cyberpunk 2077',
          category: 'video-games',
          price: '49.94',
          url: 'https://smile.amazon.com/Cyberpunk-2077-Xbox-One/dp/B07DJW4WZC/',
          misc: 'XBOX One'
        },
        {
          name: 'Dead by Daylight: Definitive Edition',
          category: 'video-games',
          price: '29.99',
          url: 'https://smile.amazon.com/Dead-Daylight-Definitive-Nintendo-Switch/dp/B07TJWSZQT/',
          misc: 'Nintendo Switch'
        },
        {
          name: 'Remothered: Tormented Fathers',
          category: 'video-games',
          price: '29.99',
          url: 'https://smile.amazon.com/Remothered-Tormented-Fathers-Nintendo-Switch/dp/B07VGP88J9/',
          misc: 'Nintendo Switch'
        },
        {
          name: 'Remothered: Broken Porcelain',
          category: 'video-games',
          price: '29.99',
          url: 'https://smile.amazon.com/Remothered-Broken-Porcelain-NSW-Nintendo-Switch/dp/B07WH3KDMH/',
          misc: 'Nintendo Switch'
        },
        {
          name: 'Garmin Instinct Solar Watch',
          category: 'everyday-carry',
          price: '292.95',
          url: 'https://smile.amazon.com/Garmin-Instinct-Solar-Powered-Smartwatch-Monitoring/dp/B089YVVLSW/',
          misc: 'Graphite'
        },
        {
          name: 'Solo Stove - Bonfire Backyard Bundle',
          category: 'outdoors',
          price: '499.99',
          url: 'https://www.solostove.com/bonfire-backyard-bundle/',
          misc: ''
        },
        {
          name: '2010-2020 Toyota 4Runner Step Edition Bolt On Rock Sliders',
          category: '4Runner',
          price: '867.74',
          url: 'https://caliraisedled.com/collections/rock-sliders/products/2010-2020-4runner-step-edition-bolt-on-rock-sliders',
          misc: '<p><strong>Kick Out Option:</strong> Yes<br><strong>Filler Plate Option:</strong> No<br><strong>Coating:</strong> Powder Coating<br><strong>Shipping:</strong> UPS</p>'
        }

      ]
    }
  },
  head () {
    return {
      title: '',
      meta: [
        { hid: 'ogtitle', property: 'og:title', content: '' },
        { hid: 'twtitle', name: 'twitter:title', content: '' },
        { hid: 'googlename', itemprop: 'name', content: '' },
        { hid: 'description', name: 'description', content: '' },
        { hid: 'ogdescription', property: 'og:description', content: '' },
        { hid: 'twdescription', name: 'twitter:description', content: '' },
        { hid: 'googledescription', itemprop: 'description', content: '' },
        { hid: 'ogurl', property: 'og:url', content: 'https://www.domain.com/' + this.$route.path },
        { hid: 'twsite', name: 'twitter:site', content: 'https://www.domain.com/' + this.$route.path }
      ],
      link: [
        { hid: 'canonical', rel: 'canonical', href: 'https://www.domain.com/' + this.$route.path }
      ]
    }
  }
}
</script>

<style>
.items {
  display: flex;
  padding: 25px;
  flex-wrap: wrap;
  justify-content: space-evenly;
  background-color: rgba(0,0,0,.6);
  height: 100vh;
}
.item {
  background-color: white;
  border: 1px solid black;
  border-radius: 5px;
  margin-bottom: 25px;
  padding: 10px;
  width: 300px;
  min-height: 75px;
}

.item p.title {
  font-size: 1.6em;
  color: rgba(0,0,0,1);
  margin-bottom: 15px;
}

.item p.category {
  font-size: 0.8em;
  color: rgba(0,0,0,.6);
  margin-bottom: 10px;
}

.item p.price {
  font-size: 1em;
  font-style: italic;
  color: rgba(0,0,0,.9);
  margin-bottom: 25px;
}

.item a {
  padding: 15px;
  color: rgba(255,255,255,1);
  background-color: rgba(200,25,82,1);
  font-weight: 700;
  text-decoration: none;
  display: block;
  text-align: center;
  margin-bottom: 25px;
}
</style>
