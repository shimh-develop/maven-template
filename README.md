# maven-template
多模块maven项目模板

## maven 官方文档
https://maven.apache.org/users/index.html


## maven 生命周期阶段与插件目标绑定


### Clean 生命周期 内置绑定
| Phase    | plugin:goal    | Description    |
|---------|---------|---------|
| clean   | clean:clean   | 内容3   |

### Default生命周期 内置绑定
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



## 依赖处理

### 排除依赖
* 排除依赖应该在直接引入该依赖的地方进行，也就是在子模块的dependencies中排除。如果在父POM的dependencyManagement里排除，可能会影响到所有子模块，导致不必要的排除，特别是当某些子模块确实需要那个传递性依赖的时候。

### 日志

* 