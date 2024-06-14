<template>
    <!-- Vue template starts here -->
    <div>
        <!-- Root element of the Vue component -->
        <v-main>
            <!-- Main content area -->
            <div style="margin: 0 150px">
                <!-- Add margin to the sides -->
                <v-container fluid style="background-color: gray">
                    <!-- Fluid container to stretch content -->
                    <v-row>
                        <!-- Row to contain columns -->
                        <v-col cols="9">
                            <!-- Column for posts section (75% of page) -->
                            <!-- First Post -->
                            <v-card class="post-card">
                                <!-- Title of the post -->
                                <v-card-title>Week 1</v-card-title>
                                <!-- Description of the post -->
                                <v-card-text>Training Week!</v-card-text>

                                <!-- Content of the post -->
                                <v-card-text>
                                    During our first week, we embarked on a
                                    journey of preparation, beginning with the
                                    essential onboarding process. Our inaugural
                                    day was dedicated to acquainting ourselves
                                    with the team and familiarizing ourselves
                                    with the office environment. We received our
                                    badge IDs and were equipped with the
                                    necessary tools, including our assigned
                                    computers for the duration of the
                                    internship.
                                    <br /><br />
                                    <!-- <img src="@/assets/alvin-badillo-picture.jpg" /> -->
                                    <v-img
                                        src="../assets/alvin-badillo-id.jpeg"
                                        height="400"
                                    ></v-img>
                                    <br /><br />
                                    Following the onboarding process, we delved
                                    into an intensive training program to
                                    sharpen our skills for the upcoming project.
                                    Pluralsight served as our primary platform
                                    for learning, providing a comprehensive
                                    array of resources. The initial two days of
                                    training were dedicated to Java, the
                                    backbone of the project's backend.
                                    Subsequently, we devoted the remaining two
                                    days to mastering Vue, a crucial frontend
                                    development tool pivotal to crafting the
                                    user interface of our application.
                                    <br /><br />
                                    Recomendations: During the training
                                    sessions, I found the content to be valuable
                                    and necessary for our project preparation.
                                    However, it's worth noting that some of the
                                    resources provided were outdated. This posed
                                    challenges as the technologies covered in
                                    these resources were no longer operational
                                    or up-to-date. As a result, it hindered our
                                    ability to effectively follow along and
                                    apply the concepts learned in real-world
                                    scenarios.
                                </v-card-text>
                            </v-card>

                            <!-- Second Post -->
                            <v-card class="post-card">
                                <!-- Title of the post -->
                                <v-card-title>Week 2</v-card-title>
                                <!-- Description of the post -->
                                <v-card-text
                                    >Practice and development of
                                    demo</v-card-text
                                >
                                <!-- Content of the post -->
                                <v-card-text>
                                    Entering the second week, we commenced with
                                    our initial meeting alongside the team we'll
                                    be collaborating with. The atmosphere was
                                    incredibly welcoming, and everyone was
                                    exceptionally helpful! This week, we'll
                                    leverage our recently acquired expertise in
                                    Vue.js to craft a demo illustrating the
                                    potential appearance of the final product.
                                    Our project entails developing the frontend
                                    portion of an application named AppQuiz.
                                    Thus, I've chosen to sketch a layout for the
                                    "Quizzes" page, drawing inspiration from
                                    Figma's documentation.
                                    <br /><br />
                                    <v-img
                                        src="../assets/quizz-page-demo.png"
                                        height="400"
                                    ></v-img>
                                    <br /><br />
                                    This was done using vue, specifically
                                    vuetify which is a great tool for frontend
                                    development. I am happy with how this turned
                                    out given the fact that it was the first
                                    time that I've developed a web application
                                    from scratch.
                                    <br /><br />
                                    After we finished the demo for QuizzApp, we
                                    decided to build this beatiful blog so we
                                    could documment our time here in Wovenware
                                    as Software Developer Interns.
                                </v-card-text>
                            </v-card>
                            <!-- Add more posts as needed -->
                        </v-col>

                        <!-- Other Information Section (25% of page) -->
                        <v-col cols="3">
                            <!-- Column for other information section -->
                            <v-card>
                                <!-- Card for other information -->
                                <v-card-title>Featured Item</v-card-title>
                                <!-- Title of the featured item -->
                                <v-card-text>
                                    <!-- Description of the featured item -->
                                    <p>This is a dummy featured item.</p>
                                </v-card-text>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-container>
            </div>
        </v-main>
    </div>
</template>

<script>
export default {
    // JavaScript logic for the Vue component
    name: "BlogPage", // Component name
};
</script>

<style>
/* CSS styles for the Vue component */
.post-card {
    /* Styling for adding space between posts */
    margin-bottom: 20px; /* Adjust the value as needed */
}
</style>
