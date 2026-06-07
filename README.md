# Tools for BMS System Engineer

一些用于 BMS 系统工程工作的个人小工具。

这些工具主要用于：

* CAN 日志分析
* DBC 信号解析
* CSV 数据导出
* 工程数据处理与转换

项目中的工具来自实际工程工作中的重复性任务，目标是提高分析效率，减少手工处理。

---

## Available Tools

### CAN Message to CSV Converter
<img width="1080" height="760" alt="image" src="https://github.com/user-attachments/assets/4dfe8fe1-c6eb-45dd-ab19-2204710cf260" />



一个用于 CAN 报文文件解析、DBC 信号解码与 CSV 导出的桌面工具。

当前支持格式：

* BLF
* ASC

功能包括：

* DBC 信号解析
* CSV 批量转换
* 多文件处理

  ---

### CAN Message Merger
<img width="980" height="680" alt="image" src="https://github.com/user-attachments/assets/8d1c6593-63f5-4984-a1d8-92bf3694f8f1" />

一个用于 CAN 报文文件合并的桌面工具。

该工具主要用于处理记录仪/电脑长时间录制后生成的多段 BLF / ASC 报文文件。  
工具会按照报文文件的开始时间顺序进行合并，减少手动打开、切换和整理多个报文文件的重复操作。

当前支持格式：

* BLF
* ASC

功能包括：

* 多段 CAN 报文文件合并
* 按文件开始时间自动排序
* 流式写入合并文件
* 保留原始 timestamp
* 跳过无法读取或不支持的文件
* 输出处理日志与跳过原因

说明：

* 全部为 ASC 文件时，默认输出 `merged.asc`
* BLF 文件或 BLF / ASC 混合文件时，默认输出 `merged.blf`
* 已生成的 `merged.blf` / `merged.asc` 不会再次参与合并

---

## Download

请前往 Releases 页面下载最新版本：

* `CAN_Message_to_CSV_Converter.exe`
* `CAN_Message_Merger.exe`

---

## Notes

* 工具为本地运行
* 不上传任何 CAN 数据
* 工具为工程辅助工具，不替代 CANoe / CANalyzer 等专业分析软件
* DBC 版本需要与报文文件匹配
* 加密文件、严重损坏文件或非标准格式文件可能无法处理
* 当前版本仍在持续优化中
