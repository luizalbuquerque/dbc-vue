<template>
  <div class="timezone-clock">
    <h1>Fusos Horários Principais</h1>
    <ul>
      <li v-for="timezone in timezones" :key="timezone.name" class="timezone-item">
        {{ timezone.displayName }} <span class="timezone-offset">{{ timezone.offset }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      timezones: []
    };
  },
  mounted() {
    this.getTimezones();
  },
  methods: {
    getTimezones() {
      // Código para obter fusos horários omitido para simplificar
      
      this.timezones = [
      { name: 'Pacific/Midway', displayName: 'Samoa', offset: -11 },
        { name: 'Pacific/Honolulu', displayName: 'Havaí', offset: -10 },
        { name: 'America/Anchorage', displayName: 'Alasca', offset: -9 },
        { name: 'America/Los_Angeles', displayName: 'Pacific Time (EUA e Canadá)', offset: -8 },
        { name: 'America/Denver', displayName: 'Montanha Time (EUA e Canadá)', offset: -7 },
        { name: 'America/Chicago', displayName: 'Central Time (EUA e Canadá)', offset: -6 },
        { name: 'America/New_York', displayName: 'Eastern Time (EUA e Canadá)', offset: -5 },
        { name: 'America/Sao_Paulo', displayName: 'Brasília', offset: -3 },
        { name: 'Atlantic/Azores', displayName: 'Açores', offset: -1 },
        { name: 'Europe/London', displayName: 'Londres', offset: 0 },
        { name: 'Europe/Paris', displayName: 'Paris', offset: 1 },
        { name: 'Europe/Moscow', displayName: 'Moscou', offset: 3 },
        { name: 'Asia/Dubai', displayName: 'Dubai', offset: 4 },
        { name: 'Asia/Kolkata', displayName: 'Mumbai', offset: 5.5 },
        { name: 'Asia/Colombo', displayName: 'Colombo', offset: 5.5 },
        { name: 'Asia/Dhaka', displayName: 'Daca', offset: 6 },
        { name: 'Asia/Bangkok', displayName: 'Bangkok', offset: 7 },
        { name: 'Asia/Hong_Kong', displayName: 'Hong Kong', offset: 8 },
        { name: 'Asia/Tokyo', displayName: 'Tóquio', offset: 9 },
        { name: 'Australia/Brisbane', displayName: 'Brisbane', offset: 10 },
        { name: 'Pacific/Guam', displayName: 'Guam', offset: 10 },
        { name: 'Pacific/Tongatapu', displayName: 'Tonga', offset: 13 },
        { name: 'Pacific/Kiritimati', displayName: 'Line Islands (Kiribati)', offset: 14 },
      ];
    }
  }
}
</script>

<style scoped>
.timezone-clock {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-family: Arial, sans-serif;
  margin-top: 20px;
}

h1 {
  font-size: 24px;
  margin-bottom: 10px;
}

ul {
  list-style-type: none;
  padding: 0;
}

.timezone-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  border-bottom: 1px solid #ccc;
  font-size: 16px;
}

.timezone-offset {
  font-weight: bold;
}

</style>
