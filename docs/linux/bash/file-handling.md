# File Handling
Linux/Unix files downloaded from the Internet usually are packaged and compressed for faster and more reliable file transfer. Files ending with tgz are known as tar-ball. If an archive is compressed with an external tool, the compression program adds its own suffix as usual, resulting in filename endings like

* ".tar.z"
* ".tar.gz"
* ".tar.bz2"
* ".tgz"

To open such file type the following command at Linux shell prompt (GNU tar syntax):
```shell
$ tar -zxvf filename.tgz
$ tar -zxvf filename.tar.gz
$ tar -jxvf filename.tar.bz2gi
```