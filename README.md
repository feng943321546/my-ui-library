# Vue 3 + TypeScript + Vite + vitepress + unplugin-vue-components

# 小沣测试UI库搭建


## ✅ 教学计划（阶段划分）
我会全程教学带你做，分为 6 个阶段，每个阶段都给你写完整代码 + 解释 + 作业（选做）。

### 📦 阶段一：初始化组件库项目
创建组件库项目结构

配置 Vite + Vue 3 + TypeScript

创建一个 Button 组件（第一个组件）

### 🔧 阶段二：组件系统设计
组件结构规范（目录/props/emits）

使用 defineComponent 编写类型安全的组件

引入样式模块 SCSS

### 📚 阶段三：文档系统 + Demo 展示
搭建 VitePress 或 Storybook 展示组件

每个组件都有 demo 和文档说明

### 📦 阶段四：组件按需加载 + 样式隔离
支持 import { MyButton } from 'my-ui' 这种用法

支持每个组件有独立样式

### 🧪 阶段五：测试系统（可选）
用 Vitest 测试每个组件的行为（例如点击是否触发事件）

### 🚀 阶段六：打包发布
使用 Rollup 打包组件库

发布到 NPM 或私有服务器


切换淘宝源（临时或永久）  淘宝镜像由阿里维护，速度快很多
npm config set registry https://registry.npmmirror.com

npm install -D vitepress


我们用社区推荐的 unplugin-vue-components 插件来做按需加载。
npm install -D unplugin-vue-components


置组件多入口 vite.config.build.ts
我们需要新建一个文件：vite.config.build.ts，来专门构建你的组件库（和文档无关）。

npm install -D vite typescript sass rollup-plugin-dts


✅ 步骤一：安装类型打包工具
我们使用 rollup-plugin-dts + tsc 结合生成类型声明：

bash
复制
编辑
npm install -D rollup-plugin-dts typescript