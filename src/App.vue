<template>
    <div id="app">
        <!-- 默认按钮  -->
        <h3>按钮组件</h3>
        <lk-button>默认按钮</lk-button>
        <!-- 带类型的按钮 -->
        <lk-button type="primary">主要按钮</lk-button>
        <lk-button type="warning">警告按钮</lk-button>
        <lk-button type="danger">危险按钮</lk-button>
        <lk-button type="success">成功按钮</lk-button>
        <lk-button type="info">信息按钮</lk-button>
        <br />
        <br />
        <!-- 带icon的按钮 -->
        <lk-button type="primary" icon="sousuo" @click="onBtnClick($event)">带图标</lk-button>
        <!-- loading状态按钮 -->
        <lk-button type="danger" loading>加载中</lk-button>
        <br />
        <br />
        <!-- 按钮组 组件 -->
        <h3>按钮组</h3>
        <lk-button-group>
            <lk-button icon="houtuishangyige">上一页</lk-button>
            <lk-button type="primary" icon="houtuishangyige">上一页</lk-button>
            <lk-button type="primary" icon="qianjinxiayige" icon-position="right">下一页</lk-button>
            <lk-button icon="qianjinxiayige" icon-position="right">下一页</lk-button>
        </lk-button-group>
        <br />
        <br />
        <!-- icon组件 -->
        <h3>icon组件</h3>
        <lk-icon icon="houtuishangyige"></lk-icon>
        <lk-icon icon="qianjinxiayige"></lk-icon>
        <lk-icon icon="sousuo"></lk-icon>
        <lk-icon icon="dengdai-"></lk-icon>
        <br />
        <br />
        <!-- 布局组件 -->
        <h3>布局组件</h3>
        <!-- span和offset属性 -->
        <lk-row>
            <lk-col :span="4">
                <div class="grid-content bg-purple"></div>
            </lk-col>
            <lk-col :span="6" :offset="1">
                <div class="grid-content bg-purple-light"></div>
            </lk-col>
            <lk-col :span="6" :offset="3">
                <div class="grid-content bg-purple"></div>
            </lk-col>
        </lk-row>
        <br />
        <br />
        <!-- gutter实现col之间的缝隙 -->
        <lk-row :gutter="100">
            <lk-col :span="6">
                <div class="grid-content bg-purple"></div>
            </lk-col>
            <lk-col :span="6">
                <div class="grid-content bg-purple-light"></div>
            </lk-col>
            <lk-col :span="6">
                <div class="grid-content bg-purple"></div>
            </lk-col>
            <lk-col :span="6">
                <div class="grid-content bg-purple-light"></div>
            </lk-col>
        </lk-row>
        <br />
        <br />
        <!-- flex布局 -->
        <lk-row justify="center">
            <lk-col :span="6">
                <div class="grid-content bg-purple"></div>
            </lk-col>
            <lk-col :span="6">
                <div class="grid-content bg-purple-light"></div>
            </lk-col>
            <lk-col :span="6">
                <div class="grid-content bg-purple"></div>
            </lk-col>
        </lk-row>
        <br />
        <br />
        <!-- 响应式变化 -->
        <lk-row :gutter="10">
            <lk-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1">
                <div class="grid-content bg-purple"></div>
            </lk-col>
            <lk-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11">
                <div class="grid-content bg-purple-light"></div>
            </lk-col>
            <lk-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11">
                <div class="grid-content bg-purple"></div>
            </lk-col>
            <lk-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1">
                <div class="grid-content bg-purple-light"></div>
            </lk-col>
        </lk-row>
        <br />
        <br />
        <!-- 容器组件 -->
        <h3>容器组件</h3>
        <lk-container>
            <lk-header>Header</lk-header>
            <lk-main>Main</lk-main>
        </lk-container>
        <br />
        <lk-container>
            <lk-header>Header</lk-header>
            <lk-main>Main</lk-main>
            <lk-footer>Footer</lk-footer>
        </lk-container>
        <br />
        <lk-container>
            <lk-aside width="200px">Aside</lk-aside>
            <lk-main>Main</lk-main>
        </lk-container>
        <br />
        <lk-container>
            <lk-header>Header</lk-header>
            <lk-container>
                <lk-aside width="200px">Aside</lk-aside>
                <lk-main>Main</lk-main>
            </lk-container>
        </lk-container>
        <br />
        <lk-container>
            <lk-header>Header</lk-header>
            <lk-container>
                <lk-aside width="200px">Aside</lk-aside>
                <lk-container>
                    <lk-main>Main</lk-main>
                    <lk-footer>Footer</lk-footer>
                </lk-container>
            </lk-container>
        </lk-container>
        <br />
        <lk-container>
            <lk-aside width="200px">Aside</lk-aside>
            <lk-container>
                <lk-header>Header</lk-header>
                <lk-main>Main</lk-main>
            </lk-container>
        </lk-container>
        <br />
        <lk-container>
            <lk-aside width="200px">Aside</lk-aside>
            <lk-container>
                <lk-header>Header</lk-header>
                <lk-main>Main</lk-main>
                <lk-footer>Footer</lk-footer>
            </lk-container>
        </lk-container>
        <br><br>
        <!-- 输入框 -->
        <h3>输入框组件</h3>
        <lk-input  
            v-model="inputValue"
            :disabled="false"
            :clearable="true"
            type="text"
            placeholder="最多输入200字"
            name="username" />
        {{inputValue}}
        <br>
        <lk-input
            v-model="passwordValue"
            placeholder="请输入密码"
            show-password
            type="password" />
        <br>
        <lk-input
            v-model="inputValue"
            placeholder="请输入"
            prefix-icon="bianji" />
        <lk-input
            v-model="inputValue"
            placeholder="请输入"
            suffix-icon="bianji" />
        <br><br>
        <!-- 上传组件 -->
        <lk-progress :percentage="60"></lk-progress>
        <h3>上传组件</h3>
        <lk-upload
            name="upload"
            :file-list="fileList"
            action="http://localhost:3000/upload"
            :limit="4"
            accept="image/jpeg"
            :multiple="true"
            :on-exceed="handleExceed"
            :on-change="handleChange"
            :on-success="handleSuccess"
            :on-error="handleError"
            :on-progress="handleProgress"
            :before-upload="beforeUpload"
            :drag="true">
            <lk-button type="primary" icon="bianji">点击上传</lk-button>
            <div slot="tip">只能上传jpg/png格式的图片，且不超过500kb</div>
        </lk-upload>
        <br>
        <br>
    </div>
</template>

<script>
export default {
    data() {
        return {
            inputValue: '22222',
            passwordValue: 'password',
            fileList: [{
                name: '我是第一张图片',
                url: 'https://dss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=2309181523,3376829556&fm=26&gp=0.jpg'
            }, {
                name: '我是第二张图片',
                url: 'https://dss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=3498227956,2363956367&fm=26&gp=0.jpg'
            }]
        }
    },
    methods: {
        onBtnClick(e) {
            console.log(e);
        },
        handleExceed() {
            console.log('超过上限数量啦！')
        },
        handleChange(file) {
            // console.log(file)
        },
        handleSuccess(res, rawFile) {
            // console.log(res, rawFile)
        },
        handleError(err) {
            console.log(err)
        },
        handleProgress() {

        },
        beforeUpload(file) {
            let limitSize = file.size / 1024 > 5000;
            if(limitSize) {
                console.log('超过了最大限制');
                return false;
            }else if(!file.name.endsWith('.jpg')) {
                console.log('文件类型错误');
                return false;
            }
            return true;
        }
    }
};
</script>

<style>
.lk-col {
    border-radius: 4px;
}
.bg-purple-dark {
    background: #99a9bf;
}
.bg-purple {
    background: #d3dce6;
}
.bg-purple-light {
    background: #e5e9f2;
}
.grid-content {
    border-radius: 4px;
    min-height: 36px;
}

.lk-header,
.lk-footer {
    background-color: #b3c0d1;
    color: #333;
    text-align: center;
    line-height: 60px;
}

.lk-aside {
    background-color: #d3dce6;
    color: #333;
    text-align: center;
    line-height: 200px;
}

.lk-main {
    background-color: #e9eef3;
    color: #333;
    text-align: center;
    line-height: 160px;
}

body > .lk-container {
    margin-bottom: 40px;
}

.lk-container:nth-child(5) .lk-aside,
.lk-container:nth-child(6) .lk-aside {
    line-height: 260px;
}

.lk-container:nth-child(7) .lk-aside {
    line-height: 320px;
}
</style>