# mcp-gopls 工具使用指南

## 核心能力

mcp-gopls 提供以下 Go 代码分析能力：

- `GoToDefinition` - 跳转到符号定义
- `FindReferences` - 查找符号引用
- `FindImplementers` - 查找接口实现
- `SearchSymbol` - 搜索符号
- `GetDiagnostics` - 获取编译错误
- `Hover` - 获取符号信息
- `RenameSymbol` - 重命名符号
- `FormatCode` - 格式化代码
- `OrganizeImports` - 整理导入

## 优先使用场景

**必须优先使用 mcp-gopls 的场景：**

1. **代码导航** - 查找函数/类型定义和引用时，使用 gopls 而非文本搜索
2. **接口分析** - 理解接口实现关系时，使用 `FindImplementers`
3. **重构准备** - 重命名或修改代码前，使用 `FindReferences` 评估影响
4. **错误诊断** - 分析编译问题时，使用 `GetDiagnostics` 获取准确信息
5. **符号搜索** - 在大型项目中定位符号时，使用 `SearchSymbol`

**基本原则：** 分析 Go 代码时，优先使用 mcp-gopls 工具，它比文本搜索更准确、更快速。
