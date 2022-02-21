<template>
  <v-container>
    <v-row justify="center" class="mt-16">
      <v-col  md="6">
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
      </v-col>
      <v-col  md="5">
        <h1>Airlines</h1>
      </v-col>
      <v-col  md="1">
        <v-btn class="mx-2" fab dark small color="pink">
          <v-icon dark> mdi-magnify </v-icon>
        </v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col md="8">
        <v-card elevation="0">
          <v-img src="2.jpg" ></v-img>
          <v-row>
            <v-col md="10"> <v-card-text>Photography</v-card-text> </v-col>
            <v-col md="2"> <v-card-text>Colorado</v-card-text> </v-col>
          </v-row>
          <v-card-title
            >Paradise Search : An Apartment In Helsinki, Finland</v-card-title
          >
          <v-divider></v-divider>
          <v-card-text style="text-align: justify"
            >Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
            aliquip ex ea commodo consequat. Lorem ipsum dolor sit amet
            consectetur adipisicing elit. Dolores accusamus quae fugiat
            voluptates consequuntur repellendus eaque, modi non fuga, dolor
            repudiandae deserunt molestias velit veritatis provident quod, ipsum
            tempore omnis.</v-card-text
          >
          <v-divider></v-divider>
          <v-card-title>Colorado</v-card-title>
          <v-row>
            <v-col md="6">
              <v-card-text style="text-align: justify"
                >Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                Ducimus, magnam dolorem optio, excepturi praesentium, atque
                ipsam quae ea repellendus animi blanditiis veniam! Maxime ea
                deleniti perspiciatis ipsum ratione voluptas consequatur. Lorem
                ipsum dolor, sit amet consectetur adipisicing elit. Quam iste
                eveniet tempore amet architecto commodi dolor nesciunt, cum
                nisi, facere magnam voluptatem aperiam, incidunt natus dolores
                voluptatibus odit tenetur quas. Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Maiores, suscipit ex ullam ipsam
                culpa autem aspernatur ipsa libero aperiam deserunt facilis eum
                inventore dolor veritatis, voluptates at nam, eius iure! Lorem,
                ipsum dolor sit amet consectetur adipisicing elit. Ipsum
                corporis sint harum amet, fuga perferendis, accusantium ratione
                ipsam sequi ea porro velit at labore ullam ut tenetur veritatis
                voluptas. Accusantium?</v-card-text
              >
            </v-col>
            <v-col md="6">
              <v-img src="2.jpg" class="ma-3"></v-img>
            </v-col>
          </v-row>
          <v-divider></v-divider>
          <v-card-title>Colorado</v-card-title>
          <v-row>
            <v-col  md="6">
              <v-img class="ma-3" src="2.jpg"></v-img>
            </v-col>
            <v-col md="6">
              <v-card-text style="text-align: justify"
                >Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                Ducimus, magnam dolorem optio, excepturi praesentium, atque
                ipsam quae ea repellendus animi blanditiis veniam! Maxime ea
                deleniti perspiciatis ipsum ratione voluptas consequatur. Lorem
                ipsum dolor, sit amet consectetur adipisicing elit. Quam iste
                eveniet tempore amet architecto commodi dolor nesciunt, cum
                nisi, facere magnam voluptatem aperiam, incidunt natus dolores
                voluptatibus odit tenetur quas. Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Maiores, suscipit ex ullam ipsam
                culpa autem aspernatur ipsa libero aperiam deserunt facilis eum
                inventore dolor veritatis, voluptates at nam, eius iure! Lorem,
                ipsum dolor sit amet consectetur adipisicing elit. Ipsum
                corporis sint harum amet, fuga perferendis, accusantium ratione
                ipsam sequi ea porro velit at labore ullam ut tenetur veritatis
                voluptas. Accusantium?</v-card-text
              >
            </v-col>
          </v-row>
        </v-card>
        <v-row>
          <v-col md="9">
            <v-card-title class="white--text">Comments</v-card-title>
          </v-col>
        
        </v-row>
        <v-card elevation="0" tile>
          <v-row>
            <v-col class="mt-4" md="3">
              <v-avatar class="ml-16" color="primary"> 
                <v-img src="2.jpg"></v-img>
              </v-avatar>
              <v-card-text class="ml-6"
                >Jeevan Shrestha <br />
                June 1, 2016
              </v-card-text>
            </v-col>
            <v-col class="mt-4" cols="12" md="9">
              <v-card-text style="text-align: justify"
                >Nullam eu eros purus. Vestibulum in aliquam nisl. Pellentesque
                condimentum egestas hendrerit. Aliquam erat volutpat. Aliquam
                lobortis hendrerit odio suscipit placerat. Mauris tincidunt,
                sapien in sagittis cursus, mauris arcu ullamcorper neque, vel
                tristique ex metus sed mi. Nulla blandit maximus odio id
                gravida.</v-card-text
              >
            </v-col>
          </v-row>
        </v-card>
        <v-card class="mt-10 mb-16">
          <v-container
            ><v-card-title>Leave A Reply</v-card-title>
            <v-card-text
              >Your email address will not be published. Required fields are
              marked *</v-card-text
            >
            <v-textarea class="ma-3" label="Comment" outlined></v-textarea>
            <v-row>
              <v-col cols="12" md="4">
                <v-text-field
                  class="ml-3"
                  label="Your Name*"
                  outlined
                ></v-text-field>
              </v-col>
              <v-col cols="12" md="4">
                <v-text-field label="Your Email*" outlined></v-text-field>
              </v-col>
              <v-col cols="12" md="4">
                <v-text-field
                  class="mr-3"
                  label="Address"
                  outlined
                ></v-text-field>
              </v-col>
            </v-row>
            <v-btn height="3em" tile class="ml-3 white--text" color="#24cb83"
              >Post Comment</v-btn
            ></v-container
          >
        </v-card>
      </v-col>
      <v-col md="4">
        <v-card elevation="0" tile>
          <v-container>
            <v-card-title>About Me</v-card-title>
          <v-img src="4.jpg"> </v-img>
          <v-card-title>I'm Susanna, I blog about travel.</v-card-title>
          <v-card-text style="text-align: justify">This season, the American designer will showcase a series of historic objects from the New York museum's.</v-card-text>
          </v-container>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style></style>
