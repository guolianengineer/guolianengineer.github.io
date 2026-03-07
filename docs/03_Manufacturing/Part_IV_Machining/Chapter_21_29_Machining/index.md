
# CNC Machining
**数控加工**

Computer Numerical Control (CNC) machining is a subtractive manufacturing process that typically uses computerized controls and machine tools to remove layers of material from a stock piece—known as the blank or workpiece—and produces a custom-designed part.
> 数控加工（CNC）是一种减材制造工艺，通常使用计算机控制和机床从毛坯（工件）上去除材料层，从而生产出定制设计的零件。

## Cases (案例)
*   **[Eliminating Chatter on Aluminum Enclosure (消除铝合金外壳的铣削颤纹)](./Cases/case_chatter.md)**

---

## 1. Working Principle (工作原理)

The process starts with a 3D CAD model, which is converted into a series of computer instructions (G-code) that control the machine's movement.
> 该过程从 3D CAD 模型开始，将其转换为一系列控制机床运动的计算机指令（G 代码）。

### Key Components (关键组件)
*   **Spindle (主轴)**: Holds and rotates the cutting tool.
    *   夹持并旋转刀具。
*   **Table (工作台)**: Holds the workpiece.
    *   固定工件。
*   **Axis (轴)**: Directions of movement (X, Y, Z, A, B, C).
    *   运动方向（X, Y, Z, A, B, C）。

---

## 2. Equipment Types (设备类型)

### 3-Axis CNC (三轴 CNC)
*   **Description**: Moves in X, Y, and Z axes. Best for simple parts.
    *   描述：在 X、Y、Z 轴方向移动。最适合简单零件。
*   **Pros**: Lower cost, simple programming.
    *   优点：成本低，编程简单。
*   **Cons**: Multiple setups required for complex geometries.
    *   缺点：复杂几何形状需要多次装夹。

### 5-Axis CNC (五轴 CNC)
*   **Description**: Adds two rotary axes (A and B/C). Allows machining of complex shapes in a single setup.
    *   描述：增加了两个旋转轴（A 和 B/C）。允许在一次装夹中加工复杂形状。
*   **Application**: Aerospace, medical implants, complex consumer electronics housings.
    *   应用：航空航天、医疗植入物、复杂的消费电子外壳。

### Turn-Mill Center (车铣复合)
*   **Description**: Combines turning (lathe) and milling capabilities.
    *   描述：结合了车削（车床）和铣削功能。
*   **Application**: Cylindrical parts with milling features (e.g., shafts with slots).
    *   应用：带有铣削特征的圆柱形零件（例如带槽的轴）。

---

## 3. Equipment Selection (设备选型)

When selecting a CNC machine, consider the following parameters:
> 选择 CNC 机床时，请考虑以下参数：

1.  **Travel Range (行程范围)**: Does the workpiece fit within the machine's working envelope?
    *   工件是否在机床的工作范围内？
2.  **Spindle Speed (主轴转速)**: High speed (20k+ RPM) for small tools/aluminum; Low speed, high torque for steel/titanium.
    *   高转速（20k+ RPM）适用于小刀具/铝合金；低速大扭矩适用于钢/钛合金。
3.  **Accuracy & Repeatability (精度与重复定位精度)**: Critical for tight tolerance parts (e.g., +/- 0.005mm).
    *   对于紧公差零件（如 +/- 0.005mm）至关重要。
4.  **Tool Magazine Capacity (刀库容量)**: Number of tools required for the operation.
    *   加工所需的刀具数量。

---

## 4. Key Process Parameters (关键工艺参数)

*   **Cutting Speed (Vc)**: The speed at which the cutting edge moves relative to the workpiece.
    *   切削速度：切削刃相对于工件移动的速度。
*   **Feed Rate (f)**: The distance the tool travels during one revolution of the spindle.
    *   进给率：主轴旋转一周刀具移动的距离。
*   **Depth of Cut (ap)**: The thickness of material removed in one pass.
    *   切削深度：一次走刀去除的材料厚度。

---

## 5. Common Defects & Troubleshooting (常见缺陷与排查)

| Defect (缺陷) | Possible Cause (可能原因) | Solution (解决方案) |
| :--- | :--- | :--- |
| **Chatter (颤纹)** | Tool overhang too long, unstable fixture | Shorten tool, improve fixture rigidity |
| **Burrs (毛刺)** | Dull tool, incorrect feeds/speeds | Change tool, optimize parameters |
| **Dimensional Variation (尺寸变异)** | Thermal expansion, tool wear | Warm-up machine, implement tool life management |
