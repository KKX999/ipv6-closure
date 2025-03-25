# ipv6禁用指令（适用于Debian 其他自行尝试）

第一步
```
echo "net.ipv6.conf.all.disable_ipv6=1" >> /etc/sysctl.conf
```

第二步
```
echo "net.ipv6.conf.default.disable_ipv6=1" >> /etc/sysctl.conf
```
第三步
```
echo "net.ipv6.conf.lo.disable_ipv6=1" >> /etc/sysctl.conf
```
保存生效
```
sysctl -p
```
测试禁用成功
```
cat /proc/sys/net/ipv6/conf/all/disable_ipv6
```
回复1代表禁用成功
