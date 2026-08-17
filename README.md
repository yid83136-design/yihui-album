# 幻紫星河 · 依慧专属云端相册

纯前端单文件云相册：**ImgBB 图床 + JSONBin 云存储**，无需服务器，双击即可运行。

## 文件说明

| 文件 | 说明 |
|------|------|
| `依慧相册最终.html` | 云端同步版（图片存 ImgBB，数据存 JSONBin，支持跨设备同步、评论区、批量管理） |
| `依慧相册1.html` | 本地版（数据存浏览器 localStorage，图片存 ImgBB） |

## 功能

- 星空粒子动态背景、灯箱浏览、分类筛选
- 批量上传（自动压缩重构）、批量分类、批量删除
- 跨设备云端同步（JSONBin 房间号）
- 图片评论、下载、"展厅呈现"开关
- 完全本地运行，无后端依赖

## ⚠️ 密钥配置（重要）

**本仓库不包含任何 API Key**（密钥已从代码中移除，防止泄露）。

首次使用前，请在浏览器打开页面后按 `F12` → Console（控制台）执行：

```js
// ImgBB 图床 API Key（https://api.imgbb.com 免费申请）
localStorage.setItem('IMGBB_API_KEY', '你的ImgBB Key');

// JSONBin 云存储 Master Key（https://jsonbin.io 获取）— 仅云端同步版需要
localStorage.setItem('JSONBIN_KEY', '你的JSONBin Master Key');
```

配置一次后浏览器会记住（localStorage），下次直接使用。

> 💡 云端同步版首次使用会提示"建立专属云端空间"，自动生成房间号（Bin ID）后填入代码中的 `BIN_ID` 常量即可跨设备同步。

## 安全说明

- 密钥仅保存在你自己的浏览器 localStorage 中，仓库代码内无任何硬编码凭据
