# OpenClaw Sync

以 DESKTOP-77NL2I1 为基准的 OpenClaw 配置同步方案。

## 同步内容

```
openclaw-sync/
├── .openclaw/
│   ├── identity/           # 设备认证（每个设备独立，需保密）
│   │   ├── device.json
│   │   └── device-auth.json
│   └── workspace/
│       └── skills/        # 自定义安装的 skills
│           ├── find-skills/
│           └── skillhub-preference/
└── agent-workspace/       # Agent 工作区配置
    ├── AGENTS.md
    ├── SOUL.md
    ├── TOOLS.md
    ├── USER.md
    ├── IDENTITY.md
    ├── MEMORY.md
    └── HEARTBEAT.md
```

## 使用方式（其他电脑）

### 1. 首次部署

```powershell
# 克隆仓库
git clone <你的仓库URL> C:\Users\Administrator\openclaw-sync

# 复制配置（需要覆盖时）
cp -Recurse -Force C:\Users\Administrator\openclaw-sync\.openclaw\* C:\Users\Administrator\.openclaw\
cp -Recurse -Force C:\Users\Administrator\openclaw-sync\agent-workspace C:\Users\Administrator\.qclaw\workspace-agent-1ec15734
```

### 2. 每次更新

当基准电脑有更新时，我会告诉你执行：

```powershell
cd C:\Users\Administrator\openclaw-sync
git pull
# 然后按上面的覆盖命令重新复制
```

---

**规则**：
- 基准电脑 = DESKTOP-77NL2I1（这台）
- 你告诉我更新 → 我同步到其他电脑
- 你没说 → 我不主动更新