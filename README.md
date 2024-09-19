### MariaDB Galera_cluster Maxscale 공부정리
---

<aside>
💡 **Galera Cluster**

- **Mysql & MariaDB 지원**
- **Multi Master : 모든 노드에서 일기 쓰기가 가능합니다.**
- **동기적 복제 : 슬레이브 지연이 없고 노드 충돌시에 데이터 손실이 없습니다.**
- **일관적인 데이터: 모든 노드는 같은 상태를 유지합니다.**
- **Multi-thread  slave : 어떠한 워크로드에서도 더 나은 성능을 가능하게 합니다.**
- **Hot standbt : 장애 복구시 down-time이 없습니다.**
- **read/wirte split 이 필요 없습니다**
- **Inoodb 엔진만 완벽히 지원한다.**
- **동기적 복제이기에 성능이 낮은 노드에 의해 전체 성능이 결정되게 된다.**
- **별도의 vip는 필요없다.**
- **binarylog 로그를 전송하는 전송하고 slave에서 릴레이로그(bin 로그를 전송 받는)를 받는 형식으로 동작한다.**
- **비동기 : 다른 노드에서 데이터를 받았는지 확인안하고 바로 응답.**
- **반동기: 한개의 복제본이라도 데이터를 받았는지는 확인함.**
- **동기 : 모든노드가 트랜잭션을 받았는지를 확인**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/7540eda1-50b0-4704-924e-78f9872ec9b8/f4421e3c-0bce-462b-8fb8-ebafbf49dec4/image.png)

