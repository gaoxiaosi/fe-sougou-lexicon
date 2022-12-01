# 前端开发词库
搜集前端常用词并构建词库，导入到各个输入法中，提高输入效率，暂时只支持搜狗输入法。

**在线词汇**：https://gaoxiaosi.github.io/fe-lexicon/

**使用方法**：`pnpm run convert`，将data目录下的词库转换成相应输入法词库文件格式，如搜狗的**sougou.txt**，然后将该文件上传到搜狗词库。词库地址：https://pinyin.sogou.com/dict/detail/index/148103。

# 使用最近热门技术重构小工具，浅谈体验
- `Vite`：
  - **优点**：确实小而美，轻且快，原生支持`ES Module`和`TypeScript`，开箱即用，大部分的默认配置足够使用，降低使用门槛。
  - **缺点**：Bug和不兼容问题，有但不多。打包依赖`rollup`，还是希望自研的比较创新的打包方式。更新频繁，对于技术发展是好事，对于开发稳定应用就未必。`Vite2`我一直没用，`Vite3`就来了。不好说和`Webpack`孰优孰劣，最近Vercel新出的基于Rust的`Turbopack`就已经在路上了！
  - **其他**：`Vue3`依旧优秀、`Vuepress`和`Vitepress`构建文档、`Vue2`用TS重构，最新版本适配`Composition API`，Vue团队在做生态，野心很大。
- `Svelte`：
  - **优点**：语法简洁，写小应用很香，上手难度一般，之前看过测试当应用变大之后性能未必优于Vue。
  - **缺点**：生态还处于起步阶段，配套UI框架少，出问题也不好找解决方案。
  - **其他**：小而美终究是小众，业务的复杂性驱使框架走向大而全甚至臃肿。
- `PNPM`：
  - **优点**：比`NPM`结构更合理一些，下载速度更快，解决幽灵依赖问题，节省硬盘空间，已有很多公司开始使用，应该会是未来。
  - **缺点**：使用的时间还不多，可能有兼容问题？对于只用小部分功能和常规包来说应该没什么问题。
- `Tailwind CSS`：
  - **优点**：体验90分，按需打包的，文件中没有出现的类不会打包进去，大量使用内置class，所有开发人员一看就知道，一定程度来说也是一种CSS规范。
  - **缺点**：扣10分是有时候要写太多的class，显得DOM很臃肿，写得很爽，看着不简洁。由于按需打包，如果动态拼接使用它内置的class时，需要在一些地方进行声明，否则不会打包进去导致样式不起作用。