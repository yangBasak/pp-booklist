<template>
  <div id="list-page">
    <header>
      <div class="header-inner center">
        <b-button v-b-modal.modal-xl variant="info"> <b-icon icon="plus-circle-fill"></b-icon>추가 </b-button>
      </div>
    </header>
    <section>
      <div class="center">
        <div class="func-container"></div>
        <ul class="list-container">
          <li v-for="item in books" :key="item.key">
            <div><img :src="item.img" /></div>
            <div>
              <h3>{{ item.bookName }}</h3>
              <span>완독날짜: {{ item.finishDate }}</span>
              <span>평점: {{ item.star }}</span>
            </div>
          </li>
        </ul>
      </div>
    </section>

    <b-modal id="modal-xl" size="xl" title="Extra Large Modal">책 목록 추가</b-modal>
  </div>
</template>

<script>
export default {
  name: "ListPage",
  created() {},
  data() {
    return {
      books: [
        {
          img: require("../assets/images/noimg.png"),
          bookName: "책이름",
          finishDate: "2020/02/20",
          star: "★★★★★",
        },
        {
          img: require("../assets/images/noimg.png"),
          bookName: "책이름",
          finishDate: "2020/02/20",
          star: "★★★★★",
        },
      ],
    };
  },
  methods: {
    getBookInfo() {},
  },
};
</script>

<style scoped></style>
