# package.json
package.json文件里面参数详解（主要是搬运<<深入浅出的node.js>> 过来的）


> 就参数的中文详解吧，入门的时候总有些参数没弄清楚

> *号里的是常用的字段

> 平时自己用就用到name、version、dependencies、devDenpendencies、main、scripts

> git:https://github.com/Maxxxz/package.json

```
{
    *name:"",
            //---包名---
            //可包含：小写的字母、数字、.、_、-，禁止出现空格
            //包名是唯一的(npm库里的包名)
    *description:"",
            //---该包的简介---
    *version:"",
            //---版本号---
            //格式 xx.xx.xx
    *keywords:"",
            //---关键词数组---
            //可被npm库中搜索到
    maintainters:"",
            //---包维护者列表---
            //示例:[{"name":xx,"email":"xx@gmail.com","web":"http://xx.com"},{...}]
    contributors:"",
            //---贡献者列表---
            //第一个是包作者本人，格式同上面包维护者相同
    bus:"",
            //---可反馈bug的url或者email
    lincenses:"",
            //---当前包所使用的许可证列表---
            //表示本包在哪些许可证下可以用
            //格式:[{"type":xx,"url":"http://xx.com"}]
    *repositories:"",
            //---源代码的托管位置---
    *dependencies:"",
            //---当前包所需的依赖包---
    homepage:"",
            //当前包的网站位置
    os:"",
            //---支持的操作系统列表---
            //一般为空（基本都支持）
    cpu:"", 
            //---支持的CPU架构列表---
            //一般为空（基本都支持）
            //有效的值：arm,mips,ppc,sparc,x86,x86_64.
    *engine:"",
            //---支持的javascript引擎列表---
            //一般为空（基本都支持）
            //有效的值：ejs,mips,flusspferd,gpsee,jsc,spidermonkey,narwhal,node,v8.
    builtin:"",
            //---标志当前包是否内建在底层系统的标准组件--- 
            //不懂 没用到
    directories:"",
            //---包目录说明---
    implements:"",
            //---实现规范的列表---
            //标志当前包实现了CommonJs的哪些规范
            //没用过。。
    *scripts："",
            //---脚本说明对象---
            //用来安装、编译、测试、卸载包
            //可是一段命令或者js文件
            /*
            "scripts": {
                "precommit": "eslint --cache --fix ./js/ ./common",
                "build_clear": "rimraf -rf build&& mkdir build",
                "start": "cross-env NODE_ENV=development node --max-old-space-size=8192,
                "test":"test.js"
            }
            */
    *author："",
            //---包作者---
    *bin:"",
            //---包可作为命令行工具使用---
            //配置好bin字段后，通过npm install <package_name> -g 将脚本添加到执行路径中，之后可以在命令行中直接执行。
            //类似全局安装了webpack~
    *main:"",
            //---入口文件---
            //如果不存在这个字段，会自动按下面顺序查找:index.js,index.node,index.json
    *devDenpendencies:""
            //---只在开发时需要的依赖包---
}            
```
