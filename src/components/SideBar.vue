<template>
    <div class="sidebar-container">
        <ul class="sidebar-menu">
            <li>
                <svg-icon type="mdi" :path="mdiFolder"></svg-icon>
            </li>
            <li>
                <svg-icon type="mdi" :path="mdiCableData "></svg-icon>
            </li>
            <li>
                <svg-icon type="mdi" :path="mdiDatabaseArrowUpOutline "></svg-icon>
            </li>
            <li>
                <svg-icon type="mdi" :path="mdiImage"></svg-icon>
            </li>
        </ul>
    </div>
</template>

<script setup>
import SvgIcon from '@jamescoyle/vue-icon';
import {
    mdiFolder,
    mdiCableData ,
    mdiDatabaseArrowUpOutline ,
    mdiImage
} from '@mdi/js';

</script>

<style scoped>
.sidebar-container {
    border-right: dashed 1px var(--color-border);
    height: 100%;
    padding-top: 20px;
}

.sidebar-menu {
    list-style-type: none;
    padding-left: 0;
}

.sidebar-menu>li {
    margin-bottom: 10px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
}

.sidebar-menu>li:hover {
    scale: 0.9;
}
</style>