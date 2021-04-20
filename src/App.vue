<template>
    <table width="100%" border="0" cellspacing="0" cellpadding="0">
        <tr>
            <td bgcolor="#EBEBEB" style="font-size: 0px">&zwnj;</td>
            <td id="center" bgcolor="#cacaca" align="center" width="600">
                <Header />
                <TitleBlock />
                <ContentBlock />
                <ThanksNotes />
                <Footer />
            </td>
            <td bgcolor="#EBEBEB" style="font-size: 0px">&zwnj;</td>
        </tr>
    </table>
</template>

<script>
import Header from "./components/Header.vue";
import TitleBlock from "./components/TitleBlock.vue";
import ContentBlock from "./components/ContentBlock.vue";
import ThanksNotes from "./components/ThanksNotes.vue";
import Footer from "./components/Footer.vue";

export default {
    name: "App",
    components: {
        Header,
        TitleBlock,
        ContentBlock,
        ThanksNotes,
        Footer,
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}

button {
    cursor: pointer;
}

@media only screen and (max-width: 600px) {
    #center {
        width: 100%;
    }
}
</style>
