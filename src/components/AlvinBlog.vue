<template>
    <!-- Vue template starts here -->
    <div>
        <!-- Root element of the Vue component -->
        <v-main>
            <!-- Main content area -->
            <div style="margin: 0 150px">
                <!-- Add margin to the sides -->
                <v-container fluid style="background-color: lightgray">
                    <!-- Fluid container to stretch content -->
                    <v-row>
                        <!-- Row to contain columns -->
                        <v-col cols="9">
                            <!-- Column for posts section (75% of page) -->
                            <!-- First Post -->
                            <v-card class="post-card">
                                <!-- Title of the post -->
                                <v-card-title>Post 1</v-card-title>
                                <!-- Description of the post -->
                                <v-card-text
                                    >Description for Post 1</v-card-text
                                >
                                <!-- <img src="@/assets/logo.jpg" /> -->
                                <!-- Content of the post -->
                                <v-card-text>
                                    <p>This is the content for Post 1.</p>
                                </v-card-text>
                            </v-card>

                            <!-- Second Post -->
                            <v-card class="post-card">
                                <!-- Title of the post -->
                                <v-card-title>Post 2</v-card-title>
                                <!-- Description of the post -->
                                <v-card-text
                                    >Description for Post 2</v-card-text
                                >
                                <!-- Content of the post -->
                                <v-card-text>
                                    <p>This is the content for Post 2.</p>
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
