<template>
  <div class="main-container">
    <div class="header">Değerlerimiz</div>
    <div class="card-container">
      <div v-for="value in values" :key="`item-${value.id}`" class="cards">
        <div v-if="value.id % 2 == 1" class="card light">
          <img :src="value.img" />
          <p>{{ value.text }}</p>
        </div>
        <div v-else class="card dark">
          <img :src="value.img" />
          <p>{{ value.text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: () => {
    return {
      values: [
        {
          id: 1,
          img: "https://ifl.com.tr/images/dogaya-saygili-icon-09.svg?crc=252346713",
          text: "DOĞAYA SAYGI",
        },
        {
          id: 2,
          img: "https://ifl.com.tr/images/insan-sagligi-icon.svg?crc=4003185263",
          text: "İNSAN SAĞLIĞINA KATKI",
        },
        {
          id: 3,
          img: "https://ifl.com.tr/images/hayvan-sagligi-icon.svg?crc=276915670",
          text: "HAYVAN SAĞLIĞINA KATKI",
        },
        {
          id: 4,
          img: "https://ifl.com.tr/images/hayati-kolaylastirma-icon-13.svg?crc=317042626",
          text: "HAYATI KOLAYLAŞTIRMA",
        },
        {
          id: 5,
          img: "https://ifl.com.tr/images/yasam-kalitesi-ikon.svg?crc=2027063",
          text: "CANLILARIN YAŞAM KALİTESİNİ ARTIRMA",
        },
        {
          id: 6,
          img: "https://ifl.com.tr/images/bilimsel-yaklasim-icon-10.svg?crc=408100603",
          text: "BİLİMSEL YAKLAŞIM",
        },
      ],
    };
  },
};
</script>

<style scoped>
* {
  align-items: center;
}
.main-container {
  display: flex;
  flex-direction: column;
  min-width: 900px;
}
.header {
  width: 50%;
  min-width: 720px;
  height: auto;
  color: #ffffff;
  background-color: #72c172;
  font-size: 30px;
  font-weight: bold;
  padding: 0.4rem;
  padding-left: 1.6rem;
}
.card-container {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  width: 900px;
  height: 600px;
}
.cards {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  justify-content: center;
  padding: 0.8rem;
}
.card {
  width: 250px;
  height: 250px;
}
.light {
  background-color: #72c172;
}
.dark {
  background-color: #30a82a;
}
.card p {
  color: #ffffff;
  font-size: 18px;
  padding-right: 2rem;
  padding-left: 2rem;
}
.card img {
  padding-top: 0.5rem;
  height: 150px;
  width: 150px;
  padding-bottom: 1rem;
}
</style>
