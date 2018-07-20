# SCV起飞的实现

## 实现原理

活用Unit Morph，点击起飞按钮后孵化为起飞形态的SCVInAir

## 具体实现

变形后的SCV其实是另一个未在游戏中出现过的单位[91] Cargo Ship (Unused)。

1. ### DatEdit

   - #### [91] Cargo Ship (Unused)

      - ##### Units - Basic

         - 把[7] Terran SCV所有属性复制过来
      - ##### Units - Advanced

         - 勾选“Flyer”
         - 勾选“Morph from other unit”
   - #### [7] Terran SCV

      - 勾选“Morph from other unit”
2. ### Firegraft

   - #### Button Sets

     - 复制SCV的按钮集
     - Paste Entry As New
     - 新增的菜单重命名为SCVInAir
     - 移除SCVInAir中的建造基本建筑、建造高级建筑按钮（因为即使有也无法建造）
     - 在SCVInAir中新增按钮，Action选择Unit Morph，Action Variable选 7 SCV
     - 在SCV中新增按钮，Action选择Unit Morph，Action Variable选 91 Unused Was Cargo Ship

   - #### Units

     - ##### [91] Unused Was Cargo Ship

       - Unit Information - Button Set 改为SCVInAir
       - Status Information - Status Presets 改为 Normal Unit
       - Status Information - Debug ID 改为91

   - #### Dat Requirements

     - ##### [7] SCV - Requirements

       - 在顶部添加Opcode “Current Unit is”
       - 添加第二行Parameter “Unused - Was Cargo Ship”
       - 添加第三行Opcode - “Or”

     - ##### [91] Unused - Was Cargo Ship

       - 勾选Used

   - #### Exe Edits

     - ##### Units - Create Unit - Unit Morph

       - Order Restriction - Check Unit Type 改为 Enabled
       - Order - All non-morph units to use cocoons 改为 Enabled

## 缺点

孵化需要消耗生产SCV、SCVInAir的资源和时间