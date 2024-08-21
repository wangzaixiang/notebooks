# my jupyter notebooks

[Polars 概念解析](polars/polars-1.ipynb)

## 环境

```shell
# create venvs
python3 -m venv ~/venvs/polars 

# activate venvs under nushell
source ~/venvs/polars/bin/activate.nu

# running notebook
jupyter notebook
```

# nushell 配置
```nushell
let ENV_POLARS_ROOT = "/Users/wangzaixiang/venvs/polars"
def left_prompt [] {
    $"\(($ENV_POLARS_ROOT)\)"
}

$env.VIRTUAL_ENV = $ENV_POLARS_ROOT
$env.PROMPT_COMMAND = { left_prompt }
$env.PATH = ($env.PATH | prepend $"($ENV_POLARS_ROOT)/bin")
```
