<script>
import Button from 'primevue/button'
import TopSection from './components/TopSection';

export default {

  components: {
    Button,
    TopSection
  },
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
        <div>
            <Button label="Submit" />
        </div>
 </template>

 <style>
 
 </style>

