# Installation

1. `sudo apt -y install bridge-utils cpu-checker libvirt-clients libvirt-daemon libvirt-daemon-system qemu qemu-kvm`

2. `sed -i -e 's/\#vnc_listen.*$/vnc_listen = "0.0.0.0"/g' /etc/libvirt/qemu.conf`

Để mở console

3. `sed -i -e 's/.*libvirtd_opts.*/libvirtd_opts="-l"/' /etc/default/libvirtd`

Lắng nghe port 16509

4. Cấu hình lại trong file `/etc/libvirt/libvirtd.conf`

5. `systemctl mask libvirtd.socket libvirtd-ro.socket libvirtd-admin.socket libvirtd-tls.socket libvirtd-tcp.socket`

Để mask các file vào `/etc/systemd/system`

6. `systemctl restart libvirtd` 

hoàn thành
