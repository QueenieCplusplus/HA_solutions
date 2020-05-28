# HA solutions
sync or share



* Replica 備份 M/S

    Sync 同步複製。

    share nothing.

* Split Brain 腦裂(failover 容錯)

    using heartbeat && DRBD :
    
    https://ssorc.tw/5928/

    Share memory. 共享數據。

    use heart beat

    需要 SAN, storage area network 共享記憶體。
    
    情境：證帣產業使用此機制，為保障資料鎖住後無法成功交易，但是因涉及共享資源，所以有競奪鎖影響 I/O 的緣故，影響使用者感受。
    
    劣處：網路工作會大量增加！網路設備性能也要求較高，否則網路設備一但運作不佳，對資料一樣沒有保障。

* Cluster Node 叢集

    Sync & Replica & Share Nothig, 同步複製但不共享。
    
   
