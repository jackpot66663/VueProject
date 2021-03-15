<template>
  <div>
    <date-picker 
      v-model="time" 
      valueType="format"
      :disabled-date=" date => date < disabledBefore || date > disabledAfter"
      v-on:change="getTime"
      placeholder="Select date">
    </date-picker>
  </div>
</template>

<script>
import DatePicker from 'vue2-datepicker';
import 'vue2-datepicker/index.css';
const moment = require("moment");
export default {
  name:'datepicker',
  components: { 
    DatePicker 
  },
  watch: {
    time() {
      if (this.$parent.toggleStatus !== true) {
        this.$parent.saveButton = true;
      }
    },
  },
  data() {
    return {
        time: [
          new Date(moment().subtract(1,"year")),
          new Date(moment().endOf("month")),
        ],
        disabledBefore: new Date("2020/11/01"),
        disabledAfter: new Date("2020/11/14"),
      };  
  },
  methods:{
    getTime:function(event){
      this.$emit('time',this.time)
    }
  }
}
</script>
