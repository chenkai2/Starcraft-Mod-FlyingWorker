# Starcraft Mod Flying worker

## Mod特色

1. ### Terran：

   1. SCV隐身，建造时间0.2s，攻击升级为16，射程16
   2. SCV可以切换到飞行模式
      - 飞行单位
      - 隐身，反隐，使用坦克炮击，带溅射，伤害35，射程16，可对空
      - 可以采矿，修理机械单位、建筑物
      - 技能：心灵控制
      - 可以切换回普通SCV模式

2. ### Zerg：

   1. 工蜂（Drone）隐身，孵化时间0.2s，攻击16，射程16
   2. 幼虫（Larva）生成时间减少到1s
   3. 跳虫（Zergling）可以变身为凯莉甘（Karrigan）
   4. 凯莉甘（Karrigan）：
      - 飞行单位
      - 隐身，反隐，单体伤害50，射程16，可对空
      - 技能：灵能风暴、心灵控制

3. ### Protoss：

   1. 探机（Probe）隐身，建造时间0.2s，攻击16，射程16
   2. 灵能风暴、心灵控制、幻象不消耗能量
   3. 狂热者（Zealot）可以变身为泽拉图（Zeratual）
   4. 泽拉图（Zeratual）：
      - 飞行单位
      - 隐身，反隐，使用幽能曲光刃，单体伤害100，射程16，可对空
      - 技能：灵能风暴、心灵控制

4. ### 所有种族：

   1. 地面、空军攻防升级时间均为17s，费用降为10矿10气，最高32级
   2. 灵能风暴、心灵控制不耗费灵能


## 使用方法

适用版本：Starcraft v 15.1

运行worker-remix.exe即可

## 编辑方法

1. ### *.dat

   使用DatEdit可以编辑所有dat文件

   这些文件主要控制单位属性、武器属性、升级属性、技能属性、命令属性，修改完成后导出到worker.mpq

2. ### iscript.bin

   使用Ice_XP编辑，用于添加相关单位的对空动画，编辑完成后使用MPQWorkshop把iscript.bin添加到worker.mpq/scripts/iscript.bin

3. ### worker-remix.exe

   使用Firegraft v0.93打开worker-remix.exe，主要用于编辑菜单、设置限制（Requirements）、使用Exe Edit。

# 发布方法

1. 编辑工具可以从[tools](https://github.com/chenkai2/Starcraft-Mod-Tookit)里找到
2. 使用DatEdit导出worker.mpq
3. 使用Ice_XP修改iscript.bin
4. 使用MPQWorkshop把iscript.bin添加到worker.mpq中
5. 使用Firgraft v0.93打开worker-remix.exe进行修改后，保存时导入worker.mpq，然后保存到worker-remix.exe

## 修改技术要点

1. ### 工具

   [星际争霸Mod工具包](https://github.com/chenkai2/Starcraft-Mod-Tookit)

2. ### 对空的修改

   参考[AirAttack.md](AirAttack.md)

3. ### UnitMorph的要点

   参考[UnitMorph.md](UnitMorph.md)

4. ### SCV起飞的实现

   参考[SCVTransform.md](SCVTransform.md)





