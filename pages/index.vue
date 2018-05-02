<template>
  <section class="container">
    <article v-for="agency of agencyList" :key="agency.id" class="article-prev">
      <figure class="article-prev__logo">
        <!-- <img  class="article-prev__logo-img" src="/images/ag.min.jpg" width="100" alt=""> -->
      </figure>
      <section class="article-prev__body">
        <h2 class="article-prev__title">{{ agency.title }}</h2>
        <ul>
        <li><b>Телефон:</b> {{ agency.telephone }}</li>
        <li><b>Сайт:</b> {{ agency.site }}</li>
        <li><b>Оставить резюме:</b> {{ agency.mail }}</li>
        <li><b>Метро:</b> {{ agency.metro }}</li>
        <li><b>Адрес:</b> {{ agency.address }}</li>
        <li><b>Кол-во отзывов:</b>{{ agency.countReview }}</li>
        </ul>
        <p>{{ agency.description }}</p>  
      </section>
    </article>
  </section>
</template>

<script>
// import AppLogo from '~/components/AppLogo.vue'

export default {
  // components: {
  //   AppLogo
  // }
  data(){
    return {
      agencyList: [
          {
            id: 1,
            visible: 1,
            title: 'КА Prime Personnel',
            telephone: '+7 (812) 741-14-44',
            site: 'primepersonnel.ru',
            mail: 'spb@primepersonnel.ru',
            metro: 'Нарвская',
            address: 'г. Санкт-Петербург, Нарвский пр,дом 18,4 этаж',
            countReview: 2,
            description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
            logo: 'img.jpg'
          },
          {
            id: 2,
            visible: 1,
            title: 'КА Prime Personnel',
            telephone: '+7 (812) 440-66-23',
            site: 'group.ru',
            mail: 'msc@primepersonnel.ru',
            metro: 'Нарвская',
            address: 'г. Санкт-Петербург, Нарвский пр,дом 18,4 этаж',
            countReview: 5,
            description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit.',
            logo: 'img2.jpg'
          },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.article-prev{
  margin-bottom: 40px;
  max-height: 150px;
  display: table;
  &__header{
    vertical-align: top;
    display: table-cell;
    width: 30%;
  }
  &__body{
    vertical-align: top;
    width: 70%;
    display: table-cell;
  }
  &__logo{
    text-align: center;
    display: table-cell;
    vertical-align: top;
  }
  &__title{
    color: #957aad;
  }

  &__img{
    display: inline-block;
    //float: left;
  }
}


</style>
