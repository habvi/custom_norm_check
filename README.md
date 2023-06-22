## custom_norm_check

42 の [norminette](https://github.com/42School/norminette) command が使える状態であり、提出前はヘッダーなし・コメント・空行などを許容してほしい…という時に使えるかもしれないスクリプトです。

### 1. set norm check paths
Edit [norm.py](norm.py) : `NORM_CHECK_PATH` &  
```shell
python3 norm.py
```
default check path :
```
includes, srcs
```

or  

Pass args
```shell
python3 norm.py dir dir/file file ...
```

<br>

### 2. set ignore warnings
Edit [norm.py](norm.py) : `IGNORE_WARNING`  
default ignored : 
```
LINE_HEADER = "INVALID_HEADER"
LINE_COMMENT = "WRONG_SCOPE_COMMENT"
LINE_EMPTY = "EMPTY_LINE_FUNCTION"
```

<br>

- 無視したい warning を自由に変更可 (追加・削除)
- `norm.log` が作成され、無視する前の結果が出力されます
- `OK!` や `Error!` などがパスに含まれる場合は未対応です
- 最終確認は `norminette` にて