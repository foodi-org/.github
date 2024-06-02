## Hi there 👋

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
🌈  something need read before start。（具体些什么我还没想好 😁）

### 关于`Golang`
* 版本: 1.22.3
* 包管理: `go mod` (应该不用说吧☺️)

### 关于框架: 使用 `go-zero` 包含 `proxy` 和 `serivice`. 在框架基础上做了相应修改。
* 配置移至`consul`，原框架中静态配置文件请配置 `consul`连接地址信息，`condfig`中请定义好你需要的配置结构体
* 服务注册与发现放弃使用`etcd`，统一整合到`consul`
* 集成了`gorm`，该方式为了方便习惯与使用`gorm`迁移同步`model`，db操作还请使用`sqlx`(还未解决切换到使用`gorm`情况下链路追踪问题)

### 你需要：
* `consul`: 作为配置中心和服务注册与发现
* `kong`: 作为网关
* `mysql`: 版本5.7
* `redis`: 缓存
