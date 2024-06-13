<template>
    <v-container>
        <!-- Section Title -->
        <v-row justify="center" class="mt-8 mb-4">
            <v-col cols="12">
                <h2 class="text-center">Eduardo Martinez's Posts</h2>
            </v-col>
        </v-row>
        <v-row justify="center">
            <v-col v-for="post in posts" :key="post.title" cols="12" md="4">
                <!-- Blog Posts -->
                <div class="clickable-card" @click="showPost(post)">
                    <v-card class="mx-auto mb-4">
                        <v-img :src="post.image"></v-img>
                        <v-card-title>{{ post.title }}</v-card-title>
                        <v-card-subtitle
                            >{{ post.subtitle }} |
                            {{ post.date }}</v-card-subtitle
                        >
                        <v-card-text>{{ post.excerpt }}</v-card-text>
                    </v-card>
                </div>
            </v-col>
        </v-row>

        <!-- Overlay Dialog -->
        <v-dialog v-model="dialog" max-width="1000px">
            <v-container>
                <v-card class="mx-auto" prepend-icon="mdi-information-outline">
                    <template v-slot:title>
                        <span class="font-weight-black">{{
                            selectedPost.title
                        }}</span>
                    </template>

                    <v-card-subtitle
                        >{{ selectedPost.subtitle }} |
                        {{ selectedPost.date }}</v-card-subtitle
                    >
                    <v-card-text class="bg-surface-light pt-4">
                        <div v-html="selectedPost.content"></div>
                    </v-card-text>
                    <v-card-actions class="bg-surface-light">
                        <v-spacer></v-spacer>
                        <v-btn text @click="dialog = false">Close</v-btn>
                    </v-card-actions>
                </v-card>
            </v-container>
        </v-dialog>
    </v-container>
</template>

<script>
import { ref } from "vue";
import internIcon from "@/assets/internIcon.png";

export default {
    setup() {
        const dialog = ref(false);
        const selectedPost = ref({});

        const posts = ref([
            {
                title: "Internship Log - Week 1",
                subtitle: "Training Week Overview",
                date: "June 7, 2024",
                excerpt:
                    "This week marked the beginning of my internship, dedicated to training and getting up to speed...",
                content: `
                    This week marked the beginning of my internship, dedicated to training and getting up to 
                    speed with the tools and technologies we will be using. The primary focus was on Java and 
                    Vue.js through a series of assigned course videos.

                    <br /><br />

                    <h4>Java Training:</h4>

                    I have previous experience with Java, so most of the content was familiar. It was beneficial 
                    to revisit the material, as it helped reinforce my understanding and reminded me of a few 
                    concepts I had forgotten or wasn't completely confident about.

                    <br /><br />

                    <h4>Vue.js Training:</h4>

                    This was my first time working with Vue.js, making the learning process both challenging 
                    and exciting. I enjoyed exploring the new framework and understanding its functionalities 
                    and applications.

                    <br /><br />

                    <h4>Challenges Faced</h4>

                    1. Outdated Vue.js Course Material

                    <br /><br />

                    A significant portion of the Vue.js course videos were outdated, relying on deprecated 
                    code and old software versions. This discrepancy made it difficult to follow along with 
                    the coding examples, leading to unnecessary time spent troubleshooting and fixing issues. 
                    Recommendation: Updating these course modules would streamline the learning process, 
                    making it more efficient and less frustrating for new learners.

                    <br /><br />

                    2. Internship Status Issue

                    <br /><br />
                    
                    My internship status was mistakenly marked as terminated and then reactivated on the 
                    website. This error prevented me from clocking in or out, requiring my supervisor to 
                    manually log my hours. While not a major problem, it was inconvenient as I couldn't 
                    track my hours in real-time or access them easily.

                    <br /><br />
                    Despite these challenges, the first week was productive and set a solid foundation 
                    for the upcoming weeks. I’m looking forward to applying what I’ve learned and tackling
                     new projects as the internship progresses.
                `,
                image: internIcon,
            },
        ]);

        const showPost = (post) => {
            selectedPost.value = post;
            dialog.value = true;
        };

        return { posts, dialog, selectedPost, showPost };
    },
};
</script>

<style scoped>
.clickable-card {
    cursor: pointer;
    display: block;
    transition: transform 0.2s, box-shadow 0.2s;
}

.clickable-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}
</style>
