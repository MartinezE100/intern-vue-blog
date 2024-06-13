<template>
    <v-app>
        <v-container class="bg-image">
            <!-- Text Section: Introduction -->
            <v-row>
                <v-col cols="4">
                    <v-card class="black-transparent" color="black">
                        <v-card-text>
                            <h1>Hi! I'm Eduardo Martinez👋</h1>
                            I'm a student pursuing a degree in Computer Science
                            and Engineering at the University of Puerto Rico
                            Mayaguez.
                            <br /><br />
                            Entering the 5th year of my program, I look forward
                            to sharing the experiences of my internship at
                            Wovenware.
                        </v-card-text>
                        <!-- Social media icons -->
                        <v-card-actions>
                            <v-btn
                                icon
                                href="https://www.facebook.com/profile.php?id=100005373247049"
                            >
                                <v-icon>mdi-facebook</v-icon>
                            </v-btn>
                            <v-btn icon href="https://github.com/MartinezE100">
                                <v-icon>mdi-github</v-icon>
                            </v-btn>
                            <v-btn
                                icon
                                href="https://www.linkedin.com/in/eduardo-martinez-3332b596/"
                            >
                                <v-icon>mdi-linkedin</v-icon>
                            </v-btn>
                            <v-spacer></v-spacer>
                            <v-btn
                                @click="
                                    $router.push({
                                        path: '/users/eduardo-martinez/posts',
                                    })
                                "
                            >
                                POSTS
                            </v-btn>
                        </v-card-actions>
                    </v-card>
                </v-col>
            </v-row>
        </v-container>
        <v-container>
            <v-card
                class="mx-auto about-me-card"
                prepend-icon="mdi-information-outline"
                subtitle="From when I was about to graduate High School."
            >
                <template v-slot:title>
                    <span class="font-weight-black">About me</span>
                </template>

                <v-card-text class="bg-surface-light pt-4">
                    My piano has been my soulmate since I was five years old.
                    Together we have transformed notes on a page to beautiful
                    music more times than I can count. Those melodies speak to
                    me and consume me as I learn to play each one; they seem to
                    transform into a warm cloak that I wear wrapped around me.
                    <br /><br />
                    Each time I began learning a new song, I found myself
                    absorbed by the melody, inspired by rhythm. Sometimes I
                    would find myself so immersed in the song that I
                    incorporated it into my daily life. My daily routine swelled
                    or slowed following the cadence for each piece.
                    <br /><br />
                    There was only one problem, every single time I started
                    learning a new song I found myself rushing through it,
                    anxious to perfect each note, wanting to reach the end and
                    be finished. I specifically remember “Für Elise,” a work
                    composed by Ludwig Van Beethoven, which I absolutely loved.
                    I just loved the tempo and the movement of my fingers as I
                    paced through the song and slowed down in crucial moments in
                    order to bring out the suspense for the audience.
                    <br /><br />
                    This beautiful piece ebbs and flows in its melody, bringing
                    the listener on its journey. As I played “Für Elise,” I
                    began to compare this melody to my life. I noticed how my
                    life was just a quick, sudden flash of every little thing,
                    nothing making its mark, nothing very significant. I was
                    rushing through life just as I rushed through the songs.
                    <br /><br />
                    “Für Elise” was my catalyst to slow down. While I practiced
                    this song to perfection, I found I didn't want it to come to
                    an end. I wanted it to continue so I could enjoy it longer.
                    As I compared the movement of the song to the passage of my
                    daily life, I knew I was missing out on the intricacies and
                    details of my life. I was in a hurry to finish, and now that
                    I am 17 and preparing for my next “composition,” I realize I
                    want to slow down.
                    <br /><br />
                    I want to enjoy every single moment of my senior year, I
                    don't want to hurry through it in any way. I know that just
                    like the end of my favorite musical piece, my high school
                    years will end, and I think I want to play this song a
                    little longer.
                </v-card-text>
            </v-card>
        </v-container>
    </v-app>
</template>

<script>
export default {
    name: "EduardoBlog",
};
</script>

<style scoped>
.bg-image {
    height: 400px;
    background-image: url("@/assets/eduardo-martinez.png");
    background-position: center;
    color: white;
}

.black-transparent {
    background-color: rgba(7, 4, 4, 0.5) !important;
}

.black-transparent .v-card-actions {
    justify-content: center;
}
</style>
