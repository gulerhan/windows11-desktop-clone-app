<template>
  <!-- Weather Drawer -->
  <v-navigation-drawer
    v-model="drawer"
    temporary
    class="m-4 rounded-lg w-auto max-w-4xl"
    style="
      height: calc(100% - 90px);
      background-color: rgba(255, 255, 255, 0.9);
      transition-duration: 0.5s;
    "
  >
    <div
      class="flex justify-between p-4 sticky top-0 align-center"
      style="background-color: rgba(253, 253, 253)"
    >
      <div class="flex gap-3 align-center">
        <span class="mdi mdi-home-variant mdi-24px hover:bg-gray-100 p-1 px-2 rounded"></span>
        <span class="mdi mdi-play-box-outline mdi-24px hover:bg-gray-100 p-1 px-2 rounded"></span>
        <span class="mdi mdi-chess-pawn mdi-24px hover:bg-gray-100 p-1 px-2 rounded"></span>
      </div>
      <div class="flex gap-3 p-3">
        <span class="mdi mdi-plus mdi-24px hover:bg-gray-100 p-1 px-2 rounded"></span>
        <span class="mdi mdi-rotate-right mdi-24px hover:bg-gray-100 p-1 px-2 rounded"></span>

        <span class="mdi mdi-arrow-expand mdi-24px hover:bg-gray-100 p-1 px-2 rounded"></span>

        <span class="mdi mdi-account-circle mdi-24px hover:bg-gray-100 p-1 px-2 rounded"></span>
      </div>
    </div>
    <div class="flex flex-wrap pl-14 gap-x-6 gap-y-6">
      <div>
        <img src="../assets/imgs/news-1.png" alt="" />
      </div>
      <div>
        <img src="../assets/imgs/news-2.png" alt="" />
        <img src="../assets/imgs/news-4.png" alt="" class="pt-4" />
      </div>
      <div><img src="../assets/imgs/news-3.png" alt="" /></div>
      <div><img src="../assets/imgs/news-5.png" alt="" /></div>
      <div><img src="../assets/imgs/news-6.png" alt="" /></div>
    </div>
  </v-navigation-drawer>
  <!-- Windows Drawer -->
  <v-navigation-drawer
    location="bottom"
    v-model="windowsDrawer"
    temporary
    class="m-4 rounded-lg"
    style="
      height: calc(90% - 90px);
      top: 10%;
      width: 40%;
      left: 32%;
      background-color: rgb(236, 247, 255);
      transition-duration: 0.5s;
    "
  >
    <div class="flex justify-around p-3 pt-6">
      <v-text-field
        density="compact"
        variant="solo"
        label="Ara"
        prepend-inner-icon="mdi-magnify"
        single-line
        hide-details
        class="w-56 pl-2 rounded-pill"
      ></v-text-field>
    </div>
    <div class="flex justify-between align-center pt-5 px-10">
      <div class="font-bold text-sm">
        <p class="">Sabitlendi</p>
      </div>
      <div class="flex">
        <p
          class="border border-2 border-slate-300 bg-white rounded text-xs p-1 cursor-pointer flex"
        >
          Tüm Uygulamalar
          <span class="mdi mdi-chevron-right mdi-12px pl-2 rounded"></span>
        </p>
      </div>
    </div>
    <div class="pl-8 p-6">
      <div class="grid grid-cols-6">
        <div class="flex flex-col align-center hover:bg-white rounded p-4 pt-1">
          <span class="mdi mdi-calendar-account-outline mdi-48px"></span>
          <p class="text-xs" style="line-height: 0">Takvim</p>
        </div>
        <div class="flex flex-col align-center hover:bg-white rounded p-4 pt-1">
          <span class="mdi mdi-instagram mdi-48px"></span>
          <p class="text-xs" style="line-height: 0">Instagram</p>
        </div>
        <div class="flex flex-col align-center hover:bg-white rounded p-4 pt-1">
          <span class="mdi mdi-facebook mdi-48px"></span>
          <p class="text-xs" style="line-height: 0">Facebook</p>
        </div>
        <div class="flex flex-col align-center hover:bg-white rounded p-4 pt-1">
          <span class="mdi mdi-twitter mdi-48px"></span>
          <p class="text-xs" style="line-height: 0">Twitter</p>
        </div>
        <div class="flex flex-col align-center hover:bg-white rounded p-4 pt-1">
          <span class="mdi mdi-snapchat mdi-48px"></span>
          <p class="text-xs" style="line-height: 0">Snapchat</p>
        </div>
        <div class="flex flex-col align-center hover:bg-white rounded p-4 pt-1">
          <span class="mdi mdi-microsoft-xbox mdi-48px"></span>
          <p class="text-xs" style="line-height: 0">Xbox</p>
        </div>
      </div>
      <div class="grid grid-cols-6 pb-28 pt-4">
        <div class="flex flex-col align-center hover:bg-white rounded p-4 pt-1">
          <span class="mdi mdi-file-pdf-box mdi-48px"></span>
          <p class="text-xs" style="line-height: 0">Adobe</p>
        </div>

        <div class="flex flex-col align-center hover:bg-white rounded p-4 pt-1">
          <span class="mdi mdi-facebook-messenger mdi-48px"></span>
          <p class="text-xs" style="line-height: 0">Messenger</p>
        </div>

        <div class="flex flex-col align-center hover:bg-white rounded p-4 pt-1">
          <span class="mdi mdi-spotify mdi-48px"></span>
          <p class="text-xs" style="line-height: 0">Spotify</p>
        </div>
      </div>
    </div>
    <div
      class="flex justify-between align-center border-t border-slate-100 p-2 px-10 rounded bg-slate-100"
    >
      <div class="flex align-center hover:bg-white rounded p-1 px-2">
        <span class="mdi mdi-account mdi-24px rounded"></span>
        <p class="text-xs pl-2">Steve Jobs</p>
      </div>
      <div class="pr-10">
        <span class="mdi mdi-power mdi-24px hover:hover:bg-white p-2 pt-3 rounded"></span>
      </div>
    </div>
  </v-navigation-drawer>
  <!-- Opened Apps Drawer -->
  <v-navigation-drawer
    location="bottom"
    v-model="openedApps"
    temporary
    class="m-5 rounded-lg"
    style="
      height: calc(25% - 90px);
      top: 76%;
      width: 15%;
      left: 77%;
      background-color: rgb(226 232 240);
      transition-duration: 0.5s;
    "
  >
    <div class="grid grid-cols-5 p-3">
      <span
        class="mdi mdi-steam mdi-12px hover:bg-white rounded flex flex-row justify-center p-1"
      ></span>
      <span
        class="mdi mdi-microsoft-visual-studio-code mdi-12px hover:bg-white rounded flex flex-row justify-center p-1"
      ></span>
      <span
        class="mdi mdi-google-chrome mdi-12px hover:bg-white rounded flex flex-row justify-center p-1"
      ></span>
      <span
        class="mdi mdi-skype mdi-12px hover:bg-white rounded flex flex-row justify-center p-1"
      ></span>
      <span
        class="mdi mdi-virus mdi-12px hover:bg-white rounded flex flex-row justify-center p-1"
      ></span>
      <span
        class="mdi mdi-github mdi-12px hover:bg-white rounded flex flex-row justify-center p-1"
      ></span>
      <span
        class="mdi mdi-git mdi-12px hover:bg-white rounded flex flex-row justify-center p-1"
      ></span>
    </div>
  </v-navigation-drawer>
  <!-- cloud Drawer -->
  <v-navigation-drawer
    location="bottom"
    v-model="cloud"
    temporary
    class="m-4 rounded-lg"
    style="
      height: calc(86.5% - 94px);
      left: 72.5%;
      top: 14%;
      width: 25%;
      background-color: rgb(236, 247, 255);
      transition-duration: 0.5s;
    "
  >
    <div class="flex justify-between p-4 align-center">
      <div class="flex align-center">
        <span class="mdi mdi-microsoft-onedrive mdi-24px cursor-pointer"></span>
        <p class="text-sm pl-2">One drive kişisel</p>
      </div>
      <span class="mdi mdi-cog mdi-24px cursor-pointer hover:bg-white p-1 py-0 rounded"></span>
    </div>
    <div class="flex w-100 hover:bg-white pl-5 cursor-pointer align-center">
      <span class="mdi mdi-cog-box mdi-48px"></span>
      <div class="pl-2">
        <p class="text-md">Merhaba</p>
        <p class="text-xs">yüklendi</p>
      </div>
    </div>
    <div class="flex w-100 hover:bg-white pl-5 cursor-pointer align-center">
      <span class="mdi mdi-cog-box mdi-48px"></span>
      <div class="pl-2">
        <p class="text-md">Merhaba</p>
        <p class="text-xs">yüklendi</p>
      </div>
    </div>
    <div class="flex w-100 hover:bg-white pl-5 cursor-pointer align-center">
      <span class="mdi mdi-cog-box mdi-48px"></span>
      <div class="pl-2">
        <p class="text-md">Merhaba</p>
        <p class="text-xs">yüklendi</p>
      </div>
    </div>
    <div class="flex w-100 hover:bg-white pl-5 cursor-pointer align-center">
      <span class="mdi mdi-cog-box mdi-48px"></span>
      <div class="pl-2">
        <p class="text-md">Merhaba</p>
        <p class="text-xs">yüklendi</p>
      </div>
    </div>
    <div class="flex w-100 hover:bg-white pl-5 cursor-pointer align-center">
      <span class="mdi mdi-cog-box mdi-48px"></span>
      <div class="pl-2">
        <p class="text-md">Merhaba</p>
        <p class="text-xs">yüklendi</p>
      </div>
    </div>
    <div class="flex justify-around border-t border-slate-600 pt-1 bg-slate-100 rounded pt-2">
      <div class="flex flex-col align-center hover:bg-white rounded w-50 py-1 ml-3">
        <span class="mdi mdi-folder mdi-24px"></span>
        <p class="text-xs">Klasörü aç</p>
      </div>
      <div class="flex flex-col align-center hover:bg-white rounded w-50 py-1">
        <span class="mdi mdi-wan mdi-24px"></span>
        <p class="text-xs">Çevrimiçi aç</p>
      </div>
      <div class="flex flex-col align-center hover:bg-white rounded w-50 py-1 pb-2">
        <span class="mdi mdi-recycle mdi-24px"></span>
        <p class="text-xs text-center">Geri dönüşüm kutusu</p>
      </div>
      <div class="flex flex-col align-center hover:bg-white rounded w-50 py-1 mr-3">
        <span class="mdi mdi-diamond-stone mdi-24px"></span>
        <p class="text-xs">Yükselt</p>
      </div>
    </div>
  </v-navigation-drawer>
  <!-- Settings Drawer -->
  <v-navigation-drawer
    location="bottom"
    v-model="settingsDrawer"
    temporary
    class="m-4 rounded-lg"
    style="
      height: calc(64% - 90px);
      top: 36%;
      width: 25%;
      left: 72.5%;
      background-color: rgb(236, 247, 255);
      transition-duration: 0.5s;
    "
  >
    <div class="flex justify-around p-3 pt-6">
      <div class="flex flex-col align-center">
        <div
          class="flex border-2 border-solid border-gray-400 bg-gray-200 shadow-lg shadow-slate-400 rounded"
        >
          <span class="mdi mdi-wifi mdi-12px p-2 px-3 hover:bg-slate-300"></span>

          <span
            class="mdi mdi-chevron-right mdi-24px p-1 px-2 hover:bg-slate-300"
            style="border-left: 1px solid rgb(148 163 184)"
          ></span>
        </div>
        <div class="text-sm pt-1">Internet</div>
      </div>
      <div class="flex flex-col align-center">
        <div
          class="flex border-2 border-solid border-gray-400 bg-gray-200 shadow-lg shadow-slate-400 rounded"
        >
          <span class="mdi mdi-bluetooth mdi-12px pt-2 px-2 hover:bg-slate-300"></span>

          <span
            class="mdi mdi-chevron-right mdi-24px p-1 px-2 hover:bg-slate-300"
            style="border-left: 1px solid rgb(148 163 184)"
          ></span>
        </div>
        <p class="text-sm pt-1">Bluetooth</p>
      </div>
      <div class="flex flex-col align-center">
        <div
          class="border-2 border-solid border-gray-400 bg-gray-200 shadow-lg shadow-slate-400 rounded py-2"
        >
          <span class="mdi mdi-airplane mdi-12px p-2 hover:bg-slate-300 px-8"></span>
        </div>
        <p class="text-sm pt-1">Plane</p>
      </div>
    </div>
    <div class="flex align-center justify-around p-3">
      <div class="flex flex-col align-center">
        <div
          class="border-2 border-solid border-gray-400 bg-gray-200 shadow-lg shadow-slate-400 rounded py-2"
        >
          <span class="mdi mdi-battery-30 mdi-12px p-2 px-8 hover:bg-slate-300"></span>
        </div>
        <p class="text-sm pt-1">Battery</p>
      </div>

      <div class="flex flex-col align-center">
        <div
          class="border-2 border-solid border-gray-400 bg-gray-200 shadow-lg shadow-slate-400 rounded py-2"
        >
          <span class="mdi mdi-brightness-6 p-2 mdi-12px hover:bg-slate-300 px-8"></span>
        </div>
        <p class="text-sm pt-1">Night Light</p>
      </div>

      <div class="flex flex-col align-center">
        <div
          class="border-2 border-solid border-gray-400 bg-gray-200 shadow-lg shadow-slate-400 rounded py-2"
        >
          <span class="mdi mdi-human mdi-12px p-2 hover:bg-slate-300 px-8"></span>
        </div>
        <p class="text-sm pt-1">Accessibility</p>
      </div>
    </div>
    <div class="flex flex-col align-center justify-center pt-2">
      <div class="w-11/12 flex align-center">
        <span class="mdi mdi-brightness-6 mdi-24px mr-3"></span>

        <v-slider hide-details></v-slider>
      </div>
      <div class="w-11/12 flex align-center">
        <span class="mdi mdi-volume-high mdi-24px mr-3 py-4"></span>

        <v-slider hide-details></v-slider>
      </div>
    </div>
    <div class="flex justify-between border-t border-slate-600 bg-slate-100 rounded p-2">
      <div class="flex align-center hover:bg-white rounded p-1">
        <span class="mdi mdi-12px" :class="{ 'mdi-battery-charging': battery?.charging }"></span>
        <span class="mdi mdi-12px" :class="{ 'mdi-battery-90': !battery?.charging }"></span>
        <p>{{ `${battery?.level * 100}%` }}</p>
      </div>
      <div class="flex align-center mt-1 mr-2">
        <span class="mdi mdi-pencil hover:bg-white p-1 rounded"></span>
        <span class="mdi mdi-cog-outline hover:bg-white rounded p-1"></span>
      </div>
    </div>
  </v-navigation-drawer>
  <!-- Date Drawer -->
  <v-navigation-drawer
    location="right"
    v-model="dateDrawer"
    temporary
    class="bg-slate-200 m-4 rounded-lg"
    style="
      height: calc(65% - 90px);
      top: 35%;
      width: 20%;
      left: 77.5%;
      background-color: rgb(226 232 240);
      transition-duration: 0.5s;
    "
  >
    <div class="flex align-center justify-between">
      <VueDatePicker v-model="date" inline auto-apply class="p-5"></VueDatePicker>
    </div>
  </v-navigation-drawer>
  <div class="home-container p-5" @click="onClickDesktop($event)">
    <div
      class="desktop-item flex flex-col align-center p-1 mt-1"
      :class="{ selected: item.active }"
      v-for="item in desktopItems"
      :key="item"
      @click="onClickItem($event, item)"
    >
      <img :src="getImageUrl(item.icon)" alt="" />
      <p class="description font-sans text-sm">{{ item.name }}</p>
    </div>
  </div>
  <v-footer color="rgb(213 214 225)" class="p-0" style="z-index: 1100">
    <v-row class="justify-between sticky" no-gutters>
      <div
        class="flex align-center mx-4 p-1 pr-8 h-100 mt-1 footer-weather"
        @click.stop="openNewsDrawer()"
      >
        <span class="mdi mdi-weather-cloudy mdi-24px"></span>
        <div class="pl-2">
          <p class="text-xs">18°C</p>
          <p class="text-xs">Çok Bulutlu</p>
        </div>
      </div>
      <div class="flex align-center">
        <img
          src="../assets//icons/win-logo.svg "
          class="w-10 hover:bg-slate-200 p-2 rounded"
          alt=""
          @click.stop="openWinDrawer()"
        />
        <v-text-field
          density="compact"
          variant="solo"
          label="Ara"
          prepend-inner-icon="mdi-magnify"
          single-line
          hide-details
          class="w-56 pl-2"
        ></v-text-field>
        <div class="hover:bg-slate-200 rounded px-2 p-1 ml-2">
          <img src="../assets/icons/mail-logo.svg" class="w-7" alt="" />
        </div>
        <div class="hover:bg-slate-200 rounded px-2 p-1 ml-1">
          <img src="../assets/icons/folder-logo.svg" class="w-7" alt="" />
        </div>
      </div>
      <div class="flex align-center p-2">
        <span
          class="mdi mdi-chevron-up mdi-24px hover:bg-slate-200 rounded px-1"
          @click.stop="openRunningApps()"
        ></span>
        <span
          class="mdi mdi-weather-cloudy mdi-18px hover:bg-slate-200 rounded p-1"
          @click.stop="openCloudDrawer()"
        ></span>
        <div class="hover:bg-slate-200 rounded p-2" @click.stop="openSettings()">
          <span class="mdi mdi-wifi mdi-12px"></span>
          <span class="mdi mdi-volume-high mdi-12px pl-2"></span>
          <span
            class="mdi mdi-12px pl-2"
            :class="{ 'mdi-battery-charging': battery?.charging }"
          ></span>
          <span class="mdi mdi-12px" :class="{ 'mdi-battery-90': !battery?.charging }"></span>
        </div>
        <div
          class="text-xs mr-4 hover:bg-slate-200 rounded px-3 p-1"
          @click.stop="openDatePicker()"
        >
          <p class="flex justify-end">{{ currentTime() }}</p>
          <p>{{ currentDate() }}</p>
        </div>
      </div>
    </v-row>
  </v-footer>
</template>
<style>
::-webkit-scrollbar {
  width: 3px;
  border-radius: 10px;
}

::-webkit-scrollbar-track {
  background: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
}

::-webkit-scrollbar-thumb {
  background: #000;
  border-radius: 10px;
}

.home-container {
  background-image: url('../assets/imgs/win11-bg.jpg');
  height: calc(100% - 57px);
  width: 100%;
  background-size: cover;
}
.home-container .desktop-item {
  @apply hover:bg-slate-300 focus:bg-slate-300 rounded w-16;
}
.selected {
  @apply bg-slate-300;
}

.selectedDrawerItems {
  @apply bg-orange-900;
}

.footer-weather:hover {
  background-color: rgb(226 232 240);
  border-radius: 5px;
  left: 0;
}
</style>
<script>
import VueDatePicker from '@vuepic/vue-datepicker'
import '@vuepic/vue-datepicker/dist/main.css'
export default {
  name: 'HomePage',
  components: { VueDatePicker },
  data: () => ({
    picker: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
      .toISOString()
      .substr(0, 10),

    battery: null,
    due: null,
    drawer: null,
    settingsDrawer: null,
    windowsDrawer: null,
    cloud: null,
    openedApps: null,
    dateDrawer: null,
    wifiItem: {
      active: false
    },
    desktopItems: [
      {
        icon: '../assets/icons/this-pc-logo.svg',
        name: 'This PC',
        active: false
      },
      {
        icon: '../assets/icons/folder-logo.svg',
        name: 'Folders',
        active: false
      }
    ]
  }),
  computed: {},
  methods: {
    closeAllDrawers() {
      this.dateDrawer = false
      this.settingsDrawer = false
      this.cloud = false
      this.openedApps = false
      this.drawer = false
      this.windowsDrawer = false
    },
    openDatePicker() {
      this.closeAllDrawers()
      this.dateDrawer = !this.dateDrawer
    },
    openSettings() {
      this.closeAllDrawers()
      this.settingsDrawer = !this.settingsDrawer
    },
    openCloudDrawer() {
      this.closeAllDrawers()
      this.cloud = !this.cloud
    },
    openRunningApps() {
      this.closeAllDrawers()
      this.openedApps = !this.openedApps
    },
    openNewsDrawer() {
      this.closeAllDrawers()
      this.drawer = !this.drawer
    },
    openWinDrawer() {
      this.closeAllDrawers()
      this.windowsDrawer = !this.windowsDrawer
    },
    getImageUrl(url) {
      return new URL(url, import.meta.url)
    },
    onClickItem(event, item) {
      event.stopPropagation()
      this.desktopItems.forEach((it) => {
        it.active = false
      })
      item.active = true
    },
    onClickDesktop() {
      this.desktopItems.forEach((it) => {
        it.active = false
      })
    },
    currentDate() {
      return new Date().toLocaleDateString().slice(0, 10).replace(/-/g, '.')
    },
    currentTime() {
      var today = new Date()
      var time = today.getHours() + ':' + today.getMinutes()
      return time
    },

    onClickDrawerSelf() {
      this.drawerItems.forEach((it) => {
        it.activeDrawer = false
      })
    },
    getBatteryInfo() {
      navigator.getBattery().then((battery) => {
        this.updateAllBatteryInfo(battery)

        battery.addEventListener('chargingchange', () => {
          this.updateChargeInfo(battery)
        })

        battery.addEventListener('levelchange', () => {
          this.updateLevelInfo(battery)
        })
      })
    },
    updateAllBatteryInfo(battery) {
      this.updateChargeInfo(battery)
      this.updateLevelInfo(battery)
    },
    updateChargeInfo(battery) {
      this.battery = battery
      console.log('updateChargeInfo battery', battery)
    },
    updateLevelInfo(battery) {
      this.battery = battery
    }
  },
  mounted() {
    this.getBatteryInfo()
  }
}
</script>
