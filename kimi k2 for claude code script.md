
Prepare For linux or macos
```shell
export ANTHROPIC_BASE_URL="https://api.moonshot.ai/anthropic"
export ANTHROPIC_AUTH_TOKEN="api-key-token"
claude
```
Put this into ~/.bashrc or ~/.zshrc on the top of  the file
```shell
kimi() {
  export ANTHROPIC_BASE_URL="https://api.moonshot.ai/anthropic/"
  export ANTHROPIC_AUTH_TOKEN="your-kimi-api-key"
  claude "$@"
}
```
Run `source ~/.bashrc` or `source ~/.zshrc` 
Kill the terminal and open again and run `kimi` -> It will automatically call the claude code command line application