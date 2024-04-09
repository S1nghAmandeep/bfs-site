<script>


export default {

    data() {
        return {

        }
    }
}
</script>

<template>
    <footer class="footer" id="contacts">
        <div class="container">
            <div class="row space-items">
                <div class="col-3 footer-card">
                    <div class="row logo-items">
                        <img class="page-logo" src="/bfslogo.png" alt="">
                        <h1 class="campony-name">BFS</h1>
                    </div>
                    <p>While the lovely vally teems with vapour around me, and the meridian sun strikes the
                        upper surface of
                        the impenetrable foliage of my trees. While the lovely valley teems with vapour aroung me.</p>
                </div>
                <div class="col-3 ">
                    <h4 class="menu-title">Contacts</h4>
                    <ul class="footer-card">
                        <li>Via del Commercio 23, Castelgomberto (VI) 36070.</li>
                        <li><a href="#">babafatehsingh17@gmail.com</a></li>
                        <li>+39 3888328881 - 0445220135</li>
                    </ul>
                </div>
                <div class="col-3">
                    <h4 class="menu-title">Location on map</h4>
                    <!-- <img src="/map.png" alt=""> -->
                    <iframe
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1395.9131225441834!2d11.38084065037966!3d45.5940375794679!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x477f4a52391e3d47%3A0x5360709392d3d003!2sVia%20del%20Commercio%2C%2023%2C%2036070%20Zona%20Industriale%20Nord%20VI!5e0!3m2!1sit!2sit!4v1712654509570!5m2!1sit!2sit"
                        width="350" height="250" style="border:0;" allowfullscreen="" loading="lazy"
                        referrerpolicy="no-referrer-when-downgrade"></iframe>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/parstials/variables' as*;

.footer [class^='col-'] {
    padding: 15px;
}

.footer {
    padding: 100px 10px 100px;
    background-color: $bg-white;


    .col-3 {
        flex-basis: calc((100% / 12) * 12);
    }

    .footer-card {
        display: flex;
        flex-direction: column;
        gap: 20px;
        align-items: flex-start;
    }
}


// Medium devices (tablets, 768px and up)
@media (min-width: 768px) {

    .footer {
        .col-3 {
            flex-basis: calc((100% / 12) * 3);
        }
    }

}
</style>