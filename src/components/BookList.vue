<!--BookList.vue-->
<template>
    <div class="container">
        <div>
            <div class="row">
                <div class="col-md-4 mb-5" v-for="(book, i) in books" :key="i">
                    <book-card :book-data="book">
                        <template v-slot>
                            <button class="btn-primary">Read more</button>
                        </template>
                        <template v-slot:preview="slotProps"> 
                          <a :href="slotProps.previewSlug"><button class="btn-secondary ml-3">Preview</button></a>
                        </template>
                    </book-card>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import BookCard from './BookCard.vue'

export default {
    components: {
        BookCard
    },
    data(){
        return {
            books: [
                {
                    'author': 'David Deustch',
                    'title': 'The beginning of Infinity',
                    'description': 'A book on philosphy about the origins of man',
                    'img_url': 'https://placeimg.com/640/480/any'
                },
                {
                    'author': 'Paul Coelho',
                    'title': 'The Alchemist',
                    'description': 'The true search for one\'s treasure',
                    'img_url': 'https://placeimg.com/640/480/any'
                },
                {
                    'author': 'Susan Kaye Quinn',
                    'title': 'Open Minds',
                    'description': 'Sci-Fi Futuristic book about mind reading',
                    'img_url': 'https://placeimg.com/640/480/any'
                },
                {
                    'author': 'Robert Kiyosaki',
                    'title': 'Rich Dad, Poor Dad',
                    'description': 'Motivational book on wealth building',
                    'img_url': 'https://placeimg.com/640/480/any'
                },
                {
                    'author': 'Dan Brown',
                    'title': 'The Da Vinci Code',
                    'description': 'Conspiracy theories about secrets of the holy grail',
                    'img_url': 'https://placeimg.com/640/480/any'
                },
                {
                    'author': 'Arthur Hailey',
                    'title': 'The money changers',
                    'description': 'Travel back in time and experience the banking system',
                    'img_url': 'https://placeimg.com/640/480/any'
                },
            ]
        }
    }
}
</script>