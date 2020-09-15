# `actix-files` cannot serve utf-8 contents

To reproduce:

```sh
cargo install
cargo run
```

Go to `http://localhost:8888/static/%E4%B8%AD%E6%96%87%E6%96%87%E4%BB%B6.txt`. 

The correct content of the text file is:

```txt
中文内容显示为乱码。

English is OK.
```

However, what is displayed is:

```txt
涓枃鍐呭鏄剧ず涓轰贡鐮併€�

English is OK.
```
