<template>
    <div class="header">
        <div class="flex-row space-between align-center">
            <!--<p>&#127281;&#127284;&#127280;&#127299;&#127297;&#127288;&#127303;</p>-->
            <nuxt-link to="/" class="logo">
                <p>Beatrix Furr</p>
            </nuxt-link>
            <div class="mobile-menu">
                <menu-icon :isOpen="isMenuVisible" @toggle-menu="toggleMenu" />
                <mobile-menu :isVisible="isMenuVisible" @toggle-menu="toggleMenu" />
            </div>
            <div class="flex-row menu-nav">
                <div class="nav-item">
                    <nuxt-link to="/education" class="menu-item" exact-active-class="active">
                        <p>Education</p>
                    </nuxt-link>
                </div>
                <div class="nav-item dropdown">
                    <nuxt-link to="/work" class="menu-item" exact-active-class="active">
                        <div class="">
                            <p class="mb1">Work</p>
                            <div class="dropdown-content">
                                <nuxt-link to="/work">
                                    <p>HolyBelly</p>
                                </nuxt-link>
                                <nuxt-link to="/work">
                                    <p>P1 Bakery</p>
                                </nuxt-link>
                                <nuxt-link to="/work">
                                    <p>Ferrandi</p>
                                </nuxt-link>
                            </div>
                        </div>
                    </nuxt-link>
                </div>
                <div class="nav-item">
                    <nuxt-link to="/originals" class="menu-item" exact-active-class="active">
                        <div class="dropdown">
                            <p class="mb1">Originals</p>
                            <div class="dropdown-content">
                                <nuxt-link to="/originals">
                                    <p>Picasso Cookie</p>
                                </nuxt-link>
                            </div>
                        </div>
                    </nuxt-link>
                </div>
                <div class="nav-item">
                    <nuxt-link to="/bread" class="menu-item" exact-active-class="active">
                        <p>Bread Theory</p>
                    </nuxt-link>
                </div>
                <div class="nav-item">
                    <nuxt-link to="/order-online" class="menu-item" exact-active-class="active">
                        <p>Order Online</p>
                    </nuxt-link>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import mobileMenu from './mobile-menu.vue';
import menuIcon from './menu-icon.vue';
export default {
    components: { mobileMenu, menuIcon },
    data() {
        return {
            isMenuVisible: false
        }
    },
    methods: {
        toggleMenu() {
            this.isMenuVisible = !this.isMenuVisible;
        }
    }
}
</script>