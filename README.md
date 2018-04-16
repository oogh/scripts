# 脚本收集

> 收集一些比较感兴趣的脚本

## 说明

内容来自网络，每个收集都会注明来源。

## 脚本

- [ssrmu.sh](https://github.com/oogh/scripts/blob/master/ssrmu.sh)
  - 来源: https://github.com/ToyoDAdoubi/doubi

  - 使用: 

    ```shell
    wget -N --no-check-certificate https://raw.githubusercontent.com/oogh/scripts/master/ssrmu.sh && chmod +x ssrmu.sh && bash ssrmu.sh
    ```

- [bbr.sh](https://github.com/oogh/scripts/blob/master/bbr.sh)

  - 来源: https://github.com/teddysun/across

  - 使用:

    ```shell
    wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh
    ```

  - 校验是否成功

    ```shell
    sysctl net.ipv4.tcp_available_congestion_control
    // 返回 net.ipv4.tcp_available_congestion_control = bbr cubic reno

    sysctl net.ipv4.tcp_congestion_control
    // 返回 net.ipv4.tcp_congestion_control = bbr

    sysctl net.core.default_qdisc
    // 返回 net.core.default_qdisc = fq

    lsmod | grep bbr
    // 有返回值，说明启动成功
    ```

    ​
