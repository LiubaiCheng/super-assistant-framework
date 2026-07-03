# 工具使用技巧与注意事项

## 文件管理规范
- **核心原则**：文件必须归入文件夹，禁止在根目录随意创建文件
- **根目录规则**：只允许文件夹和系统级文件（MEMORY/SECRET/USER/SOUL/WIKI/INDEX/LOG/heartbeat_daily/heartbeat_weekly）
- **文件归位**：知识页面→素材库 | 日志索引→素材库 | 原始文档→raw/ | 设定→基础设定/ | 用户上传→用户上传/ | 晨读→InkWell晨读/ | 临时文件→.tmp/

## 通用工具注意事项
- **bash**：curl请求需设Content-Type，JSON注意转义，支持并行多命令
- **fetch_web**：支持批量URL，境外站点访问失败改用search_web
- **微信文章抓取**：微信公众号反爬拦截，优先搜标题+转载找第三方平台内容，抓不到时提示用户提供正文/非微信链接
- **edit_file**：old_string必须完全匹配内容；写失败降级为read_file全量覆盖write
- **parse_file**：PDF解析失败降级为pdftotext命令行提取
- **skill_load**：加载后优先读取SKILL.md详细文档

## SkillSpector安全扫描
- 安装路径：/tmp/SkillSpector/（需source .venv/bin/activate后使用）
- 用法：`skillspector scan <path> --no-llm` 纯静态扫描
- 输出：终端/JSON/Markdown/SARIF四种格式，支持`--baseline`做误报抑制
- 新装skill必须先经SkillSpector审查

## 工程纪律（借鉴Superpowers方法论）
- **验证先于声称**：声称"完成""已修复""通过"之前，必须跑验证命令并确认输出。禁止用"应该没问题""看起来好了"替代实际验证
- **根因优先**：遇bug/失败时，先完成根因调查再修。禁止未定位根因就"先试试改X"。3次修不好→质疑架构而非继续修
- **交付前自检**：文件交付前确认路径存在、格式正确、内容完整。不交文件夹/未生成文件/不可确认路径

## 上下文效率（借鉴Headroom理念）
- **内容感知提取**：读大文件时先判断需要哪部分，用offset/limit分段读，避免全量加载
- **失败学习**：任务失败后提炼原因写入TOOLS.md，避免同类失败重复发生
