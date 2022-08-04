<template>
  <div class="footer-container">
    <div class="footer-container-up">
      <p>{{ copyrightText }}</p>
    </div>
    <div class="footer-container-mid">
      <!-- ?: Dinamikleştirilecek: DONE -->
      <div v-for="page in pages" :key="page.id">
        <button v-if="page.id != 5" class="mid-button">{{ page.text }}</button>
        <div v-else class="i18-button-container">
          <button class="i18-button">{{ page.text }}</button>
        </div>
      </div>
    </div>
    <div class="footer-container-down">
      <!-- ?: Dinamikleştirilecek -->
      <div v-for="description in descriptions" :key="description.id">
        <a>{{ description.text }}</a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      pages: [
        { id: 1, text: "ANASAYFA" },
        { id: 2, text: "IFL PHARMA" },
        { id: 3, text: "KATEGORİLER & ÜRÜNLER" },
        { id: 4, text: "BİZE ULAŞIN" },
        { id: 5, text: "EN" },
      ],
      descriptions: [
        { id: 1, text: "KVKK Metni" },
        { id: 2, text: "Çerez Bildirimi" },
        { id: 3, text: "Sertifikalarımız" },
      ],
      copyrightText: "Copyright © IFL Pharma 2022. Tüm hakları saklıdır.",
    };
  },
};
</script>

<style>
.footer-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  vertical-align: middle;
  height: 225px;
  width: 100%;
  min-width: 900px;
}
.footer-container-up {
  background: #17551b;
  flex: 1;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 14px;
  width: 100%;
}
.footer-container-mid {
  display: flex;
  flex-direction: row;
  background: #72c172;
  flex: 2;
  align-items: center;
  justify-content: center;
  width: 100%;
}
.mid-button {
  color: white;
  padding-left: 3rem;
  padding-right: 3rem;
  background: #72c172;
  border: none;
  font-size: 20px;
  font-weight: bold;
  height: 40px;
}
.mid-button:hover {
  background-color: gray;
}
.footer-container-down {
  display: flex;
  align-items: center;
  justify-content: center;
  background: #17551b;
  flex: 2;
  color: #72c172;
  width: 100%;
}
.footer-container-down a {
  padding-left: 8rem;
  font-size: 14px;
}
.i18-button {
  font-size: 20px;
  font-weight: bold;
  color: white;
  background: #30a83a;
  width: 60px;
  height: 30px;
  border-radius: 5px;
  border: none;
}
.i18-button-container {
  padding-left: 4rem;
}
</style>
