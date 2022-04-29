---
title: "Z"
linkTitle: "Z"
weight: 4
description: >
  ## Zero Client
---

> Not every system needs its own dedicated OS, Databases, Processors.

Zero client, also known as ultrathin client, is a server-based computing model in which the end user's computing device has no local storage.

A typical zero client product is a small box that serves to connect a keyboard, mouse, monitor and Ethernet connection to a remote server. The server, which hosts the client's operating system (OS) and software applications, can be accessed wirelessly or with cable. Basically, they are bare-bones computers that rely on a server to handle many functions that a traditional PC, or thick client, would normally handle using its own hardware and software.

Zero clients are often used in a virtual desktop infrastructure (VDI) environment. This makes them ideal for remote work situations or distributed work environments.

### How do zero clients work?

<p align="center">
    <img src="https://www.sunde.net.pk/wp-content/uploads/2016/03/NetPoint-Sharing-solution-architecture.png" alt="Zero Clients' Working" />
</p>

Zero clients are essentially input/output (I/O) redirection units. All user inputs (mouse clicks, keystrokes, etc.) are sent to a remote server, which returns data to display on a connected monitor. This is where the name "zero client" comes from -- almost all processing takes place on the server side, and almost zero processing takes place client-side.

Zero clients don't use an operating system and instead use firmware to connect to a remote device. An onboard processer is designed to use a sole protocol to communicate with a remote server -- usually PCoIP protocol to connect with the device. Firmware can be altered to support a different sole protocol, such as Microsoft RDP or Citrix HDX, but can only generally be optimized for one protocol at a time.

No data is stored on zero clients, because there is no local storage. Therefore all applications are provisioned and managed on a server in a remote data center, and served to the zero client device using its protocol.

### Zero client hardware specifications

Zero clients are often physically small pieces of hardware -- meaning they have a small form factor. They are generally not more than a foot tall, around two inches wide, and weigh approximately two pounds. They typically include a processor with basic firmware installed on it, and some combination of ports including HDMI, DVI, DisplayPort, USB and Ethernet. There is also a port for a power supply.

Zero clients also tend to have line out and mic in ports, and usually also support wireless and VESA mounting. Some zero clients support multiple monitors.

### Benefits of zero client devices

- Power usage can be as low as 1/50thof fat client requirements.

- Devices are much less expensive than PCs or thin clients.

- Efficient and secure means of delivering applications to end users.

- No software at the client means that there is no vulnerability to malware.

- Easy administration.

- In a virtual desktop environment, administrators can reduce the number of physical PCs or blades and run multiple virtual PCs on server-class hardware.

- Improved user experience stemming from increased hardware efficiency.

<p align="center">
    <img src="https://v2cloud.com/wp-content/uploads/2021/11/Benefits-of-Using-a-Zero-Client-V2-Cloud-Solution-inc-new-2021.png.webp" alt="Benefits" />
</p>

### Drawbacks of zero client devices

- They often have limited ability to render graphics.

- Performance depends on network connection because they rely on remote servers to do almost all processing.

- Many zero clients are optimized for only one vendor or connection broker. Some may be reconfigured, but at best this is an inconvenience and at worst it leads to vendor lock-in.

### Popular vendors of zero client

- Digi International Inc.

- Teradici Corporation

- Via Labs

- Dell Wyse

### Learn

Learn more about [zero client](https://v2cloud.com/blog/zero-client).
