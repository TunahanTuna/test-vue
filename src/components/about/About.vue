<template>
  <div class="about-container">
    <div class="about-seperator"></div>
    <div class="about-with-background">
      <div class="about-background">
        <img :src="backgroundImage" />
      </div>
      <div class="about">
        <h1>{{ about.title }}</h1>
        <p>{{ about.text1 }}</p>
        <p>{{ about.text2 }}</p>
        <div class="about-images">
          <div
            v-for="(image, index) in about.images"
            :key="`item-${index}`"
            class="about-image"
          >
            <img :src="image" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      backgroundImage: "https://ifl.com.tr/images/sembol-21.svg?crc=100200840",
      about: {
        title: "IFL PHARMA",
        text1:
          "IFL PHARMA 2020 yılında dünyada milyonlarca insanın ve hayvanın yaşam kalitesini doğrudan etkileyen, henüz çözüm geliştirilmemiş sağlık sorunlarını çözmek için yenilikçi ürünler geliştirmek amacıyla kuruldu. 2021 yılında Gazi Üniversitesi Teknopark’ta faaliyete geçen araştırma geliştirme merkezinin ardından 2022 yılında da Ankara OSTİM’de üretim tesisleri faaliyete başladı.",
        text2:
          "IFL PHARMA ArGe ekibi alerji, immünoloji, dermatoloji alanlarına odaklanarak çalışmalar yapmaktadır. Bu alanlarda geliştirilen yenilikçi ürünler tıbbi cihaz, kozmetik, ilaç ve veteriner ürünleri olarak kullanıma sunulacaktır.",
        images: [
          "https://ifl.com.tr/images/ikonlar-35.svg?crc=66129170",
          "https://ifl.com.tr/images/ikonlar-32.svg?crc=438266839",
          "https://ifl.com.tr/images/ikonlar-33.svg?crc=274463970",
          "https://ifl.com.tr/images/ikonlar-34.svg?crc=3775998447",
        ],
      },
    };
  },
};
</script>

<style scoped>
.about-container {
  display: flex;
  align-items: center;
  flex-direction: column;
  background-color: #457749;
  color: #fff;
  min-width: 900px;
  height: auto;
}
.about-with-background {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.about-background {
  transform: rotate(180deg);
  position: absolute;
  width: 500px;
  height: auto;
  z-index: 1;
}
.about-seperator {
  background-color: #72c172;
  height: 12px;
  width: 50%;
  min-width: 720px;
}
.about {
  width: 45%;
  min-width: 720px;
  height: auto;
  justify-content: center;
  padding-left: 3rem;
  padding-bottom: 3rem;
  padding-top: 1rem;
  z-index: 2;
}
.about h1 {
  font-weight: bold;
  font-size: 34px;
  padding-top: 2rem;
  padding-bottom: 3rem;
}
.about p {
  font-size: 23px;
  padding-bottom: 2rem;
  line-height: 2rem;
}
.about-image {
  width: 165px;
  height: 165px;
  padding-left: 1rem;
}
.about-images {
  display: flex;
  flex-direction: row;
  justify-content: center;
  padding-top: 2rem;
}
</style>
