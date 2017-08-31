### vscode下的c++开发调试配置demo

1. 安装c++插件
2. 终端里`touch main.cpp`创建`main.cpp`，然后写点测试代码
3. vscode里`ctr+shift+p`调出面板，搜索`task`，生成`tasks.json`，配置`command`、`args`、`group`
4. vscode里生成`other`的`launch.json`，将`program`属性改为需要运行的可执行文件`${workspaceRoot}/main.out`
5. 参考[官方文档](https://code.visualstudio.com/docs/languages/cpp)，把鼠标移到cpp文件代码的`#include`之前提示处，点击下拉菜单的`Update "browse.path"`，生成`c_cpp_properties.json`，后续需要包含库路径的话也是往这里面添加，如果不知道路径在哪的话，可以根据提示缺少了什么库，然后在系统里搜索一下，例如`sudo find / -name stddef.h`
6. `ctrl+shift+b`编译，并且在后续的每次编辑之后、调试之前都要编译一下
7. `f5`调试
