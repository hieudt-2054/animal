<template>
      <v-flex
        mb-5
        xs12
      >
      <v-card>
         <v-card-title>
        Nhân Viên
       <v-spacer></v-spacer>
        <v-text-field
          v-model="search"
          label="Tìm kiếm"
          single-line
          hide-details
        ></v-text-field>
      </v-card-title>
       <v-data-table
          :headers="headers"
          :items="desserts"
          :items-per-page="5"
          :search="search"
          class="elevation-1"
        >
           <template v-slot:item.image="{ item }">
             <img :src="item.image"/>
          </template>
          <template v-slot:item.dieukien="{ item }">
             Cần {{ item.star }} <img :src="starImage"/> và {{ item.fish }} <img :src="fishImage"/>
             <div v-if="item.share">
                ( {{ item.share }} )
              </div>
          </template>
        </v-data-table>
      </v-card>
      </v-flex>
</template>

<script>
export default {
  name: 'Staff',

  data: () => ({
    search: '',
    starImage: 'https://vignette.wikia.nocookie.net/animalrestaurant/images/a/a7/Rating.png/revision/latest/scale-to-width-down/20?cb=20191230195149',
    fishImage: 'https://vignette.wikia.nocookie.net/animalrestaurant/images/4/41/Cod.png/revision/latest/scale-to-width-down/20?cb=20191230195323',
    headers: [
        {
          text: 'Tên Nhân Viên',
          sortable: true,
          value: 'name',
        },
        { text: 'Hình ảnh', value: 'image', sortable: false },
        { text: 'Công dụng', value: 'congdung' },
        { text: 'Điều kiện', value: 'dieukien' },
      ],
    desserts: [
        {
          name: 'Thỏ đinh ngư dân',
          image: 'https://vignette.wikia.nocookie.net/animalrestaurant/images/0/0d/Fisherman_Rabbit_Ding.png/revision/latest/top-crop/width/80/height/80',
          congdung: 'Đào đất, mỗi ngày tự động đào (N) Mồi câu , N tùy theo level',
          star: 4000,
          fish: 0,
        },
        {
          name: 'Eggy Chạy vặt',
          image: 'https://vignette.wikia.nocookie.net/animalrestaurant/images/6/6d/Eggy_the_Handyman.png/revision/latest/top-crop/width/80/height/80',
          congdung: 'Tìm cá khô ở góc số lượng cá tùy theo level ',
          star: 0,
          fish: 8000,
        },
        {
          name: 'Jiji Bồi Bàn',
          image: 'https://vignette.wikia.nocookie.net/animalrestaurant/images/6/61/Jiji_the_Waiter.png/revision/latest/scale-to-width-down/120',
          congdung: 'Giúp khách tự động gọi món trong 1 khoảng thời gian',
          star: 0,
          fish: 35000,
        },
        {
          name: 'Apricat Quét Dọn',
          image: 'https://vignette.wikia.nocookie.net/animalrestaurant/images/6/6c/Apricat_the_Sweeper.png/revision/latest/scale-to-width-down/120',
          congdung: 'Quét dọn khắp nơi trong 1 khoảng thời gian',
          star: 0,
          fish: 15000,
        },
        {
          name: 'Dori Đón khách',
          image: 'https://vignette.wikia.nocookie.net/animalrestaurant/images/7/75/Dori_the_Promoter.png/revision/latest/scale-to-width-down/120',
          congdung: 'Tự động mời N khách sau 1 khoảng thời gian, nhấn giữ nút quảng cáo N giây có thể mời 1 khách',
          star: 0,
          fish: 65000,
        },
        {
          name: 'Timmy Phục Vụ',
          image: 'https://vignette.wikia.nocookie.net/animalrestaurant/images/7/7b/Timmy_the_Server.png/revision/latest/scale-to-width-down/120',
          congdung: 'Xua đuổi những khách hàng gây rối',
          star: 0,
          fish: 30000,
        },
        {
          name: 'Đầu bếp gumi',
          image: 'https://vignette.wikia.nocookie.net/animalrestaurant/images/7/71/Chef_Gumi.png/revision/latest/scale-to-width-down/120',
          congdung: 'Gumi vung xẻng lên, nhà bếp vào trạng thái điên cuồng, tăng tốc nấu ăn',
          star: 0,
          fish: 0,
          share: 'Nhận được từ chia sẻ FB'
        },
      ],
  }),
};
</script>
