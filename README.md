# maven-template
多模块maven项目模板



## 归类

### 文档
#### maven 官方文档
https://maven.apache.org/users/index.html


### 插件
#### Maven可用插件列表
https://maven.apache.org/plugins/index.html
#### 插件版本依赖jdk和Maven版本查看
如 maven-assembly-plugin的版本要求
https://maven.apache.org/plugins/maven-assembly-plugin/plugin-info.html

#### maven 生命周期阶段与插件目标绑定
Clean 生命周期 内置绑定

| Phase    | plugin:goal    | Description    |
|---------|---------|---------|
| clean   | clean:clean   | 内容3   |

Default生命周期 内置绑定

| Phase    | plugin:goal    | Description    |
|---------|---------|---------|
| process-resources   | resources:resources   | 内容3   |
| compile   | compiler:compile   | 内容6   |
| process-test-resources   | resources:testResources   | 内容9   |
| test-compile   | compiler:testCompile   | 内容9   |
| test   | surefire:test   | 内容9   |
| package   | ejb:ejb or ejb3:ejb3 or jar:jar or par:par or rar:rar or war:war   | 内容9   |
| install   | install:install   | 内容9   |
| deploy   | deploy:deploy   | 内容9   |

#### 常用插件
##### maven-assembly-plugin
https://maven.apache.org/plugins/maven-assembly-plugin/index.html
* 将代码、依赖、配置文件等组合成最终交付包（如 ZIP、TAR）

##### maven-shade-plugin
https://maven.apache.org/plugins/maven-shade-plugin/
* 生成可直接运行的 Fat JAR
* 解决依赖冲突，即重命名某些依赖的包


#### maven-dependency-plugin
https://maven.apache.org/plugins/maven-dependency-plugin/
* 分析依赖、列出依赖树
* 复制单个依赖或项目所有依赖jar、解压jar


### 依赖

#### 排除依赖
* 可以借助IDEA的Diagrams/showDependencies查看依赖图，也可以用maven-dependency-plugin插件查看：dependency:analyze 分析代码使用未声明的依赖、dependency:tree列出依赖树
* 排除依赖应该在直接引入该依赖的地方进行，也就是在子模块的dependencies中排除。如果在父POM的dependencyManagement里排除，可能会影响到所有子模块，导致不必要的排除，特别是当某些子模块确实需要那个传递性依赖的时候。

### 日志

* 

