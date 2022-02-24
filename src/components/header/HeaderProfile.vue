<template>
    <div class="header-profile">
        <button class="search-btn">
            <font-awesome-icon class="search-ico" :icon="['fas', 'search']"/> 
        </button>
        <a class="kids" href="">Infantil</a>
        <button class="notification">
            <font-awesome-icon class="bell-ico" :icon="['fas', 'bell']"/> 
        </button>
        <div class="account-menu">
            <div class="account-dropdown">
                <a href="" role="button">
                    <span class="profile-link" role="presentation">
                        <img class="avatar" src="@/assets/avatar.png" alt="Avatar Profile">
                    </span>
                </a>
                <font-awesome-icon class="caret-ico" :icon="['fas', 'caret-down']"/>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from 'vue'

export default defineComponent({
    name: 'HeaderProfile',
    setup() {
        const data = reactive({

        })
        
        return { ...toRefs(data) }
    },
})
</script>

<style lang="scss">

.header-profile {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-end;
    flex-grow: 1;
    height: 100%;
    top: 0;
    
    button {
        margin-right: 25px;
        background: none;
        border: none;
        cursor: pointer;
    }
}

.search-ico {
    font-size: 1.2rem;
    color: #fff;
}

.kids {
    text-decoration: none;
    margin-right: 25px;
    font-size: 14px;
    color: #FFF
}

.bell-ico {
    font-size: 1.5rem;
    color: #fff;
}

.account-menu {
    display: block;
    
    position: relative;
    font-size: 12px;
    z-index: 0;
}

.account-dropdown {
    width: 100%;
    cursor: pointer;
    display: flex;
    align-items: center;
    a {
        position: relative;
        text-decoration: none;
        background-color: transparent;
        cursor: pointer;
    }

    a:hover ~ .caret-ico {
        transform: rotate(180deg);
    }
}

.account-dropdown:hover ~ .caret-ico{
    
}

.avatar {
    width: 32px;
    height: 32px;
    vertical-align: middle;
    border-radius: 4px;
}

.caret-ico {
    margin-left: 10px;
    font-size: 14px;
    transition: ease-in 0.2s;
}
</style>
