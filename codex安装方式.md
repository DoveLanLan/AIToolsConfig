### 使用nvm 切换node版本

```bash
nvm install 22
nvm use 22
```

### 然后安装Codex

```bash
npm install -g @openai/codex
```

### 安装完成后运行Codex

```bash
codex  
```

### 运行成功后按control + c退出

```bash
cd ~/.codex && ls -all
```

![1763100108927](image/codex安装方式/1763100108927.png)

### 打开这个config.toml文件

```bash
code ~/.codex/config.toml
```
添加下面内容
```toml
model_provider = "codex"
model = "gpt-5.1"
model_reasoning_effort = "high"
disable_response_storage = true

[model_providers.codex]
name = "codex"
base_url = "https://new.xychatai.com/codex/v1"
wire_api = "responses"
env_key = "CODEX_API_KEY"
requires_openai_auth=true
```

## macOS 默认 shell 现在一般是 zsh（Catalina 及以后），如果你没手动切过，就按 zsh 操作；如果确定自己在用 bash，把文件名换一下即可。
##打开配置文件

# zsh 用户
```bash
nano ~/.zshrc
```
# bash 用户
```bash
nano ~/.bash_profile
```
在文件末尾新起一行写入

```bash
export CODEX_API_KEY="sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```
保存退出
让改动立即生效

# zsh
```bash
source ~/.zshrc
```
# bash
```bash
source ~/.bash_profile
```
验证
```bash
echo $CODEX_API_KEY
```
能打印出密钥就说明 OK。
