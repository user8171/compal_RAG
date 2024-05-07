# 請閱讀

clone 下來後請依需求以及實際情況修改 env 環境變數

## main.py

若 qdrant 容器所在的裝置為遠端裝置,請將<base_url>改成"ssh://<remote_username>@<remote_ipv4>"
若容器所在的裝置是本地的話,請依作業系統版本去做修改

- linux<br>
  以下範例為非 root 用戶的 docker desktop 的舉例
  ```
    unix:///home/{os.getlogin()}/.docker/desktop/docker.sock
  ```
- windows
  請參考[這裡](https://docs.docker.com/reference/cli/dockerd/#bind-docker-to-another-hostport-or-a-unix-socket)

  <br><br>

```python
if __name__ == "__main__":
    utils.Functional.start_qdrant_db(base_url=<base_url>)
    demo.launch(server_port=7861)
```

=v=