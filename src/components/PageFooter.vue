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
                        <li>Patricia C.Amedee 4401 Waldeck Street Grapevine Nashville, TX 76051</li>
                        <li><a href="#">info@yourdomain.com</a></li>
                        <li>+99 (0) 101 0000 888</li>
                    </ul>
                </div>
                <div class="col-3">
                    <h4 class="menu-title">Location on map</h4>
                    <img src="/map.png" alt="">
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