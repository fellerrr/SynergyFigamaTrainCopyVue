<template>
    <v-container>
      <v-col align="center">
        <v-col align="center">
          <PricingSelect @setType="setType" />
          <h1>Pricing</h1>
        </v-col>
        <div class="card">
          <PricingCard :data="data[type][0]"/>
          <PricingCard :data="data[type][1]"/>
          <PricingCard :data="data[type][2]"/>
        </div>
      </v-col>
    </v-container>
  
</template>

<script>
export default {
  data(){
    return{
      type:0,
     data: [
                [
                    {
                        title: 'Starter',
                        price: "Free",
                        color: 'grey',
                        time: 'Forever',
                        features: [
                            '3 Figma and 3 FigJam files',
                            'Unlimited personal files',
                            'Unlimited collaborators',
                            'Plugins, widgets, and templates',
                            'Mobile app',
                        ],
                    },
                    {
                        title: 'Starter',
                        price: "Free",
                        color: 'green',
                        time: 'Forever',
                        features: [
                            'Unlimited Figma files',
                            'Unlimited version history',
                            'Sharing permissions',
                            'Shared and private projects',
                            'Team libraries',
                            'Audio conversations',
                        ],
                    },
                    {
                        title: 'Starter',
                        price: "Free",
                        color: 'blue',
                        time: 'Forever',
                        features: [
                            'Org-wide libraries',
                            'Design system analytics',
                            'Branching and merging',
                            'Centralized file management',
                            'Unified admin and billing',
                            'Private plugins and widgets',
                            'Single sign-on',
                        ],
                    },
                ],
                [
                    {
                        title: 'Starter',
                        price: "Free",
                        color: 'grey',
                        time: 'Forever',
                        features: [
                            '3 Figma and 3 FigJam files',
                            'Unlimited personal files',
                            'Unlimited collaborators',
                            'Plugins and templates',
                            'Mobile app',
                        ],
                    },
                    {
                        title: 'Starter',
                        price: "Free",
                        color: 'orange',
                        time: 'Forever',
                        features: [
                            'Unlimited FigJam files',
                            'Open sessions',
                            'Sharing permissions',
                            'Team libraries',
                            'Audio conversations',
                        ],
                    },
                    {
                        title: 'Starter',
                        price: "Free",
                        color: 'violet',
                        time: 'Forever',
                        features: [
                            'Org-wide libraries',
                            'Centralized content management',
                            'Unified admin and billing',
                            'Private plugins and widgets',
                            'Single sign-on',
                        ],
                    },
                ],
            ],
        };
    },

  methods: {
    setType(type){
      this.type=type
    }
  }
}
</script>

<style scoped>
  .card{
    display:grid;
    grid-template-columns: repeat(3,1fr);
    gap:32px;
    margin: 80px auto 40px;
  }
</style>
