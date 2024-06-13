<template>
    <v-container>
        <v-row justify="center">
            <v-col cols="12" md="8">
                <!-- Header -->
                <v-card class="mb-4">
                    <v-card-title>
                        <span class="headline">Eduardo Martinez's Blog</span>
                    </v-card-title>
                    <v-card-subtitle
                        >Intern - Software Developer I</v-card-subtitle
                    >
                </v-card>

                <!-- Blog Posts -->
                <v-card class="mb-4" v-for="post in posts" :key="post.title">
                    <v-img :src="post.image" height="200px"></v-img>
                    <v-card-title>{{ post.title }}</v-card-title>
                    <v-card-subtitle>{{ post.date }}</v-card-subtitle>
                    <v-card-text>{{ post.excerpt }}</v-card-text>
                    <v-card-actions>
                        <v-btn text @click="readMore(post.title)"
                            >Read More</v-btn
                        >
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import { ref } from "vue";

export default {
    setup() {
        // Sample blog posts data
        const posts = ref([
            {
                id: 1,
                title: "Internship Log - Week 1",
                subtitle: "Training Week Overview",
                date: "June 1, 2024",
                excerpt:
                    "A brief introduction to the new Composition API in Vue 3...",
                image: "@/assets/eduardo-martinez.png",
            },
            {
                id: 2,
                title: "Getting Started with Vuetify",
                date: "May 15, 2024",
                excerpt:
                    "Learn how to quickly set up Vuetify in your Vue project...",
                image: "https://via.placeholder.com/600x200",
            },
            // Add more posts as needed
        ]);

        const readMore = (postTitle) => {
            // Handle read more action, e.g., navigate to a detailed post page
            console.log(`Read more about post: ${postTitle}`);
        };

        return { posts, readMore };
    },
};
</script>

<style scoped>
.headline {
    font-weight: bold;
}
</style>
