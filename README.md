# 代码质量检查模板项目

这是一个集成了各种代码质量检查工具的Next.js模板项目，旨在帮助开发团队保持高质量的代码标准。

## 🛠️ 集成的检查工具

### 代码质量检查

- **ESLint**: 静态代码分析，检查JavaScript/TypeScript代码问题
  - 包含React、TypeScript、Jest和可访问性规则
- **Prettier**: 代码格式化工具，确保代码风格一致
- **TypeScript**: 静态类型检查
- **Jest**: 单元测试框架，包含覆盖率报告

### 性能和可访问性检查

- **Lighthouse CI**: 检查网站性能、可访问性、SEO等
- **Pa11y**: 自动化可访问性测试

### 安全扫描

- **npm audit**: 检查依赖项中的已知安全漏洞
- **Snyk**: 深度安全扫描

### 依赖管理

- **Dependabot**: 自动检测过时依赖
- **依赖审查**: 检查新依赖是否有安全问题或许可证冲突

### 本地开发检查

- **Husky**: Git hooks工具
- **lint-staged**: 在提交前运行检查，只检查修改的文件

## 🚀 GitHub Actions工作流

本项目包含多个GitHub Actions工作流，自动执行各种检查：

1. **代码质量检查工作流** (`code-quality.yml`)
   - 运行ESLint和Prettier检查
   - TypeScript类型检查
   - 执行Jest测试和覆盖率报告
   - 安全扫描
   - 构建检查和包大小分析

2. **依赖审查工作流** (`dependency-review.yml`)
   - 检查新添加的依赖项是否有安全问题
   - 检查许可证合规性
   - 报告过时的依赖项

3. **性能和可访问性工作流** (`lighthouse.yml`)
   - 运行Lighthouse性能测试
   - 自动化可访问性检查

## 📋 如何使用

1. **克隆此仓库作为模板**:
   ```bash
   git clone https://github.com/tckwgd/code-quality-template.git your-project
   cd your-project
   ```

2. **安装依赖**:
   ```bash
   npm install
   ```

3. **初始化Husky**:
   ```bash
   npm run prepare
   ```

4. **开发**:
   ```bash
   npm run dev
   ```

5. **构建**:
   ```bash
   npm run build
   ```

6. **测试**:
   ```bash
   npm test
   ```

## 📊 检查阈值

- **测试覆盖率**: 80%（可在`jest.config.js`中调整）
- **Lighthouse性能预算**: 详见`.github/lighthouse/budget.json`

## 🧩 定制

所有检查工具都可以根据项目需求进行调整:

- **ESLint**: 编辑`.eslintrc.json`
- **Prettier**: 编辑`.prettierrc`
- **TypeScript**: 编辑`tsconfig.json`
- **Jest**: 编辑`jest.config.js`
- **GitHub Actions**: 编辑`.github/workflows/`下的文件

## 📝 许可证

MIT