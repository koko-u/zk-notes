# zkの使い方

## zk new - ノートを作成する

単純に作成する
```
zk new
```

ディレクトリを指定する
```
zk new rust
```

タイトルを指定する
```
zk new rust --title "sqlxの使い方"
```

テンプレートを作成しておいて、それを zk new する時に指定することもできる

## zk list - ノートを検索する

単純にタイトルを一覧する
```
zk list
```

ディレクトリ以下を一覧する
```
zk list rust
```

全文検索する
```
zk --match "sqlx"
```

複数語でマッチする
```
zk --match "sqlx axum"
```

タグで検索する
```
zk --tag "rust"
```

参照 [zk filtering note](https://zk-org.github.io/zk/notes/note-filtering.html?utm_source=chatgpt.com)

## zk edit - ノートを編集する

編集対象を fzf で探して編集する
```
zk edit --interactive
```

対象を検索しつつ探すこともできる
```
zk edit -i --match "sqlx"
```

## fish の関数を作成する

zk コマンドがこのままでは .zk フォルダのある場所でしか利用できない。
`--work-dir` オプションを利用するように、fish の関数を定義する

場所
`~/.config/fish/functions/zk.fish`

内容
```fish
function zk
    command zk --working-dir "$HOME/notes" $argv
end
```
