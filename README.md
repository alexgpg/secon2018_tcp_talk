Secon 2018 Забег по типичным граблям TCP приложений в Linux
============================================================

Потерять данные в TCP

[TCP Is Not Reliable](https://blog.h2o.ai/2013/08/tcp-is-not-reliable/)

[The ultimate SO_LINGER page, or: why is my tcp not reliable](https://blog.netherlabs.nl/articles/2009/01/18/the-ultimate-so_linger-page-or-why-is-my-tcp-not-reliable)

# Heartbeats: Проверка жизни соединения

[TCP and heartbeats by Martin Sústrik](http://250bpm.com/blog:22)

E-mail тред [Re: Protocol for TCP heartbeats?](https://www.ietf.org/mail-archive/web/ietf/current/msg62500.html)

## Инструменты

### strace

Доклады

[Strace — новые возможности](https://youtu.be/2K1M9ggC8Gk)

[Can strace make you fail?](https://youtu.be/bD4WC3-soA8)

Workflow

~~~
ps -eF|grep myapp
strace -f -yy -e trace=network -p PID
~~~

### Трассировщики eBPF

[Что такое eBPF](http://www.brendangregg.com/ebpf.html)

[BPF Compiler Collection](https://github.com/iovisor/bcc)

  * tcpaccept
  * tcpconnect
  * tcpconnlat
  * tcplife
  * tcpretrans
  * tcptop
  * tcptracer

Мой трассировщик [deeptcptracer](https://github.com/alexgpg/deeptcptracer)

### Почитать

Книга [High Performance Browser Networking by ILYA GRIGORIK](https://hpbn.co/)
