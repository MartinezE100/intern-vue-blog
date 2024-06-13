<template>
    <v-container>
        <v-row>
            <!-- Loop through each user and generate a card -->
            <v-col v-for="user in users" :key="user.id" cols="12" md="6">
                <v-card class="mx-auto mb-4" :width="cardWidth">
                    <template v-slot:title>
                        <span class="font-weight-black">{{ user.name }}</span>
                    </template>
                    <v-card-subtitle>{{ user.subtitle }}</v-card-subtitle>
                    <v-card-text class="bg-surface-light pt-4">
                        {{ user.description }}
                    </v-card-text>
                    <v-card-actions>
                        <!-- Button to view user's posts -->
                        <v-btn color="primary" @click="viewPosts(user)"
                            >View {{ user.name }}'s Blog</v-btn
                        >
                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import { ref } from "vue";
import { useRouter } from "vue-router/auto";

export default {
    setup() {
        const router = useRouter();

        const users = ref([
            {
                id: 1,
                name: "Eduardo Martinez",
                subtitle: "Intern - Software Developer I",
                description: "University Student at UPRM",
            },
            {
                id: 2,
                name: "Alvin Badillo",
                subtitle: "Intern - Software Developer I",
                description: "University Student at UPRM",
            },
        ]);

        const cardWidth = 400;

        const viewPosts = (user) => {
            // Transform the user's name to lowercase and replace spaces with dashes
            const formattedName = user.name.toLowerCase().replace(/\s+/g, "-");

            // Redirect to user's posts page
            router.push(`/users/${formattedName}/`);
        };

        return { users, cardWidth, viewPosts };
    },
};
</script>
