<script setup>
import { goodsArray } from '../constants/good';

const getUrl = (name) => {
  return new URL(`../assets/img/goods/${name}.jpg`, import.meta.url);
}
</script>
  
<template>
<section class="products">
          <div class="container">
            <div class="products-header-goods">
              <h3 class="products-header--title">Тануки</h3>
              <div class="products-card__description-info">
                <div class="products-card__description-info--rating">
                  <img src="../assets/img/icons/star.svg" alt="star" />
                  4.5
                </div>
                <div class="products-card__description-info--price">
                  От 900 ₽
                </div>
                <div class="products-card__description-info--group">
                  Пицца и суши
                </div>
              </div>
            </div>
            <div class="products-wrapper">

              <div           
            class="products-card"
            v-for="good in goodsArray"
            :key='good.id'            
          >
                <div class="products-card__image">
                  <img :src="getUrl(good.image)" alt="{{good.image}}" />
                </div>
                <div class="products-card__description">
                  <div class="products-card__description-row">
                    <h5 class="products-card__description--name">
                      {{good.name}}
                    </h5>
                  </div>
                  <div class="products-card__description-row">
                    <p class="products-card__description--text">
                      {{good.text}}
                    </p>
                  </div>
                  <div class="products-card__description-row">
                    <div class="products-card__description-controls">
                      <button class="btn btn-primary">
                        В корзину
                        <img src="../assets/img/icons/shopping-cart.svg" alt="cart" />
                      </button>
                      <span class="products-card__description-controls--price"
                        > {{good.price}} ₽</span
                      >
                    </div>
                  </div>
                </div>
              </div>>           
            </div>
          </div>
        </section>
</template>
