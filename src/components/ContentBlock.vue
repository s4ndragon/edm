<template>
    <table
        v-for="product in products"
        :key="product.id"
        width="600"
        border="0"
        cellspacing="0"
        cellpadding="0"
        style="padding: 15px 15px 0"
    >
        <!-- title -->
        <tr bgcolor="#ffffff">
            <td style="padding: 15px 15px 0; color: #4285f4; font-weight: 900; font-size: 18px">
                {{ product.title }}
            </td>
        </tr>
        <!-- sub title -->
        <tr bgcolor="#ffffff">
            <td style="padding: 15px 15px 0;">
                <table v-for="subBlock in product.subBlocks" :key="subBlock.id">
                    <tr>
                        <td style="font-weight: 900">{{ subBlock.subtitle }}</td>
                    </tr>
                    <tr>
                        <td style="font-size: 16px">{{ subBlock.content }}</td>
                    </tr>
                    <!-- button -->
                    <tr bgcolor="#ffffff" align="center">
                        <td style="padding: 15px">
                            <button
                                style="
                            width: 140px;
                            height: 40px;
                            background-color: #4285f4;
                            color: #ffffff;
                            border-radius: 5px;
                            border: 0;
                            font-weight: 900;
                        "
                            >
                                LEARN MORE
                            </button>
                        </td>
                    </tr>
                </table>
            </td>
        </tr>
    </table>
</template>

<script>
export default {
    name: "ProductBlock",
    data() {
        return {
            products: [
                {
                    title: "PRODUCT & FEATURE HIGHLIGHTS",
                    subBlocks: [
                        {
                            subtitle: "Introducing Data Studio Community Visualizations Developer Preview",
                            content:
                                "The new Data Studio Community Visualizations feature, in developer preview, allows you to build new charts and customize styling options, providing even more freedom and flexibility in the stories you tell with your data.",
                        },
                        {
                            subtitle: "Duplicate your filters and blended data sources",
                            content:
                                "You can now duplicate filters and blended data sources within the same report. To do this, edit your report, then choose the “Resource” menu and select the resource you want to manage. Use the “Duplicate” action to make the copy. You can then apply the copied filter or blended data source to other charts in the report.",
                        },
                    ],
                },
                {
                    title: "TIPS & BEST PRACTICES",
                    subBlocks: [
                        {
                            subtitle: "2018: The Year in Data Studio Community Connectors",
                            content:
                                "It's been a busy year for Data Studio Community Connectors. Since the developer launch, we've added over ten new features, had significant growth, seen partners grow their businesses, and collaborated with the community on open source projects.",
                        },
                        {
                            subtitle: "At airBaltic, evidence-based marketing takes flight with Google Data Studio",
                            content:
                                "Air travel might be getting easier, but for the companies that carry us from where we are to where we are going, there is an amazing amount of complexity at work — and they need insights to make critical decisions.",
                        },
                    ],
                },
                {
                    title: "NEW TITLE",
                    subBlocks: [
                        {
                            subtitle: "Lorem Ipsum",
                            content:
                                "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
                        },
                        {
                            subtitle: "Lorem Ipsum",
                            content:
                                "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
                        },
                    ],
                },
            ],
        };
    },
};
</script>
