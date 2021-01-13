<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2.1`](#nats21)
-	[`nats:2.1.9`](#nats219)
-	[`nats:2.1.9-alpine`](#nats219-alpine)
-	[`nats:2.1.9-alpine3.12`](#nats219-alpine312)
-	[`nats:2.1.9-linux`](#nats219-linux)
-	[`nats:2.1.9-nanoserver`](#nats219-nanoserver)
-	[`nats:2.1.9-nanoserver-1809`](#nats219-nanoserver-1809)
-	[`nats:2.1.9-scratch`](#nats219-scratch)
-	[`nats:2.1.9-windowsservercore`](#nats219-windowsservercore)
-	[`nats:2.1.9-windowsservercore-1809`](#nats219-windowsservercore-1809)
-	[`nats:2.1.9-windowsservercore-ltsc2016`](#nats219-windowsservercore-ltsc2016)
-	[`nats:2.1-alpine`](#nats21-alpine)
-	[`nats:2.1-alpine3.12`](#nats21-alpine312)
-	[`nats:2.1-linux`](#nats21-linux)
-	[`nats:2.1-nanoserver`](#nats21-nanoserver)
-	[`nats:2.1-nanoserver-1809`](#nats21-nanoserver-1809)
-	[`nats:2.1-scratch`](#nats21-scratch)
-	[`nats:2.1-windowsservercore`](#nats21-windowsservercore)
-	[`nats:2.1-windowsservercore-1809`](#nats21-windowsservercore-1809)
-	[`nats:2.1-windowsservercore-ltsc2016`](#nats21-windowsservercore-ltsc2016)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.12`](#nats2-alpine312)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.12`](#natsalpine312)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)
-	[`nats:windowsservercore-ltsc2016`](#natswindowsservercore-ltsc2016)

## `nats:2`

```console
$ docker pull nats@sha256:5d718b257e66e9e23691968c95ad024b114f3b64ab1cb840372f6e20677209d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1697; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1`

```console
$ docker pull nats@sha256:5d718b257e66e9e23691968c95ad024b114f3b64ab1cb840372f6e20677209d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1697; amd64

### `nats:2.1` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9`

```console
$ docker pull nats@sha256:5d718b257e66e9e23691968c95ad024b114f3b64ab1cb840372f6e20677209d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1697; amd64

### `nats:2.1.9` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-alpine`

```console
$ docker pull nats@sha256:6aeb085e155fdf6e26686f84b6bbda85decabb26618cf9a4a9a6e60fb2ddedd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:01ef6bd09ce6214b4bbbd07cd1ed71cb3c2032af363c339f0947bb201b3b0d4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d318b8714ba1c27c329e451972412e1ea98bdd9770b0ea407bc1a0eed808de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:03:45 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 13:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 13:03:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 13:03:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 13:03:48 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 13:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 13:03:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f83c9bcde6228484d4ec82867e4f643145a2815294606ef039b35e4422818`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 4.4 MB (4378529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57817554b32044006d6fcdc7f8b37b897772a6a1939deafc6300ac9e73e59649`  
		Last Modified: Thu, 17 Dec 2020 13:04:47 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da7ddd1cbb146ba5a8226840ecfcde831b9de6513dec632f31fc5f41435ad89`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:20865b74e541d996ab5962ab6adcb5c4c00d2dcde28825bee84afdd894ea61a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6704345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce89d3d68b51a65ed17a98a1b4bfcfe2723b8b89661d280e42c9c75c1727134`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:49:53 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:49:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:50:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:50:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:50:02 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:50:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:50:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f910ed5a4020ce61e84b226bdc00ddbd58e65520b167d434c069960423beca`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 4.1 MB (4099209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049560eb460c0dcf530612a04ee7de85fb97482bf25e90766016aeffd3b939ec`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a49776a36b6efbf5b89e61b31ce8b52cc9a1891deec971249aca3f8c348cc1`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a811faaeddca710bde4ebd759a8b896a8ad7930efea3d0bbfd03b13162a6264e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39fa4a36386fabdeb39d625aa9ffcdecd52b7dd569ef47f3c54045872d1cc46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:47:28 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 06:47:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 06:47:33 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 06:47:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 06:47:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 06:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:47:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0954bb3d71e3fcb08672d4956c0093467b65345d4d06710437c6e95b0c9846fd`  
		Last Modified: Thu, 17 Dec 2020 06:49:06 GMT  
		Size: 4.1 MB (4094629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72db60e9b3e73600ccfde9cd8cc86dad2f18c818d25ed93803370b30f02bb0d`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d0ce146cd9874b06be341bd5a6e16de55ac10f21f1a53d731064965a51b8f8`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd9a756af2a7cc6ffc0e22a22abe348096271681343c379d9118f93353c0e00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6788811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4d5284f6e232b2d496689a6171fe3ebe65451bb95a86198d7b98f0f4b50689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:35:31 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:35:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:35:36 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:35:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da0fc46766edc6d67bc9fa0297ed044b58ac6149a9966f5b75b50e963413cf4`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 4.1 MB (4078793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0c680e95f0e69b736b925b086864acfd590db86cd90770cd936d1f75f460b7`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf7ca242ef63f98cf4d60c719aa99b7da938719b113735c2781290b1f021a26`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-alpine3.12`

```console
$ docker pull nats@sha256:6aeb085e155fdf6e26686f84b6bbda85decabb26618cf9a4a9a6e60fb2ddedd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1.9-alpine3.12` - linux; amd64

```console
$ docker pull nats@sha256:01ef6bd09ce6214b4bbbd07cd1ed71cb3c2032af363c339f0947bb201b3b0d4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d318b8714ba1c27c329e451972412e1ea98bdd9770b0ea407bc1a0eed808de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:03:45 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 13:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 13:03:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 13:03:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 13:03:48 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 13:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 13:03:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f83c9bcde6228484d4ec82867e4f643145a2815294606ef039b35e4422818`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 4.4 MB (4378529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57817554b32044006d6fcdc7f8b37b897772a6a1939deafc6300ac9e73e59649`  
		Last Modified: Thu, 17 Dec 2020 13:04:47 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da7ddd1cbb146ba5a8226840ecfcde831b9de6513dec632f31fc5f41435ad89`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:20865b74e541d996ab5962ab6adcb5c4c00d2dcde28825bee84afdd894ea61a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6704345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce89d3d68b51a65ed17a98a1b4bfcfe2723b8b89661d280e42c9c75c1727134`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:49:53 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:49:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:50:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:50:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:50:02 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:50:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:50:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f910ed5a4020ce61e84b226bdc00ddbd58e65520b167d434c069960423beca`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 4.1 MB (4099209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049560eb460c0dcf530612a04ee7de85fb97482bf25e90766016aeffd3b939ec`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a49776a36b6efbf5b89e61b31ce8b52cc9a1891deec971249aca3f8c348cc1`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:a811faaeddca710bde4ebd759a8b896a8ad7930efea3d0bbfd03b13162a6264e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39fa4a36386fabdeb39d625aa9ffcdecd52b7dd569ef47f3c54045872d1cc46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:47:28 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 06:47:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 06:47:33 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 06:47:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 06:47:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 06:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:47:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0954bb3d71e3fcb08672d4956c0093467b65345d4d06710437c6e95b0c9846fd`  
		Last Modified: Thu, 17 Dec 2020 06:49:06 GMT  
		Size: 4.1 MB (4094629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72db60e9b3e73600ccfde9cd8cc86dad2f18c818d25ed93803370b30f02bb0d`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d0ce146cd9874b06be341bd5a6e16de55ac10f21f1a53d731064965a51b8f8`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd9a756af2a7cc6ffc0e22a22abe348096271681343c379d9118f93353c0e00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6788811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4d5284f6e232b2d496689a6171fe3ebe65451bb95a86198d7b98f0f4b50689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:35:31 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:35:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:35:36 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:35:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da0fc46766edc6d67bc9fa0297ed044b58ac6149a9966f5b75b50e963413cf4`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 4.1 MB (4078793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0c680e95f0e69b736b925b086864acfd590db86cd90770cd936d1f75f460b7`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf7ca242ef63f98cf4d60c719aa99b7da938719b113735c2781290b1f021a26`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-linux`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-nanoserver`

```console
$ docker pull nats@sha256:21f6fc01450a8b9c0a03f37fe475150800b575d5b0a05ada60f988333b2dc1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:2.1.9-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-nanoserver-1809`

```console
$ docker pull nats@sha256:21f6fc01450a8b9c0a03f37fe475150800b575d5b0a05ada60f988333b2dc1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:2.1.9-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-scratch`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-windowsservercore`

```console
$ docker pull nats@sha256:0065f20e4c3d3353a1923e3b2040b1e8ce0c8dd427ee3d5bded3a63aa095e743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64
	-	windows version 10.0.14393.4169; amd64

### `nats:2.1.9-windowsservercore` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:aada5edd446c33d7f0cdec0fefcb38a8b5590e44d4dc3c96a251e4dc70dc3331
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454148019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031dbf4ba2968a5141c84684c424493436b1c5c06ceada8f998aad51a31a186`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 15:20:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:04:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:04:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:04:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:04:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:04:37 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:05:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:05:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:05:49 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:05:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:05:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f84df50d9e20cf852bfd3555d4e56feabf7b9c735e48c613fc461146876bc03`  
		Last Modified: Wed, 13 Jan 2021 18:31:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff779c93810f460e9728c49a995f9cdd81c09b10ffc6e842f2272d19bf4389c`  
		Last Modified: Wed, 13 Jan 2021 19:10:22 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faaba717596a54bf51953c222df419b525a196529e9d4d0c98e44bf6c7bc4ee`  
		Last Modified: Wed, 13 Jan 2021 19:10:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cb7951519de47a30ef002cff4cb9c60650027cae289b36b71148ac51859b63`  
		Last Modified: Wed, 13 Jan 2021 19:10:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e01bfa5d9722f31f0db2b1d9a8b4c590620491626f2bd622eebef651c8aa8`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62774ffa1eced43b67a7b2e3ad24b3bade3513280a5135aa994e68fd6744ab46`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 5.0 MB (4995396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07cd3dac74e385b2c29cc30fee72c5dba6fe50c4e8693107469d14a3ac38e40`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 13.4 MB (13369683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac73259d45c25f57b84af56ae813f5c1071b64fd365abc139468c74741017c90`  
		Last Modified: Wed, 13 Jan 2021 19:10:14 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e972d90c5bf2368649731e44c25e0b6d0d7615adbeeb4830fdd61d05c703710`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe9f87a1c2bb4a7311943263ac9446984971e7804672e6c71473ec4619d723`  
		Last Modified: Wed, 13 Jan 2021 19:10:15 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c96eb244980fd8b710cd559fc78aba2933f3cd5bb8b7d0d8cdd2a7bc287227`  
		Last Modified: Wed, 13 Jan 2021 19:10:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1.9-windowsservercore` - windows version 10.0.14393.4169; amd64

```console
$ docker pull nats@sha256:a3d15409d2215acd9b8bb21c0fd2c006789f5147c98e91efdf04cdfb3f71ed7d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813747776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532f1992cb14b60a3059cf3651152f113910fc513246a702cae67b06fafdac27`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 15:29:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:06:11 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:06:13 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:07:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:09:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:09:19 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:09:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b5ee02f83739eef6745d432d63363ce5f490820d4b3e39ae83aa4e3771c4073`  
		Last Modified: Wed, 13 Jan 2021 18:32:39 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd1c346230e9eaf41e5c8f582c16f531efe65ddbc7fad4e748dd41227e0bbbb`  
		Last Modified: Wed, 13 Jan 2021 19:11:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a1c3cb2cafeec468c4b189a9bb82928aeff9d8d20c78fac2661ba6eefa7cd0`  
		Last Modified: Wed, 13 Jan 2021 19:11:20 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f7a55bb339a043e41c3e13a2ddc5aacdbe7909f27a5a73334bcd6981ab005`  
		Last Modified: Wed, 13 Jan 2021 19:11:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b36a1e84f430bc8f437c60f1315e5f8fb5ab2d2d2ad0d5da53867887721cc`  
		Last Modified: Wed, 13 Jan 2021 19:11:17 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f343d10dd4537d6d5f04f7f5702c0b2fa5a54f0b76e4cb07165d6b76252af5`  
		Last Modified: Wed, 13 Jan 2021 19:11:26 GMT  
		Size: 5.6 MB (5633704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf954465e03e8a00f8de44752e29cbd77730020de5ec6526fce80d822868918`  
		Last Modified: Wed, 13 Jan 2021 19:11:18 GMT  
		Size: 14.2 MB (14209225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db694fce26f8975588646948bdce55a92c5305cc61489ef76e4b5b2d16930f51`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457fc56aeae1295b29bf9edde0f0aaf9b177e5a279f82ddc05c35f3471ec4b6`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040b08654e387e662885b914e16cca191b89a16cc3577ba5fb24d3a9e903a73`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1933d956bffa8e85f00a1273a28efc2f6e9393ea13015240046d5e30222f64b2`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-windowsservercore-1809`

```console
$ docker pull nats@sha256:ea0be7c6f01582d60f391e779978dd496c114087cac9dff08c979b91ca2777c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:2.1.9-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:aada5edd446c33d7f0cdec0fefcb38a8b5590e44d4dc3c96a251e4dc70dc3331
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454148019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031dbf4ba2968a5141c84684c424493436b1c5c06ceada8f998aad51a31a186`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 15:20:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:04:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:04:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:04:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:04:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:04:37 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:05:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:05:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:05:49 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:05:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:05:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f84df50d9e20cf852bfd3555d4e56feabf7b9c735e48c613fc461146876bc03`  
		Last Modified: Wed, 13 Jan 2021 18:31:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff779c93810f460e9728c49a995f9cdd81c09b10ffc6e842f2272d19bf4389c`  
		Last Modified: Wed, 13 Jan 2021 19:10:22 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faaba717596a54bf51953c222df419b525a196529e9d4d0c98e44bf6c7bc4ee`  
		Last Modified: Wed, 13 Jan 2021 19:10:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cb7951519de47a30ef002cff4cb9c60650027cae289b36b71148ac51859b63`  
		Last Modified: Wed, 13 Jan 2021 19:10:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e01bfa5d9722f31f0db2b1d9a8b4c590620491626f2bd622eebef651c8aa8`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62774ffa1eced43b67a7b2e3ad24b3bade3513280a5135aa994e68fd6744ab46`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 5.0 MB (4995396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07cd3dac74e385b2c29cc30fee72c5dba6fe50c4e8693107469d14a3ac38e40`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 13.4 MB (13369683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac73259d45c25f57b84af56ae813f5c1071b64fd365abc139468c74741017c90`  
		Last Modified: Wed, 13 Jan 2021 19:10:14 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e972d90c5bf2368649731e44c25e0b6d0d7615adbeeb4830fdd61d05c703710`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe9f87a1c2bb4a7311943263ac9446984971e7804672e6c71473ec4619d723`  
		Last Modified: Wed, 13 Jan 2021 19:10:15 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c96eb244980fd8b710cd559fc78aba2933f3cd5bb8b7d0d8cdd2a7bc287227`  
		Last Modified: Wed, 13 Jan 2021 19:10:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.9-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b2473c0f9192eddd51042f9ecb680e61e087793aaf726ef09d8459a48447461a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `nats:2.1.9-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull nats@sha256:a3d15409d2215acd9b8bb21c0fd2c006789f5147c98e91efdf04cdfb3f71ed7d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813747776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532f1992cb14b60a3059cf3651152f113910fc513246a702cae67b06fafdac27`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 15:29:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:06:11 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:06:13 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:07:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:09:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:09:19 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:09:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b5ee02f83739eef6745d432d63363ce5f490820d4b3e39ae83aa4e3771c4073`  
		Last Modified: Wed, 13 Jan 2021 18:32:39 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd1c346230e9eaf41e5c8f582c16f531efe65ddbc7fad4e748dd41227e0bbbb`  
		Last Modified: Wed, 13 Jan 2021 19:11:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a1c3cb2cafeec468c4b189a9bb82928aeff9d8d20c78fac2661ba6eefa7cd0`  
		Last Modified: Wed, 13 Jan 2021 19:11:20 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f7a55bb339a043e41c3e13a2ddc5aacdbe7909f27a5a73334bcd6981ab005`  
		Last Modified: Wed, 13 Jan 2021 19:11:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b36a1e84f430bc8f437c60f1315e5f8fb5ab2d2d2ad0d5da53867887721cc`  
		Last Modified: Wed, 13 Jan 2021 19:11:17 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f343d10dd4537d6d5f04f7f5702c0b2fa5a54f0b76e4cb07165d6b76252af5`  
		Last Modified: Wed, 13 Jan 2021 19:11:26 GMT  
		Size: 5.6 MB (5633704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf954465e03e8a00f8de44752e29cbd77730020de5ec6526fce80d822868918`  
		Last Modified: Wed, 13 Jan 2021 19:11:18 GMT  
		Size: 14.2 MB (14209225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db694fce26f8975588646948bdce55a92c5305cc61489ef76e4b5b2d16930f51`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457fc56aeae1295b29bf9edde0f0aaf9b177e5a279f82ddc05c35f3471ec4b6`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040b08654e387e662885b914e16cca191b89a16cc3577ba5fb24d3a9e903a73`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1933d956bffa8e85f00a1273a28efc2f6e9393ea13015240046d5e30222f64b2`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine`

```console
$ docker pull nats@sha256:6aeb085e155fdf6e26686f84b6bbda85decabb26618cf9a4a9a6e60fb2ddedd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:01ef6bd09ce6214b4bbbd07cd1ed71cb3c2032af363c339f0947bb201b3b0d4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d318b8714ba1c27c329e451972412e1ea98bdd9770b0ea407bc1a0eed808de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:03:45 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 13:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 13:03:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 13:03:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 13:03:48 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 13:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 13:03:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f83c9bcde6228484d4ec82867e4f643145a2815294606ef039b35e4422818`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 4.4 MB (4378529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57817554b32044006d6fcdc7f8b37b897772a6a1939deafc6300ac9e73e59649`  
		Last Modified: Thu, 17 Dec 2020 13:04:47 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da7ddd1cbb146ba5a8226840ecfcde831b9de6513dec632f31fc5f41435ad89`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:20865b74e541d996ab5962ab6adcb5c4c00d2dcde28825bee84afdd894ea61a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6704345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce89d3d68b51a65ed17a98a1b4bfcfe2723b8b89661d280e42c9c75c1727134`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:49:53 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:49:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:50:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:50:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:50:02 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:50:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:50:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f910ed5a4020ce61e84b226bdc00ddbd58e65520b167d434c069960423beca`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 4.1 MB (4099209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049560eb460c0dcf530612a04ee7de85fb97482bf25e90766016aeffd3b939ec`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a49776a36b6efbf5b89e61b31ce8b52cc9a1891deec971249aca3f8c348cc1`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a811faaeddca710bde4ebd759a8b896a8ad7930efea3d0bbfd03b13162a6264e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39fa4a36386fabdeb39d625aa9ffcdecd52b7dd569ef47f3c54045872d1cc46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:47:28 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 06:47:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 06:47:33 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 06:47:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 06:47:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 06:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:47:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0954bb3d71e3fcb08672d4956c0093467b65345d4d06710437c6e95b0c9846fd`  
		Last Modified: Thu, 17 Dec 2020 06:49:06 GMT  
		Size: 4.1 MB (4094629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72db60e9b3e73600ccfde9cd8cc86dad2f18c818d25ed93803370b30f02bb0d`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d0ce146cd9874b06be341bd5a6e16de55ac10f21f1a53d731064965a51b8f8`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd9a756af2a7cc6ffc0e22a22abe348096271681343c379d9118f93353c0e00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6788811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4d5284f6e232b2d496689a6171fe3ebe65451bb95a86198d7b98f0f4b50689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:35:31 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:35:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:35:36 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:35:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da0fc46766edc6d67bc9fa0297ed044b58ac6149a9966f5b75b50e963413cf4`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 4.1 MB (4078793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0c680e95f0e69b736b925b086864acfd590db86cd90770cd936d1f75f460b7`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf7ca242ef63f98cf4d60c719aa99b7da938719b113735c2781290b1f021a26`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine3.12`

```console
$ docker pull nats@sha256:6aeb085e155fdf6e26686f84b6bbda85decabb26618cf9a4a9a6e60fb2ddedd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-alpine3.12` - linux; amd64

```console
$ docker pull nats@sha256:01ef6bd09ce6214b4bbbd07cd1ed71cb3c2032af363c339f0947bb201b3b0d4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d318b8714ba1c27c329e451972412e1ea98bdd9770b0ea407bc1a0eed808de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:03:45 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 13:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 13:03:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 13:03:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 13:03:48 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 13:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 13:03:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f83c9bcde6228484d4ec82867e4f643145a2815294606ef039b35e4422818`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 4.4 MB (4378529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57817554b32044006d6fcdc7f8b37b897772a6a1939deafc6300ac9e73e59649`  
		Last Modified: Thu, 17 Dec 2020 13:04:47 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da7ddd1cbb146ba5a8226840ecfcde831b9de6513dec632f31fc5f41435ad89`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:20865b74e541d996ab5962ab6adcb5c4c00d2dcde28825bee84afdd894ea61a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6704345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce89d3d68b51a65ed17a98a1b4bfcfe2723b8b89661d280e42c9c75c1727134`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:49:53 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:49:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:50:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:50:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:50:02 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:50:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:50:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f910ed5a4020ce61e84b226bdc00ddbd58e65520b167d434c069960423beca`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 4.1 MB (4099209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049560eb460c0dcf530612a04ee7de85fb97482bf25e90766016aeffd3b939ec`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a49776a36b6efbf5b89e61b31ce8b52cc9a1891deec971249aca3f8c348cc1`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:a811faaeddca710bde4ebd759a8b896a8ad7930efea3d0bbfd03b13162a6264e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39fa4a36386fabdeb39d625aa9ffcdecd52b7dd569ef47f3c54045872d1cc46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:47:28 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 06:47:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 06:47:33 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 06:47:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 06:47:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 06:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:47:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0954bb3d71e3fcb08672d4956c0093467b65345d4d06710437c6e95b0c9846fd`  
		Last Modified: Thu, 17 Dec 2020 06:49:06 GMT  
		Size: 4.1 MB (4094629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72db60e9b3e73600ccfde9cd8cc86dad2f18c818d25ed93803370b30f02bb0d`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d0ce146cd9874b06be341bd5a6e16de55ac10f21f1a53d731064965a51b8f8`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd9a756af2a7cc6ffc0e22a22abe348096271681343c379d9118f93353c0e00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6788811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4d5284f6e232b2d496689a6171fe3ebe65451bb95a86198d7b98f0f4b50689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:35:31 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:35:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:35:36 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:35:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da0fc46766edc6d67bc9fa0297ed044b58ac6149a9966f5b75b50e963413cf4`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 4.1 MB (4078793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0c680e95f0e69b736b925b086864acfd590db86cd90770cd936d1f75f460b7`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf7ca242ef63f98cf4d60c719aa99b7da938719b113735c2781290b1f021a26`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-linux`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver`

```console
$ docker pull nats@sha256:21f6fc01450a8b9c0a03f37fe475150800b575d5b0a05ada60f988333b2dc1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:2.1-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver-1809`

```console
$ docker pull nats@sha256:21f6fc01450a8b9c0a03f37fe475150800b575d5b0a05ada60f988333b2dc1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:2.1-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-scratch`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore`

```console
$ docker pull nats@sha256:0065f20e4c3d3353a1923e3b2040b1e8ce0c8dd427ee3d5bded3a63aa095e743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64
	-	windows version 10.0.14393.4169; amd64

### `nats:2.1-windowsservercore` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:aada5edd446c33d7f0cdec0fefcb38a8b5590e44d4dc3c96a251e4dc70dc3331
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454148019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031dbf4ba2968a5141c84684c424493436b1c5c06ceada8f998aad51a31a186`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 15:20:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:04:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:04:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:04:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:04:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:04:37 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:05:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:05:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:05:49 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:05:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:05:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f84df50d9e20cf852bfd3555d4e56feabf7b9c735e48c613fc461146876bc03`  
		Last Modified: Wed, 13 Jan 2021 18:31:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff779c93810f460e9728c49a995f9cdd81c09b10ffc6e842f2272d19bf4389c`  
		Last Modified: Wed, 13 Jan 2021 19:10:22 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faaba717596a54bf51953c222df419b525a196529e9d4d0c98e44bf6c7bc4ee`  
		Last Modified: Wed, 13 Jan 2021 19:10:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cb7951519de47a30ef002cff4cb9c60650027cae289b36b71148ac51859b63`  
		Last Modified: Wed, 13 Jan 2021 19:10:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e01bfa5d9722f31f0db2b1d9a8b4c590620491626f2bd622eebef651c8aa8`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62774ffa1eced43b67a7b2e3ad24b3bade3513280a5135aa994e68fd6744ab46`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 5.0 MB (4995396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07cd3dac74e385b2c29cc30fee72c5dba6fe50c4e8693107469d14a3ac38e40`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 13.4 MB (13369683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac73259d45c25f57b84af56ae813f5c1071b64fd365abc139468c74741017c90`  
		Last Modified: Wed, 13 Jan 2021 19:10:14 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e972d90c5bf2368649731e44c25e0b6d0d7615adbeeb4830fdd61d05c703710`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe9f87a1c2bb4a7311943263ac9446984971e7804672e6c71473ec4619d723`  
		Last Modified: Wed, 13 Jan 2021 19:10:15 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c96eb244980fd8b710cd559fc78aba2933f3cd5bb8b7d0d8cdd2a7bc287227`  
		Last Modified: Wed, 13 Jan 2021 19:10:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-windowsservercore` - windows version 10.0.14393.4169; amd64

```console
$ docker pull nats@sha256:a3d15409d2215acd9b8bb21c0fd2c006789f5147c98e91efdf04cdfb3f71ed7d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813747776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532f1992cb14b60a3059cf3651152f113910fc513246a702cae67b06fafdac27`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 15:29:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:06:11 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:06:13 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:07:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:09:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:09:19 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:09:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b5ee02f83739eef6745d432d63363ce5f490820d4b3e39ae83aa4e3771c4073`  
		Last Modified: Wed, 13 Jan 2021 18:32:39 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd1c346230e9eaf41e5c8f582c16f531efe65ddbc7fad4e748dd41227e0bbbb`  
		Last Modified: Wed, 13 Jan 2021 19:11:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a1c3cb2cafeec468c4b189a9bb82928aeff9d8d20c78fac2661ba6eefa7cd0`  
		Last Modified: Wed, 13 Jan 2021 19:11:20 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f7a55bb339a043e41c3e13a2ddc5aacdbe7909f27a5a73334bcd6981ab005`  
		Last Modified: Wed, 13 Jan 2021 19:11:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b36a1e84f430bc8f437c60f1315e5f8fb5ab2d2d2ad0d5da53867887721cc`  
		Last Modified: Wed, 13 Jan 2021 19:11:17 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f343d10dd4537d6d5f04f7f5702c0b2fa5a54f0b76e4cb07165d6b76252af5`  
		Last Modified: Wed, 13 Jan 2021 19:11:26 GMT  
		Size: 5.6 MB (5633704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf954465e03e8a00f8de44752e29cbd77730020de5ec6526fce80d822868918`  
		Last Modified: Wed, 13 Jan 2021 19:11:18 GMT  
		Size: 14.2 MB (14209225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db694fce26f8975588646948bdce55a92c5305cc61489ef76e4b5b2d16930f51`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457fc56aeae1295b29bf9edde0f0aaf9b177e5a279f82ddc05c35f3471ec4b6`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040b08654e387e662885b914e16cca191b89a16cc3577ba5fb24d3a9e903a73`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1933d956bffa8e85f00a1273a28efc2f6e9393ea13015240046d5e30222f64b2`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:ea0be7c6f01582d60f391e779978dd496c114087cac9dff08c979b91ca2777c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:2.1-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:aada5edd446c33d7f0cdec0fefcb38a8b5590e44d4dc3c96a251e4dc70dc3331
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454148019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031dbf4ba2968a5141c84684c424493436b1c5c06ceada8f998aad51a31a186`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 15:20:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:04:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:04:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:04:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:04:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:04:37 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:05:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:05:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:05:49 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:05:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:05:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f84df50d9e20cf852bfd3555d4e56feabf7b9c735e48c613fc461146876bc03`  
		Last Modified: Wed, 13 Jan 2021 18:31:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff779c93810f460e9728c49a995f9cdd81c09b10ffc6e842f2272d19bf4389c`  
		Last Modified: Wed, 13 Jan 2021 19:10:22 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faaba717596a54bf51953c222df419b525a196529e9d4d0c98e44bf6c7bc4ee`  
		Last Modified: Wed, 13 Jan 2021 19:10:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cb7951519de47a30ef002cff4cb9c60650027cae289b36b71148ac51859b63`  
		Last Modified: Wed, 13 Jan 2021 19:10:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e01bfa5d9722f31f0db2b1d9a8b4c590620491626f2bd622eebef651c8aa8`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62774ffa1eced43b67a7b2e3ad24b3bade3513280a5135aa994e68fd6744ab46`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 5.0 MB (4995396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07cd3dac74e385b2c29cc30fee72c5dba6fe50c4e8693107469d14a3ac38e40`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 13.4 MB (13369683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac73259d45c25f57b84af56ae813f5c1071b64fd365abc139468c74741017c90`  
		Last Modified: Wed, 13 Jan 2021 19:10:14 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e972d90c5bf2368649731e44c25e0b6d0d7615adbeeb4830fdd61d05c703710`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe9f87a1c2bb4a7311943263ac9446984971e7804672e6c71473ec4619d723`  
		Last Modified: Wed, 13 Jan 2021 19:10:15 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c96eb244980fd8b710cd559fc78aba2933f3cd5bb8b7d0d8cdd2a7bc287227`  
		Last Modified: Wed, 13 Jan 2021 19:10:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b2473c0f9192eddd51042f9ecb680e61e087793aaf726ef09d8459a48447461a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `nats:2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull nats@sha256:a3d15409d2215acd9b8bb21c0fd2c006789f5147c98e91efdf04cdfb3f71ed7d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813747776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532f1992cb14b60a3059cf3651152f113910fc513246a702cae67b06fafdac27`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 15:29:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:06:11 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:06:13 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:07:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:09:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:09:19 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:09:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b5ee02f83739eef6745d432d63363ce5f490820d4b3e39ae83aa4e3771c4073`  
		Last Modified: Wed, 13 Jan 2021 18:32:39 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd1c346230e9eaf41e5c8f582c16f531efe65ddbc7fad4e748dd41227e0bbbb`  
		Last Modified: Wed, 13 Jan 2021 19:11:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a1c3cb2cafeec468c4b189a9bb82928aeff9d8d20c78fac2661ba6eefa7cd0`  
		Last Modified: Wed, 13 Jan 2021 19:11:20 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f7a55bb339a043e41c3e13a2ddc5aacdbe7909f27a5a73334bcd6981ab005`  
		Last Modified: Wed, 13 Jan 2021 19:11:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b36a1e84f430bc8f437c60f1315e5f8fb5ab2d2d2ad0d5da53867887721cc`  
		Last Modified: Wed, 13 Jan 2021 19:11:17 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f343d10dd4537d6d5f04f7f5702c0b2fa5a54f0b76e4cb07165d6b76252af5`  
		Last Modified: Wed, 13 Jan 2021 19:11:26 GMT  
		Size: 5.6 MB (5633704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf954465e03e8a00f8de44752e29cbd77730020de5ec6526fce80d822868918`  
		Last Modified: Wed, 13 Jan 2021 19:11:18 GMT  
		Size: 14.2 MB (14209225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db694fce26f8975588646948bdce55a92c5305cc61489ef76e4b5b2d16930f51`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457fc56aeae1295b29bf9edde0f0aaf9b177e5a279f82ddc05c35f3471ec4b6`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040b08654e387e662885b914e16cca191b89a16cc3577ba5fb24d3a9e903a73`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1933d956bffa8e85f00a1273a28efc2f6e9393ea13015240046d5e30222f64b2`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:6aeb085e155fdf6e26686f84b6bbda85decabb26618cf9a4a9a6e60fb2ddedd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:01ef6bd09ce6214b4bbbd07cd1ed71cb3c2032af363c339f0947bb201b3b0d4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d318b8714ba1c27c329e451972412e1ea98bdd9770b0ea407bc1a0eed808de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:03:45 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 13:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 13:03:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 13:03:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 13:03:48 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 13:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 13:03:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f83c9bcde6228484d4ec82867e4f643145a2815294606ef039b35e4422818`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 4.4 MB (4378529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57817554b32044006d6fcdc7f8b37b897772a6a1939deafc6300ac9e73e59649`  
		Last Modified: Thu, 17 Dec 2020 13:04:47 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da7ddd1cbb146ba5a8226840ecfcde831b9de6513dec632f31fc5f41435ad89`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:20865b74e541d996ab5962ab6adcb5c4c00d2dcde28825bee84afdd894ea61a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6704345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce89d3d68b51a65ed17a98a1b4bfcfe2723b8b89661d280e42c9c75c1727134`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:49:53 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:49:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:50:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:50:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:50:02 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:50:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:50:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f910ed5a4020ce61e84b226bdc00ddbd58e65520b167d434c069960423beca`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 4.1 MB (4099209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049560eb460c0dcf530612a04ee7de85fb97482bf25e90766016aeffd3b939ec`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a49776a36b6efbf5b89e61b31ce8b52cc9a1891deec971249aca3f8c348cc1`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a811faaeddca710bde4ebd759a8b896a8ad7930efea3d0bbfd03b13162a6264e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39fa4a36386fabdeb39d625aa9ffcdecd52b7dd569ef47f3c54045872d1cc46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:47:28 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 06:47:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 06:47:33 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 06:47:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 06:47:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 06:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:47:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0954bb3d71e3fcb08672d4956c0093467b65345d4d06710437c6e95b0c9846fd`  
		Last Modified: Thu, 17 Dec 2020 06:49:06 GMT  
		Size: 4.1 MB (4094629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72db60e9b3e73600ccfde9cd8cc86dad2f18c818d25ed93803370b30f02bb0d`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d0ce146cd9874b06be341bd5a6e16de55ac10f21f1a53d731064965a51b8f8`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd9a756af2a7cc6ffc0e22a22abe348096271681343c379d9118f93353c0e00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6788811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4d5284f6e232b2d496689a6171fe3ebe65451bb95a86198d7b98f0f4b50689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:35:31 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:35:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:35:36 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:35:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da0fc46766edc6d67bc9fa0297ed044b58ac6149a9966f5b75b50e963413cf4`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 4.1 MB (4078793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0c680e95f0e69b736b925b086864acfd590db86cd90770cd936d1f75f460b7`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf7ca242ef63f98cf4d60c719aa99b7da938719b113735c2781290b1f021a26`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.12`

```console
$ docker pull nats@sha256:6aeb085e155fdf6e26686f84b6bbda85decabb26618cf9a4a9a6e60fb2ddedd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.12` - linux; amd64

```console
$ docker pull nats@sha256:01ef6bd09ce6214b4bbbd07cd1ed71cb3c2032af363c339f0947bb201b3b0d4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d318b8714ba1c27c329e451972412e1ea98bdd9770b0ea407bc1a0eed808de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:03:45 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 13:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 13:03:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 13:03:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 13:03:48 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 13:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 13:03:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f83c9bcde6228484d4ec82867e4f643145a2815294606ef039b35e4422818`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 4.4 MB (4378529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57817554b32044006d6fcdc7f8b37b897772a6a1939deafc6300ac9e73e59649`  
		Last Modified: Thu, 17 Dec 2020 13:04:47 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da7ddd1cbb146ba5a8226840ecfcde831b9de6513dec632f31fc5f41435ad89`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:20865b74e541d996ab5962ab6adcb5c4c00d2dcde28825bee84afdd894ea61a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6704345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce89d3d68b51a65ed17a98a1b4bfcfe2723b8b89661d280e42c9c75c1727134`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:49:53 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:49:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:50:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:50:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:50:02 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:50:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:50:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f910ed5a4020ce61e84b226bdc00ddbd58e65520b167d434c069960423beca`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 4.1 MB (4099209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049560eb460c0dcf530612a04ee7de85fb97482bf25e90766016aeffd3b939ec`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a49776a36b6efbf5b89e61b31ce8b52cc9a1891deec971249aca3f8c348cc1`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:a811faaeddca710bde4ebd759a8b896a8ad7930efea3d0bbfd03b13162a6264e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39fa4a36386fabdeb39d625aa9ffcdecd52b7dd569ef47f3c54045872d1cc46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:47:28 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 06:47:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 06:47:33 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 06:47:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 06:47:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 06:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:47:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0954bb3d71e3fcb08672d4956c0093467b65345d4d06710437c6e95b0c9846fd`  
		Last Modified: Thu, 17 Dec 2020 06:49:06 GMT  
		Size: 4.1 MB (4094629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72db60e9b3e73600ccfde9cd8cc86dad2f18c818d25ed93803370b30f02bb0d`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d0ce146cd9874b06be341bd5a6e16de55ac10f21f1a53d731064965a51b8f8`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd9a756af2a7cc6ffc0e22a22abe348096271681343c379d9118f93353c0e00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6788811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4d5284f6e232b2d496689a6171fe3ebe65451bb95a86198d7b98f0f4b50689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:35:31 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:35:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:35:36 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:35:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da0fc46766edc6d67bc9fa0297ed044b58ac6149a9966f5b75b50e963413cf4`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 4.1 MB (4078793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0c680e95f0e69b736b925b086864acfd590db86cd90770cd936d1f75f460b7`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf7ca242ef63f98cf4d60c719aa99b7da938719b113735c2781290b1f021a26`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:21f6fc01450a8b9c0a03f37fe475150800b575d5b0a05ada60f988333b2dc1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:21f6fc01450a8b9c0a03f37fe475150800b575d5b0a05ada60f988333b2dc1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:0065f20e4c3d3353a1923e3b2040b1e8ce0c8dd427ee3d5bded3a63aa095e743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64
	-	windows version 10.0.14393.4169; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:aada5edd446c33d7f0cdec0fefcb38a8b5590e44d4dc3c96a251e4dc70dc3331
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454148019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031dbf4ba2968a5141c84684c424493436b1c5c06ceada8f998aad51a31a186`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 15:20:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:04:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:04:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:04:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:04:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:04:37 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:05:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:05:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:05:49 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:05:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:05:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f84df50d9e20cf852bfd3555d4e56feabf7b9c735e48c613fc461146876bc03`  
		Last Modified: Wed, 13 Jan 2021 18:31:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff779c93810f460e9728c49a995f9cdd81c09b10ffc6e842f2272d19bf4389c`  
		Last Modified: Wed, 13 Jan 2021 19:10:22 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faaba717596a54bf51953c222df419b525a196529e9d4d0c98e44bf6c7bc4ee`  
		Last Modified: Wed, 13 Jan 2021 19:10:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cb7951519de47a30ef002cff4cb9c60650027cae289b36b71148ac51859b63`  
		Last Modified: Wed, 13 Jan 2021 19:10:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e01bfa5d9722f31f0db2b1d9a8b4c590620491626f2bd622eebef651c8aa8`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62774ffa1eced43b67a7b2e3ad24b3bade3513280a5135aa994e68fd6744ab46`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 5.0 MB (4995396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07cd3dac74e385b2c29cc30fee72c5dba6fe50c4e8693107469d14a3ac38e40`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 13.4 MB (13369683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac73259d45c25f57b84af56ae813f5c1071b64fd365abc139468c74741017c90`  
		Last Modified: Wed, 13 Jan 2021 19:10:14 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e972d90c5bf2368649731e44c25e0b6d0d7615adbeeb4830fdd61d05c703710`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe9f87a1c2bb4a7311943263ac9446984971e7804672e6c71473ec4619d723`  
		Last Modified: Wed, 13 Jan 2021 19:10:15 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c96eb244980fd8b710cd559fc78aba2933f3cd5bb8b7d0d8cdd2a7bc287227`  
		Last Modified: Wed, 13 Jan 2021 19:10:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4169; amd64

```console
$ docker pull nats@sha256:a3d15409d2215acd9b8bb21c0fd2c006789f5147c98e91efdf04cdfb3f71ed7d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813747776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532f1992cb14b60a3059cf3651152f113910fc513246a702cae67b06fafdac27`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 15:29:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:06:11 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:06:13 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:07:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:09:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:09:19 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:09:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b5ee02f83739eef6745d432d63363ce5f490820d4b3e39ae83aa4e3771c4073`  
		Last Modified: Wed, 13 Jan 2021 18:32:39 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd1c346230e9eaf41e5c8f582c16f531efe65ddbc7fad4e748dd41227e0bbbb`  
		Last Modified: Wed, 13 Jan 2021 19:11:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a1c3cb2cafeec468c4b189a9bb82928aeff9d8d20c78fac2661ba6eefa7cd0`  
		Last Modified: Wed, 13 Jan 2021 19:11:20 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f7a55bb339a043e41c3e13a2ddc5aacdbe7909f27a5a73334bcd6981ab005`  
		Last Modified: Wed, 13 Jan 2021 19:11:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b36a1e84f430bc8f437c60f1315e5f8fb5ab2d2d2ad0d5da53867887721cc`  
		Last Modified: Wed, 13 Jan 2021 19:11:17 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f343d10dd4537d6d5f04f7f5702c0b2fa5a54f0b76e4cb07165d6b76252af5`  
		Last Modified: Wed, 13 Jan 2021 19:11:26 GMT  
		Size: 5.6 MB (5633704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf954465e03e8a00f8de44752e29cbd77730020de5ec6526fce80d822868918`  
		Last Modified: Wed, 13 Jan 2021 19:11:18 GMT  
		Size: 14.2 MB (14209225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db694fce26f8975588646948bdce55a92c5305cc61489ef76e4b5b2d16930f51`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457fc56aeae1295b29bf9edde0f0aaf9b177e5a279f82ddc05c35f3471ec4b6`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040b08654e387e662885b914e16cca191b89a16cc3577ba5fb24d3a9e903a73`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1933d956bffa8e85f00a1273a28efc2f6e9393ea13015240046d5e30222f64b2`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:ea0be7c6f01582d60f391e779978dd496c114087cac9dff08c979b91ca2777c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:aada5edd446c33d7f0cdec0fefcb38a8b5590e44d4dc3c96a251e4dc70dc3331
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454148019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031dbf4ba2968a5141c84684c424493436b1c5c06ceada8f998aad51a31a186`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 15:20:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:04:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:04:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:04:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:04:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:04:37 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:05:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:05:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:05:49 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:05:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:05:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f84df50d9e20cf852bfd3555d4e56feabf7b9c735e48c613fc461146876bc03`  
		Last Modified: Wed, 13 Jan 2021 18:31:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff779c93810f460e9728c49a995f9cdd81c09b10ffc6e842f2272d19bf4389c`  
		Last Modified: Wed, 13 Jan 2021 19:10:22 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faaba717596a54bf51953c222df419b525a196529e9d4d0c98e44bf6c7bc4ee`  
		Last Modified: Wed, 13 Jan 2021 19:10:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cb7951519de47a30ef002cff4cb9c60650027cae289b36b71148ac51859b63`  
		Last Modified: Wed, 13 Jan 2021 19:10:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e01bfa5d9722f31f0db2b1d9a8b4c590620491626f2bd622eebef651c8aa8`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62774ffa1eced43b67a7b2e3ad24b3bade3513280a5135aa994e68fd6744ab46`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 5.0 MB (4995396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07cd3dac74e385b2c29cc30fee72c5dba6fe50c4e8693107469d14a3ac38e40`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 13.4 MB (13369683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac73259d45c25f57b84af56ae813f5c1071b64fd365abc139468c74741017c90`  
		Last Modified: Wed, 13 Jan 2021 19:10:14 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e972d90c5bf2368649731e44c25e0b6d0d7615adbeeb4830fdd61d05c703710`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe9f87a1c2bb4a7311943263ac9446984971e7804672e6c71473ec4619d723`  
		Last Modified: Wed, 13 Jan 2021 19:10:15 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c96eb244980fd8b710cd559fc78aba2933f3cd5bb8b7d0d8cdd2a7bc287227`  
		Last Modified: Wed, 13 Jan 2021 19:10:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b2473c0f9192eddd51042f9ecb680e61e087793aaf726ef09d8459a48447461a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull nats@sha256:a3d15409d2215acd9b8bb21c0fd2c006789f5147c98e91efdf04cdfb3f71ed7d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813747776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532f1992cb14b60a3059cf3651152f113910fc513246a702cae67b06fafdac27`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 15:29:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:06:11 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:06:13 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:07:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:09:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:09:19 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:09:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b5ee02f83739eef6745d432d63363ce5f490820d4b3e39ae83aa4e3771c4073`  
		Last Modified: Wed, 13 Jan 2021 18:32:39 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd1c346230e9eaf41e5c8f582c16f531efe65ddbc7fad4e748dd41227e0bbbb`  
		Last Modified: Wed, 13 Jan 2021 19:11:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a1c3cb2cafeec468c4b189a9bb82928aeff9d8d20c78fac2661ba6eefa7cd0`  
		Last Modified: Wed, 13 Jan 2021 19:11:20 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f7a55bb339a043e41c3e13a2ddc5aacdbe7909f27a5a73334bcd6981ab005`  
		Last Modified: Wed, 13 Jan 2021 19:11:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b36a1e84f430bc8f437c60f1315e5f8fb5ab2d2d2ad0d5da53867887721cc`  
		Last Modified: Wed, 13 Jan 2021 19:11:17 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f343d10dd4537d6d5f04f7f5702c0b2fa5a54f0b76e4cb07165d6b76252af5`  
		Last Modified: Wed, 13 Jan 2021 19:11:26 GMT  
		Size: 5.6 MB (5633704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf954465e03e8a00f8de44752e29cbd77730020de5ec6526fce80d822868918`  
		Last Modified: Wed, 13 Jan 2021 19:11:18 GMT  
		Size: 14.2 MB (14209225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db694fce26f8975588646948bdce55a92c5305cc61489ef76e4b5b2d16930f51`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457fc56aeae1295b29bf9edde0f0aaf9b177e5a279f82ddc05c35f3471ec4b6`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040b08654e387e662885b914e16cca191b89a16cc3577ba5fb24d3a9e903a73`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1933d956bffa8e85f00a1273a28efc2f6e9393ea13015240046d5e30222f64b2`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:6aeb085e155fdf6e26686f84b6bbda85decabb26618cf9a4a9a6e60fb2ddedd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:01ef6bd09ce6214b4bbbd07cd1ed71cb3c2032af363c339f0947bb201b3b0d4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d318b8714ba1c27c329e451972412e1ea98bdd9770b0ea407bc1a0eed808de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:03:45 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 13:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 13:03:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 13:03:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 13:03:48 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 13:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 13:03:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f83c9bcde6228484d4ec82867e4f643145a2815294606ef039b35e4422818`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 4.4 MB (4378529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57817554b32044006d6fcdc7f8b37b897772a6a1939deafc6300ac9e73e59649`  
		Last Modified: Thu, 17 Dec 2020 13:04:47 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da7ddd1cbb146ba5a8226840ecfcde831b9de6513dec632f31fc5f41435ad89`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:20865b74e541d996ab5962ab6adcb5c4c00d2dcde28825bee84afdd894ea61a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6704345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce89d3d68b51a65ed17a98a1b4bfcfe2723b8b89661d280e42c9c75c1727134`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:49:53 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:49:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:50:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:50:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:50:02 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:50:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:50:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f910ed5a4020ce61e84b226bdc00ddbd58e65520b167d434c069960423beca`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 4.1 MB (4099209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049560eb460c0dcf530612a04ee7de85fb97482bf25e90766016aeffd3b939ec`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a49776a36b6efbf5b89e61b31ce8b52cc9a1891deec971249aca3f8c348cc1`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a811faaeddca710bde4ebd759a8b896a8ad7930efea3d0bbfd03b13162a6264e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39fa4a36386fabdeb39d625aa9ffcdecd52b7dd569ef47f3c54045872d1cc46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:47:28 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 06:47:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 06:47:33 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 06:47:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 06:47:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 06:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:47:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0954bb3d71e3fcb08672d4956c0093467b65345d4d06710437c6e95b0c9846fd`  
		Last Modified: Thu, 17 Dec 2020 06:49:06 GMT  
		Size: 4.1 MB (4094629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72db60e9b3e73600ccfde9cd8cc86dad2f18c818d25ed93803370b30f02bb0d`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d0ce146cd9874b06be341bd5a6e16de55ac10f21f1a53d731064965a51b8f8`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd9a756af2a7cc6ffc0e22a22abe348096271681343c379d9118f93353c0e00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6788811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4d5284f6e232b2d496689a6171fe3ebe65451bb95a86198d7b98f0f4b50689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:35:31 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:35:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:35:36 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:35:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da0fc46766edc6d67bc9fa0297ed044b58ac6149a9966f5b75b50e963413cf4`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 4.1 MB (4078793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0c680e95f0e69b736b925b086864acfd590db86cd90770cd936d1f75f460b7`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf7ca242ef63f98cf4d60c719aa99b7da938719b113735c2781290b1f021a26`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.12`

```console
$ docker pull nats@sha256:6aeb085e155fdf6e26686f84b6bbda85decabb26618cf9a4a9a6e60fb2ddedd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.12` - linux; amd64

```console
$ docker pull nats@sha256:01ef6bd09ce6214b4bbbd07cd1ed71cb3c2032af363c339f0947bb201b3b0d4a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d318b8714ba1c27c329e451972412e1ea98bdd9770b0ea407bc1a0eed808de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:03:45 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 13:03:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 13:03:47 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 13:03:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 13:03:48 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 13:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 13:03:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f83c9bcde6228484d4ec82867e4f643145a2815294606ef039b35e4422818`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 4.4 MB (4378529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57817554b32044006d6fcdc7f8b37b897772a6a1939deafc6300ac9e73e59649`  
		Last Modified: Thu, 17 Dec 2020 13:04:47 GMT  
		Size: 530.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da7ddd1cbb146ba5a8226840ecfcde831b9de6513dec632f31fc5f41435ad89`  
		Last Modified: Thu, 17 Dec 2020 13:04:49 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:20865b74e541d996ab5962ab6adcb5c4c00d2dcde28825bee84afdd894ea61a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6704345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce89d3d68b51a65ed17a98a1b4bfcfe2723b8b89661d280e42c9c75c1727134`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:49:53 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:49:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:50:00 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:50:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:50:02 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:50:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:50:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f910ed5a4020ce61e84b226bdc00ddbd58e65520b167d434c069960423beca`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 4.1 MB (4099209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049560eb460c0dcf530612a04ee7de85fb97482bf25e90766016aeffd3b939ec`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a49776a36b6efbf5b89e61b31ce8b52cc9a1891deec971249aca3f8c348cc1`  
		Last Modified: Thu, 17 Dec 2020 01:50:43 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:a811faaeddca710bde4ebd759a8b896a8ad7930efea3d0bbfd03b13162a6264e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6503157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39fa4a36386fabdeb39d625aa9ffcdecd52b7dd569ef47f3c54045872d1cc46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:47:28 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 06:47:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 06:47:33 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 06:47:34 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 06:47:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 06:47:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 06:47:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0954bb3d71e3fcb08672d4956c0093467b65345d4d06710437c6e95b0c9846fd`  
		Last Modified: Thu, 17 Dec 2020 06:49:06 GMT  
		Size: 4.1 MB (4094629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72db60e9b3e73600ccfde9cd8cc86dad2f18c818d25ed93803370b30f02bb0d`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d0ce146cd9874b06be341bd5a6e16de55ac10f21f1a53d731064965a51b8f8`  
		Last Modified: Thu, 17 Dec 2020 06:49:04 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd9a756af2a7cc6ffc0e22a22abe348096271681343c379d9118f93353c0e00e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6788811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4d5284f6e232b2d496689a6171fe3ebe65451bb95a86198d7b98f0f4b50689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:35:31 GMT
ENV NATS_SERVER=2.1.9
# Thu, 17 Dec 2020 01:35:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 17 Dec 2020 01:35:36 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 17 Dec 2020 01:35:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Dec 2020 01:35:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Dec 2020 01:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Dec 2020 01:35:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da0fc46766edc6d67bc9fa0297ed044b58ac6149a9966f5b75b50e963413cf4`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 4.1 MB (4078793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0c680e95f0e69b736b925b086864acfd590db86cd90770cd936d1f75f460b7`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf7ca242ef63f98cf4d60c719aa99b7da938719b113735c2781290b1f021a26`  
		Last Modified: Thu, 17 Dec 2020 01:36:27 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:5d718b257e66e9e23691968c95ad024b114f3b64ab1cb840372f6e20677209d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1697; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:21f6fc01450a8b9c0a03f37fe475150800b575d5b0a05ada60f988333b2dc1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:21f6fc01450a8b9c0a03f37fe475150800b575d5b0a05ada60f988333b2dc1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:88e7ef9ed2d43c41627dba116576202a45687216a5664be9e0684736728df2ed
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105387760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318f8c1d3e273dae2d784752559c2e4004fbfdab8510027f9cd975ae63989cca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:06:01 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:02 GMT
RUN cmd /S /C #(nop) COPY file:1bed18dba32dca3cc37e8d20c1b6b2b5179bbc92f869531591951b440efda07a in C:\nats-server.exe 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:06:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:06:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:06:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a89b73109217060f51d51b7d3a7eda3a9ac0de9c5f76db54addb98b7f1c24c1`  
		Last Modified: Wed, 13 Jan 2021 19:10:49 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa49af7930d322a3f544efd04656b6212d6be0f38a1c9a9147f33da4577d926`  
		Last Modified: Wed, 13 Jan 2021 19:10:48 GMT  
		Size: 4.0 MB (4042705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7f858b484246ab3fc517691e1aeba2e6b57ddd4ffe2ae2a23aac5686623c92`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 1.5 KB (1498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a625d562403cf1d7dbb43a360e0bdb16af8d917d80c6c163bfb53d3e3f04ad`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab387c849a175742ba9eda4ccba7bcd0d63d367a60eb6964dd0ddfb7df17d`  
		Last Modified: Wed, 13 Jan 2021 19:10:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6181698bf9c06bad79f24e75146be1cc83f547d7b5563dd723433c4c05badeb`  
		Last Modified: Wed, 13 Jan 2021 19:10:47 GMT  
		Size: 874.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:dc0ba254275cb917eec2b9d1fd1055fe132c854a9afea39628c4871a10b49db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:679524b91e0a1e4b983d20d70f7a1495f1c16247cf568f29cbf88f5c4b25e914
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95713166e2236aefedbb92b1d1ef989f979e5c737ff5c14d45d9e32803f032bb`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:e0a0cbd14b84d81f9a3d73a7eefe99693215eb890370f9aba1b574d4cbf63b52 in /nats-server 
# Tue, 03 Nov 2020 00:32:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:32:03 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:32:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:32:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d6c7151b0c792ecf790fde24412769bf193e4c1922c8a508f8e137d292b4179`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 4.1 MB (4097661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920bf257e35e5e325af3ffc17a4baed7903a77f327e8ec3021f94016a78a239`  
		Last Modified: Tue, 03 Nov 2020 00:32:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7c6e8cffea7e48d3ee02b22fb93947963731051dcc56f3c8ec98f2260768814b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3817067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a584107a14f067c0a007db6f0e42b3ff0c190fa2d866f5581552cc559a035125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:4cd9814103fc39d1b5bf81e4e528b12e56d59d0efda223c50a7ea420e6d4b421 in /nats-server 
# Mon, 02 Nov 2020 23:53:40 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Mon, 02 Nov 2020 23:53:41 GMT
EXPOSE 4222 6222 8222
# Mon, 02 Nov 2020 23:53:41 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 02 Nov 2020 23:53:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e162374a08bbb575088c1eaffc753891ab6589b134493a9f8ba1b148e20f8dec`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 3.8 MB (3816591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77a00778e9ed2ae19795da75b6f12f291e70490f03cc4565c407af242ace47`  
		Last Modified: Mon, 02 Nov 2020 23:54:20 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1f4b725d1989c235e10f362b0f9c04a708fe6b1dfb22e2efc236b0d2a001ef8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d6781ef03c3263effcb9f73ae01394a0dae4af477e75c00c19544d0bfe66b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:0513d05e9f97918c0430b076865e30771904270865892c092e15d1beb98d08c4 in /nats-server 
# Tue, 03 Nov 2020 00:03:52 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:03:53 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:03:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:03:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed0e6ae1888bfc5be9efcd3bbca71bd2840e4361003c98476fd25ce7d6e9ee14`  
		Last Modified: Tue, 03 Nov 2020 00:04:34 GMT  
		Size: 3.8 MB (3812940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b242a83395577c4be465d49aee9b3d407ea026cb0383e18836fb6ed16caa34c`  
		Last Modified: Tue, 03 Nov 2020 00:04:33 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:670bb4f03b559b3f9d0d2e736450bbb77ae1a789bbfac3b11a09c531d6cf412e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd733d2cc8ad31f06df9779323962d0e6f73681100397d3090b1e57bc25be709`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:e1e30af7043f9127562e3a3ea4612aaf12d52aac32a8466b822dbbbeebaaef76 in /nats-server 
# Tue, 03 Nov 2020 00:21:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Tue, 03 Nov 2020 00:21:38 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:21:39 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 03 Nov 2020 00:21:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6433bc19867b0af777bb4176a307bfb021a5ee3d3ad8390bb912e6787b729c8`  
		Last Modified: Tue, 03 Nov 2020 00:22:16 GMT  
		Size: 3.8 MB (3794815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d0ed92b996d8a726daa5da839bd0dfa4651c38c36a2f9a62af31ed304b10a6`  
		Last Modified: Tue, 03 Nov 2020 00:22:14 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:0065f20e4c3d3353a1923e3b2040b1e8ce0c8dd427ee3d5bded3a63aa095e743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64
	-	windows version 10.0.14393.4169; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:aada5edd446c33d7f0cdec0fefcb38a8b5590e44d4dc3c96a251e4dc70dc3331
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454148019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031dbf4ba2968a5141c84684c424493436b1c5c06ceada8f998aad51a31a186`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 15:20:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:04:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:04:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:04:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:04:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:04:37 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:05:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:05:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:05:49 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:05:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:05:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f84df50d9e20cf852bfd3555d4e56feabf7b9c735e48c613fc461146876bc03`  
		Last Modified: Wed, 13 Jan 2021 18:31:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff779c93810f460e9728c49a995f9cdd81c09b10ffc6e842f2272d19bf4389c`  
		Last Modified: Wed, 13 Jan 2021 19:10:22 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faaba717596a54bf51953c222df419b525a196529e9d4d0c98e44bf6c7bc4ee`  
		Last Modified: Wed, 13 Jan 2021 19:10:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cb7951519de47a30ef002cff4cb9c60650027cae289b36b71148ac51859b63`  
		Last Modified: Wed, 13 Jan 2021 19:10:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e01bfa5d9722f31f0db2b1d9a8b4c590620491626f2bd622eebef651c8aa8`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62774ffa1eced43b67a7b2e3ad24b3bade3513280a5135aa994e68fd6744ab46`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 5.0 MB (4995396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07cd3dac74e385b2c29cc30fee72c5dba6fe50c4e8693107469d14a3ac38e40`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 13.4 MB (13369683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac73259d45c25f57b84af56ae813f5c1071b64fd365abc139468c74741017c90`  
		Last Modified: Wed, 13 Jan 2021 19:10:14 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e972d90c5bf2368649731e44c25e0b6d0d7615adbeeb4830fdd61d05c703710`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe9f87a1c2bb4a7311943263ac9446984971e7804672e6c71473ec4619d723`  
		Last Modified: Wed, 13 Jan 2021 19:10:15 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c96eb244980fd8b710cd559fc78aba2933f3cd5bb8b7d0d8cdd2a7bc287227`  
		Last Modified: Wed, 13 Jan 2021 19:10:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4169; amd64

```console
$ docker pull nats@sha256:a3d15409d2215acd9b8bb21c0fd2c006789f5147c98e91efdf04cdfb3f71ed7d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813747776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532f1992cb14b60a3059cf3651152f113910fc513246a702cae67b06fafdac27`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 15:29:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:06:11 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:06:13 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:07:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:09:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:09:19 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:09:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b5ee02f83739eef6745d432d63363ce5f490820d4b3e39ae83aa4e3771c4073`  
		Last Modified: Wed, 13 Jan 2021 18:32:39 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd1c346230e9eaf41e5c8f582c16f531efe65ddbc7fad4e748dd41227e0bbbb`  
		Last Modified: Wed, 13 Jan 2021 19:11:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a1c3cb2cafeec468c4b189a9bb82928aeff9d8d20c78fac2661ba6eefa7cd0`  
		Last Modified: Wed, 13 Jan 2021 19:11:20 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f7a55bb339a043e41c3e13a2ddc5aacdbe7909f27a5a73334bcd6981ab005`  
		Last Modified: Wed, 13 Jan 2021 19:11:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b36a1e84f430bc8f437c60f1315e5f8fb5ab2d2d2ad0d5da53867887721cc`  
		Last Modified: Wed, 13 Jan 2021 19:11:17 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f343d10dd4537d6d5f04f7f5702c0b2fa5a54f0b76e4cb07165d6b76252af5`  
		Last Modified: Wed, 13 Jan 2021 19:11:26 GMT  
		Size: 5.6 MB (5633704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf954465e03e8a00f8de44752e29cbd77730020de5ec6526fce80d822868918`  
		Last Modified: Wed, 13 Jan 2021 19:11:18 GMT  
		Size: 14.2 MB (14209225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db694fce26f8975588646948bdce55a92c5305cc61489ef76e4b5b2d16930f51`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457fc56aeae1295b29bf9edde0f0aaf9b177e5a279f82ddc05c35f3471ec4b6`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040b08654e387e662885b914e16cca191b89a16cc3577ba5fb24d3a9e903a73`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1933d956bffa8e85f00a1273a28efc2f6e9393ea13015240046d5e30222f64b2`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:ea0be7c6f01582d60f391e779978dd496c114087cac9dff08c979b91ca2777c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull nats@sha256:aada5edd446c33d7f0cdec0fefcb38a8b5590e44d4dc3c96a251e4dc70dc3331
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2454148019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c031dbf4ba2968a5141c84684c424493436b1c5c06ceada8f998aad51a31a186`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 15:20:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:04:04 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:04:05 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:04:06 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:04:06 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:04:37 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:05:47 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:05:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:05:49 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:05:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:05:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f84df50d9e20cf852bfd3555d4e56feabf7b9c735e48c613fc461146876bc03`  
		Last Modified: Wed, 13 Jan 2021 18:31:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff779c93810f460e9728c49a995f9cdd81c09b10ffc6e842f2272d19bf4389c`  
		Last Modified: Wed, 13 Jan 2021 19:10:22 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faaba717596a54bf51953c222df419b525a196529e9d4d0c98e44bf6c7bc4ee`  
		Last Modified: Wed, 13 Jan 2021 19:10:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cb7951519de47a30ef002cff4cb9c60650027cae289b36b71148ac51859b63`  
		Last Modified: Wed, 13 Jan 2021 19:10:21 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2e01bfa5d9722f31f0db2b1d9a8b4c590620491626f2bd622eebef651c8aa8`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62774ffa1eced43b67a7b2e3ad24b3bade3513280a5135aa994e68fd6744ab46`  
		Last Modified: Wed, 13 Jan 2021 19:10:19 GMT  
		Size: 5.0 MB (4995396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07cd3dac74e385b2c29cc30fee72c5dba6fe50c4e8693107469d14a3ac38e40`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 13.4 MB (13369683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac73259d45c25f57b84af56ae813f5c1071b64fd365abc139468c74741017c90`  
		Last Modified: Wed, 13 Jan 2021 19:10:14 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e972d90c5bf2368649731e44c25e0b6d0d7615adbeeb4830fdd61d05c703710`  
		Last Modified: Wed, 13 Jan 2021 19:10:17 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe9f87a1c2bb4a7311943263ac9446984971e7804672e6c71473ec4619d723`  
		Last Modified: Wed, 13 Jan 2021 19:10:15 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c96eb244980fd8b710cd559fc78aba2933f3cd5bb8b7d0d8cdd2a7bc287227`  
		Last Modified: Wed, 13 Jan 2021 19:10:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:b2473c0f9192eddd51042f9ecb680e61e087793aaf726ef09d8459a48447461a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull nats@sha256:a3d15409d2215acd9b8bb21c0fd2c006789f5147c98e91efdf04cdfb3f71ed7d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813747776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532f1992cb14b60a3059cf3651152f113910fc513246a702cae67b06fafdac27`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 15:29:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jan 2021 19:06:11 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER=2.1.9
# Wed, 13 Jan 2021 19:06:12 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.9/nats-server-v2.1.9-windows-amd64.zip
# Wed, 13 Jan 2021 19:06:13 GMT
ENV GIT_DOWNLOAD_SHA256=cb4ec25356a0200edcd5df579cfa06154f5576c2c48d3727dca2117d6e7e5891
# Wed, 13 Jan 2021 19:07:22 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jan 2021 19:09:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jan 2021 19:09:18 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 13 Jan 2021 19:09:19 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Jan 2021 19:09:20 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Jan 2021 19:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b5ee02f83739eef6745d432d63363ce5f490820d4b3e39ae83aa4e3771c4073`  
		Last Modified: Wed, 13 Jan 2021 18:32:39 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd1c346230e9eaf41e5c8f582c16f531efe65ddbc7fad4e748dd41227e0bbbb`  
		Last Modified: Wed, 13 Jan 2021 19:11:23 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a1c3cb2cafeec468c4b189a9bb82928aeff9d8d20c78fac2661ba6eefa7cd0`  
		Last Modified: Wed, 13 Jan 2021 19:11:20 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090f7a55bb339a043e41c3e13a2ddc5aacdbe7909f27a5a73334bcd6981ab005`  
		Last Modified: Wed, 13 Jan 2021 19:11:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b36a1e84f430bc8f437c60f1315e5f8fb5ab2d2d2ad0d5da53867887721cc`  
		Last Modified: Wed, 13 Jan 2021 19:11:17 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f343d10dd4537d6d5f04f7f5702c0b2fa5a54f0b76e4cb07165d6b76252af5`  
		Last Modified: Wed, 13 Jan 2021 19:11:26 GMT  
		Size: 5.6 MB (5633704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf954465e03e8a00f8de44752e29cbd77730020de5ec6526fce80d822868918`  
		Last Modified: Wed, 13 Jan 2021 19:11:18 GMT  
		Size: 14.2 MB (14209225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db694fce26f8975588646948bdce55a92c5305cc61489ef76e4b5b2d16930f51`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457fc56aeae1295b29bf9edde0f0aaf9b177e5a279f82ddc05c35f3471ec4b6`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040b08654e387e662885b914e16cca191b89a16cc3577ba5fb24d3a9e903a73`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1933d956bffa8e85f00a1273a28efc2f6e9393ea13015240046d5e30222f64b2`  
		Last Modified: Wed, 13 Jan 2021 19:11:14 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
