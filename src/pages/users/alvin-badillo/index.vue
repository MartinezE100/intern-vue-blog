<template>
    <!-- Main content area -->
    <v-container style="background-color: grey">
        <!-- First section -->
        <v-container style="margin-bottom: 10vh">
            <v-row>
                <!-- Left column for image -->
                <v-col cols="12" md="6" class="text-center">
                    <v-avatar size="400">
                        <!-- Adjust the size here -->
                        <v-img
                            src="../../../assets/alvin-badillo-picture.jpg"
                            alt="Your Image"
                            class="avatar-image"
                        />
                    </v-avatar>
                </v-col>
                <!-- Right column for text content -->
                <v-col
                    cols="12"
                    md="6"
                    class="d-flex justify-center align-center"
                >
                    <v-card
                        color="transparent"
                        flat
                        class="d-flex flex-column align-center justify-center"
                    >
                        <v-card-text class="text-center">
                            <h4>Hello, I'm</h4>
                            <h1>Alvin Badillo Ramos</h1>
                            <h3>Software Developer Intern @Wovenware</h3>
                        </v-card-text>
                        <v-card-actions>
                            <v-btn icon href="https://github.com/AlvinBadillo">
                                <v-icon>mdi-github</v-icon>
                            </v-btn>
                            <v-btn
                                @click="
                                    $router.push({
                                        path: '/users/alvin-badillo/posts',
                                    })
                                "
                            >
                                POSTS
                            </v-btn>
                            <v-btn
                                icon
                                href="https://www.linkedin.com/in/alvin-y-badillo-ramos/"
                            >
                                <v-icon>mdi-linkedin</v-icon>
                            </v-btn>
                        </v-card-actions>
                    </v-card>
                </v-col>
            </v-row>
        </v-container>
        <!-- Second section -->
        <v-row>
            <v-col cols="12" sm="6">
                <v-card
                    class="mx-auto about-me-card"
                    prepend-icon="mdi-account"
                    subtitle=""
                >
                    <template v-slot:title>
                        <span class="font-weight-black">Who am I?</span>
                    </template>
                    <v-card-text class="bg-surface-light pt-4">
                        I'm Alvin Badillo, I'm a rising 4th year computer
                        science and engineering student at University of Puerto
                        Rico. Currently I'm taking part in my first internship
                        at Wovenware as a Software Developer Intern, marking my
                        debut to the tech industry.
                        <br /><br />
                        Although I will start my fourth year in collage, it's
                        only my second year as a computer science and
                        enginnering mayor. As of now, I'm working every day to
                        become a better software developer so when I graduate I
                        can join the industry as a full time developer. I've
                        always strived to be the best at whatever it is that I
                        am doing, and this is no different. The sky is the
                        limit!
                    </v-card-text>
                </v-card>
            </v-col>
            <v-col cols="12" sm="6">
                <v-card
                    class="mx-auto about-me-card"
                    prepend-icon="mdi-laptop"
                    subtitle=""
                >
                    <template v-slot:title>
                        <span class="font-weight-black"
                            >What's my background?</span
                        >
                    </template>
                    <v-card-text class="bg-surface-light pt-4">
                        I was born and raised in Puerto Rico, I've lived all my
                        life in Quebradillas until I graduated from high school
                        that I had to move to Mayaguez to go to college. I've
                        been involved in sports since I was little. Although I
                        played many sports, the one I played the most was
                        basketball, where I palyed in various turnaments and
                        played in high school team.
                        <br /><br />
                        In addition to my love for sports, I also love music. I
                        first learned to play drums at the age of 14, later on I
                        learned how to play the guitar, then the bass and now
                        I'm learning piano. Everyone in my family is a musician,
                        I guess it runs in the blood.
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<style></style>
