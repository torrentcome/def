# Selinux
## SElinux = Security-Enhanced Linux 

As part of the Android security model.
Android uses SELinux to enforce mandatory access control (MAC) over all processes.
Even processes running with root/superuser privileges (a.k.a. Linux capabilities).
SELinux enhances Android security by confining privileged processes and automating security policy creation.

### Operation
SELinux operates on the principle of default denial: Anything not explicitly allowed is denied. SELinux can operate in two global modes
- Permissive mode, in which permission denials are logged but not enforced.
- Enforcing mode, in which permissions denials are both logged and enforced.

### Schema
<figure>
  <img src ="../image/selinux.png" />
</figure>
