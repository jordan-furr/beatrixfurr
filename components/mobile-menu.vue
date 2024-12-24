<template>
    <div class="menu-overlay" v-if="isVisible" @click="toggleMenu">
        <p class="logo">Beatrix Furr</p>
        <nav @click.stop>
            <ul>
                <li>
                    <nuxt-link to="/education" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>Education</p>
                    </nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/work" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>Work</p>
                    </nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/originals" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>Originals</p>
                    </nuxt-link>
                </li>
                <li>

                    <nuxt-link to="/bread" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>Bread Theory</p>
                    </nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/order-online" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>Order Online</p>
                    </nuxt-link>
                </li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
    props: {
        isVisible: {
            type: Boolean,
            required: true
        }
    },
    methods: {
        toggleMenu() {
            this.$emit('toggle-menu');
        },
        closeMenu() {
            this.$emit('toggle-menu');
        }
    }
}
</script>