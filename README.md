# hello-world
practise more. Focus, investigate and balance


# both stdout and stderr are redirect to the same log file

[zyw@fedora ~]$  ### 1 file is there ###### 
[zyw@fedora ~]$ touch file
[zyw@fedora ~]$ 
[zyw@fedora ~]$ stat file > fstat.log 2>&1
[zyw@fedora ~]$ 
  ################## 2. stdout ##################
[zyw@fedora ~]$ cat fstat.log 
  文件：file
  大小：0         	块：0          IO 块：4096   普通空文件
设备：fd00h/64768d	Inode：278976      硬链接：1
权限：(0664/-rw-rw-r--)  Uid：( 1000/     zyw)   Gid：( 1000/     zyw)
环境：unconfined_u:object_r:user_home_t:s0
最近访问：2018-06-02 20:17:08.429612159 +0800
最近更改：2018-06-02 20:17:08.429612159 +0800
最近改动：2018-06-02 20:17:08.429612159 +0800
创建时间：-
[zyw@fedora ~]$ 
[zyw@fedora ~]$ rm file 
[zyw@fedora ~]$ 
################### 3. stderr ###################
[zyw@fedora ~]$ stat file > fstat.log 2>&1
[zyw@fedora ~]$ 
[zyw@fedora ~]$ cat fstat.log 
stat: 无法获取'file' 的文件状态(stat): 没有那个文件或目录
[zyw@fedora ~]$ 
[zyw@fedora ~]$
