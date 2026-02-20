# PyPizza
## Chinese
**PyPizza是一个Python项目管理器**<br>
**使用非常简单的PyPizza的项目格式**<br>
### 使用
#### 安装
**要求: ```Python>=3.8```**<br>

**依赖: ```PyInstaller>=6.0```**<br>

**运行: ```pip install pypizza```**

> **通常python和pip会处理好这些依赖**

---

#### 运行
> _**运行Pizza项目十分简单**_

```pizza run``` - **直接运行项目**

```pizza run 文件``` - **以main为入口点运行Python脚本** _(没用?)_

```pizza run 文件:入口函数``` - **指定入口点运行Python脚本**

---

#### 编译
>_**依旧很简单**_

```pizza build``` - **编译项目**

```pizza build <文件>``` - **以main为入口点编译Python脚本**

```pizza run <文件:入口函数>``` - **指定入口点编译Python脚本**

---

#### 参数
> 如果你使用Pizza项目, 请到pizza.json中配置

```-i <图标>``` - **设置编译的可执行程序图标 (pizza.json的build的icon项)**

```-g``` - **设置编译的可执行程序没有控制台 (pizza.json的build的console项)**

```-s``` - **设置编译/运行前安装依赖时跳过错误 (pizza.json的build的skip项)**

---

#### 其它

```pizza clean``` - **清理临时文件**

```pizza new <名称>``` - **新建项目**

```pizza info``` - **显示项目信息**

---

### 示例

**hello**<br>
&nbsp;├─&nbsp;**pizza.json**<br>
&nbsp;└─&nbsp;**src/**<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ **main.py**<br>


```json
// pizza.json
{
    "name": "我的项目", //项目名称
    "version": "1.0", //版本号
    "desc": "一个打印HelloWorld的项目", //描述
    "author": "作者的名字", //作者
    "main": "src/main.py:main", //入口点(文件路径:入口函数)
    "deps": [], //依赖(pip)
    "build": { //编译参数
        "icon": null, //图标(null使用默认)
        "console": true, //是否有控制台
        "skip": false //依赖安装失败是否跳过错误
    }
}
```
```python
# src/main.py
def main():
    print("Hello,World!")
```
```shell
$ pizza run
Hello,World!
$ pizza build
╭─ 项目结构 ────────────╮
│ demo/                 │
│ ├─ pizza.json [253 B] │
│ └─ src/               │
│     └─ main.py [38 B] │
╰───────────────────────╯

╭─ Pizza ─────────────────────╮
│ 编译成功 -> output/main.exe │
╰─────────────────────────────╯
```
## English
**PyPizza is a Python project manager**<br>
**Uses a very simple PyPizza project format**<br>
### Usage
#### Installation
**Requirements: ```Python>=3.8```**<br>

**Dependencies: ```PyInstaller>=6.0```**<br>

**Run: ```pip install pypizza```**

> **Usually python and pip will handle these dependencies**

---

#### Running
> _Running a Pizza project is very simple_

```pizza run``` - **Run the project directly**

```pizza run <file>``` - **Run a Python script with main as the entry point** _(not useful?)_

```pizza run <file:entry function>``` - **Run a Python script with a specified entry point**

---

#### Building
>_Still very simple_

```pizza build``` - **Build the project**

```pizza build <file>``` - **Build a Python script with main as the entry point**

```pizza build <file:entry function>``` - **Build a Python script with a specified entry point**

---

#### Parameters
> If you're using a Pizza project, configure these in pizza.json

```-i <icon>``` - **Set the icon for the compiled executable (pizza.json build icon item)**

```-g``` - **Compile the executable without a console (pizza.json build console item)**

```-s``` - **Skip errors when installing dependencies before building/running (pizza.json build skip item)**

---

#### Others

```pizza clean``` - **Clean temporary files**

```pizza new <name>``` - **Create a new project**

```pizza info``` - **Display project information**

---

### Example

**hello**<br>
&nbsp;├─&nbsp;**pizza.json**<br>
&nbsp;└─&nbsp;**src/**<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ **main.py**<br>


```json
// pizza.json
{
    "name": "My Project",
    "version": "1.0",
    "desc": "A project that prints HelloWorld",
    "author": "Author's Name",
    "main": "src/main.py:main",
    "deps": [],
    "build": {
        "icon": null,
        "console": true,
        "skip": false
    }
}
```
```python
# src/main.py
def main():
    print("Hello,World!")
```
```shell
$ pizza run
Hello,World!
$ pizza build
╭─ 项目结构 ────────────╮
│ demo/                 │
│ ├─ pizza.json [253 B] │
│ └─ src/               │
│     └─ main.py [38 B] │
╰───────────────────────╯

╭─ Pizza ─────────────────────╮
│ 编译成功 -> output/main.exe │
╰─────────────────────────────╯
```
