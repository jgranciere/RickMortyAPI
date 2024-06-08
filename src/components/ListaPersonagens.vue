<script setup>
import { onMounted, reactive, ref } from 'vue';

defineProps([
    "personagem"
])

</script>

<template>
    <div class="col">
        <div class="card m-3">
            <div class="row g-0">
                <div class="col-md-4">
                    <img :src="personagem.image" class="img-fluid rounded-start" alt="...">
                </div>
                <div class="col-md-8" style="background-color: #052405;">
                    <div class="card-body" style="background-color: #052405;">
                        <h5 class="card-title" style="color: white;">{{ personagem.name }}</h5>
                        <p class="card-text" style="color: white;">
                            Status: {{ personagem.status }} <br>
                            Espécie: {{ personagem.species }} <br>
                            Gênero: {{ personagem.gender }} <br>
                            Local: {{ personagem.location.name }} <br>
                            Total De episódios: {{ personagem.episode.length }} <br>
                        </p>

                    </div>
                </div>
            </div>
        </div>
    </div>
</template>