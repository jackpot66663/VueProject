<template>
  <div class="main">
      <div class="search-section">
          <div class="filter">
              <div class="title" style="position:absolute">
                <h1 style="font-weight:bold;font-size:24px">Search Filter</h1>
              </div>
              <b-form v-if="show">
                <div class="date" style="margin-top:50px">
                  <h2>Select date:</h2>
                  <DatePicker style="position:absolute" v-model="form.time" v-on:time="getTime" required></DatePicker>
                </div>
                <div class="city" style="margin-top:130px">
                  <h2>Select city:</h2>
                  <b-form-select  style="margin-top:30px"
                    v-model="form.city" 
                    :options="citys" 
                    required
                  ></b-form-select>
                </div>
              </b-form>
          </div>
          <div class="result">
              
          </div>
      </div>
      <br>
      <b-button class="search-button" variant="primary" @submit="Search" @reset="Reset">Search</b-button>
  </div>
</template>

<script>
import DatePicker from '@/components/DateRangePicker'
import Axios from "axios";
export default {
  name: 'Home',
  components:{
    DatePicker
  },
  data () {
    return {
      form:{
        time:'',
        city:null
      },
      citys:[{text:'Select City',value:null},'Taipei','Beijing','New York'],
      show:true
    }
  },
  methods:{
    getTime(value){
      this.form.time = value;
    },
    Search(event){
      event.preventDefault
      console.log(JSON.stringify(this.form))
      this.Axios.post('/',{
        search_json:JSON.stringify(this.form)
      })
      .then(function(response){
        //todo
      })
      .catch(function(error){
          console.log(error)
      });
    },
    Reset(event){
      this.form.time= ''
      this.form.city = ''
    }
  }
}
</script>
<style scoped src="../assets/css/home.css">
</style>