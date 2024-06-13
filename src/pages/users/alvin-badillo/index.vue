<template>
    <!-- Main content area -->
    <v-container class="about-content" style="margin-top: 10vh">
        <!-- First section -->
        <v-container class="section">
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
                <v-col cols="12" md="6" class="text-column">
                    <h4 class="text-center">Hello, I'm</h4>
                    <h1 class="text-center name">Alvin Badillo Ramos</h1>
                    <h3 class="text-center">
                        Software Developer Intern @Wovenware
                    </h3>
                </v-col>
            </v-row>
        </v-container>
        <!-- Second section -->
        <v-card class="section">
            <h1>Current Projects and Technologies</h1>
            <p>
                Currently, I'm working on several exciting projects, including a
                web-based application using Vue.js. I'm also exploring the world
                of artificial intelligence and machine learning, fascinated by
                its potential to revolutionize various industries.
            </p>
            <p>
                In addition to my technical projects, I'm passionate about
                sharing my knowledge with others. I frequently contribute to
                open-source projects and participate in community events to help
                others learn and grow in their programming journey.
            </p>
            <p>
                In addition to my technical projects, I'm passionate about
                sharing my knowledge with others. I frequently contribute to
                open-source projects and participate in community events to help
                others learn and grow in their programming journey.
            </p>
            <p>
                In addition to my technical projects, I'm passionate about
                sharing my knowledge with others. I frequently contribute to
                open-source projects and participate in community events to help
                others learn and grow in their programming journey.
            </p>
        </v-card>
    </v-container>
</template>

<style>
/* CSS styles for the AboutMe component */
.about-content {
    height: 100vh; /* Set height to fill the entire viewport */
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: lightgray;
}

.text-column {
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.section {
    margin-bottom: 40px; /* Add margin between sections */
}

.section h1,
.section p {
    max-width: 600px; /* Limit width of paragraph */
}

.text-center {
    text-align: center;
}

.name {
    font-size: 2.5rem; /* Adjust the font size as needed */
}
</style>
