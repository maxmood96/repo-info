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
-	[`nats:2.11.15`](#nats21115)
-	[`nats:2.11.15-alpine`](#nats21115-alpine)
-	[`nats:2.11.15-alpine3.22`](#nats21115-alpine322)
-	[`nats:2.11.15-linux`](#nats21115-linux)
-	[`nats:2.11.15-nanoserver`](#nats21115-nanoserver)
-	[`nats:2.11.15-nanoserver-ltsc2022`](#nats21115-nanoserver-ltsc2022)
-	[`nats:2.11.15-scratch`](#nats21115-scratch)
-	[`nats:2.11.15-windowsservercore`](#nats21115-windowsservercore)
-	[`nats:2.11.15-windowsservercore-ltsc2022`](#nats21115-windowsservercore-ltsc2022)
-	[`nats:2.12`](#nats212)
-	[`nats:2.12-alpine`](#nats212-alpine)
-	[`nats:2.12-alpine3.22`](#nats212-alpine322)
-	[`nats:2.12-linux`](#nats212-linux)
-	[`nats:2.12-nanoserver`](#nats212-nanoserver)
-	[`nats:2.12-nanoserver-ltsc2022`](#nats212-nanoserver-ltsc2022)
-	[`nats:2.12-scratch`](#nats212-scratch)
-	[`nats:2.12-windowsservercore`](#nats212-windowsservercore)
-	[`nats:2.12-windowsservercore-ltsc2022`](#nats212-windowsservercore-ltsc2022)
-	[`nats:2.12.6`](#nats2126)
-	[`nats:2.12.6-alpine`](#nats2126-alpine)
-	[`nats:2.12.6-alpine3.22`](#nats2126-alpine322)
-	[`nats:2.12.6-linux`](#nats2126-linux)
-	[`nats:2.12.6-nanoserver`](#nats2126-nanoserver)
-	[`nats:2.12.6-nanoserver-ltsc2022`](#nats2126-nanoserver-ltsc2022)
-	[`nats:2.12.6-scratch`](#nats2126-scratch)
-	[`nats:2.12.6-windowsservercore`](#nats2126-windowsservercore)
-	[`nats:2.12.6-windowsservercore-ltsc2022`](#nats2126-windowsservercore-ltsc2022)
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
$ docker pull nats@sha256:24e20d33a7214208b1cb699c2e4ebfbed32f7a30b41c18b36be75f019a96616c
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
	-	windows version 10.0.20348.4893; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:1cfc36e2e5e638243d8c722f72c954cd0ec4b15ee82fadbc718ce12e2b3c1652
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
$ docker pull nats@sha256:5bb4bf05e7b13ab68145d526ddcf7cd9b122ab4e9be396318b470fbb3db56cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10901603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6289e36de6a653c3a6fdf4c209ab5af57ddc1e4df304025e5b0319578c5de58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724b6d79b0328c1e41c2e402e40355a84657fd655ea7a04d70e56ef30d88e8d`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 7.1 MB (7095760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba8f8d786c0db5eca6a8142087d4b4f7f7ed64e4f273875c72e0ad427ddf121`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc12736b5f7dcd0aa0232b895c2814f574271450bdd11216c09df4166309c8`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:919d5a1842b84c6b23cb36b4520926b9354c437266edf1f27431ad586e66800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f7b6f48ee2d002cdfd9aacb5c4133eb01d8739a2a8d35d325ea2888c14086f`

```dockerfile
```

-	Layers:
	-	`sha256:930d7ae9e007d75b212ac2cc214b7bcd2ab2e84cacca424823b100cdf48e9834`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:14385cdceab398aa6dd31fd51a8d0eb48f42a9d9a9c8baa88a4ba8a2d0e6d23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db147dcb95e7238e38282e2c4ae9aaa5458bc3e9f34d986671345b0add344f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dd16a263fb7b1c26ba67d42231ee535f3d00df3fe3d4f5238711e29683dbb8`  
		Last Modified: Tue, 24 Mar 2026 18:13:42 GMT  
		Size: 6.8 MB (6815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec38e01326bb918550c36013b0b0e623f7982193707ffc9aa2039204670bbf`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8594a1e0b9d5ba01c5f7247e80cd021b8a3f1b8506d38915575ada877f132f22`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ffd7509c5c7f864d7afff95c068a34f1ca118c768bdca9420ee11046979332f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150020eb28e70d47c0ab5cf9a194589fc277d61e2d9fbdd92ea9c8c455ddc134`

```dockerfile
```

-	Layers:
	-	`sha256:ad2785802c0f18173a579ea09f8a176800c7b83e75133ac73b642a19dece30a4`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8d06b4be0657e317e6fb3f38328294c42c2006e1b8f4f36a703a3fb830799bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fbb045461dbfe04fea74b58c92e0717a120b330d96769922081255eb66162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc4bc127449c7715baf7736c50c8753a177bb234c94a8fd7232fd208006f28`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 6.8 MB (6801564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c2fb00e3905b6cef1c48a75670171e564c04556824be30ba32b633016f1507`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f42b05edd76961960f90d1423d0cbd73d62026f6de01455b7a5cf8bcb3c6b7`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4b4c651289e935e8cb85348a1cffb88cce5d1f34582da27a3352e2a91484ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f995cd5707bf9bac5e586042d4329d1fe2559673e4228b8bf4fb5e009e75587`

```dockerfile
```

-	Layers:
	-	`sha256:4f1cae97aebe3d7bacb664be9a66dff39c030b1cf24216b8d339e9e02787fea0`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:38a21bc067dd790300a33c7a77df288526a88d03808b328a9eabe8d13b152a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10641789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564348acc3c55422d9537181b01dfa0d9d6cf275964069c2fd10b25b8dda339`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383bfc032c7f2638ebfce96b0976e02ee30dcd64cdd4b1a0b23012ea2f78718`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 6.5 MB (6501302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd5bf99f5370727619bf2f95ee9315d3b144ddbf1b3ac8e19a907638ef8ebb`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01ba58374b0a722748241e4256b7bd0dbf522f999248b0ae2269a437263eb5`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6dd0076c1cd64737f8de4b7333e624dfe55173329fb2bac1010522d0b435cdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72caa6f6852373a1ace85c8e8fa5d990923b87e473a50fd58427f20eab29eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:8ef47ff5baeebf3463deb04fb68fb758a95f5ff00412a157f52a285f56482fc7`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:b57e19246c78c3589fb6d2a2d7b57d30e9a8f26a5dea9ecf06278eb47f41ce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e681b291aba2493b6548c5c72f81addeb967503bb75bf7cf22d689c7485b4d2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:57 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152168711ce043c658e36a34e2fd496c19c723f91680ec04f28e212e6b20451`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.6 MB (6550474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba6028f2ec6815bede0ce5a102ff4bf694edd8bd6cc576002e29592d253d9a`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00127979287ad785bdbfea091d652471cb758c03d8b0dd75a34262462608bdb5`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:53acfbd102851dc8657ed52c0adeb138ab2f4f98998712113c290468e44b627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c97473b65b616ab5c4187d1c87706c2ac01ee00d37f590e151ab7390b2d537b`

```dockerfile
```

-	Layers:
	-	`sha256:ae32e72632dade7a0e851b51611d6cb44dd2b476e62c370c017b15f9f02df2d1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:0b96d8319dc5a7fccd30e6b28dfa53bf4a55c113ac3d2f905c900de31bbdc90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8a578d8c5fc8897c630a0895dddec8179595f2038c6902307485a3f14cace0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f13fc4ac0665282379187825661bac82224da72b34bac38edbc43050b2c6e`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 6.9 MB (6934327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a19b2713e4ee80cf7b9d33d33ba4d0a52228b2fa7eb14e1182905f99f1a137`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef841b2f70cfab0cb037b8b542ea4f1700328311b69209d7fa5d50f7bafb99ed`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cd39df443a3b3b87bb26196bddb0601fc93613f151a051eb0bb1743bdd2a97d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3dd97cc216c9d1ad2f0e9b34ce573244908160be058b01282c4190c32c6d7`

```dockerfile
```

-	Layers:
	-	`sha256:5b786517ad8b86d4c95e63a0440e89692600c9115a3c414313d362bb5b4e1b36`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:1cfc36e2e5e638243d8c722f72c954cd0ec4b15ee82fadbc718ce12e2b3c1652
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
$ docker pull nats@sha256:5bb4bf05e7b13ab68145d526ddcf7cd9b122ab4e9be396318b470fbb3db56cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10901603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6289e36de6a653c3a6fdf4c209ab5af57ddc1e4df304025e5b0319578c5de58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724b6d79b0328c1e41c2e402e40355a84657fd655ea7a04d70e56ef30d88e8d`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 7.1 MB (7095760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba8f8d786c0db5eca6a8142087d4b4f7f7ed64e4f273875c72e0ad427ddf121`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc12736b5f7dcd0aa0232b895c2814f574271450bdd11216c09df4166309c8`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:919d5a1842b84c6b23cb36b4520926b9354c437266edf1f27431ad586e66800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f7b6f48ee2d002cdfd9aacb5c4133eb01d8739a2a8d35d325ea2888c14086f`

```dockerfile
```

-	Layers:
	-	`sha256:930d7ae9e007d75b212ac2cc214b7bcd2ab2e84cacca424823b100cdf48e9834`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:14385cdceab398aa6dd31fd51a8d0eb48f42a9d9a9c8baa88a4ba8a2d0e6d23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db147dcb95e7238e38282e2c4ae9aaa5458bc3e9f34d986671345b0add344f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dd16a263fb7b1c26ba67d42231ee535f3d00df3fe3d4f5238711e29683dbb8`  
		Last Modified: Tue, 24 Mar 2026 18:13:42 GMT  
		Size: 6.8 MB (6815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec38e01326bb918550c36013b0b0e623f7982193707ffc9aa2039204670bbf`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8594a1e0b9d5ba01c5f7247e80cd021b8a3f1b8506d38915575ada877f132f22`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ffd7509c5c7f864d7afff95c068a34f1ca118c768bdca9420ee11046979332f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150020eb28e70d47c0ab5cf9a194589fc277d61e2d9fbdd92ea9c8c455ddc134`

```dockerfile
```

-	Layers:
	-	`sha256:ad2785802c0f18173a579ea09f8a176800c7b83e75133ac73b642a19dece30a4`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8d06b4be0657e317e6fb3f38328294c42c2006e1b8f4f36a703a3fb830799bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fbb045461dbfe04fea74b58c92e0717a120b330d96769922081255eb66162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc4bc127449c7715baf7736c50c8753a177bb234c94a8fd7232fd208006f28`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 6.8 MB (6801564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c2fb00e3905b6cef1c48a75670171e564c04556824be30ba32b633016f1507`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f42b05edd76961960f90d1423d0cbd73d62026f6de01455b7a5cf8bcb3c6b7`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4b4c651289e935e8cb85348a1cffb88cce5d1f34582da27a3352e2a91484ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f995cd5707bf9bac5e586042d4329d1fe2559673e4228b8bf4fb5e009e75587`

```dockerfile
```

-	Layers:
	-	`sha256:4f1cae97aebe3d7bacb664be9a66dff39c030b1cf24216b8d339e9e02787fea0`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:38a21bc067dd790300a33c7a77df288526a88d03808b328a9eabe8d13b152a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10641789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564348acc3c55422d9537181b01dfa0d9d6cf275964069c2fd10b25b8dda339`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383bfc032c7f2638ebfce96b0976e02ee30dcd64cdd4b1a0b23012ea2f78718`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 6.5 MB (6501302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd5bf99f5370727619bf2f95ee9315d3b144ddbf1b3ac8e19a907638ef8ebb`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01ba58374b0a722748241e4256b7bd0dbf522f999248b0ae2269a437263eb5`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6dd0076c1cd64737f8de4b7333e624dfe55173329fb2bac1010522d0b435cdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72caa6f6852373a1ace85c8e8fa5d990923b87e473a50fd58427f20eab29eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:8ef47ff5baeebf3463deb04fb68fb758a95f5ff00412a157f52a285f56482fc7`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:b57e19246c78c3589fb6d2a2d7b57d30e9a8f26a5dea9ecf06278eb47f41ce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e681b291aba2493b6548c5c72f81addeb967503bb75bf7cf22d689c7485b4d2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:57 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152168711ce043c658e36a34e2fd496c19c723f91680ec04f28e212e6b20451`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.6 MB (6550474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba6028f2ec6815bede0ce5a102ff4bf694edd8bd6cc576002e29592d253d9a`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00127979287ad785bdbfea091d652471cb758c03d8b0dd75a34262462608bdb5`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:53acfbd102851dc8657ed52c0adeb138ab2f4f98998712113c290468e44b627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c97473b65b616ab5c4187d1c87706c2ac01ee00d37f590e151ab7390b2d537b`

```dockerfile
```

-	Layers:
	-	`sha256:ae32e72632dade7a0e851b51611d6cb44dd2b476e62c370c017b15f9f02df2d1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0b96d8319dc5a7fccd30e6b28dfa53bf4a55c113ac3d2f905c900de31bbdc90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8a578d8c5fc8897c630a0895dddec8179595f2038c6902307485a3f14cace0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f13fc4ac0665282379187825661bac82224da72b34bac38edbc43050b2c6e`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 6.9 MB (6934327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a19b2713e4ee80cf7b9d33d33ba4d0a52228b2fa7eb14e1182905f99f1a137`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef841b2f70cfab0cb037b8b542ea4f1700328311b69209d7fa5d50f7bafb99ed`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cd39df443a3b3b87bb26196bddb0601fc93613f151a051eb0bb1743bdd2a97d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3dd97cc216c9d1ad2f0e9b34ce573244908160be058b01282c4190c32c6d7`

```dockerfile
```

-	Layers:
	-	`sha256:5b786517ad8b86d4c95e63a0440e89692600c9115a3c414313d362bb5b4e1b36`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:81fb519cf3229a15af68b6c89342b09e89bbb0dc4dcafec9ced7a3c0137e8771
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
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:419eda332cc243b564050f8ff6c94e9df148f930aa3184aaabda593a7313786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:419eda332cc243b564050f8ff6c94e9df148f930aa3184aaabda593a7313786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:81fb519cf3229a15af68b6c89342b09e89bbb0dc4dcafec9ced7a3c0137e8771
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
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:4d37e8d6cdeee8b32d4fd382d2bf2a69505277cdd13e180c04fb0e38390e351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:f41fb080320027c5286199c5569b908be086e4612a46e4c7e82f178aa3103288
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989978837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14ee40d14a8fef68d45a8b5702bb6f311e96e21e417235f7b222d2ae770ca4b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:15:30 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:15:32 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.6/nats-server-v2.12.6-windows-amd64.zip
# Tue, 24 Mar 2026 18:15:35 GMT
ENV NATS_SERVER_SHASUM=35445ebdf3232eeafb866e5c3bca5ac3c189525423367997b81945e9b2ace45b
# Tue, 24 Mar 2026 18:16:44 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:17:10 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:17:10 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:17:11 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:17:12 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:17:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ebb7dfcf4ac9b8f43e43c51a3d50dcca87256a00ae4ea377609728728b0f29`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6634d966c316ea226c2850cb5cd991ccde17cdce2933e1020e8c60efc94dbba2`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dad0e2dd4454c1e1451af56c4aa70cfad3e76e78100716d6af66bfd009863c4`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4f6f4239d361d0624b0a3191f19e5aa55b1cb40ca70aeca4aebf7c4a3ebed3`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f1856c416e46ebb6eca1328e0ad9eb402ab18c2ba270d2250a19ad7f9ad8e0`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 498.9 KB (498917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a9397cefbe2cff3e7f23e244eb5a68d02e076f5667ee1a82a4f34253354fb6`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 7.2 MB (7184887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375bab48f011d171877b0100ab3f1e0d72f66cd2c5470bd70aa1d7f9addce14e`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff354d3bb3841d9b4e1ac9f888a81702c96e420ba432074d8c74327b39d089`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d26923e5a217d54c4d0b5d8442af5cce29a96b1b0e95154a562841f379bd7d`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d67ab5aa667bb65182f7b16d680d2eb370dc87f113ccd5cc5a71a626ee814`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:4d37e8d6cdeee8b32d4fd382d2bf2a69505277cdd13e180c04fb0e38390e351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:f41fb080320027c5286199c5569b908be086e4612a46e4c7e82f178aa3103288
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989978837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14ee40d14a8fef68d45a8b5702bb6f311e96e21e417235f7b222d2ae770ca4b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:15:30 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:15:32 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.6/nats-server-v2.12.6-windows-amd64.zip
# Tue, 24 Mar 2026 18:15:35 GMT
ENV NATS_SERVER_SHASUM=35445ebdf3232eeafb866e5c3bca5ac3c189525423367997b81945e9b2ace45b
# Tue, 24 Mar 2026 18:16:44 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:17:10 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:17:10 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:17:11 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:17:12 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:17:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ebb7dfcf4ac9b8f43e43c51a3d50dcca87256a00ae4ea377609728728b0f29`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6634d966c316ea226c2850cb5cd991ccde17cdce2933e1020e8c60efc94dbba2`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dad0e2dd4454c1e1451af56c4aa70cfad3e76e78100716d6af66bfd009863c4`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4f6f4239d361d0624b0a3191f19e5aa55b1cb40ca70aeca4aebf7c4a3ebed3`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f1856c416e46ebb6eca1328e0ad9eb402ab18c2ba270d2250a19ad7f9ad8e0`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 498.9 KB (498917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a9397cefbe2cff3e7f23e244eb5a68d02e076f5667ee1a82a4f34253354fb6`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 7.2 MB (7184887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375bab48f011d171877b0100ab3f1e0d72f66cd2c5470bd70aa1d7f9addce14e`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff354d3bb3841d9b4e1ac9f888a81702c96e420ba432074d8c74327b39d089`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d26923e5a217d54c4d0b5d8442af5cce29a96b1b0e95154a562841f379bd7d`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d67ab5aa667bb65182f7b16d680d2eb370dc87f113ccd5cc5a71a626ee814`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:0800d39b5cb258e231232318592e9d96bdf24f1518f34503272f93846a089e32
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
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:6beefe4b70a2ffbb01cda9826e1d569a8a79d1f2acf01005f355e2b07606ca44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e8e4be3a366673cca39f017feff6959a97e0bf0c7532f6f46c331759df468a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:51 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:51 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7e63c3af64c8405f5d23275254d5a1685d8b6769408b1389d5cbb5e69727de9`  
		Last Modified: Tue, 24 Mar 2026 15:55:28 GMT  
		Size: 6.5 MB (6494855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec55e3b36d28a1727c9006137813c27d6115506a4e18a39cde0fb76d0e9616`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:f6ace49b50ed85d0cad754b01517bcef040e7a4fe048bb091d3fa602b6bdb218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2346e39fee769925c3c23b5f5d24337e60bdb07e7206ab969c9910ee9bc5`

```dockerfile
```

-	Layers:
	-	`sha256:2442aeb9d053e9aebac1749deabd69065737b708cc2ccdaf914eb2084c6cd234`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:c8f6d2e51a224517eb269d02cb9c8272bd99ad3cb7b3a90bb563133f2b2bd1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42bc1cd2a79eeac49db67b13c4f80bf93741cdd1a99e82bad3de9796c7b2f2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99fe1ed0d1a3485150391b8e0454b8178cb17fc15a68e6cad8ca54d49802a30a`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 6.2 MB (6218017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcacc6fd95141f743750760c71c1be8ab1f635e30b595eef94fac3d5306522`  
		Last Modified: Tue, 24 Mar 2026 18:39:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:377c745606afedf02308b7fad2f62c7240cf71b04d15e1a94c0f4703cff8fa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94d5afc50036cb3a5eba21ec11cca57e4ab2c84463b19fdfe3e3e291e7a74cf`

```dockerfile
```

-	Layers:
	-	`sha256:0a8af9199220ee3a782696072117154ef76ffc7aa0c9b42181aa09f33e979ba6`  
		Last Modified: Tue, 24 Mar 2026 18:39:53 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:055dfd0c6acf95ee1c307329df0e438ed20e7c67118b9fe2701012cc3eecdb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c52b0a01335266a8f573e23b83dff5c40a50a37df8218b7b584ee141e42fda4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:065c3ae51de74392d9d99a5b43c84d98f1960fe6ce8c355c7e4b4bf9eef4a5c4`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.2 MB (6207765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:288aeb087717f3d445d13febfef6ad933eecfa68ec4c55a2d9a3c9ac60fb0510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bec437861679e7e73a1bd94e866278722db4fb2c84f515f3a209368281508e`

```dockerfile
```

-	Layers:
	-	`sha256:07c1d60302821ed87af9e3c3f3e829bb0ecd68820fbc12fbd581c86759176afb`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd263bc467a1ece21cdae5119f115a03f6a14564d0996c53b4d0adf299635f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e2ca270d24eee57643c49734763d61bb3dd341f04dc9ef55a5f206aff22919`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:82f1bcf7cdc5a871f261539fd2792c122943051a252ed1974fe0f05e3c44cf68`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 5.9 MB (5914074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe75ac13e6539cf5c58ef37905585748a85c7973493c0630965332a7ffb36c0`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:23eb4b439edda7cbb15fd544bbfc9592dc9513c21e1aa3e095181a7496c74bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5877514342232a29d753a50754bc6a6921a450417495c4572805e6e655e8ded5`

```dockerfile
```

-	Layers:
	-	`sha256:1b6d810b6eb7d44d522f711c5c170ce2df7279c9fd90a6d5b72c09443a2316b5`  
		Last Modified: Tue, 24 Mar 2026 18:40:34 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:ff62b32c9052feba1c98f26252211307c5334256189741e05b7f51735723ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1347ddb9e066d1fd367d07ed5ab9c09dd2b2a724995dc71b7ceb9d91a6ff125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a52a724beb3d6edbc8a6c1bcbf1ca075c87995b1ba8cd45c0cfc0d4105c3b00`  
		Last Modified: Tue, 24 Mar 2026 15:55:24 GMT  
		Size: 6.0 MB (5962181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6b264c693a6c247cc7d1d8799bf4318655c1291916b8e3abab01448bc62e49`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:6d64bb907eb2d82b924cb5b7311bc175f5b9dab6e6215d408872935564d819b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48158be55bff71e1e86262d537b30e74fd4cf81d452a481222c6fc941b75583`

```dockerfile
```

-	Layers:
	-	`sha256:9198ecc0eef93f55015b5ad1ec90d164de361b6b8888aa63b8a3f50df53d5e02`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:7ba1afeff1c795fbfa4570ba90caaf7b32612dce3b6c22f92df9d08fb54b769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d6d26f36ddd6b3fcb03c5756a05f19575698c7e3b9193bb2227989abc92e49`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38e32835a80931455e48f3851737e748f5746d8cc85e076c87e48210d2437c30`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.3 MB (6333902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf712fe01491a02befe3d223500d656bf6c58b29898a209f9418e4d339195bb`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:c238441fd63b4bcb8ee269435d2239f5a0136213bac6d305a3dd7e705532d6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5f710b01fc3e3df1e867019432f69b8585870510917a65453c508367b885e5`

```dockerfile
```

-	Layers:
	-	`sha256:1518e888792ffe72daeb5ffce1c2e76b70d5c5027583377942bff9f2723b9053`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:84b335872ab1dd7e19b6fab35a2e7c6c139b12d13aa7001f09fbb0a1a31e45a4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133329674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2eace19bc689c1819b557a0aa6a86cfe6484e910cba543d483fe28f3cc66a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:28 GMT
RUN cmd /S /C #(nop) COPY file:ed1189637cf14d6f82bd62abd3ebc861a2617a31a09ae7f962048b040a639644 in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d7ab56f5d9cb0cf9d9af8a0c4e0ab9a576a3d3f3b1282a696ab132d4cd0360`  
		Last Modified: Tue, 24 Mar 2026 18:39:38 GMT  
		Size: 6.7 MB (6673215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89139a704ae0938dfa4c1b9530e208a7ab930535ec9c6df24c638ae696ea36a`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c20967f993fd513f9bfdf04e3f67ae0307388313b37638d57e10fbfd9d1cfd`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e378f20627e786391a69d075c2c1edce83a3e242d594589128be0a8d4570af`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4551ca094c842533ca2d88482c737291c0b7b089e927c2b365ed8003450a4dc2`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:a7da54d489edb63f95ac9ec6c22834041d20a18a3b3413481764d7d6985aa59a
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
$ docker pull nats@sha256:e71a1cdced17dede784e79ef1cb38465560671cc65648ab2cf37b8e85dd2a998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10759846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4916f00b11d821bfd76cbe7ea612f64e7171067bf6c6d947df1f6df57a81cac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c629c9999718b4c6b3e4524bad2c29ae78c32a79c4daa95250b6ba1e1eab1aaa`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 7.0 MB (6954002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7233360756ffdeb22fc9a86a3a6d620c9925f338d61cf653c2f771562fd79229`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa11fa3e09b6dc7a3a8bfc68966822b618bfa1e28dfb16806110afc00b028801`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5a1882ccb45af23a1e6d7a03e11a6c34379de4653fe4697f759244b80bc2c383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea4cd6d5385dd6db79b9a50061234289d7bd084603d19184ad12d58d038dfd4`

```dockerfile
```

-	Layers:
	-	`sha256:7cab5da085c06baf637ebf4f2f3451f5d935df8d8ad344f14d4f95b6e539582b`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8929001b45eab6eaf0ed916cf5b6de266e15b868dcd98ed47e4e6a0606b3cd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10180614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0107502dbba5034afa32f69a55c30675018f7768389941b8df4459c8e5631d28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:49 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:49 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:49 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0dc2e3a53e7dfe9bf1fd1a22974bd2d659294613be2f882137d0555dd521f3`  
		Last Modified: Tue, 24 Mar 2026 18:13:54 GMT  
		Size: 6.7 MB (6674600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22826ee17c11632e573d45c662f52c9e16086b931509b08c913b644cf5753a2`  
		Last Modified: Tue, 24 Mar 2026 18:13:53 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086fd7ce839159e7cb142c22e0968bec9f9c2301046934360c730b00d83e16bd`  
		Last Modified: Tue, 24 Mar 2026 18:13:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f35d9e93231a149640d7d44feec9d33f21f9202317ca6bf0ac1f454117ce4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c8c08932d30a060bf1ea0be11f77c6dff447bbeff3437667f6a7298844a3ee`

```dockerfile
```

-	Layers:
	-	`sha256:943515928efb2421d691a3c5c316716237c0efd031a41f9bca1b621f1cae752b`  
		Last Modified: Tue, 24 Mar 2026 18:13:54 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:20d70ab66f6719f6cf8790375e43b608159c4690f387a5b3a88cc9c6f02c2ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9891953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2e339bcc0ef62e00dc9f9a87da1d175359930f50e96e2fcf56e200f80a053c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:46 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:14:46 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:14:46 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3e31ee0e1db5d78c8ebab8a6dbba9808c27d27563582b1d315f86a5260c7c`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 6.7 MB (6667355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f6f60b934e7bd07fb20a1b0a36151d3627617fb015114749ce09b2916fddf0`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaf85dadd0874ca6900a953c7661993333993768e210bb5550b1ed499d36e68`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9344184c04e86741d4c696463189817983f22d3b402f55da26b68d34c4359b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e406555c320d2b9bbf5850a193a1bb4f0ed4819afaa6c815efb97472e3e1b6d5`

```dockerfile
```

-	Layers:
	-	`sha256:d6702d41711813eb86abd00c922acd57a7aa59714bb639a19c644aa6e2ba38bc`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36507fcd1538a86bd3aee16397816942014ef98e60cf382c69e0b1a7873f9b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515d3db296da783262131ea09b404a7eeee88325deb10ed182637b235abcb55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:06 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:21:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:21:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67fc99252adb5c0ce2b9e63be9ad8a5169d555955b7d067f342d8122f3fac74`  
		Last Modified: Tue, 24 Mar 2026 18:21:11 GMT  
		Size: 6.4 MB (6374799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecb5e11849f806590b036b643a5da097e026e7c39cdeb1a37367cf6a55483cd`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93969f7f79030de2627f1e7599ebf69c7f7abb6edd6cc3a744427ee16049144`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4ecb252842e0f6e72cc520e39cb036d4e52ce14d038f0a34fe462d4b8f1aad75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ac12f685ad559ca3c645ae05f9f4477191d83250f72b8e7f9b48204aeb9d7f`

```dockerfile
```

-	Layers:
	-	`sha256:faf3c18e344bd4f44c93e42c3508e3e775a8ff94fe840e27bc10ac836fc365b9`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:120629293ebfcf410e16bb071f883706bf26721b4c1c9cd3464e0bd8253a6b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10157559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a6fc48e4a3fa6c7f9d82de810932b57b724c8aa7d9a116043029e56e108792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa49855571a70f310dc8def33262bbee295e2492166a38c2a449df058a6577`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.4 MB (6422291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e953c0818eb7566baea5faba9a891bbb7b5070778e2eead7c2acd034fab2face`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d767892645e66c28cacd5091c75449dce029986589320c668602d32772a2abb`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4db4dd0c9d0abd7b268c4244a7853de599c58ce3eb3b49a983c22437105c4d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95079863e6c20529b2f4f3dade6d11723434e4bf97dd2828fea56440c4e513f6`

```dockerfile
```

-	Layers:
	-	`sha256:0d4be26a949b1e7fabf9af3594928f1389db8f5d656e39f829441ffc459c7ae1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:481e422723267a967e57d451c9119acbab0c36f0a8476192a9239afb86b1f599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10447068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7233e45dcd427bf115ea11b2ae3ff629e54b44064d1b12155a1271540ef037eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:10 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413afd7d07ec861732bcf80918930a61263fc6607441f3820570662cd3a3cdbc`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 6.8 MB (6795667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df47538a8f294397d3aa4f0fc0323c4471e2e3a070039fcab75a9e2608a7e525`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4525ac0099c66d3e0e55f0cd35f4bec7d56a58d7d55c8bdd319cab1da0d7021e`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6c1b6331a7ec2cf433553957d23378998f62b21513e10e848425b9d0d924205b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cc7799beae56f6603ac257802e481fdddbf767159e7e80d7e7db888d250127`

```dockerfile
```

-	Layers:
	-	`sha256:2e2457bdb66ca67af83180c43c59ba4a4cf3c837f80a1f3a8df7a5ab5483ba90`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.22`

```console
$ docker pull nats@sha256:a7da54d489edb63f95ac9ec6c22834041d20a18a3b3413481764d7d6985aa59a
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
$ docker pull nats@sha256:e71a1cdced17dede784e79ef1cb38465560671cc65648ab2cf37b8e85dd2a998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10759846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4916f00b11d821bfd76cbe7ea612f64e7171067bf6c6d947df1f6df57a81cac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c629c9999718b4c6b3e4524bad2c29ae78c32a79c4daa95250b6ba1e1eab1aaa`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 7.0 MB (6954002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7233360756ffdeb22fc9a86a3a6d620c9925f338d61cf653c2f771562fd79229`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa11fa3e09b6dc7a3a8bfc68966822b618bfa1e28dfb16806110afc00b028801`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5a1882ccb45af23a1e6d7a03e11a6c34379de4653fe4697f759244b80bc2c383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea4cd6d5385dd6db79b9a50061234289d7bd084603d19184ad12d58d038dfd4`

```dockerfile
```

-	Layers:
	-	`sha256:7cab5da085c06baf637ebf4f2f3451f5d935df8d8ad344f14d4f95b6e539582b`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:8929001b45eab6eaf0ed916cf5b6de266e15b868dcd98ed47e4e6a0606b3cd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10180614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0107502dbba5034afa32f69a55c30675018f7768389941b8df4459c8e5631d28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:49 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:49 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:49 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0dc2e3a53e7dfe9bf1fd1a22974bd2d659294613be2f882137d0555dd521f3`  
		Last Modified: Tue, 24 Mar 2026 18:13:54 GMT  
		Size: 6.7 MB (6674600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22826ee17c11632e573d45c662f52c9e16086b931509b08c913b644cf5753a2`  
		Last Modified: Tue, 24 Mar 2026 18:13:53 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086fd7ce839159e7cb142c22e0968bec9f9c2301046934360c730b00d83e16bd`  
		Last Modified: Tue, 24 Mar 2026 18:13:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2f35d9e93231a149640d7d44feec9d33f21f9202317ca6bf0ac1f454117ce4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c8c08932d30a060bf1ea0be11f77c6dff447bbeff3437667f6a7298844a3ee`

```dockerfile
```

-	Layers:
	-	`sha256:943515928efb2421d691a3c5c316716237c0efd031a41f9bca1b621f1cae752b`  
		Last Modified: Tue, 24 Mar 2026 18:13:54 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:20d70ab66f6719f6cf8790375e43b608159c4690f387a5b3a88cc9c6f02c2ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9891953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2e339bcc0ef62e00dc9f9a87da1d175359930f50e96e2fcf56e200f80a053c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:46 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:14:46 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:14:46 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3e31ee0e1db5d78c8ebab8a6dbba9808c27d27563582b1d315f86a5260c7c`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 6.7 MB (6667355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f6f60b934e7bd07fb20a1b0a36151d3627617fb015114749ce09b2916fddf0`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaf85dadd0874ca6900a953c7661993333993768e210bb5550b1ed499d36e68`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9344184c04e86741d4c696463189817983f22d3b402f55da26b68d34c4359b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e406555c320d2b9bbf5850a193a1bb4f0ed4819afaa6c815efb97472e3e1b6d5`

```dockerfile
```

-	Layers:
	-	`sha256:d6702d41711813eb86abd00c922acd57a7aa59714bb639a19c644aa6e2ba38bc`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36507fcd1538a86bd3aee16397816942014ef98e60cf382c69e0b1a7873f9b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515d3db296da783262131ea09b404a7eeee88325deb10ed182637b235abcb55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:06 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:21:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:21:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67fc99252adb5c0ce2b9e63be9ad8a5169d555955b7d067f342d8122f3fac74`  
		Last Modified: Tue, 24 Mar 2026 18:21:11 GMT  
		Size: 6.4 MB (6374799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecb5e11849f806590b036b643a5da097e026e7c39cdeb1a37367cf6a55483cd`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93969f7f79030de2627f1e7599ebf69c7f7abb6edd6cc3a744427ee16049144`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4ecb252842e0f6e72cc520e39cb036d4e52ce14d038f0a34fe462d4b8f1aad75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ac12f685ad559ca3c645ae05f9f4477191d83250f72b8e7f9b48204aeb9d7f`

```dockerfile
```

-	Layers:
	-	`sha256:faf3c18e344bd4f44c93e42c3508e3e775a8ff94fe840e27bc10ac836fc365b9`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:120629293ebfcf410e16bb071f883706bf26721b4c1c9cd3464e0bd8253a6b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10157559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a6fc48e4a3fa6c7f9d82de810932b57b724c8aa7d9a116043029e56e108792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa49855571a70f310dc8def33262bbee295e2492166a38c2a449df058a6577`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.4 MB (6422291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e953c0818eb7566baea5faba9a891bbb7b5070778e2eead7c2acd034fab2face`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d767892645e66c28cacd5091c75449dce029986589320c668602d32772a2abb`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4db4dd0c9d0abd7b268c4244a7853de599c58ce3eb3b49a983c22437105c4d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95079863e6c20529b2f4f3dade6d11723434e4bf97dd2828fea56440c4e513f6`

```dockerfile
```

-	Layers:
	-	`sha256:0d4be26a949b1e7fabf9af3594928f1389db8f5d656e39f829441ffc459c7ae1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:481e422723267a967e57d451c9119acbab0c36f0a8476192a9239afb86b1f599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10447068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7233e45dcd427bf115ea11b2ae3ff629e54b44064d1b12155a1271540ef037eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:10 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413afd7d07ec861732bcf80918930a61263fc6607441f3820570662cd3a3cdbc`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 6.8 MB (6795667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df47538a8f294397d3aa4f0fc0323c4471e2e3a070039fcab75a9e2608a7e525`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4525ac0099c66d3e0e55f0cd35f4bec7d56a58d7d55c8bdd319cab1da0d7021e`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6c1b6331a7ec2cf433553957d23378998f62b21513e10e848425b9d0d924205b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cc7799beae56f6603ac257802e481fdddbf767159e7e80d7e7db888d250127`

```dockerfile
```

-	Layers:
	-	`sha256:2e2457bdb66ca67af83180c43c59ba4a4cf3c837f80a1f3a8df7a5ab5483ba90`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:f83065787c094e3315c60e7ded5cf05694675c77b116f5b15e5aeffced804804
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
$ docker pull nats@sha256:6beefe4b70a2ffbb01cda9826e1d569a8a79d1f2acf01005f355e2b07606ca44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e8e4be3a366673cca39f017feff6959a97e0bf0c7532f6f46c331759df468a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:51 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:51 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7e63c3af64c8405f5d23275254d5a1685d8b6769408b1389d5cbb5e69727de9`  
		Last Modified: Tue, 24 Mar 2026 15:55:28 GMT  
		Size: 6.5 MB (6494855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec55e3b36d28a1727c9006137813c27d6115506a4e18a39cde0fb76d0e9616`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6ace49b50ed85d0cad754b01517bcef040e7a4fe048bb091d3fa602b6bdb218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2346e39fee769925c3c23b5f5d24337e60bdb07e7206ab969c9910ee9bc5`

```dockerfile
```

-	Layers:
	-	`sha256:2442aeb9d053e9aebac1749deabd69065737b708cc2ccdaf914eb2084c6cd234`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:c8f6d2e51a224517eb269d02cb9c8272bd99ad3cb7b3a90bb563133f2b2bd1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42bc1cd2a79eeac49db67b13c4f80bf93741cdd1a99e82bad3de9796c7b2f2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99fe1ed0d1a3485150391b8e0454b8178cb17fc15a68e6cad8ca54d49802a30a`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 6.2 MB (6218017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcacc6fd95141f743750760c71c1be8ab1f635e30b595eef94fac3d5306522`  
		Last Modified: Tue, 24 Mar 2026 18:39:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:377c745606afedf02308b7fad2f62c7240cf71b04d15e1a94c0f4703cff8fa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94d5afc50036cb3a5eba21ec11cca57e4ab2c84463b19fdfe3e3e291e7a74cf`

```dockerfile
```

-	Layers:
	-	`sha256:0a8af9199220ee3a782696072117154ef76ffc7aa0c9b42181aa09f33e979ba6`  
		Last Modified: Tue, 24 Mar 2026 18:39:53 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:055dfd0c6acf95ee1c307329df0e438ed20e7c67118b9fe2701012cc3eecdb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c52b0a01335266a8f573e23b83dff5c40a50a37df8218b7b584ee141e42fda4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:065c3ae51de74392d9d99a5b43c84d98f1960fe6ce8c355c7e4b4bf9eef4a5c4`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.2 MB (6207765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:288aeb087717f3d445d13febfef6ad933eecfa68ec4c55a2d9a3c9ac60fb0510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bec437861679e7e73a1bd94e866278722db4fb2c84f515f3a209368281508e`

```dockerfile
```

-	Layers:
	-	`sha256:07c1d60302821ed87af9e3c3f3e829bb0ecd68820fbc12fbd581c86759176afb`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd263bc467a1ece21cdae5119f115a03f6a14564d0996c53b4d0adf299635f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e2ca270d24eee57643c49734763d61bb3dd341f04dc9ef55a5f206aff22919`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:82f1bcf7cdc5a871f261539fd2792c122943051a252ed1974fe0f05e3c44cf68`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 5.9 MB (5914074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe75ac13e6539cf5c58ef37905585748a85c7973493c0630965332a7ffb36c0`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:23eb4b439edda7cbb15fd544bbfc9592dc9513c21e1aa3e095181a7496c74bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5877514342232a29d753a50754bc6a6921a450417495c4572805e6e655e8ded5`

```dockerfile
```

-	Layers:
	-	`sha256:1b6d810b6eb7d44d522f711c5c170ce2df7279c9fd90a6d5b72c09443a2316b5`  
		Last Modified: Tue, 24 Mar 2026 18:40:34 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:ff62b32c9052feba1c98f26252211307c5334256189741e05b7f51735723ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1347ddb9e066d1fd367d07ed5ab9c09dd2b2a724995dc71b7ceb9d91a6ff125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a52a724beb3d6edbc8a6c1bcbf1ca075c87995b1ba8cd45c0cfc0d4105c3b00`  
		Last Modified: Tue, 24 Mar 2026 15:55:24 GMT  
		Size: 6.0 MB (5962181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6b264c693a6c247cc7d1d8799bf4318655c1291916b8e3abab01448bc62e49`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6d64bb907eb2d82b924cb5b7311bc175f5b9dab6e6215d408872935564d819b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48158be55bff71e1e86262d537b30e74fd4cf81d452a481222c6fc941b75583`

```dockerfile
```

-	Layers:
	-	`sha256:9198ecc0eef93f55015b5ad1ec90d164de361b6b8888aa63b8a3f50df53d5e02`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:7ba1afeff1c795fbfa4570ba90caaf7b32612dce3b6c22f92df9d08fb54b769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d6d26f36ddd6b3fcb03c5756a05f19575698c7e3b9193bb2227989abc92e49`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38e32835a80931455e48f3851737e748f5746d8cc85e076c87e48210d2437c30`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.3 MB (6333902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf712fe01491a02befe3d223500d656bf6c58b29898a209f9418e4d339195bb`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c238441fd63b4bcb8ee269435d2239f5a0136213bac6d305a3dd7e705532d6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5f710b01fc3e3df1e867019432f69b8585870510917a65453c508367b885e5`

```dockerfile
```

-	Layers:
	-	`sha256:1518e888792ffe72daeb5ffce1c2e76b70d5c5027583377942bff9f2723b9053`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:a45756f638afc778a0b6818abb7d451f97670e72263bde178811d1dbf6314bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:84b335872ab1dd7e19b6fab35a2e7c6c139b12d13aa7001f09fbb0a1a31e45a4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133329674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2eace19bc689c1819b557a0aa6a86cfe6484e910cba543d483fe28f3cc66a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:28 GMT
RUN cmd /S /C #(nop) COPY file:ed1189637cf14d6f82bd62abd3ebc861a2617a31a09ae7f962048b040a639644 in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d7ab56f5d9cb0cf9d9af8a0c4e0ab9a576a3d3f3b1282a696ab132d4cd0360`  
		Last Modified: Tue, 24 Mar 2026 18:39:38 GMT  
		Size: 6.7 MB (6673215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89139a704ae0938dfa4c1b9530e208a7ab930535ec9c6df24c638ae696ea36a`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c20967f993fd513f9bfdf04e3f67ae0307388313b37638d57e10fbfd9d1cfd`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e378f20627e786391a69d075c2c1edce83a3e242d594589128be0a8d4570af`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4551ca094c842533ca2d88482c737291c0b7b089e927c2b365ed8003450a4dc2`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:a45756f638afc778a0b6818abb7d451f97670e72263bde178811d1dbf6314bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:84b335872ab1dd7e19b6fab35a2e7c6c139b12d13aa7001f09fbb0a1a31e45a4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133329674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2eace19bc689c1819b557a0aa6a86cfe6484e910cba543d483fe28f3cc66a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:28 GMT
RUN cmd /S /C #(nop) COPY file:ed1189637cf14d6f82bd62abd3ebc861a2617a31a09ae7f962048b040a639644 in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d7ab56f5d9cb0cf9d9af8a0c4e0ab9a576a3d3f3b1282a696ab132d4cd0360`  
		Last Modified: Tue, 24 Mar 2026 18:39:38 GMT  
		Size: 6.7 MB (6673215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89139a704ae0938dfa4c1b9530e208a7ab930535ec9c6df24c638ae696ea36a`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c20967f993fd513f9bfdf04e3f67ae0307388313b37638d57e10fbfd9d1cfd`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e378f20627e786391a69d075c2c1edce83a3e242d594589128be0a8d4570af`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4551ca094c842533ca2d88482c737291c0b7b089e927c2b365ed8003450a4dc2`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:f83065787c094e3315c60e7ded5cf05694675c77b116f5b15e5aeffced804804
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
$ docker pull nats@sha256:6beefe4b70a2ffbb01cda9826e1d569a8a79d1f2acf01005f355e2b07606ca44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e8e4be3a366673cca39f017feff6959a97e0bf0c7532f6f46c331759df468a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:51 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:51 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7e63c3af64c8405f5d23275254d5a1685d8b6769408b1389d5cbb5e69727de9`  
		Last Modified: Tue, 24 Mar 2026 15:55:28 GMT  
		Size: 6.5 MB (6494855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec55e3b36d28a1727c9006137813c27d6115506a4e18a39cde0fb76d0e9616`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f6ace49b50ed85d0cad754b01517bcef040e7a4fe048bb091d3fa602b6bdb218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2346e39fee769925c3c23b5f5d24337e60bdb07e7206ab969c9910ee9bc5`

```dockerfile
```

-	Layers:
	-	`sha256:2442aeb9d053e9aebac1749deabd69065737b708cc2ccdaf914eb2084c6cd234`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:c8f6d2e51a224517eb269d02cb9c8272bd99ad3cb7b3a90bb563133f2b2bd1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42bc1cd2a79eeac49db67b13c4f80bf93741cdd1a99e82bad3de9796c7b2f2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99fe1ed0d1a3485150391b8e0454b8178cb17fc15a68e6cad8ca54d49802a30a`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 6.2 MB (6218017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcacc6fd95141f743750760c71c1be8ab1f635e30b595eef94fac3d5306522`  
		Last Modified: Tue, 24 Mar 2026 18:39:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:377c745606afedf02308b7fad2f62c7240cf71b04d15e1a94c0f4703cff8fa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94d5afc50036cb3a5eba21ec11cca57e4ab2c84463b19fdfe3e3e291e7a74cf`

```dockerfile
```

-	Layers:
	-	`sha256:0a8af9199220ee3a782696072117154ef76ffc7aa0c9b42181aa09f33e979ba6`  
		Last Modified: Tue, 24 Mar 2026 18:39:53 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:055dfd0c6acf95ee1c307329df0e438ed20e7c67118b9fe2701012cc3eecdb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c52b0a01335266a8f573e23b83dff5c40a50a37df8218b7b584ee141e42fda4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:065c3ae51de74392d9d99a5b43c84d98f1960fe6ce8c355c7e4b4bf9eef4a5c4`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.2 MB (6207765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:288aeb087717f3d445d13febfef6ad933eecfa68ec4c55a2d9a3c9ac60fb0510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bec437861679e7e73a1bd94e866278722db4fb2c84f515f3a209368281508e`

```dockerfile
```

-	Layers:
	-	`sha256:07c1d60302821ed87af9e3c3f3e829bb0ecd68820fbc12fbd581c86759176afb`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd263bc467a1ece21cdae5119f115a03f6a14564d0996c53b4d0adf299635f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e2ca270d24eee57643c49734763d61bb3dd341f04dc9ef55a5f206aff22919`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:82f1bcf7cdc5a871f261539fd2792c122943051a252ed1974fe0f05e3c44cf68`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 5.9 MB (5914074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe75ac13e6539cf5c58ef37905585748a85c7973493c0630965332a7ffb36c0`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:23eb4b439edda7cbb15fd544bbfc9592dc9513c21e1aa3e095181a7496c74bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5877514342232a29d753a50754bc6a6921a450417495c4572805e6e655e8ded5`

```dockerfile
```

-	Layers:
	-	`sha256:1b6d810b6eb7d44d522f711c5c170ce2df7279c9fd90a6d5b72c09443a2316b5`  
		Last Modified: Tue, 24 Mar 2026 18:40:34 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:ff62b32c9052feba1c98f26252211307c5334256189741e05b7f51735723ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1347ddb9e066d1fd367d07ed5ab9c09dd2b2a724995dc71b7ceb9d91a6ff125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a52a724beb3d6edbc8a6c1bcbf1ca075c87995b1ba8cd45c0cfc0d4105c3b00`  
		Last Modified: Tue, 24 Mar 2026 15:55:24 GMT  
		Size: 6.0 MB (5962181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6b264c693a6c247cc7d1d8799bf4318655c1291916b8e3abab01448bc62e49`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6d64bb907eb2d82b924cb5b7311bc175f5b9dab6e6215d408872935564d819b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48158be55bff71e1e86262d537b30e74fd4cf81d452a481222c6fc941b75583`

```dockerfile
```

-	Layers:
	-	`sha256:9198ecc0eef93f55015b5ad1ec90d164de361b6b8888aa63b8a3f50df53d5e02`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:7ba1afeff1c795fbfa4570ba90caaf7b32612dce3b6c22f92df9d08fb54b769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d6d26f36ddd6b3fcb03c5756a05f19575698c7e3b9193bb2227989abc92e49`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38e32835a80931455e48f3851737e748f5746d8cc85e076c87e48210d2437c30`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.3 MB (6333902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf712fe01491a02befe3d223500d656bf6c58b29898a209f9418e4d339195bb`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c238441fd63b4bcb8ee269435d2239f5a0136213bac6d305a3dd7e705532d6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5f710b01fc3e3df1e867019432f69b8585870510917a65453c508367b885e5`

```dockerfile
```

-	Layers:
	-	`sha256:1518e888792ffe72daeb5ffce1c2e76b70d5c5027583377942bff9f2723b9053`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:5dd9e244a9129dae0e2a1376f2a674d48449ffc713b4db50f43fa065a708f9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:2309ec8a0a4c528ab4b31287b1e1796db21e598834bcc725a870c431050a95ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989838238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d38376f954f629ae732ecd96e45094cc8a697e03abc2bf6a918565d5884b5b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:33:35 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:33:35 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:33:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.15/nats-server-v2.11.15-windows-amd64.zip
# Tue, 24 Mar 2026 18:33:37 GMT
ENV NATS_SERVER_SHASUM=25ffe2528406c9f0a038b3e2044edeb0220848b0eeef984d6a635071e13d073b
# Tue, 24 Mar 2026 18:33:45 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:34:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:34:07 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:34:08 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:34:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:34:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d326228f48cb794c7bb9aa65a5116873809441461fb3d90daa22e73631cdaee`  
		Last Modified: Tue, 24 Mar 2026 18:34:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8455a6abb1832f1311b97fe501dcb999801f72c18585ed3d92f67a2e7b7b1042`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397579ee30eb49948a6bf467d0a8c4098496472e451ec91e62f13de9c9d9e7b2`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c39206ad86593cb944a9eea94a53d7456be978c6f9a167e7b438309f3152b8`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94436b7f73a2569f6f5e7e64615614652f15a633d21f24f049d78726ff85db87`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 502.1 KB (502102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e68c5e1ca4b3164aa3e8e3b6ff218693d3b3a0edf9d059e3b6f5617b7622d2`  
		Last Modified: Tue, 24 Mar 2026 18:34:18 GMT  
		Size: 7.0 MB (7041118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea850075983ab6151db5dab006dc247fdebe9859a840db9f8c181162bfc5bc9b`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b337a3c72e466a7afbed061bd2926e751ece63a8bea7faf3e9f7018e1080df45`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62ab004cc600d1c8431b83a1943cf829530d17cba4dfbc76242490a62208b14`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040bc400564d6411725e3162b65902a003d97f5987f2ebc59df98ed36eda862`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:5dd9e244a9129dae0e2a1376f2a674d48449ffc713b4db50f43fa065a708f9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:2309ec8a0a4c528ab4b31287b1e1796db21e598834bcc725a870c431050a95ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989838238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d38376f954f629ae732ecd96e45094cc8a697e03abc2bf6a918565d5884b5b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:33:35 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:33:35 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:33:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.15/nats-server-v2.11.15-windows-amd64.zip
# Tue, 24 Mar 2026 18:33:37 GMT
ENV NATS_SERVER_SHASUM=25ffe2528406c9f0a038b3e2044edeb0220848b0eeef984d6a635071e13d073b
# Tue, 24 Mar 2026 18:33:45 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:34:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:34:07 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:34:08 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:34:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:34:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d326228f48cb794c7bb9aa65a5116873809441461fb3d90daa22e73631cdaee`  
		Last Modified: Tue, 24 Mar 2026 18:34:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8455a6abb1832f1311b97fe501dcb999801f72c18585ed3d92f67a2e7b7b1042`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397579ee30eb49948a6bf467d0a8c4098496472e451ec91e62f13de9c9d9e7b2`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c39206ad86593cb944a9eea94a53d7456be978c6f9a167e7b438309f3152b8`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94436b7f73a2569f6f5e7e64615614652f15a633d21f24f049d78726ff85db87`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 502.1 KB (502102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e68c5e1ca4b3164aa3e8e3b6ff218693d3b3a0edf9d059e3b6f5617b7622d2`  
		Last Modified: Tue, 24 Mar 2026 18:34:18 GMT  
		Size: 7.0 MB (7041118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea850075983ab6151db5dab006dc247fdebe9859a840db9f8c181162bfc5bc9b`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b337a3c72e466a7afbed061bd2926e751ece63a8bea7faf3e9f7018e1080df45`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62ab004cc600d1c8431b83a1943cf829530d17cba4dfbc76242490a62208b14`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040bc400564d6411725e3162b65902a003d97f5987f2ebc59df98ed36eda862`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.15`

```console
$ docker pull nats@sha256:0800d39b5cb258e231232318592e9d96bdf24f1518f34503272f93846a089e32
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
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11.15` - linux; amd64

```console
$ docker pull nats@sha256:6beefe4b70a2ffbb01cda9826e1d569a8a79d1f2acf01005f355e2b07606ca44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e8e4be3a366673cca39f017feff6959a97e0bf0c7532f6f46c331759df468a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:51 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:51 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7e63c3af64c8405f5d23275254d5a1685d8b6769408b1389d5cbb5e69727de9`  
		Last Modified: Tue, 24 Mar 2026 15:55:28 GMT  
		Size: 6.5 MB (6494855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec55e3b36d28a1727c9006137813c27d6115506a4e18a39cde0fb76d0e9616`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15` - unknown; unknown

```console
$ docker pull nats@sha256:f6ace49b50ed85d0cad754b01517bcef040e7a4fe048bb091d3fa602b6bdb218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2346e39fee769925c3c23b5f5d24337e60bdb07e7206ab969c9910ee9bc5`

```dockerfile
```

-	Layers:
	-	`sha256:2442aeb9d053e9aebac1749deabd69065737b708cc2ccdaf914eb2084c6cd234`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:c8f6d2e51a224517eb269d02cb9c8272bd99ad3cb7b3a90bb563133f2b2bd1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42bc1cd2a79eeac49db67b13c4f80bf93741cdd1a99e82bad3de9796c7b2f2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99fe1ed0d1a3485150391b8e0454b8178cb17fc15a68e6cad8ca54d49802a30a`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 6.2 MB (6218017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcacc6fd95141f743750760c71c1be8ab1f635e30b595eef94fac3d5306522`  
		Last Modified: Tue, 24 Mar 2026 18:39:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15` - unknown; unknown

```console
$ docker pull nats@sha256:377c745606afedf02308b7fad2f62c7240cf71b04d15e1a94c0f4703cff8fa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94d5afc50036cb3a5eba21ec11cca57e4ab2c84463b19fdfe3e3e291e7a74cf`

```dockerfile
```

-	Layers:
	-	`sha256:0a8af9199220ee3a782696072117154ef76ffc7aa0c9b42181aa09f33e979ba6`  
		Last Modified: Tue, 24 Mar 2026 18:39:53 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:055dfd0c6acf95ee1c307329df0e438ed20e7c67118b9fe2701012cc3eecdb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c52b0a01335266a8f573e23b83dff5c40a50a37df8218b7b584ee141e42fda4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:065c3ae51de74392d9d99a5b43c84d98f1960fe6ce8c355c7e4b4bf9eef4a5c4`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.2 MB (6207765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15` - unknown; unknown

```console
$ docker pull nats@sha256:288aeb087717f3d445d13febfef6ad933eecfa68ec4c55a2d9a3c9ac60fb0510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bec437861679e7e73a1bd94e866278722db4fb2c84f515f3a209368281508e`

```dockerfile
```

-	Layers:
	-	`sha256:07c1d60302821ed87af9e3c3f3e829bb0ecd68820fbc12fbd581c86759176afb`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd263bc467a1ece21cdae5119f115a03f6a14564d0996c53b4d0adf299635f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e2ca270d24eee57643c49734763d61bb3dd341f04dc9ef55a5f206aff22919`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:82f1bcf7cdc5a871f261539fd2792c122943051a252ed1974fe0f05e3c44cf68`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 5.9 MB (5914074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe75ac13e6539cf5c58ef37905585748a85c7973493c0630965332a7ffb36c0`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15` - unknown; unknown

```console
$ docker pull nats@sha256:23eb4b439edda7cbb15fd544bbfc9592dc9513c21e1aa3e095181a7496c74bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5877514342232a29d753a50754bc6a6921a450417495c4572805e6e655e8ded5`

```dockerfile
```

-	Layers:
	-	`sha256:1b6d810b6eb7d44d522f711c5c170ce2df7279c9fd90a6d5b72c09443a2316b5`  
		Last Modified: Tue, 24 Mar 2026 18:40:34 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15` - linux; ppc64le

```console
$ docker pull nats@sha256:ff62b32c9052feba1c98f26252211307c5334256189741e05b7f51735723ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1347ddb9e066d1fd367d07ed5ab9c09dd2b2a724995dc71b7ceb9d91a6ff125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a52a724beb3d6edbc8a6c1bcbf1ca075c87995b1ba8cd45c0cfc0d4105c3b00`  
		Last Modified: Tue, 24 Mar 2026 15:55:24 GMT  
		Size: 6.0 MB (5962181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6b264c693a6c247cc7d1d8799bf4318655c1291916b8e3abab01448bc62e49`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15` - unknown; unknown

```console
$ docker pull nats@sha256:6d64bb907eb2d82b924cb5b7311bc175f5b9dab6e6215d408872935564d819b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48158be55bff71e1e86262d537b30e74fd4cf81d452a481222c6fc941b75583`

```dockerfile
```

-	Layers:
	-	`sha256:9198ecc0eef93f55015b5ad1ec90d164de361b6b8888aa63b8a3f50df53d5e02`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15` - linux; s390x

```console
$ docker pull nats@sha256:7ba1afeff1c795fbfa4570ba90caaf7b32612dce3b6c22f92df9d08fb54b769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d6d26f36ddd6b3fcb03c5756a05f19575698c7e3b9193bb2227989abc92e49`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38e32835a80931455e48f3851737e748f5746d8cc85e076c87e48210d2437c30`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.3 MB (6333902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf712fe01491a02befe3d223500d656bf6c58b29898a209f9418e4d339195bb`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15` - unknown; unknown

```console
$ docker pull nats@sha256:c238441fd63b4bcb8ee269435d2239f5a0136213bac6d305a3dd7e705532d6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5f710b01fc3e3df1e867019432f69b8585870510917a65453c508367b885e5`

```dockerfile
```

-	Layers:
	-	`sha256:1518e888792ffe72daeb5ffce1c2e76b70d5c5027583377942bff9f2723b9053`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:84b335872ab1dd7e19b6fab35a2e7c6c139b12d13aa7001f09fbb0a1a31e45a4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133329674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2eace19bc689c1819b557a0aa6a86cfe6484e910cba543d483fe28f3cc66a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:28 GMT
RUN cmd /S /C #(nop) COPY file:ed1189637cf14d6f82bd62abd3ebc861a2617a31a09ae7f962048b040a639644 in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d7ab56f5d9cb0cf9d9af8a0c4e0ab9a576a3d3f3b1282a696ab132d4cd0360`  
		Last Modified: Tue, 24 Mar 2026 18:39:38 GMT  
		Size: 6.7 MB (6673215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89139a704ae0938dfa4c1b9530e208a7ab930535ec9c6df24c638ae696ea36a`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c20967f993fd513f9bfdf04e3f67ae0307388313b37638d57e10fbfd9d1cfd`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e378f20627e786391a69d075c2c1edce83a3e242d594589128be0a8d4570af`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4551ca094c842533ca2d88482c737291c0b7b089e927c2b365ed8003450a4dc2`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.15-alpine`

```console
$ docker pull nats@sha256:a7da54d489edb63f95ac9ec6c22834041d20a18a3b3413481764d7d6985aa59a
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

### `nats:2.11.15-alpine` - linux; amd64

```console
$ docker pull nats@sha256:e71a1cdced17dede784e79ef1cb38465560671cc65648ab2cf37b8e85dd2a998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10759846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4916f00b11d821bfd76cbe7ea612f64e7171067bf6c6d947df1f6df57a81cac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c629c9999718b4c6b3e4524bad2c29ae78c32a79c4daa95250b6ba1e1eab1aaa`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 7.0 MB (6954002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7233360756ffdeb22fc9a86a3a6d620c9925f338d61cf653c2f771562fd79229`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa11fa3e09b6dc7a3a8bfc68966822b618bfa1e28dfb16806110afc00b028801`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5a1882ccb45af23a1e6d7a03e11a6c34379de4653fe4697f759244b80bc2c383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea4cd6d5385dd6db79b9a50061234289d7bd084603d19184ad12d58d038dfd4`

```dockerfile
```

-	Layers:
	-	`sha256:7cab5da085c06baf637ebf4f2f3451f5d935df8d8ad344f14d4f95b6e539582b`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8929001b45eab6eaf0ed916cf5b6de266e15b868dcd98ed47e4e6a0606b3cd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10180614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0107502dbba5034afa32f69a55c30675018f7768389941b8df4459c8e5631d28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:49 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:49 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:49 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0dc2e3a53e7dfe9bf1fd1a22974bd2d659294613be2f882137d0555dd521f3`  
		Last Modified: Tue, 24 Mar 2026 18:13:54 GMT  
		Size: 6.7 MB (6674600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22826ee17c11632e573d45c662f52c9e16086b931509b08c913b644cf5753a2`  
		Last Modified: Tue, 24 Mar 2026 18:13:53 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086fd7ce839159e7cb142c22e0968bec9f9c2301046934360c730b00d83e16bd`  
		Last Modified: Tue, 24 Mar 2026 18:13:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f35d9e93231a149640d7d44feec9d33f21f9202317ca6bf0ac1f454117ce4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c8c08932d30a060bf1ea0be11f77c6dff447bbeff3437667f6a7298844a3ee`

```dockerfile
```

-	Layers:
	-	`sha256:943515928efb2421d691a3c5c316716237c0efd031a41f9bca1b621f1cae752b`  
		Last Modified: Tue, 24 Mar 2026 18:13:54 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:20d70ab66f6719f6cf8790375e43b608159c4690f387a5b3a88cc9c6f02c2ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9891953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2e339bcc0ef62e00dc9f9a87da1d175359930f50e96e2fcf56e200f80a053c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:46 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:14:46 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:14:46 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3e31ee0e1db5d78c8ebab8a6dbba9808c27d27563582b1d315f86a5260c7c`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 6.7 MB (6667355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f6f60b934e7bd07fb20a1b0a36151d3627617fb015114749ce09b2916fddf0`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaf85dadd0874ca6900a953c7661993333993768e210bb5550b1ed499d36e68`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9344184c04e86741d4c696463189817983f22d3b402f55da26b68d34c4359b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e406555c320d2b9bbf5850a193a1bb4f0ed4819afaa6c815efb97472e3e1b6d5`

```dockerfile
```

-	Layers:
	-	`sha256:d6702d41711813eb86abd00c922acd57a7aa59714bb639a19c644aa6e2ba38bc`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36507fcd1538a86bd3aee16397816942014ef98e60cf382c69e0b1a7873f9b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515d3db296da783262131ea09b404a7eeee88325deb10ed182637b235abcb55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:06 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:21:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:21:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67fc99252adb5c0ce2b9e63be9ad8a5169d555955b7d067f342d8122f3fac74`  
		Last Modified: Tue, 24 Mar 2026 18:21:11 GMT  
		Size: 6.4 MB (6374799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecb5e11849f806590b036b643a5da097e026e7c39cdeb1a37367cf6a55483cd`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93969f7f79030de2627f1e7599ebf69c7f7abb6edd6cc3a744427ee16049144`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4ecb252842e0f6e72cc520e39cb036d4e52ce14d038f0a34fe462d4b8f1aad75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ac12f685ad559ca3c645ae05f9f4477191d83250f72b8e7f9b48204aeb9d7f`

```dockerfile
```

-	Layers:
	-	`sha256:faf3c18e344bd4f44c93e42c3508e3e775a8ff94fe840e27bc10ac836fc365b9`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:120629293ebfcf410e16bb071f883706bf26721b4c1c9cd3464e0bd8253a6b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10157559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a6fc48e4a3fa6c7f9d82de810932b57b724c8aa7d9a116043029e56e108792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa49855571a70f310dc8def33262bbee295e2492166a38c2a449df058a6577`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.4 MB (6422291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e953c0818eb7566baea5faba9a891bbb7b5070778e2eead7c2acd034fab2face`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d767892645e66c28cacd5091c75449dce029986589320c668602d32772a2abb`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4db4dd0c9d0abd7b268c4244a7853de599c58ce3eb3b49a983c22437105c4d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95079863e6c20529b2f4f3dade6d11723434e4bf97dd2828fea56440c4e513f6`

```dockerfile
```

-	Layers:
	-	`sha256:0d4be26a949b1e7fabf9af3594928f1389db8f5d656e39f829441ffc459c7ae1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-alpine` - linux; s390x

```console
$ docker pull nats@sha256:481e422723267a967e57d451c9119acbab0c36f0a8476192a9239afb86b1f599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10447068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7233e45dcd427bf115ea11b2ae3ff629e54b44064d1b12155a1271540ef037eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:10 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413afd7d07ec861732bcf80918930a61263fc6607441f3820570662cd3a3cdbc`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 6.8 MB (6795667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df47538a8f294397d3aa4f0fc0323c4471e2e3a070039fcab75a9e2608a7e525`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4525ac0099c66d3e0e55f0cd35f4bec7d56a58d7d55c8bdd319cab1da0d7021e`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6c1b6331a7ec2cf433553957d23378998f62b21513e10e848425b9d0d924205b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cc7799beae56f6603ac257802e481fdddbf767159e7e80d7e7db888d250127`

```dockerfile
```

-	Layers:
	-	`sha256:2e2457bdb66ca67af83180c43c59ba4a4cf3c837f80a1f3a8df7a5ab5483ba90`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.15-alpine3.22`

```console
$ docker pull nats@sha256:a7da54d489edb63f95ac9ec6c22834041d20a18a3b3413481764d7d6985aa59a
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

### `nats:2.11.15-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:e71a1cdced17dede784e79ef1cb38465560671cc65648ab2cf37b8e85dd2a998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10759846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4916f00b11d821bfd76cbe7ea612f64e7171067bf6c6d947df1f6df57a81cac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c629c9999718b4c6b3e4524bad2c29ae78c32a79c4daa95250b6ba1e1eab1aaa`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 7.0 MB (6954002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7233360756ffdeb22fc9a86a3a6d620c9925f338d61cf653c2f771562fd79229`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa11fa3e09b6dc7a3a8bfc68966822b618bfa1e28dfb16806110afc00b028801`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5a1882ccb45af23a1e6d7a03e11a6c34379de4653fe4697f759244b80bc2c383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea4cd6d5385dd6db79b9a50061234289d7bd084603d19184ad12d58d038dfd4`

```dockerfile
```

-	Layers:
	-	`sha256:7cab5da085c06baf637ebf4f2f3451f5d935df8d8ad344f14d4f95b6e539582b`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:8929001b45eab6eaf0ed916cf5b6de266e15b868dcd98ed47e4e6a0606b3cd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10180614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0107502dbba5034afa32f69a55c30675018f7768389941b8df4459c8e5631d28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:49 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:49 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:49 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0dc2e3a53e7dfe9bf1fd1a22974bd2d659294613be2f882137d0555dd521f3`  
		Last Modified: Tue, 24 Mar 2026 18:13:54 GMT  
		Size: 6.7 MB (6674600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22826ee17c11632e573d45c662f52c9e16086b931509b08c913b644cf5753a2`  
		Last Modified: Tue, 24 Mar 2026 18:13:53 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086fd7ce839159e7cb142c22e0968bec9f9c2301046934360c730b00d83e16bd`  
		Last Modified: Tue, 24 Mar 2026 18:13:53 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2f35d9e93231a149640d7d44feec9d33f21f9202317ca6bf0ac1f454117ce4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c8c08932d30a060bf1ea0be11f77c6dff447bbeff3437667f6a7298844a3ee`

```dockerfile
```

-	Layers:
	-	`sha256:943515928efb2421d691a3c5c316716237c0efd031a41f9bca1b621f1cae752b`  
		Last Modified: Tue, 24 Mar 2026 18:13:54 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:20d70ab66f6719f6cf8790375e43b608159c4690f387a5b3a88cc9c6f02c2ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9891953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2e339bcc0ef62e00dc9f9a87da1d175359930f50e96e2fcf56e200f80a053c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:46 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:14:46 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:14:46 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c3e31ee0e1db5d78c8ebab8a6dbba9808c27d27563582b1d315f86a5260c7c`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 6.7 MB (6667355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f6f60b934e7bd07fb20a1b0a36151d3627617fb015114749ce09b2916fddf0`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaf85dadd0874ca6900a953c7661993333993768e210bb5550b1ed499d36e68`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9344184c04e86741d4c696463189817983f22d3b402f55da26b68d34c4359b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e406555c320d2b9bbf5850a193a1bb4f0ed4819afaa6c815efb97472e3e1b6d5`

```dockerfile
```

-	Layers:
	-	`sha256:d6702d41711813eb86abd00c922acd57a7aa59714bb639a19c644aa6e2ba38bc`  
		Last Modified: Tue, 24 Mar 2026 18:14:51 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:36507fcd1538a86bd3aee16397816942014ef98e60cf382c69e0b1a7873f9b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515d3db296da783262131ea09b404a7eeee88325deb10ed182637b235abcb55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:06 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:21:06 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:21:06 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67fc99252adb5c0ce2b9e63be9ad8a5169d555955b7d067f342d8122f3fac74`  
		Last Modified: Tue, 24 Mar 2026 18:21:11 GMT  
		Size: 6.4 MB (6374799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecb5e11849f806590b036b643a5da097e026e7c39cdeb1a37367cf6a55483cd`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93969f7f79030de2627f1e7599ebf69c7f7abb6edd6cc3a744427ee16049144`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4ecb252842e0f6e72cc520e39cb036d4e52ce14d038f0a34fe462d4b8f1aad75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ac12f685ad559ca3c645ae05f9f4477191d83250f72b8e7f9b48204aeb9d7f`

```dockerfile
```

-	Layers:
	-	`sha256:faf3c18e344bd4f44c93e42c3508e3e775a8ff94fe840e27bc10ac836fc365b9`  
		Last Modified: Tue, 24 Mar 2026 18:21:10 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:120629293ebfcf410e16bb071f883706bf26721b4c1c9cd3464e0bd8253a6b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10157559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a6fc48e4a3fa6c7f9d82de810932b57b724c8aa7d9a116043029e56e108792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fa49855571a70f310dc8def33262bbee295e2492166a38c2a449df058a6577`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.4 MB (6422291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e953c0818eb7566baea5faba9a891bbb7b5070778e2eead7c2acd034fab2face`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d767892645e66c28cacd5091c75449dce029986589320c668602d32772a2abb`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4db4dd0c9d0abd7b268c4244a7853de599c58ce3eb3b49a983c22437105c4d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95079863e6c20529b2f4f3dade6d11723434e4bf97dd2828fea56440c4e513f6`

```dockerfile
```

-	Layers:
	-	`sha256:0d4be26a949b1e7fabf9af3594928f1389db8f5d656e39f829441ffc459c7ae1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:481e422723267a967e57d451c9119acbab0c36f0a8476192a9239afb86b1f599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10447068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7233e45dcd427bf115ea11b2ae3ff629e54b44064d1b12155a1271540ef037eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:10 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:13:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:13:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='0745274620731eab1a6463609f8291589e5a408356411e7dc89cf4bd5747684e' ;;     armhf) natsArch='arm6'; sha256='cd11a96b5a8707c3a76a3a41ddf7404b7c1a5b4794c7ee4c1c2377ebf7b6bdc1' ;;     armv7) natsArch='arm7'; sha256='8dd7965446ab48d0f5faa3bfbf899c44d991a504a5c9d9fe88ffe15ee541d114' ;;     x86_64) natsArch='amd64'; sha256='7035d70262d1ce85d0f58df6530be3eab16c7ebe0eaa4d48868460c796e87cb4' ;;     x86) natsArch='386'; sha256='9b66a56df40b827d9f186a5f586a56babc85188f736f4748d034e8dee39a6c7b' ;;     s390x) natsArch='s390x'; sha256='fa2ad3e10a9f9fe733bc8ced81025cce0a1ca7e96889b30e1c97ab147e1deaef' ;;     ppc64le) natsArch='ppc64le'; sha256='c3cbda79292ee463c5422dc4f51a6ce09f837a33c716657893592e301555b97b' ;;     loong64) natsArch='loong64'; sha256='19900ea0e0fff742cbb40af5e387cb1b8deb7d1cb1101d07c6b2222bdf132636' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413afd7d07ec861732bcf80918930a61263fc6607441f3820570662cd3a3cdbc`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 6.8 MB (6795667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df47538a8f294397d3aa4f0fc0323c4471e2e3a070039fcab75a9e2608a7e525`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4525ac0099c66d3e0e55f0cd35f4bec7d56a58d7d55c8bdd319cab1da0d7021e`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6c1b6331a7ec2cf433553957d23378998f62b21513e10e848425b9d0d924205b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cc7799beae56f6603ac257802e481fdddbf767159e7e80d7e7db888d250127`

```dockerfile
```

-	Layers:
	-	`sha256:2e2457bdb66ca67af83180c43c59ba4a4cf3c837f80a1f3a8df7a5ab5483ba90`  
		Last Modified: Tue, 24 Mar 2026 18:13:17 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.15-linux`

```console
$ docker pull nats@sha256:f83065787c094e3315c60e7ded5cf05694675c77b116f5b15e5aeffced804804
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

### `nats:2.11.15-linux` - linux; amd64

```console
$ docker pull nats@sha256:6beefe4b70a2ffbb01cda9826e1d569a8a79d1f2acf01005f355e2b07606ca44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e8e4be3a366673cca39f017feff6959a97e0bf0c7532f6f46c331759df468a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:51 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:51 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7e63c3af64c8405f5d23275254d5a1685d8b6769408b1389d5cbb5e69727de9`  
		Last Modified: Tue, 24 Mar 2026 15:55:28 GMT  
		Size: 6.5 MB (6494855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec55e3b36d28a1727c9006137813c27d6115506a4e18a39cde0fb76d0e9616`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6ace49b50ed85d0cad754b01517bcef040e7a4fe048bb091d3fa602b6bdb218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2346e39fee769925c3c23b5f5d24337e60bdb07e7206ab969c9910ee9bc5`

```dockerfile
```

-	Layers:
	-	`sha256:2442aeb9d053e9aebac1749deabd69065737b708cc2ccdaf914eb2084c6cd234`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:c8f6d2e51a224517eb269d02cb9c8272bd99ad3cb7b3a90bb563133f2b2bd1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42bc1cd2a79eeac49db67b13c4f80bf93741cdd1a99e82bad3de9796c7b2f2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99fe1ed0d1a3485150391b8e0454b8178cb17fc15a68e6cad8ca54d49802a30a`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 6.2 MB (6218017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcacc6fd95141f743750760c71c1be8ab1f635e30b595eef94fac3d5306522`  
		Last Modified: Tue, 24 Mar 2026 18:39:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-linux` - unknown; unknown

```console
$ docker pull nats@sha256:377c745606afedf02308b7fad2f62c7240cf71b04d15e1a94c0f4703cff8fa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94d5afc50036cb3a5eba21ec11cca57e4ab2c84463b19fdfe3e3e291e7a74cf`

```dockerfile
```

-	Layers:
	-	`sha256:0a8af9199220ee3a782696072117154ef76ffc7aa0c9b42181aa09f33e979ba6`  
		Last Modified: Tue, 24 Mar 2026 18:39:53 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:055dfd0c6acf95ee1c307329df0e438ed20e7c67118b9fe2701012cc3eecdb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c52b0a01335266a8f573e23b83dff5c40a50a37df8218b7b584ee141e42fda4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:065c3ae51de74392d9d99a5b43c84d98f1960fe6ce8c355c7e4b4bf9eef4a5c4`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.2 MB (6207765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-linux` - unknown; unknown

```console
$ docker pull nats@sha256:288aeb087717f3d445d13febfef6ad933eecfa68ec4c55a2d9a3c9ac60fb0510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bec437861679e7e73a1bd94e866278722db4fb2c84f515f3a209368281508e`

```dockerfile
```

-	Layers:
	-	`sha256:07c1d60302821ed87af9e3c3f3e829bb0ecd68820fbc12fbd581c86759176afb`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd263bc467a1ece21cdae5119f115a03f6a14564d0996c53b4d0adf299635f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e2ca270d24eee57643c49734763d61bb3dd341f04dc9ef55a5f206aff22919`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:82f1bcf7cdc5a871f261539fd2792c122943051a252ed1974fe0f05e3c44cf68`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 5.9 MB (5914074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe75ac13e6539cf5c58ef37905585748a85c7973493c0630965332a7ffb36c0`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-linux` - unknown; unknown

```console
$ docker pull nats@sha256:23eb4b439edda7cbb15fd544bbfc9592dc9513c21e1aa3e095181a7496c74bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5877514342232a29d753a50754bc6a6921a450417495c4572805e6e655e8ded5`

```dockerfile
```

-	Layers:
	-	`sha256:1b6d810b6eb7d44d522f711c5c170ce2df7279c9fd90a6d5b72c09443a2316b5`  
		Last Modified: Tue, 24 Mar 2026 18:40:34 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:ff62b32c9052feba1c98f26252211307c5334256189741e05b7f51735723ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1347ddb9e066d1fd367d07ed5ab9c09dd2b2a724995dc71b7ceb9d91a6ff125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a52a724beb3d6edbc8a6c1bcbf1ca075c87995b1ba8cd45c0cfc0d4105c3b00`  
		Last Modified: Tue, 24 Mar 2026 15:55:24 GMT  
		Size: 6.0 MB (5962181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6b264c693a6c247cc7d1d8799bf4318655c1291916b8e3abab01448bc62e49`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6d64bb907eb2d82b924cb5b7311bc175f5b9dab6e6215d408872935564d819b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48158be55bff71e1e86262d537b30e74fd4cf81d452a481222c6fc941b75583`

```dockerfile
```

-	Layers:
	-	`sha256:9198ecc0eef93f55015b5ad1ec90d164de361b6b8888aa63b8a3f50df53d5e02`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-linux` - linux; s390x

```console
$ docker pull nats@sha256:7ba1afeff1c795fbfa4570ba90caaf7b32612dce3b6c22f92df9d08fb54b769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d6d26f36ddd6b3fcb03c5756a05f19575698c7e3b9193bb2227989abc92e49`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38e32835a80931455e48f3851737e748f5746d8cc85e076c87e48210d2437c30`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.3 MB (6333902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf712fe01491a02befe3d223500d656bf6c58b29898a209f9418e4d339195bb`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c238441fd63b4bcb8ee269435d2239f5a0136213bac6d305a3dd7e705532d6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5f710b01fc3e3df1e867019432f69b8585870510917a65453c508367b885e5`

```dockerfile
```

-	Layers:
	-	`sha256:1518e888792ffe72daeb5ffce1c2e76b70d5c5027583377942bff9f2723b9053`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.15-nanoserver`

```console
$ docker pull nats@sha256:a45756f638afc778a0b6818abb7d451f97670e72263bde178811d1dbf6314bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11.15-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:84b335872ab1dd7e19b6fab35a2e7c6c139b12d13aa7001f09fbb0a1a31e45a4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133329674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2eace19bc689c1819b557a0aa6a86cfe6484e910cba543d483fe28f3cc66a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:28 GMT
RUN cmd /S /C #(nop) COPY file:ed1189637cf14d6f82bd62abd3ebc861a2617a31a09ae7f962048b040a639644 in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d7ab56f5d9cb0cf9d9af8a0c4e0ab9a576a3d3f3b1282a696ab132d4cd0360`  
		Last Modified: Tue, 24 Mar 2026 18:39:38 GMT  
		Size: 6.7 MB (6673215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89139a704ae0938dfa4c1b9530e208a7ab930535ec9c6df24c638ae696ea36a`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c20967f993fd513f9bfdf04e3f67ae0307388313b37638d57e10fbfd9d1cfd`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e378f20627e786391a69d075c2c1edce83a3e242d594589128be0a8d4570af`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4551ca094c842533ca2d88482c737291c0b7b089e927c2b365ed8003450a4dc2`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.15-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:a45756f638afc778a0b6818abb7d451f97670e72263bde178811d1dbf6314bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11.15-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:84b335872ab1dd7e19b6fab35a2e7c6c139b12d13aa7001f09fbb0a1a31e45a4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133329674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2eace19bc689c1819b557a0aa6a86cfe6484e910cba543d483fe28f3cc66a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:28 GMT
RUN cmd /S /C #(nop) COPY file:ed1189637cf14d6f82bd62abd3ebc861a2617a31a09ae7f962048b040a639644 in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:30 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d7ab56f5d9cb0cf9d9af8a0c4e0ab9a576a3d3f3b1282a696ab132d4cd0360`  
		Last Modified: Tue, 24 Mar 2026 18:39:38 GMT  
		Size: 6.7 MB (6673215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89139a704ae0938dfa4c1b9530e208a7ab930535ec9c6df24c638ae696ea36a`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c20967f993fd513f9bfdf04e3f67ae0307388313b37638d57e10fbfd9d1cfd`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e378f20627e786391a69d075c2c1edce83a3e242d594589128be0a8d4570af`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4551ca094c842533ca2d88482c737291c0b7b089e927c2b365ed8003450a4dc2`  
		Last Modified: Tue, 24 Mar 2026 18:39:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.15-scratch`

```console
$ docker pull nats@sha256:f83065787c094e3315c60e7ded5cf05694675c77b116f5b15e5aeffced804804
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

### `nats:2.11.15-scratch` - linux; amd64

```console
$ docker pull nats@sha256:6beefe4b70a2ffbb01cda9826e1d569a8a79d1f2acf01005f355e2b07606ca44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6495364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e8e4be3a366673cca39f017feff6959a97e0bf0c7532f6f46c331759df468a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:51 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:51 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7e63c3af64c8405f5d23275254d5a1685d8b6769408b1389d5cbb5e69727de9`  
		Last Modified: Tue, 24 Mar 2026 15:55:28 GMT  
		Size: 6.5 MB (6494855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec55e3b36d28a1727c9006137813c27d6115506a4e18a39cde0fb76d0e9616`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f6ace49b50ed85d0cad754b01517bcef040e7a4fe048bb091d3fa602b6bdb218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2346e39fee769925c3c23b5f5d24337e60bdb07e7206ab969c9910ee9bc5`

```dockerfile
```

-	Layers:
	-	`sha256:2442aeb9d053e9aebac1749deabd69065737b708cc2ccdaf914eb2084c6cd234`  
		Last Modified: Tue, 24 Mar 2026 18:40:55 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:c8f6d2e51a224517eb269d02cb9c8272bd99ad3cb7b3a90bb563133f2b2bd1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42bc1cd2a79eeac49db67b13c4f80bf93741cdd1a99e82bad3de9796c7b2f2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:99fe1ed0d1a3485150391b8e0454b8178cb17fc15a68e6cad8ca54d49802a30a`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 6.2 MB (6218017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcacc6fd95141f743750760c71c1be8ab1f635e30b595eef94fac3d5306522`  
		Last Modified: Tue, 24 Mar 2026 18:39:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:377c745606afedf02308b7fad2f62c7240cf71b04d15e1a94c0f4703cff8fa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94d5afc50036cb3a5eba21ec11cca57e4ab2c84463b19fdfe3e3e291e7a74cf`

```dockerfile
```

-	Layers:
	-	`sha256:0a8af9199220ee3a782696072117154ef76ffc7aa0c9b42181aa09f33e979ba6`  
		Last Modified: Tue, 24 Mar 2026 18:39:53 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:055dfd0c6acf95ee1c307329df0e438ed20e7c67118b9fe2701012cc3eecdb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c52b0a01335266a8f573e23b83dff5c40a50a37df8218b7b584ee141e42fda4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:065c3ae51de74392d9d99a5b43c84d98f1960fe6ce8c355c7e4b4bf9eef4a5c4`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.2 MB (6207765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:288aeb087717f3d445d13febfef6ad933eecfa68ec4c55a2d9a3c9ac60fb0510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bec437861679e7e73a1bd94e866278722db4fb2c84f515f3a209368281508e`

```dockerfile
```

-	Layers:
	-	`sha256:07c1d60302821ed87af9e3c3f3e829bb0ecd68820fbc12fbd581c86759176afb`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fd263bc467a1ece21cdae5119f115a03f6a14564d0996c53b4d0adf299635f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e2ca270d24eee57643c49734763d61bb3dd341f04dc9ef55a5f206aff22919`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:31 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:31 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:31 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:82f1bcf7cdc5a871f261539fd2792c122943051a252ed1974fe0f05e3c44cf68`  
		Last Modified: Tue, 24 Mar 2026 15:55:25 GMT  
		Size: 5.9 MB (5914074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe75ac13e6539cf5c58ef37905585748a85c7973493c0630965332a7ffb36c0`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:23eb4b439edda7cbb15fd544bbfc9592dc9513c21e1aa3e095181a7496c74bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5877514342232a29d753a50754bc6a6921a450417495c4572805e6e655e8ded5`

```dockerfile
```

-	Layers:
	-	`sha256:1b6d810b6eb7d44d522f711c5c170ce2df7279c9fd90a6d5b72c09443a2316b5`  
		Last Modified: Tue, 24 Mar 2026 18:40:34 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:ff62b32c9052feba1c98f26252211307c5334256189741e05b7f51735723ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1347ddb9e066d1fd367d07ed5ab9c09dd2b2a724995dc71b7ceb9d91a6ff125`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7a52a724beb3d6edbc8a6c1bcbf1ca075c87995b1ba8cd45c0cfc0d4105c3b00`  
		Last Modified: Tue, 24 Mar 2026 15:55:24 GMT  
		Size: 6.0 MB (5962181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6b264c693a6c247cc7d1d8799bf4318655c1291916b8e3abab01448bc62e49`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6d64bb907eb2d82b924cb5b7311bc175f5b9dab6e6215d408872935564d819b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48158be55bff71e1e86262d537b30e74fd4cf81d452a481222c6fc941b75583`

```dockerfile
```

-	Layers:
	-	`sha256:9198ecc0eef93f55015b5ad1ec90d164de361b6b8888aa63b8a3f50df53d5e02`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.15-scratch` - linux; s390x

```console
$ docker pull nats@sha256:7ba1afeff1c795fbfa4570ba90caaf7b32612dce3b6c22f92df9d08fb54b769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6334412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d6d26f36ddd6b3fcb03c5756a05f19575698c7e3b9193bb2227989abc92e49`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:38e32835a80931455e48f3851737e748f5746d8cc85e076c87e48210d2437c30`  
		Last Modified: Tue, 24 Mar 2026 15:55:29 GMT  
		Size: 6.3 MB (6333902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf712fe01491a02befe3d223500d656bf6c58b29898a209f9418e4d339195bb`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.15-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c238441fd63b4bcb8ee269435d2239f5a0136213bac6d305a3dd7e705532d6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5f710b01fc3e3df1e867019432f69b8585870510917a65453c508367b885e5`

```dockerfile
```

-	Layers:
	-	`sha256:1518e888792ffe72daeb5ffce1c2e76b70d5c5027583377942bff9f2723b9053`  
		Last Modified: Tue, 24 Mar 2026 18:39:26 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.15-windowsservercore`

```console
$ docker pull nats@sha256:5dd9e244a9129dae0e2a1376f2a674d48449ffc713b4db50f43fa065a708f9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11.15-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:2309ec8a0a4c528ab4b31287b1e1796db21e598834bcc725a870c431050a95ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989838238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d38376f954f629ae732ecd96e45094cc8a697e03abc2bf6a918565d5884b5b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:33:35 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:33:35 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:33:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.15/nats-server-v2.11.15-windows-amd64.zip
# Tue, 24 Mar 2026 18:33:37 GMT
ENV NATS_SERVER_SHASUM=25ffe2528406c9f0a038b3e2044edeb0220848b0eeef984d6a635071e13d073b
# Tue, 24 Mar 2026 18:33:45 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:34:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:34:07 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:34:08 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:34:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:34:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d326228f48cb794c7bb9aa65a5116873809441461fb3d90daa22e73631cdaee`  
		Last Modified: Tue, 24 Mar 2026 18:34:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8455a6abb1832f1311b97fe501dcb999801f72c18585ed3d92f67a2e7b7b1042`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397579ee30eb49948a6bf467d0a8c4098496472e451ec91e62f13de9c9d9e7b2`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c39206ad86593cb944a9eea94a53d7456be978c6f9a167e7b438309f3152b8`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94436b7f73a2569f6f5e7e64615614652f15a633d21f24f049d78726ff85db87`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 502.1 KB (502102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e68c5e1ca4b3164aa3e8e3b6ff218693d3b3a0edf9d059e3b6f5617b7622d2`  
		Last Modified: Tue, 24 Mar 2026 18:34:18 GMT  
		Size: 7.0 MB (7041118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea850075983ab6151db5dab006dc247fdebe9859a840db9f8c181162bfc5bc9b`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b337a3c72e466a7afbed061bd2926e751ece63a8bea7faf3e9f7018e1080df45`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62ab004cc600d1c8431b83a1943cf829530d17cba4dfbc76242490a62208b14`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040bc400564d6411725e3162b65902a003d97f5987f2ebc59df98ed36eda862`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.15-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:5dd9e244a9129dae0e2a1376f2a674d48449ffc713b4db50f43fa065a708f9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.11.15-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:2309ec8a0a4c528ab4b31287b1e1796db21e598834bcc725a870c431050a95ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989838238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d38376f954f629ae732ecd96e45094cc8a697e03abc2bf6a918565d5884b5b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:33:35 GMT
ENV NATS_SERVER=2.11.15
# Tue, 24 Mar 2026 18:33:35 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.15
# Tue, 24 Mar 2026 18:33:36 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.15/nats-server-v2.11.15-windows-amd64.zip
# Tue, 24 Mar 2026 18:33:37 GMT
ENV NATS_SERVER_SHASUM=25ffe2528406c9f0a038b3e2044edeb0220848b0eeef984d6a635071e13d073b
# Tue, 24 Mar 2026 18:33:45 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:34:07 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:34:07 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:34:08 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:34:08 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:34:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d326228f48cb794c7bb9aa65a5116873809441461fb3d90daa22e73631cdaee`  
		Last Modified: Tue, 24 Mar 2026 18:34:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8455a6abb1832f1311b97fe501dcb999801f72c18585ed3d92f67a2e7b7b1042`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397579ee30eb49948a6bf467d0a8c4098496472e451ec91e62f13de9c9d9e7b2`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c39206ad86593cb944a9eea94a53d7456be978c6f9a167e7b438309f3152b8`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94436b7f73a2569f6f5e7e64615614652f15a633d21f24f049d78726ff85db87`  
		Last Modified: Tue, 24 Mar 2026 18:34:15 GMT  
		Size: 502.1 KB (502102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e68c5e1ca4b3164aa3e8e3b6ff218693d3b3a0edf9d059e3b6f5617b7622d2`  
		Last Modified: Tue, 24 Mar 2026 18:34:18 GMT  
		Size: 7.0 MB (7041118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea850075983ab6151db5dab006dc247fdebe9859a840db9f8c181162bfc5bc9b`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b337a3c72e466a7afbed061bd2926e751ece63a8bea7faf3e9f7018e1080df45`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62ab004cc600d1c8431b83a1943cf829530d17cba4dfbc76242490a62208b14`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040bc400564d6411725e3162b65902a003d97f5987f2ebc59df98ed36eda862`  
		Last Modified: Tue, 24 Mar 2026 18:34:13 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12`

```console
$ docker pull nats@sha256:24e20d33a7214208b1cb699c2e4ebfbed32f7a30b41c18b36be75f019a96616c
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
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12` - linux; amd64

```console
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-alpine`

```console
$ docker pull nats@sha256:1cfc36e2e5e638243d8c722f72c954cd0ec4b15ee82fadbc718ce12e2b3c1652
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
$ docker pull nats@sha256:5bb4bf05e7b13ab68145d526ddcf7cd9b122ab4e9be396318b470fbb3db56cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10901603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6289e36de6a653c3a6fdf4c209ab5af57ddc1e4df304025e5b0319578c5de58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724b6d79b0328c1e41c2e402e40355a84657fd655ea7a04d70e56ef30d88e8d`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 7.1 MB (7095760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba8f8d786c0db5eca6a8142087d4b4f7f7ed64e4f273875c72e0ad427ddf121`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc12736b5f7dcd0aa0232b895c2814f574271450bdd11216c09df4166309c8`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:919d5a1842b84c6b23cb36b4520926b9354c437266edf1f27431ad586e66800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f7b6f48ee2d002cdfd9aacb5c4133eb01d8739a2a8d35d325ea2888c14086f`

```dockerfile
```

-	Layers:
	-	`sha256:930d7ae9e007d75b212ac2cc214b7bcd2ab2e84cacca424823b100cdf48e9834`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:14385cdceab398aa6dd31fd51a8d0eb48f42a9d9a9c8baa88a4ba8a2d0e6d23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db147dcb95e7238e38282e2c4ae9aaa5458bc3e9f34d986671345b0add344f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dd16a263fb7b1c26ba67d42231ee535f3d00df3fe3d4f5238711e29683dbb8`  
		Last Modified: Tue, 24 Mar 2026 18:13:42 GMT  
		Size: 6.8 MB (6815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec38e01326bb918550c36013b0b0e623f7982193707ffc9aa2039204670bbf`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8594a1e0b9d5ba01c5f7247e80cd021b8a3f1b8506d38915575ada877f132f22`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ffd7509c5c7f864d7afff95c068a34f1ca118c768bdca9420ee11046979332f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150020eb28e70d47c0ab5cf9a194589fc277d61e2d9fbdd92ea9c8c455ddc134`

```dockerfile
```

-	Layers:
	-	`sha256:ad2785802c0f18173a579ea09f8a176800c7b83e75133ac73b642a19dece30a4`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8d06b4be0657e317e6fb3f38328294c42c2006e1b8f4f36a703a3fb830799bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fbb045461dbfe04fea74b58c92e0717a120b330d96769922081255eb66162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc4bc127449c7715baf7736c50c8753a177bb234c94a8fd7232fd208006f28`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 6.8 MB (6801564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c2fb00e3905b6cef1c48a75670171e564c04556824be30ba32b633016f1507`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f42b05edd76961960f90d1423d0cbd73d62026f6de01455b7a5cf8bcb3c6b7`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4b4c651289e935e8cb85348a1cffb88cce5d1f34582da27a3352e2a91484ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f995cd5707bf9bac5e586042d4329d1fe2559673e4228b8bf4fb5e009e75587`

```dockerfile
```

-	Layers:
	-	`sha256:4f1cae97aebe3d7bacb664be9a66dff39c030b1cf24216b8d339e9e02787fea0`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:38a21bc067dd790300a33c7a77df288526a88d03808b328a9eabe8d13b152a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10641789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564348acc3c55422d9537181b01dfa0d9d6cf275964069c2fd10b25b8dda339`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383bfc032c7f2638ebfce96b0976e02ee30dcd64cdd4b1a0b23012ea2f78718`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 6.5 MB (6501302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd5bf99f5370727619bf2f95ee9315d3b144ddbf1b3ac8e19a907638ef8ebb`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01ba58374b0a722748241e4256b7bd0dbf522f999248b0ae2269a437263eb5`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6dd0076c1cd64737f8de4b7333e624dfe55173329fb2bac1010522d0b435cdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72caa6f6852373a1ace85c8e8fa5d990923b87e473a50fd58427f20eab29eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:8ef47ff5baeebf3463deb04fb68fb758a95f5ff00412a157f52a285f56482fc7`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:b57e19246c78c3589fb6d2a2d7b57d30e9a8f26a5dea9ecf06278eb47f41ce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e681b291aba2493b6548c5c72f81addeb967503bb75bf7cf22d689c7485b4d2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:57 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152168711ce043c658e36a34e2fd496c19c723f91680ec04f28e212e6b20451`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.6 MB (6550474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba6028f2ec6815bede0ce5a102ff4bf694edd8bd6cc576002e29592d253d9a`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00127979287ad785bdbfea091d652471cb758c03d8b0dd75a34262462608bdb5`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:53acfbd102851dc8657ed52c0adeb138ab2f4f98998712113c290468e44b627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c97473b65b616ab5c4187d1c87706c2ac01ee00d37f590e151ab7390b2d537b`

```dockerfile
```

-	Layers:
	-	`sha256:ae32e72632dade7a0e851b51611d6cb44dd2b476e62c370c017b15f9f02df2d1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:0b96d8319dc5a7fccd30e6b28dfa53bf4a55c113ac3d2f905c900de31bbdc90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8a578d8c5fc8897c630a0895dddec8179595f2038c6902307485a3f14cace0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f13fc4ac0665282379187825661bac82224da72b34bac38edbc43050b2c6e`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 6.9 MB (6934327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a19b2713e4ee80cf7b9d33d33ba4d0a52228b2fa7eb14e1182905f99f1a137`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef841b2f70cfab0cb037b8b542ea4f1700328311b69209d7fa5d50f7bafb99ed`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cd39df443a3b3b87bb26196bddb0601fc93613f151a051eb0bb1743bdd2a97d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3dd97cc216c9d1ad2f0e9b34ce573244908160be058b01282c4190c32c6d7`

```dockerfile
```

-	Layers:
	-	`sha256:5b786517ad8b86d4c95e63a0440e89692600c9115a3c414313d362bb5b4e1b36`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:1cfc36e2e5e638243d8c722f72c954cd0ec4b15ee82fadbc718ce12e2b3c1652
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
$ docker pull nats@sha256:5bb4bf05e7b13ab68145d526ddcf7cd9b122ab4e9be396318b470fbb3db56cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10901603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6289e36de6a653c3a6fdf4c209ab5af57ddc1e4df304025e5b0319578c5de58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724b6d79b0328c1e41c2e402e40355a84657fd655ea7a04d70e56ef30d88e8d`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 7.1 MB (7095760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba8f8d786c0db5eca6a8142087d4b4f7f7ed64e4f273875c72e0ad427ddf121`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc12736b5f7dcd0aa0232b895c2814f574271450bdd11216c09df4166309c8`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:919d5a1842b84c6b23cb36b4520926b9354c437266edf1f27431ad586e66800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f7b6f48ee2d002cdfd9aacb5c4133eb01d8739a2a8d35d325ea2888c14086f`

```dockerfile
```

-	Layers:
	-	`sha256:930d7ae9e007d75b212ac2cc214b7bcd2ab2e84cacca424823b100cdf48e9834`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:14385cdceab398aa6dd31fd51a8d0eb48f42a9d9a9c8baa88a4ba8a2d0e6d23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db147dcb95e7238e38282e2c4ae9aaa5458bc3e9f34d986671345b0add344f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dd16a263fb7b1c26ba67d42231ee535f3d00df3fe3d4f5238711e29683dbb8`  
		Last Modified: Tue, 24 Mar 2026 18:13:42 GMT  
		Size: 6.8 MB (6815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec38e01326bb918550c36013b0b0e623f7982193707ffc9aa2039204670bbf`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8594a1e0b9d5ba01c5f7247e80cd021b8a3f1b8506d38915575ada877f132f22`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ffd7509c5c7f864d7afff95c068a34f1ca118c768bdca9420ee11046979332f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150020eb28e70d47c0ab5cf9a194589fc277d61e2d9fbdd92ea9c8c455ddc134`

```dockerfile
```

-	Layers:
	-	`sha256:ad2785802c0f18173a579ea09f8a176800c7b83e75133ac73b642a19dece30a4`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8d06b4be0657e317e6fb3f38328294c42c2006e1b8f4f36a703a3fb830799bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fbb045461dbfe04fea74b58c92e0717a120b330d96769922081255eb66162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc4bc127449c7715baf7736c50c8753a177bb234c94a8fd7232fd208006f28`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 6.8 MB (6801564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c2fb00e3905b6cef1c48a75670171e564c04556824be30ba32b633016f1507`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f42b05edd76961960f90d1423d0cbd73d62026f6de01455b7a5cf8bcb3c6b7`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4b4c651289e935e8cb85348a1cffb88cce5d1f34582da27a3352e2a91484ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f995cd5707bf9bac5e586042d4329d1fe2559673e4228b8bf4fb5e009e75587`

```dockerfile
```

-	Layers:
	-	`sha256:4f1cae97aebe3d7bacb664be9a66dff39c030b1cf24216b8d339e9e02787fea0`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:38a21bc067dd790300a33c7a77df288526a88d03808b328a9eabe8d13b152a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10641789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564348acc3c55422d9537181b01dfa0d9d6cf275964069c2fd10b25b8dda339`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383bfc032c7f2638ebfce96b0976e02ee30dcd64cdd4b1a0b23012ea2f78718`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 6.5 MB (6501302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd5bf99f5370727619bf2f95ee9315d3b144ddbf1b3ac8e19a907638ef8ebb`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01ba58374b0a722748241e4256b7bd0dbf522f999248b0ae2269a437263eb5`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6dd0076c1cd64737f8de4b7333e624dfe55173329fb2bac1010522d0b435cdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72caa6f6852373a1ace85c8e8fa5d990923b87e473a50fd58427f20eab29eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:8ef47ff5baeebf3463deb04fb68fb758a95f5ff00412a157f52a285f56482fc7`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:b57e19246c78c3589fb6d2a2d7b57d30e9a8f26a5dea9ecf06278eb47f41ce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e681b291aba2493b6548c5c72f81addeb967503bb75bf7cf22d689c7485b4d2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:57 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152168711ce043c658e36a34e2fd496c19c723f91680ec04f28e212e6b20451`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.6 MB (6550474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba6028f2ec6815bede0ce5a102ff4bf694edd8bd6cc576002e29592d253d9a`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00127979287ad785bdbfea091d652471cb758c03d8b0dd75a34262462608bdb5`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:53acfbd102851dc8657ed52c0adeb138ab2f4f98998712113c290468e44b627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c97473b65b616ab5c4187d1c87706c2ac01ee00d37f590e151ab7390b2d537b`

```dockerfile
```

-	Layers:
	-	`sha256:ae32e72632dade7a0e851b51611d6cb44dd2b476e62c370c017b15f9f02df2d1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0b96d8319dc5a7fccd30e6b28dfa53bf4a55c113ac3d2f905c900de31bbdc90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8a578d8c5fc8897c630a0895dddec8179595f2038c6902307485a3f14cace0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f13fc4ac0665282379187825661bac82224da72b34bac38edbc43050b2c6e`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 6.9 MB (6934327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a19b2713e4ee80cf7b9d33d33ba4d0a52228b2fa7eb14e1182905f99f1a137`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef841b2f70cfab0cb037b8b542ea4f1700328311b69209d7fa5d50f7bafb99ed`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cd39df443a3b3b87bb26196bddb0601fc93613f151a051eb0bb1743bdd2a97d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3dd97cc216c9d1ad2f0e9b34ce573244908160be058b01282c4190c32c6d7`

```dockerfile
```

-	Layers:
	-	`sha256:5b786517ad8b86d4c95e63a0440e89692600c9115a3c414313d362bb5b4e1b36`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:81fb519cf3229a15af68b6c89342b09e89bbb0dc4dcafec9ced7a3c0137e8771
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
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-nanoserver`

```console
$ docker pull nats@sha256:419eda332cc243b564050f8ff6c94e9df148f930aa3184aaabda593a7313786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:419eda332cc243b564050f8ff6c94e9df148f930aa3184aaabda593a7313786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-scratch`

```console
$ docker pull nats@sha256:81fb519cf3229a15af68b6c89342b09e89bbb0dc4dcafec9ced7a3c0137e8771
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
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-windowsservercore`

```console
$ docker pull nats@sha256:4d37e8d6cdeee8b32d4fd382d2bf2a69505277cdd13e180c04fb0e38390e351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:f41fb080320027c5286199c5569b908be086e4612a46e4c7e82f178aa3103288
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989978837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14ee40d14a8fef68d45a8b5702bb6f311e96e21e417235f7b222d2ae770ca4b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:15:30 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:15:32 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.6/nats-server-v2.12.6-windows-amd64.zip
# Tue, 24 Mar 2026 18:15:35 GMT
ENV NATS_SERVER_SHASUM=35445ebdf3232eeafb866e5c3bca5ac3c189525423367997b81945e9b2ace45b
# Tue, 24 Mar 2026 18:16:44 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:17:10 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:17:10 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:17:11 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:17:12 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:17:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ebb7dfcf4ac9b8f43e43c51a3d50dcca87256a00ae4ea377609728728b0f29`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6634d966c316ea226c2850cb5cd991ccde17cdce2933e1020e8c60efc94dbba2`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dad0e2dd4454c1e1451af56c4aa70cfad3e76e78100716d6af66bfd009863c4`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4f6f4239d361d0624b0a3191f19e5aa55b1cb40ca70aeca4aebf7c4a3ebed3`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f1856c416e46ebb6eca1328e0ad9eb402ab18c2ba270d2250a19ad7f9ad8e0`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 498.9 KB (498917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a9397cefbe2cff3e7f23e244eb5a68d02e076f5667ee1a82a4f34253354fb6`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 7.2 MB (7184887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375bab48f011d171877b0100ab3f1e0d72f66cd2c5470bd70aa1d7f9addce14e`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff354d3bb3841d9b4e1ac9f888a81702c96e420ba432074d8c74327b39d089`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d26923e5a217d54c4d0b5d8442af5cce29a96b1b0e95154a562841f379bd7d`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d67ab5aa667bb65182f7b16d680d2eb370dc87f113ccd5cc5a71a626ee814`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:4d37e8d6cdeee8b32d4fd382d2bf2a69505277cdd13e180c04fb0e38390e351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:f41fb080320027c5286199c5569b908be086e4612a46e4c7e82f178aa3103288
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989978837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14ee40d14a8fef68d45a8b5702bb6f311e96e21e417235f7b222d2ae770ca4b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:15:30 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:15:32 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.6/nats-server-v2.12.6-windows-amd64.zip
# Tue, 24 Mar 2026 18:15:35 GMT
ENV NATS_SERVER_SHASUM=35445ebdf3232eeafb866e5c3bca5ac3c189525423367997b81945e9b2ace45b
# Tue, 24 Mar 2026 18:16:44 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:17:10 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:17:10 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:17:11 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:17:12 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:17:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ebb7dfcf4ac9b8f43e43c51a3d50dcca87256a00ae4ea377609728728b0f29`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6634d966c316ea226c2850cb5cd991ccde17cdce2933e1020e8c60efc94dbba2`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dad0e2dd4454c1e1451af56c4aa70cfad3e76e78100716d6af66bfd009863c4`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4f6f4239d361d0624b0a3191f19e5aa55b1cb40ca70aeca4aebf7c4a3ebed3`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f1856c416e46ebb6eca1328e0ad9eb402ab18c2ba270d2250a19ad7f9ad8e0`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 498.9 KB (498917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a9397cefbe2cff3e7f23e244eb5a68d02e076f5667ee1a82a4f34253354fb6`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 7.2 MB (7184887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375bab48f011d171877b0100ab3f1e0d72f66cd2c5470bd70aa1d7f9addce14e`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff354d3bb3841d9b4e1ac9f888a81702c96e420ba432074d8c74327b39d089`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d26923e5a217d54c4d0b5d8442af5cce29a96b1b0e95154a562841f379bd7d`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d67ab5aa667bb65182f7b16d680d2eb370dc87f113ccd5cc5a71a626ee814`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.6`

```console
$ docker pull nats@sha256:24e20d33a7214208b1cb699c2e4ebfbed32f7a30b41c18b36be75f019a96616c
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
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12.6` - linux; amd64

```console
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.6-alpine`

```console
$ docker pull nats@sha256:1cfc36e2e5e638243d8c722f72c954cd0ec4b15ee82fadbc718ce12e2b3c1652
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

### `nats:2.12.6-alpine` - linux; amd64

```console
$ docker pull nats@sha256:5bb4bf05e7b13ab68145d526ddcf7cd9b122ab4e9be396318b470fbb3db56cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10901603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6289e36de6a653c3a6fdf4c209ab5af57ddc1e4df304025e5b0319578c5de58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724b6d79b0328c1e41c2e402e40355a84657fd655ea7a04d70e56ef30d88e8d`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 7.1 MB (7095760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba8f8d786c0db5eca6a8142087d4b4f7f7ed64e4f273875c72e0ad427ddf121`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc12736b5f7dcd0aa0232b895c2814f574271450bdd11216c09df4166309c8`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:919d5a1842b84c6b23cb36b4520926b9354c437266edf1f27431ad586e66800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f7b6f48ee2d002cdfd9aacb5c4133eb01d8739a2a8d35d325ea2888c14086f`

```dockerfile
```

-	Layers:
	-	`sha256:930d7ae9e007d75b212ac2cc214b7bcd2ab2e84cacca424823b100cdf48e9834`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:14385cdceab398aa6dd31fd51a8d0eb48f42a9d9a9c8baa88a4ba8a2d0e6d23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db147dcb95e7238e38282e2c4ae9aaa5458bc3e9f34d986671345b0add344f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dd16a263fb7b1c26ba67d42231ee535f3d00df3fe3d4f5238711e29683dbb8`  
		Last Modified: Tue, 24 Mar 2026 18:13:42 GMT  
		Size: 6.8 MB (6815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec38e01326bb918550c36013b0b0e623f7982193707ffc9aa2039204670bbf`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8594a1e0b9d5ba01c5f7247e80cd021b8a3f1b8506d38915575ada877f132f22`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ffd7509c5c7f864d7afff95c068a34f1ca118c768bdca9420ee11046979332f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150020eb28e70d47c0ab5cf9a194589fc277d61e2d9fbdd92ea9c8c455ddc134`

```dockerfile
```

-	Layers:
	-	`sha256:ad2785802c0f18173a579ea09f8a176800c7b83e75133ac73b642a19dece30a4`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8d06b4be0657e317e6fb3f38328294c42c2006e1b8f4f36a703a3fb830799bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fbb045461dbfe04fea74b58c92e0717a120b330d96769922081255eb66162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc4bc127449c7715baf7736c50c8753a177bb234c94a8fd7232fd208006f28`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 6.8 MB (6801564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c2fb00e3905b6cef1c48a75670171e564c04556824be30ba32b633016f1507`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f42b05edd76961960f90d1423d0cbd73d62026f6de01455b7a5cf8bcb3c6b7`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4b4c651289e935e8cb85348a1cffb88cce5d1f34582da27a3352e2a91484ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f995cd5707bf9bac5e586042d4329d1fe2559673e4228b8bf4fb5e009e75587`

```dockerfile
```

-	Layers:
	-	`sha256:4f1cae97aebe3d7bacb664be9a66dff39c030b1cf24216b8d339e9e02787fea0`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:38a21bc067dd790300a33c7a77df288526a88d03808b328a9eabe8d13b152a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10641789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564348acc3c55422d9537181b01dfa0d9d6cf275964069c2fd10b25b8dda339`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383bfc032c7f2638ebfce96b0976e02ee30dcd64cdd4b1a0b23012ea2f78718`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 6.5 MB (6501302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd5bf99f5370727619bf2f95ee9315d3b144ddbf1b3ac8e19a907638ef8ebb`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01ba58374b0a722748241e4256b7bd0dbf522f999248b0ae2269a437263eb5`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6dd0076c1cd64737f8de4b7333e624dfe55173329fb2bac1010522d0b435cdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72caa6f6852373a1ace85c8e8fa5d990923b87e473a50fd58427f20eab29eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:8ef47ff5baeebf3463deb04fb68fb758a95f5ff00412a157f52a285f56482fc7`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:b57e19246c78c3589fb6d2a2d7b57d30e9a8f26a5dea9ecf06278eb47f41ce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e681b291aba2493b6548c5c72f81addeb967503bb75bf7cf22d689c7485b4d2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:57 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152168711ce043c658e36a34e2fd496c19c723f91680ec04f28e212e6b20451`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.6 MB (6550474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba6028f2ec6815bede0ce5a102ff4bf694edd8bd6cc576002e29592d253d9a`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00127979287ad785bdbfea091d652471cb758c03d8b0dd75a34262462608bdb5`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:53acfbd102851dc8657ed52c0adeb138ab2f4f98998712113c290468e44b627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c97473b65b616ab5c4187d1c87706c2ac01ee00d37f590e151ab7390b2d537b`

```dockerfile
```

-	Layers:
	-	`sha256:ae32e72632dade7a0e851b51611d6cb44dd2b476e62c370c017b15f9f02df2d1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-alpine` - linux; s390x

```console
$ docker pull nats@sha256:0b96d8319dc5a7fccd30e6b28dfa53bf4a55c113ac3d2f905c900de31bbdc90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8a578d8c5fc8897c630a0895dddec8179595f2038c6902307485a3f14cace0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f13fc4ac0665282379187825661bac82224da72b34bac38edbc43050b2c6e`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 6.9 MB (6934327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a19b2713e4ee80cf7b9d33d33ba4d0a52228b2fa7eb14e1182905f99f1a137`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef841b2f70cfab0cb037b8b542ea4f1700328311b69209d7fa5d50f7bafb99ed`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cd39df443a3b3b87bb26196bddb0601fc93613f151a051eb0bb1743bdd2a97d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3dd97cc216c9d1ad2f0e9b34ce573244908160be058b01282c4190c32c6d7`

```dockerfile
```

-	Layers:
	-	`sha256:5b786517ad8b86d4c95e63a0440e89692600c9115a3c414313d362bb5b4e1b36`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.6-alpine3.22`

```console
$ docker pull nats@sha256:1cfc36e2e5e638243d8c722f72c954cd0ec4b15ee82fadbc718ce12e2b3c1652
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

### `nats:2.12.6-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:5bb4bf05e7b13ab68145d526ddcf7cd9b122ab4e9be396318b470fbb3db56cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10901603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6289e36de6a653c3a6fdf4c209ab5af57ddc1e4df304025e5b0319578c5de58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724b6d79b0328c1e41c2e402e40355a84657fd655ea7a04d70e56ef30d88e8d`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 7.1 MB (7095760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba8f8d786c0db5eca6a8142087d4b4f7f7ed64e4f273875c72e0ad427ddf121`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc12736b5f7dcd0aa0232b895c2814f574271450bdd11216c09df4166309c8`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:919d5a1842b84c6b23cb36b4520926b9354c437266edf1f27431ad586e66800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f7b6f48ee2d002cdfd9aacb5c4133eb01d8739a2a8d35d325ea2888c14086f`

```dockerfile
```

-	Layers:
	-	`sha256:930d7ae9e007d75b212ac2cc214b7bcd2ab2e84cacca424823b100cdf48e9834`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:14385cdceab398aa6dd31fd51a8d0eb48f42a9d9a9c8baa88a4ba8a2d0e6d23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db147dcb95e7238e38282e2c4ae9aaa5458bc3e9f34d986671345b0add344f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dd16a263fb7b1c26ba67d42231ee535f3d00df3fe3d4f5238711e29683dbb8`  
		Last Modified: Tue, 24 Mar 2026 18:13:42 GMT  
		Size: 6.8 MB (6815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec38e01326bb918550c36013b0b0e623f7982193707ffc9aa2039204670bbf`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8594a1e0b9d5ba01c5f7247e80cd021b8a3f1b8506d38915575ada877f132f22`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ffd7509c5c7f864d7afff95c068a34f1ca118c768bdca9420ee11046979332f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150020eb28e70d47c0ab5cf9a194589fc277d61e2d9fbdd92ea9c8c455ddc134`

```dockerfile
```

-	Layers:
	-	`sha256:ad2785802c0f18173a579ea09f8a176800c7b83e75133ac73b642a19dece30a4`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8d06b4be0657e317e6fb3f38328294c42c2006e1b8f4f36a703a3fb830799bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fbb045461dbfe04fea74b58c92e0717a120b330d96769922081255eb66162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc4bc127449c7715baf7736c50c8753a177bb234c94a8fd7232fd208006f28`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 6.8 MB (6801564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c2fb00e3905b6cef1c48a75670171e564c04556824be30ba32b633016f1507`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f42b05edd76961960f90d1423d0cbd73d62026f6de01455b7a5cf8bcb3c6b7`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4b4c651289e935e8cb85348a1cffb88cce5d1f34582da27a3352e2a91484ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f995cd5707bf9bac5e586042d4329d1fe2559673e4228b8bf4fb5e009e75587`

```dockerfile
```

-	Layers:
	-	`sha256:4f1cae97aebe3d7bacb664be9a66dff39c030b1cf24216b8d339e9e02787fea0`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:38a21bc067dd790300a33c7a77df288526a88d03808b328a9eabe8d13b152a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10641789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564348acc3c55422d9537181b01dfa0d9d6cf275964069c2fd10b25b8dda339`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383bfc032c7f2638ebfce96b0976e02ee30dcd64cdd4b1a0b23012ea2f78718`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 6.5 MB (6501302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd5bf99f5370727619bf2f95ee9315d3b144ddbf1b3ac8e19a907638ef8ebb`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01ba58374b0a722748241e4256b7bd0dbf522f999248b0ae2269a437263eb5`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6dd0076c1cd64737f8de4b7333e624dfe55173329fb2bac1010522d0b435cdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72caa6f6852373a1ace85c8e8fa5d990923b87e473a50fd58427f20eab29eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:8ef47ff5baeebf3463deb04fb68fb758a95f5ff00412a157f52a285f56482fc7`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:b57e19246c78c3589fb6d2a2d7b57d30e9a8f26a5dea9ecf06278eb47f41ce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e681b291aba2493b6548c5c72f81addeb967503bb75bf7cf22d689c7485b4d2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:57 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152168711ce043c658e36a34e2fd496c19c723f91680ec04f28e212e6b20451`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.6 MB (6550474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba6028f2ec6815bede0ce5a102ff4bf694edd8bd6cc576002e29592d253d9a`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00127979287ad785bdbfea091d652471cb758c03d8b0dd75a34262462608bdb5`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:53acfbd102851dc8657ed52c0adeb138ab2f4f98998712113c290468e44b627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c97473b65b616ab5c4187d1c87706c2ac01ee00d37f590e151ab7390b2d537b`

```dockerfile
```

-	Layers:
	-	`sha256:ae32e72632dade7a0e851b51611d6cb44dd2b476e62c370c017b15f9f02df2d1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0b96d8319dc5a7fccd30e6b28dfa53bf4a55c113ac3d2f905c900de31bbdc90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8a578d8c5fc8897c630a0895dddec8179595f2038c6902307485a3f14cace0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f13fc4ac0665282379187825661bac82224da72b34bac38edbc43050b2c6e`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 6.9 MB (6934327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a19b2713e4ee80cf7b9d33d33ba4d0a52228b2fa7eb14e1182905f99f1a137`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef841b2f70cfab0cb037b8b542ea4f1700328311b69209d7fa5d50f7bafb99ed`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cd39df443a3b3b87bb26196bddb0601fc93613f151a051eb0bb1743bdd2a97d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3dd97cc216c9d1ad2f0e9b34ce573244908160be058b01282c4190c32c6d7`

```dockerfile
```

-	Layers:
	-	`sha256:5b786517ad8b86d4c95e63a0440e89692600c9115a3c414313d362bb5b4e1b36`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.6-linux`

```console
$ docker pull nats@sha256:81fb519cf3229a15af68b6c89342b09e89bbb0dc4dcafec9ced7a3c0137e8771
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

### `nats:2.12.6-linux` - linux; amd64

```console
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-linux` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-linux` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-linux` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-linux` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.6-nanoserver`

```console
$ docker pull nats@sha256:419eda332cc243b564050f8ff6c94e9df148f930aa3184aaabda593a7313786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12.6-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.6-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:419eda332cc243b564050f8ff6c94e9df148f930aa3184aaabda593a7313786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12.6-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.6-scratch`

```console
$ docker pull nats@sha256:81fb519cf3229a15af68b6c89342b09e89bbb0dc4dcafec9ced7a3c0137e8771
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

### `nats:2.12.6-scratch` - linux; amd64

```console
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.6-scratch` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.6-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.6-windowsservercore`

```console
$ docker pull nats@sha256:4d37e8d6cdeee8b32d4fd382d2bf2a69505277cdd13e180c04fb0e38390e351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12.6-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:f41fb080320027c5286199c5569b908be086e4612a46e4c7e82f178aa3103288
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989978837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14ee40d14a8fef68d45a8b5702bb6f311e96e21e417235f7b222d2ae770ca4b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:15:30 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:15:32 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.6/nats-server-v2.12.6-windows-amd64.zip
# Tue, 24 Mar 2026 18:15:35 GMT
ENV NATS_SERVER_SHASUM=35445ebdf3232eeafb866e5c3bca5ac3c189525423367997b81945e9b2ace45b
# Tue, 24 Mar 2026 18:16:44 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:17:10 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:17:10 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:17:11 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:17:12 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:17:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ebb7dfcf4ac9b8f43e43c51a3d50dcca87256a00ae4ea377609728728b0f29`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6634d966c316ea226c2850cb5cd991ccde17cdce2933e1020e8c60efc94dbba2`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dad0e2dd4454c1e1451af56c4aa70cfad3e76e78100716d6af66bfd009863c4`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4f6f4239d361d0624b0a3191f19e5aa55b1cb40ca70aeca4aebf7c4a3ebed3`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f1856c416e46ebb6eca1328e0ad9eb402ab18c2ba270d2250a19ad7f9ad8e0`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 498.9 KB (498917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a9397cefbe2cff3e7f23e244eb5a68d02e076f5667ee1a82a4f34253354fb6`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 7.2 MB (7184887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375bab48f011d171877b0100ab3f1e0d72f66cd2c5470bd70aa1d7f9addce14e`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff354d3bb3841d9b4e1ac9f888a81702c96e420ba432074d8c74327b39d089`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d26923e5a217d54c4d0b5d8442af5cce29a96b1b0e95154a562841f379bd7d`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d67ab5aa667bb65182f7b16d680d2eb370dc87f113ccd5cc5a71a626ee814`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.6-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:4d37e8d6cdeee8b32d4fd382d2bf2a69505277cdd13e180c04fb0e38390e351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:2.12.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:f41fb080320027c5286199c5569b908be086e4612a46e4c7e82f178aa3103288
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989978837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14ee40d14a8fef68d45a8b5702bb6f311e96e21e417235f7b222d2ae770ca4b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:15:30 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:15:32 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.6/nats-server-v2.12.6-windows-amd64.zip
# Tue, 24 Mar 2026 18:15:35 GMT
ENV NATS_SERVER_SHASUM=35445ebdf3232eeafb866e5c3bca5ac3c189525423367997b81945e9b2ace45b
# Tue, 24 Mar 2026 18:16:44 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:17:10 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:17:10 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:17:11 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:17:12 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:17:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ebb7dfcf4ac9b8f43e43c51a3d50dcca87256a00ae4ea377609728728b0f29`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6634d966c316ea226c2850cb5cd991ccde17cdce2933e1020e8c60efc94dbba2`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dad0e2dd4454c1e1451af56c4aa70cfad3e76e78100716d6af66bfd009863c4`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4f6f4239d361d0624b0a3191f19e5aa55b1cb40ca70aeca4aebf7c4a3ebed3`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f1856c416e46ebb6eca1328e0ad9eb402ab18c2ba270d2250a19ad7f9ad8e0`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 498.9 KB (498917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a9397cefbe2cff3e7f23e244eb5a68d02e076f5667ee1a82a4f34253354fb6`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 7.2 MB (7184887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375bab48f011d171877b0100ab3f1e0d72f66cd2c5470bd70aa1d7f9addce14e`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff354d3bb3841d9b4e1ac9f888a81702c96e420ba432074d8c74327b39d089`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d26923e5a217d54c4d0b5d8442af5cce29a96b1b0e95154a562841f379bd7d`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d67ab5aa667bb65182f7b16d680d2eb370dc87f113ccd5cc5a71a626ee814`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:1cfc36e2e5e638243d8c722f72c954cd0ec4b15ee82fadbc718ce12e2b3c1652
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
$ docker pull nats@sha256:5bb4bf05e7b13ab68145d526ddcf7cd9b122ab4e9be396318b470fbb3db56cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10901603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6289e36de6a653c3a6fdf4c209ab5af57ddc1e4df304025e5b0319578c5de58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724b6d79b0328c1e41c2e402e40355a84657fd655ea7a04d70e56ef30d88e8d`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 7.1 MB (7095760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba8f8d786c0db5eca6a8142087d4b4f7f7ed64e4f273875c72e0ad427ddf121`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc12736b5f7dcd0aa0232b895c2814f574271450bdd11216c09df4166309c8`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:919d5a1842b84c6b23cb36b4520926b9354c437266edf1f27431ad586e66800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f7b6f48ee2d002cdfd9aacb5c4133eb01d8739a2a8d35d325ea2888c14086f`

```dockerfile
```

-	Layers:
	-	`sha256:930d7ae9e007d75b212ac2cc214b7bcd2ab2e84cacca424823b100cdf48e9834`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:14385cdceab398aa6dd31fd51a8d0eb48f42a9d9a9c8baa88a4ba8a2d0e6d23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db147dcb95e7238e38282e2c4ae9aaa5458bc3e9f34d986671345b0add344f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dd16a263fb7b1c26ba67d42231ee535f3d00df3fe3d4f5238711e29683dbb8`  
		Last Modified: Tue, 24 Mar 2026 18:13:42 GMT  
		Size: 6.8 MB (6815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec38e01326bb918550c36013b0b0e623f7982193707ffc9aa2039204670bbf`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8594a1e0b9d5ba01c5f7247e80cd021b8a3f1b8506d38915575ada877f132f22`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ffd7509c5c7f864d7afff95c068a34f1ca118c768bdca9420ee11046979332f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150020eb28e70d47c0ab5cf9a194589fc277d61e2d9fbdd92ea9c8c455ddc134`

```dockerfile
```

-	Layers:
	-	`sha256:ad2785802c0f18173a579ea09f8a176800c7b83e75133ac73b642a19dece30a4`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:8d06b4be0657e317e6fb3f38328294c42c2006e1b8f4f36a703a3fb830799bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fbb045461dbfe04fea74b58c92e0717a120b330d96769922081255eb66162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc4bc127449c7715baf7736c50c8753a177bb234c94a8fd7232fd208006f28`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 6.8 MB (6801564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c2fb00e3905b6cef1c48a75670171e564c04556824be30ba32b633016f1507`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f42b05edd76961960f90d1423d0cbd73d62026f6de01455b7a5cf8bcb3c6b7`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:4b4c651289e935e8cb85348a1cffb88cce5d1f34582da27a3352e2a91484ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f995cd5707bf9bac5e586042d4329d1fe2559673e4228b8bf4fb5e009e75587`

```dockerfile
```

-	Layers:
	-	`sha256:4f1cae97aebe3d7bacb664be9a66dff39c030b1cf24216b8d339e9e02787fea0`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:38a21bc067dd790300a33c7a77df288526a88d03808b328a9eabe8d13b152a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10641789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564348acc3c55422d9537181b01dfa0d9d6cf275964069c2fd10b25b8dda339`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383bfc032c7f2638ebfce96b0976e02ee30dcd64cdd4b1a0b23012ea2f78718`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 6.5 MB (6501302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd5bf99f5370727619bf2f95ee9315d3b144ddbf1b3ac8e19a907638ef8ebb`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01ba58374b0a722748241e4256b7bd0dbf522f999248b0ae2269a437263eb5`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6dd0076c1cd64737f8de4b7333e624dfe55173329fb2bac1010522d0b435cdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72caa6f6852373a1ace85c8e8fa5d990923b87e473a50fd58427f20eab29eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:8ef47ff5baeebf3463deb04fb68fb758a95f5ff00412a157f52a285f56482fc7`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:b57e19246c78c3589fb6d2a2d7b57d30e9a8f26a5dea9ecf06278eb47f41ce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e681b291aba2493b6548c5c72f81addeb967503bb75bf7cf22d689c7485b4d2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:57 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152168711ce043c658e36a34e2fd496c19c723f91680ec04f28e212e6b20451`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.6 MB (6550474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba6028f2ec6815bede0ce5a102ff4bf694edd8bd6cc576002e29592d253d9a`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00127979287ad785bdbfea091d652471cb758c03d8b0dd75a34262462608bdb5`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:53acfbd102851dc8657ed52c0adeb138ab2f4f98998712113c290468e44b627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c97473b65b616ab5c4187d1c87706c2ac01ee00d37f590e151ab7390b2d537b`

```dockerfile
```

-	Layers:
	-	`sha256:ae32e72632dade7a0e851b51611d6cb44dd2b476e62c370c017b15f9f02df2d1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:0b96d8319dc5a7fccd30e6b28dfa53bf4a55c113ac3d2f905c900de31bbdc90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8a578d8c5fc8897c630a0895dddec8179595f2038c6902307485a3f14cace0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f13fc4ac0665282379187825661bac82224da72b34bac38edbc43050b2c6e`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 6.9 MB (6934327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a19b2713e4ee80cf7b9d33d33ba4d0a52228b2fa7eb14e1182905f99f1a137`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef841b2f70cfab0cb037b8b542ea4f1700328311b69209d7fa5d50f7bafb99ed`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cd39df443a3b3b87bb26196bddb0601fc93613f151a051eb0bb1743bdd2a97d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3dd97cc216c9d1ad2f0e9b34ce573244908160be058b01282c4190c32c6d7`

```dockerfile
```

-	Layers:
	-	`sha256:5b786517ad8b86d4c95e63a0440e89692600c9115a3c414313d362bb5b4e1b36`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:1cfc36e2e5e638243d8c722f72c954cd0ec4b15ee82fadbc718ce12e2b3c1652
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
$ docker pull nats@sha256:5bb4bf05e7b13ab68145d526ddcf7cd9b122ab4e9be396318b470fbb3db56cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10901603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6289e36de6a653c3a6fdf4c209ab5af57ddc1e4df304025e5b0319578c5de58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:20:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:20:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:20:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4724b6d79b0328c1e41c2e402e40355a84657fd655ea7a04d70e56ef30d88e8d`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 7.1 MB (7095760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba8f8d786c0db5eca6a8142087d4b4f7f7ed64e4f273875c72e0ad427ddf121`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc12736b5f7dcd0aa0232b895c2814f574271450bdd11216c09df4166309c8`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:919d5a1842b84c6b23cb36b4520926b9354c437266edf1f27431ad586e66800a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f7b6f48ee2d002cdfd9aacb5c4133eb01d8739a2a8d35d325ea2888c14086f`

```dockerfile
```

-	Layers:
	-	`sha256:930d7ae9e007d75b212ac2cc214b7bcd2ab2e84cacca424823b100cdf48e9834`  
		Last Modified: Tue, 24 Mar 2026 18:21:00 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:14385cdceab398aa6dd31fd51a8d0eb48f42a9d9a9c8baa88a4ba8a2d0e6d23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65db147dcb95e7238e38282e2c4ae9aaa5458bc3e9f34d986671345b0add344f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dd16a263fb7b1c26ba67d42231ee535f3d00df3fe3d4f5238711e29683dbb8`  
		Last Modified: Tue, 24 Mar 2026 18:13:42 GMT  
		Size: 6.8 MB (6815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec38e01326bb918550c36013b0b0e623f7982193707ffc9aa2039204670bbf`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8594a1e0b9d5ba01c5f7247e80cd021b8a3f1b8506d38915575ada877f132f22`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ffd7509c5c7f864d7afff95c068a34f1ca118c768bdca9420ee11046979332f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150020eb28e70d47c0ab5cf9a194589fc277d61e2d9fbdd92ea9c8c455ddc134`

```dockerfile
```

-	Layers:
	-	`sha256:ad2785802c0f18173a579ea09f8a176800c7b83e75133ac73b642a19dece30a4`  
		Last Modified: Tue, 24 Mar 2026 18:13:41 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:8d06b4be0657e317e6fb3f38328294c42c2006e1b8f4f36a703a3fb830799bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10026163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fbb045461dbfe04fea74b58c92e0717a120b330d96769922081255eb66162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc4bc127449c7715baf7736c50c8753a177bb234c94a8fd7232fd208006f28`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 6.8 MB (6801564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c2fb00e3905b6cef1c48a75670171e564c04556824be30ba32b633016f1507`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f42b05edd76961960f90d1423d0cbd73d62026f6de01455b7a5cf8bcb3c6b7`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:4b4c651289e935e8cb85348a1cffb88cce5d1f34582da27a3352e2a91484ce24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f995cd5707bf9bac5e586042d4329d1fe2559673e4228b8bf4fb5e009e75587`

```dockerfile
```

-	Layers:
	-	`sha256:4f1cae97aebe3d7bacb664be9a66dff39c030b1cf24216b8d339e9e02787fea0`  
		Last Modified: Tue, 24 Mar 2026 18:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:38a21bc067dd790300a33c7a77df288526a88d03808b328a9eabe8d13b152a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10641789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4564348acc3c55422d9537181b01dfa0d9d6cf275964069c2fd10b25b8dda339`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:21:01 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:21:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:21:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:21:01 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8383bfc032c7f2638ebfce96b0976e02ee30dcd64cdd4b1a0b23012ea2f78718`  
		Last Modified: Tue, 24 Mar 2026 18:21:06 GMT  
		Size: 6.5 MB (6501302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fd5bf99f5370727619bf2f95ee9315d3b144ddbf1b3ac8e19a907638ef8ebb`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f01ba58374b0a722748241e4256b7bd0dbf522f999248b0ae2269a437263eb5`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6dd0076c1cd64737f8de4b7333e624dfe55173329fb2bac1010522d0b435cdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72caa6f6852373a1ace85c8e8fa5d990923b87e473a50fd58427f20eab29eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:8ef47ff5baeebf3463deb04fb68fb758a95f5ff00412a157f52a285f56482fc7`  
		Last Modified: Tue, 24 Mar 2026 18:21:05 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:b57e19246c78c3589fb6d2a2d7b57d30e9a8f26a5dea9ecf06278eb47f41ce4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e681b291aba2493b6548c5c72f81addeb967503bb75bf7cf22d689c7485b4d2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:57 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:57 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:57 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152168711ce043c658e36a34e2fd496c19c723f91680ec04f28e212e6b20451`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 6.6 MB (6550474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba6028f2ec6815bede0ce5a102ff4bf694edd8bd6cc576002e29592d253d9a`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00127979287ad785bdbfea091d652471cb758c03d8b0dd75a34262462608bdb5`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:53acfbd102851dc8657ed52c0adeb138ab2f4f98998712113c290468e44b627f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c97473b65b616ab5c4187d1c87706c2ac01ee00d37f590e151ab7390b2d537b`

```dockerfile
```

-	Layers:
	-	`sha256:ae32e72632dade7a0e851b51611d6cb44dd2b476e62c370c017b15f9f02df2d1`  
		Last Modified: Tue, 24 Mar 2026 18:14:06 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0b96d8319dc5a7fccd30e6b28dfa53bf4a55c113ac3d2f905c900de31bbdc90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10585730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8a578d8c5fc8897c630a0895dddec8179595f2038c6902307485a3f14cace0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:13:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='fddaf3f223c7af3f4d0a0d2c2fc084406e6b3ec7adfd1b9e6a37fbd03bfe222f' ;;     armhf) natsArch='arm6'; sha256='db693c694a647198ee23e43c0c34055a02d53f2b133184025d650c03d72a92b6' ;;     armv7) natsArch='arm7'; sha256='cd9998b41d16e6339bb11ef7f8402911e6132e01b8506d21ce7e5494188b6891' ;;     x86_64) natsArch='amd64'; sha256='77fe7dd69ff5144126026b78355900be0ab0bb4339dc61a7621dcc9b9e9d07a6' ;;     x86) natsArch='386'; sha256='b9f6119c607b0095d3b1a342b88cad7064d2fd9bd1e0708adba9b99a5c246d67' ;;     s390x) natsArch='s390x'; sha256='90eb878938011d2f15ef365ed278e35191693ccb92255dcf9730348da786bdc8' ;;     ppc64le) natsArch='ppc64le'; sha256='b7c68219ad7005a0faca4cce3658dc72b389aacacd346a58aa33bbe7953beb44' ;;     loong64) natsArch='loong64'; sha256='506bf995f1d4b3a9a444734b93eb5de15bd1e5cba5fa91bb2071314cafbee019' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 24 Mar 2026 18:13:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:13:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 18:13:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49f13fc4ac0665282379187825661bac82224da72b34bac38edbc43050b2c6e`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 6.9 MB (6934327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a19b2713e4ee80cf7b9d33d33ba4d0a52228b2fa7eb14e1182905f99f1a137`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef841b2f70cfab0cb037b8b542ea4f1700328311b69209d7fa5d50f7bafb99ed`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cd39df443a3b3b87bb26196bddb0601fc93613f151a051eb0bb1743bdd2a97d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3dd97cc216c9d1ad2f0e9b34ce573244908160be058b01282c4190c32c6d7`

```dockerfile
```

-	Layers:
	-	`sha256:5b786517ad8b86d4c95e63a0440e89692600c9115a3c414313d362bb5b4e1b36`  
		Last Modified: Tue, 24 Mar 2026 18:13:13 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:24e20d33a7214208b1cb699c2e4ebfbed32f7a30b41c18b36be75f019a96616c
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
	-	windows version 10.0.20348.4893; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:81fb519cf3229a15af68b6c89342b09e89bbb0dc4dcafec9ced7a3c0137e8771
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
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:419eda332cc243b564050f8ff6c94e9df148f930aa3184aaabda593a7313786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:419eda332cc243b564050f8ff6c94e9df148f930aa3184aaabda593a7313786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:270c8d8463baa51263649bb7edccca8023ff18cb3d3e2b7c50c18f66842fcf63
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133481939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e273b1f3c093291412f2567a093288ae663ff189298335e43c0b4843054227a5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 24 Mar 2026 18:39:02 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:e4db7c8068a18ff6128cb4e29dc113730e5e5bba4a56f7dd5ff0f84a46b740da in C:\nats-server.exe 
# Tue, 24 Mar 2026 18:39:03 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:39:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:39:05 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:39:06 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351c93818316b8da5c0ea0e81ae0f1287bb470901778b5ed4f873c38627b928`  
		Last Modified: Tue, 24 Mar 2026 18:39:12 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b23a6e5cc7736a9f8f4af4b4592aeec779d74315a2ae986e1c61954c30566c`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 6.8 MB (6825438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ccd3dac508a5cfb9034d3c13be911cf02ab3328a3c89f770fca378c699b45e`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2f227f27ba8db3b1d452511a545f8dceca13ccda3041ed3815eaa39206d89`  
		Last Modified: Tue, 24 Mar 2026 18:39:11 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54af9b204ea2f0fccd137eda046a7b9d75b76bdcbec8dac0d6b70c9330ddd1e`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae8cb95ef4ed26bb079ed5404f2127da438bff5d4b0e02a68597191ce0068b1`  
		Last Modified: Tue, 24 Mar 2026 18:39:10 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:81fb519cf3229a15af68b6c89342b09e89bbb0dc4dcafec9ced7a3c0137e8771
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
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:4d37e8d6cdeee8b32d4fd382d2bf2a69505277cdd13e180c04fb0e38390e351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:f41fb080320027c5286199c5569b908be086e4612a46e4c7e82f178aa3103288
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989978837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14ee40d14a8fef68d45a8b5702bb6f311e96e21e417235f7b222d2ae770ca4b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:15:30 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:15:32 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.6/nats-server-v2.12.6-windows-amd64.zip
# Tue, 24 Mar 2026 18:15:35 GMT
ENV NATS_SERVER_SHASUM=35445ebdf3232eeafb866e5c3bca5ac3c189525423367997b81945e9b2ace45b
# Tue, 24 Mar 2026 18:16:44 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:17:10 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:17:10 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:17:11 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:17:12 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:17:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ebb7dfcf4ac9b8f43e43c51a3d50dcca87256a00ae4ea377609728728b0f29`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6634d966c316ea226c2850cb5cd991ccde17cdce2933e1020e8c60efc94dbba2`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dad0e2dd4454c1e1451af56c4aa70cfad3e76e78100716d6af66bfd009863c4`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4f6f4239d361d0624b0a3191f19e5aa55b1cb40ca70aeca4aebf7c4a3ebed3`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f1856c416e46ebb6eca1328e0ad9eb402ab18c2ba270d2250a19ad7f9ad8e0`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 498.9 KB (498917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a9397cefbe2cff3e7f23e244eb5a68d02e076f5667ee1a82a4f34253354fb6`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 7.2 MB (7184887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375bab48f011d171877b0100ab3f1e0d72f66cd2c5470bd70aa1d7f9addce14e`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff354d3bb3841d9b4e1ac9f888a81702c96e420ba432074d8c74327b39d089`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d26923e5a217d54c4d0b5d8442af5cce29a96b1b0e95154a562841f379bd7d`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d67ab5aa667bb65182f7b16d680d2eb370dc87f113ccd5cc5a71a626ee814`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:4d37e8d6cdeee8b32d4fd382d2bf2a69505277cdd13e180c04fb0e38390e351a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull nats@sha256:f41fb080320027c5286199c5569b908be086e4612a46e4c7e82f178aa3103288
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1989978837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14ee40d14a8fef68d45a8b5702bb6f311e96e21e417235f7b222d2ae770ca4b`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 24 Mar 2026 18:15:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 24 Mar 2026 18:15:28 GMT
ENV NATS_DOCKERIZED=1
# Tue, 24 Mar 2026 18:15:30 GMT
ENV NATS_SERVER=2.12.6
# Tue, 24 Mar 2026 18:15:32 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.6
# Tue, 24 Mar 2026 18:15:33 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.6/nats-server-v2.12.6-windows-amd64.zip
# Tue, 24 Mar 2026 18:15:35 GMT
ENV NATS_SERVER_SHASUM=35445ebdf3232eeafb866e5c3bca5ac3c189525423367997b81945e9b2ace45b
# Tue, 24 Mar 2026 18:16:44 GMT
RUN Set-PSDebug -Trace 2
# Tue, 24 Mar 2026 18:17:10 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 24 Mar 2026 18:17:10 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 24 Mar 2026 18:17:11 GMT
EXPOSE 4222 6222 8222
# Tue, 24 Mar 2026 18:17:12 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 24 Mar 2026 18:17:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d8a28f8ce4f70e086f76e30fd695c1b894f3028f9b957e1ff7fe4d9f163c5c`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7de85c1597c8f74f6e51a2f585487e912a441506aa312739baa8a5908353a`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ebb7dfcf4ac9b8f43e43c51a3d50dcca87256a00ae4ea377609728728b0f29`  
		Last Modified: Tue, 24 Mar 2026 18:17:22 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6634d966c316ea226c2850cb5cd991ccde17cdce2933e1020e8c60efc94dbba2`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dad0e2dd4454c1e1451af56c4aa70cfad3e76e78100716d6af66bfd009863c4`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4f6f4239d361d0624b0a3191f19e5aa55b1cb40ca70aeca4aebf7c4a3ebed3`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f1856c416e46ebb6eca1328e0ad9eb402ab18c2ba270d2250a19ad7f9ad8e0`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 498.9 KB (498917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a9397cefbe2cff3e7f23e244eb5a68d02e076f5667ee1a82a4f34253354fb6`  
		Last Modified: Tue, 24 Mar 2026 18:17:20 GMT  
		Size: 7.2 MB (7184887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375bab48f011d171877b0100ab3f1e0d72f66cd2c5470bd70aa1d7f9addce14e`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff354d3bb3841d9b4e1ac9f888a81702c96e420ba432074d8c74327b39d089`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d26923e5a217d54c4d0b5d8442af5cce29a96b1b0e95154a562841f379bd7d`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d67ab5aa667bb65182f7b16d680d2eb370dc87f113ccd5cc5a71a626ee814`  
		Last Modified: Tue, 24 Mar 2026 18:17:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
