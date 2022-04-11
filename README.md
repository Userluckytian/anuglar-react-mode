# angular 添加响应式到项目中

### （1）修改angular.json中的build配置项,添加以下内容：
    // angular.json
    {
        ......
        "projects": {
            ......
            "architect": {
                "build": {
                ......
                "options": {
                    ......
                    "stylePreprocessorOptions": {
                        "includePaths": [
                            "src/core-styles",
                            "src/core-styles/react"
                        ]
                    }
                    ......
                },
            ......
        ......
    }
### （2）在自己的组件scss文件中直接使用

    // xxx.component.scss
    @import "mixins.scss";
    .box {
        border: solid 1px #ddd;
        width: calc(100vw - 40px);
        height: calc(100vh - 40px);
        background-color: #f2f2f2;
        @include respondTo(medium) {
            background-color: #666;
        }
    }


### （3）效果图

[![LV6QC6.md.gif](https://s1.ax1x.com/2022/04/11/LV6QC6.md.gif)](https://imgtu.com/i/LV6QC6)

   