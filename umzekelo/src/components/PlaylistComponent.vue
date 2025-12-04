<script>
    export default{
        data(){
            return{
                playlist: [
                    {
                    "id": 1,
                    "title": "Ayina Chorus",
                    "artist": "Mshoza",
                    "cover_art": "https://tse1.mm.bing.net/th/id/OIP.yUPRbu8dTR7Hj5PXgq4OsAHaHa?o=7&cb=ucfimg2&rm=3&ucfimg=1&rs=1&pid=ImgDetMain&o=7&rm=3"
                    },
                    {
                    "id": 2,
                    "title": "Bruce Lee",
                    "artist": "Chris Brown",
                    "cover_art": "https://i.ytimg.com/vi/HpEF6TrXlQE/sddefault.jpg"
                    },
                    {
                    "id": 3,
                    "title": "staysem",
                    "artist": "SIZA M",
                    "cover_art": "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRTOQLRlizexgO3MMtLqf7Aa23RpVyFcVWfNg&s"
                    },
                    {
                    "id": 4,
                    "title": "Nonchalant",
                    "artist": "Daliwonga",
                    "cover_art": "https://i1.sndcdn.com/artworks-3OwlLI2jbdpx-0-t500x500.jpg"
                    }
                ]
            }
        }
    }
</script>

<template>
    <div class="container">
        <div class="cards">
            <div class="card" style="width: 18rem;" v-for="song in playlist" :key="song.id">
                <img :src="song.cover_art" class="card-img-top" :alt="song.title">
                <div class="card-body">
                    <h5 class="card-title">{{song.title}}</h5>
                    <a href="#" class="btn btn-primary">{{song.artist}}</a>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
    .cards{
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 30px
    }

    .container{
        padding-left: 250px;
    }
</style>