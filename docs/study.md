
### 如何添加一个新的道具
1. 将预制体使用的美术资源放到texture/matchItems目录下.将道具的图标放到resources/texture/resource 目录下备用。将碎裂效果图片放到texture/Parts目录下备用。
2. 找到道具销毁音效放到audio目录下。添加Public文件的《音效》sheet中备用
3. 制作道具的碎裂效果，将信息添加到Public表中的《效果》sheet中。将预制体放到bundles/game/prefab/particle 目录下备用
4. 在游戏对象表的《CellItemModel》sheet中添加一行，填写对应列的数据。添加GameObjectType中的游戏类型，如果没有此类型自己添加新类型，并实现对应的功能，还要在《类型操作交换表》sheet中添加对应的操作。
5. 在《CellObjectModel》表中加一行。
6. 在《CellStepIModel》加一行或者多行，要看道具有多少个阶段。
7. 在bundles/game/prefab/cell_objs 目录下创建一个预制体（也可以复制一个已经存在的预制体）修改名字，将预制体名称放到CellObjectModel表中（注意预制体的结构，将对应会消除的图片放到animation节点下）
8. 利用关卡编辑关卡。制作关卡，将关卡数据起名为map_dataXX.json 放到resources/map目录下
9.  找到DBBattle类，修改测试关卡 //   this.level.setValue(51)
10. 运行测试。
