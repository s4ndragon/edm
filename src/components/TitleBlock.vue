<template>
    <table width="600" border="0" cellspacing="0" cellpadding="0" style="padding: 15px 15px 0">
        <tr bgcolor="#ffffff">
            <td style="text-align: center; font-size: 24px; padding: 30px 0" colspan="2">
                {{ month }} {{ year }} - Product Update
            </td>
        </tr>
        <tr>
            <td>
                <img style="width: 100%" src="../assets/background.png" />
            </td>
        </tr>
    </table>
</template>
<script>
export default {
    name: "TitleBlock",
    data() {
        return {
            month: "",
            year: "",
        };
    },
    created() {
        setInterval(this.getNow, 1000);
    },
    methods: {
        getNow: function() {
            const today = new Date();
            const monthNames = [
                "January",
                "February",
                "March",
                "April",
                "May",
                "June",
                "July",
                "August",
                "September",
                "October",
                "November",
                "December",
            ];
            this.month = monthNames[today.getMonth()];
            this.year = today.getFullYear();
            // const date = today.getFullYear() + "-" + (today.getMonth() + 1) + "-" + today.getDate();
            // const time = today.getHours() + ":" + today.getMinutes() + ":" + today.getSeconds();
            // const dateTime = date + " " + time;
            // this.timestamp = dateTime;
        },
    },
};
</script>
