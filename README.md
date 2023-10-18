## 修改設定

### Step 1. 開啟 /etc/sysctl.conf

請於終端機輸入下方指令

```shell=
sudo vi /etc/sysctl.conf
```

### Step 2. 新增設定

在 /etc/sysctl.conf 檔案最後加入下面兩行設定

```shell=
vm.max_map_count=262144
fs.file-max=65536
```

> vm.max_map_count: 控制一個進程可以擁有的虛擬記憶體映射數量的上限  
> fs.file-max: 允許的文件描述符數目的上限

### Step 3. 設定生效

請於終端機輸入下方指令

```shell=
sudo sysctl -p
```
