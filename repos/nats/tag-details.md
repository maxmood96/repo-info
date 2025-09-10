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
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.22`](#nats210-alpine322)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-ltsc2022`](#nats210-nanoserver-ltsc2022)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-ltsc2022`](#nats210-windowsservercore-ltsc2022)
-	[`nats:2.10.29`](#nats21029)
-	[`nats:2.10.29-alpine`](#nats21029-alpine)
-	[`nats:2.10.29-alpine3.22`](#nats21029-alpine322)
-	[`nats:2.10.29-linux`](#nats21029-linux)
-	[`nats:2.10.29-nanoserver`](#nats21029-nanoserver)
-	[`nats:2.10.29-nanoserver-ltsc2022`](#nats21029-nanoserver-ltsc2022)
-	[`nats:2.10.29-scratch`](#nats21029-scratch)
-	[`nats:2.10.29-windowsservercore`](#nats21029-windowsservercore)
-	[`nats:2.10.29-windowsservercore-ltsc2022`](#nats21029-windowsservercore-ltsc2022)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.22`](#nats211-alpine322)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-ltsc2022`](#nats211-nanoserver-ltsc2022)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-ltsc2022`](#nats211-windowsservercore-ltsc2022)
-	[`nats:2.11.9`](#nats2119)
-	[`nats:2.11.9-alpine`](#nats2119-alpine)
-	[`nats:2.11.9-alpine3.22`](#nats2119-alpine322)
-	[`nats:2.11.9-linux`](#nats2119-linux)
-	[`nats:2.11.9-nanoserver`](#nats2119-nanoserver)
-	[`nats:2.11.9-nanoserver-ltsc2022`](#nats2119-nanoserver-ltsc2022)
-	[`nats:2.11.9-scratch`](#nats2119-scratch)
-	[`nats:2.11.9-windowsservercore`](#nats2119-windowsservercore)
-	[`nats:2.11.9-windowsservercore-ltsc2022`](#nats2119-windowsservercore-ltsc2022)
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
$ docker pull nats@sha256:a8fe3a4066d3c14d893dd92a6d85f117cfb3567d4d0df11bc3161782b34dc351
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
	-	windows version 10.0.20348.4052; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:777787bbb4c7c4083ec2213b0b8b14151617610a3e0d85776bd995cd46599c73
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
$ docker pull nats@sha256:383e95bac92d099fa612f6bbe5c4c83ae15af22e409a89fecd2e3c5092a8b2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e317eb6ac10bc33a158896aec219c58122b17191d82ad8059edfdd348687beca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab2a6f9512b153493f557d6c5cfaaa4a7c3cb1211f22480cb0d5c50d3a4b17`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 6.8 MB (6811571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee5018631bdb543650e4026cef806de7225147757a9e052ab075bc9ce41192`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4d4963114e48d99ec239e86fdee1a87c26a0e2d581a26bc7a82c659486b221`  
		Last Modified: Tue, 09 Sep 2025 21:28:03 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ba0a85e05e92baa4dc25c2d468c7055ed378ed85e8cef076e528de3db68d5d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d338ea42bfc75ac6382f89e464fb4f8968277e57e510d15d0516ec454dc2a8ee`

```dockerfile
```

-	Layers:
	-	`sha256:afdda197879734c0f39320dd4b5d9022177afc5ed488a2ec3bc5100477686c47`  
		Last Modified: Tue, 09 Sep 2025 23:56:39 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e40ee2e909ecb5d5497f954e4bae9fe52ff74799dc1916a38a9501d3a601236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10023996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a9c25c10fb7e66ad634861abcd1f91711d6ad5aeb2f3c7107b22f6ada83fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2acf2abeee38084f132adc7fc2df4157782dac0272a686992cf569149b35f9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 6.5 MB (6522116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590716c3787e83b577093cbf8f4c94109c354ce9d4a8f4e1a77c40df98d08323`  
		Last Modified: Tue, 09 Sep 2025 21:43:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a98b784cf4f30652bb9977f4b8182b43e8facd172a4941225c99ab5995dba9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8328b4789d4fbe7d5b301f3bd5035ae9db9ad28510f44990ee8566e1e7e1dbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddc73c38f5ff5cf3bb96c33e0ce7c05fbc401d129d48c24368267d9cc5605bc`

```dockerfile
```

-	Layers:
	-	`sha256:2db5fa19161bff44ba2f7e98f558c2306b54b8593a3acd92b4c51812baaadf96`  
		Last Modified: Tue, 09 Sep 2025 23:56:42 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:da2887adbe5a9b5ce19ba1daf5f5323382993e2999e1a5450dea6d5d615af554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9732548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa53562ec436568c3bf00db1fb91bc89ebfddf47fe2f946af086551b7d0240d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031341d8662c24b611d19217b15697c7e1eeb7fb20ae015769304f3d9e416f4`  
		Last Modified: Tue, 09 Sep 2025 21:59:39 GMT  
		Size: 6.5 MB (6512539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4721d57828fe2cba2dda46e5e717ad9ee4278ab187e170e498625e6116e7d5f`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc30ccba0a3c016998f1b5b2e2cdccd8d8f698e228a65dd364b2adb41b185f3`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:af1dd4d927ea33740d8992643ce68d26a2d5ff2e68fa53849efbaec72158a770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e92010b8b482e98d125d98981583e131f2df9dbd380f6b38cbcd1b45eb9b95`

```dockerfile
```

-	Layers:
	-	`sha256:785b567e7e5ebabe0f6b6d6e32479ec15565ad1886ce491f7b90e7af1eae9c54`  
		Last Modified: Tue, 09 Sep 2025 23:56:45 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b78f1e58f75bba9a7393b5f2bfe919ed0516e154ceb1260cdc013093e0d08daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e807b412fc1138feba48d67aa5c005eea691e786927abca0174930a194059dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81efb27a24236aa9d4dd850761611e76ba6addbab29a3200f3394ddb61e8b457`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.3 MB (6299385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82430e347407921b5c2f85841823aac9ee8ad9e3e96a91c355b0195f303337e`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a300c8b17b92657dc962e711a386e4a85537831d47c4dd21abdf78281c75ffe2`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:17e3e88060ad541c6b4c32996093543b4dff70e3ed4858411180475c8fdb726a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52155310f554543e3eba1ff4e53c6d064d0c1554b36243f55cc7b47991d1bffb`

```dockerfile
```

-	Layers:
	-	`sha256:71290e70b093feda2cec83ba57599465c9c85d6a25207135ffe14156b636e16a`  
		Last Modified: Tue, 09 Sep 2025 23:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:54e05d0d4583d88acae58396444e5a856104ea167b8be5441bc559181cc5a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10005035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f0fa028221d6d5d34463a7ae1561e9c4b6429343c173387bb4b6ca560be435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdf74981cd55b1384057c7128506e55ba5cb405d3805d01d372d78639b6f68f`  
		Last Modified: Tue, 09 Sep 2025 22:41:34 GMT  
		Size: 6.3 MB (6276953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20c0fbc0352f22902cf45129dfed4ad8d39bdfb4ddc662750875e826f0fa048`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9a8a923704ae9582e7e000943845e579ce24fe430b260de5e0b6511b8ada0`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:edc001c19fc6f746a25c2ad86c35a9ae36ea65996d0bb0c4fb079541607a2b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea334b98e4c0c7cdf7544a7944458efbd59d206ffb201dbc9bfde0fcd1eb081`

```dockerfile
```

-	Layers:
	-	`sha256:fb1473e3d857e75ce42f899fae73871d5325888dd66b94dccebb3a786e13a6f1`  
		Last Modified: Tue, 09 Sep 2025 23:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:c092626e962687b5c5819475844a8aabd59265be101a1c6876a1ac9c4293e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8d1105a8bbefc2fc8ded940d6b0bfb291fedfa8496dbe6671ea9f1675a0b3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee21526533161753c86a71f59d0df970aa35c45d24fdef163007b752fe70e3`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 6.6 MB (6646165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b3c4b7b79090468183fcf1696975567f84eb65fb97befa05d25ce48efccee`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e44737618f643a95798867bcd27e21c0ea885cede55a7fb81f96a9c7c7e19c`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c0ce755324c31309757a9e71aec2d4164dd8e5eb70127b5ff8d402fe15807f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ffb49aae826cb2119b2c3420d4f3b9c2cd24d4f20626d536cf9b4606d1dc9`

```dockerfile
```

-	Layers:
	-	`sha256:5badeeb273e199fa585a1f83872b8d1f5ba9c8987464a21caec5530d62973b86`  
		Last Modified: Tue, 09 Sep 2025 23:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:777787bbb4c7c4083ec2213b0b8b14151617610a3e0d85776bd995cd46599c73
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
$ docker pull nats@sha256:383e95bac92d099fa612f6bbe5c4c83ae15af22e409a89fecd2e3c5092a8b2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e317eb6ac10bc33a158896aec219c58122b17191d82ad8059edfdd348687beca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab2a6f9512b153493f557d6c5cfaaa4a7c3cb1211f22480cb0d5c50d3a4b17`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 6.8 MB (6811571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee5018631bdb543650e4026cef806de7225147757a9e052ab075bc9ce41192`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4d4963114e48d99ec239e86fdee1a87c26a0e2d581a26bc7a82c659486b221`  
		Last Modified: Tue, 09 Sep 2025 21:28:03 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ba0a85e05e92baa4dc25c2d468c7055ed378ed85e8cef076e528de3db68d5d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d338ea42bfc75ac6382f89e464fb4f8968277e57e510d15d0516ec454dc2a8ee`

```dockerfile
```

-	Layers:
	-	`sha256:afdda197879734c0f39320dd4b5d9022177afc5ed488a2ec3bc5100477686c47`  
		Last Modified: Tue, 09 Sep 2025 23:56:39 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e40ee2e909ecb5d5497f954e4bae9fe52ff74799dc1916a38a9501d3a601236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10023996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a9c25c10fb7e66ad634861abcd1f91711d6ad5aeb2f3c7107b22f6ada83fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2acf2abeee38084f132adc7fc2df4157782dac0272a686992cf569149b35f9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 6.5 MB (6522116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590716c3787e83b577093cbf8f4c94109c354ce9d4a8f4e1a77c40df98d08323`  
		Last Modified: Tue, 09 Sep 2025 21:43:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a98b784cf4f30652bb9977f4b8182b43e8facd172a4941225c99ab5995dba9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8328b4789d4fbe7d5b301f3bd5035ae9db9ad28510f44990ee8566e1e7e1dbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddc73c38f5ff5cf3bb96c33e0ce7c05fbc401d129d48c24368267d9cc5605bc`

```dockerfile
```

-	Layers:
	-	`sha256:2db5fa19161bff44ba2f7e98f558c2306b54b8593a3acd92b4c51812baaadf96`  
		Last Modified: Tue, 09 Sep 2025 23:56:42 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:da2887adbe5a9b5ce19ba1daf5f5323382993e2999e1a5450dea6d5d615af554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9732548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa53562ec436568c3bf00db1fb91bc89ebfddf47fe2f946af086551b7d0240d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031341d8662c24b611d19217b15697c7e1eeb7fb20ae015769304f3d9e416f4`  
		Last Modified: Tue, 09 Sep 2025 21:59:39 GMT  
		Size: 6.5 MB (6512539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4721d57828fe2cba2dda46e5e717ad9ee4278ab187e170e498625e6116e7d5f`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc30ccba0a3c016998f1b5b2e2cdccd8d8f698e228a65dd364b2adb41b185f3`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:af1dd4d927ea33740d8992643ce68d26a2d5ff2e68fa53849efbaec72158a770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e92010b8b482e98d125d98981583e131f2df9dbd380f6b38cbcd1b45eb9b95`

```dockerfile
```

-	Layers:
	-	`sha256:785b567e7e5ebabe0f6b6d6e32479ec15565ad1886ce491f7b90e7af1eae9c54`  
		Last Modified: Tue, 09 Sep 2025 23:56:45 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b78f1e58f75bba9a7393b5f2bfe919ed0516e154ceb1260cdc013093e0d08daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e807b412fc1138feba48d67aa5c005eea691e786927abca0174930a194059dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81efb27a24236aa9d4dd850761611e76ba6addbab29a3200f3394ddb61e8b457`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.3 MB (6299385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82430e347407921b5c2f85841823aac9ee8ad9e3e96a91c355b0195f303337e`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a300c8b17b92657dc962e711a386e4a85537831d47c4dd21abdf78281c75ffe2`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:17e3e88060ad541c6b4c32996093543b4dff70e3ed4858411180475c8fdb726a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52155310f554543e3eba1ff4e53c6d064d0c1554b36243f55cc7b47991d1bffb`

```dockerfile
```

-	Layers:
	-	`sha256:71290e70b093feda2cec83ba57599465c9c85d6a25207135ffe14156b636e16a`  
		Last Modified: Tue, 09 Sep 2025 23:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:54e05d0d4583d88acae58396444e5a856104ea167b8be5441bc559181cc5a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10005035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f0fa028221d6d5d34463a7ae1561e9c4b6429343c173387bb4b6ca560be435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdf74981cd55b1384057c7128506e55ba5cb405d3805d01d372d78639b6f68f`  
		Last Modified: Tue, 09 Sep 2025 22:41:34 GMT  
		Size: 6.3 MB (6276953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20c0fbc0352f22902cf45129dfed4ad8d39bdfb4ddc662750875e826f0fa048`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9a8a923704ae9582e7e000943845e579ce24fe430b260de5e0b6511b8ada0`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:edc001c19fc6f746a25c2ad86c35a9ae36ea65996d0bb0c4fb079541607a2b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea334b98e4c0c7cdf7544a7944458efbd59d206ffb201dbc9bfde0fcd1eb081`

```dockerfile
```

-	Layers:
	-	`sha256:fb1473e3d857e75ce42f899fae73871d5325888dd66b94dccebb3a786e13a6f1`  
		Last Modified: Tue, 09 Sep 2025 23:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:c092626e962687b5c5819475844a8aabd59265be101a1c6876a1ac9c4293e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8d1105a8bbefc2fc8ded940d6b0bfb291fedfa8496dbe6671ea9f1675a0b3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee21526533161753c86a71f59d0df970aa35c45d24fdef163007b752fe70e3`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 6.6 MB (6646165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b3c4b7b79090468183fcf1696975567f84eb65fb97befa05d25ce48efccee`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e44737618f643a95798867bcd27e21c0ea885cede55a7fb81f96a9c7c7e19c`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c0ce755324c31309757a9e71aec2d4164dd8e5eb70127b5ff8d402fe15807f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ffb49aae826cb2119b2c3420d4f3b9c2cd24d4f20626d536cf9b4606d1dc9`

```dockerfile
```

-	Layers:
	-	`sha256:5badeeb273e199fa585a1f83872b8d1f5ba9c8987464a21caec5530d62973b86`  
		Last Modified: Tue, 09 Sep 2025 23:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:ee3312f4e9d4b67ff197b0ed1e98756596f0d7db872e7fe30d9bf64fccddf92c
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
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:950519f31ba604e5d89f5b7abb1aa2dfa10b04b00e7559e52cdaa0c5f077b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:950519f31ba604e5d89f5b7abb1aa2dfa10b04b00e7559e52cdaa0c5f077b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:ee3312f4e9d4b67ff197b0ed1e98756596f0d7db872e7fe30d9bf64fccddf92c
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
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:bb0d35aa5eed764e627f92b57cb5eceaaf6707b0ae52ddf0c31716c54870bb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:6adfca3411b50bb2d743507583ac87476d7965b2cbed6518a20d4931d3491f45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288928787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98c80bef79058b0466c1d9f41b8d4ca392f9ba73250a750c7ea21bab930aa97`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 21:27:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Sep 2025 21:27:29 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 21:27:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 21:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.9/nats-server-v2.11.9-windows-amd64.zip
# Tue, 09 Sep 2025 21:27:33 GMT
ENV NATS_SERVER_SHASUM=841a953d9be1d55b5f2b990c624b239f7f938baaf00d5627ac34d6c363a2fda3
# Tue, 09 Sep 2025 21:27:53 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Sep 2025 21:28:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Sep 2025 21:28:15 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 21:28:16 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 21:28:18 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 21:28:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873d00bcaff9497f2d332fa6897defb80cc97bf202af48ef6c713377e8d9df48`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b198342f09ddc645f6fc2b65a830146f5d0d7b0fe1eb41f306dde5eef7f46b`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990e7ded3458108fd3c5e4e46d956fb4821b25c1be30560397a4c05e6bbffc3c`  
		Last Modified: Tue, 09 Sep 2025 21:28:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8258a2f8d54eef32d8c8da5489e1222917b41d56e62e97b7889cad5929dac7`  
		Last Modified: Tue, 09 Sep 2025 21:28:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2939a4cd8a8edb8a73065013d6ff136be09a5c80fb388692a0eb284bb9516d91`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c8f62dd915a272e9ebf61afe2ec754bfb7592db3760a577412e1456b4a1a3d`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 343.2 KB (343172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8604f83c30deda1e29d968f6384c4e584eeb306c7df98b9a754743e760128785`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.9 MB (6881510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a7e192f98db48a22a47dd45e84dace5542d6245b2f0acfb82d28be2485dd13`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f754f15699c71eb0c940dac7c0ff3f6e668ea993a2b45320344a34f5b9006f77`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc414a41a0ef3729968b13a6c80750a0f8afb723bebab36a4fd4e0d76ae4cc4`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3955ff1a4e10e862f6c1364516e5e72757e2ec571b70019de550d19b435131c`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:bb0d35aa5eed764e627f92b57cb5eceaaf6707b0ae52ddf0c31716c54870bb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:6adfca3411b50bb2d743507583ac87476d7965b2cbed6518a20d4931d3491f45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288928787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98c80bef79058b0466c1d9f41b8d4ca392f9ba73250a750c7ea21bab930aa97`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 21:27:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Sep 2025 21:27:29 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 21:27:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 21:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.9/nats-server-v2.11.9-windows-amd64.zip
# Tue, 09 Sep 2025 21:27:33 GMT
ENV NATS_SERVER_SHASUM=841a953d9be1d55b5f2b990c624b239f7f938baaf00d5627ac34d6c363a2fda3
# Tue, 09 Sep 2025 21:27:53 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Sep 2025 21:28:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Sep 2025 21:28:15 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 21:28:16 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 21:28:18 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 21:28:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873d00bcaff9497f2d332fa6897defb80cc97bf202af48ef6c713377e8d9df48`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b198342f09ddc645f6fc2b65a830146f5d0d7b0fe1eb41f306dde5eef7f46b`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990e7ded3458108fd3c5e4e46d956fb4821b25c1be30560397a4c05e6bbffc3c`  
		Last Modified: Tue, 09 Sep 2025 21:28:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8258a2f8d54eef32d8c8da5489e1222917b41d56e62e97b7889cad5929dac7`  
		Last Modified: Tue, 09 Sep 2025 21:28:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2939a4cd8a8edb8a73065013d6ff136be09a5c80fb388692a0eb284bb9516d91`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c8f62dd915a272e9ebf61afe2ec754bfb7592db3760a577412e1456b4a1a3d`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 343.2 KB (343172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8604f83c30deda1e29d968f6384c4e584eeb306c7df98b9a754743e760128785`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.9 MB (6881510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a7e192f98db48a22a47dd45e84dace5542d6245b2f0acfb82d28be2485dd13`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f754f15699c71eb0c940dac7c0ff3f6e668ea993a2b45320344a34f5b9006f77`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc414a41a0ef3729968b13a6c80750a0f8afb723bebab36a4fd4e0d76ae4cc4`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3955ff1a4e10e862f6c1364516e5e72757e2ec571b70019de550d19b435131c`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:d7f4c3c9a9f33f55714d186653dabf6a267bdb7c01b6026ca52dcc6107cdd195
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
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:eca033f54dbb5d0a5df80c60ff229e53c71de63a8b4ddd0c2f04dd3e55d287df
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

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:820a97ef8a0e8e4b1f1c940c1fbf92e57ad548429dd20754de24ffe4f08996a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad9be7ec221398a67b66fa5f6dc4afe4e24f62ff6a2860f3a914caf5172c90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c015b317061ba6cf363edd67bb9353c30207a61e58e505226168bc0da98afe`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 6.6 MB (6627507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97296c7fe6d9f4da2c4c2dde8e7b27ce58644942a70f97ce0622c116554dc7`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7355fe018b748ae16c9a4bbdaa99767706e56854d8d0535fd5aa2f96fbde81`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2b30e09f1d5f9b8e841201cf1ac53ade8e643572c891218121424a8b792908b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ad2f85e296997148a5e7d39b4527ad05c5559df3691d711ac6d93cc2b2799a`

```dockerfile
```

-	Layers:
	-	`sha256:89817af9341cc2fe811ba2110f7ecca87b5b39105610d0abae9f3e3da0a9777a`  
		Last Modified: Tue, 15 Jul 2025 20:57:03 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bbbd389071ab1d8d254eb3df7fa93150882b5229c3a99da9d4cdd9d9d9fb4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9852288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa1eb6ecb82b890304acc50b41737e48830c07d6adb9d5457e9eccebadb3768`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acf1350211366512043db3b27f0e92a67c14e308e2f135f34345d30309834ba`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 6.4 MB (6350410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9e0e3d02f0321c18cfb1f4ca8cf20685fcdb82a54101021179760ffa1115b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1209aaaa768e3b746d249f5d8401d372e7d5523f3a4397dde59eb595e0962b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:18c88d88649738fbf3c7c2459ea047163f1256228fa7897077a0bf288dc884b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d11b71658547861a6f90067c7fb4d97c2d27cf0a804fba09a4535f16249da`

```dockerfile
```

-	Layers:
	-	`sha256:cd47a78549dc53d5c15b84eef49a9ad57778519a088bfbdafa38ec0be31ce357`  
		Last Modified: Tue, 15 Jul 2025 20:57:06 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bae5228a4b8fa7abf5b2d2daeda9617519e08cc86149630e7adde2141efeb3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9559514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4262f443d7ff0a48649c5f56e9ea6b6fa4f198ea37b29733999f51ae562c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0607845d0fa55bdc3e76e0de89b169dd06188e51f5b2fb955e7ed32ae35f2380`  
		Last Modified: Tue, 15 Jul 2025 19:34:22 GMT  
		Size: 6.3 MB (6339508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0483d372ec00a330e5264b9f6e35c5d71ac4528d86a6a9584483bc0212031`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5469ded3bdfb31968ff768c86467701029b614a24b30acd8b12cf171bd1e3ef`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9c07cf58635126d1738dbc4853752497aeb197c3bf272aa23efc136bf8f18a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e7a9555de683929fd2a60677efa3416e877cd39c83ddf52e88187ae583703e`

```dockerfile
```

-	Layers:
	-	`sha256:8108e75ff73bb20deeee1f58da34c3cadf06f927494ad913c09b75c63eba39d8`  
		Last Modified: Tue, 15 Jul 2025 20:57:09 GMT  
		Size: 13.2 KB (13197 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:517e9d2a336ceb5f7d2bb56e2e760a0e519bc17980d917a1249963124a3009c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d275fb226d388d4dd3a791d2935b9e666b0bdcbb308c9ed5c3c275b9a6bf1b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da79ae039b8d8ecfd0f25dc397e0f909bd174215282d35acdf1d652d2405163a`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 6.1 MB (6134432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e331104b5a2920b354684dc09575a324baffa357a7f6d0f1fb72f295736c2`  
		Last Modified: Tue, 15 Jul 2025 19:55:24 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30985de1842eae4c1801550eefc16aa2dd11494d3b0d68b4bfd3eee8e477a969`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:291485af4a8930aeb01d6b2901e705d4e95e732c6b9641951ec8a39056797e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fd0a95567de843d6b30ff329f17bec6a7025150f0bdedd1dc0e66e6d0ced35`

```dockerfile
```

-	Layers:
	-	`sha256:b32eee42ece80938b5d8ccfe8ec8ce549a3c23ba61b4dae5d47b2987444084d9`  
		Last Modified: Tue, 15 Jul 2025 20:57:12 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9fbb7e16a173fecf7e21d9f680c8ad01db7223d9272eb7ce77f00d1e073343d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9839117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e963a992e85fc13c981c490490ffe14da51fb501d335d1ae9179347930be7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422db94aea345dcc4b152e623d957565ff862281021eaf67ca3c633d51915ee`  
		Last Modified: Tue, 15 Jul 2025 19:44:16 GMT  
		Size: 6.1 MB (6111037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd307c13a337a7bea13fe784ac75d29d42bdd8667556e52f5a0a9692b7a636`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b6b324f57973538f4622138b68d8d07a706ab3d27a788fedb1d1363551490b`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:406badf2d3ae772f4bd44c8d377c85c9ead5f36a96c9df85c4548e809c0d119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18389ddb2de7441fcb4b0e971a1363544c7120e69b057660eb6fbdf1a4650407`

```dockerfile
```

-	Layers:
	-	`sha256:774987c353747896140a05754243761038dae43ae58535b71a2c4918f6e606b5`  
		Last Modified: Tue, 15 Jul 2025 20:57:15 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:b1c180246efdee1f796387ed45c5d804ec3cdc7d0d99c9016ec73546545214de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10112489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc2bff49a935d91e94697fcd60f34d6fc3b487d0a8b21fa6df89d5d5931e900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1202729b6d9714c15f30c3dd1bea1d18add10323ffa34e9a0577e120356652d5`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 6.5 MB (6466550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5991bdba51cef03218a54daaf3057e75284c051ef0be6579e0b4fd39f388f6`  
		Last Modified: Tue, 15 Jul 2025 19:41:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334bcc04ba509cb8cdcfc5c52d3fbcb603b47fd5f6678b6600f7aeb1616bf557`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2665ec030c93be192eb44bd8e0517cd08761cd3ad98038dd72a182d8e1fb1cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b807b6464060a5c291e852155161137fa6a827bec9628c68c3d7c21fff68186a`

```dockerfile
```

-	Layers:
	-	`sha256:24831b5b37fe96a1f1d2cf2e30b77d0e59b1acf33b9953bf9fe12643150cb44c`  
		Last Modified: Tue, 15 Jul 2025 20:57:19 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.22`

```console
$ docker pull nats@sha256:eca033f54dbb5d0a5df80c60ff229e53c71de63a8b4ddd0c2f04dd3e55d287df
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

### `nats:2.10-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:820a97ef8a0e8e4b1f1c940c1fbf92e57ad548429dd20754de24ffe4f08996a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad9be7ec221398a67b66fa5f6dc4afe4e24f62ff6a2860f3a914caf5172c90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c015b317061ba6cf363edd67bb9353c30207a61e58e505226168bc0da98afe`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 6.6 MB (6627507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97296c7fe6d9f4da2c4c2dde8e7b27ce58644942a70f97ce0622c116554dc7`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7355fe018b748ae16c9a4bbdaa99767706e56854d8d0535fd5aa2f96fbde81`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2b30e09f1d5f9b8e841201cf1ac53ade8e643572c891218121424a8b792908b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ad2f85e296997148a5e7d39b4527ad05c5559df3691d711ac6d93cc2b2799a`

```dockerfile
```

-	Layers:
	-	`sha256:89817af9341cc2fe811ba2110f7ecca87b5b39105610d0abae9f3e3da0a9777a`  
		Last Modified: Tue, 15 Jul 2025 20:57:03 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:bbbd389071ab1d8d254eb3df7fa93150882b5229c3a99da9d4cdd9d9d9fb4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9852288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa1eb6ecb82b890304acc50b41737e48830c07d6adb9d5457e9eccebadb3768`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acf1350211366512043db3b27f0e92a67c14e308e2f135f34345d30309834ba`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 6.4 MB (6350410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9e0e3d02f0321c18cfb1f4ca8cf20685fcdb82a54101021179760ffa1115b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1209aaaa768e3b746d249f5d8401d372e7d5523f3a4397dde59eb595e0962b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:18c88d88649738fbf3c7c2459ea047163f1256228fa7897077a0bf288dc884b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d11b71658547861a6f90067c7fb4d97c2d27cf0a804fba09a4535f16249da`

```dockerfile
```

-	Layers:
	-	`sha256:cd47a78549dc53d5c15b84eef49a9ad57778519a088bfbdafa38ec0be31ce357`  
		Last Modified: Tue, 15 Jul 2025 20:57:06 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bae5228a4b8fa7abf5b2d2daeda9617519e08cc86149630e7adde2141efeb3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9559514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4262f443d7ff0a48649c5f56e9ea6b6fa4f198ea37b29733999f51ae562c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0607845d0fa55bdc3e76e0de89b169dd06188e51f5b2fb955e7ed32ae35f2380`  
		Last Modified: Tue, 15 Jul 2025 19:34:22 GMT  
		Size: 6.3 MB (6339508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0483d372ec00a330e5264b9f6e35c5d71ac4528d86a6a9584483bc0212031`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5469ded3bdfb31968ff768c86467701029b614a24b30acd8b12cf171bd1e3ef`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9c07cf58635126d1738dbc4853752497aeb197c3bf272aa23efc136bf8f18a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e7a9555de683929fd2a60677efa3416e877cd39c83ddf52e88187ae583703e`

```dockerfile
```

-	Layers:
	-	`sha256:8108e75ff73bb20deeee1f58da34c3cadf06f927494ad913c09b75c63eba39d8`  
		Last Modified: Tue, 15 Jul 2025 20:57:09 GMT  
		Size: 13.2 KB (13197 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:517e9d2a336ceb5f7d2bb56e2e760a0e519bc17980d917a1249963124a3009c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d275fb226d388d4dd3a791d2935b9e666b0bdcbb308c9ed5c3c275b9a6bf1b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da79ae039b8d8ecfd0f25dc397e0f909bd174215282d35acdf1d652d2405163a`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 6.1 MB (6134432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e331104b5a2920b354684dc09575a324baffa357a7f6d0f1fb72f295736c2`  
		Last Modified: Tue, 15 Jul 2025 19:55:24 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30985de1842eae4c1801550eefc16aa2dd11494d3b0d68b4bfd3eee8e477a969`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:291485af4a8930aeb01d6b2901e705d4e95e732c6b9641951ec8a39056797e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fd0a95567de843d6b30ff329f17bec6a7025150f0bdedd1dc0e66e6d0ced35`

```dockerfile
```

-	Layers:
	-	`sha256:b32eee42ece80938b5d8ccfe8ec8ce549a3c23ba61b4dae5d47b2987444084d9`  
		Last Modified: Tue, 15 Jul 2025 20:57:12 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9fbb7e16a173fecf7e21d9f680c8ad01db7223d9272eb7ce77f00d1e073343d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9839117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e963a992e85fc13c981c490490ffe14da51fb501d335d1ae9179347930be7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422db94aea345dcc4b152e623d957565ff862281021eaf67ca3c633d51915ee`  
		Last Modified: Tue, 15 Jul 2025 19:44:16 GMT  
		Size: 6.1 MB (6111037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd307c13a337a7bea13fe784ac75d29d42bdd8667556e52f5a0a9692b7a636`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b6b324f57973538f4622138b68d8d07a706ab3d27a788fedb1d1363551490b`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:406badf2d3ae772f4bd44c8d377c85c9ead5f36a96c9df85c4548e809c0d119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18389ddb2de7441fcb4b0e971a1363544c7120e69b057660eb6fbdf1a4650407`

```dockerfile
```

-	Layers:
	-	`sha256:774987c353747896140a05754243761038dae43ae58535b71a2c4918f6e606b5`  
		Last Modified: Tue, 15 Jul 2025 20:57:15 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:b1c180246efdee1f796387ed45c5d804ec3cdc7d0d99c9016ec73546545214de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10112489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc2bff49a935d91e94697fcd60f34d6fc3b487d0a8b21fa6df89d5d5931e900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1202729b6d9714c15f30c3dd1bea1d18add10323ffa34e9a0577e120356652d5`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 6.5 MB (6466550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5991bdba51cef03218a54daaf3057e75284c051ef0be6579e0b4fd39f388f6`  
		Last Modified: Tue, 15 Jul 2025 19:41:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334bcc04ba509cb8cdcfc5c52d3fbcb603b47fd5f6678b6600f7aeb1616bf557`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2665ec030c93be192eb44bd8e0517cd08761cd3ad98038dd72a182d8e1fb1cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b807b6464060a5c291e852155161137fa6a827bec9628c68c3d7c21fff68186a`

```dockerfile
```

-	Layers:
	-	`sha256:24831b5b37fe96a1f1d2cf2e30b77d0e59b1acf33b9953bf9fe12643150cb44c`  
		Last Modified: Tue, 15 Jul 2025 20:57:19 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:13bf7761f143a1a82892026489162b8699068d239af79e242292b600df83cd18
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

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:937644ce140eeef6e00310097663bc72a3ebc6d7a9ba0fa15aeff4c1bb0870c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:937644ce140eeef6e00310097663bc72a3ebc6d7a9ba0fa15aeff4c1bb0870c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:13bf7761f143a1a82892026489162b8699068d239af79e242292b600df83cd18
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

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:29927408a93e7326852ef265c921ace9e759be2911e7ec85aede94eea816ccd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:be846b5e8cb605dcba06fd770098cce2af40380738f3441e14ae22104232c611
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288662304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade757d73346c5e0022a2f188676344fa11a7fdea7fd404d05b5ee974ee4bbea`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:01 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:27:02 GMT
ENV NATS_SERVER=2.10.29
# Tue, 12 Aug 2025 20:27:04 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 12 Aug 2025 20:27:05 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 12 Aug 2025 20:27:14 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Aug 2025 20:27:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Aug 2025 20:27:33 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:27:34 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:27:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:27:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2a4c01281f1ae501db3064c77b77dbd9ffaaa260b46486f8dfc009cddbd8b1`  
		Last Modified: Tue, 12 Aug 2025 20:29:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296600cfec08efd5530d7fd473aed79a9561c64f71209ca66802d1175aa618a7`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e4271830b813f72ed5591ee787565fcf2da4ad52b65853e264ff6e39283b6f`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662fe2d5b041e59d112c112fb4fc64f3bb6955c72f220821fb2cae76230c695f`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa8dc0c5e39061acce001fc58e690668965a4ab3f56945e7bbdb2d136653bc6`  
		Last Modified: Tue, 12 Aug 2025 20:45:15 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d30b7bdca9af240eea67bcf4d4adf7623350dfe2c833446e0c9a29b9855480`  
		Last Modified: Tue, 12 Aug 2025 20:29:18 GMT  
		Size: 321.5 KB (321463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184936b767a8f9cb88d544108366787e9f5398b7c71da2dcbbd19e9d047e69a6`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 6.6 MB (6636730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103f8877b3beef57c768abb7061975f50c76a237352bc576717f5868e9dcb113`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2585b97227de952538a0ea34cb493ca9f7a87004ebb054e0d5bd8cc1b9e409ca`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eee2932ebf82391707e464199109eac1d85673e4af6b9990443d1a798b3520`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853c197674c3d054317d51e5b282132553b510776d8f41da2e05945fa7d9b083`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:29927408a93e7326852ef265c921ace9e759be2911e7ec85aede94eea816ccd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:be846b5e8cb605dcba06fd770098cce2af40380738f3441e14ae22104232c611
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288662304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade757d73346c5e0022a2f188676344fa11a7fdea7fd404d05b5ee974ee4bbea`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:01 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:27:02 GMT
ENV NATS_SERVER=2.10.29
# Tue, 12 Aug 2025 20:27:04 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 12 Aug 2025 20:27:05 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 12 Aug 2025 20:27:14 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Aug 2025 20:27:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Aug 2025 20:27:33 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:27:34 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:27:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:27:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2a4c01281f1ae501db3064c77b77dbd9ffaaa260b46486f8dfc009cddbd8b1`  
		Last Modified: Tue, 12 Aug 2025 20:29:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296600cfec08efd5530d7fd473aed79a9561c64f71209ca66802d1175aa618a7`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e4271830b813f72ed5591ee787565fcf2da4ad52b65853e264ff6e39283b6f`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662fe2d5b041e59d112c112fb4fc64f3bb6955c72f220821fb2cae76230c695f`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa8dc0c5e39061acce001fc58e690668965a4ab3f56945e7bbdb2d136653bc6`  
		Last Modified: Tue, 12 Aug 2025 20:45:15 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d30b7bdca9af240eea67bcf4d4adf7623350dfe2c833446e0c9a29b9855480`  
		Last Modified: Tue, 12 Aug 2025 20:29:18 GMT  
		Size: 321.5 KB (321463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184936b767a8f9cb88d544108366787e9f5398b7c71da2dcbbd19e9d047e69a6`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 6.6 MB (6636730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103f8877b3beef57c768abb7061975f50c76a237352bc576717f5868e9dcb113`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2585b97227de952538a0ea34cb493ca9f7a87004ebb054e0d5bd8cc1b9e409ca`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eee2932ebf82391707e464199109eac1d85673e4af6b9990443d1a798b3520`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853c197674c3d054317d51e5b282132553b510776d8f41da2e05945fa7d9b083`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29`

```console
$ docker pull nats@sha256:d7f4c3c9a9f33f55714d186653dabf6a267bdb7c01b6026ca52dcc6107cdd195
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
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10.29` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-alpine`

```console
$ docker pull nats@sha256:eca033f54dbb5d0a5df80c60ff229e53c71de63a8b4ddd0c2f04dd3e55d287df
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

### `nats:2.10.29-alpine` - linux; amd64

```console
$ docker pull nats@sha256:820a97ef8a0e8e4b1f1c940c1fbf92e57ad548429dd20754de24ffe4f08996a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad9be7ec221398a67b66fa5f6dc4afe4e24f62ff6a2860f3a914caf5172c90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c015b317061ba6cf363edd67bb9353c30207a61e58e505226168bc0da98afe`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 6.6 MB (6627507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97296c7fe6d9f4da2c4c2dde8e7b27ce58644942a70f97ce0622c116554dc7`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7355fe018b748ae16c9a4bbdaa99767706e56854d8d0535fd5aa2f96fbde81`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2b30e09f1d5f9b8e841201cf1ac53ade8e643572c891218121424a8b792908b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ad2f85e296997148a5e7d39b4527ad05c5559df3691d711ac6d93cc2b2799a`

```dockerfile
```

-	Layers:
	-	`sha256:89817af9341cc2fe811ba2110f7ecca87b5b39105610d0abae9f3e3da0a9777a`  
		Last Modified: Tue, 15 Jul 2025 20:57:03 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bbbd389071ab1d8d254eb3df7fa93150882b5229c3a99da9d4cdd9d9d9fb4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9852288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa1eb6ecb82b890304acc50b41737e48830c07d6adb9d5457e9eccebadb3768`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acf1350211366512043db3b27f0e92a67c14e308e2f135f34345d30309834ba`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 6.4 MB (6350410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9e0e3d02f0321c18cfb1f4ca8cf20685fcdb82a54101021179760ffa1115b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1209aaaa768e3b746d249f5d8401d372e7d5523f3a4397dde59eb595e0962b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:18c88d88649738fbf3c7c2459ea047163f1256228fa7897077a0bf288dc884b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d11b71658547861a6f90067c7fb4d97c2d27cf0a804fba09a4535f16249da`

```dockerfile
```

-	Layers:
	-	`sha256:cd47a78549dc53d5c15b84eef49a9ad57778519a088bfbdafa38ec0be31ce357`  
		Last Modified: Tue, 15 Jul 2025 20:57:06 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bae5228a4b8fa7abf5b2d2daeda9617519e08cc86149630e7adde2141efeb3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9559514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4262f443d7ff0a48649c5f56e9ea6b6fa4f198ea37b29733999f51ae562c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0607845d0fa55bdc3e76e0de89b169dd06188e51f5b2fb955e7ed32ae35f2380`  
		Last Modified: Tue, 15 Jul 2025 19:34:22 GMT  
		Size: 6.3 MB (6339508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0483d372ec00a330e5264b9f6e35c5d71ac4528d86a6a9584483bc0212031`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5469ded3bdfb31968ff768c86467701029b614a24b30acd8b12cf171bd1e3ef`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9c07cf58635126d1738dbc4853752497aeb197c3bf272aa23efc136bf8f18a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e7a9555de683929fd2a60677efa3416e877cd39c83ddf52e88187ae583703e`

```dockerfile
```

-	Layers:
	-	`sha256:8108e75ff73bb20deeee1f58da34c3cadf06f927494ad913c09b75c63eba39d8`  
		Last Modified: Tue, 15 Jul 2025 20:57:09 GMT  
		Size: 13.2 KB (13197 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:517e9d2a336ceb5f7d2bb56e2e760a0e519bc17980d917a1249963124a3009c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d275fb226d388d4dd3a791d2935b9e666b0bdcbb308c9ed5c3c275b9a6bf1b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da79ae039b8d8ecfd0f25dc397e0f909bd174215282d35acdf1d652d2405163a`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 6.1 MB (6134432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e331104b5a2920b354684dc09575a324baffa357a7f6d0f1fb72f295736c2`  
		Last Modified: Tue, 15 Jul 2025 19:55:24 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30985de1842eae4c1801550eefc16aa2dd11494d3b0d68b4bfd3eee8e477a969`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:291485af4a8930aeb01d6b2901e705d4e95e732c6b9641951ec8a39056797e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fd0a95567de843d6b30ff329f17bec6a7025150f0bdedd1dc0e66e6d0ced35`

```dockerfile
```

-	Layers:
	-	`sha256:b32eee42ece80938b5d8ccfe8ec8ce549a3c23ba61b4dae5d47b2987444084d9`  
		Last Modified: Tue, 15 Jul 2025 20:57:12 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9fbb7e16a173fecf7e21d9f680c8ad01db7223d9272eb7ce77f00d1e073343d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9839117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e963a992e85fc13c981c490490ffe14da51fb501d335d1ae9179347930be7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422db94aea345dcc4b152e623d957565ff862281021eaf67ca3c633d51915ee`  
		Last Modified: Tue, 15 Jul 2025 19:44:16 GMT  
		Size: 6.1 MB (6111037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd307c13a337a7bea13fe784ac75d29d42bdd8667556e52f5a0a9692b7a636`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b6b324f57973538f4622138b68d8d07a706ab3d27a788fedb1d1363551490b`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:406badf2d3ae772f4bd44c8d377c85c9ead5f36a96c9df85c4548e809c0d119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18389ddb2de7441fcb4b0e971a1363544c7120e69b057660eb6fbdf1a4650407`

```dockerfile
```

-	Layers:
	-	`sha256:774987c353747896140a05754243761038dae43ae58535b71a2c4918f6e606b5`  
		Last Modified: Tue, 15 Jul 2025 20:57:15 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; s390x

```console
$ docker pull nats@sha256:b1c180246efdee1f796387ed45c5d804ec3cdc7d0d99c9016ec73546545214de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10112489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc2bff49a935d91e94697fcd60f34d6fc3b487d0a8b21fa6df89d5d5931e900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1202729b6d9714c15f30c3dd1bea1d18add10323ffa34e9a0577e120356652d5`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 6.5 MB (6466550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5991bdba51cef03218a54daaf3057e75284c051ef0be6579e0b4fd39f388f6`  
		Last Modified: Tue, 15 Jul 2025 19:41:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334bcc04ba509cb8cdcfc5c52d3fbcb603b47fd5f6678b6600f7aeb1616bf557`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2665ec030c93be192eb44bd8e0517cd08761cd3ad98038dd72a182d8e1fb1cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b807b6464060a5c291e852155161137fa6a827bec9628c68c3d7c21fff68186a`

```dockerfile
```

-	Layers:
	-	`sha256:24831b5b37fe96a1f1d2cf2e30b77d0e59b1acf33b9953bf9fe12643150cb44c`  
		Last Modified: Tue, 15 Jul 2025 20:57:19 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-alpine3.22`

```console
$ docker pull nats@sha256:eca033f54dbb5d0a5df80c60ff229e53c71de63a8b4ddd0c2f04dd3e55d287df
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

### `nats:2.10.29-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:820a97ef8a0e8e4b1f1c940c1fbf92e57ad548429dd20754de24ffe4f08996a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad9be7ec221398a67b66fa5f6dc4afe4e24f62ff6a2860f3a914caf5172c90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c015b317061ba6cf363edd67bb9353c30207a61e58e505226168bc0da98afe`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 6.6 MB (6627507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97296c7fe6d9f4da2c4c2dde8e7b27ce58644942a70f97ce0622c116554dc7`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7355fe018b748ae16c9a4bbdaa99767706e56854d8d0535fd5aa2f96fbde81`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2b30e09f1d5f9b8e841201cf1ac53ade8e643572c891218121424a8b792908b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ad2f85e296997148a5e7d39b4527ad05c5559df3691d711ac6d93cc2b2799a`

```dockerfile
```

-	Layers:
	-	`sha256:89817af9341cc2fe811ba2110f7ecca87b5b39105610d0abae9f3e3da0a9777a`  
		Last Modified: Tue, 15 Jul 2025 20:57:03 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:bbbd389071ab1d8d254eb3df7fa93150882b5229c3a99da9d4cdd9d9d9fb4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9852288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa1eb6ecb82b890304acc50b41737e48830c07d6adb9d5457e9eccebadb3768`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acf1350211366512043db3b27f0e92a67c14e308e2f135f34345d30309834ba`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 6.4 MB (6350410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9e0e3d02f0321c18cfb1f4ca8cf20685fcdb82a54101021179760ffa1115b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1209aaaa768e3b746d249f5d8401d372e7d5523f3a4397dde59eb595e0962b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:18c88d88649738fbf3c7c2459ea047163f1256228fa7897077a0bf288dc884b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d11b71658547861a6f90067c7fb4d97c2d27cf0a804fba09a4535f16249da`

```dockerfile
```

-	Layers:
	-	`sha256:cd47a78549dc53d5c15b84eef49a9ad57778519a088bfbdafa38ec0be31ce357`  
		Last Modified: Tue, 15 Jul 2025 20:57:06 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bae5228a4b8fa7abf5b2d2daeda9617519e08cc86149630e7adde2141efeb3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9559514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4262f443d7ff0a48649c5f56e9ea6b6fa4f198ea37b29733999f51ae562c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0607845d0fa55bdc3e76e0de89b169dd06188e51f5b2fb955e7ed32ae35f2380`  
		Last Modified: Tue, 15 Jul 2025 19:34:22 GMT  
		Size: 6.3 MB (6339508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0483d372ec00a330e5264b9f6e35c5d71ac4528d86a6a9584483bc0212031`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5469ded3bdfb31968ff768c86467701029b614a24b30acd8b12cf171bd1e3ef`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9c07cf58635126d1738dbc4853752497aeb197c3bf272aa23efc136bf8f18a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e7a9555de683929fd2a60677efa3416e877cd39c83ddf52e88187ae583703e`

```dockerfile
```

-	Layers:
	-	`sha256:8108e75ff73bb20deeee1f58da34c3cadf06f927494ad913c09b75c63eba39d8`  
		Last Modified: Tue, 15 Jul 2025 20:57:09 GMT  
		Size: 13.2 KB (13197 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:517e9d2a336ceb5f7d2bb56e2e760a0e519bc17980d917a1249963124a3009c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d275fb226d388d4dd3a791d2935b9e666b0bdcbb308c9ed5c3c275b9a6bf1b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da79ae039b8d8ecfd0f25dc397e0f909bd174215282d35acdf1d652d2405163a`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 6.1 MB (6134432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e331104b5a2920b354684dc09575a324baffa357a7f6d0f1fb72f295736c2`  
		Last Modified: Tue, 15 Jul 2025 19:55:24 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30985de1842eae4c1801550eefc16aa2dd11494d3b0d68b4bfd3eee8e477a969`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:291485af4a8930aeb01d6b2901e705d4e95e732c6b9641951ec8a39056797e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fd0a95567de843d6b30ff329f17bec6a7025150f0bdedd1dc0e66e6d0ced35`

```dockerfile
```

-	Layers:
	-	`sha256:b32eee42ece80938b5d8ccfe8ec8ce549a3c23ba61b4dae5d47b2987444084d9`  
		Last Modified: Tue, 15 Jul 2025 20:57:12 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9fbb7e16a173fecf7e21d9f680c8ad01db7223d9272eb7ce77f00d1e073343d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9839117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e963a992e85fc13c981c490490ffe14da51fb501d335d1ae9179347930be7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422db94aea345dcc4b152e623d957565ff862281021eaf67ca3c633d51915ee`  
		Last Modified: Tue, 15 Jul 2025 19:44:16 GMT  
		Size: 6.1 MB (6111037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd307c13a337a7bea13fe784ac75d29d42bdd8667556e52f5a0a9692b7a636`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b6b324f57973538f4622138b68d8d07a706ab3d27a788fedb1d1363551490b`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:406badf2d3ae772f4bd44c8d377c85c9ead5f36a96c9df85c4548e809c0d119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18389ddb2de7441fcb4b0e971a1363544c7120e69b057660eb6fbdf1a4650407`

```dockerfile
```

-	Layers:
	-	`sha256:774987c353747896140a05754243761038dae43ae58535b71a2c4918f6e606b5`  
		Last Modified: Tue, 15 Jul 2025 20:57:15 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:b1c180246efdee1f796387ed45c5d804ec3cdc7d0d99c9016ec73546545214de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10112489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc2bff49a935d91e94697fcd60f34d6fc3b487d0a8b21fa6df89d5d5931e900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1202729b6d9714c15f30c3dd1bea1d18add10323ffa34e9a0577e120356652d5`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 6.5 MB (6466550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5991bdba51cef03218a54daaf3057e75284c051ef0be6579e0b4fd39f388f6`  
		Last Modified: Tue, 15 Jul 2025 19:41:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334bcc04ba509cb8cdcfc5c52d3fbcb603b47fd5f6678b6600f7aeb1616bf557`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2665ec030c93be192eb44bd8e0517cd08761cd3ad98038dd72a182d8e1fb1cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b807b6464060a5c291e852155161137fa6a827bec9628c68c3d7c21fff68186a`

```dockerfile
```

-	Layers:
	-	`sha256:24831b5b37fe96a1f1d2cf2e30b77d0e59b1acf33b9953bf9fe12643150cb44c`  
		Last Modified: Tue, 15 Jul 2025 20:57:19 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-linux`

```console
$ docker pull nats@sha256:13bf7761f143a1a82892026489162b8699068d239af79e242292b600df83cd18
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

### `nats:2.10.29-linux` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-nanoserver`

```console
$ docker pull nats@sha256:937644ce140eeef6e00310097663bc72a3ebc6d7a9ba0fa15aeff4c1bb0870c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10.29-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:937644ce140eeef6e00310097663bc72a3ebc6d7a9ba0fa15aeff4c1bb0870c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10.29-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-scratch`

```console
$ docker pull nats@sha256:13bf7761f143a1a82892026489162b8699068d239af79e242292b600df83cd18
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

### `nats:2.10.29-scratch` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-windowsservercore`

```console
$ docker pull nats@sha256:29927408a93e7326852ef265c921ace9e759be2911e7ec85aede94eea816ccd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10.29-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:be846b5e8cb605dcba06fd770098cce2af40380738f3441e14ae22104232c611
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288662304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade757d73346c5e0022a2f188676344fa11a7fdea7fd404d05b5ee974ee4bbea`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:01 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:27:02 GMT
ENV NATS_SERVER=2.10.29
# Tue, 12 Aug 2025 20:27:04 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 12 Aug 2025 20:27:05 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 12 Aug 2025 20:27:14 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Aug 2025 20:27:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Aug 2025 20:27:33 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:27:34 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:27:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:27:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2a4c01281f1ae501db3064c77b77dbd9ffaaa260b46486f8dfc009cddbd8b1`  
		Last Modified: Tue, 12 Aug 2025 20:29:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296600cfec08efd5530d7fd473aed79a9561c64f71209ca66802d1175aa618a7`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e4271830b813f72ed5591ee787565fcf2da4ad52b65853e264ff6e39283b6f`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662fe2d5b041e59d112c112fb4fc64f3bb6955c72f220821fb2cae76230c695f`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa8dc0c5e39061acce001fc58e690668965a4ab3f56945e7bbdb2d136653bc6`  
		Last Modified: Tue, 12 Aug 2025 20:45:15 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d30b7bdca9af240eea67bcf4d4adf7623350dfe2c833446e0c9a29b9855480`  
		Last Modified: Tue, 12 Aug 2025 20:29:18 GMT  
		Size: 321.5 KB (321463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184936b767a8f9cb88d544108366787e9f5398b7c71da2dcbbd19e9d047e69a6`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 6.6 MB (6636730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103f8877b3beef57c768abb7061975f50c76a237352bc576717f5868e9dcb113`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2585b97227de952538a0ea34cb493ca9f7a87004ebb054e0d5bd8cc1b9e409ca`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eee2932ebf82391707e464199109eac1d85673e4af6b9990443d1a798b3520`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853c197674c3d054317d51e5b282132553b510776d8f41da2e05945fa7d9b083`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:29927408a93e7326852ef265c921ace9e759be2911e7ec85aede94eea816ccd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10.29-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:be846b5e8cb605dcba06fd770098cce2af40380738f3441e14ae22104232c611
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288662304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade757d73346c5e0022a2f188676344fa11a7fdea7fd404d05b5ee974ee4bbea`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:01 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:27:02 GMT
ENV NATS_SERVER=2.10.29
# Tue, 12 Aug 2025 20:27:04 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 12 Aug 2025 20:27:05 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 12 Aug 2025 20:27:14 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Aug 2025 20:27:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Aug 2025 20:27:33 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:27:34 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:27:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:27:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2a4c01281f1ae501db3064c77b77dbd9ffaaa260b46486f8dfc009cddbd8b1`  
		Last Modified: Tue, 12 Aug 2025 20:29:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296600cfec08efd5530d7fd473aed79a9561c64f71209ca66802d1175aa618a7`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e4271830b813f72ed5591ee787565fcf2da4ad52b65853e264ff6e39283b6f`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662fe2d5b041e59d112c112fb4fc64f3bb6955c72f220821fb2cae76230c695f`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa8dc0c5e39061acce001fc58e690668965a4ab3f56945e7bbdb2d136653bc6`  
		Last Modified: Tue, 12 Aug 2025 20:45:15 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d30b7bdca9af240eea67bcf4d4adf7623350dfe2c833446e0c9a29b9855480`  
		Last Modified: Tue, 12 Aug 2025 20:29:18 GMT  
		Size: 321.5 KB (321463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184936b767a8f9cb88d544108366787e9f5398b7c71da2dcbbd19e9d047e69a6`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 6.6 MB (6636730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103f8877b3beef57c768abb7061975f50c76a237352bc576717f5868e9dcb113`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2585b97227de952538a0ea34cb493ca9f7a87004ebb054e0d5bd8cc1b9e409ca`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eee2932ebf82391707e464199109eac1d85673e4af6b9990443d1a798b3520`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853c197674c3d054317d51e5b282132553b510776d8f41da2e05945fa7d9b083`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:a8fe3a4066d3c14d893dd92a6d85f117cfb3567d4d0df11bc3161782b34dc351
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
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:777787bbb4c7c4083ec2213b0b8b14151617610a3e0d85776bd995cd46599c73
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
$ docker pull nats@sha256:383e95bac92d099fa612f6bbe5c4c83ae15af22e409a89fecd2e3c5092a8b2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e317eb6ac10bc33a158896aec219c58122b17191d82ad8059edfdd348687beca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab2a6f9512b153493f557d6c5cfaaa4a7c3cb1211f22480cb0d5c50d3a4b17`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 6.8 MB (6811571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee5018631bdb543650e4026cef806de7225147757a9e052ab075bc9ce41192`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4d4963114e48d99ec239e86fdee1a87c26a0e2d581a26bc7a82c659486b221`  
		Last Modified: Tue, 09 Sep 2025 21:28:03 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ba0a85e05e92baa4dc25c2d468c7055ed378ed85e8cef076e528de3db68d5d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d338ea42bfc75ac6382f89e464fb4f8968277e57e510d15d0516ec454dc2a8ee`

```dockerfile
```

-	Layers:
	-	`sha256:afdda197879734c0f39320dd4b5d9022177afc5ed488a2ec3bc5100477686c47`  
		Last Modified: Tue, 09 Sep 2025 23:56:39 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e40ee2e909ecb5d5497f954e4bae9fe52ff74799dc1916a38a9501d3a601236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10023996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a9c25c10fb7e66ad634861abcd1f91711d6ad5aeb2f3c7107b22f6ada83fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2acf2abeee38084f132adc7fc2df4157782dac0272a686992cf569149b35f9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 6.5 MB (6522116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590716c3787e83b577093cbf8f4c94109c354ce9d4a8f4e1a77c40df98d08323`  
		Last Modified: Tue, 09 Sep 2025 21:43:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a98b784cf4f30652bb9977f4b8182b43e8facd172a4941225c99ab5995dba9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8328b4789d4fbe7d5b301f3bd5035ae9db9ad28510f44990ee8566e1e7e1dbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddc73c38f5ff5cf3bb96c33e0ce7c05fbc401d129d48c24368267d9cc5605bc`

```dockerfile
```

-	Layers:
	-	`sha256:2db5fa19161bff44ba2f7e98f558c2306b54b8593a3acd92b4c51812baaadf96`  
		Last Modified: Tue, 09 Sep 2025 23:56:42 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:da2887adbe5a9b5ce19ba1daf5f5323382993e2999e1a5450dea6d5d615af554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9732548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa53562ec436568c3bf00db1fb91bc89ebfddf47fe2f946af086551b7d0240d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031341d8662c24b611d19217b15697c7e1eeb7fb20ae015769304f3d9e416f4`  
		Last Modified: Tue, 09 Sep 2025 21:59:39 GMT  
		Size: 6.5 MB (6512539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4721d57828fe2cba2dda46e5e717ad9ee4278ab187e170e498625e6116e7d5f`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc30ccba0a3c016998f1b5b2e2cdccd8d8f698e228a65dd364b2adb41b185f3`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:af1dd4d927ea33740d8992643ce68d26a2d5ff2e68fa53849efbaec72158a770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e92010b8b482e98d125d98981583e131f2df9dbd380f6b38cbcd1b45eb9b95`

```dockerfile
```

-	Layers:
	-	`sha256:785b567e7e5ebabe0f6b6d6e32479ec15565ad1886ce491f7b90e7af1eae9c54`  
		Last Modified: Tue, 09 Sep 2025 23:56:45 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b78f1e58f75bba9a7393b5f2bfe919ed0516e154ceb1260cdc013093e0d08daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e807b412fc1138feba48d67aa5c005eea691e786927abca0174930a194059dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81efb27a24236aa9d4dd850761611e76ba6addbab29a3200f3394ddb61e8b457`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.3 MB (6299385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82430e347407921b5c2f85841823aac9ee8ad9e3e96a91c355b0195f303337e`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a300c8b17b92657dc962e711a386e4a85537831d47c4dd21abdf78281c75ffe2`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:17e3e88060ad541c6b4c32996093543b4dff70e3ed4858411180475c8fdb726a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52155310f554543e3eba1ff4e53c6d064d0c1554b36243f55cc7b47991d1bffb`

```dockerfile
```

-	Layers:
	-	`sha256:71290e70b093feda2cec83ba57599465c9c85d6a25207135ffe14156b636e16a`  
		Last Modified: Tue, 09 Sep 2025 23:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:54e05d0d4583d88acae58396444e5a856104ea167b8be5441bc559181cc5a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10005035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f0fa028221d6d5d34463a7ae1561e9c4b6429343c173387bb4b6ca560be435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdf74981cd55b1384057c7128506e55ba5cb405d3805d01d372d78639b6f68f`  
		Last Modified: Tue, 09 Sep 2025 22:41:34 GMT  
		Size: 6.3 MB (6276953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20c0fbc0352f22902cf45129dfed4ad8d39bdfb4ddc662750875e826f0fa048`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9a8a923704ae9582e7e000943845e579ce24fe430b260de5e0b6511b8ada0`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:edc001c19fc6f746a25c2ad86c35a9ae36ea65996d0bb0c4fb079541607a2b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea334b98e4c0c7cdf7544a7944458efbd59d206ffb201dbc9bfde0fcd1eb081`

```dockerfile
```

-	Layers:
	-	`sha256:fb1473e3d857e75ce42f899fae73871d5325888dd66b94dccebb3a786e13a6f1`  
		Last Modified: Tue, 09 Sep 2025 23:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:c092626e962687b5c5819475844a8aabd59265be101a1c6876a1ac9c4293e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8d1105a8bbefc2fc8ded940d6b0bfb291fedfa8496dbe6671ea9f1675a0b3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee21526533161753c86a71f59d0df970aa35c45d24fdef163007b752fe70e3`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 6.6 MB (6646165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b3c4b7b79090468183fcf1696975567f84eb65fb97befa05d25ce48efccee`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e44737618f643a95798867bcd27e21c0ea885cede55a7fb81f96a9c7c7e19c`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c0ce755324c31309757a9e71aec2d4164dd8e5eb70127b5ff8d402fe15807f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ffb49aae826cb2119b2c3420d4f3b9c2cd24d4f20626d536cf9b4606d1dc9`

```dockerfile
```

-	Layers:
	-	`sha256:5badeeb273e199fa585a1f83872b8d1f5ba9c8987464a21caec5530d62973b86`  
		Last Modified: Tue, 09 Sep 2025 23:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.22`

```console
$ docker pull nats@sha256:777787bbb4c7c4083ec2213b0b8b14151617610a3e0d85776bd995cd46599c73
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
$ docker pull nats@sha256:383e95bac92d099fa612f6bbe5c4c83ae15af22e409a89fecd2e3c5092a8b2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e317eb6ac10bc33a158896aec219c58122b17191d82ad8059edfdd348687beca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab2a6f9512b153493f557d6c5cfaaa4a7c3cb1211f22480cb0d5c50d3a4b17`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 6.8 MB (6811571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee5018631bdb543650e4026cef806de7225147757a9e052ab075bc9ce41192`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4d4963114e48d99ec239e86fdee1a87c26a0e2d581a26bc7a82c659486b221`  
		Last Modified: Tue, 09 Sep 2025 21:28:03 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ba0a85e05e92baa4dc25c2d468c7055ed378ed85e8cef076e528de3db68d5d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d338ea42bfc75ac6382f89e464fb4f8968277e57e510d15d0516ec454dc2a8ee`

```dockerfile
```

-	Layers:
	-	`sha256:afdda197879734c0f39320dd4b5d9022177afc5ed488a2ec3bc5100477686c47`  
		Last Modified: Tue, 09 Sep 2025 23:56:39 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e40ee2e909ecb5d5497f954e4bae9fe52ff74799dc1916a38a9501d3a601236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10023996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a9c25c10fb7e66ad634861abcd1f91711d6ad5aeb2f3c7107b22f6ada83fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2acf2abeee38084f132adc7fc2df4157782dac0272a686992cf569149b35f9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 6.5 MB (6522116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590716c3787e83b577093cbf8f4c94109c354ce9d4a8f4e1a77c40df98d08323`  
		Last Modified: Tue, 09 Sep 2025 21:43:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a98b784cf4f30652bb9977f4b8182b43e8facd172a4941225c99ab5995dba9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8328b4789d4fbe7d5b301f3bd5035ae9db9ad28510f44990ee8566e1e7e1dbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddc73c38f5ff5cf3bb96c33e0ce7c05fbc401d129d48c24368267d9cc5605bc`

```dockerfile
```

-	Layers:
	-	`sha256:2db5fa19161bff44ba2f7e98f558c2306b54b8593a3acd92b4c51812baaadf96`  
		Last Modified: Tue, 09 Sep 2025 23:56:42 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:da2887adbe5a9b5ce19ba1daf5f5323382993e2999e1a5450dea6d5d615af554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9732548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa53562ec436568c3bf00db1fb91bc89ebfddf47fe2f946af086551b7d0240d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031341d8662c24b611d19217b15697c7e1eeb7fb20ae015769304f3d9e416f4`  
		Last Modified: Tue, 09 Sep 2025 21:59:39 GMT  
		Size: 6.5 MB (6512539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4721d57828fe2cba2dda46e5e717ad9ee4278ab187e170e498625e6116e7d5f`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc30ccba0a3c016998f1b5b2e2cdccd8d8f698e228a65dd364b2adb41b185f3`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:af1dd4d927ea33740d8992643ce68d26a2d5ff2e68fa53849efbaec72158a770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e92010b8b482e98d125d98981583e131f2df9dbd380f6b38cbcd1b45eb9b95`

```dockerfile
```

-	Layers:
	-	`sha256:785b567e7e5ebabe0f6b6d6e32479ec15565ad1886ce491f7b90e7af1eae9c54`  
		Last Modified: Tue, 09 Sep 2025 23:56:45 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b78f1e58f75bba9a7393b5f2bfe919ed0516e154ceb1260cdc013093e0d08daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e807b412fc1138feba48d67aa5c005eea691e786927abca0174930a194059dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81efb27a24236aa9d4dd850761611e76ba6addbab29a3200f3394ddb61e8b457`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.3 MB (6299385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82430e347407921b5c2f85841823aac9ee8ad9e3e96a91c355b0195f303337e`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a300c8b17b92657dc962e711a386e4a85537831d47c4dd21abdf78281c75ffe2`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:17e3e88060ad541c6b4c32996093543b4dff70e3ed4858411180475c8fdb726a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52155310f554543e3eba1ff4e53c6d064d0c1554b36243f55cc7b47991d1bffb`

```dockerfile
```

-	Layers:
	-	`sha256:71290e70b093feda2cec83ba57599465c9c85d6a25207135ffe14156b636e16a`  
		Last Modified: Tue, 09 Sep 2025 23:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:54e05d0d4583d88acae58396444e5a856104ea167b8be5441bc559181cc5a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10005035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f0fa028221d6d5d34463a7ae1561e9c4b6429343c173387bb4b6ca560be435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdf74981cd55b1384057c7128506e55ba5cb405d3805d01d372d78639b6f68f`  
		Last Modified: Tue, 09 Sep 2025 22:41:34 GMT  
		Size: 6.3 MB (6276953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20c0fbc0352f22902cf45129dfed4ad8d39bdfb4ddc662750875e826f0fa048`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9a8a923704ae9582e7e000943845e579ce24fe430b260de5e0b6511b8ada0`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:edc001c19fc6f746a25c2ad86c35a9ae36ea65996d0bb0c4fb079541607a2b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea334b98e4c0c7cdf7544a7944458efbd59d206ffb201dbc9bfde0fcd1eb081`

```dockerfile
```

-	Layers:
	-	`sha256:fb1473e3d857e75ce42f899fae73871d5325888dd66b94dccebb3a786e13a6f1`  
		Last Modified: Tue, 09 Sep 2025 23:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:c092626e962687b5c5819475844a8aabd59265be101a1c6876a1ac9c4293e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8d1105a8bbefc2fc8ded940d6b0bfb291fedfa8496dbe6671ea9f1675a0b3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee21526533161753c86a71f59d0df970aa35c45d24fdef163007b752fe70e3`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 6.6 MB (6646165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b3c4b7b79090468183fcf1696975567f84eb65fb97befa05d25ce48efccee`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e44737618f643a95798867bcd27e21c0ea885cede55a7fb81f96a9c7c7e19c`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c0ce755324c31309757a9e71aec2d4164dd8e5eb70127b5ff8d402fe15807f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ffb49aae826cb2119b2c3420d4f3b9c2cd24d4f20626d536cf9b4606d1dc9`

```dockerfile
```

-	Layers:
	-	`sha256:5badeeb273e199fa585a1f83872b8d1f5ba9c8987464a21caec5530d62973b86`  
		Last Modified: Tue, 09 Sep 2025 23:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:ee3312f4e9d4b67ff197b0ed1e98756596f0d7db872e7fe30d9bf64fccddf92c
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
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:950519f31ba604e5d89f5b7abb1aa2dfa10b04b00e7559e52cdaa0c5f077b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:950519f31ba604e5d89f5b7abb1aa2dfa10b04b00e7559e52cdaa0c5f077b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:ee3312f4e9d4b67ff197b0ed1e98756596f0d7db872e7fe30d9bf64fccddf92c
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
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:bb0d35aa5eed764e627f92b57cb5eceaaf6707b0ae52ddf0c31716c54870bb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:6adfca3411b50bb2d743507583ac87476d7965b2cbed6518a20d4931d3491f45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288928787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98c80bef79058b0466c1d9f41b8d4ca392f9ba73250a750c7ea21bab930aa97`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 21:27:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Sep 2025 21:27:29 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 21:27:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 21:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.9/nats-server-v2.11.9-windows-amd64.zip
# Tue, 09 Sep 2025 21:27:33 GMT
ENV NATS_SERVER_SHASUM=841a953d9be1d55b5f2b990c624b239f7f938baaf00d5627ac34d6c363a2fda3
# Tue, 09 Sep 2025 21:27:53 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Sep 2025 21:28:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Sep 2025 21:28:15 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 21:28:16 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 21:28:18 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 21:28:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873d00bcaff9497f2d332fa6897defb80cc97bf202af48ef6c713377e8d9df48`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b198342f09ddc645f6fc2b65a830146f5d0d7b0fe1eb41f306dde5eef7f46b`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990e7ded3458108fd3c5e4e46d956fb4821b25c1be30560397a4c05e6bbffc3c`  
		Last Modified: Tue, 09 Sep 2025 21:28:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8258a2f8d54eef32d8c8da5489e1222917b41d56e62e97b7889cad5929dac7`  
		Last Modified: Tue, 09 Sep 2025 21:28:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2939a4cd8a8edb8a73065013d6ff136be09a5c80fb388692a0eb284bb9516d91`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c8f62dd915a272e9ebf61afe2ec754bfb7592db3760a577412e1456b4a1a3d`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 343.2 KB (343172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8604f83c30deda1e29d968f6384c4e584eeb306c7df98b9a754743e760128785`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.9 MB (6881510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a7e192f98db48a22a47dd45e84dace5542d6245b2f0acfb82d28be2485dd13`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f754f15699c71eb0c940dac7c0ff3f6e668ea993a2b45320344a34f5b9006f77`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc414a41a0ef3729968b13a6c80750a0f8afb723bebab36a4fd4e0d76ae4cc4`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3955ff1a4e10e862f6c1364516e5e72757e2ec571b70019de550d19b435131c`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:bb0d35aa5eed764e627f92b57cb5eceaaf6707b0ae52ddf0c31716c54870bb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:6adfca3411b50bb2d743507583ac87476d7965b2cbed6518a20d4931d3491f45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288928787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98c80bef79058b0466c1d9f41b8d4ca392f9ba73250a750c7ea21bab930aa97`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 21:27:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Sep 2025 21:27:29 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 21:27:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 21:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.9/nats-server-v2.11.9-windows-amd64.zip
# Tue, 09 Sep 2025 21:27:33 GMT
ENV NATS_SERVER_SHASUM=841a953d9be1d55b5f2b990c624b239f7f938baaf00d5627ac34d6c363a2fda3
# Tue, 09 Sep 2025 21:27:53 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Sep 2025 21:28:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Sep 2025 21:28:15 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 21:28:16 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 21:28:18 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 21:28:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873d00bcaff9497f2d332fa6897defb80cc97bf202af48ef6c713377e8d9df48`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b198342f09ddc645f6fc2b65a830146f5d0d7b0fe1eb41f306dde5eef7f46b`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990e7ded3458108fd3c5e4e46d956fb4821b25c1be30560397a4c05e6bbffc3c`  
		Last Modified: Tue, 09 Sep 2025 21:28:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8258a2f8d54eef32d8c8da5489e1222917b41d56e62e97b7889cad5929dac7`  
		Last Modified: Tue, 09 Sep 2025 21:28:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2939a4cd8a8edb8a73065013d6ff136be09a5c80fb388692a0eb284bb9516d91`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c8f62dd915a272e9ebf61afe2ec754bfb7592db3760a577412e1456b4a1a3d`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 343.2 KB (343172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8604f83c30deda1e29d968f6384c4e584eeb306c7df98b9a754743e760128785`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.9 MB (6881510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a7e192f98db48a22a47dd45e84dace5542d6245b2f0acfb82d28be2485dd13`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f754f15699c71eb0c940dac7c0ff3f6e668ea993a2b45320344a34f5b9006f77`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc414a41a0ef3729968b13a6c80750a0f8afb723bebab36a4fd4e0d76ae4cc4`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3955ff1a4e10e862f6c1364516e5e72757e2ec571b70019de550d19b435131c`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.9`

```console
$ docker pull nats@sha256:a8fe3a4066d3c14d893dd92a6d85f117cfb3567d4d0df11bc3161782b34dc351
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
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11.9` - linux; amd64

```console
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.9-alpine`

```console
$ docker pull nats@sha256:777787bbb4c7c4083ec2213b0b8b14151617610a3e0d85776bd995cd46599c73
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

### `nats:2.11.9-alpine` - linux; amd64

```console
$ docker pull nats@sha256:383e95bac92d099fa612f6bbe5c4c83ae15af22e409a89fecd2e3c5092a8b2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e317eb6ac10bc33a158896aec219c58122b17191d82ad8059edfdd348687beca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab2a6f9512b153493f557d6c5cfaaa4a7c3cb1211f22480cb0d5c50d3a4b17`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 6.8 MB (6811571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee5018631bdb543650e4026cef806de7225147757a9e052ab075bc9ce41192`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4d4963114e48d99ec239e86fdee1a87c26a0e2d581a26bc7a82c659486b221`  
		Last Modified: Tue, 09 Sep 2025 21:28:03 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ba0a85e05e92baa4dc25c2d468c7055ed378ed85e8cef076e528de3db68d5d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d338ea42bfc75ac6382f89e464fb4f8968277e57e510d15d0516ec454dc2a8ee`

```dockerfile
```

-	Layers:
	-	`sha256:afdda197879734c0f39320dd4b5d9022177afc5ed488a2ec3bc5100477686c47`  
		Last Modified: Tue, 09 Sep 2025 23:56:39 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e40ee2e909ecb5d5497f954e4bae9fe52ff74799dc1916a38a9501d3a601236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10023996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a9c25c10fb7e66ad634861abcd1f91711d6ad5aeb2f3c7107b22f6ada83fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2acf2abeee38084f132adc7fc2df4157782dac0272a686992cf569149b35f9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 6.5 MB (6522116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590716c3787e83b577093cbf8f4c94109c354ce9d4a8f4e1a77c40df98d08323`  
		Last Modified: Tue, 09 Sep 2025 21:43:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a98b784cf4f30652bb9977f4b8182b43e8facd172a4941225c99ab5995dba9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8328b4789d4fbe7d5b301f3bd5035ae9db9ad28510f44990ee8566e1e7e1dbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddc73c38f5ff5cf3bb96c33e0ce7c05fbc401d129d48c24368267d9cc5605bc`

```dockerfile
```

-	Layers:
	-	`sha256:2db5fa19161bff44ba2f7e98f558c2306b54b8593a3acd92b4c51812baaadf96`  
		Last Modified: Tue, 09 Sep 2025 23:56:42 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:da2887adbe5a9b5ce19ba1daf5f5323382993e2999e1a5450dea6d5d615af554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9732548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa53562ec436568c3bf00db1fb91bc89ebfddf47fe2f946af086551b7d0240d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031341d8662c24b611d19217b15697c7e1eeb7fb20ae015769304f3d9e416f4`  
		Last Modified: Tue, 09 Sep 2025 21:59:39 GMT  
		Size: 6.5 MB (6512539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4721d57828fe2cba2dda46e5e717ad9ee4278ab187e170e498625e6116e7d5f`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc30ccba0a3c016998f1b5b2e2cdccd8d8f698e228a65dd364b2adb41b185f3`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:af1dd4d927ea33740d8992643ce68d26a2d5ff2e68fa53849efbaec72158a770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e92010b8b482e98d125d98981583e131f2df9dbd380f6b38cbcd1b45eb9b95`

```dockerfile
```

-	Layers:
	-	`sha256:785b567e7e5ebabe0f6b6d6e32479ec15565ad1886ce491f7b90e7af1eae9c54`  
		Last Modified: Tue, 09 Sep 2025 23:56:45 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b78f1e58f75bba9a7393b5f2bfe919ed0516e154ceb1260cdc013093e0d08daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e807b412fc1138feba48d67aa5c005eea691e786927abca0174930a194059dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81efb27a24236aa9d4dd850761611e76ba6addbab29a3200f3394ddb61e8b457`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.3 MB (6299385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82430e347407921b5c2f85841823aac9ee8ad9e3e96a91c355b0195f303337e`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a300c8b17b92657dc962e711a386e4a85537831d47c4dd21abdf78281c75ffe2`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:17e3e88060ad541c6b4c32996093543b4dff70e3ed4858411180475c8fdb726a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52155310f554543e3eba1ff4e53c6d064d0c1554b36243f55cc7b47991d1bffb`

```dockerfile
```

-	Layers:
	-	`sha256:71290e70b093feda2cec83ba57599465c9c85d6a25207135ffe14156b636e16a`  
		Last Modified: Tue, 09 Sep 2025 23:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:54e05d0d4583d88acae58396444e5a856104ea167b8be5441bc559181cc5a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10005035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f0fa028221d6d5d34463a7ae1561e9c4b6429343c173387bb4b6ca560be435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdf74981cd55b1384057c7128506e55ba5cb405d3805d01d372d78639b6f68f`  
		Last Modified: Tue, 09 Sep 2025 22:41:34 GMT  
		Size: 6.3 MB (6276953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20c0fbc0352f22902cf45129dfed4ad8d39bdfb4ddc662750875e826f0fa048`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9a8a923704ae9582e7e000943845e579ce24fe430b260de5e0b6511b8ada0`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:edc001c19fc6f746a25c2ad86c35a9ae36ea65996d0bb0c4fb079541607a2b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea334b98e4c0c7cdf7544a7944458efbd59d206ffb201dbc9bfde0fcd1eb081`

```dockerfile
```

-	Layers:
	-	`sha256:fb1473e3d857e75ce42f899fae73871d5325888dd66b94dccebb3a786e13a6f1`  
		Last Modified: Tue, 09 Sep 2025 23:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-alpine` - linux; s390x

```console
$ docker pull nats@sha256:c092626e962687b5c5819475844a8aabd59265be101a1c6876a1ac9c4293e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8d1105a8bbefc2fc8ded940d6b0bfb291fedfa8496dbe6671ea9f1675a0b3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee21526533161753c86a71f59d0df970aa35c45d24fdef163007b752fe70e3`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 6.6 MB (6646165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b3c4b7b79090468183fcf1696975567f84eb65fb97befa05d25ce48efccee`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e44737618f643a95798867bcd27e21c0ea885cede55a7fb81f96a9c7c7e19c`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c0ce755324c31309757a9e71aec2d4164dd8e5eb70127b5ff8d402fe15807f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ffb49aae826cb2119b2c3420d4f3b9c2cd24d4f20626d536cf9b4606d1dc9`

```dockerfile
```

-	Layers:
	-	`sha256:5badeeb273e199fa585a1f83872b8d1f5ba9c8987464a21caec5530d62973b86`  
		Last Modified: Tue, 09 Sep 2025 23:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.9-alpine3.22`

```console
$ docker pull nats@sha256:777787bbb4c7c4083ec2213b0b8b14151617610a3e0d85776bd995cd46599c73
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

### `nats:2.11.9-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:383e95bac92d099fa612f6bbe5c4c83ae15af22e409a89fecd2e3c5092a8b2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e317eb6ac10bc33a158896aec219c58122b17191d82ad8059edfdd348687beca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab2a6f9512b153493f557d6c5cfaaa4a7c3cb1211f22480cb0d5c50d3a4b17`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 6.8 MB (6811571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee5018631bdb543650e4026cef806de7225147757a9e052ab075bc9ce41192`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4d4963114e48d99ec239e86fdee1a87c26a0e2d581a26bc7a82c659486b221`  
		Last Modified: Tue, 09 Sep 2025 21:28:03 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ba0a85e05e92baa4dc25c2d468c7055ed378ed85e8cef076e528de3db68d5d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d338ea42bfc75ac6382f89e464fb4f8968277e57e510d15d0516ec454dc2a8ee`

```dockerfile
```

-	Layers:
	-	`sha256:afdda197879734c0f39320dd4b5d9022177afc5ed488a2ec3bc5100477686c47`  
		Last Modified: Tue, 09 Sep 2025 23:56:39 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e40ee2e909ecb5d5497f954e4bae9fe52ff74799dc1916a38a9501d3a601236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10023996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a9c25c10fb7e66ad634861abcd1f91711d6ad5aeb2f3c7107b22f6ada83fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2acf2abeee38084f132adc7fc2df4157782dac0272a686992cf569149b35f9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 6.5 MB (6522116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590716c3787e83b577093cbf8f4c94109c354ce9d4a8f4e1a77c40df98d08323`  
		Last Modified: Tue, 09 Sep 2025 21:43:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a98b784cf4f30652bb9977f4b8182b43e8facd172a4941225c99ab5995dba9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8328b4789d4fbe7d5b301f3bd5035ae9db9ad28510f44990ee8566e1e7e1dbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddc73c38f5ff5cf3bb96c33e0ce7c05fbc401d129d48c24368267d9cc5605bc`

```dockerfile
```

-	Layers:
	-	`sha256:2db5fa19161bff44ba2f7e98f558c2306b54b8593a3acd92b4c51812baaadf96`  
		Last Modified: Tue, 09 Sep 2025 23:56:42 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:da2887adbe5a9b5ce19ba1daf5f5323382993e2999e1a5450dea6d5d615af554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9732548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa53562ec436568c3bf00db1fb91bc89ebfddf47fe2f946af086551b7d0240d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031341d8662c24b611d19217b15697c7e1eeb7fb20ae015769304f3d9e416f4`  
		Last Modified: Tue, 09 Sep 2025 21:59:39 GMT  
		Size: 6.5 MB (6512539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4721d57828fe2cba2dda46e5e717ad9ee4278ab187e170e498625e6116e7d5f`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc30ccba0a3c016998f1b5b2e2cdccd8d8f698e228a65dd364b2adb41b185f3`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:af1dd4d927ea33740d8992643ce68d26a2d5ff2e68fa53849efbaec72158a770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e92010b8b482e98d125d98981583e131f2df9dbd380f6b38cbcd1b45eb9b95`

```dockerfile
```

-	Layers:
	-	`sha256:785b567e7e5ebabe0f6b6d6e32479ec15565ad1886ce491f7b90e7af1eae9c54`  
		Last Modified: Tue, 09 Sep 2025 23:56:45 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b78f1e58f75bba9a7393b5f2bfe919ed0516e154ceb1260cdc013093e0d08daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e807b412fc1138feba48d67aa5c005eea691e786927abca0174930a194059dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81efb27a24236aa9d4dd850761611e76ba6addbab29a3200f3394ddb61e8b457`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.3 MB (6299385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82430e347407921b5c2f85841823aac9ee8ad9e3e96a91c355b0195f303337e`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a300c8b17b92657dc962e711a386e4a85537831d47c4dd21abdf78281c75ffe2`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:17e3e88060ad541c6b4c32996093543b4dff70e3ed4858411180475c8fdb726a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52155310f554543e3eba1ff4e53c6d064d0c1554b36243f55cc7b47991d1bffb`

```dockerfile
```

-	Layers:
	-	`sha256:71290e70b093feda2cec83ba57599465c9c85d6a25207135ffe14156b636e16a`  
		Last Modified: Tue, 09 Sep 2025 23:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:54e05d0d4583d88acae58396444e5a856104ea167b8be5441bc559181cc5a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10005035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f0fa028221d6d5d34463a7ae1561e9c4b6429343c173387bb4b6ca560be435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdf74981cd55b1384057c7128506e55ba5cb405d3805d01d372d78639b6f68f`  
		Last Modified: Tue, 09 Sep 2025 22:41:34 GMT  
		Size: 6.3 MB (6276953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20c0fbc0352f22902cf45129dfed4ad8d39bdfb4ddc662750875e826f0fa048`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9a8a923704ae9582e7e000943845e579ce24fe430b260de5e0b6511b8ada0`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:edc001c19fc6f746a25c2ad86c35a9ae36ea65996d0bb0c4fb079541607a2b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea334b98e4c0c7cdf7544a7944458efbd59d206ffb201dbc9bfde0fcd1eb081`

```dockerfile
```

-	Layers:
	-	`sha256:fb1473e3d857e75ce42f899fae73871d5325888dd66b94dccebb3a786e13a6f1`  
		Last Modified: Tue, 09 Sep 2025 23:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:c092626e962687b5c5819475844a8aabd59265be101a1c6876a1ac9c4293e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8d1105a8bbefc2fc8ded940d6b0bfb291fedfa8496dbe6671ea9f1675a0b3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee21526533161753c86a71f59d0df970aa35c45d24fdef163007b752fe70e3`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 6.6 MB (6646165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b3c4b7b79090468183fcf1696975567f84eb65fb97befa05d25ce48efccee`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e44737618f643a95798867bcd27e21c0ea885cede55a7fb81f96a9c7c7e19c`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c0ce755324c31309757a9e71aec2d4164dd8e5eb70127b5ff8d402fe15807f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ffb49aae826cb2119b2c3420d4f3b9c2cd24d4f20626d536cf9b4606d1dc9`

```dockerfile
```

-	Layers:
	-	`sha256:5badeeb273e199fa585a1f83872b8d1f5ba9c8987464a21caec5530d62973b86`  
		Last Modified: Tue, 09 Sep 2025 23:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.9-linux`

```console
$ docker pull nats@sha256:ee3312f4e9d4b67ff197b0ed1e98756596f0d7db872e7fe30d9bf64fccddf92c
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

### `nats:2.11.9-linux` - linux; amd64

```console
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-linux` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.9-nanoserver`

```console
$ docker pull nats@sha256:950519f31ba604e5d89f5b7abb1aa2dfa10b04b00e7559e52cdaa0c5f077b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11.9-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.9-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:950519f31ba604e5d89f5b7abb1aa2dfa10b04b00e7559e52cdaa0c5f077b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11.9-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.9-scratch`

```console
$ docker pull nats@sha256:ee3312f4e9d4b67ff197b0ed1e98756596f0d7db872e7fe30d9bf64fccddf92c
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

### `nats:2.11.9-scratch` - linux; amd64

```console
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.9-scratch` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.9-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.9-windowsservercore`

```console
$ docker pull nats@sha256:bb0d35aa5eed764e627f92b57cb5eceaaf6707b0ae52ddf0c31716c54870bb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11.9-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:6adfca3411b50bb2d743507583ac87476d7965b2cbed6518a20d4931d3491f45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288928787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98c80bef79058b0466c1d9f41b8d4ca392f9ba73250a750c7ea21bab930aa97`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 21:27:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Sep 2025 21:27:29 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 21:27:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 21:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.9/nats-server-v2.11.9-windows-amd64.zip
# Tue, 09 Sep 2025 21:27:33 GMT
ENV NATS_SERVER_SHASUM=841a953d9be1d55b5f2b990c624b239f7f938baaf00d5627ac34d6c363a2fda3
# Tue, 09 Sep 2025 21:27:53 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Sep 2025 21:28:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Sep 2025 21:28:15 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 21:28:16 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 21:28:18 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 21:28:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873d00bcaff9497f2d332fa6897defb80cc97bf202af48ef6c713377e8d9df48`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b198342f09ddc645f6fc2b65a830146f5d0d7b0fe1eb41f306dde5eef7f46b`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990e7ded3458108fd3c5e4e46d956fb4821b25c1be30560397a4c05e6bbffc3c`  
		Last Modified: Tue, 09 Sep 2025 21:28:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8258a2f8d54eef32d8c8da5489e1222917b41d56e62e97b7889cad5929dac7`  
		Last Modified: Tue, 09 Sep 2025 21:28:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2939a4cd8a8edb8a73065013d6ff136be09a5c80fb388692a0eb284bb9516d91`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c8f62dd915a272e9ebf61afe2ec754bfb7592db3760a577412e1456b4a1a3d`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 343.2 KB (343172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8604f83c30deda1e29d968f6384c4e584eeb306c7df98b9a754743e760128785`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.9 MB (6881510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a7e192f98db48a22a47dd45e84dace5542d6245b2f0acfb82d28be2485dd13`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f754f15699c71eb0c940dac7c0ff3f6e668ea993a2b45320344a34f5b9006f77`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc414a41a0ef3729968b13a6c80750a0f8afb723bebab36a4fd4e0d76ae4cc4`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3955ff1a4e10e862f6c1364516e5e72757e2ec571b70019de550d19b435131c`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.9-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:bb0d35aa5eed764e627f92b57cb5eceaaf6707b0ae52ddf0c31716c54870bb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11.9-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:6adfca3411b50bb2d743507583ac87476d7965b2cbed6518a20d4931d3491f45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288928787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98c80bef79058b0466c1d9f41b8d4ca392f9ba73250a750c7ea21bab930aa97`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 21:27:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Sep 2025 21:27:29 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 21:27:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 21:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.9/nats-server-v2.11.9-windows-amd64.zip
# Tue, 09 Sep 2025 21:27:33 GMT
ENV NATS_SERVER_SHASUM=841a953d9be1d55b5f2b990c624b239f7f938baaf00d5627ac34d6c363a2fda3
# Tue, 09 Sep 2025 21:27:53 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Sep 2025 21:28:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Sep 2025 21:28:15 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 21:28:16 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 21:28:18 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 21:28:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873d00bcaff9497f2d332fa6897defb80cc97bf202af48ef6c713377e8d9df48`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b198342f09ddc645f6fc2b65a830146f5d0d7b0fe1eb41f306dde5eef7f46b`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990e7ded3458108fd3c5e4e46d956fb4821b25c1be30560397a4c05e6bbffc3c`  
		Last Modified: Tue, 09 Sep 2025 21:28:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8258a2f8d54eef32d8c8da5489e1222917b41d56e62e97b7889cad5929dac7`  
		Last Modified: Tue, 09 Sep 2025 21:28:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2939a4cd8a8edb8a73065013d6ff136be09a5c80fb388692a0eb284bb9516d91`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c8f62dd915a272e9ebf61afe2ec754bfb7592db3760a577412e1456b4a1a3d`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 343.2 KB (343172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8604f83c30deda1e29d968f6384c4e584eeb306c7df98b9a754743e760128785`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.9 MB (6881510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a7e192f98db48a22a47dd45e84dace5542d6245b2f0acfb82d28be2485dd13`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f754f15699c71eb0c940dac7c0ff3f6e668ea993a2b45320344a34f5b9006f77`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc414a41a0ef3729968b13a6c80750a0f8afb723bebab36a4fd4e0d76ae4cc4`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3955ff1a4e10e862f6c1364516e5e72757e2ec571b70019de550d19b435131c`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:777787bbb4c7c4083ec2213b0b8b14151617610a3e0d85776bd995cd46599c73
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
$ docker pull nats@sha256:383e95bac92d099fa612f6bbe5c4c83ae15af22e409a89fecd2e3c5092a8b2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e317eb6ac10bc33a158896aec219c58122b17191d82ad8059edfdd348687beca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab2a6f9512b153493f557d6c5cfaaa4a7c3cb1211f22480cb0d5c50d3a4b17`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 6.8 MB (6811571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee5018631bdb543650e4026cef806de7225147757a9e052ab075bc9ce41192`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4d4963114e48d99ec239e86fdee1a87c26a0e2d581a26bc7a82c659486b221`  
		Last Modified: Tue, 09 Sep 2025 21:28:03 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ba0a85e05e92baa4dc25c2d468c7055ed378ed85e8cef076e528de3db68d5d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d338ea42bfc75ac6382f89e464fb4f8968277e57e510d15d0516ec454dc2a8ee`

```dockerfile
```

-	Layers:
	-	`sha256:afdda197879734c0f39320dd4b5d9022177afc5ed488a2ec3bc5100477686c47`  
		Last Modified: Tue, 09 Sep 2025 23:56:39 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e40ee2e909ecb5d5497f954e4bae9fe52ff74799dc1916a38a9501d3a601236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10023996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a9c25c10fb7e66ad634861abcd1f91711d6ad5aeb2f3c7107b22f6ada83fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2acf2abeee38084f132adc7fc2df4157782dac0272a686992cf569149b35f9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 6.5 MB (6522116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590716c3787e83b577093cbf8f4c94109c354ce9d4a8f4e1a77c40df98d08323`  
		Last Modified: Tue, 09 Sep 2025 21:43:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a98b784cf4f30652bb9977f4b8182b43e8facd172a4941225c99ab5995dba9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8328b4789d4fbe7d5b301f3bd5035ae9db9ad28510f44990ee8566e1e7e1dbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddc73c38f5ff5cf3bb96c33e0ce7c05fbc401d129d48c24368267d9cc5605bc`

```dockerfile
```

-	Layers:
	-	`sha256:2db5fa19161bff44ba2f7e98f558c2306b54b8593a3acd92b4c51812baaadf96`  
		Last Modified: Tue, 09 Sep 2025 23:56:42 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:da2887adbe5a9b5ce19ba1daf5f5323382993e2999e1a5450dea6d5d615af554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9732548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa53562ec436568c3bf00db1fb91bc89ebfddf47fe2f946af086551b7d0240d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031341d8662c24b611d19217b15697c7e1eeb7fb20ae015769304f3d9e416f4`  
		Last Modified: Tue, 09 Sep 2025 21:59:39 GMT  
		Size: 6.5 MB (6512539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4721d57828fe2cba2dda46e5e717ad9ee4278ab187e170e498625e6116e7d5f`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc30ccba0a3c016998f1b5b2e2cdccd8d8f698e228a65dd364b2adb41b185f3`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:af1dd4d927ea33740d8992643ce68d26a2d5ff2e68fa53849efbaec72158a770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e92010b8b482e98d125d98981583e131f2df9dbd380f6b38cbcd1b45eb9b95`

```dockerfile
```

-	Layers:
	-	`sha256:785b567e7e5ebabe0f6b6d6e32479ec15565ad1886ce491f7b90e7af1eae9c54`  
		Last Modified: Tue, 09 Sep 2025 23:56:45 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b78f1e58f75bba9a7393b5f2bfe919ed0516e154ceb1260cdc013093e0d08daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e807b412fc1138feba48d67aa5c005eea691e786927abca0174930a194059dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81efb27a24236aa9d4dd850761611e76ba6addbab29a3200f3394ddb61e8b457`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.3 MB (6299385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82430e347407921b5c2f85841823aac9ee8ad9e3e96a91c355b0195f303337e`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a300c8b17b92657dc962e711a386e4a85537831d47c4dd21abdf78281c75ffe2`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:17e3e88060ad541c6b4c32996093543b4dff70e3ed4858411180475c8fdb726a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52155310f554543e3eba1ff4e53c6d064d0c1554b36243f55cc7b47991d1bffb`

```dockerfile
```

-	Layers:
	-	`sha256:71290e70b093feda2cec83ba57599465c9c85d6a25207135ffe14156b636e16a`  
		Last Modified: Tue, 09 Sep 2025 23:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:54e05d0d4583d88acae58396444e5a856104ea167b8be5441bc559181cc5a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10005035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f0fa028221d6d5d34463a7ae1561e9c4b6429343c173387bb4b6ca560be435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdf74981cd55b1384057c7128506e55ba5cb405d3805d01d372d78639b6f68f`  
		Last Modified: Tue, 09 Sep 2025 22:41:34 GMT  
		Size: 6.3 MB (6276953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20c0fbc0352f22902cf45129dfed4ad8d39bdfb4ddc662750875e826f0fa048`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9a8a923704ae9582e7e000943845e579ce24fe430b260de5e0b6511b8ada0`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:edc001c19fc6f746a25c2ad86c35a9ae36ea65996d0bb0c4fb079541607a2b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea334b98e4c0c7cdf7544a7944458efbd59d206ffb201dbc9bfde0fcd1eb081`

```dockerfile
```

-	Layers:
	-	`sha256:fb1473e3d857e75ce42f899fae73871d5325888dd66b94dccebb3a786e13a6f1`  
		Last Modified: Tue, 09 Sep 2025 23:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:c092626e962687b5c5819475844a8aabd59265be101a1c6876a1ac9c4293e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8d1105a8bbefc2fc8ded940d6b0bfb291fedfa8496dbe6671ea9f1675a0b3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee21526533161753c86a71f59d0df970aa35c45d24fdef163007b752fe70e3`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 6.6 MB (6646165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b3c4b7b79090468183fcf1696975567f84eb65fb97befa05d25ce48efccee`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e44737618f643a95798867bcd27e21c0ea885cede55a7fb81f96a9c7c7e19c`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c0ce755324c31309757a9e71aec2d4164dd8e5eb70127b5ff8d402fe15807f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ffb49aae826cb2119b2c3420d4f3b9c2cd24d4f20626d536cf9b4606d1dc9`

```dockerfile
```

-	Layers:
	-	`sha256:5badeeb273e199fa585a1f83872b8d1f5ba9c8987464a21caec5530d62973b86`  
		Last Modified: Tue, 09 Sep 2025 23:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:777787bbb4c7c4083ec2213b0b8b14151617610a3e0d85776bd995cd46599c73
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
$ docker pull nats@sha256:383e95bac92d099fa612f6bbe5c4c83ae15af22e409a89fecd2e3c5092a8b2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10612234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e317eb6ac10bc33a158896aec219c58122b17191d82ad8059edfdd348687beca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab2a6f9512b153493f557d6c5cfaaa4a7c3cb1211f22480cb0d5c50d3a4b17`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 6.8 MB (6811571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ee5018631bdb543650e4026cef806de7225147757a9e052ab075bc9ce41192`  
		Last Modified: Tue, 09 Sep 2025 21:28:04 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4d4963114e48d99ec239e86fdee1a87c26a0e2d581a26bc7a82c659486b221`  
		Last Modified: Tue, 09 Sep 2025 21:28:03 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ba0a85e05e92baa4dc25c2d468c7055ed378ed85e8cef076e528de3db68d5d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d338ea42bfc75ac6382f89e464fb4f8968277e57e510d15d0516ec454dc2a8ee`

```dockerfile
```

-	Layers:
	-	`sha256:afdda197879734c0f39320dd4b5d9022177afc5ed488a2ec3bc5100477686c47`  
		Last Modified: Tue, 09 Sep 2025 23:56:39 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e40ee2e909ecb5d5497f954e4bae9fe52ff74799dc1916a38a9501d3a601236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10023996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13a9c25c10fb7e66ad634861abcd1f91711d6ad5aeb2f3c7107b22f6ada83fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2acf2abeee38084f132adc7fc2df4157782dac0272a686992cf569149b35f9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 6.5 MB (6522116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590716c3787e83b577093cbf8f4c94109c354ce9d4a8f4e1a77c40df98d08323`  
		Last Modified: Tue, 09 Sep 2025 21:43:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a98b784cf4f30652bb9977f4b8182b43e8facd172a4941225c99ab5995dba9`  
		Last Modified: Tue, 09 Sep 2025 21:43:58 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8328b4789d4fbe7d5b301f3bd5035ae9db9ad28510f44990ee8566e1e7e1dbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddc73c38f5ff5cf3bb96c33e0ce7c05fbc401d129d48c24368267d9cc5605bc`

```dockerfile
```

-	Layers:
	-	`sha256:2db5fa19161bff44ba2f7e98f558c2306b54b8593a3acd92b4c51812baaadf96`  
		Last Modified: Tue, 09 Sep 2025 23:56:42 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:da2887adbe5a9b5ce19ba1daf5f5323382993e2999e1a5450dea6d5d615af554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9732548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa53562ec436568c3bf00db1fb91bc89ebfddf47fe2f946af086551b7d0240d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031341d8662c24b611d19217b15697c7e1eeb7fb20ae015769304f3d9e416f4`  
		Last Modified: Tue, 09 Sep 2025 21:59:39 GMT  
		Size: 6.5 MB (6512539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4721d57828fe2cba2dda46e5e717ad9ee4278ab187e170e498625e6116e7d5f`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc30ccba0a3c016998f1b5b2e2cdccd8d8f698e228a65dd364b2adb41b185f3`  
		Last Modified: Tue, 09 Sep 2025 21:59:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:af1dd4d927ea33740d8992643ce68d26a2d5ff2e68fa53849efbaec72158a770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e92010b8b482e98d125d98981583e131f2df9dbd380f6b38cbcd1b45eb9b95`

```dockerfile
```

-	Layers:
	-	`sha256:785b567e7e5ebabe0f6b6d6e32479ec15565ad1886ce491f7b90e7af1eae9c54`  
		Last Modified: Tue, 09 Sep 2025 23:56:45 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b78f1e58f75bba9a7393b5f2bfe919ed0516e154ceb1260cdc013093e0d08daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10431106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e807b412fc1138feba48d67aa5c005eea691e786927abca0174930a194059dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81efb27a24236aa9d4dd850761611e76ba6addbab29a3200f3394ddb61e8b457`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.3 MB (6299385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82430e347407921b5c2f85841823aac9ee8ad9e3e96a91c355b0195f303337e`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a300c8b17b92657dc962e711a386e4a85537831d47c4dd21abdf78281c75ffe2`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:17e3e88060ad541c6b4c32996093543b4dff70e3ed4858411180475c8fdb726a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52155310f554543e3eba1ff4e53c6d064d0c1554b36243f55cc7b47991d1bffb`

```dockerfile
```

-	Layers:
	-	`sha256:71290e70b093feda2cec83ba57599465c9c85d6a25207135ffe14156b636e16a`  
		Last Modified: Tue, 09 Sep 2025 23:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:54e05d0d4583d88acae58396444e5a856104ea167b8be5441bc559181cc5a5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10005035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f0fa028221d6d5d34463a7ae1561e9c4b6429343c173387bb4b6ca560be435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdf74981cd55b1384057c7128506e55ba5cb405d3805d01d372d78639b6f68f`  
		Last Modified: Tue, 09 Sep 2025 22:41:34 GMT  
		Size: 6.3 MB (6276953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20c0fbc0352f22902cf45129dfed4ad8d39bdfb4ddc662750875e826f0fa048`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9a8a923704ae9582e7e000943845e579ce24fe430b260de5e0b6511b8ada0`  
		Last Modified: Tue, 09 Sep 2025 22:41:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:edc001c19fc6f746a25c2ad86c35a9ae36ea65996d0bb0c4fb079541607a2b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea334b98e4c0c7cdf7544a7944458efbd59d206ffb201dbc9bfde0fcd1eb081`

```dockerfile
```

-	Layers:
	-	`sha256:fb1473e3d857e75ce42f899fae73871d5325888dd66b94dccebb3a786e13a6f1`  
		Last Modified: Tue, 09 Sep 2025 23:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:c092626e962687b5c5819475844a8aabd59265be101a1c6876a1ac9c4293e4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8d1105a8bbefc2fc8ded940d6b0bfb291fedfa8496dbe6671ea9f1675a0b3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 15:29:30 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='47d7e652eb761d771bc42df04924aae0acf4e026d30ea98faa9bab216cc2e742' ;;     armhf) natsArch='arm6'; sha256='70775a662c5a9f5935845b1efb08911089f796d096ad2b2d42b765cf4c3d77bd' ;;     armv7) natsArch='arm7'; sha256='991ed42c5d4d40ff44658fc88450b7467c99eb392ccee14e53f3d8eddeb44245' ;;     x86_64) natsArch='amd64'; sha256='3eef83faa048d3879937a6871f59ae5d9c3bbf5900905b7a9ff996a894d755ab' ;;     x86) natsArch='386'; sha256='035fd051433d2e0282320ba5da4ef09bec0b6e8c5ea95bced4ca1e72b4a1918a' ;;     s390x) natsArch='s390x'; sha256='1e94dc439696af6ad49e68049d2945b5521732db7ad943aa3d4442deb8f4496a' ;;     ppc64le) natsArch='ppc64le'; sha256='a48a7f3ea2dd7336439672c3198d24beae42bcfa6291140b40ca44aeef9eeaf9' ;;     loong64) natsArch='loong64'; sha256='1f8de18cce53631d1b73fe4ad7d332e1741523ae725a0d913983c81c9798d2e6' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee21526533161753c86a71f59d0df970aa35c45d24fdef163007b752fe70e3`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 6.6 MB (6646165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15b3c4b7b79090468183fcf1696975567f84eb65fb97befa05d25ce48efccee`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e44737618f643a95798867bcd27e21c0ea885cede55a7fb81f96a9c7c7e19c`  
		Last Modified: Tue, 09 Sep 2025 23:34:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c0ce755324c31309757a9e71aec2d4164dd8e5eb70127b5ff8d402fe15807f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42ffb49aae826cb2119b2c3420d4f3b9c2cd24d4f20626d536cf9b4606d1dc9`

```dockerfile
```

-	Layers:
	-	`sha256:5badeeb273e199fa585a1f83872b8d1f5ba9c8987464a21caec5530d62973b86`  
		Last Modified: Tue, 09 Sep 2025 23:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:a8fe3a4066d3c14d893dd92a6d85f117cfb3567d4d0df11bc3161782b34dc351
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
	-	windows version 10.0.20348.4052; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:ee3312f4e9d4b67ff197b0ed1e98756596f0d7db872e7fe30d9bf64fccddf92c
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
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:950519f31ba604e5d89f5b7abb1aa2dfa10b04b00e7559e52cdaa0c5f077b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:950519f31ba604e5d89f5b7abb1aa2dfa10b04b00e7559e52cdaa0c5f077b564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cb08882db4f97531b99bb40e1ad43592e424ab9662ecea55270c3ffecf633dcb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129203884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61086a00f9a7a92dfa03e67a1cbbf4008ae7ccc07a75624420edbb3619dd750d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 22:08:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 22:08:09 GMT
RUN cmd /S /C #(nop) COPY file:1b1fcd7178cea6fb7bddd5819f166b3d91e649d03fb0e35c6dbd25342d3cce79 in C:\nats-server.exe 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 22:08:11 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 22:08:12 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 22:08:13 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7cd3ced6244771a57adebff75df542330263be15717b8587eba0706f05d7ae`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea961252df9f370c252dbfadee42af63576ed2d527908ff835809cc7d4ebcd9`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 6.5 MB (6537756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd26970cfc15effd40419fb02a46ab6251ac71d1f57a87ac50cb97785d8e005`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23ad27018f963f0407bf1089ea2832e29f710b3b9678f87dab2d2d8fa5c6a05`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6a8b7a39d3531b55385b3be93ea1870b677b2f6ecc487a9aae86add343b599`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9fa7fe845651dc2aab94e869ad57b16a5ba27fd764eec87d90ab31376785eb`  
		Last Modified: Tue, 09 Sep 2025 22:08:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:ee3312f4e9d4b67ff197b0ed1e98756596f0d7db872e7fe30d9bf64fccddf92c
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
$ docker pull nats@sha256:0366581599528ac497ee0495b85e912578564d47f4d00026c5bb46c155d3e9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7a832dff1ddf9d7f164c5bcdfb99a174a196e2cc089cbd53cef0f6c506acdd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f1e5e99e9e8e314054239bd52d522a319466a9f7fcf972882b9818712e711c80`  
		Last Modified: Tue, 09 Sep 2025 15:32:16 GMT  
		Size: 6.4 MB (6360826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0db0261279bad5dfe553062862dcf60b5e8df2ace4b10e4c593cfadf39869`  
		Last Modified: Tue, 09 Sep 2025 22:08:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4497347445f7ccdefb45098959d69760b32679a1f2581284b3b9823e0785708a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a27366aa1f5a38775ec5d381496143b4ca2fe9fd846ab69d84bdca5b13e0b`

```dockerfile
```

-	Layers:
	-	`sha256:02bc7ec45ccee88b20cb26fc0833f8670ce32e9f9c7a30dde2c7e535470c8ada`  
		Last Modified: Tue, 09 Sep 2025 23:56:23 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:df59895e6f317d92058c3f53b1a9544b96fd80579ec950b7e4d67f9c9b539690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f123bdee14496687de6ec3eee3447c6381fb3717dacaea05474bcadc2019fa48`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2b6f7cc8134ea0773d9caff5bf8e8875997f13c8890f8858a07fb618d4226024`  
		Last Modified: Wed, 10 Sep 2025 03:04:11 GMT  
		Size: 6.1 MB (6073981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47342606c525913bb81290e7197a7595dc146afc44e19cada08858b97216a5`  
		Last Modified: Wed, 10 Sep 2025 03:04:04 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:54e77c5788599e7eca88e13e6508731e74173b3ad37aafd0a6d0de641b4406cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e8cdfeea16ef858ef72dfa7ce6045c67bd558c9582f9f8ae22495bed5fe874`

```dockerfile
```

-	Layers:
	-	`sha256:1c69d82154a696989581e38dd2bdfeb417abc08245f0697898c4a790ef82be6b`  
		Last Modified: Wed, 10 Sep 2025 05:56:22 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a518a104ae2b1aad0647dd838be7967a9fe0a3009480644f3bdfc14b2e429e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645f3612cba5f4aac9aedee3e8d59dec572a714a915d6c24960ff00c40cbeebd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8c5268ea0d0b83bfc9157796de81bd3fab9dce3a7b038b6beaf1911cc37a60cb`  
		Last Modified: Wed, 10 Sep 2025 03:04:41 GMT  
		Size: 6.1 MB (6063945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6433b4eb34ec7229032973eb2ef093451a00bc9227dee8d939c6a96a0f1b35`  
		Last Modified: Wed, 10 Sep 2025 03:04:33 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f9bd1ebe6d8849975174dc9ce0c43e7c9297cc648ba8d41d21b859e5ae0afb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788549f1effaeaae27143b3960d07f2aeeeb70d82b5b1f59bdc61f31e4dee93f`

```dockerfile
```

-	Layers:
	-	`sha256:f6e74ad52574f198559a65cf1b2fbbacfc0d6f10bf2b72eee72aacecaa090175`  
		Last Modified: Wed, 10 Sep 2025 05:56:24 GMT  
		Size: 10.6 KB (10597 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7781e7c23d25ee4d13bf87dbd07619596faa25f465b3d526237c4e683457e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e69ca2ac8851f45d9ba52346473cfd8424ec21aef83f48d05be81f999a0b06`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cbde7a53b4e0a59cd5430565c0294229084bce14d9b5024c316fced138b10546`  
		Last Modified: Tue, 09 Sep 2025 16:18:18 GMT  
		Size: 5.8 MB (5848338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedfa50f58252aeabd0f5034bd79cc5b82d9661cf625ebccb95f9f5e62c3fc33`  
		Last Modified: Tue, 09 Sep 2025 22:09:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e1cb1d77737cabfc6940ec9b6736786f03b9512ba1ffd98625711f49feab89e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73246af39702079d557176a46db0601015f8a0969434d96c3d90f12cf81dfd1d`

```dockerfile
```

-	Layers:
	-	`sha256:f29e37449541a809b445fe1393a998d8b691e0288279c99ad212f42cd108d8de`  
		Last Modified: Tue, 09 Sep 2025 23:56:30 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:be85ebfcfba590d7c624f4e861900117267e9ab4d5f5480cc6c713f90ff0bdb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e885894bb8802249f36a29f2558e86b843185694675d7a112a43c95566bffdf`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4c1e7f0c6032756bcce246dfd791b1ade5e61f9b697caa1c3ab3c558d9a884e8`  
		Last Modified: Wed, 10 Sep 2025 08:56:13 GMT  
		Size: 5.8 MB (5826566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72233a125708fdfecfbb0adfc24da0d712d38fa6d1354babf7e5bca67b6396be`  
		Last Modified: Wed, 10 Sep 2025 11:55:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:35df3851843024cd8f6036946ccc42ab2abfcbe1f492070c74d231f81ccda571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e7d4c020cdb7d868d21bd26881a0f1ef167a535ef473cf2f3743a6c06cc6e1`

```dockerfile
```

-	Layers:
	-	`sha256:75e02092ff017b1458b54f1ae1cb1bc752a5b2093ca83dfebb3e6b0c0896313e`  
		Last Modified: Wed, 10 Sep 2025 14:56:25 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:98ab2d71a429177db97a9d5d21a237338d1db9dfe83790d4956d34ad1a270587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cdf0e571cb9adb8c61493ab9f778b8ce9e9573709427e85a3dd7a2d988a972`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Sep 2025 15:29:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Sep 2025 15:29:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Sep 2025 15:29:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Sep 2025 15:29:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Sep 2025 15:29:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:33d4b78a45d256556f78665974744159b23f603ddfaa92c5cd874b4206ea9f67`  
		Last Modified: Wed, 10 Sep 2025 09:03:20 GMT  
		Size: 6.2 MB (6195492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913cd8ec5da2c71d2db0113e3c442ec35ccc80764a3148e938087400c787e33`  
		Last Modified: Wed, 10 Sep 2025 09:27:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ddcee029df0dd3112a0d83e79de8f1ac9ded95665165b9c9d3c88aaf891b653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa10e2de6cc16fde4ddbb1022eb94a44c06f84c0d44042adbe03cd3fbdeda85`

```dockerfile
```

-	Layers:
	-	`sha256:14177593028ae4bbb71f1b5c45b4d2c8a21583a230c79d05c154714e458ec563`  
		Last Modified: Wed, 10 Sep 2025 11:56:27 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:bb0d35aa5eed764e627f92b57cb5eceaaf6707b0ae52ddf0c31716c54870bb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:6adfca3411b50bb2d743507583ac87476d7965b2cbed6518a20d4931d3491f45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288928787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98c80bef79058b0466c1d9f41b8d4ca392f9ba73250a750c7ea21bab930aa97`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 21:27:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Sep 2025 21:27:29 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 21:27:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 21:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.9/nats-server-v2.11.9-windows-amd64.zip
# Tue, 09 Sep 2025 21:27:33 GMT
ENV NATS_SERVER_SHASUM=841a953d9be1d55b5f2b990c624b239f7f938baaf00d5627ac34d6c363a2fda3
# Tue, 09 Sep 2025 21:27:53 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Sep 2025 21:28:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Sep 2025 21:28:15 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 21:28:16 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 21:28:18 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 21:28:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873d00bcaff9497f2d332fa6897defb80cc97bf202af48ef6c713377e8d9df48`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b198342f09ddc645f6fc2b65a830146f5d0d7b0fe1eb41f306dde5eef7f46b`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990e7ded3458108fd3c5e4e46d956fb4821b25c1be30560397a4c05e6bbffc3c`  
		Last Modified: Tue, 09 Sep 2025 21:28:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8258a2f8d54eef32d8c8da5489e1222917b41d56e62e97b7889cad5929dac7`  
		Last Modified: Tue, 09 Sep 2025 21:28:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2939a4cd8a8edb8a73065013d6ff136be09a5c80fb388692a0eb284bb9516d91`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c8f62dd915a272e9ebf61afe2ec754bfb7592db3760a577412e1456b4a1a3d`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 343.2 KB (343172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8604f83c30deda1e29d968f6384c4e584eeb306c7df98b9a754743e760128785`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.9 MB (6881510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a7e192f98db48a22a47dd45e84dace5542d6245b2f0acfb82d28be2485dd13`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f754f15699c71eb0c940dac7c0ff3f6e668ea993a2b45320344a34f5b9006f77`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc414a41a0ef3729968b13a6c80750a0f8afb723bebab36a4fd4e0d76ae4cc4`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3955ff1a4e10e862f6c1364516e5e72757e2ec571b70019de550d19b435131c`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:bb0d35aa5eed764e627f92b57cb5eceaaf6707b0ae52ddf0c31716c54870bb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:6adfca3411b50bb2d743507583ac87476d7965b2cbed6518a20d4931d3491f45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288928787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98c80bef79058b0466c1d9f41b8d4ca392f9ba73250a750c7ea21bab930aa97`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 21:27:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Sep 2025 21:27:29 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Sep 2025 21:27:30 GMT
ENV NATS_SERVER=2.11.9
# Tue, 09 Sep 2025 21:27:32 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.9/nats-server-v2.11.9-windows-amd64.zip
# Tue, 09 Sep 2025 21:27:33 GMT
ENV NATS_SERVER_SHASUM=841a953d9be1d55b5f2b990c624b239f7f938baaf00d5627ac34d6c363a2fda3
# Tue, 09 Sep 2025 21:27:53 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Sep 2025 21:28:14 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Sep 2025 21:28:15 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 09 Sep 2025 21:28:16 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Sep 2025 21:28:18 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Sep 2025 21:28:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873d00bcaff9497f2d332fa6897defb80cc97bf202af48ef6c713377e8d9df48`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b198342f09ddc645f6fc2b65a830146f5d0d7b0fe1eb41f306dde5eef7f46b`  
		Last Modified: Tue, 09 Sep 2025 21:28:49 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990e7ded3458108fd3c5e4e46d956fb4821b25c1be30560397a4c05e6bbffc3c`  
		Last Modified: Tue, 09 Sep 2025 21:28:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8258a2f8d54eef32d8c8da5489e1222917b41d56e62e97b7889cad5929dac7`  
		Last Modified: Tue, 09 Sep 2025 21:28:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2939a4cd8a8edb8a73065013d6ff136be09a5c80fb388692a0eb284bb9516d91`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c8f62dd915a272e9ebf61afe2ec754bfb7592db3760a577412e1456b4a1a3d`  
		Last Modified: Tue, 09 Sep 2025 21:28:59 GMT  
		Size: 343.2 KB (343172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8604f83c30deda1e29d968f6384c4e584eeb306c7df98b9a754743e760128785`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 6.9 MB (6881510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a7e192f98db48a22a47dd45e84dace5542d6245b2f0acfb82d28be2485dd13`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f754f15699c71eb0c940dac7c0ff3f6e668ea993a2b45320344a34f5b9006f77`  
		Last Modified: Tue, 09 Sep 2025 21:29:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc414a41a0ef3729968b13a6c80750a0f8afb723bebab36a4fd4e0d76ae4cc4`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3955ff1a4e10e862f6c1364516e5e72757e2ec571b70019de550d19b435131c`  
		Last Modified: Tue, 09 Sep 2025 21:29:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
