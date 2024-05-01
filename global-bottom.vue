<style>
#pageno {
    position: absolute;
    bottom: 4px;
    right: 8px;
}
</style>
<template>
    <div
        id="pageno"
        v-if="
            $slidev.nav.currentLayout !== 'cover' &&
            $slidev.nav.currentPage !== 2
        "
    >
        <SlideCurrentNo />
    </div>
</template>
