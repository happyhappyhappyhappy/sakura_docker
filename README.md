# wsl2-ubuntuで作成したdockerの為のプロジェクト 
[コマンドリンク](https://docs.docker.com/engine/reference/commandline/docker/)
## 20210306確認
イメージ作成済みからdockerコンテナを作成する
「alpine_sandbox:1.o」としてイメージは作成完了
~~~ 
docker run --init --name "alpine_sandbox0" -it alpine_sandbox:1.0
~~~
ここで入った場合、Linuxのコマンドラインに戻るには「Ctrl+p -> Ctrl+q」を使う。「detatch」と同じ作業をする。
** 決してexitで終わってはいけない **
なぜなら、コンテナそのものが終了してしまうから。
次に入るときはexecオプションで入る
~~~
docker exec -it alpine_sandbox0 /bin/sh
~~~
こうしたとき、exitで抜けても上がったままなので最終的に止めるには

~~~
docker stop alpine_sandbox0
~~~
で終了する。
と思うがもう一度チェックする。
