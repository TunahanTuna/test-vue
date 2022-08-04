<template>
  <div class="members-container">
    <div class="members-main"></div>
    <div class="members-header">Kurucu Ekibimiz</div>
    <div class="members" v-for="member in members" :key="`item-${member.id}`">
      <div class="member">
        <img :src="member.img" class="member-image" />
        <div class="member-features">
          <div class="member-name">
            <p>{{ member.name }}</p>
          </div>
          <div class="member-title">
            <p>{{ member.title }}</p>
          </div>
          <div class="member-biography">
            <p>{{ member.biography }}</p>
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
      // !: PROPS OLARAK ALINACAK
      members: [
        {
          id: 1,
          img: "https://ifl.com.tr/images/naz-balkan-foto.jpg?crc=142920261",
          name: "Nazlı Balkan Gürses",
          title: "Yönetim Kurulu Başkanı",
          biography:
            "Naz Balkan Gürses’in Medikal Sektörde 22 yıldan uzun bir süredir deneyimi bulunmaktadır. Kurt&Kurt ve Hitachi Healthcare firmalarında Genel Müdürlük pozisyonunun yanı sıra pek çok görevde yer almıştır. İngiltere’de University of Hertfordshire’da İşletme Eğitimini takiben Harvard Universitesinde İşletme Ve Yönetim programına katılmıştır. Yönetim Kurulu Başkanı olarak hedefi IFL Pharma’yı global sağlık pazarında lider kuruluşlardan biri yapmaktır.",
        },
        {
          id: 2,
          img: "https://ifl.com.tr/images/firat-balkan-foto.jpg?crc=131108426",
          name: "Fırat Balkan",
          title: "Genel Müdür",
          biography:
            "Fırat Balkan Orta Doğu Teknik Üniversitesi Maden Mühendisliği bölümünden mezundur. Otomotiv ve Telekomünikasyon altyapı inşaası sektörlerinde geniş yönetim deneyimine sahiptir. Reysaş İnşaat ve Subaru Ankara’da yönetici pozisyonlarında bulunmuştur. Profesyonel Dalış Eğitmeni ve kaptan olan Fırat Balkan, IFL Pharma firmasında Genel Müdür olarak görev yapmaktadır.",
        },
        {
          id: 3,
          img: "https://ifl.com.tr/images/mahir-tulunay-foto.jpg?crc=3783764954",
          name: "Dr. Mahir Tulunay",
          title: "Operasyon ve ArGe Direktörü",
          biography:
            "Mahir Tulunay 17 yılı aşan Kalite Kontrol ve ArGe deneyiminin yanı sıra Yeditepe Üniversitesi Kimya Mühendisliği bölümünde öğretim görevlisi olarak çalışmıştır. Osmangazi Üniversitesi Kimya Mühendisliğini takiben Yeditepe Üniversitesinde MBA ve Kimya Mühendisliği bölümünde Doktora yapmıştır. Mahir Novartis Türkiye ve İsviçre’de Stabilite Sorumlusu olarak çalışmıştır. Sonrasında Kalite Sistem Laboratuarları, Johnson Diversey Sealed Air, SGS Supervise Kontrol Sistemleri firmalarında çalışmıştır. Real Hipermarketleri ve Şok Marketlerde Teknik Müdürlük ve Denetmenlik yapan Mahir, IFL Pharma’da ArGe ve Operasyonlardan sorumludur.",
        },
        {
          id: 4,
          img: "https://ifl.com.tr/images/ilker-karakuscu-foto.jpg?crc=211534791",
          name: "İlker Karakuşçu",
          title: "Satış ve Pazarlama Direktörü",
          biography:
            "İlker Karakuşcu 20 yılı aşan deneyime sahip bir Satış Yöneticisidir. Colgate Palmolive ve Reckitt gibi uluslararası firmalarda çeşitli satış pozisyonlarından sonra Vileda ve Hobby Kozmetik firmalarında Direktör olarak çalıştı. IFL Pharma firmasınında Satış ve Pazarlama yönetim sorumluluğunu üstlenmektedir. Ürün Geliştirme, tasarım, pazar araştırmaları ve satış yapısı oluşturulması konularında çalışmaktadır.",
        },
        {
          id: 5,
          img: "https://ifl.com.tr/images/emre-tombuloglu-foto.jpg?crc=4036547481",
          name: "Emre Tombuloğlu",
          title: "Finans Direktörü",
          biography:
            "Emre Tombuloğlu 20 yıllık bağımsız denetim, kurumsal şirket yönetimi, yatırım bankacılığı ve sağlık sektöründe stratejik danışmanlık tecrübesine sahiptir. Babson College’da işletme üzerine lisans eğitimi almıştır. Emre birçok şirket birleşme ve satın alma projesinde yer almış ve global sağlık şirketlerine stratejik danışmanlık hizmeti sunmuştur. IFL Pharma'nın CFO'su olarak, tüm finansal faaliyetlerin planlanması, uygulanması, yönetilmesi ve yürütülmesinden sorumludur.",
        },
      ],
    };
  },
};
</script>

<style scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.members-header {
  width: 50%;
  min-width: 720px;
  height: auto;
  background-color: #17551b;
  color: #fff;
  font-size: 30px;
  font-weight: bold;
  padding: 0.4rem;
  padding-left: 1.6rem;
}
.members-container {
  min-width: 900px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #d5edd5;
}
.members {
  min-width: 720px;
  max-width: 50%;
}
.member {
  display: flex;
  padding: 1rem;
}
.member-image {
  width: 280px;
  height: 280px;
  display: block;
}
.member-features {
  padding-left: 1rem;
  text-align: left;
}
.member-name {
  font-weight: bold;
  padding-bottom: 0.5rem;
  font-size: 20px;
}
.member-title {
  font-size: 18px;
  padding-bottom: 1rem;
}

.member-biography {
  font-size: 18px;
}
</style>
