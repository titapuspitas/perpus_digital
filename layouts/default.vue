<template> 
    <div class="container-fluid">
        <div class="row bg-success text-light">
                <div class="col-lg-2">
                    <img 
                    src="~/assets/img/logo.sekolah.png"
                    alt=""
                    width="150"
                    height="150"
                    class="d-inline-block align-text-top left = 20"
                    />
                </div>
                <div class="col-lg">
                    <h1>Catatan pengunjung perpustakaan</h1>
                    <p>Smkn 4 kota Tasikmalaya</p>
                    <p>Jl.Depok, Sukamenak, Kec.Purbaratu, Kab.Tasikmalaya, Jawa Barat</p>
                </div>
                <div class="col">
                    <img 
                    src="~/assets/img/logo.grup.png"
                    alt=""
                    width="150"
                    height="150"
                    class="d-inline-block align-text-top right= 20"
                    />
                </div>
            </div>
            
            <slot/>
        </div>
    </template>      