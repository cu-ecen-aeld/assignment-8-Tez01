# echo "hello world" > /dev/faulty
Unable to handle kernel NULL pointer dereference at virtual address 0000000000000000 — a NULL pointer dereference caused a kernel oops.
Mem abort info:
  ESR = 0x0000000096000044
  EC = 0x25: DABT (current EL), IL = 32 bits
  SET = 0, FnV = 0
  EA = 0, S1PTW = 0
  FSC = 0x04: level 0 translation fault
Data abort info:
  ISV = 0, ISS = 0x00000044, ISS2 = 0x00000000
  CM = 0, WnR = 1, TnD = 0, TagAccess = 0
  GCS = 0, Overlay = 0, DirtyBit = 0, Xs = 0
user pgtable: 4k pages, 48-bit VAs, pgdp=0000000041bba000
[0000000000000000] pgd=0000000000000000, p4d=0000000000000000
Internal error: Oops: 0000000096000044 [#1]  SMP
Modules linked in: hello(O) faulty(O) scull(O)
CPU: 0 UID: 0 PID: 132 Comm: sh Tainted: G           O        6.18.7 #1 NONE 
Tainted: [O]=OOT_MODULE - kernel is tainted because of out of tree modules loaded
Hardware name: linux,dummy-virt (DT)
pstate: 80000005 (Nzcv daif -PAN -UAO -TCO -DIT -SSBS BTYPE=--)
pc : faulty_write+0x8/0x10 [faulty]     - fault occured at this program counter
lr : vfs_write+0xbc/0x3b0
sp : ffff800080f1bd30
x29: ffff800080f1bda0 x28: ffff000001ca4ec0 x27: 0000000000000000
x26: 0000000000000000 x25: 0000000000000000 x24: 0000000000000000
x23: 0000000040000000 x22: 000000000000000c x21: 0000aaaaceb6b9f0
x20: ffff000001c71000 x19: 000000000000000c x18: 0000000000000000
x17: 0000000000000000 x16: 0000000000000000 x15: 0000000000000000
x14: 0000000000000000 x13: 0000000000000000 x12: 0000000000000000
x11: 0000000000000000 x10: 0000000000000000 x9 : 0000000000000000
x8 : 0000000000000000 x7 : 0000000000000000 x6 : 0000000000000000
x5 : 0000000000000000 x4 : ffff800078d3a000 x3 : ffff800080f1bdd0
x2 : 000000000000000c x1 : 0000000000000000 x0 : 0000000000000000
Call trace:
 faulty_write+0x8/0x10 [faulty] (P)
 ksys_write+0x70/0x110
 __arm64_sys_write+0x1c/0x30
 invoke_syscall+0x48/0x110
 el0_svc_common.constprop.0+0x40/0xe0
 do_el0_svc+0x1c/0x30
 el0_svc+0x34/0xf0
 el0t_64_sync_handler+0xa0/0xf0
 el0t_64_sync+0x198/0x19c
Code: ???????? ???????? d2800001 d2800000 (b900003f) 
---[ end trace 0000000000000000 ]---

Welcome to Buildroot
buildroot login:  -     Wasn't a kernel panic, cz we again went to login screen
                        but some internal state could potentially be inconsistent
