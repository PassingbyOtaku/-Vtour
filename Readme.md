#易途Vtour
这是一个基于ArkTS开发的AI智慧旅游助手，目前开发到了前端部分。
以下是一份简短的 **hap软件包** 和 **ArkTS语言程序** 的安装与使用说明：

---

### **1. 环境准备**
#### **安装DevEco Studio**
1. 访问 [HarmonyOS开发者官网](https://developer.harmonyos.com/cn/)，下载并安装最新版 **DevEco Studio**（支持Windows/macOS）。
2. 安装时勾选 **ArkTS** 和 **HarmonyOS SDK**。

#### **配置环境**
- 安装 **Node.js**（建议v16+）和 **Ohpm**（HarmonyOS包管理器）。
- 打开DevEco Studio，进入 `Settings > SDK Manager` 配置HarmonyOS SDK路径。

---

### **2. 创建ArkTS项目**
1. 打开DevEco Studio，选择 **Create Project**。
2. 选择 **Application > Empty Ability**（模板），语言选择 **ArkTS**。
3. 配置项目名称、保存路径和HarmonyOS版本，点击 **Finish**。

---

### **3. 构建与运行**
#### **使用模拟器**
1. 点击 `Tools > Device Manager`，选择HarmonyOS模拟器（需提前下载镜像）。
2. 点击 **运行按钮（▶）**，项目将自动编译并部署到模拟器。

#### **真机调试**
1. 手机开启开发者模式（设置 > 关于手机 > 连续点击版本号）。
2. 通过USB连接电脑，授权调试权限。
3. 选择设备后运行项目。

---

### **5. 导出hap软件包**
1. 点击菜单栏 `Build > Build Hap(s)/APP(s) > Build Hap(s)`。
2. 生成的 `.hap` 文件位于 `entry/build/default/outputs/default` 目录。

---

### **6. 安装hap包**
#### **通过命令行安装**
1. 使用 `hdc` 工具（HarmonyOS Device Connector）：
   ```bash
   hdc install path/to/your_app.hap
   ```

#### **通过设备安装**
1. 将 `.hap` 文件拷贝到设备存储。
2. 使用系统应用 **“文件管理”** 找到文件并点击安装。

---

### **常见问题**
- **安装失败**：检查hap签名是否与设备匹配（调试证书需绑定设备UDID）。
- **兼容性问题**：确保hap的SDK版本与设备HarmonyOS版本兼容。
- **USB调试失败**：确认手机已开启“USB调试”和“仅充电模式下允许ADB调试”。

---

### **注意事项**
- 正式发布前需使用 **正式签名证书** 重新打包。
- ArkTS语法与TypeScript/React语法类似，但需遵循HarmonyOS组件规范。

---

以上流程可帮助您快速上手ArkTS开发和hap包的部署。如有更多问题，请参考HarmonyOS官方文档或社区资源。