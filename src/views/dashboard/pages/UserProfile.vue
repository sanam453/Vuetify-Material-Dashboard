<template>
  <v-container
    id="user-profile"
    fluid
    tag="section"
  >
  <v-row>
      <v-col
        cols="12"
        sm="6"
        lg="3"
      >
        <base-material-stats-card
          color="indigo"
          icon="mdi-facebook"
          title="Followers"
          value="+445"
          sub-icon="mdi-clock"
          sub-text="Just Updated"
        />
      </v-col>

      <v-col
        cols="12"
        sm="6"
        lg="3"
      >
        <base-material-stats-card
          color="info"
          icon="mdi-heart"
          title="Likes"
          value="8675"
          sub-icon="mdi-tag"
          sub-text="Tracked from Google Analytics"
        />
      </v-col>

      <v-col
        cols="12"
        sm="6"
        lg="3"
      >
        <base-material-stats-card
          color="indigo"
          icon="mdi-store"
          title="Proceed"
          value="$ 87887"
          sub-icon="mdi-calendar"
          sub-text="Last 24 Hours"
        />
      </v-col>

      <v-col
        cols="12"
        sm="6"
        lg="3"
      >
        <base-material-stats-card
          color="pink"
          icon="mdi-video"
          title="Bookings"
          value="765"
          sub-icon="mdi-alert"
          sub-icon-color="red"
          sub-text="Get More Space..."
        />
      </v-col>
  </v-row>
    <v-row
     justify="center"
     >
      <v-col
        cols="12"
        md="8"
      >
        <base-material-card color="indigo">
          <template v-slot:heading>
            <div class="text-h3 font-weight-light">
              Edit Profile
            </div>

            <div class="text-subtitle-1 font-weight-light">
              Complete your profile
            </div>
          </template>

          <v-form>
            <v-container class="py-0">
              <v-row>
                <v-col
                  cols="12"
                  md="4"
                >
                  <v-text-field
                    label="Company (disabled)"
                    disabled
                  />
                </v-col>

                <v-col
                  cols="12"
                  md="4"
                >
                  <v-text-field
                    class="purple-input"
                    label="User Name"
                  />
                </v-col>

                <v-col
                  cols="12"
                  md="4"
                >
                  <v-text-field
                    label="Email Address"
                    class="purple-input"
                  />
                </v-col>

                <v-col
                  cols="12"
                  md="6"
                >
                  <v-text-field
                    label="First Name"
                    class="purple-input"
                  />
                </v-col>

                <v-col
                  cols="12"
                  md="6"
                >
                  <v-text-field
                    label="Last Name"
                    class="purple-input"
                  />
                </v-col>

                <v-col
                  cols="12"
                  class="text-right"
                >
                  <v-btn
                    color="indigo"
                    class="mr-0"
                  >
                    Update Profile
                  </v-btn>
                </v-col>
              </v-row>
            </v-container>
          </v-form>
        </base-material-card>
      </v-col>
      <v-col
        cols="12"
        md="4"
      >
        <base-material-card
          class="v-card-profile"
          avatar="https://demos.creative-tim.com/vue-material-dashboard/img/marc.aba54d65.jpg"
        >
          <v-card-text class="text-center">
            <h6 class="display-h4 mb-1 grey--text">
              CEO / CO-FOUNDER
            </h6>

            <h4 class="display-h3 font-weight-light mb-3 black--text">
              Alec Thompson
            </h4>

            <p class="font-weight-light grey--text">
              Don't be scared of the truth because we need to restart the human foundation in truth And I love you like Kanye loves Kanye I love Rick Owens’ bed design but the back is...
            </p>

            <v-btn
              color="info"
              rounded
              class="mr-0"
            >
              Follow
            </v-btn>
          </v-card-text>
        </base-material-card>
      </v-col>

        <v-row
         v-for="card in sideCard"
          :key="card.avatar"
          >
                <template>
  <v-card
    class="mx-auto"
    max-width="350"
  >
      <v-img
      height="270"
      :src="card.avatar"
    ></v-img>
        <div class="mx-5 mt-5 mb-2 font-weight-bold">
          {{ card.title }}
        </div>
            <div class="pl-5">{{ card.content }}</div>
    <v-card-actions>
      <v-btn
       class="pink ml-3"
       small
       >
        Button
      </v-btn>
    </v-card-actions>
  </v-card>
  </template>
  </v-row>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        sideCard: [
          { avatar: 'avatar-4.png', title: 'Headline 6', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.' },
          { avatar: 'avatar-4.png', title: 'Headline 7', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.' },
          { avatar: 'avatar-4.png', title: 'Headline 8', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.' },
        ],
      }
    },
  }
</script>
