
## 加入系统命令

* 1、cd sys-shell

* 2、sudo cp stream-2.8.0-SNAPSHOT-exec.jar /opt/java/lib 

* 3、sudo vim /etc/profile
     添加：export STREAM_LIB_PATH=/opt/java/lib
     
* 4、source /etc/profile

* 5、sudo cp cardinality /usr/bin
     sudo cp topk /usr/bin

## 使用示例

    $ echo -e "foo\nfoo\nbar" | topk 
    item count error
    ---- ----- -----
     foo     2     0
     bar     1     0
    
    Item count: 3

    
    $ echo -e "foo\nfoo\nbar" | cardinality 
    Item Count Cardinality Estimate
    ---------- --------------------
             3                    2


