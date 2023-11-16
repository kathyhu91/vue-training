<template>
  <div>
    <!-- brand -->
    <div class="min-vh-100 position-relative mb-3 mb-md-5">
      <!-- bg block -->
      <div class="decoBox decoBox--plant position-absolute top-0 start-0"></div>
      <div class="decoBox decoBox--plant position-absolute bottom-0 end-0"></div>
      <div
        class="position-absolute banner--position bg-cover bg-attachment--fixed"
        :style="{ backgroundImage: 'url(' + img.brandImg + ')' }"
      ></div>
      <!-- main content -->
      <div class="position-absolute top-50 start-50 translate-middle text-light text-center">
        <h1 class="display-1 fw-bold">
          三木森八百屋<br />
          <span class="ff--particular">Forest Yaoya</span>
        </h1>
        <hr />
        <h2 class="h3 ff--special">Fresh and Flavorful, Your One-Stop Veggie Shop !</h2>
      </div>
    </div>
    <!-- intro -->
    <div class="container mb-3 mb-md-5">
      <div class="row flex-md-row-reverse justify-content-md-center align-items-md-center py-5">
        <div class="col-md-3">
          <img :src="img.ShopImg" alt="yaoya-shop" class="w-100 object-fit-cover" />
        </div>
        <div class="col-md-6 text-center">
          <p class="fs-4 mb-3">關於</p>
          <h3 class="h3 fw-bold mb-3 text-success">
            三木森八百屋 <span class="ff--particular">Forest Yaoya</span>
          </h3>
          <p class="fw-bold mb-2 fs-5">品味生活，從蔬食開始！</p>
          <p>
            三木森八百屋擁有自己的農場，由職人細心栽種。<br />為您挑選新鮮、有機的時令蔬菜，直送您的餐桌。<br />從農田到餐桌，保證新鮮美味，讓您輕鬆享受營養美食。
          </p>
        </div>
      </div>
    </div>
    <!-- prod -->
    <div class="container">
      <div class="row">
        <div class="col-md-4" v-for="info in introInfo" :key="'productList' + info.id">
          <div class="card h-100 link--hover">
            <img :src="info.img" class="card-img-top infoImg--size" alt="intro-img" />
            <div class="card-body">
              <h5 class="card-title text-center fw-bold text-success">{{ info.title }}</h5>
              <p class="card-text">
                {{ info.text }}
              </p>
              <a href="#" class="btn btn-outline-success w-100">瀏覽更多</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- end brand -->
    <div class="container my-5">
      <div class="row justify-content-md-center align-items-md-center py-5">
        <div class="col-1"></div>
        <div class="col-4"><img :src="img.carImg" alt="car" class="w-100 object-fit-cover" /></div>
        <div class="col-6">
          <h5 class="h4 fst-italic fw-bold lh-lg text-center text-success mb-4">
            來自大自然的新鮮滋味<br />為您的生活注入健康和美味！
          </h5>
          <div class="d-flex justify-content-center">
            <button type="button" class="btn btn-success w-50">立即選購</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import brandImg from '@/assets/img/brand.jpeg'
import ShopImg from '@/assets/img/shop.png'
import carImg from '@/assets/img/car.png'
import fieldImg from '@/assets/img/field.png'
import farmersImg from '@/assets/img/farmers.png'
import productImg from '@/assets/img/product.png'

export default {
  data() {
    return {
      img: {
        brandImg,
        ShopImg,
        carImg
      },
      introInfo: [
        {
          id: 'info01',
          title: '自有農場有機栽種',
          text: '我們以環保有機方式，自有農場精心栽種，確保每一份蔬菜都擁有自然的滋味，為您提供最健康美味的食材。',
          img: fieldImg
        },
        {
          id: 'info02',
          title: '農家職人細心耕作',
          text: '農家職人以細心耕作，呈現土地的真實味道。我們堅守傳統農耕，讓每一份農產品都散發濃濃的農家情懷。',
          img: farmersImg
        },
        {
          id: 'info03',
          title: '精選搭配營養均衡健康',
          text: '我們精心搭配，確保每一份蔬果箱都兼具營養均衡，為您提供最健康美味的食材，享受健康生活。',
          img: productImg
        }
      ]
    }
  }
}
</script>
