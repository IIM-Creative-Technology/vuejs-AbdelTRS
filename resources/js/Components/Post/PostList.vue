<template>
    <table class="min-w-full divide-y divide-gray-200">
        <thead class="bg-gray-50">
        <tr>
            <th scope="col"
                class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">
                Name
            </th>
            <th scope="col"
                class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">
                Slug
            </th>
            <th scope="col"
                class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">
                Content
            </th>
            <th scope="col"
                class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">
                Publié ?
            </th>
            <th scope="col" class="relative px-6 py-3">
                <span class="sr-only">Editer</span>
                <span class="sr-only">Supprimer</span>
            </th>
        </tr>
        </thead>
        <tbody>
            <post-list-item v-for="post in posts" :key="post.id" :post="post" />
        </tbody>
    </table>
</template>

<script>
import PostListItem from "@/Components/Post/PostListItem";
export default {
    components: {PostListItem},
    props: [ 'posts' ]
}
</script>
