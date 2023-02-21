<script>
import Button from 'primevue/button'
import InputText from 'primevue/inputtext'
import Calendar from 'primevue/calendar'
import Checkbox from 'primevue/checkbox'
import TopSection from './components/TopSection'

export default {

  components: {
    Button,
    InputText,
    Calendar,
    Checkbox,
    TopSection
  },
  data() {
    return {
        firstName: '',
        lastName: '',
        middleName: '',
        addCapability: false,
        date: new Date(),
        components: [TopSection]
    }
  },
  methods: {
     addCapabilitySection(){
        this.components.push(TopSection)
    } 
  },
  watch: {
    
  }
}
</script>

 
 <template>

     <h2>Hello! World</h2>
        <div class="grid">
            <div class="col-6">
                <p>Test</p>
            </div>
                
            <div class="col-6">
            <TopSection />
                <p>Test 2</p>
            </div>
        </div>
        <div class="grid">
            <div class="col-3">
               <div class="form-control">
                    <label for="firstName">First Name</label>
                    <InputText id="firstName" type="text" placeholder="First Name" v-model="firstName"/>
               </div>
            </div>
                
            <div class="col-3">
                <div class="form-control">
                    <label for="firstName">Middle Name</label>
                    <InputText id="middleName" type="text" placeholder="Middle Name" v-model="middleName"/>
               </div>
            </div>
               <div class="col-3">
                <div class="form-control">
                    <label for="firstName">Last Name</label>
                    <InputText id="lastName" type="text" placeholder="Last Name" v-model="lastName"/>
               </div>
            </div>
               <div class="col-3">
               <div class="form-control">
                    <label for="date">Date</label>
                    <Calendar v-model="date" id="date" />
               </div>
            </div>
        </div>
        <div class="grid">
            <div class="col-3">
                <label for="capability">Add capability</label>
                <Checkbox v-model="addCapability" :binary="true" @click="addCapabilitySection" />
            </div>
        </div>
        <component v-for="(component, index) in components"
        :key="index"
        :is="component"/>

        <div>
            <Button label="Submit" />
        </div>
        <h2>checking github</h2>
 </template>

 <style scoped>

input, label {
    display:block;
    box-sizing:border-box;
    width: 100%;
}

 </style>

