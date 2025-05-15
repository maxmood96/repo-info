<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.21`](#nats2-alpine321)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.21`](#nats210-alpine321)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.29`](#nats21029)
-	[`nats:2.10.29-alpine`](#nats21029-alpine)
-	[`nats:2.10.29-alpine3.21`](#nats21029-alpine321)
-	[`nats:2.10.29-linux`](#nats21029-linux)
-	[`nats:2.10.29-nanoserver`](#nats21029-nanoserver)
-	[`nats:2.10.29-nanoserver-1809`](#nats21029-nanoserver-1809)
-	[`nats:2.10.29-scratch`](#nats21029-scratch)
-	[`nats:2.10.29-windowsservercore`](#nats21029-windowsservercore)
-	[`nats:2.10.29-windowsservercore-1809`](#nats21029-windowsservercore-1809)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.21`](#nats211-alpine321)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-1809`](#nats211-nanoserver-1809)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-1809`](#nats211-windowsservercore-1809)
-	[`nats:2.11.3`](#nats2113)
-	[`nats:2.11.3-alpine`](#nats2113-alpine)
-	[`nats:2.11.3-alpine3.21`](#nats2113-alpine321)
-	[`nats:2.11.3-linux`](#nats2113-linux)
-	[`nats:2.11.3-nanoserver`](#nats2113-nanoserver)
-	[`nats:2.11.3-nanoserver-1809`](#nats2113-nanoserver-1809)
-	[`nats:2.11.3-scratch`](#nats2113-scratch)
-	[`nats:2.11.3-windowsservercore`](#nats2113-windowsservercore)
-	[`nats:2.11.3-windowsservercore-1809`](#nats2113-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.21`](#natsalpine321)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:3072e8ea890fe66b5921f75c1385b5f49b59a7f46171d697517d186830131fa7
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
	-	windows version 10.0.17763.7314; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:a79a6ff6e42ef41ef964c52bef9fe6eed02fc91cf348801e3dddbbd57636077a
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
$ docker pull nats@sha256:f6be324fcee27f2a91178d74f77bb4ba3e5a9d2e72ba7d6871f45d14aadca40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c567f7e9cb3bfc4d455ff826598a76a99a73fa13ec7367efaacf1e12c0dd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5d0247fe0c99cf6c1ecf760cd78e32964d3ddb3759704f6684937b17e5142`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 6.8 MB (6765302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b37c9588055ed3b254ae4ba53ef4c63f34fcc2aeab92b8475fcbcacfcd80b55`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe44b0610308731d27dd1e577ba8612ea42d8995d7543ffc050198010b94663`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6606e7bd2585dbedc93618630113f5655e877c1bd5dfc496a02e725e4a2fe9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e72e1fa9e878b2aba34410a32cef5eabe2a785ebf18d74b2b308387268ae11`

```dockerfile
```

-	Layers:
	-	`sha256:a096f4f7ad0e75fb3bf34e4f9cc376cccfe906466ff7158c5adcace3fc78d8eb`  
		Last Modified: Thu, 01 May 2025 16:39:11 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:10c04125727c8e5799732cbf4bb257a0be62ef4178a8305430c81e20d8c2e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9167a50c86fbbf9faacc0ba649170615658a1bcb97ea922126d16bed0b6b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637af45acc37a7a2c3ca6ce929b4671046476166442a11fc80d8f0bf90ecd868`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 6.5 MB (6484260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b2aff493c7a4b631188bf1e08800a5b7c4ff8c7b0a35d871d1e064b7b229f`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d157ed7867da0b76320ba85d657071b09d9648c20c89a328178ea46464e1b7`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:10c402d37b4e7ac39b9a3ae564dabb8171b6ebf57f29b2086adf5bf5bfc70452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69355e40015e4b8bba82c7bc204868461a260267941f8bfd4d8136e4c6d14f1a`

```dockerfile
```

-	Layers:
	-	`sha256:ae16ff4d4e58738b65ec2f42e2b394b9ef1c4cd8b294509afffaf0d3585aa2b0`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3d1385ecd165eeddcd5b60fe068d6cdf140ddcdc687af8e7544197e451b89be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4228daa974404161b0811acf95429df4a1c07f409613b14a22891f9d0229b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1f7a3c7b77c14f08c57f994d653a1573a628813f51ad57c8ffa6704eb1e7c`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 6.5 MB (6471695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133786e3c707b99368ea0262c4da45fbb457ff538f3e4245164f71c9d04ebcb3`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a93d5da73eaad0dceef4a853a5fda3e77ff002488070801a2e0df946562874`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b1a5520c26787b7b5b7598e8c6d32e04b6442246f45f51702f8ab9602311695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1d0f6677c8e2f5972add8fb8d56a1a1949d15ca4c27d662d5c221b9bb3987b`

```dockerfile
```

-	Layers:
	-	`sha256:91912f94323f40a81b369bdf7b31adec099387298167e8ee48fdbd643c54bbd7`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:77790b065a14aa640a9906611f2593849afbc24e3dfe9ea845191d6d6b2b9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715cd7234f00f3838f631d95b5ade02f3f069b16c157eed1908f21f1e0539245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ead951cdd1051dce5e434c83e45a7f8035db209e137743eadba8e07891ffdf`  
		Last Modified: Thu, 08 May 2025 17:14:47 GMT  
		Size: 6.3 MB (6260210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a94e80a2eaf0a11748ce4e055b47b3131f7bf07fbf5822a6684d7baaca7fe`  
		Last Modified: Thu, 08 May 2025 17:14:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedeae9f370d7774766d58004d8794999e8ee0270a3ace165434935b755ba4e1`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7be154f67a95eb115edaf3da2c42409d3cc505c20e23282796088eb999a488ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153445c3a76a150eac532c5d5e8be9663decfd6cc7f0abd49cfe93e6864c896`

```dockerfile
```

-	Layers:
	-	`sha256:11e95946e2efd0801ccd7e4d3c070b684baf2d8e019eb4eeacd52b28cbfd858f`  
		Last Modified: Thu, 01 May 2025 16:38:44 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:aeffcf1a5fd10a494bc66c184585616f260d480c74d5e5253b56d450a809146d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc14e50d0acbca9b182a873a3c80f9967dbb1442be773cba6ab4e8cfe17688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829f47e2f6c4e37799e70fe955cbec9218f793ba67d3c42843028581f41d46c`  
		Last Modified: Thu, 01 May 2025 16:39:04 GMT  
		Size: 6.2 MB (6239898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26d5042fdff67ea8c94d44aa8763edc52e021387e6d064673d469c2bc47275`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da66dedca6ed504a33045c53e38cc74882153eb3a260560fe268bb9d1b6c8e4`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:352c383d3b82380dbd9a1ac107937d3991846006be06142ba8698aa65c990a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54eb654e9afb7bbd3bf867ba6dfcbf287ad262569f86c0815723a5376118ac8`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d2cc36c0ae1fb4725dfc44754cc365298d189308b25b6a818f9373c56d8b5`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:2f0d53def59230c037431fb279d69f0aca7b8603e3ddc47716d6a629b7837c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacf064fa25d7454a1aaa536a529a948d63741e3c9dd839168560f8b02c79d3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9647734b695bae36f7e0c32edbeebd3cf169b841161c9d4c577a1ece6018`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 6.6 MB (6603836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652b02d0c60b9d62fa04ca56202b067023a35da376bc9a712492b39a4338579`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5a6d01daa3a734095f6be97aa9b7b10a347d019c52cbf4dfffca96bb55f8d6`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:46d9178ace4d9f9b7e8307fdf38c831b0130174836ad584ec872a1d86af216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59c14622147cf68ab22ed7eb89e630f31c7d3213c566032a73cc0b9918fa51`

```dockerfile
```

-	Layers:
	-	`sha256:1046c910412b33c1747ecde0dd3656153062c8e55cde48158e5aa2a7f3053e86`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:a79a6ff6e42ef41ef964c52bef9fe6eed02fc91cf348801e3dddbbd57636077a
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

### `nats:2-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:f6be324fcee27f2a91178d74f77bb4ba3e5a9d2e72ba7d6871f45d14aadca40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c567f7e9cb3bfc4d455ff826598a76a99a73fa13ec7367efaacf1e12c0dd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5d0247fe0c99cf6c1ecf760cd78e32964d3ddb3759704f6684937b17e5142`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 6.8 MB (6765302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b37c9588055ed3b254ae4ba53ef4c63f34fcc2aeab92b8475fcbcacfcd80b55`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe44b0610308731d27dd1e577ba8612ea42d8995d7543ffc050198010b94663`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6606e7bd2585dbedc93618630113f5655e877c1bd5dfc496a02e725e4a2fe9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e72e1fa9e878b2aba34410a32cef5eabe2a785ebf18d74b2b308387268ae11`

```dockerfile
```

-	Layers:
	-	`sha256:a096f4f7ad0e75fb3bf34e4f9cc376cccfe906466ff7158c5adcace3fc78d8eb`  
		Last Modified: Thu, 01 May 2025 16:39:11 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:10c04125727c8e5799732cbf4bb257a0be62ef4178a8305430c81e20d8c2e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9167a50c86fbbf9faacc0ba649170615658a1bcb97ea922126d16bed0b6b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637af45acc37a7a2c3ca6ce929b4671046476166442a11fc80d8f0bf90ecd868`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 6.5 MB (6484260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b2aff493c7a4b631188bf1e08800a5b7c4ff8c7b0a35d871d1e064b7b229f`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d157ed7867da0b76320ba85d657071b09d9648c20c89a328178ea46464e1b7`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:10c402d37b4e7ac39b9a3ae564dabb8171b6ebf57f29b2086adf5bf5bfc70452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69355e40015e4b8bba82c7bc204868461a260267941f8bfd4d8136e4c6d14f1a`

```dockerfile
```

-	Layers:
	-	`sha256:ae16ff4d4e58738b65ec2f42e2b394b9ef1c4cd8b294509afffaf0d3585aa2b0`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:3d1385ecd165eeddcd5b60fe068d6cdf140ddcdc687af8e7544197e451b89be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4228daa974404161b0811acf95429df4a1c07f409613b14a22891f9d0229b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1f7a3c7b77c14f08c57f994d653a1573a628813f51ad57c8ffa6704eb1e7c`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 6.5 MB (6471695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133786e3c707b99368ea0262c4da45fbb457ff538f3e4245164f71c9d04ebcb3`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a93d5da73eaad0dceef4a853a5fda3e77ff002488070801a2e0df946562874`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b1a5520c26787b7b5b7598e8c6d32e04b6442246f45f51702f8ab9602311695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1d0f6677c8e2f5972add8fb8d56a1a1949d15ca4c27d662d5c221b9bb3987b`

```dockerfile
```

-	Layers:
	-	`sha256:91912f94323f40a81b369bdf7b31adec099387298167e8ee48fdbd643c54bbd7`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:77790b065a14aa640a9906611f2593849afbc24e3dfe9ea845191d6d6b2b9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715cd7234f00f3838f631d95b5ade02f3f069b16c157eed1908f21f1e0539245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ead951cdd1051dce5e434c83e45a7f8035db209e137743eadba8e07891ffdf`  
		Last Modified: Thu, 08 May 2025 17:14:47 GMT  
		Size: 6.3 MB (6260210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a94e80a2eaf0a11748ce4e055b47b3131f7bf07fbf5822a6684d7baaca7fe`  
		Last Modified: Thu, 08 May 2025 17:14:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedeae9f370d7774766d58004d8794999e8ee0270a3ace165434935b755ba4e1`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:7be154f67a95eb115edaf3da2c42409d3cc505c20e23282796088eb999a488ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153445c3a76a150eac532c5d5e8be9663decfd6cc7f0abd49cfe93e6864c896`

```dockerfile
```

-	Layers:
	-	`sha256:11e95946e2efd0801ccd7e4d3c070b684baf2d8e019eb4eeacd52b28cbfd858f`  
		Last Modified: Thu, 01 May 2025 16:38:44 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:aeffcf1a5fd10a494bc66c184585616f260d480c74d5e5253b56d450a809146d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc14e50d0acbca9b182a873a3c80f9967dbb1442be773cba6ab4e8cfe17688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829f47e2f6c4e37799e70fe955cbec9218f793ba67d3c42843028581f41d46c`  
		Last Modified: Thu, 01 May 2025 16:39:04 GMT  
		Size: 6.2 MB (6239898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26d5042fdff67ea8c94d44aa8763edc52e021387e6d064673d469c2bc47275`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da66dedca6ed504a33045c53e38cc74882153eb3a260560fe268bb9d1b6c8e4`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:352c383d3b82380dbd9a1ac107937d3991846006be06142ba8698aa65c990a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54eb654e9afb7bbd3bf867ba6dfcbf287ad262569f86c0815723a5376118ac8`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d2cc36c0ae1fb4725dfc44754cc365298d189308b25b6a818f9373c56d8b5`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:2f0d53def59230c037431fb279d69f0aca7b8603e3ddc47716d6a629b7837c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacf064fa25d7454a1aaa536a529a948d63741e3c9dd839168560f8b02c79d3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9647734b695bae36f7e0c32edbeebd3cf169b841161c9d4c577a1ece6018`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 6.6 MB (6603836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652b02d0c60b9d62fa04ca56202b067023a35da376bc9a712492b39a4338579`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5a6d01daa3a734095f6be97aa9b7b10a347d019c52cbf4dfffca96bb55f8d6`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:46d9178ace4d9f9b7e8307fdf38c831b0130174836ad584ec872a1d86af216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59c14622147cf68ab22ed7eb89e630f31c7d3213c566032a73cc0b9918fa51`

```dockerfile
```

-	Layers:
	-	`sha256:1046c910412b33c1747ecde0dd3656153062c8e55cde48158e5aa2a7f3053e86`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:b14393862d9ba5aed718097fefbc0ab96f29dee8f3e91d9bc293b76a913dce3e
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
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:a07df4097a4c1873483b76056063eb213f9ab0d0f6fd8ee605afdc6aa54b7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:a07df4097a4c1873483b76056063eb213f9ab0d0f6fd8ee605afdc6aa54b7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:b14393862d9ba5aed718097fefbc0ab96f29dee8f3e91d9bc293b76a913dce3e
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
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:430b604c3deba1df9281ce46d0f370f7eb006dc5b82dcba2db0db9d12aca8f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2c7c65263538bb027f22ec3c9b98be9de93b9fb8607794d8fcae9e7c099f014a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190866639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eda5d64d526aaf3ca69f70b5a7bebe2403fff0fa5385dacd8f5573909d612a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:00:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 21:00:23 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER=2.11.3
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.3/nats-server-v2.11.3-windows-amd64.zip
# Wed, 14 May 2025 21:00:25 GMT
ENV NATS_SERVER_SHASUM=553b61ad3581c28a93eb039f0167efc4470fb3ec3a5cff9570545eb5f57acf25
# Wed, 14 May 2025 21:01:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 21:01:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 21:01:38 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:01:39 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:01:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:01:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0ae011bb62d528ca9feb89e5812ff25ebe8c57772e044d4c488929899d089`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf68f22b1d09993c857196717ed40e9cb7137187950fac4d1314e1e71983dc`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0376a7d0c30827c309d390afdce9e1a185638d792e02cc7f6a3a618e3d77d145`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b424104a0f6fdad4cf32e6b1ea463948071a9f6281bb735a161545ab27497b`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f34380762d67935a8cf37e7afa8403df4a48589429bbffe6feee81ffd7b909`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ce307d87e99925c7a34c82120959f82f8fad23e831c4de345f631695149a1`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 325.3 KB (325291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38678459c07cd527b3ed295ec5f5224e17077ff707e9cdf6dc8d9997884bbf`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 6.8 MB (6811608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d854eedd2a7079826ab676fd665e341f97a277c29cb5b21da355d7b5cd71ab4f`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f204f830eae1b5ed87a5df94e9b2559d80612052d81ca1009f415f278bfa8b5e`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645b40626dba336c258c04ff62dfc043bc24e01c2cbbf3c82d084e449e2231a`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf65b00896e5230131bedb16fef3f1edb66ef2014a30d2c1b7e303f65dadc9c`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:430b604c3deba1df9281ce46d0f370f7eb006dc5b82dcba2db0db9d12aca8f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2c7c65263538bb027f22ec3c9b98be9de93b9fb8607794d8fcae9e7c099f014a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190866639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eda5d64d526aaf3ca69f70b5a7bebe2403fff0fa5385dacd8f5573909d612a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:00:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 21:00:23 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER=2.11.3
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.3/nats-server-v2.11.3-windows-amd64.zip
# Wed, 14 May 2025 21:00:25 GMT
ENV NATS_SERVER_SHASUM=553b61ad3581c28a93eb039f0167efc4470fb3ec3a5cff9570545eb5f57acf25
# Wed, 14 May 2025 21:01:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 21:01:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 21:01:38 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:01:39 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:01:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:01:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0ae011bb62d528ca9feb89e5812ff25ebe8c57772e044d4c488929899d089`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf68f22b1d09993c857196717ed40e9cb7137187950fac4d1314e1e71983dc`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0376a7d0c30827c309d390afdce9e1a185638d792e02cc7f6a3a618e3d77d145`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b424104a0f6fdad4cf32e6b1ea463948071a9f6281bb735a161545ab27497b`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f34380762d67935a8cf37e7afa8403df4a48589429bbffe6feee81ffd7b909`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ce307d87e99925c7a34c82120959f82f8fad23e831c4de345f631695149a1`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 325.3 KB (325291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38678459c07cd527b3ed295ec5f5224e17077ff707e9cdf6dc8d9997884bbf`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 6.8 MB (6811608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d854eedd2a7079826ab676fd665e341f97a277c29cb5b21da355d7b5cd71ab4f`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f204f830eae1b5ed87a5df94e9b2559d80612052d81ca1009f415f278bfa8b5e`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645b40626dba336c258c04ff62dfc043bc24e01c2cbbf3c82d084e449e2231a`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf65b00896e5230131bedb16fef3f1edb66ef2014a30d2c1b7e303f65dadc9c`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:90e0218d56c985136af5a251758962585c8f82e64d2a222bb3a0525f28f076a4
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
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 08 May 2025 17:10:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 08 May 2025 19:09:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:93712e2af4500282de4687c70a83f586e4d54c4d70da10d0c4d9c156bd394b47
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
$ docker pull nats@sha256:c34d45bf23d649a4d37ce201fda0b320a648321400c3a748316e56de6e99fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad8efc48f3f88e92f1aa1217506d1695658b3d9a6bad7d60e3fedefa53c2579`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3b2d23beaad798bb05689b7b0c38b571c62de55bb42fe3d53872cc5ff92da`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 6.6 MB (6639761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af882d59a8322a1c938ce881bae1d6f8e4c67a83cd10de3093fe63d84bd4816e`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e33ceb26f25c0ca98ca5658db546fc04ca902221f66297bc2f30b3468abd4`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:279bfc65a9ab0e539497f45337ff6ed2faf7b612fb4839dd6a0fa900508b4ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c778b071dcf85c9d9104248b88336f83be5b3bda6b70cba034976af2f275f57`

```dockerfile
```

-	Layers:
	-	`sha256:129e2409afba42dbf5c67d05ec6eb6f8c873f5904c0ff5f38b4c981d2b7f412c`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d9215923753a980ccecb0dcf2b6841e4d3ef6884ebcd05292cb7a2583a3b8530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb831cfb4294c6f1b05e21607b2f6872b235265cc47089cb18582b225d1249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f67ef15a3e6592471363dd18bc7267cd47ab6e65d7d6a0d811a3364d59df6e`  
		Last Modified: Thu, 01 May 2025 16:38:54 GMT  
		Size: 6.4 MB (6363842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb3661b4153de935d2124a23b501709ed0f710a1b9cf9d6a6137525c18d05b9`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ef4f92c061db0ef6d4931e407e1583e53dc6aa441535c15eb5dd789a115773`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c65a6c7bf9a8b042b1f449b053bfe0dfd1cef9fa4249f8747268c49a5740f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe767250ee00671e619eb9b99c513d9cc1e0dd692f51ae4ffd655f0055bd6af`

```dockerfile
```

-	Layers:
	-	`sha256:5615a93039a5f61ab9bef28288f3860598c067c009e128dcd27e42f85ac20301`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 13.2 KB (13196 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e2cef85475714d4ad1c8e8fa1e69852499955d83730737ef2bbd8fe633e7020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9450061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2ef8b03fec17a1a701077878f52a06d67317d0cb6010c569f3e791633fdbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d33a05d4fc89796e871bbc51f7c2f03473ab7d395ae867ea6ded0925425930`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 6.4 MB (6350965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfb48057ca2884d5cbbe61f040003470fb7d1eef9df85d1d6d1f106b2e6ae3`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e033463ccd5cbae1b4d8e4c658de11bcd5d60e3a4813360434b14b905b47693`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:bd174726bb7e67dcf23132668b2a382995ff24039238aa054c6375c9cd59d298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cce4b6f193efa833d132fc5128ad9519e927160b35c56112d7e60d8eb9469b3`

```dockerfile
```

-	Layers:
	-	`sha256:f8bb9a0270a41c5386708d530c1e9d2e65144998b4ad8ed0e5d6be7bb9e44baa`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3145ec04db64e45caeb0f29667668a316c36b68e31c2b3d939bb9d958f0a74f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92f22cb37c471307a70200f79c08e245c8bd15242fcf35614f427ca7444321f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438f232ef49cc8a1c095d8de2c048f9e3b5601888fd3765fdfe35a2460f21fe9`  
		Last Modified: Thu, 08 May 2025 17:22:48 GMT  
		Size: 6.1 MB (6145669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d605f23890a635dfb31c63a57f053984f104fb935e1773e0e2fded93c7426b`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa6c6da40fc6e072ba6046754df41177e7d69a56c57fefc409dec3e2f0cc32d`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0f19f785d00a6cefc980a3a8e6b4005413c51965fdd6766b476dbd39812a05a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15084770e78cbbec61e01f467cf7900076a503f69fcf484cbb8aba6d23e5041e`

```dockerfile
```

-	Layers:
	-	`sha256:e5d13f6b4cb7d8778987db76d62b9476b8ec77826cf66bbf8f51f9ea9c9ce687`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:50117e272809853308376a05ca020eb6e23911a49abff46c55ab692efc3b3669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9700852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aea0efae4f9a3fbbbb9baf1f485e5a90b04723d760946fc74a51f1058bd97b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b3911883a3d22279373bc74804c2995b36c10520bf9ac1c4667699b5374db`  
		Last Modified: Thu, 01 May 2025 16:39:22 GMT  
		Size: 6.1 MB (6125534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eea76948941bc50b2efbec987784930fe42c32734bada6dbecd4c52b2a5929`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51479d12c82553566d4db85b775ebe378ffd06e2344f6e86160683723e6902`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9832a8b75f208a0ab0465377e7fa87f571195898fe81a85ce2913fb69ffd907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229468fb8f66a01208934dcf50680c63131e71f6c657a63de7795f7d99b6854a`

```dockerfile
```

-	Layers:
	-	`sha256:b604ecda47807a4ab87664a2f0113fe11475ceb9affe4d8ddb7f52f062e8ae59`  
		Last Modified: Thu, 01 May 2025 16:39:21 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:82d76d997f357c81c1b979178924d10a329b209d7a040afb9fbb1f4a4ab9160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9951046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f8de5e69e58a8f32dcdcda2a08579afa328c71127508bdbafa8785e78fa8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0886cbd4a169e692b2e3025d48b7b4eedc22bde576167e4ce914a4fc6be2fabd`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 6.5 MB (6482509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b1086d683042d9331e427a01afd7e8bcc39c56a16a0c83c21ee709f9badf1`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6041a9ca0a4f2a5124f9cb2a670689ec22aee1c2595024425dfc8e7417e39f2f`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ba0291acad692758de3bd8a88cd7ba9adadd48b6656814e1cb476265bffda4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa7f57e04cd4ba1e1494ad1dd08230beb012c65d8d0b062fea2ec2754167687`

```dockerfile
```

-	Layers:
	-	`sha256:b804766c02248fbcab4d51f20fb87a2c613a90e9e3a244f0b1adb142fabbfb3a`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:93712e2af4500282de4687c70a83f586e4d54c4d70da10d0c4d9c156bd394b47
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

### `nats:2.10-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:c34d45bf23d649a4d37ce201fda0b320a648321400c3a748316e56de6e99fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad8efc48f3f88e92f1aa1217506d1695658b3d9a6bad7d60e3fedefa53c2579`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3b2d23beaad798bb05689b7b0c38b571c62de55bb42fe3d53872cc5ff92da`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 6.6 MB (6639761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af882d59a8322a1c938ce881bae1d6f8e4c67a83cd10de3093fe63d84bd4816e`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e33ceb26f25c0ca98ca5658db546fc04ca902221f66297bc2f30b3468abd4`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:279bfc65a9ab0e539497f45337ff6ed2faf7b612fb4839dd6a0fa900508b4ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c778b071dcf85c9d9104248b88336f83be5b3bda6b70cba034976af2f275f57`

```dockerfile
```

-	Layers:
	-	`sha256:129e2409afba42dbf5c67d05ec6eb6f8c873f5904c0ff5f38b4c981d2b7f412c`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:d9215923753a980ccecb0dcf2b6841e4d3ef6884ebcd05292cb7a2583a3b8530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb831cfb4294c6f1b05e21607b2f6872b235265cc47089cb18582b225d1249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f67ef15a3e6592471363dd18bc7267cd47ab6e65d7d6a0d811a3364d59df6e`  
		Last Modified: Thu, 01 May 2025 16:38:54 GMT  
		Size: 6.4 MB (6363842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb3661b4153de935d2124a23b501709ed0f710a1b9cf9d6a6137525c18d05b9`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ef4f92c061db0ef6d4931e407e1583e53dc6aa441535c15eb5dd789a115773`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c65a6c7bf9a8b042b1f449b053bfe0dfd1cef9fa4249f8747268c49a5740f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe767250ee00671e619eb9b99c513d9cc1e0dd692f51ae4ffd655f0055bd6af`

```dockerfile
```

-	Layers:
	-	`sha256:5615a93039a5f61ab9bef28288f3860598c067c009e128dcd27e42f85ac20301`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 13.2 KB (13196 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:e2cef85475714d4ad1c8e8fa1e69852499955d83730737ef2bbd8fe633e7020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9450061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2ef8b03fec17a1a701077878f52a06d67317d0cb6010c569f3e791633fdbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d33a05d4fc89796e871bbc51f7c2f03473ab7d395ae867ea6ded0925425930`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 6.4 MB (6350965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfb48057ca2884d5cbbe61f040003470fb7d1eef9df85d1d6d1f106b2e6ae3`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e033463ccd5cbae1b4d8e4c658de11bcd5d60e3a4813360434b14b905b47693`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:bd174726bb7e67dcf23132668b2a382995ff24039238aa054c6375c9cd59d298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cce4b6f193efa833d132fc5128ad9519e927160b35c56112d7e60d8eb9469b3`

```dockerfile
```

-	Layers:
	-	`sha256:f8bb9a0270a41c5386708d530c1e9d2e65144998b4ad8ed0e5d6be7bb9e44baa`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3145ec04db64e45caeb0f29667668a316c36b68e31c2b3d939bb9d958f0a74f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92f22cb37c471307a70200f79c08e245c8bd15242fcf35614f427ca7444321f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438f232ef49cc8a1c095d8de2c048f9e3b5601888fd3765fdfe35a2460f21fe9`  
		Last Modified: Thu, 08 May 2025 17:22:48 GMT  
		Size: 6.1 MB (6145669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d605f23890a635dfb31c63a57f053984f104fb935e1773e0e2fded93c7426b`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa6c6da40fc6e072ba6046754df41177e7d69a56c57fefc409dec3e2f0cc32d`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:0f19f785d00a6cefc980a3a8e6b4005413c51965fdd6766b476dbd39812a05a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15084770e78cbbec61e01f467cf7900076a503f69fcf484cbb8aba6d23e5041e`

```dockerfile
```

-	Layers:
	-	`sha256:e5d13f6b4cb7d8778987db76d62b9476b8ec77826cf66bbf8f51f9ea9c9ce687`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:50117e272809853308376a05ca020eb6e23911a49abff46c55ab692efc3b3669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9700852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aea0efae4f9a3fbbbb9baf1f485e5a90b04723d760946fc74a51f1058bd97b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b3911883a3d22279373bc74804c2995b36c10520bf9ac1c4667699b5374db`  
		Last Modified: Thu, 01 May 2025 16:39:22 GMT  
		Size: 6.1 MB (6125534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eea76948941bc50b2efbec987784930fe42c32734bada6dbecd4c52b2a5929`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51479d12c82553566d4db85b775ebe378ffd06e2344f6e86160683723e6902`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f9832a8b75f208a0ab0465377e7fa87f571195898fe81a85ce2913fb69ffd907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229468fb8f66a01208934dcf50680c63131e71f6c657a63de7795f7d99b6854a`

```dockerfile
```

-	Layers:
	-	`sha256:b604ecda47807a4ab87664a2f0113fe11475ceb9affe4d8ddb7f52f062e8ae59`  
		Last Modified: Thu, 01 May 2025 16:39:21 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:82d76d997f357c81c1b979178924d10a329b209d7a040afb9fbb1f4a4ab9160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9951046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f8de5e69e58a8f32dcdcda2a08579afa328c71127508bdbafa8785e78fa8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0886cbd4a169e692b2e3025d48b7b4eedc22bde576167e4ce914a4fc6be2fabd`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 6.5 MB (6482509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b1086d683042d9331e427a01afd7e8bcc39c56a16a0c83c21ee709f9badf1`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6041a9ca0a4f2a5124f9cb2a670689ec22aee1c2595024425dfc8e7417e39f2f`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ba0291acad692758de3bd8a88cd7ba9adadd48b6656814e1cb476265bffda4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa7f57e04cd4ba1e1494ad1dd08230beb012c65d8d0b062fea2ec2754167687`

```dockerfile
```

-	Layers:
	-	`sha256:b804766c02248fbcab4d51f20fb87a2c613a90e9e3a244f0b1adb142fabbfb3a`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:f1fc04f650ac4cd8c40aa3c7c46a0f2066999a61b4e3be99945151adb1d24aa5
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
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 08 May 2025 17:10:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 08 May 2025 19:09:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:1bb553cba2972802ff22b0a1281c11e946a66147579ed4ebab3a310058505097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:1bb553cba2972802ff22b0a1281c11e946a66147579ed4ebab3a310058505097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:f1fc04f650ac4cd8c40aa3c7c46a0f2066999a61b4e3be99945151adb1d24aa5
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
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 08 May 2025 17:10:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 08 May 2025 19:09:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:497a9cb9259dea3157192c47053d210e90285f245a40302113147c78935f415a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7cee34982b9961eca0791af019a96210f3acfb0b541c777fef4674acce9ebffd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190701818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304379749a747af729040c8fc24ea557b571e8851904d77062912ce7f19ed13e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_SERVER=2.10.29
# Wed, 14 May 2025 20:57:48 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Wed, 14 May 2025 20:57:49 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Wed, 14 May 2025 20:58:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 20:58:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 20:58:40 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 20:58:41 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 20:58:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 20:58:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61077ce6abbdae8515ed8aee8d125e78c4cac8c784a425794f86615c897c5350`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794b39a004828c5754f1625d423719263b57a56c0f9d146dac4f3f4eeca00619`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084927b2191adc36daf6f816dbfc6f7fc2f39616f120eb2651541cc473469c1d`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f419ade08147d57977fc7931cc12b84db32642f88e21afce4da375e7e51dee`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef3124c22d55ce500386d4b4e302947756899e4b22694baa0f983ac49331ec8`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ce137abceda359d4a3c7b368ea88cf8f545610e1cf97d8b6a883455b6cb49`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 332.9 KB (332919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7d2e2aeda12346ac02cd0fbd2469f9b9139a606a9993af6d38d1f5067291f4`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 6.6 MB (6639239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e924aac8362f8466698a1b3cb28f4d7cc0b32f9ec6db4146dae40bb696b0b9a`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2218925f1c3045fd7b8c4c505a18617b96b18b25084ff3c704702a01def48dcf`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe49501346aad8e6904d0c916ae6c2977054bb03a19422d25bb61fa17f4c048`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eee89edd57fb6cba67f1345aa73742d0a392b8fce89e8db3349b02fab6f9292`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:497a9cb9259dea3157192c47053d210e90285f245a40302113147c78935f415a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7cee34982b9961eca0791af019a96210f3acfb0b541c777fef4674acce9ebffd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190701818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304379749a747af729040c8fc24ea557b571e8851904d77062912ce7f19ed13e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_SERVER=2.10.29
# Wed, 14 May 2025 20:57:48 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Wed, 14 May 2025 20:57:49 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Wed, 14 May 2025 20:58:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 20:58:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 20:58:40 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 20:58:41 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 20:58:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 20:58:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61077ce6abbdae8515ed8aee8d125e78c4cac8c784a425794f86615c897c5350`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794b39a004828c5754f1625d423719263b57a56c0f9d146dac4f3f4eeca00619`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084927b2191adc36daf6f816dbfc6f7fc2f39616f120eb2651541cc473469c1d`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f419ade08147d57977fc7931cc12b84db32642f88e21afce4da375e7e51dee`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef3124c22d55ce500386d4b4e302947756899e4b22694baa0f983ac49331ec8`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ce137abceda359d4a3c7b368ea88cf8f545610e1cf97d8b6a883455b6cb49`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 332.9 KB (332919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7d2e2aeda12346ac02cd0fbd2469f9b9139a606a9993af6d38d1f5067291f4`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 6.6 MB (6639239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e924aac8362f8466698a1b3cb28f4d7cc0b32f9ec6db4146dae40bb696b0b9a`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2218925f1c3045fd7b8c4c505a18617b96b18b25084ff3c704702a01def48dcf`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe49501346aad8e6904d0c916ae6c2977054bb03a19422d25bb61fa17f4c048`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eee89edd57fb6cba67f1345aa73742d0a392b8fce89e8db3349b02fab6f9292`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29`

```console
$ docker pull nats@sha256:90e0218d56c985136af5a251758962585c8f82e64d2a222bb3a0525f28f076a4
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
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10.29` - linux; amd64

```console
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 08 May 2025 17:10:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 08 May 2025 19:09:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-alpine`

```console
$ docker pull nats@sha256:93712e2af4500282de4687c70a83f586e4d54c4d70da10d0c4d9c156bd394b47
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
$ docker pull nats@sha256:c34d45bf23d649a4d37ce201fda0b320a648321400c3a748316e56de6e99fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad8efc48f3f88e92f1aa1217506d1695658b3d9a6bad7d60e3fedefa53c2579`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3b2d23beaad798bb05689b7b0c38b571c62de55bb42fe3d53872cc5ff92da`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 6.6 MB (6639761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af882d59a8322a1c938ce881bae1d6f8e4c67a83cd10de3093fe63d84bd4816e`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e33ceb26f25c0ca98ca5658db546fc04ca902221f66297bc2f30b3468abd4`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:279bfc65a9ab0e539497f45337ff6ed2faf7b612fb4839dd6a0fa900508b4ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c778b071dcf85c9d9104248b88336f83be5b3bda6b70cba034976af2f275f57`

```dockerfile
```

-	Layers:
	-	`sha256:129e2409afba42dbf5c67d05ec6eb6f8c873f5904c0ff5f38b4c981d2b7f412c`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d9215923753a980ccecb0dcf2b6841e4d3ef6884ebcd05292cb7a2583a3b8530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb831cfb4294c6f1b05e21607b2f6872b235265cc47089cb18582b225d1249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f67ef15a3e6592471363dd18bc7267cd47ab6e65d7d6a0d811a3364d59df6e`  
		Last Modified: Thu, 01 May 2025 16:38:54 GMT  
		Size: 6.4 MB (6363842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb3661b4153de935d2124a23b501709ed0f710a1b9cf9d6a6137525c18d05b9`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ef4f92c061db0ef6d4931e407e1583e53dc6aa441535c15eb5dd789a115773`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c65a6c7bf9a8b042b1f449b053bfe0dfd1cef9fa4249f8747268c49a5740f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe767250ee00671e619eb9b99c513d9cc1e0dd692f51ae4ffd655f0055bd6af`

```dockerfile
```

-	Layers:
	-	`sha256:5615a93039a5f61ab9bef28288f3860598c067c009e128dcd27e42f85ac20301`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 13.2 KB (13196 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e2cef85475714d4ad1c8e8fa1e69852499955d83730737ef2bbd8fe633e7020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9450061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2ef8b03fec17a1a701077878f52a06d67317d0cb6010c569f3e791633fdbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d33a05d4fc89796e871bbc51f7c2f03473ab7d395ae867ea6ded0925425930`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 6.4 MB (6350965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfb48057ca2884d5cbbe61f040003470fb7d1eef9df85d1d6d1f106b2e6ae3`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e033463ccd5cbae1b4d8e4c658de11bcd5d60e3a4813360434b14b905b47693`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:bd174726bb7e67dcf23132668b2a382995ff24039238aa054c6375c9cd59d298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cce4b6f193efa833d132fc5128ad9519e927160b35c56112d7e60d8eb9469b3`

```dockerfile
```

-	Layers:
	-	`sha256:f8bb9a0270a41c5386708d530c1e9d2e65144998b4ad8ed0e5d6be7bb9e44baa`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3145ec04db64e45caeb0f29667668a316c36b68e31c2b3d939bb9d958f0a74f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92f22cb37c471307a70200f79c08e245c8bd15242fcf35614f427ca7444321f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438f232ef49cc8a1c095d8de2c048f9e3b5601888fd3765fdfe35a2460f21fe9`  
		Last Modified: Thu, 08 May 2025 17:22:48 GMT  
		Size: 6.1 MB (6145669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d605f23890a635dfb31c63a57f053984f104fb935e1773e0e2fded93c7426b`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa6c6da40fc6e072ba6046754df41177e7d69a56c57fefc409dec3e2f0cc32d`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0f19f785d00a6cefc980a3a8e6b4005413c51965fdd6766b476dbd39812a05a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15084770e78cbbec61e01f467cf7900076a503f69fcf484cbb8aba6d23e5041e`

```dockerfile
```

-	Layers:
	-	`sha256:e5d13f6b4cb7d8778987db76d62b9476b8ec77826cf66bbf8f51f9ea9c9ce687`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:50117e272809853308376a05ca020eb6e23911a49abff46c55ab692efc3b3669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9700852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aea0efae4f9a3fbbbb9baf1f485e5a90b04723d760946fc74a51f1058bd97b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b3911883a3d22279373bc74804c2995b36c10520bf9ac1c4667699b5374db`  
		Last Modified: Thu, 01 May 2025 16:39:22 GMT  
		Size: 6.1 MB (6125534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eea76948941bc50b2efbec987784930fe42c32734bada6dbecd4c52b2a5929`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51479d12c82553566d4db85b775ebe378ffd06e2344f6e86160683723e6902`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9832a8b75f208a0ab0465377e7fa87f571195898fe81a85ce2913fb69ffd907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229468fb8f66a01208934dcf50680c63131e71f6c657a63de7795f7d99b6854a`

```dockerfile
```

-	Layers:
	-	`sha256:b604ecda47807a4ab87664a2f0113fe11475ceb9affe4d8ddb7f52f062e8ae59`  
		Last Modified: Thu, 01 May 2025 16:39:21 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; s390x

```console
$ docker pull nats@sha256:82d76d997f357c81c1b979178924d10a329b209d7a040afb9fbb1f4a4ab9160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9951046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f8de5e69e58a8f32dcdcda2a08579afa328c71127508bdbafa8785e78fa8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0886cbd4a169e692b2e3025d48b7b4eedc22bde576167e4ce914a4fc6be2fabd`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 6.5 MB (6482509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b1086d683042d9331e427a01afd7e8bcc39c56a16a0c83c21ee709f9badf1`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6041a9ca0a4f2a5124f9cb2a670689ec22aee1c2595024425dfc8e7417e39f2f`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ba0291acad692758de3bd8a88cd7ba9adadd48b6656814e1cb476265bffda4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa7f57e04cd4ba1e1494ad1dd08230beb012c65d8d0b062fea2ec2754167687`

```dockerfile
```

-	Layers:
	-	`sha256:b804766c02248fbcab4d51f20fb87a2c613a90e9e3a244f0b1adb142fabbfb3a`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-alpine3.21`

```console
$ docker pull nats@sha256:93712e2af4500282de4687c70a83f586e4d54c4d70da10d0c4d9c156bd394b47
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

### `nats:2.10.29-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:c34d45bf23d649a4d37ce201fda0b320a648321400c3a748316e56de6e99fa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad8efc48f3f88e92f1aa1217506d1695658b3d9a6bad7d60e3fedefa53c2579`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f3b2d23beaad798bb05689b7b0c38b571c62de55bb42fe3d53872cc5ff92da`  
		Last Modified: Thu, 08 May 2025 17:06:34 GMT  
		Size: 6.6 MB (6639761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af882d59a8322a1c938ce881bae1d6f8e4c67a83cd10de3093fe63d84bd4816e`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e33ceb26f25c0ca98ca5658db546fc04ca902221f66297bc2f30b3468abd4`  
		Last Modified: Thu, 08 May 2025 17:06:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:279bfc65a9ab0e539497f45337ff6ed2faf7b612fb4839dd6a0fa900508b4ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c778b071dcf85c9d9104248b88336f83be5b3bda6b70cba034976af2f275f57`

```dockerfile
```

-	Layers:
	-	`sha256:129e2409afba42dbf5c67d05ec6eb6f8c873f5904c0ff5f38b4c981d2b7f412c`  
		Last Modified: Thu, 01 May 2025 16:39:23 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:d9215923753a980ccecb0dcf2b6841e4d3ef6884ebcd05292cb7a2583a3b8530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb831cfb4294c6f1b05e21607b2f6872b235265cc47089cb18582b225d1249`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f67ef15a3e6592471363dd18bc7267cd47ab6e65d7d6a0d811a3364d59df6e`  
		Last Modified: Thu, 01 May 2025 16:38:54 GMT  
		Size: 6.4 MB (6363842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb3661b4153de935d2124a23b501709ed0f710a1b9cf9d6a6137525c18d05b9`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ef4f92c061db0ef6d4931e407e1583e53dc6aa441535c15eb5dd789a115773`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c65a6c7bf9a8b042b1f449b053bfe0dfd1cef9fa4249f8747268c49a5740f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe767250ee00671e619eb9b99c513d9cc1e0dd692f51ae4ffd655f0055bd6af`

```dockerfile
```

-	Layers:
	-	`sha256:5615a93039a5f61ab9bef28288f3860598c067c009e128dcd27e42f85ac20301`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 13.2 KB (13196 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:e2cef85475714d4ad1c8e8fa1e69852499955d83730737ef2bbd8fe633e7020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9450061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2ef8b03fec17a1a701077878f52a06d67317d0cb6010c569f3e791633fdbd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d33a05d4fc89796e871bbc51f7c2f03473ab7d395ae867ea6ded0925425930`  
		Last Modified: Thu, 01 May 2025 16:38:53 GMT  
		Size: 6.4 MB (6350965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfb48057ca2884d5cbbe61f040003470fb7d1eef9df85d1d6d1f106b2e6ae3`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e033463ccd5cbae1b4d8e4c658de11bcd5d60e3a4813360434b14b905b47693`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:bd174726bb7e67dcf23132668b2a382995ff24039238aa054c6375c9cd59d298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cce4b6f193efa833d132fc5128ad9519e927160b35c56112d7e60d8eb9469b3`

```dockerfile
```

-	Layers:
	-	`sha256:f8bb9a0270a41c5386708d530c1e9d2e65144998b4ad8ed0e5d6be7bb9e44baa`  
		Last Modified: Thu, 01 May 2025 16:38:52 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3145ec04db64e45caeb0f29667668a316c36b68e31c2b3d939bb9d958f0a74f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92f22cb37c471307a70200f79c08e245c8bd15242fcf35614f427ca7444321f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438f232ef49cc8a1c095d8de2c048f9e3b5601888fd3765fdfe35a2460f21fe9`  
		Last Modified: Thu, 08 May 2025 17:22:48 GMT  
		Size: 6.1 MB (6145669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d605f23890a635dfb31c63a57f053984f104fb935e1773e0e2fded93c7426b`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa6c6da40fc6e072ba6046754df41177e7d69a56c57fefc409dec3e2f0cc32d`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:0f19f785d00a6cefc980a3a8e6b4005413c51965fdd6766b476dbd39812a05a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15084770e78cbbec61e01f467cf7900076a503f69fcf484cbb8aba6d23e5041e`

```dockerfile
```

-	Layers:
	-	`sha256:e5d13f6b4cb7d8778987db76d62b9476b8ec77826cf66bbf8f51f9ea9c9ce687`  
		Last Modified: Thu, 01 May 2025 16:38:56 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:50117e272809853308376a05ca020eb6e23911a49abff46c55ab692efc3b3669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9700852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aea0efae4f9a3fbbbb9baf1f485e5a90b04723d760946fc74a51f1058bd97b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3b3911883a3d22279373bc74804c2995b36c10520bf9ac1c4667699b5374db`  
		Last Modified: Thu, 01 May 2025 16:39:22 GMT  
		Size: 6.1 MB (6125534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eea76948941bc50b2efbec987784930fe42c32734bada6dbecd4c52b2a5929`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df51479d12c82553566d4db85b775ebe378ffd06e2344f6e86160683723e6902`  
		Last Modified: Thu, 01 May 2025 16:39:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:f9832a8b75f208a0ab0465377e7fa87f571195898fe81a85ce2913fb69ffd907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229468fb8f66a01208934dcf50680c63131e71f6c657a63de7795f7d99b6854a`

```dockerfile
```

-	Layers:
	-	`sha256:b604ecda47807a4ab87664a2f0113fe11475ceb9affe4d8ddb7f52f062e8ae59`  
		Last Modified: Thu, 01 May 2025 16:39:21 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:82d76d997f357c81c1b979178924d10a329b209d7a040afb9fbb1f4a4ab9160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9951046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f8de5e69e58a8f32dcdcda2a08579afa328c71127508bdbafa8785e78fa8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.10.29
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0886cbd4a169e692b2e3025d48b7b4eedc22bde576167e4ce914a4fc6be2fabd`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 6.5 MB (6482509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b1086d683042d9331e427a01afd7e8bcc39c56a16a0c83c21ee709f9badf1`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6041a9ca0a4f2a5124f9cb2a670689ec22aee1c2595024425dfc8e7417e39f2f`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:ba0291acad692758de3bd8a88cd7ba9adadd48b6656814e1cb476265bffda4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa7f57e04cd4ba1e1494ad1dd08230beb012c65d8d0b062fea2ec2754167687`

```dockerfile
```

-	Layers:
	-	`sha256:b804766c02248fbcab4d51f20fb87a2c613a90e9e3a244f0b1adb142fabbfb3a`  
		Last Modified: Thu, 01 May 2025 16:40:27 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-linux`

```console
$ docker pull nats@sha256:f1fc04f650ac4cd8c40aa3c7c46a0f2066999a61b4e3be99945151adb1d24aa5
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
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 08 May 2025 17:10:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 08 May 2025 19:09:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-nanoserver`

```console
$ docker pull nats@sha256:1bb553cba2972802ff22b0a1281c11e946a66147579ed4ebab3a310058505097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10.29-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-nanoserver-1809`

```console
$ docker pull nats@sha256:1bb553cba2972802ff22b0a1281c11e946a66147579ed4ebab3a310058505097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10.29-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2161d1e1f94ac34edd3eeb3e988a132d0b80e1ae578a28901ced25b5d5a4be04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989144758dca5d5bc74a916c0fbc16f6c3d6772d0ac66f3f5c3154a304fb1926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:22:56 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:23:00 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:23:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:23:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:23:03 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35a13d3a2ccb6d6921800013fd2bafb22fdddd0839e1702de9c3ed71d624e01`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fcabfa424d4764fde945c8ef78c9a9e3447fe9fa96663564fac1e1ad6b5269`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 6.3 MB (6298138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4d978b7505d1beafe17ec8bd7a83c79d9f90cb9c838cacb0a65ba0d62e925`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8b062d5e7dc7c72a41dce15f3c57b7c154f653dbf3f3af39380330b8378d24`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee38558620886b53646fde38cf4bceb3c93944c4c1fbf218d71a2d1ea7d7b1a`  
		Last Modified: Wed, 14 May 2025 21:23:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac45ac9cff58dc0e1d04bdba98a370b8fb4b0092dcb07e4f7b213595a395a8`  
		Last Modified: Wed, 14 May 2025 21:23:06 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-scratch`

```console
$ docker pull nats@sha256:f1fc04f650ac4cd8c40aa3c7c46a0f2066999a61b4e3be99945151adb1d24aa5
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
$ docker pull nats@sha256:3ccfdfb4f67d6b15d69e5b590eebbd96c3f7ec53f8ced1a9a4aac60d93aa11c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a774814288e1fd893f7331df669215f646f6cf98fb4a0b0b67ac130ecbc292`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aeeb60ebe6caabdf00087638b31e612157fb76df70f09daae4aaf298f3339d`  
		Last Modified: Thu, 08 May 2025 17:10:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fb05c36e05cb6fd98ab9578bf3f3522c5dda3b8db87c4b3f994bab4fb2c52bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5217c566ef49ccb62eb72b4d63e24c23407e01d1a483f783d19f43deb31978`

```dockerfile
```

-	Layers:
	-	`sha256:bf329933f2001d892b1db19e56be440c7cc1471cbfd53e85627380b9eeecfa13`  
		Last Modified: Thu, 01 May 2025 16:46:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b6ca28cb0f26d521de072e0428eda868dfc1053f02ee89da87e122abbbcc5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a244218290447acaf4597f5813cdd9b33d442f548e97ac69f3ba9bf77b007e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2635c150a57e298a8572ecc73e84b470cf6f64d5d04bb81b438de0d2a578e`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ba5d033bc950f897b411410b7bfb78b5058d32b86b8ffaf7265e62e043e20f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfee55275a487ab6b108c1e0c26fd8d58c5914aac413eaa083766552f361395`

```dockerfile
```

-	Layers:
	-	`sha256:49a95ae7819d7b3b2da785dc18d291000c88914a33318296ef12da97f0616623`  
		Last Modified: Thu, 01 May 2025 16:46:12 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:df20fbfe0bb522658b99afc79ac3890e502c6970a671f3ad578076fe583eb5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b209380767db19497ed31465cd8ea6f57747719a0b7c3424178728fa4ef380`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Thu, 01 May 2025 10:59:24 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b68896e7d11974b1313147602b9b9672df2062a2a1ba0fb0254c70bc0dc0e`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b0cfe6d5686bf2b793b3456b56e58e4709af2b1be8896efd6a883dbf3afd8947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4cc0b81dfacb98ca6bbac7f072e0daf502def9b3d32ec1fa94ea2ba790bc8c`

```dockerfile
```

-	Layers:
	-	`sha256:54a912eaf0fc6d63db9786e668ee5fbd92a4b32c3480891aa1db26c32b50284c`  
		Last Modified: Thu, 01 May 2025 16:46:15 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:935fb840a8c73adfaff297b1980187748a4b3fd7816c4a78cb3524165d20a338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783285edc88812d5d1cac420dd84fda126b9342da1ddd4a5ad24724d70b0766`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc364f50cefcf174b35bb61af86057cdb8d5030b40433f6a32f2b2c9b8c05d`  
		Last Modified: Thu, 08 May 2025 19:09:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:245530ad8e2639d51db319933a737ae5e6d6d451cad28296889bd066ed9e87f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d366dc53cfe6e71c360d90a3e634be45150175d442cc53c416936d03bd1556c2`

```dockerfile
```

-	Layers:
	-	`sha256:d18e0c2e5eab72b82113e68b6bd114b5e2127dae37ea5fdae90468e3f51f31eb`  
		Last Modified: Thu, 01 May 2025 16:46:31 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:75880b6c63b7cebe9255b7608fbc73d00b8933e46ca0cbbe90c2b6c58d8abb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81da7825b3708ab6faf26cc9ccdab7321e3396534294da2330041bd16cc10322`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01318be57fae6110f9534fcddaee8e6a1c3e69f25ae1e4d106c4c8de8ae29409`  
		Last Modified: Fri, 09 May 2025 08:02:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5b57ed930c2667fe65ad1bcee2b9818a79e11a7500f81bf6abf002f323a40614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee26f11ca9c8bf7645aaa93d4a9b71a44b8e5eec7c6d2da88292202cb0c94ba0`

```dockerfile
```

-	Layers:
	-	`sha256:8d564d37941aabc78a509d369ad843dd9bbd31e598a5eb086e6ed43f44520de0`  
		Last Modified: Thu, 01 May 2025 16:47:00 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; s390x

```console
$ docker pull nats@sha256:84075ae55673cd07f22de63d995d5fb6f6ad9237fb03cd9628d8093314717a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8ab527386a9db0e153388584e1d45bde0ef4d42a924ecb08c07492c2cd4188`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Thu, 01 May 2025 10:59:27 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74d173bad3ebbebf172e48ea474c921f04af212478f36048d2ae48e968fdb19`  
		Last Modified: Fri, 09 May 2025 08:02:53 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:366a7884992207edcdabb534dadc23e5194a82acb271a57feb915092c3161a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a7d69878d9010d1441db5562973317245edebea32c25d731de86833b22a30e`

```dockerfile
```

-	Layers:
	-	`sha256:7d9401f2d8bdddd29f021b02a49ab29c2c347e45f7f6f5fab6e6aaaca052ff85`  
		Last Modified: Thu, 01 May 2025 16:46:58 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-windowsservercore`

```console
$ docker pull nats@sha256:497a9cb9259dea3157192c47053d210e90285f245a40302113147c78935f415a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10.29-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7cee34982b9961eca0791af019a96210f3acfb0b541c777fef4674acce9ebffd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190701818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304379749a747af729040c8fc24ea557b571e8851904d77062912ce7f19ed13e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_SERVER=2.10.29
# Wed, 14 May 2025 20:57:48 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Wed, 14 May 2025 20:57:49 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Wed, 14 May 2025 20:58:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 20:58:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 20:58:40 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 20:58:41 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 20:58:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 20:58:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61077ce6abbdae8515ed8aee8d125e78c4cac8c784a425794f86615c897c5350`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794b39a004828c5754f1625d423719263b57a56c0f9d146dac4f3f4eeca00619`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084927b2191adc36daf6f816dbfc6f7fc2f39616f120eb2651541cc473469c1d`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f419ade08147d57977fc7931cc12b84db32642f88e21afce4da375e7e51dee`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef3124c22d55ce500386d4b4e302947756899e4b22694baa0f983ac49331ec8`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ce137abceda359d4a3c7b368ea88cf8f545610e1cf97d8b6a883455b6cb49`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 332.9 KB (332919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7d2e2aeda12346ac02cd0fbd2469f9b9139a606a9993af6d38d1f5067291f4`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 6.6 MB (6639239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e924aac8362f8466698a1b3cb28f4d7cc0b32f9ec6db4146dae40bb696b0b9a`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2218925f1c3045fd7b8c4c505a18617b96b18b25084ff3c704702a01def48dcf`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe49501346aad8e6904d0c916ae6c2977054bb03a19422d25bb61fa17f4c048`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eee89edd57fb6cba67f1345aa73742d0a392b8fce89e8db3349b02fab6f9292`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-windowsservercore-1809`

```console
$ docker pull nats@sha256:497a9cb9259dea3157192c47053d210e90285f245a40302113147c78935f415a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.10.29-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:7cee34982b9961eca0791af019a96210f3acfb0b541c777fef4674acce9ebffd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190701818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304379749a747af729040c8fc24ea557b571e8851904d77062912ce7f19ed13e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:57:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 20:57:47 GMT
ENV NATS_SERVER=2.10.29
# Wed, 14 May 2025 20:57:48 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Wed, 14 May 2025 20:57:49 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Wed, 14 May 2025 20:58:23 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 20:58:39 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 20:58:40 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 20:58:41 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 20:58:41 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 20:58:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61077ce6abbdae8515ed8aee8d125e78c4cac8c784a425794f86615c897c5350`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794b39a004828c5754f1625d423719263b57a56c0f9d146dac4f3f4eeca00619`  
		Last Modified: Wed, 14 May 2025 20:58:46 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084927b2191adc36daf6f816dbfc6f7fc2f39616f120eb2651541cc473469c1d`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f419ade08147d57977fc7931cc12b84db32642f88e21afce4da375e7e51dee`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef3124c22d55ce500386d4b4e302947756899e4b22694baa0f983ac49331ec8`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ce137abceda359d4a3c7b368ea88cf8f545610e1cf97d8b6a883455b6cb49`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 332.9 KB (332919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7d2e2aeda12346ac02cd0fbd2469f9b9139a606a9993af6d38d1f5067291f4`  
		Last Modified: Wed, 14 May 2025 20:58:45 GMT  
		Size: 6.6 MB (6639239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e924aac8362f8466698a1b3cb28f4d7cc0b32f9ec6db4146dae40bb696b0b9a`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2218925f1c3045fd7b8c4c505a18617b96b18b25084ff3c704702a01def48dcf`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe49501346aad8e6904d0c916ae6c2977054bb03a19422d25bb61fa17f4c048`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eee89edd57fb6cba67f1345aa73742d0a392b8fce89e8db3349b02fab6f9292`  
		Last Modified: Wed, 14 May 2025 20:58:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:3072e8ea890fe66b5921f75c1385b5f49b59a7f46171d697517d186830131fa7
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
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:a79a6ff6e42ef41ef964c52bef9fe6eed02fc91cf348801e3dddbbd57636077a
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
$ docker pull nats@sha256:f6be324fcee27f2a91178d74f77bb4ba3e5a9d2e72ba7d6871f45d14aadca40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c567f7e9cb3bfc4d455ff826598a76a99a73fa13ec7367efaacf1e12c0dd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5d0247fe0c99cf6c1ecf760cd78e32964d3ddb3759704f6684937b17e5142`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 6.8 MB (6765302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b37c9588055ed3b254ae4ba53ef4c63f34fcc2aeab92b8475fcbcacfcd80b55`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe44b0610308731d27dd1e577ba8612ea42d8995d7543ffc050198010b94663`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6606e7bd2585dbedc93618630113f5655e877c1bd5dfc496a02e725e4a2fe9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e72e1fa9e878b2aba34410a32cef5eabe2a785ebf18d74b2b308387268ae11`

```dockerfile
```

-	Layers:
	-	`sha256:a096f4f7ad0e75fb3bf34e4f9cc376cccfe906466ff7158c5adcace3fc78d8eb`  
		Last Modified: Thu, 01 May 2025 16:39:11 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:10c04125727c8e5799732cbf4bb257a0be62ef4178a8305430c81e20d8c2e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9167a50c86fbbf9faacc0ba649170615658a1bcb97ea922126d16bed0b6b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637af45acc37a7a2c3ca6ce929b4671046476166442a11fc80d8f0bf90ecd868`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 6.5 MB (6484260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b2aff493c7a4b631188bf1e08800a5b7c4ff8c7b0a35d871d1e064b7b229f`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d157ed7867da0b76320ba85d657071b09d9648c20c89a328178ea46464e1b7`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:10c402d37b4e7ac39b9a3ae564dabb8171b6ebf57f29b2086adf5bf5bfc70452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69355e40015e4b8bba82c7bc204868461a260267941f8bfd4d8136e4c6d14f1a`

```dockerfile
```

-	Layers:
	-	`sha256:ae16ff4d4e58738b65ec2f42e2b394b9ef1c4cd8b294509afffaf0d3585aa2b0`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3d1385ecd165eeddcd5b60fe068d6cdf140ddcdc687af8e7544197e451b89be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4228daa974404161b0811acf95429df4a1c07f409613b14a22891f9d0229b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1f7a3c7b77c14f08c57f994d653a1573a628813f51ad57c8ffa6704eb1e7c`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 6.5 MB (6471695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133786e3c707b99368ea0262c4da45fbb457ff538f3e4245164f71c9d04ebcb3`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a93d5da73eaad0dceef4a853a5fda3e77ff002488070801a2e0df946562874`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b1a5520c26787b7b5b7598e8c6d32e04b6442246f45f51702f8ab9602311695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1d0f6677c8e2f5972add8fb8d56a1a1949d15ca4c27d662d5c221b9bb3987b`

```dockerfile
```

-	Layers:
	-	`sha256:91912f94323f40a81b369bdf7b31adec099387298167e8ee48fdbd643c54bbd7`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:77790b065a14aa640a9906611f2593849afbc24e3dfe9ea845191d6d6b2b9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715cd7234f00f3838f631d95b5ade02f3f069b16c157eed1908f21f1e0539245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ead951cdd1051dce5e434c83e45a7f8035db209e137743eadba8e07891ffdf`  
		Last Modified: Thu, 08 May 2025 17:14:47 GMT  
		Size: 6.3 MB (6260210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a94e80a2eaf0a11748ce4e055b47b3131f7bf07fbf5822a6684d7baaca7fe`  
		Last Modified: Thu, 08 May 2025 17:14:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedeae9f370d7774766d58004d8794999e8ee0270a3ace165434935b755ba4e1`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7be154f67a95eb115edaf3da2c42409d3cc505c20e23282796088eb999a488ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153445c3a76a150eac532c5d5e8be9663decfd6cc7f0abd49cfe93e6864c896`

```dockerfile
```

-	Layers:
	-	`sha256:11e95946e2efd0801ccd7e4d3c070b684baf2d8e019eb4eeacd52b28cbfd858f`  
		Last Modified: Thu, 01 May 2025 16:38:44 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:aeffcf1a5fd10a494bc66c184585616f260d480c74d5e5253b56d450a809146d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc14e50d0acbca9b182a873a3c80f9967dbb1442be773cba6ab4e8cfe17688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829f47e2f6c4e37799e70fe955cbec9218f793ba67d3c42843028581f41d46c`  
		Last Modified: Thu, 01 May 2025 16:39:04 GMT  
		Size: 6.2 MB (6239898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26d5042fdff67ea8c94d44aa8763edc52e021387e6d064673d469c2bc47275`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da66dedca6ed504a33045c53e38cc74882153eb3a260560fe268bb9d1b6c8e4`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:352c383d3b82380dbd9a1ac107937d3991846006be06142ba8698aa65c990a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54eb654e9afb7bbd3bf867ba6dfcbf287ad262569f86c0815723a5376118ac8`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d2cc36c0ae1fb4725dfc44754cc365298d189308b25b6a818f9373c56d8b5`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:2f0d53def59230c037431fb279d69f0aca7b8603e3ddc47716d6a629b7837c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacf064fa25d7454a1aaa536a529a948d63741e3c9dd839168560f8b02c79d3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9647734b695bae36f7e0c32edbeebd3cf169b841161c9d4c577a1ece6018`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 6.6 MB (6603836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652b02d0c60b9d62fa04ca56202b067023a35da376bc9a712492b39a4338579`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5a6d01daa3a734095f6be97aa9b7b10a347d019c52cbf4dfffca96bb55f8d6`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:46d9178ace4d9f9b7e8307fdf38c831b0130174836ad584ec872a1d86af216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59c14622147cf68ab22ed7eb89e630f31c7d3213c566032a73cc0b9918fa51`

```dockerfile
```

-	Layers:
	-	`sha256:1046c910412b33c1747ecde0dd3656153062c8e55cde48158e5aa2a7f3053e86`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.21`

```console
$ docker pull nats@sha256:a79a6ff6e42ef41ef964c52bef9fe6eed02fc91cf348801e3dddbbd57636077a
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

### `nats:2.11-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:f6be324fcee27f2a91178d74f77bb4ba3e5a9d2e72ba7d6871f45d14aadca40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c567f7e9cb3bfc4d455ff826598a76a99a73fa13ec7367efaacf1e12c0dd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5d0247fe0c99cf6c1ecf760cd78e32964d3ddb3759704f6684937b17e5142`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 6.8 MB (6765302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b37c9588055ed3b254ae4ba53ef4c63f34fcc2aeab92b8475fcbcacfcd80b55`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe44b0610308731d27dd1e577ba8612ea42d8995d7543ffc050198010b94663`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6606e7bd2585dbedc93618630113f5655e877c1bd5dfc496a02e725e4a2fe9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e72e1fa9e878b2aba34410a32cef5eabe2a785ebf18d74b2b308387268ae11`

```dockerfile
```

-	Layers:
	-	`sha256:a096f4f7ad0e75fb3bf34e4f9cc376cccfe906466ff7158c5adcace3fc78d8eb`  
		Last Modified: Thu, 01 May 2025 16:39:11 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:10c04125727c8e5799732cbf4bb257a0be62ef4178a8305430c81e20d8c2e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9167a50c86fbbf9faacc0ba649170615658a1bcb97ea922126d16bed0b6b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637af45acc37a7a2c3ca6ce929b4671046476166442a11fc80d8f0bf90ecd868`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 6.5 MB (6484260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b2aff493c7a4b631188bf1e08800a5b7c4ff8c7b0a35d871d1e064b7b229f`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d157ed7867da0b76320ba85d657071b09d9648c20c89a328178ea46464e1b7`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:10c402d37b4e7ac39b9a3ae564dabb8171b6ebf57f29b2086adf5bf5bfc70452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69355e40015e4b8bba82c7bc204868461a260267941f8bfd4d8136e4c6d14f1a`

```dockerfile
```

-	Layers:
	-	`sha256:ae16ff4d4e58738b65ec2f42e2b394b9ef1c4cd8b294509afffaf0d3585aa2b0`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:3d1385ecd165eeddcd5b60fe068d6cdf140ddcdc687af8e7544197e451b89be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4228daa974404161b0811acf95429df4a1c07f409613b14a22891f9d0229b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1f7a3c7b77c14f08c57f994d653a1573a628813f51ad57c8ffa6704eb1e7c`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 6.5 MB (6471695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133786e3c707b99368ea0262c4da45fbb457ff538f3e4245164f71c9d04ebcb3`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a93d5da73eaad0dceef4a853a5fda3e77ff002488070801a2e0df946562874`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b1a5520c26787b7b5b7598e8c6d32e04b6442246f45f51702f8ab9602311695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1d0f6677c8e2f5972add8fb8d56a1a1949d15ca4c27d662d5c221b9bb3987b`

```dockerfile
```

-	Layers:
	-	`sha256:91912f94323f40a81b369bdf7b31adec099387298167e8ee48fdbd643c54bbd7`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:77790b065a14aa640a9906611f2593849afbc24e3dfe9ea845191d6d6b2b9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715cd7234f00f3838f631d95b5ade02f3f069b16c157eed1908f21f1e0539245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ead951cdd1051dce5e434c83e45a7f8035db209e137743eadba8e07891ffdf`  
		Last Modified: Thu, 08 May 2025 17:14:47 GMT  
		Size: 6.3 MB (6260210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a94e80a2eaf0a11748ce4e055b47b3131f7bf07fbf5822a6684d7baaca7fe`  
		Last Modified: Thu, 08 May 2025 17:14:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedeae9f370d7774766d58004d8794999e8ee0270a3ace165434935b755ba4e1`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:7be154f67a95eb115edaf3da2c42409d3cc505c20e23282796088eb999a488ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153445c3a76a150eac532c5d5e8be9663decfd6cc7f0abd49cfe93e6864c896`

```dockerfile
```

-	Layers:
	-	`sha256:11e95946e2efd0801ccd7e4d3c070b684baf2d8e019eb4eeacd52b28cbfd858f`  
		Last Modified: Thu, 01 May 2025 16:38:44 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:aeffcf1a5fd10a494bc66c184585616f260d480c74d5e5253b56d450a809146d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc14e50d0acbca9b182a873a3c80f9967dbb1442be773cba6ab4e8cfe17688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829f47e2f6c4e37799e70fe955cbec9218f793ba67d3c42843028581f41d46c`  
		Last Modified: Thu, 01 May 2025 16:39:04 GMT  
		Size: 6.2 MB (6239898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26d5042fdff67ea8c94d44aa8763edc52e021387e6d064673d469c2bc47275`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da66dedca6ed504a33045c53e38cc74882153eb3a260560fe268bb9d1b6c8e4`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:352c383d3b82380dbd9a1ac107937d3991846006be06142ba8698aa65c990a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54eb654e9afb7bbd3bf867ba6dfcbf287ad262569f86c0815723a5376118ac8`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d2cc36c0ae1fb4725dfc44754cc365298d189308b25b6a818f9373c56d8b5`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:2f0d53def59230c037431fb279d69f0aca7b8603e3ddc47716d6a629b7837c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacf064fa25d7454a1aaa536a529a948d63741e3c9dd839168560f8b02c79d3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9647734b695bae36f7e0c32edbeebd3cf169b841161c9d4c577a1ece6018`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 6.6 MB (6603836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652b02d0c60b9d62fa04ca56202b067023a35da376bc9a712492b39a4338579`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5a6d01daa3a734095f6be97aa9b7b10a347d019c52cbf4dfffca96bb55f8d6`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:46d9178ace4d9f9b7e8307fdf38c831b0130174836ad584ec872a1d86af216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59c14622147cf68ab22ed7eb89e630f31c7d3213c566032a73cc0b9918fa51`

```dockerfile
```

-	Layers:
	-	`sha256:1046c910412b33c1747ecde0dd3656153062c8e55cde48158e5aa2a7f3053e86`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:b14393862d9ba5aed718097fefbc0ab96f29dee8f3e91d9bc293b76a913dce3e
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
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:a07df4097a4c1873483b76056063eb213f9ab0d0f6fd8ee605afdc6aa54b7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-1809`

```console
$ docker pull nats@sha256:a07df4097a4c1873483b76056063eb213f9ab0d0f6fd8ee605afdc6aa54b7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:b14393862d9ba5aed718097fefbc0ab96f29dee8f3e91d9bc293b76a913dce3e
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
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:430b604c3deba1df9281ce46d0f370f7eb006dc5b82dcba2db0db9d12aca8f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2c7c65263538bb027f22ec3c9b98be9de93b9fb8607794d8fcae9e7c099f014a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190866639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eda5d64d526aaf3ca69f70b5a7bebe2403fff0fa5385dacd8f5573909d612a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:00:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 21:00:23 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER=2.11.3
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.3/nats-server-v2.11.3-windows-amd64.zip
# Wed, 14 May 2025 21:00:25 GMT
ENV NATS_SERVER_SHASUM=553b61ad3581c28a93eb039f0167efc4470fb3ec3a5cff9570545eb5f57acf25
# Wed, 14 May 2025 21:01:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 21:01:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 21:01:38 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:01:39 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:01:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:01:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0ae011bb62d528ca9feb89e5812ff25ebe8c57772e044d4c488929899d089`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf68f22b1d09993c857196717ed40e9cb7137187950fac4d1314e1e71983dc`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0376a7d0c30827c309d390afdce9e1a185638d792e02cc7f6a3a618e3d77d145`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b424104a0f6fdad4cf32e6b1ea463948071a9f6281bb735a161545ab27497b`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f34380762d67935a8cf37e7afa8403df4a48589429bbffe6feee81ffd7b909`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ce307d87e99925c7a34c82120959f82f8fad23e831c4de345f631695149a1`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 325.3 KB (325291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38678459c07cd527b3ed295ec5f5224e17077ff707e9cdf6dc8d9997884bbf`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 6.8 MB (6811608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d854eedd2a7079826ab676fd665e341f97a277c29cb5b21da355d7b5cd71ab4f`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f204f830eae1b5ed87a5df94e9b2559d80612052d81ca1009f415f278bfa8b5e`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645b40626dba336c258c04ff62dfc043bc24e01c2cbbf3c82d084e449e2231a`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf65b00896e5230131bedb16fef3f1edb66ef2014a30d2c1b7e303f65dadc9c`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-1809`

```console
$ docker pull nats@sha256:430b604c3deba1df9281ce46d0f370f7eb006dc5b82dcba2db0db9d12aca8f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2c7c65263538bb027f22ec3c9b98be9de93b9fb8607794d8fcae9e7c099f014a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190866639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eda5d64d526aaf3ca69f70b5a7bebe2403fff0fa5385dacd8f5573909d612a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:00:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 21:00:23 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER=2.11.3
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.3/nats-server-v2.11.3-windows-amd64.zip
# Wed, 14 May 2025 21:00:25 GMT
ENV NATS_SERVER_SHASUM=553b61ad3581c28a93eb039f0167efc4470fb3ec3a5cff9570545eb5f57acf25
# Wed, 14 May 2025 21:01:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 21:01:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 21:01:38 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:01:39 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:01:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:01:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0ae011bb62d528ca9feb89e5812ff25ebe8c57772e044d4c488929899d089`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf68f22b1d09993c857196717ed40e9cb7137187950fac4d1314e1e71983dc`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0376a7d0c30827c309d390afdce9e1a185638d792e02cc7f6a3a618e3d77d145`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b424104a0f6fdad4cf32e6b1ea463948071a9f6281bb735a161545ab27497b`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f34380762d67935a8cf37e7afa8403df4a48589429bbffe6feee81ffd7b909`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ce307d87e99925c7a34c82120959f82f8fad23e831c4de345f631695149a1`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 325.3 KB (325291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38678459c07cd527b3ed295ec5f5224e17077ff707e9cdf6dc8d9997884bbf`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 6.8 MB (6811608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d854eedd2a7079826ab676fd665e341f97a277c29cb5b21da355d7b5cd71ab4f`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f204f830eae1b5ed87a5df94e9b2559d80612052d81ca1009f415f278bfa8b5e`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645b40626dba336c258c04ff62dfc043bc24e01c2cbbf3c82d084e449e2231a`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf65b00896e5230131bedb16fef3f1edb66ef2014a30d2c1b7e303f65dadc9c`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.3`

```console
$ docker pull nats@sha256:3072e8ea890fe66b5921f75c1385b5f49b59a7f46171d697517d186830131fa7
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
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11.3` - linux; amd64

```console
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.3-alpine`

```console
$ docker pull nats@sha256:a79a6ff6e42ef41ef964c52bef9fe6eed02fc91cf348801e3dddbbd57636077a
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

### `nats:2.11.3-alpine` - linux; amd64

```console
$ docker pull nats@sha256:f6be324fcee27f2a91178d74f77bb4ba3e5a9d2e72ba7d6871f45d14aadca40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c567f7e9cb3bfc4d455ff826598a76a99a73fa13ec7367efaacf1e12c0dd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5d0247fe0c99cf6c1ecf760cd78e32964d3ddb3759704f6684937b17e5142`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 6.8 MB (6765302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b37c9588055ed3b254ae4ba53ef4c63f34fcc2aeab92b8475fcbcacfcd80b55`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe44b0610308731d27dd1e577ba8612ea42d8995d7543ffc050198010b94663`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6606e7bd2585dbedc93618630113f5655e877c1bd5dfc496a02e725e4a2fe9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e72e1fa9e878b2aba34410a32cef5eabe2a785ebf18d74b2b308387268ae11`

```dockerfile
```

-	Layers:
	-	`sha256:a096f4f7ad0e75fb3bf34e4f9cc376cccfe906466ff7158c5adcace3fc78d8eb`  
		Last Modified: Thu, 01 May 2025 16:39:11 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:10c04125727c8e5799732cbf4bb257a0be62ef4178a8305430c81e20d8c2e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9167a50c86fbbf9faacc0ba649170615658a1bcb97ea922126d16bed0b6b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637af45acc37a7a2c3ca6ce929b4671046476166442a11fc80d8f0bf90ecd868`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 6.5 MB (6484260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b2aff493c7a4b631188bf1e08800a5b7c4ff8c7b0a35d871d1e064b7b229f`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d157ed7867da0b76320ba85d657071b09d9648c20c89a328178ea46464e1b7`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:10c402d37b4e7ac39b9a3ae564dabb8171b6ebf57f29b2086adf5bf5bfc70452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69355e40015e4b8bba82c7bc204868461a260267941f8bfd4d8136e4c6d14f1a`

```dockerfile
```

-	Layers:
	-	`sha256:ae16ff4d4e58738b65ec2f42e2b394b9ef1c4cd8b294509afffaf0d3585aa2b0`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3d1385ecd165eeddcd5b60fe068d6cdf140ddcdc687af8e7544197e451b89be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4228daa974404161b0811acf95429df4a1c07f409613b14a22891f9d0229b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1f7a3c7b77c14f08c57f994d653a1573a628813f51ad57c8ffa6704eb1e7c`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 6.5 MB (6471695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133786e3c707b99368ea0262c4da45fbb457ff538f3e4245164f71c9d04ebcb3`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a93d5da73eaad0dceef4a853a5fda3e77ff002488070801a2e0df946562874`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b1a5520c26787b7b5b7598e8c6d32e04b6442246f45f51702f8ab9602311695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1d0f6677c8e2f5972add8fb8d56a1a1949d15ca4c27d662d5c221b9bb3987b`

```dockerfile
```

-	Layers:
	-	`sha256:91912f94323f40a81b369bdf7b31adec099387298167e8ee48fdbd643c54bbd7`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:77790b065a14aa640a9906611f2593849afbc24e3dfe9ea845191d6d6b2b9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715cd7234f00f3838f631d95b5ade02f3f069b16c157eed1908f21f1e0539245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ead951cdd1051dce5e434c83e45a7f8035db209e137743eadba8e07891ffdf`  
		Last Modified: Thu, 08 May 2025 17:14:47 GMT  
		Size: 6.3 MB (6260210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a94e80a2eaf0a11748ce4e055b47b3131f7bf07fbf5822a6684d7baaca7fe`  
		Last Modified: Thu, 08 May 2025 17:14:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedeae9f370d7774766d58004d8794999e8ee0270a3ace165434935b755ba4e1`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7be154f67a95eb115edaf3da2c42409d3cc505c20e23282796088eb999a488ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153445c3a76a150eac532c5d5e8be9663decfd6cc7f0abd49cfe93e6864c896`

```dockerfile
```

-	Layers:
	-	`sha256:11e95946e2efd0801ccd7e4d3c070b684baf2d8e019eb4eeacd52b28cbfd858f`  
		Last Modified: Thu, 01 May 2025 16:38:44 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:aeffcf1a5fd10a494bc66c184585616f260d480c74d5e5253b56d450a809146d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc14e50d0acbca9b182a873a3c80f9967dbb1442be773cba6ab4e8cfe17688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829f47e2f6c4e37799e70fe955cbec9218f793ba67d3c42843028581f41d46c`  
		Last Modified: Thu, 01 May 2025 16:39:04 GMT  
		Size: 6.2 MB (6239898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26d5042fdff67ea8c94d44aa8763edc52e021387e6d064673d469c2bc47275`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da66dedca6ed504a33045c53e38cc74882153eb3a260560fe268bb9d1b6c8e4`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:352c383d3b82380dbd9a1ac107937d3991846006be06142ba8698aa65c990a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54eb654e9afb7bbd3bf867ba6dfcbf287ad262569f86c0815723a5376118ac8`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d2cc36c0ae1fb4725dfc44754cc365298d189308b25b6a818f9373c56d8b5`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-alpine` - linux; s390x

```console
$ docker pull nats@sha256:2f0d53def59230c037431fb279d69f0aca7b8603e3ddc47716d6a629b7837c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacf064fa25d7454a1aaa536a529a948d63741e3c9dd839168560f8b02c79d3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9647734b695bae36f7e0c32edbeebd3cf169b841161c9d4c577a1ece6018`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 6.6 MB (6603836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652b02d0c60b9d62fa04ca56202b067023a35da376bc9a712492b39a4338579`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5a6d01daa3a734095f6be97aa9b7b10a347d019c52cbf4dfffca96bb55f8d6`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:46d9178ace4d9f9b7e8307fdf38c831b0130174836ad584ec872a1d86af216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59c14622147cf68ab22ed7eb89e630f31c7d3213c566032a73cc0b9918fa51`

```dockerfile
```

-	Layers:
	-	`sha256:1046c910412b33c1747ecde0dd3656153062c8e55cde48158e5aa2a7f3053e86`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.3-alpine3.21`

```console
$ docker pull nats@sha256:a79a6ff6e42ef41ef964c52bef9fe6eed02fc91cf348801e3dddbbd57636077a
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

### `nats:2.11.3-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:f6be324fcee27f2a91178d74f77bb4ba3e5a9d2e72ba7d6871f45d14aadca40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c567f7e9cb3bfc4d455ff826598a76a99a73fa13ec7367efaacf1e12c0dd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5d0247fe0c99cf6c1ecf760cd78e32964d3ddb3759704f6684937b17e5142`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 6.8 MB (6765302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b37c9588055ed3b254ae4ba53ef4c63f34fcc2aeab92b8475fcbcacfcd80b55`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe44b0610308731d27dd1e577ba8612ea42d8995d7543ffc050198010b94663`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6606e7bd2585dbedc93618630113f5655e877c1bd5dfc496a02e725e4a2fe9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e72e1fa9e878b2aba34410a32cef5eabe2a785ebf18d74b2b308387268ae11`

```dockerfile
```

-	Layers:
	-	`sha256:a096f4f7ad0e75fb3bf34e4f9cc376cccfe906466ff7158c5adcace3fc78d8eb`  
		Last Modified: Thu, 01 May 2025 16:39:11 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:10c04125727c8e5799732cbf4bb257a0be62ef4178a8305430c81e20d8c2e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9167a50c86fbbf9faacc0ba649170615658a1bcb97ea922126d16bed0b6b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637af45acc37a7a2c3ca6ce929b4671046476166442a11fc80d8f0bf90ecd868`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 6.5 MB (6484260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b2aff493c7a4b631188bf1e08800a5b7c4ff8c7b0a35d871d1e064b7b229f`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d157ed7867da0b76320ba85d657071b09d9648c20c89a328178ea46464e1b7`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:10c402d37b4e7ac39b9a3ae564dabb8171b6ebf57f29b2086adf5bf5bfc70452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69355e40015e4b8bba82c7bc204868461a260267941f8bfd4d8136e4c6d14f1a`

```dockerfile
```

-	Layers:
	-	`sha256:ae16ff4d4e58738b65ec2f42e2b394b9ef1c4cd8b294509afffaf0d3585aa2b0`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:3d1385ecd165eeddcd5b60fe068d6cdf140ddcdc687af8e7544197e451b89be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4228daa974404161b0811acf95429df4a1c07f409613b14a22891f9d0229b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1f7a3c7b77c14f08c57f994d653a1573a628813f51ad57c8ffa6704eb1e7c`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 6.5 MB (6471695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133786e3c707b99368ea0262c4da45fbb457ff538f3e4245164f71c9d04ebcb3`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a93d5da73eaad0dceef4a853a5fda3e77ff002488070801a2e0df946562874`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b1a5520c26787b7b5b7598e8c6d32e04b6442246f45f51702f8ab9602311695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1d0f6677c8e2f5972add8fb8d56a1a1949d15ca4c27d662d5c221b9bb3987b`

```dockerfile
```

-	Layers:
	-	`sha256:91912f94323f40a81b369bdf7b31adec099387298167e8ee48fdbd643c54bbd7`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:77790b065a14aa640a9906611f2593849afbc24e3dfe9ea845191d6d6b2b9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715cd7234f00f3838f631d95b5ade02f3f069b16c157eed1908f21f1e0539245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ead951cdd1051dce5e434c83e45a7f8035db209e137743eadba8e07891ffdf`  
		Last Modified: Thu, 08 May 2025 17:14:47 GMT  
		Size: 6.3 MB (6260210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a94e80a2eaf0a11748ce4e055b47b3131f7bf07fbf5822a6684d7baaca7fe`  
		Last Modified: Thu, 08 May 2025 17:14:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedeae9f370d7774766d58004d8794999e8ee0270a3ace165434935b755ba4e1`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:7be154f67a95eb115edaf3da2c42409d3cc505c20e23282796088eb999a488ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153445c3a76a150eac532c5d5e8be9663decfd6cc7f0abd49cfe93e6864c896`

```dockerfile
```

-	Layers:
	-	`sha256:11e95946e2efd0801ccd7e4d3c070b684baf2d8e019eb4eeacd52b28cbfd858f`  
		Last Modified: Thu, 01 May 2025 16:38:44 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:aeffcf1a5fd10a494bc66c184585616f260d480c74d5e5253b56d450a809146d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc14e50d0acbca9b182a873a3c80f9967dbb1442be773cba6ab4e8cfe17688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829f47e2f6c4e37799e70fe955cbec9218f793ba67d3c42843028581f41d46c`  
		Last Modified: Thu, 01 May 2025 16:39:04 GMT  
		Size: 6.2 MB (6239898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26d5042fdff67ea8c94d44aa8763edc52e021387e6d064673d469c2bc47275`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da66dedca6ed504a33045c53e38cc74882153eb3a260560fe268bb9d1b6c8e4`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:352c383d3b82380dbd9a1ac107937d3991846006be06142ba8698aa65c990a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54eb654e9afb7bbd3bf867ba6dfcbf287ad262569f86c0815723a5376118ac8`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d2cc36c0ae1fb4725dfc44754cc365298d189308b25b6a818f9373c56d8b5`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:2f0d53def59230c037431fb279d69f0aca7b8603e3ddc47716d6a629b7837c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacf064fa25d7454a1aaa536a529a948d63741e3c9dd839168560f8b02c79d3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9647734b695bae36f7e0c32edbeebd3cf169b841161c9d4c577a1ece6018`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 6.6 MB (6603836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652b02d0c60b9d62fa04ca56202b067023a35da376bc9a712492b39a4338579`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5a6d01daa3a734095f6be97aa9b7b10a347d019c52cbf4dfffca96bb55f8d6`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:46d9178ace4d9f9b7e8307fdf38c831b0130174836ad584ec872a1d86af216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59c14622147cf68ab22ed7eb89e630f31c7d3213c566032a73cc0b9918fa51`

```dockerfile
```

-	Layers:
	-	`sha256:1046c910412b33c1747ecde0dd3656153062c8e55cde48158e5aa2a7f3053e86`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.3-linux`

```console
$ docker pull nats@sha256:b14393862d9ba5aed718097fefbc0ab96f29dee8f3e91d9bc293b76a913dce3e
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

### `nats:2.11.3-linux` - linux; amd64

```console
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-linux` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.3-nanoserver`

```console
$ docker pull nats@sha256:a07df4097a4c1873483b76056063eb213f9ab0d0f6fd8ee605afdc6aa54b7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11.3-nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.3-nanoserver-1809`

```console
$ docker pull nats@sha256:a07df4097a4c1873483b76056063eb213f9ab0d0f6fd8ee605afdc6aa54b7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11.3-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.3-scratch`

```console
$ docker pull nats@sha256:b14393862d9ba5aed718097fefbc0ab96f29dee8f3e91d9bc293b76a913dce3e
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

### `nats:2.11.3-scratch` - linux; amd64

```console
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.3-scratch` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.3-windowsservercore`

```console
$ docker pull nats@sha256:430b604c3deba1df9281ce46d0f370f7eb006dc5b82dcba2db0db9d12aca8f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11.3-windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2c7c65263538bb027f22ec3c9b98be9de93b9fb8607794d8fcae9e7c099f014a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190866639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eda5d64d526aaf3ca69f70b5a7bebe2403fff0fa5385dacd8f5573909d612a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:00:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 21:00:23 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER=2.11.3
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.3/nats-server-v2.11.3-windows-amd64.zip
# Wed, 14 May 2025 21:00:25 GMT
ENV NATS_SERVER_SHASUM=553b61ad3581c28a93eb039f0167efc4470fb3ec3a5cff9570545eb5f57acf25
# Wed, 14 May 2025 21:01:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 21:01:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 21:01:38 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:01:39 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:01:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:01:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0ae011bb62d528ca9feb89e5812ff25ebe8c57772e044d4c488929899d089`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf68f22b1d09993c857196717ed40e9cb7137187950fac4d1314e1e71983dc`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0376a7d0c30827c309d390afdce9e1a185638d792e02cc7f6a3a618e3d77d145`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b424104a0f6fdad4cf32e6b1ea463948071a9f6281bb735a161545ab27497b`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f34380762d67935a8cf37e7afa8403df4a48589429bbffe6feee81ffd7b909`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ce307d87e99925c7a34c82120959f82f8fad23e831c4de345f631695149a1`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 325.3 KB (325291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38678459c07cd527b3ed295ec5f5224e17077ff707e9cdf6dc8d9997884bbf`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 6.8 MB (6811608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d854eedd2a7079826ab676fd665e341f97a277c29cb5b21da355d7b5cd71ab4f`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f204f830eae1b5ed87a5df94e9b2559d80612052d81ca1009f415f278bfa8b5e`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645b40626dba336c258c04ff62dfc043bc24e01c2cbbf3c82d084e449e2231a`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf65b00896e5230131bedb16fef3f1edb66ef2014a30d2c1b7e303f65dadc9c`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.3-windowsservercore-1809`

```console
$ docker pull nats@sha256:430b604c3deba1df9281ce46d0f370f7eb006dc5b82dcba2db0db9d12aca8f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:2.11.3-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2c7c65263538bb027f22ec3c9b98be9de93b9fb8607794d8fcae9e7c099f014a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190866639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eda5d64d526aaf3ca69f70b5a7bebe2403fff0fa5385dacd8f5573909d612a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:00:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 21:00:23 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER=2.11.3
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.3/nats-server-v2.11.3-windows-amd64.zip
# Wed, 14 May 2025 21:00:25 GMT
ENV NATS_SERVER_SHASUM=553b61ad3581c28a93eb039f0167efc4470fb3ec3a5cff9570545eb5f57acf25
# Wed, 14 May 2025 21:01:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 21:01:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 21:01:38 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:01:39 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:01:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:01:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0ae011bb62d528ca9feb89e5812ff25ebe8c57772e044d4c488929899d089`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf68f22b1d09993c857196717ed40e9cb7137187950fac4d1314e1e71983dc`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0376a7d0c30827c309d390afdce9e1a185638d792e02cc7f6a3a618e3d77d145`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b424104a0f6fdad4cf32e6b1ea463948071a9f6281bb735a161545ab27497b`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f34380762d67935a8cf37e7afa8403df4a48589429bbffe6feee81ffd7b909`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ce307d87e99925c7a34c82120959f82f8fad23e831c4de345f631695149a1`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 325.3 KB (325291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38678459c07cd527b3ed295ec5f5224e17077ff707e9cdf6dc8d9997884bbf`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 6.8 MB (6811608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d854eedd2a7079826ab676fd665e341f97a277c29cb5b21da355d7b5cd71ab4f`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f204f830eae1b5ed87a5df94e9b2559d80612052d81ca1009f415f278bfa8b5e`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645b40626dba336c258c04ff62dfc043bc24e01c2cbbf3c82d084e449e2231a`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf65b00896e5230131bedb16fef3f1edb66ef2014a30d2c1b7e303f65dadc9c`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:a79a6ff6e42ef41ef964c52bef9fe6eed02fc91cf348801e3dddbbd57636077a
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
$ docker pull nats@sha256:f6be324fcee27f2a91178d74f77bb4ba3e5a9d2e72ba7d6871f45d14aadca40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c567f7e9cb3bfc4d455ff826598a76a99a73fa13ec7367efaacf1e12c0dd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5d0247fe0c99cf6c1ecf760cd78e32964d3ddb3759704f6684937b17e5142`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 6.8 MB (6765302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b37c9588055ed3b254ae4ba53ef4c63f34fcc2aeab92b8475fcbcacfcd80b55`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe44b0610308731d27dd1e577ba8612ea42d8995d7543ffc050198010b94663`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6606e7bd2585dbedc93618630113f5655e877c1bd5dfc496a02e725e4a2fe9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e72e1fa9e878b2aba34410a32cef5eabe2a785ebf18d74b2b308387268ae11`

```dockerfile
```

-	Layers:
	-	`sha256:a096f4f7ad0e75fb3bf34e4f9cc376cccfe906466ff7158c5adcace3fc78d8eb`  
		Last Modified: Thu, 01 May 2025 16:39:11 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:10c04125727c8e5799732cbf4bb257a0be62ef4178a8305430c81e20d8c2e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9167a50c86fbbf9faacc0ba649170615658a1bcb97ea922126d16bed0b6b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637af45acc37a7a2c3ca6ce929b4671046476166442a11fc80d8f0bf90ecd868`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 6.5 MB (6484260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b2aff493c7a4b631188bf1e08800a5b7c4ff8c7b0a35d871d1e064b7b229f`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d157ed7867da0b76320ba85d657071b09d9648c20c89a328178ea46464e1b7`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:10c402d37b4e7ac39b9a3ae564dabb8171b6ebf57f29b2086adf5bf5bfc70452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69355e40015e4b8bba82c7bc204868461a260267941f8bfd4d8136e4c6d14f1a`

```dockerfile
```

-	Layers:
	-	`sha256:ae16ff4d4e58738b65ec2f42e2b394b9ef1c4cd8b294509afffaf0d3585aa2b0`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:3d1385ecd165eeddcd5b60fe068d6cdf140ddcdc687af8e7544197e451b89be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4228daa974404161b0811acf95429df4a1c07f409613b14a22891f9d0229b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1f7a3c7b77c14f08c57f994d653a1573a628813f51ad57c8ffa6704eb1e7c`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 6.5 MB (6471695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133786e3c707b99368ea0262c4da45fbb457ff538f3e4245164f71c9d04ebcb3`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a93d5da73eaad0dceef4a853a5fda3e77ff002488070801a2e0df946562874`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b1a5520c26787b7b5b7598e8c6d32e04b6442246f45f51702f8ab9602311695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1d0f6677c8e2f5972add8fb8d56a1a1949d15ca4c27d662d5c221b9bb3987b`

```dockerfile
```

-	Layers:
	-	`sha256:91912f94323f40a81b369bdf7b31adec099387298167e8ee48fdbd643c54bbd7`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:77790b065a14aa640a9906611f2593849afbc24e3dfe9ea845191d6d6b2b9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715cd7234f00f3838f631d95b5ade02f3f069b16c157eed1908f21f1e0539245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ead951cdd1051dce5e434c83e45a7f8035db209e137743eadba8e07891ffdf`  
		Last Modified: Thu, 08 May 2025 17:14:47 GMT  
		Size: 6.3 MB (6260210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a94e80a2eaf0a11748ce4e055b47b3131f7bf07fbf5822a6684d7baaca7fe`  
		Last Modified: Thu, 08 May 2025 17:14:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedeae9f370d7774766d58004d8794999e8ee0270a3ace165434935b755ba4e1`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7be154f67a95eb115edaf3da2c42409d3cc505c20e23282796088eb999a488ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153445c3a76a150eac532c5d5e8be9663decfd6cc7f0abd49cfe93e6864c896`

```dockerfile
```

-	Layers:
	-	`sha256:11e95946e2efd0801ccd7e4d3c070b684baf2d8e019eb4eeacd52b28cbfd858f`  
		Last Modified: Thu, 01 May 2025 16:38:44 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:aeffcf1a5fd10a494bc66c184585616f260d480c74d5e5253b56d450a809146d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc14e50d0acbca9b182a873a3c80f9967dbb1442be773cba6ab4e8cfe17688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829f47e2f6c4e37799e70fe955cbec9218f793ba67d3c42843028581f41d46c`  
		Last Modified: Thu, 01 May 2025 16:39:04 GMT  
		Size: 6.2 MB (6239898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26d5042fdff67ea8c94d44aa8763edc52e021387e6d064673d469c2bc47275`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da66dedca6ed504a33045c53e38cc74882153eb3a260560fe268bb9d1b6c8e4`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:352c383d3b82380dbd9a1ac107937d3991846006be06142ba8698aa65c990a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54eb654e9afb7bbd3bf867ba6dfcbf287ad262569f86c0815723a5376118ac8`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d2cc36c0ae1fb4725dfc44754cc365298d189308b25b6a818f9373c56d8b5`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:2f0d53def59230c037431fb279d69f0aca7b8603e3ddc47716d6a629b7837c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacf064fa25d7454a1aaa536a529a948d63741e3c9dd839168560f8b02c79d3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9647734b695bae36f7e0c32edbeebd3cf169b841161c9d4c577a1ece6018`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 6.6 MB (6603836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652b02d0c60b9d62fa04ca56202b067023a35da376bc9a712492b39a4338579`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5a6d01daa3a734095f6be97aa9b7b10a347d019c52cbf4dfffca96bb55f8d6`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:46d9178ace4d9f9b7e8307fdf38c831b0130174836ad584ec872a1d86af216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59c14622147cf68ab22ed7eb89e630f31c7d3213c566032a73cc0b9918fa51`

```dockerfile
```

-	Layers:
	-	`sha256:1046c910412b33c1747ecde0dd3656153062c8e55cde48158e5aa2a7f3053e86`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:a79a6ff6e42ef41ef964c52bef9fe6eed02fc91cf348801e3dddbbd57636077a
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

### `nats:alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:f6be324fcee27f2a91178d74f77bb4ba3e5a9d2e72ba7d6871f45d14aadca40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c567f7e9cb3bfc4d455ff826598a76a99a73fa13ec7367efaacf1e12c0dd45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5d0247fe0c99cf6c1ecf760cd78e32964d3ddb3759704f6684937b17e5142`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 6.8 MB (6765302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b37c9588055ed3b254ae4ba53ef4c63f34fcc2aeab92b8475fcbcacfcd80b55`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe44b0610308731d27dd1e577ba8612ea42d8995d7543ffc050198010b94663`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6606e7bd2585dbedc93618630113f5655e877c1bd5dfc496a02e725e4a2fe9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e72e1fa9e878b2aba34410a32cef5eabe2a785ebf18d74b2b308387268ae11`

```dockerfile
```

-	Layers:
	-	`sha256:a096f4f7ad0e75fb3bf34e4f9cc376cccfe906466ff7158c5adcace3fc78d8eb`  
		Last Modified: Thu, 01 May 2025 16:39:11 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:10c04125727c8e5799732cbf4bb257a0be62ef4178a8305430c81e20d8c2e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9167a50c86fbbf9faacc0ba649170615658a1bcb97ea922126d16bed0b6b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637af45acc37a7a2c3ca6ce929b4671046476166442a11fc80d8f0bf90ecd868`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 6.5 MB (6484260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b2aff493c7a4b631188bf1e08800a5b7c4ff8c7b0a35d871d1e064b7b229f`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d157ed7867da0b76320ba85d657071b09d9648c20c89a328178ea46464e1b7`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:10c402d37b4e7ac39b9a3ae564dabb8171b6ebf57f29b2086adf5bf5bfc70452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69355e40015e4b8bba82c7bc204868461a260267941f8bfd4d8136e4c6d14f1a`

```dockerfile
```

-	Layers:
	-	`sha256:ae16ff4d4e58738b65ec2f42e2b394b9ef1c4cd8b294509afffaf0d3585aa2b0`  
		Last Modified: Thu, 01 May 2025 16:38:41 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:3d1385ecd165eeddcd5b60fe068d6cdf140ddcdc687af8e7544197e451b89be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4228daa974404161b0811acf95429df4a1c07f409613b14a22891f9d0229b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f1f7a3c7b77c14f08c57f994d653a1573a628813f51ad57c8ffa6704eb1e7c`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 6.5 MB (6471695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133786e3c707b99368ea0262c4da45fbb457ff538f3e4245164f71c9d04ebcb3`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a93d5da73eaad0dceef4a853a5fda3e77ff002488070801a2e0df946562874`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b1a5520c26787b7b5b7598e8c6d32e04b6442246f45f51702f8ab9602311695e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1d0f6677c8e2f5972add8fb8d56a1a1949d15ca4c27d662d5c221b9bb3987b`

```dockerfile
```

-	Layers:
	-	`sha256:91912f94323f40a81b369bdf7b31adec099387298167e8ee48fdbd643c54bbd7`  
		Last Modified: Thu, 01 May 2025 16:38:40 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:77790b065a14aa640a9906611f2593849afbc24e3dfe9ea845191d6d6b2b9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715cd7234f00f3838f631d95b5ade02f3f069b16c157eed1908f21f1e0539245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ead951cdd1051dce5e434c83e45a7f8035db209e137743eadba8e07891ffdf`  
		Last Modified: Thu, 08 May 2025 17:14:47 GMT  
		Size: 6.3 MB (6260210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a94e80a2eaf0a11748ce4e055b47b3131f7bf07fbf5822a6684d7baaca7fe`  
		Last Modified: Thu, 08 May 2025 17:14:44 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedeae9f370d7774766d58004d8794999e8ee0270a3ace165434935b755ba4e1`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:7be154f67a95eb115edaf3da2c42409d3cc505c20e23282796088eb999a488ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153445c3a76a150eac532c5d5e8be9663decfd6cc7f0abd49cfe93e6864c896`

```dockerfile
```

-	Layers:
	-	`sha256:11e95946e2efd0801ccd7e4d3c070b684baf2d8e019eb4eeacd52b28cbfd858f`  
		Last Modified: Thu, 01 May 2025 16:38:44 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:aeffcf1a5fd10a494bc66c184585616f260d480c74d5e5253b56d450a809146d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadc14e50d0acbca9b182a873a3c80f9967dbb1442be773cba6ab4e8cfe17688`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7829f47e2f6c4e37799e70fe955cbec9218f793ba67d3c42843028581f41d46c`  
		Last Modified: Thu, 01 May 2025 16:39:04 GMT  
		Size: 6.2 MB (6239898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26d5042fdff67ea8c94d44aa8763edc52e021387e6d064673d469c2bc47275`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da66dedca6ed504a33045c53e38cc74882153eb3a260560fe268bb9d1b6c8e4`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:352c383d3b82380dbd9a1ac107937d3991846006be06142ba8698aa65c990a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54eb654e9afb7bbd3bf867ba6dfcbf287ad262569f86c0815723a5376118ac8`

```dockerfile
```

-	Layers:
	-	`sha256:6b0d2cc36c0ae1fb4725dfc44754cc365298d189308b25b6a818f9373c56d8b5`  
		Last Modified: Thu, 01 May 2025 16:39:03 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:2f0d53def59230c037431fb279d69f0aca7b8603e3ddc47716d6a629b7837c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacf064fa25d7454a1aaa536a529a948d63741e3c9dd839168560f8b02c79d3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 01 May 2025 10:58:11 GMT
ENV NATS_SERVER=2.11.3
# Thu, 01 May 2025 10:58:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='24a56aa64219aa6668a18e2d0ea9108d72472852e47677b384c856fc412ae4c7' ;; 		armhf) natsArch='arm6'; sha256='86fe21d7413b6c7ce68250c0645567b0550eacf2a18eea56374630c83f0f1a76' ;; 		armv7) natsArch='arm7'; sha256='1832b4f0e105a01b0366ea2e3071aa235870067f0d042db2ff4dfdb6ceb673a8' ;; 		x86_64) natsArch='amd64'; sha256='9cdab8b2e2488128caee6519e2f15f1aa33a78b4386ee1776a06b4818d7ec197' ;; 		x86) natsArch='386'; sha256='9173707ded6d71210c5e0eb9a29f3979888a7e658d52cb8fe32b7e498a852143' ;; 		s390x) natsArch='s390x'; sha256='61de816adafa99fbe7130ee77a350fd44f7c97c51bc28a210e0a53c0ced1621f' ;; 		ppc64le) natsArch='ppc64le'; sha256='5b1a2ea2bcd68d0751dd718ce434a7c57161415c202e5723191891360b1e5fd7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fe9647734b695bae36f7e0c32edbeebd3cf169b841161c9d4c577a1ece6018`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 6.6 MB (6603836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652b02d0c60b9d62fa04ca56202b067023a35da376bc9a712492b39a4338579`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5a6d01daa3a734095f6be97aa9b7b10a347d019c52cbf4dfffca96bb55f8d6`  
		Last Modified: Fri, 09 May 2025 11:59:46 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:46d9178ace4d9f9b7e8307fdf38c831b0130174836ad584ec872a1d86af216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f59c14622147cf68ab22ed7eb89e630f31c7d3213c566032a73cc0b9918fa51`

```dockerfile
```

-	Layers:
	-	`sha256:1046c910412b33c1747ecde0dd3656153062c8e55cde48158e5aa2a7f3053e86`  
		Last Modified: Thu, 01 May 2025 16:40:06 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:3072e8ea890fe66b5921f75c1385b5f49b59a7f46171d697517d186830131fa7
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
	-	windows version 10.0.17763.7314; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:b14393862d9ba5aed718097fefbc0ab96f29dee8f3e91d9bc293b76a913dce3e
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
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:a07df4097a4c1873483b76056063eb213f9ab0d0f6fd8ee605afdc6aa54b7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:nanoserver` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:a07df4097a4c1873483b76056063eb213f9ab0d0f6fd8ee605afdc6aa54b7dbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:642d8ac9e0f7bc76792c08a25b9cacf71d116f1fc48701d53e0b036972d7f948
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115265569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9784848fd15a61547f896c95456c69a4624a5ccfa6f84f14f47b55784e7b4294`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 21:16:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:597800b942878c0dcccccdeec13566a54f5747a8b41cbc437b6c383be7c26c87 in C:\nats-server.exe 
# Wed, 14 May 2025 21:16:25 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:16:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:16:27 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Thu, 15 May 2025 19:27:12 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad300c79b9fb6f66461ded839672cf5492f7b7af1319ba6344cb0f67263cfaa`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2d6584ea4f816da9da1b5bde7348f1a160d02be028974fdec19ec192f9658c`  
		Last Modified: Wed, 14 May 2025 21:16:31 GMT  
		Size: 6.5 MB (6478829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e50007f7d9408bcf642455e42c149e2cf2daa0055501cd7dae3b7667d00cd6`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71cf377f3df963a9df597c52163edb65f2c3248bf2de4f778ff73143482f0ad`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2abb8e2da4d28cdfdade0dc0170836c44ba60c406a99fb05c0a8625b2a455`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ed03abb4afa45ed75da236ad6dbc36cce574ce5dfb494e488e44f5f1e4ef4a`  
		Last Modified: Wed, 14 May 2025 21:16:30 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:b14393862d9ba5aed718097fefbc0ab96f29dee8f3e91d9bc293b76a913dce3e
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
$ docker pull nats@sha256:458160f855bc40f8b6283873c77cd2b742e3d715a295adae385a9637f592b38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849b928de1527bbe219d64ab22a1d69ee0e488e3c0af8d7dc9fa6759331e4a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3711a19759dd9b1ccf103e6c33930d841575852cedc78315de00cd9cd8dc91`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 6.3 MB (6305589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f38f3d491599103f72a53ae2f51c6993a4795929948b3ba32dd6758fb8c7d`  
		Last Modified: Thu, 08 May 2025 17:05:09 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a065a38037bd4b448f287fa25bf67929e3b523b6506995191cd2c684246bbd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4896d55afbe1e8385cf782927695e96c2f68aca23dc64bf5ee04ec4ee9325ffc`

```dockerfile
```

-	Layers:
	-	`sha256:7694815e52b11475c2de15cf80b221e609ad5b6d1c6a2069e8a699d076045c5f`  
		Last Modified: Thu, 08 May 2025 22:53:36 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4bdebef03708d5444b287ef5b1c778bd7b72ba10fd8869ae89f07b6721a2c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256090245eb70862de1534b41cca4d1d4a7c481374fb3a8b07651b34b228bc97`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0643d544801ad51152c2a82bf05db8b8b6dcccef04a5d6998f1984261fd89a69`  
		Last Modified: Thu, 08 May 2025 22:53:41 GMT  
		Size: 6.0 MB (6020433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec7442cd987c384de00872594230b26d82513a92848aa0adb7284ea2a4d8315`  
		Last Modified: Thu, 08 May 2025 22:53:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9705999d828ce89e0d55ba3227fd89bcf5d285adb2d6406dfc48a25690fa5a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99e2ce213ec8e9fccee9d33c8c57d63d989647f0d130aab110a9cc261e24ba7`

```dockerfile
```

-	Layers:
	-	`sha256:a2535cfda40f54e2d026e6921763a73d37beafefe586b03da04c4ccc4790f37f`  
		Last Modified: Thu, 08 May 2025 22:53:44 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:7394c273c09fd456f14468d79a1a55ef446ae6855b7ffa83d5f9e0af2150d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7ad65223869dda2be03fa1efa4b1b19fb161ed3404d4ce430aecdb070c8cf5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d2b43118d0ba30e91ba6df99c7526f966392bbbd4cb077618cd0c6550473e617`  
		Last Modified: Thu, 08 May 2025 22:53:50 GMT  
		Size: 6.0 MB (6011430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5cfa7b21217954eb7baaa94d2cab35453ffe42a652f181ebd1c8db918696e`  
		Last Modified: Thu, 08 May 2025 22:53:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:642b1b53acc235c25773e03837ef49a41d778b54b9a46993b3d9f2260d6cc4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e030d4bca2c8250fbe600a622bed18e59d7990ea4e164a859dc3e16c8278a44`

```dockerfile
```

-	Layers:
	-	`sha256:a2ec37944b94cb42acf8fccd1e264c326be5047ddba31b6d78d779d873df8733`  
		Last Modified: Thu, 08 May 2025 22:53:53 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:34f5e709e346b49096606c518df397d7ac4872cf5b5d4671efb9a6467acfea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c310645196d2f0aecf3c61d942cfeefcd0eea3550389ce32e1873dcbd5b83e1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba48198a1bced15d74c6e4047520381e1897e248157f58b1be1b1246e47cf1dd`  
		Last Modified: Thu, 08 May 2025 17:10:01 GMT  
		Size: 5.8 MB (5795961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1da3cab88c69bda5cd205aa86b1fa4e4e52e71bdf0a67731d029ca831acb7`  
		Last Modified: Thu, 08 May 2025 17:09:59 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:547bc2e62a92b151be17b883016a2c672d858912663d54f704a94e9cd8644908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb4eac0a9e2ce33a2f9dff770acd52341a5100e65fba6d643768e9bbc38e43a`

```dockerfile
```

-	Layers:
	-	`sha256:d24755c729ee82fdb4323b59df0776dcd009ae2db4ad8e1b2ad03edb4a58719c`  
		Last Modified: Thu, 08 May 2025 22:54:01 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fa63abf98c3203251e68c47f9dc3f86e3eb4a320b7cc6c3c5fcab8dd85b623c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5776199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ace0ef39867c11531bcd7c2ef86e2a8a4cbfc52fcfda176f19b7cf1d0cd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b419816d4c4f127836b2ffaa7214b9d7eddd180870f7657ac031b4d75f6658d3`  
		Last Modified: Thu, 08 May 2025 22:54:07 GMT  
		Size: 5.8 MB (5775689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b80f067a8a7829f802bfa77f107358728683934af115a104d124d7b0c52b`  
		Last Modified: Thu, 08 May 2025 22:54:06 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b513e7dcd16551d7b851b646a9e14f376f478adc55395a2f3c92f6def18c7965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973b9adecbedfa4e368d44d1265d2bc96ec167084d1f5745a3ef0b119e275b21`

```dockerfile
```

-	Layers:
	-	`sha256:766275ce24032a30734315e25c6546689f03ed2b04136eb5fce673b3b689d546`  
		Last Modified: Thu, 08 May 2025 22:54:10 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:e18c7dc55b95480aae451b286c1131fceb1459b3f755ece290a2d8148c6509ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d57d4d75c6c1bf07b50686bd980399fd495381624b7c58416e0c788b2ba7e71`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 01 May 2025 10:58:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 01 May 2025 10:58:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 01 May 2025 10:58:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 01 May 2025 10:58:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 01 May 2025 10:58:11 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 01 May 2025 10:58:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5e00dbdbe1a95dcf3abdface4d1bf59135f6f2881e1f30b47f67ad9c9587d3a6`  
		Last Modified: Thu, 08 May 2025 22:54:15 GMT  
		Size: 6.1 MB (6142598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5f79aea173f85bf064a725a7207a90f4b8ae5f546538f0a8081381fbeb449a`  
		Last Modified: Thu, 08 May 2025 22:54:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c1a600806078b42c80fd272b0752a7554337194c9225bbe260462fc8819cdd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bec08fec82a7b4747cf2d83a4753043018563a4cf594fc80a85122e11524b7`

```dockerfile
```

-	Layers:
	-	`sha256:2fdba41aa3a5bd616080baa79e80364fba5ec79520bff02667c59c95a865ce52`  
		Last Modified: Thu, 08 May 2025 22:54:19 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:430b604c3deba1df9281ce46d0f370f7eb006dc5b82dcba2db0db9d12aca8f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:windowsservercore` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2c7c65263538bb027f22ec3c9b98be9de93b9fb8607794d8fcae9e7c099f014a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190866639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eda5d64d526aaf3ca69f70b5a7bebe2403fff0fa5385dacd8f5573909d612a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:00:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 21:00:23 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER=2.11.3
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.3/nats-server-v2.11.3-windows-amd64.zip
# Wed, 14 May 2025 21:00:25 GMT
ENV NATS_SERVER_SHASUM=553b61ad3581c28a93eb039f0167efc4470fb3ec3a5cff9570545eb5f57acf25
# Wed, 14 May 2025 21:01:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 21:01:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 21:01:38 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:01:39 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:01:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:01:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0ae011bb62d528ca9feb89e5812ff25ebe8c57772e044d4c488929899d089`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf68f22b1d09993c857196717ed40e9cb7137187950fac4d1314e1e71983dc`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0376a7d0c30827c309d390afdce9e1a185638d792e02cc7f6a3a618e3d77d145`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b424104a0f6fdad4cf32e6b1ea463948071a9f6281bb735a161545ab27497b`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f34380762d67935a8cf37e7afa8403df4a48589429bbffe6feee81ffd7b909`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ce307d87e99925c7a34c82120959f82f8fad23e831c4de345f631695149a1`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 325.3 KB (325291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38678459c07cd527b3ed295ec5f5224e17077ff707e9cdf6dc8d9997884bbf`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 6.8 MB (6811608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d854eedd2a7079826ab676fd665e341f97a277c29cb5b21da355d7b5cd71ab4f`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f204f830eae1b5ed87a5df94e9b2559d80612052d81ca1009f415f278bfa8b5e`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645b40626dba336c258c04ff62dfc043bc24e01c2cbbf3c82d084e449e2231a`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf65b00896e5230131bedb16fef3f1edb66ef2014a30d2c1b7e303f65dadc9c`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:430b604c3deba1df9281ce46d0f370f7eb006dc5b82dcba2db0db9d12aca8f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull nats@sha256:2c7c65263538bb027f22ec3c9b98be9de93b9fb8607794d8fcae9e7c099f014a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190866639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eda5d64d526aaf3ca69f70b5a7bebe2403fff0fa5385dacd8f5573909d612a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:00:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 21:00:23 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER=2.11.3
# Wed, 14 May 2025 21:00:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.3/nats-server-v2.11.3-windows-amd64.zip
# Wed, 14 May 2025 21:00:25 GMT
ENV NATS_SERVER_SHASUM=553b61ad3581c28a93eb039f0167efc4470fb3ec3a5cff9570545eb5f57acf25
# Wed, 14 May 2025 21:01:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 May 2025 21:01:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 14 May 2025 21:01:38 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Wed, 14 May 2025 21:01:39 GMT
EXPOSE 4222 6222 8222
# Wed, 14 May 2025 21:01:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 14 May 2025 21:01:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0ae011bb62d528ca9feb89e5812ff25ebe8c57772e044d4c488929899d089`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cf68f22b1d09993c857196717ed40e9cb7137187950fac4d1314e1e71983dc`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0376a7d0c30827c309d390afdce9e1a185638d792e02cc7f6a3a618e3d77d145`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b424104a0f6fdad4cf32e6b1ea463948071a9f6281bb735a161545ab27497b`  
		Last Modified: Wed, 14 May 2025 21:01:44 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f34380762d67935a8cf37e7afa8403df4a48589429bbffe6feee81ffd7b909`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854ce307d87e99925c7a34c82120959f82f8fad23e831c4de345f631695149a1`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 325.3 KB (325291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38678459c07cd527b3ed295ec5f5224e17077ff707e9cdf6dc8d9997884bbf`  
		Last Modified: Wed, 14 May 2025 21:01:43 GMT  
		Size: 6.8 MB (6811608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d854eedd2a7079826ab676fd665e341f97a277c29cb5b21da355d7b5cd71ab4f`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f204f830eae1b5ed87a5df94e9b2559d80612052d81ca1009f415f278bfa8b5e`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645b40626dba336c258c04ff62dfc043bc24e01c2cbbf3c82d084e449e2231a`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf65b00896e5230131bedb16fef3f1edb66ef2014a30d2c1b7e303f65dadc9c`  
		Last Modified: Wed, 14 May 2025 21:01:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
