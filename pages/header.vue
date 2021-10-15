<template>
      <div class="header">
            <a-row>
            <a-col :xs="12" :sm="12" :md="12" :lg="12" :xl="12">
                <h3 :style="headerTitleStyles">{{headerTitle}}</h3>
            </a-col>
            <a-col :xs="12" :sm="12" :md="12" :lg="12" :xl="12">
                
            </a-col>
            </a-row>

      </div>
</template>

<script>
// import { defineComponent } from '@vue/composition-api'

export default {
    name: 'Header',
    props:{
        headerTitle: String,
    },
    data(){
        return {
            headerTitleStyles:{
            'font-weight':'bold',

            }
        }
        
    }

}
</script>
