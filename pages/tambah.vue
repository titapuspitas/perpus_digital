<template>
    <div>
        <h2>isi buku tamu</h2>
        <form>
            <input v-model="form.nama" type="text" placeholder="nama" required> <br>
            <select v-model="form.anggota">
                <option value="">pilih keanggotaan</option>
                <option v-for="a in anggota" :key="a.id" :value="a.id">{{ a.nama }}</option>
            </select> <br>
            <textarea v-model="form.keperluan" cols="30"  rows="10" placeholder="keperluan"></textarea> <br>
            <button type="sumbit">kirim</button>
            <nuxt-link to="back"> - kembali</nuxt-link>
        </form>
    </div>
</template>

<script setup>
const supabase=useSupabaseClient()
const anggota=ref([])
const form=reactive({
    nama: "",
    anggota: "",
    keperluan: "",
})

async function getAnggota() {
    const { data,error } = await supabase.from('anggota').select()
    if(data) anggota.value=data
}
async function simpanKunjungan() {
    const { error } = await supabase.from('pengunjung').insert(from)
}

onMounted(() => getAnggota())
</script>