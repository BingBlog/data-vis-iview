<template>
    <i-article>
        <article>
            <h1>卡片</h1>
            <inAnchor title="概述" h2 />
            <p>折线图是用折线将各个数据点标志连接起来的图表，用于展现数据的变化趋势。</p>
            <inAnchor title="类型三：基于iView Card 组件的数据概览卡片" h3 />
            <div class="api">
                <table>
                    <thead>
                        <tr>
                            <th>属性</th>
                            <th>说明</th>
                            <th>类型</th>
                            <th>默认值</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>charts</td>
                            <td>图的配置集合</td>
                            <td>Array</td>
                            <td>不可为空</td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <Demo title="核心数据展示" vertical>
                <div slot="demo">
                    <DataVisGroup
                        display="inline"
                        :charts="code.simple.data.charts"
                    />
                </div>
                <div slot="desc">
                    <p>通过设置<code>charts</code>即可生成一个一系列可视化图表。</p>
                </div>
                <i-code slot="code" lang="html">{{ code.simple.code }}</i-code>
            </Demo>
        </article>
    </i-article>
</template>

<script>
import iArticle from 'website/components/article';
import inAnchor from 'website/components/anchor';
import iCode from 'website/components/code';
import Demo from 'website/components/Demo';
import Code from 'website/code/config-guide/card/index';

export default {
    components: {
        iArticle,
        inAnchor,
        iCode,
        Demo
    },
    data() {
        return {
            code: Code
        };
    },
    methods: {
        handleFieldChange(model, value) {
            // eslint-disable-next-line no-console
            console.log(model, value);
        }
    }
};
</script>
