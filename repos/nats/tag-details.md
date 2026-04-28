<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.22`](#nats2-alpine322)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-ltsc2022`](#nats2-nanoserver-ltsc2022)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-ltsc2022`](#nats2-windowsservercore-ltsc2022)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.22`](#nats211-alpine322)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-ltsc2022`](#nats211-nanoserver-ltsc2022)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-ltsc2022`](#nats211-windowsservercore-ltsc2022)
-	[`nats:2.11.17`](#nats21117)
-	[`nats:2.11.17-alpine`](#nats21117-alpine)
-	[`nats:2.11.17-alpine3.22`](#nats21117-alpine322)
-	[`nats:2.11.17-linux`](#nats21117-linux)
-	[`nats:2.11.17-nanoserver`](#nats21117-nanoserver)
-	[`nats:2.11.17-nanoserver-ltsc2022`](#nats21117-nanoserver-ltsc2022)
-	[`nats:2.11.17-scratch`](#nats21117-scratch)
-	[`nats:2.11.17-windowsservercore`](#nats21117-windowsservercore)
-	[`nats:2.11.17-windowsservercore-ltsc2022`](#nats21117-windowsservercore-ltsc2022)
-	[`nats:2.12`](#nats212)
-	[`nats:2.12-alpine`](#nats212-alpine)
-	[`nats:2.12-alpine3.22`](#nats212-alpine322)
-	[`nats:2.12-linux`](#nats212-linux)
-	[`nats:2.12-nanoserver`](#nats212-nanoserver)
-	[`nats:2.12-nanoserver-ltsc2022`](#nats212-nanoserver-ltsc2022)
-	[`nats:2.12-scratch`](#nats212-scratch)
-	[`nats:2.12-windowsservercore`](#nats212-windowsservercore)
-	[`nats:2.12-windowsservercore-ltsc2022`](#nats212-windowsservercore-ltsc2022)
-	[`nats:2.12.8`](#nats2128)
-	[`nats:2.12.8-alpine`](#nats2128-alpine)
-	[`nats:2.12.8-alpine3.22`](#nats2128-alpine322)
-	[`nats:2.12.8-linux`](#nats2128-linux)
-	[`nats:2.12.8-nanoserver`](#nats2128-nanoserver)
-	[`nats:2.12.8-nanoserver-ltsc2022`](#nats2128-nanoserver-ltsc2022)
-	[`nats:2.12.8-scratch`](#nats2128-scratch)
-	[`nats:2.12.8-windowsservercore`](#nats2128-windowsservercore)
-	[`nats:2.12.8-windowsservercore-ltsc2022`](#nats2128-windowsservercore-ltsc2022)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.22`](#natsalpine322)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-ltsc2022`](#natsnanoserver-ltsc2022)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-ltsc2022`](#natswindowsservercore-ltsc2022)

## `nats:2`

```console
$ docker pull nats@sha256:5c5ae59dd58fe77318be7ae31b5a18a1730c6ca2c2fd94572d0ee5a81e0c9234
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5020; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:fd5dd09bc60658223075241956f5c1a12ee7b7899258b2a481aad6782476b747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:fd5dd09bc60658223075241956f5c1a12ee7b7899258b2a481aad6782476b747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:7be687bd0fcf28c0ff569af5d07b5586400ddc2e656ed5059fa069a1861d5310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:513908e15de358856596ba7150e84b831f6f711b57c69bff1dab9e0f2334ccc1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5993871186ecfe774a9cf8a2b3de0621e6afaf3fd93f99cbbaff6fffc782a8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:22:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:22:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:22:21 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:22:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:22:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 28 Apr 2026 00:22:24 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 28 Apr 2026 00:23:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:24:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:24:04 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:24:05 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:24:05 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:24:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ffdad23a2259ee9605b07af3b8756afac669d72d7f4df289af5e1bfa765df`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349750824325190c58f7211d2a32fac8867324987e4912f6187dc9d6f9fb4ae8`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e65ce208cc089d5d84714aa1b4c702e6514a37bc1a25a9e317e5484c4b6770`  
		Last Modified: Tue, 28 Apr 2026 00:24:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fefac29241015b39520060d922c7fb6054787dd9dd417b2cabd03743d7bda5f`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe557d93a73db69714369a258c20de37e40d04268b2f4804c92e12e16976bdd`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3130aba43c6a9d55589835a86638de2d3125fa2366b684015a8ac9fc1c818d`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19f58f4c90bd0a1c10a151c0165e6d1660f82cb62c97e4a3e1ec5be69c14d0`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 507.2 KB (507220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b029516bfa850bb0dc8d626d1e3a9cda785c0b6ff3e1ac8797afb2adf5f0ed3`  
		Last Modified: Tue, 28 Apr 2026 00:24:15 GMT  
		Size: 7.2 MB (7178445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8a07055de8fc46e4e8f02f1a81c1872033e0a3dda665ba7f3a7cdba7cd203`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2e16a4341e7b5618098955dbd5110c7fc4e24810d6e25bb7cd53e768b4539`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a737b9ff5aae65f741d22ddd5e6e1c210d6f45528f4778fcb53b923c0e903`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbeaf674140e140a6e0cb9b0b83df4612f9ab45bc55e9507b8d32bb2be05e1`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:7be687bd0fcf28c0ff569af5d07b5586400ddc2e656ed5059fa069a1861d5310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:513908e15de358856596ba7150e84b831f6f711b57c69bff1dab9e0f2334ccc1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5993871186ecfe774a9cf8a2b3de0621e6afaf3fd93f99cbbaff6fffc782a8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:22:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:22:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:22:21 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:22:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:22:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 28 Apr 2026 00:22:24 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 28 Apr 2026 00:23:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:24:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:24:04 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:24:05 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:24:05 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:24:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ffdad23a2259ee9605b07af3b8756afac669d72d7f4df289af5e1bfa765df`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349750824325190c58f7211d2a32fac8867324987e4912f6187dc9d6f9fb4ae8`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e65ce208cc089d5d84714aa1b4c702e6514a37bc1a25a9e317e5484c4b6770`  
		Last Modified: Tue, 28 Apr 2026 00:24:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fefac29241015b39520060d922c7fb6054787dd9dd417b2cabd03743d7bda5f`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe557d93a73db69714369a258c20de37e40d04268b2f4804c92e12e16976bdd`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3130aba43c6a9d55589835a86638de2d3125fa2366b684015a8ac9fc1c818d`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19f58f4c90bd0a1c10a151c0165e6d1660f82cb62c97e4a3e1ec5be69c14d0`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 507.2 KB (507220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b029516bfa850bb0dc8d626d1e3a9cda785c0b6ff3e1ac8797afb2adf5f0ed3`  
		Last Modified: Tue, 28 Apr 2026 00:24:15 GMT  
		Size: 7.2 MB (7178445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8a07055de8fc46e4e8f02f1a81c1872033e0a3dda665ba7f3a7cdba7cd203`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2e16a4341e7b5618098955dbd5110c7fc4e24810d6e25bb7cd53e768b4539`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a737b9ff5aae65f741d22ddd5e6e1c210d6f45528f4778fcb53b923c0e903`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbeaf674140e140a6e0cb9b0b83df4612f9ab45bc55e9507b8d32bb2be05e1`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:d832f2afda7c4029e7a8a8ced293e10c85afdf1393218a55afa1e572de87addf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:71a050049d35eba31bcb508dbbb7354f78d3c2095c5bb5607a24387cc5bc4a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6506533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8296541e734afc4b6f168616aecb56cd7168616d55b63d5eea8ed82ccb6411d6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:18 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aec33d706d05c0d0673a0501735c6856bf256195120254d0de66b2ed8487b518`  
		Last Modified: Mon, 27 Apr 2026 16:34:37 GMT  
		Size: 6.5 MB (6506024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373d31d8c613e3d8b7187644e676f86abc8ac126a61bcec845abe87615a25c60`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:a4f0911609b3aed35285a1a023fdc4339cdafe40a3dc7ff4b44a32894268edf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1571b84fa4de3ebfb8bb1b52ec208f93ff9f944e01f4c39085654782dfe31e`

```dockerfile
```

-	Layers:
	-	`sha256:ac9ef0dc94f099a1d6b5159715d9b9f485407bb888d585fae78dee1fb8a0f54a`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:5af32bb50db4178223e7f2ae746f250688a2ac5f8251f1b0301cc325ca2b4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff60a9c1027e6d6dac58b0b5b930c1f9e8aaa7d2258c0c0d45bfeec219b8c1c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c8f4c909fd0463d9b5b13c9f56b1811ce5523b2543f4d1e2c56b82831e5a4e9`  
		Last Modified: Mon, 27 Apr 2026 16:34:34 GMT  
		Size: 6.2 MB (6227926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad28a45d074122dc77de825b24829a158ed4144d3b089fc552c2cef59bfef6b`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:524d0da25890b35e24714c0e4475fac2f5b2cb4170e8e2d0b791117770144875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3b6f2f449e6cb4715a28621439b1003a9b7bfcfbbda49afe212518add9b86e`

```dockerfile
```

-	Layers:
	-	`sha256:ff9ac7cf2ce3006d3a49116832bfe4d8607d0e74db9c63b505ba8312143e1eb4`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:075508e648218cd7576c21cd34d51303d30c33ba7701e9277e9bc697e639d315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6217157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8342812a9880b1bba9090606591051b1205e793a55a9daa07c2b8ec69151cdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9078b87ee8498b3d94d7549f00ad3d978318f849ad8317e3929c38283f48980a`  
		Last Modified: Mon, 27 Apr 2026 16:34:36 GMT  
		Size: 6.2 MB (6216647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:3305bbef52bf5d8195e149421f737534304c6052e691b03cb4614ac028b903a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1994ac9373db777505778e0f36c5c67cdc3c48edf51c14cad1ebc1d68d54c51`

```dockerfile
```

-	Layers:
	-	`sha256:5b4d2ea9acb88f8a5b1b3f7f096762dd1f361efef8fd74687640963e88c9bc05`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ea40df8297d021756a9d6f5cce234d04424d067849d089e87b7d45e0eb0c2e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5920552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160754dbd0c1d280f89c70d023f003957b69de52f2f7a7e39f82c4c0272e2700`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1ce8862d5cf59cc1c1fc9f8534b9ad9707adb7e4ffca95852e829e0d9c6246cc`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 5.9 MB (5920042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe27b9af333eebb2c391e8c349d49dca334d0981f22eace6afe19240ac639d`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:b215c14c5042de1ef395b6195ab83103c3289a103ba7b11ef7694b1b9d9b2315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133abc1576edbe5bc8fad94ae0a96e22a4f159158e05b355f465e2e20de5617a`

```dockerfile
```

-	Layers:
	-	`sha256:52e00b6d6c84eb1189627237d780fc71be9065ec2dea64361f469287e9fccfcd`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:1d20b1fe94f9c2b77b8b5decb3e8f28750e7ee17b9043872a206c16712954f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dadc06aaae2240c7750e1536c5077f8de1875669e5a4ba1dddb44a22b37e0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:26 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8ceef00297aadc77f604a976e256c7afc8ad7d11975a0a70c8d18989f84c377`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 6.0 MB (5970296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92f65bc5b9eb57afda73d65184405d53b72810b4dbbf96522528f810b7db9cf`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:d9a0da7986d6d545c8c60d7629ccd762270083819a8906e2d4a649b9419f0c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28237b9ce41d2c243867583d6a0264a050bf08bca473927228a653d6ce0a0ccd`

```dockerfile
```

-	Layers:
	-	`sha256:b1faceab9662f79250490806f3fea1c75a45ecc38e6df8324ff609299620af98`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:e35294278ff76bcb1fe56374110f4b06c269576ed7790035cb884905514779bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f361bf360d8325e6fcd51b413da8e62bc9d3349d5ffa47ce66c77b64b681ec30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9078b3e5e7cd72051df8071c386cbf0335d800dad99509157ffcfd8f4fc361`  
		Last Modified: Fri, 17 Apr 2026 03:00:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:f7b77c54d8013e193fe1637d61d70596d15af7f467886c746e4990c02b80a60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd2c9c3f0905b48a181ecb2c54e99817e889d09b559ccb3625163e3ddb9966`

```dockerfile
```

-	Layers:
	-	`sha256:553590c07c651e9bd4871f634514aac2810de7afce20d412adc0440624524452`  
		Last Modified: Fri, 17 Apr 2026 03:00:37 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:5ffa3167d5e3e3fd4258586b3e58689d9ca02a145f6b5cbc6a82f8416b7c61e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133637234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29654dc94df41eabc4fec5c6267f3e71846d39bd31cc97f52dd46404020ce98`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:52 GMT
RUN cmd /S /C #(nop) COPY file:f1ed4e18be63052ebd2a9f8f87593bf079db370ff176ea712b36dc2ac83ea376 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:54 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed04d46136c3797ba3fc4ddcaceedae8a6fc3fd40e4f77f0929591c7b645a51`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2f5a47ed51a8fd3b8ccbc37ae5b9d89766a7cd30ac5138fc1abab63a8917e`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 6.7 MB (6675280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd0b5b898034b9675ff6aa86b1a3b107c8ca3cc2788fca25c8f4f1ff65c4840`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823643c2dcd9d2a19ef822365ba3d59a932d0f663749945aec1c1fb74a7fff98`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286cfe5bab4a54ba713d5f92768b2ecfd0a029b275ba96d7b2c6dcca57056c6`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4274ef274b88859bdfe852c4c36f18d9eca26a752f7d521c3ee89749b253221`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:e4bf19f15fd3218814a4e3c9e0064e1334bd8aa20d5984b9f1a0afd084f8cc00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a7d440bf0240e664ed74fc17c70d616e6ff4bb9890dc26f7276589daedd1e196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10769172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c7ef2d2b735068633f2dc9012ce5189e5f006096b6dad5ecff36dd3c6eb9b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6b54cbc38525fc1d30bbbb48e738ce617b74e93908bbb872cc93b73315db66`  
		Last Modified: Tue, 28 Apr 2026 00:10:50 GMT  
		Size: 7.0 MB (6960013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca157d5b7da38d0cb5255d9031d0f3c52f3303720e20cf79cbf201b80d94c0d`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be21133830b00a74c18a4947a0aafba1532fbcba6546b27d6397ff82713cafbd`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7ba2eadf86813e9a2a364a6f4670ee4418722dca64ee00be1c2e3cfc3b66077e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28b8be38c0d25f99437dc9b5790913b65d1400c46c71b1bfcac89ef301e2bbb`

```dockerfile
```

-	Layers:
	-	`sha256:218267d15d714bea6549013852c5ad8c07af7afeed21d08a62fdda53c0e98fca`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c8bada39c7f8448cdaecf39592855d589b23ace79c47c7f236ecba7d68b33aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10193817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a358738e52ffe5c541003daa6c899dc10715b9c91de1350a2673300a34aa5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:59 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:10:59 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:10:59 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e168a6db6ab9021053c1d1be43765a9182b87283ad4cf420ad7b8efbe3b24fcd`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 6.7 MB (6685465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb40f4dd56e1396a6ee32561a8ca3185283d320f12eb93885a3cabb41cf8d932`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e076015276b74b5cc31eb2cf84848ec6ff0a84e5afa62ece72ff21ca3822e7ba`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:45681bb1b26adeb0bdc0329beafef7b2f80677e0cc332f46cd6022d1e14873b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34948f0787240b55485f6d9c1c24640400b74832a0b228fac861ecf4fe1617f4`

```dockerfile
```

-	Layers:
	-	`sha256:288462c9c0469ef7dd15de311c843a0854e1af099f303c3347af7bdf1c05aa1e`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e6ca3f449ab5b378b030a47e7bbfbda9063cc722e0437c9be1ca8a6b627b0f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9901537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f3333717afc3b36a6eeb66c988f20c07f9a1eda8b03ec39280ebc45122d3fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:31 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:11:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:11:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad226131af5a49e8e5da1ddd881df2b35b10a7a3e12cde83b27a966e8259d930`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 6.7 MB (6674737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56bba8fd3f5f27de4228f8a29adfba16bd15df9fb46a2726c72c7afc8375828`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a46cc9867199da12df2ff8f366aad6030fc73c8376f3d00cdb2ee39164c9ae`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1dc353c67460bbb8a1e5b156837bb144f999a524ed85d5852e6aee82b3b63fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d972ca3d35d3ca43407bdb4fe5ae1002f438e6347dc4eb7705426a06f7f9c1f4`

```dockerfile
```

-	Layers:
	-	`sha256:a83bc6829540b6b2bc2bebf85423ffca9bdcac4b9f25e9f973fa095baf131b26`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:69fa60167708111e9318f327bb7b3609ad9d4d3e7a0d16243231c5a6e9a8fb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7f87c86557a749c3b414af53a0a5ac4f3a8a3bd94a4c5395f28071fad8289a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:17 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:11:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:11:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767309eebe99876fafbf4a9ef30dac5fd062c98907a979c91301cadd8419a8e`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 6.4 MB (6382369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e279c81670829f705cb5d56a31edfd682dc3e6867db2f0744613a2c3c8141`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fddd138a70823c87b6d9a5835c6d164301d59c457b5ace8b4d09178e10570e`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c354d41ddf541af425a5daf4d02f00611d60b964ef8a2138077c7ecba39fd48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29aa5190dd4a144cac18e09c2145e7c2b133b2513e4fbcb4aa955f972281c51`

```dockerfile
```

-	Layers:
	-	`sha256:24580254badc6cc0410a9ceda2b19ee728de9bdea1749c24921888a7983b4d79`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:c81b5302d3988d6fa2c166ccf2340164a9ce9bd76f468180a0038c063e9c3d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10168040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb3d41b4064e711a4fbe5d12883d3f4eb16f072908619352ef59331bd52baf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3fd852d0afd5e21d494d8333dc133779914e56c90f51f200586eb0ecac28ee`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.4 MB (6430411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0568b8daea5a9bf497889271f07cda84b490fd3b16a1da88b0cb11f028e42da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3166e2d4947db30db38aa4ecb26aca06d282daaa111b14be944c9cce3043dc3d`

```dockerfile
```

-	Layers:
	-	`sha256:4e9be753004a392414cda36251748f3ef58bdb58d883ecc3ce43c603a04a447e`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:b91caeb3114b6318269374969d3ef1d3007ad1ff6d415b2459895b86041c3c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714f4e2e84044a1be752471a916485a584d46e02f070cac266029247a8186946`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:01 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:16:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:16:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d782e28ffadbebd6def10357cfd2f31431bd0fb84bdee0592406e8f18656094`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.8 MB (6803883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2285ded99cc9a628d98575421a3d519dedd90b80c572a82911bcbd49ce89fed5`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128fd32596802807b84459b2b3dc2a91dd083261a2da76168fbd385bfd5f9dab`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4d5bc00030f9b8e9cc663d67e992c46b73b9a5f7b53e26f7ae6936e8932f4b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fbdaf743cac00badea79267ceb4a58b85839e640a1938f7cba612ffb9050fa`

```dockerfile
```

-	Layers:
	-	`sha256:75caba598230dbf1aa625443cfa3a6e95061b18ec6e8731f0b1cbbf3ccb50b71`  
		Last Modified: Tue, 28 Apr 2026 00:16:44 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.22`

```console
$ docker pull nats@sha256:e4bf19f15fd3218814a4e3c9e0064e1334bd8aa20d5984b9f1a0afd084f8cc00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:a7d440bf0240e664ed74fc17c70d616e6ff4bb9890dc26f7276589daedd1e196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10769172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c7ef2d2b735068633f2dc9012ce5189e5f006096b6dad5ecff36dd3c6eb9b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6b54cbc38525fc1d30bbbb48e738ce617b74e93908bbb872cc93b73315db66`  
		Last Modified: Tue, 28 Apr 2026 00:10:50 GMT  
		Size: 7.0 MB (6960013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca157d5b7da38d0cb5255d9031d0f3c52f3303720e20cf79cbf201b80d94c0d`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be21133830b00a74c18a4947a0aafba1532fbcba6546b27d6397ff82713cafbd`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7ba2eadf86813e9a2a364a6f4670ee4418722dca64ee00be1c2e3cfc3b66077e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28b8be38c0d25f99437dc9b5790913b65d1400c46c71b1bfcac89ef301e2bbb`

```dockerfile
```

-	Layers:
	-	`sha256:218267d15d714bea6549013852c5ad8c07af7afeed21d08a62fdda53c0e98fca`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:c8bada39c7f8448cdaecf39592855d589b23ace79c47c7f236ecba7d68b33aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10193817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a358738e52ffe5c541003daa6c899dc10715b9c91de1350a2673300a34aa5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:59 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:10:59 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:10:59 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e168a6db6ab9021053c1d1be43765a9182b87283ad4cf420ad7b8efbe3b24fcd`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 6.7 MB (6685465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb40f4dd56e1396a6ee32561a8ca3185283d320f12eb93885a3cabb41cf8d932`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e076015276b74b5cc31eb2cf84848ec6ff0a84e5afa62ece72ff21ca3822e7ba`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:45681bb1b26adeb0bdc0329beafef7b2f80677e0cc332f46cd6022d1e14873b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34948f0787240b55485f6d9c1c24640400b74832a0b228fac861ecf4fe1617f4`

```dockerfile
```

-	Layers:
	-	`sha256:288462c9c0469ef7dd15de311c843a0854e1af099f303c3347af7bdf1c05aa1e`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:e6ca3f449ab5b378b030a47e7bbfbda9063cc722e0437c9be1ca8a6b627b0f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9901537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f3333717afc3b36a6eeb66c988f20c07f9a1eda8b03ec39280ebc45122d3fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:31 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:11:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:11:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad226131af5a49e8e5da1ddd881df2b35b10a7a3e12cde83b27a966e8259d930`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 6.7 MB (6674737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56bba8fd3f5f27de4228f8a29adfba16bd15df9fb46a2726c72c7afc8375828`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a46cc9867199da12df2ff8f366aad6030fc73c8376f3d00cdb2ee39164c9ae`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1dc353c67460bbb8a1e5b156837bb144f999a524ed85d5852e6aee82b3b63fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d972ca3d35d3ca43407bdb4fe5ae1002f438e6347dc4eb7705426a06f7f9c1f4`

```dockerfile
```

-	Layers:
	-	`sha256:a83bc6829540b6b2bc2bebf85423ffca9bdcac4b9f25e9f973fa095baf131b26`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:69fa60167708111e9318f327bb7b3609ad9d4d3e7a0d16243231c5a6e9a8fb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7f87c86557a749c3b414af53a0a5ac4f3a8a3bd94a4c5395f28071fad8289a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:17 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:11:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:11:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767309eebe99876fafbf4a9ef30dac5fd062c98907a979c91301cadd8419a8e`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 6.4 MB (6382369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e279c81670829f705cb5d56a31edfd682dc3e6867db2f0744613a2c3c8141`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fddd138a70823c87b6d9a5835c6d164301d59c457b5ace8b4d09178e10570e`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c354d41ddf541af425a5daf4d02f00611d60b964ef8a2138077c7ecba39fd48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29aa5190dd4a144cac18e09c2145e7c2b133b2513e4fbcb4aa955f972281c51`

```dockerfile
```

-	Layers:
	-	`sha256:24580254badc6cc0410a9ceda2b19ee728de9bdea1749c24921888a7983b4d79`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:c81b5302d3988d6fa2c166ccf2340164a9ce9bd76f468180a0038c063e9c3d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10168040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb3d41b4064e711a4fbe5d12883d3f4eb16f072908619352ef59331bd52baf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3fd852d0afd5e21d494d8333dc133779914e56c90f51f200586eb0ecac28ee`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.4 MB (6430411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:0568b8daea5a9bf497889271f07cda84b490fd3b16a1da88b0cb11f028e42da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3166e2d4947db30db38aa4ecb26aca06d282daaa111b14be944c9cce3043dc3d`

```dockerfile
```

-	Layers:
	-	`sha256:4e9be753004a392414cda36251748f3ef58bdb58d883ecc3ce43c603a04a447e`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:b91caeb3114b6318269374969d3ef1d3007ad1ff6d415b2459895b86041c3c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714f4e2e84044a1be752471a916485a584d46e02f070cac266029247a8186946`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:01 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:16:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:16:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d782e28ffadbebd6def10357cfd2f31431bd0fb84bdee0592406e8f18656094`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.8 MB (6803883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2285ded99cc9a628d98575421a3d519dedd90b80c572a82911bcbd49ce89fed5`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128fd32596802807b84459b2b3dc2a91dd083261a2da76168fbd385bfd5f9dab`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4d5bc00030f9b8e9cc663d67e992c46b73b9a5f7b53e26f7ae6936e8932f4b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fbdaf743cac00badea79267ceb4a58b85839e640a1938f7cba612ffb9050fa`

```dockerfile
```

-	Layers:
	-	`sha256:75caba598230dbf1aa625443cfa3a6e95061b18ec6e8731f0b1cbbf3ccb50b71`  
		Last Modified: Tue, 28 Apr 2026 00:16:44 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:913196dcd3ca23ae5075a5175efd2dc8d6b3de7fcd1fb2c111b2a1c4aeba5154
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-linux` - linux; amd64

```console
$ docker pull nats@sha256:71a050049d35eba31bcb508dbbb7354f78d3c2095c5bb5607a24387cc5bc4a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6506533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8296541e734afc4b6f168616aecb56cd7168616d55b63d5eea8ed82ccb6411d6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:18 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aec33d706d05c0d0673a0501735c6856bf256195120254d0de66b2ed8487b518`  
		Last Modified: Mon, 27 Apr 2026 16:34:37 GMT  
		Size: 6.5 MB (6506024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373d31d8c613e3d8b7187644e676f86abc8ac126a61bcec845abe87615a25c60`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a4f0911609b3aed35285a1a023fdc4339cdafe40a3dc7ff4b44a32894268edf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1571b84fa4de3ebfb8bb1b52ec208f93ff9f944e01f4c39085654782dfe31e`

```dockerfile
```

-	Layers:
	-	`sha256:ac9ef0dc94f099a1d6b5159715d9b9f485407bb888d585fae78dee1fb8a0f54a`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5af32bb50db4178223e7f2ae746f250688a2ac5f8251f1b0301cc325ca2b4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff60a9c1027e6d6dac58b0b5b930c1f9e8aaa7d2258c0c0d45bfeec219b8c1c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c8f4c909fd0463d9b5b13c9f56b1811ce5523b2543f4d1e2c56b82831e5a4e9`  
		Last Modified: Mon, 27 Apr 2026 16:34:34 GMT  
		Size: 6.2 MB (6227926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad28a45d074122dc77de825b24829a158ed4144d3b089fc552c2cef59bfef6b`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:524d0da25890b35e24714c0e4475fac2f5b2cb4170e8e2d0b791117770144875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3b6f2f449e6cb4715a28621439b1003a9b7bfcfbbda49afe212518add9b86e`

```dockerfile
```

-	Layers:
	-	`sha256:ff9ac7cf2ce3006d3a49116832bfe4d8607d0e74db9c63b505ba8312143e1eb4`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:075508e648218cd7576c21cd34d51303d30c33ba7701e9277e9bc697e639d315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6217157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8342812a9880b1bba9090606591051b1205e793a55a9daa07c2b8ec69151cdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9078b87ee8498b3d94d7549f00ad3d978318f849ad8317e3929c38283f48980a`  
		Last Modified: Mon, 27 Apr 2026 16:34:36 GMT  
		Size: 6.2 MB (6216647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:3305bbef52bf5d8195e149421f737534304c6052e691b03cb4614ac028b903a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1994ac9373db777505778e0f36c5c67cdc3c48edf51c14cad1ebc1d68d54c51`

```dockerfile
```

-	Layers:
	-	`sha256:5b4d2ea9acb88f8a5b1b3f7f096762dd1f361efef8fd74687640963e88c9bc05`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ea40df8297d021756a9d6f5cce234d04424d067849d089e87b7d45e0eb0c2e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5920552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160754dbd0c1d280f89c70d023f003957b69de52f2f7a7e39f82c4c0272e2700`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1ce8862d5cf59cc1c1fc9f8534b9ad9707adb7e4ffca95852e829e0d9c6246cc`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 5.9 MB (5920042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe27b9af333eebb2c391e8c349d49dca334d0981f22eace6afe19240ac639d`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b215c14c5042de1ef395b6195ab83103c3289a103ba7b11ef7694b1b9d9b2315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133abc1576edbe5bc8fad94ae0a96e22a4f159158e05b355f465e2e20de5617a`

```dockerfile
```

-	Layers:
	-	`sha256:52e00b6d6c84eb1189627237d780fc71be9065ec2dea64361f469287e9fccfcd`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1d20b1fe94f9c2b77b8b5decb3e8f28750e7ee17b9043872a206c16712954f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dadc06aaae2240c7750e1536c5077f8de1875669e5a4ba1dddb44a22b37e0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:26 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8ceef00297aadc77f604a976e256c7afc8ad7d11975a0a70c8d18989f84c377`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 6.0 MB (5970296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92f65bc5b9eb57afda73d65184405d53b72810b4dbbf96522528f810b7db9cf`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d9a0da7986d6d545c8c60d7629ccd762270083819a8906e2d4a649b9419f0c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28237b9ce41d2c243867583d6a0264a050bf08bca473927228a653d6ce0a0ccd`

```dockerfile
```

-	Layers:
	-	`sha256:b1faceab9662f79250490806f3fea1c75a45ecc38e6df8324ff609299620af98`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:e35294278ff76bcb1fe56374110f4b06c269576ed7790035cb884905514779bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f361bf360d8325e6fcd51b413da8e62bc9d3349d5ffa47ce66c77b64b681ec30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9078b3e5e7cd72051df8071c386cbf0335d800dad99509157ffcfd8f4fc361`  
		Last Modified: Fri, 17 Apr 2026 03:00:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f7b77c54d8013e193fe1637d61d70596d15af7f467886c746e4990c02b80a60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd2c9c3f0905b48a181ecb2c54e99817e889d09b559ccb3625163e3ddb9966`

```dockerfile
```

-	Layers:
	-	`sha256:553590c07c651e9bd4871f634514aac2810de7afce20d412adc0440624524452`  
		Last Modified: Fri, 17 Apr 2026 03:00:37 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:8369f10fa05d956de0096a7a744a1b1d55175a37c2841087081423b4165fae7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:5ffa3167d5e3e3fd4258586b3e58689d9ca02a145f6b5cbc6a82f8416b7c61e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133637234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29654dc94df41eabc4fec5c6267f3e71846d39bd31cc97f52dd46404020ce98`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:52 GMT
RUN cmd /S /C #(nop) COPY file:f1ed4e18be63052ebd2a9f8f87593bf079db370ff176ea712b36dc2ac83ea376 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:54 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed04d46136c3797ba3fc4ddcaceedae8a6fc3fd40e4f77f0929591c7b645a51`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2f5a47ed51a8fd3b8ccbc37ae5b9d89766a7cd30ac5138fc1abab63a8917e`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 6.7 MB (6675280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd0b5b898034b9675ff6aa86b1a3b107c8ca3cc2788fca25c8f4f1ff65c4840`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823643c2dcd9d2a19ef822365ba3d59a932d0f663749945aec1c1fb74a7fff98`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286cfe5bab4a54ba713d5f92768b2ecfd0a029b275ba96d7b2c6dcca57056c6`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4274ef274b88859bdfe852c4c36f18d9eca26a752f7d521c3ee89749b253221`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:8369f10fa05d956de0096a7a744a1b1d55175a37c2841087081423b4165fae7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:5ffa3167d5e3e3fd4258586b3e58689d9ca02a145f6b5cbc6a82f8416b7c61e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133637234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29654dc94df41eabc4fec5c6267f3e71846d39bd31cc97f52dd46404020ce98`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:52 GMT
RUN cmd /S /C #(nop) COPY file:f1ed4e18be63052ebd2a9f8f87593bf079db370ff176ea712b36dc2ac83ea376 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:54 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed04d46136c3797ba3fc4ddcaceedae8a6fc3fd40e4f77f0929591c7b645a51`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2f5a47ed51a8fd3b8ccbc37ae5b9d89766a7cd30ac5138fc1abab63a8917e`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 6.7 MB (6675280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd0b5b898034b9675ff6aa86b1a3b107c8ca3cc2788fca25c8f4f1ff65c4840`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823643c2dcd9d2a19ef822365ba3d59a932d0f663749945aec1c1fb74a7fff98`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286cfe5bab4a54ba713d5f92768b2ecfd0a029b275ba96d7b2c6dcca57056c6`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4274ef274b88859bdfe852c4c36f18d9eca26a752f7d521c3ee89749b253221`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:913196dcd3ca23ae5075a5175efd2dc8d6b3de7fcd1fb2c111b2a1c4aeba5154
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-scratch` - linux; amd64

```console
$ docker pull nats@sha256:71a050049d35eba31bcb508dbbb7354f78d3c2095c5bb5607a24387cc5bc4a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6506533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8296541e734afc4b6f168616aecb56cd7168616d55b63d5eea8ed82ccb6411d6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:18 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aec33d706d05c0d0673a0501735c6856bf256195120254d0de66b2ed8487b518`  
		Last Modified: Mon, 27 Apr 2026 16:34:37 GMT  
		Size: 6.5 MB (6506024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373d31d8c613e3d8b7187644e676f86abc8ac126a61bcec845abe87615a25c60`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a4f0911609b3aed35285a1a023fdc4339cdafe40a3dc7ff4b44a32894268edf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1571b84fa4de3ebfb8bb1b52ec208f93ff9f944e01f4c39085654782dfe31e`

```dockerfile
```

-	Layers:
	-	`sha256:ac9ef0dc94f099a1d6b5159715d9b9f485407bb888d585fae78dee1fb8a0f54a`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5af32bb50db4178223e7f2ae746f250688a2ac5f8251f1b0301cc325ca2b4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff60a9c1027e6d6dac58b0b5b930c1f9e8aaa7d2258c0c0d45bfeec219b8c1c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c8f4c909fd0463d9b5b13c9f56b1811ce5523b2543f4d1e2c56b82831e5a4e9`  
		Last Modified: Mon, 27 Apr 2026 16:34:34 GMT  
		Size: 6.2 MB (6227926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad28a45d074122dc77de825b24829a158ed4144d3b089fc552c2cef59bfef6b`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:524d0da25890b35e24714c0e4475fac2f5b2cb4170e8e2d0b791117770144875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3b6f2f449e6cb4715a28621439b1003a9b7bfcfbbda49afe212518add9b86e`

```dockerfile
```

-	Layers:
	-	`sha256:ff9ac7cf2ce3006d3a49116832bfe4d8607d0e74db9c63b505ba8312143e1eb4`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:075508e648218cd7576c21cd34d51303d30c33ba7701e9277e9bc697e639d315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6217157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8342812a9880b1bba9090606591051b1205e793a55a9daa07c2b8ec69151cdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9078b87ee8498b3d94d7549f00ad3d978318f849ad8317e3929c38283f48980a`  
		Last Modified: Mon, 27 Apr 2026 16:34:36 GMT  
		Size: 6.2 MB (6216647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3305bbef52bf5d8195e149421f737534304c6052e691b03cb4614ac028b903a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1994ac9373db777505778e0f36c5c67cdc3c48edf51c14cad1ebc1d68d54c51`

```dockerfile
```

-	Layers:
	-	`sha256:5b4d2ea9acb88f8a5b1b3f7f096762dd1f361efef8fd74687640963e88c9bc05`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ea40df8297d021756a9d6f5cce234d04424d067849d089e87b7d45e0eb0c2e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5920552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160754dbd0c1d280f89c70d023f003957b69de52f2f7a7e39f82c4c0272e2700`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1ce8862d5cf59cc1c1fc9f8534b9ad9707adb7e4ffca95852e829e0d9c6246cc`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 5.9 MB (5920042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe27b9af333eebb2c391e8c349d49dca334d0981f22eace6afe19240ac639d`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b215c14c5042de1ef395b6195ab83103c3289a103ba7b11ef7694b1b9d9b2315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133abc1576edbe5bc8fad94ae0a96e22a4f159158e05b355f465e2e20de5617a`

```dockerfile
```

-	Layers:
	-	`sha256:52e00b6d6c84eb1189627237d780fc71be9065ec2dea64361f469287e9fccfcd`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1d20b1fe94f9c2b77b8b5decb3e8f28750e7ee17b9043872a206c16712954f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dadc06aaae2240c7750e1536c5077f8de1875669e5a4ba1dddb44a22b37e0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:26 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8ceef00297aadc77f604a976e256c7afc8ad7d11975a0a70c8d18989f84c377`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 6.0 MB (5970296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92f65bc5b9eb57afda73d65184405d53b72810b4dbbf96522528f810b7db9cf`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d9a0da7986d6d545c8c60d7629ccd762270083819a8906e2d4a649b9419f0c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28237b9ce41d2c243867583d6a0264a050bf08bca473927228a653d6ce0a0ccd`

```dockerfile
```

-	Layers:
	-	`sha256:b1faceab9662f79250490806f3fea1c75a45ecc38e6df8324ff609299620af98`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:e35294278ff76bcb1fe56374110f4b06c269576ed7790035cb884905514779bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f361bf360d8325e6fcd51b413da8e62bc9d3349d5ffa47ce66c77b64b681ec30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9078b3e5e7cd72051df8071c386cbf0335d800dad99509157ffcfd8f4fc361`  
		Last Modified: Fri, 17 Apr 2026 03:00:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f7b77c54d8013e193fe1637d61d70596d15af7f467886c746e4990c02b80a60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd2c9c3f0905b48a181ecb2c54e99817e889d09b559ccb3625163e3ddb9966`

```dockerfile
```

-	Layers:
	-	`sha256:553590c07c651e9bd4871f634514aac2810de7afce20d412adc0440624524452`  
		Last Modified: Fri, 17 Apr 2026 03:00:37 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:ee80356953306ec6fad75bab7c04975f5ccbe8ca3a0e261f3441e6613c57d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:18513bc49c5a5956ff3c90bc08b3dd1ce25ccbea36e6c833eed196162ba15069
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077766932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04438768b61ba1d4486dba86ec22b4f3972967ef3d61bd363b40fc36f0da5e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:27:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:27:41 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:27:41 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:27:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:27:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.17/nats-server-v2.11.17-windows-amd64.zip
# Tue, 28 Apr 2026 00:27:43 GMT
ENV NATS_SERVER_SHASUM=45c6a61420c87afaa31edf89372b3cfb4335ac12838fc8c593967a4d8b503f5a
# Tue, 28 Apr 2026 00:28:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:28:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:28:55 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:28:55 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:28:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:28:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa39b5520a569dcca74cc87b71474f103bd609085e86cd3a8d864b2c2eeee0f5`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f16e3219763e73943ff08622645258ae0dceb86c1f11548029542ef8c4bb6`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c5744f3bca141af630b109e9e2e6ad0f0cc3b26a88e8b639aa978e664c7391`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cc8954c56aae3cf50b57bfbee1b5a42c34bcb67fa5daaa172df290665bd6be`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b23b278723665c620bf48065b45297c89fd59c644f527a96f095a16f42ca6`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a4aef486a946e37a9891f7f0e06329bdb3eee03b6e116d0400be3515ce33f2`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d361404222ce7f8a02d1feb2fc47a604fd08de211389453544d90f2b895aa9e4`  
		Last Modified: Tue, 28 Apr 2026 00:29:03 GMT  
		Size: 498.5 KB (498491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ba63cb15569ff45ec09d133e5eb4855fdd9e8928ffcb904e40c0f17225a951`  
		Last Modified: Tue, 28 Apr 2026 00:29:06 GMT  
		Size: 7.0 MB (7043445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73db759e9cbcb5bc653d1c210aac02c7c6e386e66c88e972f0eeb18dd44295`  
		Last Modified: Tue, 28 Apr 2026 00:29:00 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958115d1e45d1edfedb763d7e3a007e163deb4e8d9321a7da226782199c964d4`  
		Last Modified: Tue, 28 Apr 2026 00:29:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7ed809f943aa373fd52f59d8e7b82e6feae266e3634ef8016c4937c50e9e5`  
		Last Modified: Tue, 28 Apr 2026 00:29:01 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b41e57bbe7114127ed66d10456ab29e89cc2b0c1edd5940c59957cf12f3738`  
		Last Modified: Tue, 28 Apr 2026 00:29:01 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:ee80356953306ec6fad75bab7c04975f5ccbe8ca3a0e261f3441e6613c57d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:18513bc49c5a5956ff3c90bc08b3dd1ce25ccbea36e6c833eed196162ba15069
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077766932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04438768b61ba1d4486dba86ec22b4f3972967ef3d61bd363b40fc36f0da5e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:27:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:27:41 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:27:41 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:27:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:27:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.17/nats-server-v2.11.17-windows-amd64.zip
# Tue, 28 Apr 2026 00:27:43 GMT
ENV NATS_SERVER_SHASUM=45c6a61420c87afaa31edf89372b3cfb4335ac12838fc8c593967a4d8b503f5a
# Tue, 28 Apr 2026 00:28:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:28:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:28:55 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:28:55 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:28:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:28:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa39b5520a569dcca74cc87b71474f103bd609085e86cd3a8d864b2c2eeee0f5`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f16e3219763e73943ff08622645258ae0dceb86c1f11548029542ef8c4bb6`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c5744f3bca141af630b109e9e2e6ad0f0cc3b26a88e8b639aa978e664c7391`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cc8954c56aae3cf50b57bfbee1b5a42c34bcb67fa5daaa172df290665bd6be`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b23b278723665c620bf48065b45297c89fd59c644f527a96f095a16f42ca6`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a4aef486a946e37a9891f7f0e06329bdb3eee03b6e116d0400be3515ce33f2`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d361404222ce7f8a02d1feb2fc47a604fd08de211389453544d90f2b895aa9e4`  
		Last Modified: Tue, 28 Apr 2026 00:29:03 GMT  
		Size: 498.5 KB (498491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ba63cb15569ff45ec09d133e5eb4855fdd9e8928ffcb904e40c0f17225a951`  
		Last Modified: Tue, 28 Apr 2026 00:29:06 GMT  
		Size: 7.0 MB (7043445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73db759e9cbcb5bc653d1c210aac02c7c6e386e66c88e972f0eeb18dd44295`  
		Last Modified: Tue, 28 Apr 2026 00:29:00 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958115d1e45d1edfedb763d7e3a007e163deb4e8d9321a7da226782199c964d4`  
		Last Modified: Tue, 28 Apr 2026 00:29:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7ed809f943aa373fd52f59d8e7b82e6feae266e3634ef8016c4937c50e9e5`  
		Last Modified: Tue, 28 Apr 2026 00:29:01 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b41e57bbe7114127ed66d10456ab29e89cc2b0c1edd5940c59957cf12f3738`  
		Last Modified: Tue, 28 Apr 2026 00:29:01 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.17`

```console
$ docker pull nats@sha256:9f9a7b0a9285b6a4e155e61d237bc208842c655b127dcddb2084d83dd9791141
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `nats:2.11.17` - linux; amd64

```console
$ docker pull nats@sha256:71a050049d35eba31bcb508dbbb7354f78d3c2095c5bb5607a24387cc5bc4a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6506533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8296541e734afc4b6f168616aecb56cd7168616d55b63d5eea8ed82ccb6411d6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:18 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aec33d706d05c0d0673a0501735c6856bf256195120254d0de66b2ed8487b518`  
		Last Modified: Mon, 27 Apr 2026 16:34:37 GMT  
		Size: 6.5 MB (6506024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373d31d8c613e3d8b7187644e676f86abc8ac126a61bcec845abe87615a25c60`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17` - unknown; unknown

```console
$ docker pull nats@sha256:a4f0911609b3aed35285a1a023fdc4339cdafe40a3dc7ff4b44a32894268edf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1571b84fa4de3ebfb8bb1b52ec208f93ff9f944e01f4c39085654782dfe31e`

```dockerfile
```

-	Layers:
	-	`sha256:ac9ef0dc94f099a1d6b5159715d9b9f485407bb888d585fae78dee1fb8a0f54a`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:5af32bb50db4178223e7f2ae746f250688a2ac5f8251f1b0301cc325ca2b4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff60a9c1027e6d6dac58b0b5b930c1f9e8aaa7d2258c0c0d45bfeec219b8c1c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c8f4c909fd0463d9b5b13c9f56b1811ce5523b2543f4d1e2c56b82831e5a4e9`  
		Last Modified: Mon, 27 Apr 2026 16:34:34 GMT  
		Size: 6.2 MB (6227926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad28a45d074122dc77de825b24829a158ed4144d3b089fc552c2cef59bfef6b`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17` - unknown; unknown

```console
$ docker pull nats@sha256:524d0da25890b35e24714c0e4475fac2f5b2cb4170e8e2d0b791117770144875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3b6f2f449e6cb4715a28621439b1003a9b7bfcfbbda49afe212518add9b86e`

```dockerfile
```

-	Layers:
	-	`sha256:ff9ac7cf2ce3006d3a49116832bfe4d8607d0e74db9c63b505ba8312143e1eb4`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:075508e648218cd7576c21cd34d51303d30c33ba7701e9277e9bc697e639d315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6217157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8342812a9880b1bba9090606591051b1205e793a55a9daa07c2b8ec69151cdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9078b87ee8498b3d94d7549f00ad3d978318f849ad8317e3929c38283f48980a`  
		Last Modified: Mon, 27 Apr 2026 16:34:36 GMT  
		Size: 6.2 MB (6216647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17` - unknown; unknown

```console
$ docker pull nats@sha256:3305bbef52bf5d8195e149421f737534304c6052e691b03cb4614ac028b903a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1994ac9373db777505778e0f36c5c67cdc3c48edf51c14cad1ebc1d68d54c51`

```dockerfile
```

-	Layers:
	-	`sha256:5b4d2ea9acb88f8a5b1b3f7f096762dd1f361efef8fd74687640963e88c9bc05`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ea40df8297d021756a9d6f5cce234d04424d067849d089e87b7d45e0eb0c2e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5920552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160754dbd0c1d280f89c70d023f003957b69de52f2f7a7e39f82c4c0272e2700`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1ce8862d5cf59cc1c1fc9f8534b9ad9707adb7e4ffca95852e829e0d9c6246cc`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 5.9 MB (5920042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe27b9af333eebb2c391e8c349d49dca334d0981f22eace6afe19240ac639d`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17` - unknown; unknown

```console
$ docker pull nats@sha256:b215c14c5042de1ef395b6195ab83103c3289a103ba7b11ef7694b1b9d9b2315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133abc1576edbe5bc8fad94ae0a96e22a4f159158e05b355f465e2e20de5617a`

```dockerfile
```

-	Layers:
	-	`sha256:52e00b6d6c84eb1189627237d780fc71be9065ec2dea64361f469287e9fccfcd`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17` - linux; ppc64le

```console
$ docker pull nats@sha256:1d20b1fe94f9c2b77b8b5decb3e8f28750e7ee17b9043872a206c16712954f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dadc06aaae2240c7750e1536c5077f8de1875669e5a4ba1dddb44a22b37e0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:26 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8ceef00297aadc77f604a976e256c7afc8ad7d11975a0a70c8d18989f84c377`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 6.0 MB (5970296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92f65bc5b9eb57afda73d65184405d53b72810b4dbbf96522528f810b7db9cf`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17` - unknown; unknown

```console
$ docker pull nats@sha256:d9a0da7986d6d545c8c60d7629ccd762270083819a8906e2d4a649b9419f0c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28237b9ce41d2c243867583d6a0264a050bf08bca473927228a653d6ce0a0ccd`

```dockerfile
```

-	Layers:
	-	`sha256:b1faceab9662f79250490806f3fea1c75a45ecc38e6df8324ff609299620af98`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.17-alpine`

```console
$ docker pull nats@sha256:e4bf19f15fd3218814a4e3c9e0064e1334bd8aa20d5984b9f1a0afd084f8cc00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.17-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a7d440bf0240e664ed74fc17c70d616e6ff4bb9890dc26f7276589daedd1e196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10769172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c7ef2d2b735068633f2dc9012ce5189e5f006096b6dad5ecff36dd3c6eb9b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6b54cbc38525fc1d30bbbb48e738ce617b74e93908bbb872cc93b73315db66`  
		Last Modified: Tue, 28 Apr 2026 00:10:50 GMT  
		Size: 7.0 MB (6960013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca157d5b7da38d0cb5255d9031d0f3c52f3303720e20cf79cbf201b80d94c0d`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be21133830b00a74c18a4947a0aafba1532fbcba6546b27d6397ff82713cafbd`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7ba2eadf86813e9a2a364a6f4670ee4418722dca64ee00be1c2e3cfc3b66077e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28b8be38c0d25f99437dc9b5790913b65d1400c46c71b1bfcac89ef301e2bbb`

```dockerfile
```

-	Layers:
	-	`sha256:218267d15d714bea6549013852c5ad8c07af7afeed21d08a62fdda53c0e98fca`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c8bada39c7f8448cdaecf39592855d589b23ace79c47c7f236ecba7d68b33aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10193817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a358738e52ffe5c541003daa6c899dc10715b9c91de1350a2673300a34aa5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:59 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:10:59 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:10:59 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e168a6db6ab9021053c1d1be43765a9182b87283ad4cf420ad7b8efbe3b24fcd`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 6.7 MB (6685465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb40f4dd56e1396a6ee32561a8ca3185283d320f12eb93885a3cabb41cf8d932`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e076015276b74b5cc31eb2cf84848ec6ff0a84e5afa62ece72ff21ca3822e7ba`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:45681bb1b26adeb0bdc0329beafef7b2f80677e0cc332f46cd6022d1e14873b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34948f0787240b55485f6d9c1c24640400b74832a0b228fac861ecf4fe1617f4`

```dockerfile
```

-	Layers:
	-	`sha256:288462c9c0469ef7dd15de311c843a0854e1af099f303c3347af7bdf1c05aa1e`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e6ca3f449ab5b378b030a47e7bbfbda9063cc722e0437c9be1ca8a6b627b0f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9901537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f3333717afc3b36a6eeb66c988f20c07f9a1eda8b03ec39280ebc45122d3fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:31 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:11:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:11:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad226131af5a49e8e5da1ddd881df2b35b10a7a3e12cde83b27a966e8259d930`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 6.7 MB (6674737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56bba8fd3f5f27de4228f8a29adfba16bd15df9fb46a2726c72c7afc8375828`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a46cc9867199da12df2ff8f366aad6030fc73c8376f3d00cdb2ee39164c9ae`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1dc353c67460bbb8a1e5b156837bb144f999a524ed85d5852e6aee82b3b63fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d972ca3d35d3ca43407bdb4fe5ae1002f438e6347dc4eb7705426a06f7f9c1f4`

```dockerfile
```

-	Layers:
	-	`sha256:a83bc6829540b6b2bc2bebf85423ffca9bdcac4b9f25e9f973fa095baf131b26`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:69fa60167708111e9318f327bb7b3609ad9d4d3e7a0d16243231c5a6e9a8fb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7f87c86557a749c3b414af53a0a5ac4f3a8a3bd94a4c5395f28071fad8289a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:17 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:11:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:11:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767309eebe99876fafbf4a9ef30dac5fd062c98907a979c91301cadd8419a8e`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 6.4 MB (6382369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e279c81670829f705cb5d56a31edfd682dc3e6867db2f0744613a2c3c8141`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fddd138a70823c87b6d9a5835c6d164301d59c457b5ace8b4d09178e10570e`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c354d41ddf541af425a5daf4d02f00611d60b964ef8a2138077c7ecba39fd48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29aa5190dd4a144cac18e09c2145e7c2b133b2513e4fbcb4aa955f972281c51`

```dockerfile
```

-	Layers:
	-	`sha256:24580254badc6cc0410a9ceda2b19ee728de9bdea1749c24921888a7983b4d79`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:c81b5302d3988d6fa2c166ccf2340164a9ce9bd76f468180a0038c063e9c3d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10168040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb3d41b4064e711a4fbe5d12883d3f4eb16f072908619352ef59331bd52baf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3fd852d0afd5e21d494d8333dc133779914e56c90f51f200586eb0ecac28ee`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.4 MB (6430411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0568b8daea5a9bf497889271f07cda84b490fd3b16a1da88b0cb11f028e42da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3166e2d4947db30db38aa4ecb26aca06d282daaa111b14be944c9cce3043dc3d`

```dockerfile
```

-	Layers:
	-	`sha256:4e9be753004a392414cda36251748f3ef58bdb58d883ecc3ce43c603a04a447e`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-alpine` - linux; s390x

```console
$ docker pull nats@sha256:b91caeb3114b6318269374969d3ef1d3007ad1ff6d415b2459895b86041c3c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714f4e2e84044a1be752471a916485a584d46e02f070cac266029247a8186946`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:01 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:16:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:16:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d782e28ffadbebd6def10357cfd2f31431bd0fb84bdee0592406e8f18656094`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.8 MB (6803883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2285ded99cc9a628d98575421a3d519dedd90b80c572a82911bcbd49ce89fed5`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128fd32596802807b84459b2b3dc2a91dd083261a2da76168fbd385bfd5f9dab`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4d5bc00030f9b8e9cc663d67e992c46b73b9a5f7b53e26f7ae6936e8932f4b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fbdaf743cac00badea79267ceb4a58b85839e640a1938f7cba612ffb9050fa`

```dockerfile
```

-	Layers:
	-	`sha256:75caba598230dbf1aa625443cfa3a6e95061b18ec6e8731f0b1cbbf3ccb50b71`  
		Last Modified: Tue, 28 Apr 2026 00:16:44 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.17-alpine3.22`

```console
$ docker pull nats@sha256:e4bf19f15fd3218814a4e3c9e0064e1334bd8aa20d5984b9f1a0afd084f8cc00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.17-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:a7d440bf0240e664ed74fc17c70d616e6ff4bb9890dc26f7276589daedd1e196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10769172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c7ef2d2b735068633f2dc9012ce5189e5f006096b6dad5ecff36dd3c6eb9b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6b54cbc38525fc1d30bbbb48e738ce617b74e93908bbb872cc93b73315db66`  
		Last Modified: Tue, 28 Apr 2026 00:10:50 GMT  
		Size: 7.0 MB (6960013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca157d5b7da38d0cb5255d9031d0f3c52f3303720e20cf79cbf201b80d94c0d`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be21133830b00a74c18a4947a0aafba1532fbcba6546b27d6397ff82713cafbd`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7ba2eadf86813e9a2a364a6f4670ee4418722dca64ee00be1c2e3cfc3b66077e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28b8be38c0d25f99437dc9b5790913b65d1400c46c71b1bfcac89ef301e2bbb`

```dockerfile
```

-	Layers:
	-	`sha256:218267d15d714bea6549013852c5ad8c07af7afeed21d08a62fdda53c0e98fca`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:c8bada39c7f8448cdaecf39592855d589b23ace79c47c7f236ecba7d68b33aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10193817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a358738e52ffe5c541003daa6c899dc10715b9c91de1350a2673300a34aa5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:59 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:10:59 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:10:59 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e168a6db6ab9021053c1d1be43765a9182b87283ad4cf420ad7b8efbe3b24fcd`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 6.7 MB (6685465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb40f4dd56e1396a6ee32561a8ca3185283d320f12eb93885a3cabb41cf8d932`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e076015276b74b5cc31eb2cf84848ec6ff0a84e5afa62ece72ff21ca3822e7ba`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:45681bb1b26adeb0bdc0329beafef7b2f80677e0cc332f46cd6022d1e14873b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34948f0787240b55485f6d9c1c24640400b74832a0b228fac861ecf4fe1617f4`

```dockerfile
```

-	Layers:
	-	`sha256:288462c9c0469ef7dd15de311c843a0854e1af099f303c3347af7bdf1c05aa1e`  
		Last Modified: Tue, 28 Apr 2026 00:11:03 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:e6ca3f449ab5b378b030a47e7bbfbda9063cc722e0437c9be1ca8a6b627b0f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9901537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f3333717afc3b36a6eeb66c988f20c07f9a1eda8b03ec39280ebc45122d3fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:31 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:11:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:11:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad226131af5a49e8e5da1ddd881df2b35b10a7a3e12cde83b27a966e8259d930`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 6.7 MB (6674737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56bba8fd3f5f27de4228f8a29adfba16bd15df9fb46a2726c72c7afc8375828`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a46cc9867199da12df2ff8f366aad6030fc73c8376f3d00cdb2ee39164c9ae`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1dc353c67460bbb8a1e5b156837bb144f999a524ed85d5852e6aee82b3b63fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d972ca3d35d3ca43407bdb4fe5ae1002f438e6347dc4eb7705426a06f7f9c1f4`

```dockerfile
```

-	Layers:
	-	`sha256:a83bc6829540b6b2bc2bebf85423ffca9bdcac4b9f25e9f973fa095baf131b26`  
		Last Modified: Tue, 28 Apr 2026 00:11:35 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:69fa60167708111e9318f327bb7b3609ad9d4d3e7a0d16243231c5a6e9a8fb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7f87c86557a749c3b414af53a0a5ac4f3a8a3bd94a4c5395f28071fad8289a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:17 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:11:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:11:17 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6767309eebe99876fafbf4a9ef30dac5fd062c98907a979c91301cadd8419a8e`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 6.4 MB (6382369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e279c81670829f705cb5d56a31edfd682dc3e6867db2f0744613a2c3c8141`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fddd138a70823c87b6d9a5835c6d164301d59c457b5ace8b4d09178e10570e`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c354d41ddf541af425a5daf4d02f00611d60b964ef8a2138077c7ecba39fd48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29aa5190dd4a144cac18e09c2145e7c2b133b2513e4fbcb4aa955f972281c51`

```dockerfile
```

-	Layers:
	-	`sha256:24580254badc6cc0410a9ceda2b19ee728de9bdea1749c24921888a7983b4d79`  
		Last Modified: Tue, 28 Apr 2026 00:11:22 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:c81b5302d3988d6fa2c166ccf2340164a9ce9bd76f468180a0038c063e9c3d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10168040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb3d41b4064e711a4fbe5d12883d3f4eb16f072908619352ef59331bd52baf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3fd852d0afd5e21d494d8333dc133779914e56c90f51f200586eb0ecac28ee`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.4 MB (6430411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:0568b8daea5a9bf497889271f07cda84b490fd3b16a1da88b0cb11f028e42da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3166e2d4947db30db38aa4ecb26aca06d282daaa111b14be944c9cce3043dc3d`

```dockerfile
```

-	Layers:
	-	`sha256:4e9be753004a392414cda36251748f3ef58bdb58d883ecc3ce43c603a04a447e`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:b91caeb3114b6318269374969d3ef1d3007ad1ff6d415b2459895b86041c3c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10458728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714f4e2e84044a1be752471a916485a584d46e02f070cac266029247a8186946`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:01 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:16:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:16:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d21df24f262f34f8bf6d1f0bca557c08429e433fd9f60f6983105539ae517feb' ;;     armhf) natsArch='arm6'; sha256='13e090f2f433d31f1408543ef52204108eb1fcee4ac74b839a3f2f0b72aceade' ;;     armv7) natsArch='arm7'; sha256='5c1f445095ea9a455d6dd092967d20dd38c6bc8c4da13d108e7d3a1386ca3c7d' ;;     x86_64) natsArch='amd64'; sha256='ad608dd0ea8bbfa58c40e3b8f58ed67478eec26166ec49c502db8d17589b51b5' ;;     x86) natsArch='386'; sha256='6bfe7637dd61b9386074294c37c0790061feb39fd5198c34f9d1882c94926d5d' ;;     s390x) natsArch='s390x'; sha256='4e19f27f2ee5f2fe9a5480d6b4541b63f58934524c14b839b2d4d32459ca91bc' ;;     ppc64le) natsArch='ppc64le'; sha256='822e7a6ab51dca0cda69a3dc274ecf058f4502265984d09d9b45ab13b749a4f3' ;;     loong64) natsArch='loong64'; sha256='c410deb61bcad2e39739e4cc4d2a7d8cd84bb17d655d4a1e97a92c98cd309e6f' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d782e28ffadbebd6def10357cfd2f31431bd0fb84bdee0592406e8f18656094`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.8 MB (6803883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2285ded99cc9a628d98575421a3d519dedd90b80c572a82911bcbd49ce89fed5`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128fd32596802807b84459b2b3dc2a91dd083261a2da76168fbd385bfd5f9dab`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4d5bc00030f9b8e9cc663d67e992c46b73b9a5f7b53e26f7ae6936e8932f4b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fbdaf743cac00badea79267ceb4a58b85839e640a1938f7cba612ffb9050fa`

```dockerfile
```

-	Layers:
	-	`sha256:75caba598230dbf1aa625443cfa3a6e95061b18ec6e8731f0b1cbbf3ccb50b71`  
		Last Modified: Tue, 28 Apr 2026 00:16:44 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.17-linux`

```console
$ docker pull nats@sha256:9f9a7b0a9285b6a4e155e61d237bc208842c655b127dcddb2084d83dd9791141
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `nats:2.11.17-linux` - linux; amd64

```console
$ docker pull nats@sha256:71a050049d35eba31bcb508dbbb7354f78d3c2095c5bb5607a24387cc5bc4a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6506533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8296541e734afc4b6f168616aecb56cd7168616d55b63d5eea8ed82ccb6411d6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:18 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aec33d706d05c0d0673a0501735c6856bf256195120254d0de66b2ed8487b518`  
		Last Modified: Mon, 27 Apr 2026 16:34:37 GMT  
		Size: 6.5 MB (6506024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373d31d8c613e3d8b7187644e676f86abc8ac126a61bcec845abe87615a25c60`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a4f0911609b3aed35285a1a023fdc4339cdafe40a3dc7ff4b44a32894268edf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1571b84fa4de3ebfb8bb1b52ec208f93ff9f944e01f4c39085654782dfe31e`

```dockerfile
```

-	Layers:
	-	`sha256:ac9ef0dc94f099a1d6b5159715d9b9f485407bb888d585fae78dee1fb8a0f54a`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:5af32bb50db4178223e7f2ae746f250688a2ac5f8251f1b0301cc325ca2b4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff60a9c1027e6d6dac58b0b5b930c1f9e8aaa7d2258c0c0d45bfeec219b8c1c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c8f4c909fd0463d9b5b13c9f56b1811ce5523b2543f4d1e2c56b82831e5a4e9`  
		Last Modified: Mon, 27 Apr 2026 16:34:34 GMT  
		Size: 6.2 MB (6227926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad28a45d074122dc77de825b24829a158ed4144d3b089fc552c2cef59bfef6b`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-linux` - unknown; unknown

```console
$ docker pull nats@sha256:524d0da25890b35e24714c0e4475fac2f5b2cb4170e8e2d0b791117770144875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3b6f2f449e6cb4715a28621439b1003a9b7bfcfbbda49afe212518add9b86e`

```dockerfile
```

-	Layers:
	-	`sha256:ff9ac7cf2ce3006d3a49116832bfe4d8607d0e74db9c63b505ba8312143e1eb4`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:075508e648218cd7576c21cd34d51303d30c33ba7701e9277e9bc697e639d315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6217157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8342812a9880b1bba9090606591051b1205e793a55a9daa07c2b8ec69151cdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9078b87ee8498b3d94d7549f00ad3d978318f849ad8317e3929c38283f48980a`  
		Last Modified: Mon, 27 Apr 2026 16:34:36 GMT  
		Size: 6.2 MB (6216647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-linux` - unknown; unknown

```console
$ docker pull nats@sha256:3305bbef52bf5d8195e149421f737534304c6052e691b03cb4614ac028b903a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1994ac9373db777505778e0f36c5c67cdc3c48edf51c14cad1ebc1d68d54c51`

```dockerfile
```

-	Layers:
	-	`sha256:5b4d2ea9acb88f8a5b1b3f7f096762dd1f361efef8fd74687640963e88c9bc05`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ea40df8297d021756a9d6f5cce234d04424d067849d089e87b7d45e0eb0c2e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5920552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160754dbd0c1d280f89c70d023f003957b69de52f2f7a7e39f82c4c0272e2700`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1ce8862d5cf59cc1c1fc9f8534b9ad9707adb7e4ffca95852e829e0d9c6246cc`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 5.9 MB (5920042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe27b9af333eebb2c391e8c349d49dca334d0981f22eace6afe19240ac639d`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b215c14c5042de1ef395b6195ab83103c3289a103ba7b11ef7694b1b9d9b2315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133abc1576edbe5bc8fad94ae0a96e22a4f159158e05b355f465e2e20de5617a`

```dockerfile
```

-	Layers:
	-	`sha256:52e00b6d6c84eb1189627237d780fc71be9065ec2dea64361f469287e9fccfcd`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1d20b1fe94f9c2b77b8b5decb3e8f28750e7ee17b9043872a206c16712954f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dadc06aaae2240c7750e1536c5077f8de1875669e5a4ba1dddb44a22b37e0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:26 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8ceef00297aadc77f604a976e256c7afc8ad7d11975a0a70c8d18989f84c377`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 6.0 MB (5970296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92f65bc5b9eb57afda73d65184405d53b72810b4dbbf96522528f810b7db9cf`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d9a0da7986d6d545c8c60d7629ccd762270083819a8906e2d4a649b9419f0c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28237b9ce41d2c243867583d6a0264a050bf08bca473927228a653d6ce0a0ccd`

```dockerfile
```

-	Layers:
	-	`sha256:b1faceab9662f79250490806f3fea1c75a45ecc38e6df8324ff609299620af98`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.17-nanoserver`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.11.17-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.11.17-scratch`

```console
$ docker pull nats@sha256:9f9a7b0a9285b6a4e155e61d237bc208842c655b127dcddb2084d83dd9791141
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `nats:2.11.17-scratch` - linux; amd64

```console
$ docker pull nats@sha256:71a050049d35eba31bcb508dbbb7354f78d3c2095c5bb5607a24387cc5bc4a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6506533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8296541e734afc4b6f168616aecb56cd7168616d55b63d5eea8ed82ccb6411d6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:17 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:18 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aec33d706d05c0d0673a0501735c6856bf256195120254d0de66b2ed8487b518`  
		Last Modified: Mon, 27 Apr 2026 16:34:37 GMT  
		Size: 6.5 MB (6506024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373d31d8c613e3d8b7187644e676f86abc8ac126a61bcec845abe87615a25c60`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a4f0911609b3aed35285a1a023fdc4339cdafe40a3dc7ff4b44a32894268edf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1571b84fa4de3ebfb8bb1b52ec208f93ff9f944e01f4c39085654782dfe31e`

```dockerfile
```

-	Layers:
	-	`sha256:ac9ef0dc94f099a1d6b5159715d9b9f485407bb888d585fae78dee1fb8a0f54a`  
		Last Modified: Tue, 28 Apr 2026 00:16:22 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:5af32bb50db4178223e7f2ae746f250688a2ac5f8251f1b0301cc325ca2b4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff60a9c1027e6d6dac58b0b5b930c1f9e8aaa7d2258c0c0d45bfeec219b8c1c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:41 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c8f4c909fd0463d9b5b13c9f56b1811ce5523b2543f4d1e2c56b82831e5a4e9`  
		Last Modified: Mon, 27 Apr 2026 16:34:34 GMT  
		Size: 6.2 MB (6227926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad28a45d074122dc77de825b24829a158ed4144d3b089fc552c2cef59bfef6b`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:524d0da25890b35e24714c0e4475fac2f5b2cb4170e8e2d0b791117770144875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3b6f2f449e6cb4715a28621439b1003a9b7bfcfbbda49afe212518add9b86e`

```dockerfile
```

-	Layers:
	-	`sha256:ff9ac7cf2ce3006d3a49116832bfe4d8607d0e74db9c63b505ba8312143e1eb4`  
		Last Modified: Tue, 28 Apr 2026 00:16:45 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:075508e648218cd7576c21cd34d51303d30c33ba7701e9277e9bc697e639d315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6217157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8342812a9880b1bba9090606591051b1205e793a55a9daa07c2b8ec69151cdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9078b87ee8498b3d94d7549f00ad3d978318f849ad8317e3929c38283f48980a`  
		Last Modified: Mon, 27 Apr 2026 16:34:36 GMT  
		Size: 6.2 MB (6216647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3305bbef52bf5d8195e149421f737534304c6052e691b03cb4614ac028b903a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1994ac9373db777505778e0f36c5c67cdc3c48edf51c14cad1ebc1d68d54c51`

```dockerfile
```

-	Layers:
	-	`sha256:5b4d2ea9acb88f8a5b1b3f7f096762dd1f361efef8fd74687640963e88c9bc05`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ea40df8297d021756a9d6f5cce234d04424d067849d089e87b7d45e0eb0c2e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5920552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160754dbd0c1d280f89c70d023f003957b69de52f2f7a7e39f82c4c0272e2700`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1ce8862d5cf59cc1c1fc9f8534b9ad9707adb7e4ffca95852e829e0d9c6246cc`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 5.9 MB (5920042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe27b9af333eebb2c391e8c349d49dca334d0981f22eace6afe19240ac639d`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b215c14c5042de1ef395b6195ab83103c3289a103ba7b11ef7694b1b9d9b2315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133abc1576edbe5bc8fad94ae0a96e22a4f159158e05b355f465e2e20de5617a`

```dockerfile
```

-	Layers:
	-	`sha256:52e00b6d6c84eb1189627237d780fc71be9065ec2dea64361f469287e9fccfcd`  
		Last Modified: Tue, 28 Apr 2026 00:16:18 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.17-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1d20b1fe94f9c2b77b8b5decb3e8f28750e7ee17b9043872a206c16712954f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dadc06aaae2240c7750e1536c5077f8de1875669e5a4ba1dddb44a22b37e0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:26 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:26 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:26 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8ceef00297aadc77f604a976e256c7afc8ad7d11975a0a70c8d18989f84c377`  
		Last Modified: Mon, 27 Apr 2026 16:34:33 GMT  
		Size: 6.0 MB (5970296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92f65bc5b9eb57afda73d65184405d53b72810b4dbbf96522528f810b7db9cf`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.17-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d9a0da7986d6d545c8c60d7629ccd762270083819a8906e2d4a649b9419f0c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28237b9ce41d2c243867583d6a0264a050bf08bca473927228a653d6ce0a0ccd`

```dockerfile
```

-	Layers:
	-	`sha256:b1faceab9662f79250490806f3fea1c75a45ecc38e6df8324ff609299620af98`  
		Last Modified: Tue, 28 Apr 2026 00:16:32 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.17-windowsservercore`

```console
$ docker pull nats@sha256:ee80356953306ec6fad75bab7c04975f5ccbe8ca3a0e261f3441e6613c57d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11.17-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:18513bc49c5a5956ff3c90bc08b3dd1ce25ccbea36e6c833eed196162ba15069
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077766932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04438768b61ba1d4486dba86ec22b4f3972967ef3d61bd363b40fc36f0da5e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:27:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:27:41 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:27:41 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:27:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:27:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.17/nats-server-v2.11.17-windows-amd64.zip
# Tue, 28 Apr 2026 00:27:43 GMT
ENV NATS_SERVER_SHASUM=45c6a61420c87afaa31edf89372b3cfb4335ac12838fc8c593967a4d8b503f5a
# Tue, 28 Apr 2026 00:28:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:28:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:28:55 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:28:55 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:28:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:28:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa39b5520a569dcca74cc87b71474f103bd609085e86cd3a8d864b2c2eeee0f5`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f16e3219763e73943ff08622645258ae0dceb86c1f11548029542ef8c4bb6`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c5744f3bca141af630b109e9e2e6ad0f0cc3b26a88e8b639aa978e664c7391`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cc8954c56aae3cf50b57bfbee1b5a42c34bcb67fa5daaa172df290665bd6be`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b23b278723665c620bf48065b45297c89fd59c644f527a96f095a16f42ca6`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a4aef486a946e37a9891f7f0e06329bdb3eee03b6e116d0400be3515ce33f2`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d361404222ce7f8a02d1feb2fc47a604fd08de211389453544d90f2b895aa9e4`  
		Last Modified: Tue, 28 Apr 2026 00:29:03 GMT  
		Size: 498.5 KB (498491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ba63cb15569ff45ec09d133e5eb4855fdd9e8928ffcb904e40c0f17225a951`  
		Last Modified: Tue, 28 Apr 2026 00:29:06 GMT  
		Size: 7.0 MB (7043445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73db759e9cbcb5bc653d1c210aac02c7c6e386e66c88e972f0eeb18dd44295`  
		Last Modified: Tue, 28 Apr 2026 00:29:00 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958115d1e45d1edfedb763d7e3a007e163deb4e8d9321a7da226782199c964d4`  
		Last Modified: Tue, 28 Apr 2026 00:29:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7ed809f943aa373fd52f59d8e7b82e6feae266e3634ef8016c4937c50e9e5`  
		Last Modified: Tue, 28 Apr 2026 00:29:01 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b41e57bbe7114127ed66d10456ab29e89cc2b0c1edd5940c59957cf12f3738`  
		Last Modified: Tue, 28 Apr 2026 00:29:01 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.17-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:ee80356953306ec6fad75bab7c04975f5ccbe8ca3a0e261f3441e6613c57d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11.17-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:18513bc49c5a5956ff3c90bc08b3dd1ce25ccbea36e6c833eed196162ba15069
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077766932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04438768b61ba1d4486dba86ec22b4f3972967ef3d61bd363b40fc36f0da5e0c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:27:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:27:41 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:27:41 GMT
ENV NATS_SERVER=2.11.17
# Tue, 28 Apr 2026 00:27:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.17
# Tue, 28 Apr 2026 00:27:42 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.17/nats-server-v2.11.17-windows-amd64.zip
# Tue, 28 Apr 2026 00:27:43 GMT
ENV NATS_SERVER_SHASUM=45c6a61420c87afaa31edf89372b3cfb4335ac12838fc8c593967a4d8b503f5a
# Tue, 28 Apr 2026 00:28:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:28:54 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:28:55 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:28:55 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:28:56 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:28:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa39b5520a569dcca74cc87b71474f103bd609085e86cd3a8d864b2c2eeee0f5`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f16e3219763e73943ff08622645258ae0dceb86c1f11548029542ef8c4bb6`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c5744f3bca141af630b109e9e2e6ad0f0cc3b26a88e8b639aa978e664c7391`  
		Last Modified: Tue, 28 Apr 2026 00:29:04 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cc8954c56aae3cf50b57bfbee1b5a42c34bcb67fa5daaa172df290665bd6be`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6b23b278723665c620bf48065b45297c89fd59c644f527a96f095a16f42ca6`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a4aef486a946e37a9891f7f0e06329bdb3eee03b6e116d0400be3515ce33f2`  
		Last Modified: Tue, 28 Apr 2026 00:29:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d361404222ce7f8a02d1feb2fc47a604fd08de211389453544d90f2b895aa9e4`  
		Last Modified: Tue, 28 Apr 2026 00:29:03 GMT  
		Size: 498.5 KB (498491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ba63cb15569ff45ec09d133e5eb4855fdd9e8928ffcb904e40c0f17225a951`  
		Last Modified: Tue, 28 Apr 2026 00:29:06 GMT  
		Size: 7.0 MB (7043445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73db759e9cbcb5bc653d1c210aac02c7c6e386e66c88e972f0eeb18dd44295`  
		Last Modified: Tue, 28 Apr 2026 00:29:00 GMT  
		Size: 1.9 KB (1864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958115d1e45d1edfedb763d7e3a007e163deb4e8d9321a7da226782199c964d4`  
		Last Modified: Tue, 28 Apr 2026 00:29:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7ed809f943aa373fd52f59d8e7b82e6feae266e3634ef8016c4937c50e9e5`  
		Last Modified: Tue, 28 Apr 2026 00:29:01 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b41e57bbe7114127ed66d10456ab29e89cc2b0c1edd5940c59957cf12f3738`  
		Last Modified: Tue, 28 Apr 2026 00:29:01 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12`

```console
$ docker pull nats@sha256:5c5ae59dd58fe77318be7ae31b5a18a1730c6ca2c2fd94572d0ee5a81e0c9234
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-alpine`

```console
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:fd5dd09bc60658223075241956f5c1a12ee7b7899258b2a481aad6782476b747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-linux` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-nanoserver`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-scratch`

```console
$ docker pull nats@sha256:fd5dd09bc60658223075241956f5c1a12ee7b7899258b2a481aad6782476b747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-scratch` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-windowsservercore`

```console
$ docker pull nats@sha256:7be687bd0fcf28c0ff569af5d07b5586400ddc2e656ed5059fa069a1861d5310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:513908e15de358856596ba7150e84b831f6f711b57c69bff1dab9e0f2334ccc1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5993871186ecfe774a9cf8a2b3de0621e6afaf3fd93f99cbbaff6fffc782a8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:22:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:22:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:22:21 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:22:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:22:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 28 Apr 2026 00:22:24 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 28 Apr 2026 00:23:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:24:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:24:04 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:24:05 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:24:05 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:24:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ffdad23a2259ee9605b07af3b8756afac669d72d7f4df289af5e1bfa765df`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349750824325190c58f7211d2a32fac8867324987e4912f6187dc9d6f9fb4ae8`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e65ce208cc089d5d84714aa1b4c702e6514a37bc1a25a9e317e5484c4b6770`  
		Last Modified: Tue, 28 Apr 2026 00:24:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fefac29241015b39520060d922c7fb6054787dd9dd417b2cabd03743d7bda5f`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe557d93a73db69714369a258c20de37e40d04268b2f4804c92e12e16976bdd`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3130aba43c6a9d55589835a86638de2d3125fa2366b684015a8ac9fc1c818d`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19f58f4c90bd0a1c10a151c0165e6d1660f82cb62c97e4a3e1ec5be69c14d0`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 507.2 KB (507220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b029516bfa850bb0dc8d626d1e3a9cda785c0b6ff3e1ac8797afb2adf5f0ed3`  
		Last Modified: Tue, 28 Apr 2026 00:24:15 GMT  
		Size: 7.2 MB (7178445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8a07055de8fc46e4e8f02f1a81c1872033e0a3dda665ba7f3a7cdba7cd203`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2e16a4341e7b5618098955dbd5110c7fc4e24810d6e25bb7cd53e768b4539`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a737b9ff5aae65f741d22ddd5e6e1c210d6f45528f4778fcb53b923c0e903`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbeaf674140e140a6e0cb9b0b83df4612f9ab45bc55e9507b8d32bb2be05e1`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:7be687bd0fcf28c0ff569af5d07b5586400ddc2e656ed5059fa069a1861d5310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:513908e15de358856596ba7150e84b831f6f711b57c69bff1dab9e0f2334ccc1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5993871186ecfe774a9cf8a2b3de0621e6afaf3fd93f99cbbaff6fffc782a8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:22:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:22:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:22:21 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:22:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:22:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 28 Apr 2026 00:22:24 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 28 Apr 2026 00:23:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:24:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:24:04 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:24:05 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:24:05 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:24:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ffdad23a2259ee9605b07af3b8756afac669d72d7f4df289af5e1bfa765df`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349750824325190c58f7211d2a32fac8867324987e4912f6187dc9d6f9fb4ae8`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e65ce208cc089d5d84714aa1b4c702e6514a37bc1a25a9e317e5484c4b6770`  
		Last Modified: Tue, 28 Apr 2026 00:24:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fefac29241015b39520060d922c7fb6054787dd9dd417b2cabd03743d7bda5f`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe557d93a73db69714369a258c20de37e40d04268b2f4804c92e12e16976bdd`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3130aba43c6a9d55589835a86638de2d3125fa2366b684015a8ac9fc1c818d`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19f58f4c90bd0a1c10a151c0165e6d1660f82cb62c97e4a3e1ec5be69c14d0`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 507.2 KB (507220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b029516bfa850bb0dc8d626d1e3a9cda785c0b6ff3e1ac8797afb2adf5f0ed3`  
		Last Modified: Tue, 28 Apr 2026 00:24:15 GMT  
		Size: 7.2 MB (7178445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8a07055de8fc46e4e8f02f1a81c1872033e0a3dda665ba7f3a7cdba7cd203`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2e16a4341e7b5618098955dbd5110c7fc4e24810d6e25bb7cd53e768b4539`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a737b9ff5aae65f741d22ddd5e6e1c210d6f45528f4778fcb53b923c0e903`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbeaf674140e140a6e0cb9b0b83df4612f9ab45bc55e9507b8d32bb2be05e1`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.8`

```console
$ docker pull nats@sha256:0513276baf942cbb6b1dbb1fd9a50aa1f9bb0c62058b59e961e18023b9a1a2d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `nats:2.12.8` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.8-alpine`

```console
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12.8-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-alpine` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.8-alpine3.22`

```console
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12.8-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.8-linux`

```console
$ docker pull nats@sha256:0513276baf942cbb6b1dbb1fd9a50aa1f9bb0c62058b59e961e18023b9a1a2d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `nats:2.12.8-linux` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-linux` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-linux` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-linux` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-linux` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.8-nanoserver`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.8-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.8-scratch`

```console
$ docker pull nats@sha256:0513276baf942cbb6b1dbb1fd9a50aa1f9bb0c62058b59e961e18023b9a1a2d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `nats:2.12.8-scratch` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.8-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.8-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.8-windowsservercore`

```console
$ docker pull nats@sha256:7be687bd0fcf28c0ff569af5d07b5586400ddc2e656ed5059fa069a1861d5310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12.8-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:513908e15de358856596ba7150e84b831f6f711b57c69bff1dab9e0f2334ccc1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5993871186ecfe774a9cf8a2b3de0621e6afaf3fd93f99cbbaff6fffc782a8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:22:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:22:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:22:21 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:22:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:22:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 28 Apr 2026 00:22:24 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 28 Apr 2026 00:23:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:24:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:24:04 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:24:05 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:24:05 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:24:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ffdad23a2259ee9605b07af3b8756afac669d72d7f4df289af5e1bfa765df`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349750824325190c58f7211d2a32fac8867324987e4912f6187dc9d6f9fb4ae8`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e65ce208cc089d5d84714aa1b4c702e6514a37bc1a25a9e317e5484c4b6770`  
		Last Modified: Tue, 28 Apr 2026 00:24:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fefac29241015b39520060d922c7fb6054787dd9dd417b2cabd03743d7bda5f`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe557d93a73db69714369a258c20de37e40d04268b2f4804c92e12e16976bdd`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3130aba43c6a9d55589835a86638de2d3125fa2366b684015a8ac9fc1c818d`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19f58f4c90bd0a1c10a151c0165e6d1660f82cb62c97e4a3e1ec5be69c14d0`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 507.2 KB (507220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b029516bfa850bb0dc8d626d1e3a9cda785c0b6ff3e1ac8797afb2adf5f0ed3`  
		Last Modified: Tue, 28 Apr 2026 00:24:15 GMT  
		Size: 7.2 MB (7178445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8a07055de8fc46e4e8f02f1a81c1872033e0a3dda665ba7f3a7cdba7cd203`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2e16a4341e7b5618098955dbd5110c7fc4e24810d6e25bb7cd53e768b4539`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a737b9ff5aae65f741d22ddd5e6e1c210d6f45528f4778fcb53b923c0e903`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbeaf674140e140a6e0cb9b0b83df4612f9ab45bc55e9507b8d32bb2be05e1`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.8-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:7be687bd0fcf28c0ff569af5d07b5586400ddc2e656ed5059fa069a1861d5310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12.8-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:513908e15de358856596ba7150e84b831f6f711b57c69bff1dab9e0f2334ccc1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5993871186ecfe774a9cf8a2b3de0621e6afaf3fd93f99cbbaff6fffc782a8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:22:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:22:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:22:21 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:22:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:22:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 28 Apr 2026 00:22:24 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 28 Apr 2026 00:23:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:24:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:24:04 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:24:05 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:24:05 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:24:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ffdad23a2259ee9605b07af3b8756afac669d72d7f4df289af5e1bfa765df`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349750824325190c58f7211d2a32fac8867324987e4912f6187dc9d6f9fb4ae8`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e65ce208cc089d5d84714aa1b4c702e6514a37bc1a25a9e317e5484c4b6770`  
		Last Modified: Tue, 28 Apr 2026 00:24:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fefac29241015b39520060d922c7fb6054787dd9dd417b2cabd03743d7bda5f`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe557d93a73db69714369a258c20de37e40d04268b2f4804c92e12e16976bdd`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3130aba43c6a9d55589835a86638de2d3125fa2366b684015a8ac9fc1c818d`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19f58f4c90bd0a1c10a151c0165e6d1660f82cb62c97e4a3e1ec5be69c14d0`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 507.2 KB (507220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b029516bfa850bb0dc8d626d1e3a9cda785c0b6ff3e1ac8797afb2adf5f0ed3`  
		Last Modified: Tue, 28 Apr 2026 00:24:15 GMT  
		Size: 7.2 MB (7178445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8a07055de8fc46e4e8f02f1a81c1872033e0a3dda665ba7f3a7cdba7cd203`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2e16a4341e7b5618098955dbd5110c7fc4e24810d6e25bb7cd53e768b4539`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a737b9ff5aae65f741d22ddd5e6e1c210d6f45528f4778fcb53b923c0e903`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbeaf674140e140a6e0cb9b0b83df4612f9ab45bc55e9507b8d32bb2be05e1`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:6b2156f7491cdeddfa8b7ca15cd6fd59b9cabadec5019e933c65c01cf82b1c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:d11cbec9afb91f27adb44a1e36c74b6ae59a674258531cb045acba39730d53b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10920773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27082b56ef0e728c0b25055b2a8297d49f499bbf5df5d491272af38a7c44cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:10:45 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:10:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:10:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a74686f11568e98d1e391b903678ee618b9a39aa5ceaa255da2a7ff23ed7c`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 7.1 MB (7111614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ed50c18d13cc5345f43115a144cb1c8b81b8372631c87bf8d7dc83cdea031b`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5afa1e4cafbcd5b1672cb7a8effb2e2a63673c56c1f6b57f4a4cac7830b8d9`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f072e0c0cb980ba295d6d09ffab0720392b9051fbc587df9d3a1546baa020b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762e2789ffcec0a32eec4d90db5348f0a420b61c14b288991a8ce5988c0f005`

```dockerfile
```

-	Layers:
	-	`sha256:3a11e1b7b0fe61acdca91af7d67d2bfa36475246e9ee47e374f181f6d774a204`  
		Last Modified: Tue, 28 Apr 2026 00:10:49 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:de64f8fbea0904878bf0709cb3115130600bd3fb8c8775d8b5a6556be0a6cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3186438c73a75ded34b50aba9a315007ddd4f2861b160d9afb3c863948abcf5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c03acd4f097cbf133e82f8d4452cccdb54257260b2f85dbd386b038f430521`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6829604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460c92b264e4ac559d4e544ec3a0cd7d6127a531fffdb0db2154ccdfda82f98`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7104b49da8cc9c42091091216f1d29564cd20dc28a154cb48933c382073ea327`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ff7edffe58c50fa5dc64a1d234009d9f618d1d925d0b56286919045e4e95ce4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdee6938423b9a114c22acb9699fdd4022c8969cfe341fb47e3022a29e7d2657`

```dockerfile
```

-	Layers:
	-	`sha256:bc2be06e9d1d8bad4d5e67284d5051946b9aabf787aab6e75467498c13b5bb68`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:83c6bbdb6f6930bd8f77a9c53556fe708b64c69cebc0fb281df0ce1e85599f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10044884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5404d1316a2dbeb592a121da51851996d2b456fc90d76663684a2ee4395fa598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c0c1cdfba8772720f404d6560ec4c5c7b210c2c1342cc3232f9cbb95aaac2`  
		Last Modified: Tue, 28 Apr 2026 00:11:24 GMT  
		Size: 6.8 MB (6818083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee1d8aa61dc7fe184a4afa412505957c2b4a7e1538b23e9eb0567c217b221`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67374b5796f89fbf4825af6ff83925281b51e3a597fc4b5baef090c6eacdb129`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:729af97741ea84b7cd43a0f5b68e6a01b844eda27473601c214d5fcd756584a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c69f772e4d0413f8faa402d1a944a672814c9f0cc459abd865225bb251b8d22`

```dockerfile
```

-	Layers:
	-	`sha256:bc6466cc1dfda6baac01df16d9cb34bf26a929c5008b8e9c83c260eefec91008`  
		Last Modified: Tue, 28 Apr 2026 00:11:23 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:309c3a317f98e396a5687b31ee3eccc5fd14121d27e96f99d307055c33afb154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10659231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c31459ac1dd3166e7b6a56dc48799e3355fc3c2eee66c73bcb6982c096d124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:11:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:11:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:11:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0264ec65d1c94e26eb13ece3293fd0f1a223a083f07123a89ab6533fa7f3ea3`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 6.5 MB (6516368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8720fa9574209724faf15869ee142fb3465e685ab0377192bf9b2d6b801df158`  
		Last Modified: Tue, 28 Apr 2026 00:11:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cab18aed7cf17ef64ccb91a99fc238c3c88fde554678d1f90ded2f38ecaf0d7`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e05fe41e9457ed0d7b0738daa11b7ed4df2ef0483d42e415d92d3d866847bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da164679dfd40fa005a81bdee8a8f4f929cdec1bdfac87231b7fe5e7457ba99`

```dockerfile
```

-	Layers:
	-	`sha256:25926700f4d2f5b98eae89a4bd6d3f6b0df83af058030add1eb43f93db01d776`  
		Last Modified: Tue, 28 Apr 2026 00:11:20 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9182046bc9c75c50fe6738ac524dab8187db8317900daec750a58666ca89fc20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10302333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d38dd3a196967303aeefe505d29ff782d68870c62bd38b262f89436ced913d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:12:50 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:12:50 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:12:50 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:12:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:12:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:12:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f4d9d616afa995dc3996e50baa1ead256ff76b85ea197302fa8f17b5e6ec8c`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 6.6 MB (6564704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067041a71c2cccd9442e4006fff1fdeed654fb2721dc8cdee35791d195917123`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a289f277d81f7348ba8aeee142878f93583d0d9aa7e8beb7796bc6d34e92a`  
		Last Modified: Tue, 28 Apr 2026 00:12:57 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:109c930003fb0d902fc75741c7f2aa1a5d20a060b6348fb6b50dd3a436020eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d1f2e6d3c5103a4a8ce89d1eea6f6cb28092efd4a529280969f99c9112a934`

```dockerfile
```

-	Layers:
	-	`sha256:73c35d38c6c10ef3f24aef75adfe3c8135cca707abd0a557d78aa623c05137b6`  
		Last Modified: Tue, 28 Apr 2026 00:12:58 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:765cf41f86293cbfc817903a2e95c9fc460095ffa6a2afd14e9fbf6098a863e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a300b10c87307999e280d8044bc933dc6a769bf134c71dc069b7df45c1acf71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:16:06 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:16:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='7d20e93c23924cdd5cb6ec51c92f9478c97f9c8a0dbe049dd7ab88af115d622c' ;;     armhf) natsArch='arm6'; sha256='10bbd0cc9648c305bc524f63372f6689004d507273b923782299249116d69306' ;;     armv7) natsArch='arm7'; sha256='7080cc18aafe35f2d3a073bd25cc19510248ec95c56f4ba88342c91b3aecdcb3' ;;     x86_64) natsArch='amd64'; sha256='6abc397684567e133649688a13564ad6de786d64e88253fbb4f6a3aa8c2fca63' ;;     x86) natsArch='386'; sha256='bb0973788e963aa0fe070d29a7bbf3255be04079d3842c3d14572b363d854c16' ;;     s390x) natsArch='s390x'; sha256='7c654954abd640c61cb1805274a7c69502570b71f0b515565cdf52f9303e39fc' ;;     ppc64le) natsArch='ppc64le'; sha256='20d693ceffaf09e79180ad4e1d9411a90fe9791d5aaf1c0f94d6c8b8706824b9' ;;     loong64) natsArch='loong64'; sha256='3e418d560a3c872fb6c7fbc3132172615f0482a152d85f5e705c1c9244f6328b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 28 Apr 2026 00:16:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b00d570ea6fe160e330c54a027a3541fb1ca0795604be5975cba634fb9327b`  
		Last Modified: Tue, 28 Apr 2026 00:16:49 GMT  
		Size: 6.9 MB (6949611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51608ad68619bc3a9ab77b844278637a43da5a519228babd3caee4d0be374c7f`  
		Last Modified: Tue, 28 Apr 2026 00:16:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4568a16c47624175fa8b3ccb3e0db1369f5afb9048bbdcf0d2462d19429c3b`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:66210453cac12e4f00ea8be9a556a70ab26a636163a953598ed5290b8b1ab0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa02bb916d5e127a400bf5a556ddc9a617cdb97906db85765c21264c02b7d1d9`

```dockerfile
```

-	Layers:
	-	`sha256:fbd9e7d40544704e8408524131ac7132b11191a74051051f016bdb84f132d5a1`  
		Last Modified: Tue, 28 Apr 2026 00:16:47 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:5c5ae59dd58fe77318be7ae31b5a18a1730c6ca2c2fd94572d0ee5a81e0c9234
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5020; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:fd5dd09bc60658223075241956f5c1a12ee7b7899258b2a481aad6782476b747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:fd5dd09bc60658223075241956f5c1a12ee7b7899258b2a481aad6782476b747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:f93258804b7b750e94c9f40ff731f37dd3f1d58b3d701747296b389195392e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6656689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdf7f95cd1106aed70d3193211b84336327d7d6e39227a378b132e59cd2811c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:15 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:15 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:645cafb0707c72bb739d648c580351713e463ab89288425fa7d98b2f1fdbf620`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.7 MB (6656179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fa6534131868c72ae11fbdd285d01b9005f1fee11db5bfa8658461dad9ad2`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:1be7db338354131214e3b3470a5c8c8b31042ea4e3aa866dec380b1220cec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aff98c3ae467add0b9dafa6344292ae2d25e4f04d8fed29b96c90ce191558ff`

```dockerfile
```

-	Layers:
	-	`sha256:20abdca85fc4db4036559291726149283e27c173cc3b35669d56848f82455686`  
		Last Modified: Tue, 28 Apr 2026 00:16:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4ed1f54b89f8e5060fe759dc6e248ceeac804b7d348e1f04d6bf6d31c59aa9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6372321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccdbf090baf47e27ae4db0f9c8790d75e1c8d8e82c1b79720b6501e132e89a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f919df7e429763a93b5d6d27149a1a87bc9ac127f959e72f5b3c28d8c18f1c4`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.4 MB (6371812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfd2b733753a6df4c23123458ffe788ed06f7d8077d811230afee5cad866fee`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9ae94cb9c13cf156258901cdd4f02e6f74a272120e1cc4b45c4be1174fca4ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd965b8e180bd7307035f120e36d3e847033d34286c559ed939620672ef540e5`

```dockerfile
```

-	Layers:
	-	`sha256:dde62fc4f35630954901b6cb8ff36fb5ae9ac356a529b38c1feb1da347c6ad99`  
		Last Modified: Tue, 28 Apr 2026 00:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a590e4ec09ca77561055ae23b0c13ddcbd7e883dd1ec7a7eaab79d2287df3855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6362271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7a04813b4f35b04c559770a31858968ceb86a246557eabac4df76f98f6c1c0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1c6002c24a32b8bd34f94ce775d91b9cb180b4ae61c2fd90f3f6e1aeea7bfbec`  
		Last Modified: Mon, 27 Apr 2026 16:34:26 GMT  
		Size: 6.4 MB (6361763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f2429bab47acfd2fdc0a15cce8084ecaf46470f9eda31e915ddc0b269d25a2`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:11db550a869bad0db62e56e53cb855620bb7ca2dc948332c410af7e1250fdcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d443c7db7f097116541a6285df60c40e60bbdf2d30632953fb53002fd6110cb`

```dockerfile
```

-	Layers:
	-	`sha256:f3b62cbe08c54dcada8f9a45c2913825710e196e2f6664da522893602a66c520`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:af178b6f767c98a8b24c8f2919b0afa4bf38e5cd220bd56fd58c2fa034685bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221f9f948e2571a034de89eb42190dab1269f5df9e10a5205da9a81850c106b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:57e2ab576a3f4cf4fde4306db1872fb80293ba1b8a2f842c0afb42cef3b64416`  
		Last Modified: Mon, 27 Apr 2026 16:34:25 GMT  
		Size: 6.1 MB (6059630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1963ade9683354464bc1d9576f0197e3f7a0729c07bdb2d004c7f2107fd6bf04`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:987bfdc54ae277a4d7da8dfb0832967a07c3132fe97fcab68182f91a45966987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb60b3b93a3e9a49efbb7ae7d34e0feaf4dd5917040de681c9cabc8f4d069a61`

```dockerfile
```

-	Layers:
	-	`sha256:f09992496cddb8dd4c6699a5fec53154841cd0bae5755bcc0148d244838a7662`  
		Last Modified: Tue, 28 Apr 2026 00:16:17 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:823c2ee752d1f48475d52d056cbb2544d2dc457ee924054b3a693355743cf468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60234166a503b84593fb27f2563b3cb76161cb74bf3f4ea33bf714ce8e9fe19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 28 Apr 2026 00:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 28 Apr 2026 00:16:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 28 Apr 2026 00:16:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 28 Apr 2026 00:16:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 28 Apr 2026 00:16:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8e011301252c1fece8721a66305f99b55297838af8b7d418ba681b0773979438`  
		Last Modified: Mon, 27 Apr 2026 16:34:28 GMT  
		Size: 6.1 MB (6108560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad746aced13c58c33976fcdb8817f9e7572751eee3b0358e723bfa065c3fc4`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:519715fcfad957e69d2c3d6ea663c442e3ac74f23e4c35f12cda2a2b44e94022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfdcdbb344772476d9933326c37523b935e24c1a3ca3a30fe92308880fb37d2`

```dockerfile
```

-	Layers:
	-	`sha256:f9f179885eb75eace465ec4059e94129c086256826d5cc3a1b2edd4bbc66b59e`  
		Last Modified: Tue, 28 Apr 2026 00:16:31 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:7be687bd0fcf28c0ff569af5d07b5586400ddc2e656ed5059fa069a1861d5310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:513908e15de358856596ba7150e84b831f6f711b57c69bff1dab9e0f2334ccc1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5993871186ecfe774a9cf8a2b3de0621e6afaf3fd93f99cbbaff6fffc782a8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:22:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:22:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:22:21 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:22:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:22:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 28 Apr 2026 00:22:24 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 28 Apr 2026 00:23:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:24:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:24:04 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:24:05 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:24:05 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:24:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ffdad23a2259ee9605b07af3b8756afac669d72d7f4df289af5e1bfa765df`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349750824325190c58f7211d2a32fac8867324987e4912f6187dc9d6f9fb4ae8`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e65ce208cc089d5d84714aa1b4c702e6514a37bc1a25a9e317e5484c4b6770`  
		Last Modified: Tue, 28 Apr 2026 00:24:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fefac29241015b39520060d922c7fb6054787dd9dd417b2cabd03743d7bda5f`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe557d93a73db69714369a258c20de37e40d04268b2f4804c92e12e16976bdd`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3130aba43c6a9d55589835a86638de2d3125fa2366b684015a8ac9fc1c818d`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19f58f4c90bd0a1c10a151c0165e6d1660f82cb62c97e4a3e1ec5be69c14d0`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 507.2 KB (507220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b029516bfa850bb0dc8d626d1e3a9cda785c0b6ff3e1ac8797afb2adf5f0ed3`  
		Last Modified: Tue, 28 Apr 2026 00:24:15 GMT  
		Size: 7.2 MB (7178445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8a07055de8fc46e4e8f02f1a81c1872033e0a3dda665ba7f3a7cdba7cd203`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2e16a4341e7b5618098955dbd5110c7fc4e24810d6e25bb7cd53e768b4539`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a737b9ff5aae65f741d22ddd5e6e1c210d6f45528f4778fcb53b923c0e903`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbeaf674140e140a6e0cb9b0b83df4612f9ab45bc55e9507b8d32bb2be05e1`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:7be687bd0fcf28c0ff569af5d07b5586400ddc2e656ed5059fa069a1861d5310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:513908e15de358856596ba7150e84b831f6f711b57c69bff1dab9e0f2334ccc1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5993871186ecfe774a9cf8a2b3de0621e6afaf3fd93f99cbbaff6fffc782a8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 00:22:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 28 Apr 2026 00:22:20 GMT
ENV NATS_DOCKERIZED=1
# Tue, 28 Apr 2026 00:22:21 GMT
ENV NATS_SERVER=2.12.8
# Tue, 28 Apr 2026 00:22:22 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.8
# Tue, 28 Apr 2026 00:22:23 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.8/nats-server-v2.12.8-windows-amd64.zip
# Tue, 28 Apr 2026 00:22:24 GMT
ENV NATS_SERVER_SHASUM=61836ff8d0cecbb773faf7daa22f5212b7ed3ab5a0c58c12b013d67d64edd6cc
# Tue, 28 Apr 2026 00:23:39 GMT
RUN Set-PSDebug -Trace 2
# Tue, 28 Apr 2026 00:24:04 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 28 Apr 2026 00:24:04 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 28 Apr 2026 00:24:05 GMT
EXPOSE 4222 6222 8222
# Tue, 28 Apr 2026 00:24:05 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 28 Apr 2026 00:24:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06ffdad23a2259ee9605b07af3b8756afac669d72d7f4df289af5e1bfa765df`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349750824325190c58f7211d2a32fac8867324987e4912f6187dc9d6f9fb4ae8`  
		Last Modified: Tue, 28 Apr 2026 00:24:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e65ce208cc089d5d84714aa1b4c702e6514a37bc1a25a9e317e5484c4b6770`  
		Last Modified: Tue, 28 Apr 2026 00:24:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fefac29241015b39520060d922c7fb6054787dd9dd417b2cabd03743d7bda5f`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe557d93a73db69714369a258c20de37e40d04268b2f4804c92e12e16976bdd`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3130aba43c6a9d55589835a86638de2d3125fa2366b684015a8ac9fc1c818d`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19f58f4c90bd0a1c10a151c0165e6d1660f82cb62c97e4a3e1ec5be69c14d0`  
		Last Modified: Tue, 28 Apr 2026 00:24:12 GMT  
		Size: 507.2 KB (507220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b029516bfa850bb0dc8d626d1e3a9cda785c0b6ff3e1ac8797afb2adf5f0ed3`  
		Last Modified: Tue, 28 Apr 2026 00:24:15 GMT  
		Size: 7.2 MB (7178445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8a07055de8fc46e4e8f02f1a81c1872033e0a3dda665ba7f3a7cdba7cd203`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2e16a4341e7b5618098955dbd5110c7fc4e24810d6e25bb7cd53e768b4539`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5a737b9ff5aae65f741d22ddd5e6e1c210d6f45528f4778fcb53b923c0e903`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbeaf674140e140a6e0cb9b0b83df4612f9ab45bc55e9507b8d32bb2be05e1`  
		Last Modified: Tue, 28 Apr 2026 00:24:10 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
