# Unit Morph的要点

## Unit

被孵化出来的单位

- 必须勾选“Morph from other unit”
- 不能勾选“Spellcaster”

## 菜单

该单位的菜单不能存在冲突。所谓冲突就是两个按纽在同一个位置，并且同时出现。

## Dat Requirements

需要修改被孵化出来的单位的Dat Requirements，能让孵化前的单位孵化出它来

- 一种方法是删光所有条件（*注）
- 另一种是在最开头加上“Current unit is ... Or”

## Exe Edits

需要勾选Exe Edits（最重要的！）

- Units - Create Unit - Unit Morph
  - Order Restriction - Check Unit Type 改为 Enabled
  - Order - All non-morph units to use cocoons 改为 Enabled

​        

*注1：删光所有条件的缺点是可能造成未知后果。
比如删光SCV的所有条件之后，如果指挥中心被打爆了的话，电脑会从任何建筑物中造SCV，比如补给站，比如飞机场。
*注2：DatEdit - Unit - AI Actions - Computer Idle 设置为 Stay in Range 会导致运行一段时间后（触发Computer Idle时）突然崩溃