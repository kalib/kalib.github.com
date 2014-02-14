---
layout: post
title: "Alterando os parâmetros do kernel em tempo real com o Systcl"
date: 2014-02-13 22:02
comments: true
keywords: Linux,Kernel,Parâmetros,Sysctl
description: Utilize o sysctl para alterar parâmetros do kernel com o mesmo em execução.
categories:
- Linux
- Seguranca
- Cultura Hacker
---
{% img left /imgs/linux-kernel.jpg 'Linux Kernel' %}
**O** *kernel*, em se tratando de sistemas operacionais, é o núcleo e componente mais importante da maioria dos computadores. Basicamente, serve de ponte entre os aplicativos e o processamento real de dados feito a nível de hardware. É ele o responsável por gerenciar os recursos do sistema, podendo oferecer uma camada de abstração de nível mais baixo para os recursos, como processadores e dispositivos de entrada/saída, que os softwares aplicativos devem controlar para realizar sua função. Com o GNU/Linux não é diferente. O núcleo Linux (Linux Kernel) forma a estrutura do sistema operacional GNU/Linux.

**C**omo é de se esperar, o kernel possui diversos parâmetros configurados que definirão as características do seu sistema, controle de dispositivos, módulos, drivers, etc. Por vezes faz-se necessário alterar algum parâmetro do kernel para alguma tarefa ou rotina específica, portanto que tal ganhar tempo e alterar um ou mais parâmetros do kernel *on the fly*?!

**O** comando *sysctl* pode ajudar nesta tarefa. Ele ajuda a configurar os parâmetros do kernel em tempo de execução.

**P**ara listar os atuais parâmetros de seu kernel digite:

```
 [kalib@tuxcaverna ~]$ sysctl -a
  
 abi.vsyscall32 = 1
 debug.exception-trace = 1
 dev.cdrom.autoclose = 1
 dev.cdrom.autoeject = 0
 dev.cdrom.check_media = 0
 dev.cdrom.lock = 1
 dev.hpet.max-user-freq = 64
 dev.mac_hid.mouse_button2_keycode = 97
 dev.mac_hid.mouse_button3_keycode = 100
 dev.mac_hid.mouse_button_emulation = 0
 dev.scsi.logging_level = 0
 fs.aio-max-nr = 65536
 fs.aio-nr = 41192
 fs.binfmt_misc.status = enabled
 fs.dentry-state = 177183        161128  45      0       0       0
 fs.dir-notify-enable = 1
 fs.epoll.max_user_watches = 1209446
 fs.file-max = 586836
 fs.file-nr = 8992       0       586836
 fs.inode-nr = 96800     290
 fs.inotify.max_user_watches = 8192
 fs.lease-break-time = 45
 kernel.sched_cfs_bandwidth_slice_us = 5000
 kernel.sched_child_runs_first = 0
 kernel.version = #1 SMP PREEMPT Fri Jan 31 10:22:54 CET 2014
 kernel.watchdog = 1
 kernel.watchdog_thresh = 10
 kernel.yama.ptrace_scope = 1
 net.core.bpf_jit_enable = 0
 net.core.busy_poll = 0
 net.ipv4.cipso_cache_bucket_size = 10
 net.ipv4.conf.all.accept_local = 0
```

**O** retorno deste comando é bastante extenso, portanto colei aqui apenas algumas linhas aleatórias de meu resultado.

**P**ara alterar temporariamente um parâmetro, utilize o parâmetro -w do sysctl, indicando a variável que deseja alterar e o novo valor que será utilizado para a mesma.

```
 [kalib@tuxcaverna ~]$ sysctl -w {nome-da-variável=valor}
```

**N**o caso acima a(s) alteração(ões) será(ão) perdida(s) após a reinicialização do sistema.

**C**aso deseje realizar alterações permanentes, edite o arquivo */etc/sysctl.conf* e em seguida aplique suas modificações com o parâmetro -p do sysctl.

```
 [kalib@tuxcaverna ~]$ sysctl -p
```

**D**esta forma, após a reinicialização suas modificações permanecerão ativas.

**H**appy Hacking!