<template>
    <div id="app">
        <Bar></Bar>
        <div class="container-fluid">
            <div class="row">
                <SideBar class="col-3"></SideBar>
                <router-view class="col-9"></router-view>
            </div>
        </div>
        <div style="height: 33px;"></div>

        <Top></Top>
        <ListDialogue></ListDialogue>
    </div>
</template>

<script>
import Bar from './components/Bar.vue'
import SideBar from './components/SideBar.vue'
import ListDialogue from './components/ListDialogue.vue'
import Top from './components/Top.vue'

export default {
    name: 'App',
    components: {
        Bar,
        SideBar,
        ListDialogue,
        Top,
    },
    created() {
        window.addEventListener('beforeunload', (e) => {
            e.preventDefault()
            e.returnValue = ''
        })
    },
}
</script>

<style>
.inline {
    display: inline-block;
}

.wa {
    width: auto;
}

.table caption {
    caption-side: top;
}

.mb11px {
    margin-bottom: 11px;
}

.mr11px {
    margin-right: 11px;
}

.mt11px {
    margin-top: 11px;
}

.mtb11px {
    margin-top: 11px;
    margin-bottom: 11px;
}

.button-label {
    padding: 0;
    margin: 0;
}
</style>
