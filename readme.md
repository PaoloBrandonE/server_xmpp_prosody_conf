# Servicio XMPP con Prosody

Implementación de un servicio de mensajería y notificación de presencia utilizando el protocolo XMPP y el servidor Prosody.

El proyecto fue desarrollado para el curso de Redes de Computadoras II y contempla la configuración de dos servidores XMPP, clientes conectados a cada servidor, comunicación entre servidores y modificación de los puertos de escucha predeterminados.

## 1. Descripción del proyecto

El proyecto utiliza dos servidores XMPP independientes:

- `empresaa.local`
- `empresab.local`

Cada servidor cuenta con sus propios usuarios y clientes. La comunicación entre ambos servidores se realiza mediante XMPP Server-to-Server (S2S).

La configuración también incluye un servidor DNS local mediante `dnsmasq`, utilizado para resolver los dominios y registros SRV necesarios para XMPP.

Como parte del proyecto se modificaron los puertos predeterminados de XMPP y se verificó que la comunicación continuara funcionando correctamente.

## 2. Tecnologías utilizadas

- Ubuntu Server
- Prosody
- XMPP
- dnsmasq
- systemd-resolved
- Gajim
- TLS
- VirtualBox

## 3. Estructura del repositorio

```text
.
├── configuracion/
│   ├── dns/
│   │   ├── hosts.example
│   │   ├── resolved.conf
│   │   └── xmpp.conf
│   │
│   └── prosody/
│       └── prosody.cfg.lua
│
└── readme.md
