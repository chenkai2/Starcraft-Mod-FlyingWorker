# SCV对空的修改要点

SCV、工蜂、探机等原本无法对空的单位改为可对空：

## DatEdit

Unit - Basic - Weapons:

- Choose Air Attack Type  (某些类型的攻击会导致崩溃，崩溃的原因是缺少必要的动画) 
  - 一种处理方式是选用和地面攻击相同类型的伤害，然后进入该伤害的修改处，Target Flags勾选Air
  - 另一种处理方式是选择已有的对空攻击类型，比如ATA Laser Battery
- Max Hits: 1

## Ice_XP

以SCV为例，其他单位类似。

1. 打开Icp_XP，File - Auto Load from Local SC MPQ，从本地SC的MPQ中加载默认脚本

2. 从Header of Unit/etc: 找到SCV：

   Terran SCV

3. 切换到Entry Header标签页

   - Initial Air Attack：从地面攻击处复制过来
   - Return to basic pose from Air Attack：从地面攻击恢复动作处复制过来
   - Repeated Air Attack：从地面重复Air Attack处复制过来

4. 特殊例子：

   Infested Karrigan的动画会导致武器无溅射伤害，即使设置成攻城坦克的武器；

   解决方案是修改她的动画，改为和Karrigan（或者Protoss Dark Templar）一样的动画

# 打包方法

使用Mpq WorkShop在DatEdit导出的mpq中建立scripts目录，把Ice_XP保存的iscript.bin拉进去，放到scripts目录中