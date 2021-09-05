<template>
  <Header />
  <main>
    <Presentation />
    <WeAre />
    <Custom />
    <WeHave :supplies="supplies" />
    <Comments :comments="comments" />
    <Subscribe />
  </main>
  <Footer />
</template>

<script>
import Header from '@/components/blocks/Header/Header.vue'
import Presentation from '@/components/blocks/Presentation/Presentation.vue'
import WeAre from '@/components/blocks/WeAre/WeAre.vue'
import Custom from '@/components/blocks/Custom/Custom.vue'
import WeHave from '@/components/blocks/WeHave/WeHave.vue'
import Comments from '@/components/blocks/Comments/Comments.vue'
import Subscribe from '@/components/blocks/Subscribe/Subscribe.vue'
import Footer from './components/blocks/Footer/Footer.vue'
export default {
  data () {
    return {
      supplies: [
        { title: 'Desk', img: require('@/assets/images/desk-card.jpg') },
        { title: 'Chair', img: require('@/assets/images/chair-card.jpg') },
        {
          title: 'Kitchenware',
          img: require('@/assets/images/kitchenware-card.jpg')
        },
        {
          title: 'Book Shelf',
          img: require('@/assets/images/book-shelf-card.jpg')
        },
        {
          title: 'Electronics',
          img: require('@/assets/images/electronics.jpg')
        }
      ],
      comments: [
        {
          stars: 5,
          text: 'My experience with WOODIES is a complete success, from customed furniture, range of product, modern design, purchasing experience, the delivery and newsletter. Litterally everything is great. Thank you!',
          avatar: require('@/assets/images/sandra-avatar.png'),
          name: 'Sandra Dewi',
          city: 'Jakarta Selatan'
        },
        {
          stars: 4,
          text: 'My experience with WOODIES is a complete success, from customed furniture, range of product, modern design, purchaewsletter. Litterally everything is great. Thank you!',
          avatar: require('@/assets/images/sandra-avatar.png'),
          name: 'Jane Smith',
          city: 'Jersey City'
        },
        {
          stars: 5,
          text: 'My experience with WOODIES is a duct, modern design, purchasing experience, the delivery and newsletter. Litterally everything is great. Thank you!',
          avatar: require('@/assets/images/sandra-avatar.png'),
          name: 'Alex Williams',
          city: 'Los Angeles'
        },
        {
          stars: 4,
          text: 'My experience withd furniture, range of product, modern design, purchasing experience, the delivery and newsletter. Litterally everything is great. Thank you!',
          avatar: require('@/assets/images/sandra-avatar.png'),
          name: 'Jim Davis',
          city: 'New York'
        }
      ]
    }
  },
  components: {
    Header,
    Presentation,
    WeAre,
    Custom,
    WeHave,
    Comments,
    Subscribe,
    Footer
  }
}
</script>

<style>
</style>
