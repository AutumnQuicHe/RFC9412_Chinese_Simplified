---
title: "2. ORIGIN HTTP/3帧"
anchor: "2_The_ORIGIN_HTTP3_Frame"
weight: 200000
rank: "h1"
---

ORIGIN HTTP/3帧允许服务器向客户端指示一个或多个源站（origin）[RFC6454](#RFC6454)，服务器希望客户端将这些源站视为该连接发生时所处源站集合（Origin Set，[ORIGIN](#ORIGIN)的[第2.3章](https://www.rfc-editor.org/info/rfc8336/#section-2.3)）的成员。

该帧负载的语义与[ORIGIN](#ORIGIN)中定义的HTTP/2帧的语义完全相同。HTTP/2将流0预留给与连接状态相关的帧，而HTTP/3为此目的定义了一对单向流，称为“控制流（control streams）”。

当[ORIGIN](#ORIGIN)指出ORIGIN帧在流0上发送时，应将其理解为HTTP/3的控制流：即ORIGIN帧由服务器在服务器的控制流上发送给客户端。

HTTP/3在通用帧布局中未定义Flags字段。由于尚未为ORIGIN帧定义任何标志位，本规范不在HTTP/3中定义传递此类标志位的机制。
