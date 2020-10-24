<template>
    <header >
<HeaderCta />
<HeaderGraphics />
    </header>
  <HeaderStats id="stats"/>
</template>

<script>
import HeaderCta from './header-cta';
import HeaderStats from './header-stats';

import HeaderGraphics from './header-graphics';
    export default {
        name: 'Header',
        components: {
            HeaderGraphics, HeaderCta, HeaderStats
        },

        
    }
</script>

<style lang="scss" scoped>
header{
    display: flex;
    align-content: center;
    justify-content: space-between;
   
}

</style>