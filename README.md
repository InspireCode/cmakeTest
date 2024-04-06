# 使用CMake构建具有菱形依赖关系的项目

### 1. 文件(项目)依赖关系如下：
```
A<---B<---D
 ↑---C<---┘
```
最终构建的项目以A.cpp中的main函数为入口

### 2. 一些问题
B依赖D，但是D不是B的子目录，因此B目录下的CMakeLists.txt中如此添加D依赖：`add_subdirectory(../D buildD1)`，必须指定第二个参数`build_dir="buildD1"`，否则cmake报错 `add_subdirectory not given a binary directory but the given sourcedirectory is not a subdirectory of...`

### 3. 最后
cmake项目报错：
`
CMake Error at D/CMakeLists.txt:1 (add_library):add_library cannot create target "D" because another target with the same name already exists.  The existing target is a static library created in source directory D.  See documentation for policy CMP0002 for more details.`
