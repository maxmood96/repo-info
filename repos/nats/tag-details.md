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
$ docker pull nats@sha256:c234638526f0632617be436a8ea399a11214bb7579372d57060cb2a52d731d4e
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
	-	windows version 10.0.17763.7249; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:62b20bb99cf963ee9b0c78e26380a78a7dfa12eb8516d93bcf16b1f7eef252ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6305886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff853eebff5ea1827f264f2e22732dc892275c5bcd973db5058f4c4f0fe847e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d047c65ec95267487af401e091602880c16619e1ad4da3e7e962e8273ad589f3`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.3 MB (6305377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d3015f0a3ad1a5fecef389bb3fad1f3c80a49cbc71a62ab8d7db7516772ee`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:d6c4492d078b6bd4aeba68dd433b2a71adcb56e2e389703dc6af3f8a5af646ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663437ee61b0867cdc6f83e65e7751bb848af12bf9ccb7704573df8e32e95bd`

```dockerfile
```

-	Layers:
	-	`sha256:3d12f58e08eefe61f0ba37c703f5646cf255aac6449a7c65b2b43f5a7bacb48f`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:102aa9adbc4a30a8bab821dd4d77d548b6ea7a12f339b04a5f1c31747eca7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd05d7ce42a7ec76ac0d22af9a9659a44dca6a1cf2d735cd27fde215a0db0506`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:500b76d02a1b23c604281d5c714a2c35e9bb75cc592a66e885e0f5a6e37f01f7`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.0 MB (6019989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5024945048c8d9454d3d901d804208e05dee841a927428da15b56f6cda2dfe0f`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f4642d3b2d1c595bd38ad079f450119842676b9c767451642ba468377601232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4adb1d0380f2178fe3652a824902cb41144dc0865ce28afe86223e2ddffd7`

```dockerfile
```

-	Layers:
	-	`sha256:f45013d27d687c2029f50a853a6baa027e4a22520d0eebd6226cf9f5c6dc409b`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:ea87c80ec3b41d7c75130d62bcef1a297124c3a88d268381ab2c37ba307d73ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c48211b5750cd5af18bc0f8b0cb7210dc7b7442b3dddff32f3ed46470a2da8c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ddc6cab03365e07f2c6d7f059130a7dc282d4412f564e8e2c0df08c8bc73b654`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.0 MB (6011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c437fd34339124b6d3297d0074974f27d9c07d30fe42d04fb34c41bef2c43d`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:fffc88ae5d459abcedbd5c5d7e5f8d19b8794c52ca6188ca9f0c52afb76757d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add82b13529e611ce4c97b4933e0e140c7f8ebd67c1b6fc44ab3f06b3251fe1`

```dockerfile
```

-	Layers:
	-	`sha256:12a9e12b0405328b67372116138c73054a00281115d2f51f53d6ab18acd37481`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5af5adb666cd46b7cd6eaa3475636fd706a459a4c271c2bae0f663afa2e456d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f919a929c1e17f23640fb47e0fc43b05ad1b484c6197cad307207530716bd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84272a2e628924f03610b8c1c3c6e85b489ac87f290d0f685882def49de9ecd1`  
		Last Modified: Fri, 25 Apr 2025 09:28:47 GMT  
		Size: 5.8 MB (5796146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755f468e87f12862403c7a2d37f55dff1372e29f88136c0ba50bff80618988d`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:ae261bb9805c736ed0d01a8af3f50ba6b75cd32b8a61a30bab0f3f38a7ad3397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f774c66ce1e2de4b74c2b0932ded1d5e97875334f0b5addf36ec617bdfcac`

```dockerfile
```

-	Layers:
	-	`sha256:6530cb0c6d8f35499127965fc373643eb042bd0291136f4fd82e137888b9cc27`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:f19a5e664bc3140ac051b51ff581345afc3974ca87e4377e64bcbbef2fc7837d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f90ce596ba2b9ffbe8c3d7836d7557f80f2eff80976acbda88bd45337bba78c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:edd6d59c7e29dc4aedef9eaa0785a9ced8aff83bf96b1f830e36dfa46f53be68`  
		Last Modified: Fri, 25 Apr 2025 09:28:46 GMT  
		Size: 5.8 MB (5775437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b27a2c43cc9286a86142e9071ba262afa4ac6a97ee4607fc43fa7f71ad97bc`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:a758d3a359b53da7c6fed233fe42ef45b42a0dcd90f901aaa06a8d7c4b4f9590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605196d61046805754dda3246312272f529b7bd6a95a6b62b1e216d706c9f69`

```dockerfile
```

-	Layers:
	-	`sha256:9ce5dab5019211eb3c4213657f39f0272e6a0e24a6bfbbf1980a7fbd9a5bc11b`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:dea1543c1392e56a44b03ee62f370fc7bfbadb871a4387ae8fe199ec98a3ff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5035eb69783eaf7b9b82362cf68d01382ec0f326297e8878be99af8f9871e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1a8280710dc7fc73564b9f4f49fd6b32365882791aa95344c40d406b0a13f25`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.1 MB (6142593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033cc57448f08a332bf30589df2ea6255c2b00b7b7c31da4e1663a19dc06c9b`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:9703f39141dc639788e95d00bfec218510dc9f2ab474dbb78470e2bc476212d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de3562e8db441250ba64bd95bc8b554fde7b751d0a567b223d312c5eaab6e00`

```dockerfile
```

-	Layers:
	-	`sha256:e260a2ca5c98ebac8d27b48ad48bdc5e6293498718316b387e725d6fed20cdf7`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de296657002e12709da3c23acf58143be37a698131dc288d4cc2c0309d43f108
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb13670aa8a73fbb2b50a99b8f822097b91002c77c9e1a26d7b154316e88ca0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:16:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:16:26 GMT
RUN cmd /S /C #(nop) COPY file:5e3840af0e267b510d2e54914f636d4b01f954b096bf81d459cc821ca4b3b468 in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b95fc9f036b2ce06ef6f75c0142446cf388b3fba5797ae076811cae5833b6`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be78d14ed5a916b3852e5c5b8f0c11c5ec282c35d533f16824dff33610aa794`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 6.5 MB (6479002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4903b008a32f8cb1eec6d3c17a357bb5a5292b67abdefef767f778101422a266`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48da8f54d5ccf3ef130af0a73b7b96919c2914ff036e75afef02bdbaa3434ad`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2a11075603c8b13618e5c581a166f4c1092208a1e0b6f6a1cd1cdd3e4d05d`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602c735353ba767b46b959a65eed16ad8ad55667c0a070c399b925fa4c2fea6`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:d66042bb0f58546eb0e075e0e09cfd8030c31775d48c4396d2b12aed8b5ba8dc
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
$ docker pull nats@sha256:cc459c48ef61cac3f0da86a77a704def265e4fff6cdeb187fff4809b25134243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b192c13111c95d3650c60ba63ec639b3b9ff0de658743bbe316c2c40ec87761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30972518cedbab8035d013f6db6bcf5c288a5fce5ac9f5c4a49ca2e2ff162a24`  
		Last Modified: Fri, 25 Apr 2025 17:48:19 GMT  
		Size: 6.8 MB (6765181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43044524251b03418bed238109a3814f628cc30699f91fc8ddb4e61d21600845`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11478db0daa336af1fe1f03f4d426ddc8348dfee6453c3739caf888706524ec2`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:117e29392d3bb1664288874dc5ce1a6743cefeb606a6586a2b6f1a800565b719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b540eafd19924a51341d6c7da202445ebab34b94b7cd9d88bb0c9c94fab48451`

```dockerfile
```

-	Layers:
	-	`sha256:43064c2c8a3ae9f3aee5a2655ad540820779e43c1ae8d89fe53fc27519ab0285`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:46fbf055d62fb4755f9183a500aadc9c4b044c87f5ce88626f2e1e1a986f0d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e3ef175b500d95e0c5dc1df1ba06def48741be20ac7f639752862b21a65093`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c836485cdab40ee18791138507d840e61a5dd6002da521973ae9f747f9cb341`  
		Last Modified: Fri, 25 Apr 2025 17:52:20 GMT  
		Size: 6.5 MB (6471410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3594a7da4ff92a9abd27dc550a385c8bbeb5e28fabc967958775a3df2a0f96`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d68568eb773d06ed29e95f236f5900e0f575a70c3ee006c543384607da0b11`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9d34bfb1916f9e9afecb9491c2e54a28cad04787d7b5e9317ee15100d051beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2490b80fcdf37dc28c990ea6049540776446b9c0973f77f88086356465f5cc0`

```dockerfile
```

-	Layers:
	-	`sha256:1b506a0fb93e704e1d6a0dbbac29ebc8f1dfb3cd813dd0f139df51422cc09052`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7aed6760d32ff60522af0fe9dbbf411bb35f190c908dd34c2e1c35918070388a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155e98f2eedb665b03ec44e3975582a728961e440a725c0f69f690fff44568db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a64ee773ee396bff692796312d9b7dcc7fb44f952d2c908b4d376f16d9581d`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 6.2 MB (6239702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af4a70c73af05cb86c61280f805804a2f0ace4ab434db07169117ce347ae30b`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1084beee85752d4193e9e16db34006162f5878a5031f7b0e7c7e5c80b8c6f27`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c691956323d34a6b74e2dfbe1ab1bab5de30fe964ff714970639a2a122dc0e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bba8ffd862cccff6f4f84b00f8c0f1017110269d10624b18160c9ce2909636`

```dockerfile
```

-	Layers:
	-	`sha256:39f5fb5aec21d1cc18c2b4652236b54c02c55583eafa99d8c1d100f42ea99352`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:5689e34a9410f0b3a43f78ac470d2064ad40e49d1f6dc79eeb818bd41a7be3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288603c30be026199e52b513d137fd803edbb3bae2c21940fd3ab4a9565d29bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776b5dd8bbdaa374387b6347dd990a3afb1db9fd111c9542ff347efb9e8e262`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 6.6 MB (6603909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b72da8f217ee883d534bf8b81b4968bfe98d01195019acf154437d744a24a30`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02335cc369df4703ddd8bc4151583583c53a1490c756e6665be8d4bf73e9232c`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b984b0eb744f6b7b434f640a3c00e4c0d780f4ec952703fd4369cbecbd8764f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0b39651391cbc684b373c09fe28338c152436a70a949d8a2ded08402f8fff2`

```dockerfile
```

-	Layers:
	-	`sha256:ae85806ecae7c531d7315c6ecefafc450b8facf67c31d55c74ace2c47cb0aa46`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:d66042bb0f58546eb0e075e0e09cfd8030c31775d48c4396d2b12aed8b5ba8dc
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
$ docker pull nats@sha256:cc459c48ef61cac3f0da86a77a704def265e4fff6cdeb187fff4809b25134243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b192c13111c95d3650c60ba63ec639b3b9ff0de658743bbe316c2c40ec87761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30972518cedbab8035d013f6db6bcf5c288a5fce5ac9f5c4a49ca2e2ff162a24`  
		Last Modified: Fri, 25 Apr 2025 17:48:19 GMT  
		Size: 6.8 MB (6765181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43044524251b03418bed238109a3814f628cc30699f91fc8ddb4e61d21600845`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11478db0daa336af1fe1f03f4d426ddc8348dfee6453c3739caf888706524ec2`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:117e29392d3bb1664288874dc5ce1a6743cefeb606a6586a2b6f1a800565b719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b540eafd19924a51341d6c7da202445ebab34b94b7cd9d88bb0c9c94fab48451`

```dockerfile
```

-	Layers:
	-	`sha256:43064c2c8a3ae9f3aee5a2655ad540820779e43c1ae8d89fe53fc27519ab0285`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:46fbf055d62fb4755f9183a500aadc9c4b044c87f5ce88626f2e1e1a986f0d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e3ef175b500d95e0c5dc1df1ba06def48741be20ac7f639752862b21a65093`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c836485cdab40ee18791138507d840e61a5dd6002da521973ae9f747f9cb341`  
		Last Modified: Fri, 25 Apr 2025 17:52:20 GMT  
		Size: 6.5 MB (6471410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3594a7da4ff92a9abd27dc550a385c8bbeb5e28fabc967958775a3df2a0f96`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d68568eb773d06ed29e95f236f5900e0f575a70c3ee006c543384607da0b11`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:9d34bfb1916f9e9afecb9491c2e54a28cad04787d7b5e9317ee15100d051beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2490b80fcdf37dc28c990ea6049540776446b9c0973f77f88086356465f5cc0`

```dockerfile
```

-	Layers:
	-	`sha256:1b506a0fb93e704e1d6a0dbbac29ebc8f1dfb3cd813dd0f139df51422cc09052`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:7aed6760d32ff60522af0fe9dbbf411bb35f190c908dd34c2e1c35918070388a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155e98f2eedb665b03ec44e3975582a728961e440a725c0f69f690fff44568db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a64ee773ee396bff692796312d9b7dcc7fb44f952d2c908b4d376f16d9581d`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 6.2 MB (6239702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af4a70c73af05cb86c61280f805804a2f0ace4ab434db07169117ce347ae30b`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1084beee85752d4193e9e16db34006162f5878a5031f7b0e7c7e5c80b8c6f27`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c691956323d34a6b74e2dfbe1ab1bab5de30fe964ff714970639a2a122dc0e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bba8ffd862cccff6f4f84b00f8c0f1017110269d10624b18160c9ce2909636`

```dockerfile
```

-	Layers:
	-	`sha256:39f5fb5aec21d1cc18c2b4652236b54c02c55583eafa99d8c1d100f42ea99352`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:5689e34a9410f0b3a43f78ac470d2064ad40e49d1f6dc79eeb818bd41a7be3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288603c30be026199e52b513d137fd803edbb3bae2c21940fd3ab4a9565d29bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776b5dd8bbdaa374387b6347dd990a3afb1db9fd111c9542ff347efb9e8e262`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 6.6 MB (6603909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b72da8f217ee883d534bf8b81b4968bfe98d01195019acf154437d744a24a30`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02335cc369df4703ddd8bc4151583583c53a1490c756e6665be8d4bf73e9232c`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b984b0eb744f6b7b434f640a3c00e4c0d780f4ec952703fd4369cbecbd8764f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0b39651391cbc684b373c09fe28338c152436a70a949d8a2ded08402f8fff2`

```dockerfile
```

-	Layers:
	-	`sha256:ae85806ecae7c531d7315c6ecefafc450b8facf67c31d55c74ace2c47cb0aa46`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:960ff66153e19c70bd0c2f9f53fceb653b32381b2f6800e5a3b785ff73f650bd
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
$ docker pull nats@sha256:62b20bb99cf963ee9b0c78e26380a78a7dfa12eb8516d93bcf16b1f7eef252ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6305886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff853eebff5ea1827f264f2e22732dc892275c5bcd973db5058f4c4f0fe847e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d047c65ec95267487af401e091602880c16619e1ad4da3e7e962e8273ad589f3`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.3 MB (6305377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d3015f0a3ad1a5fecef389bb3fad1f3c80a49cbc71a62ab8d7db7516772ee`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d6c4492d078b6bd4aeba68dd433b2a71adcb56e2e389703dc6af3f8a5af646ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663437ee61b0867cdc6f83e65e7751bb848af12bf9ccb7704573df8e32e95bd`

```dockerfile
```

-	Layers:
	-	`sha256:3d12f58e08eefe61f0ba37c703f5646cf255aac6449a7c65b2b43f5a7bacb48f`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:102aa9adbc4a30a8bab821dd4d77d548b6ea7a12f339b04a5f1c31747eca7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd05d7ce42a7ec76ac0d22af9a9659a44dca6a1cf2d735cd27fde215a0db0506`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:500b76d02a1b23c604281d5c714a2c35e9bb75cc592a66e885e0f5a6e37f01f7`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.0 MB (6019989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5024945048c8d9454d3d901d804208e05dee841a927428da15b56f6cda2dfe0f`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f4642d3b2d1c595bd38ad079f450119842676b9c767451642ba468377601232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4adb1d0380f2178fe3652a824902cb41144dc0865ce28afe86223e2ddffd7`

```dockerfile
```

-	Layers:
	-	`sha256:f45013d27d687c2029f50a853a6baa027e4a22520d0eebd6226cf9f5c6dc409b`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ea87c80ec3b41d7c75130d62bcef1a297124c3a88d268381ab2c37ba307d73ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c48211b5750cd5af18bc0f8b0cb7210dc7b7442b3dddff32f3ed46470a2da8c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ddc6cab03365e07f2c6d7f059130a7dc282d4412f564e8e2c0df08c8bc73b654`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.0 MB (6011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c437fd34339124b6d3297d0074974f27d9c07d30fe42d04fb34c41bef2c43d`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:fffc88ae5d459abcedbd5c5d7e5f8d19b8794c52ca6188ca9f0c52afb76757d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add82b13529e611ce4c97b4933e0e140c7f8ebd67c1b6fc44ab3f06b3251fe1`

```dockerfile
```

-	Layers:
	-	`sha256:12a9e12b0405328b67372116138c73054a00281115d2f51f53d6ab18acd37481`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5af5adb666cd46b7cd6eaa3475636fd706a459a4c271c2bae0f663afa2e456d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f919a929c1e17f23640fb47e0fc43b05ad1b484c6197cad307207530716bd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84272a2e628924f03610b8c1c3c6e85b489ac87f290d0f685882def49de9ecd1`  
		Last Modified: Fri, 25 Apr 2025 09:28:47 GMT  
		Size: 5.8 MB (5796146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755f468e87f12862403c7a2d37f55dff1372e29f88136c0ba50bff80618988d`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ae261bb9805c736ed0d01a8af3f50ba6b75cd32b8a61a30bab0f3f38a7ad3397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f774c66ce1e2de4b74c2b0932ded1d5e97875334f0b5addf36ec617bdfcac`

```dockerfile
```

-	Layers:
	-	`sha256:6530cb0c6d8f35499127965fc373643eb042bd0291136f4fd82e137888b9cc27`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:f19a5e664bc3140ac051b51ff581345afc3974ca87e4377e64bcbbef2fc7837d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f90ce596ba2b9ffbe8c3d7836d7557f80f2eff80976acbda88bd45337bba78c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:edd6d59c7e29dc4aedef9eaa0785a9ced8aff83bf96b1f830e36dfa46f53be68`  
		Last Modified: Fri, 25 Apr 2025 09:28:46 GMT  
		Size: 5.8 MB (5775437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b27a2c43cc9286a86142e9071ba262afa4ac6a97ee4607fc43fa7f71ad97bc`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a758d3a359b53da7c6fed233fe42ef45b42a0dcd90f901aaa06a8d7c4b4f9590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605196d61046805754dda3246312272f529b7bd6a95a6b62b1e216d706c9f69`

```dockerfile
```

-	Layers:
	-	`sha256:9ce5dab5019211eb3c4213657f39f0272e6a0e24a6bfbbf1980a7fbd9a5bc11b`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:dea1543c1392e56a44b03ee62f370fc7bfbadb871a4387ae8fe199ec98a3ff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5035eb69783eaf7b9b82362cf68d01382ec0f326297e8878be99af8f9871e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1a8280710dc7fc73564b9f4f49fd6b32365882791aa95344c40d406b0a13f25`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.1 MB (6142593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033cc57448f08a332bf30589df2ea6255c2b00b7b7c31da4e1663a19dc06c9b`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9703f39141dc639788e95d00bfec218510dc9f2ab474dbb78470e2bc476212d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de3562e8db441250ba64bd95bc8b554fde7b751d0a567b223d312c5eaab6e00`

```dockerfile
```

-	Layers:
	-	`sha256:e260a2ca5c98ebac8d27b48ad48bdc5e6293498718316b387e725d6fed20cdf7`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:8ad5e6770c1df7c06e37c1855692061a4dec81c3bc4d289d3873a4554aa94d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de296657002e12709da3c23acf58143be37a698131dc288d4cc2c0309d43f108
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb13670aa8a73fbb2b50a99b8f822097b91002c77c9e1a26d7b154316e88ca0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:16:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:16:26 GMT
RUN cmd /S /C #(nop) COPY file:5e3840af0e267b510d2e54914f636d4b01f954b096bf81d459cc821ca4b3b468 in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b95fc9f036b2ce06ef6f75c0142446cf388b3fba5797ae076811cae5833b6`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be78d14ed5a916b3852e5c5b8f0c11c5ec282c35d533f16824dff33610aa794`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 6.5 MB (6479002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4903b008a32f8cb1eec6d3c17a357bb5a5292b67abdefef767f778101422a266`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48da8f54d5ccf3ef130af0a73b7b96919c2914ff036e75afef02bdbaa3434ad`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2a11075603c8b13618e5c581a166f4c1092208a1e0b6f6a1cd1cdd3e4d05d`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602c735353ba767b46b959a65eed16ad8ad55667c0a070c399b925fa4c2fea6`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:8ad5e6770c1df7c06e37c1855692061a4dec81c3bc4d289d3873a4554aa94d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de296657002e12709da3c23acf58143be37a698131dc288d4cc2c0309d43f108
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb13670aa8a73fbb2b50a99b8f822097b91002c77c9e1a26d7b154316e88ca0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:16:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:16:26 GMT
RUN cmd /S /C #(nop) COPY file:5e3840af0e267b510d2e54914f636d4b01f954b096bf81d459cc821ca4b3b468 in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b95fc9f036b2ce06ef6f75c0142446cf388b3fba5797ae076811cae5833b6`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be78d14ed5a916b3852e5c5b8f0c11c5ec282c35d533f16824dff33610aa794`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 6.5 MB (6479002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4903b008a32f8cb1eec6d3c17a357bb5a5292b67abdefef767f778101422a266`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48da8f54d5ccf3ef130af0a73b7b96919c2914ff036e75afef02bdbaa3434ad`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2a11075603c8b13618e5c581a166f4c1092208a1e0b6f6a1cd1cdd3e4d05d`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602c735353ba767b46b959a65eed16ad8ad55667c0a070c399b925fa4c2fea6`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:960ff66153e19c70bd0c2f9f53fceb653b32381b2f6800e5a3b785ff73f650bd
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
$ docker pull nats@sha256:62b20bb99cf963ee9b0c78e26380a78a7dfa12eb8516d93bcf16b1f7eef252ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6305886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff853eebff5ea1827f264f2e22732dc892275c5bcd973db5058f4c4f0fe847e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d047c65ec95267487af401e091602880c16619e1ad4da3e7e962e8273ad589f3`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.3 MB (6305377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d3015f0a3ad1a5fecef389bb3fad1f3c80a49cbc71a62ab8d7db7516772ee`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d6c4492d078b6bd4aeba68dd433b2a71adcb56e2e389703dc6af3f8a5af646ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663437ee61b0867cdc6f83e65e7751bb848af12bf9ccb7704573df8e32e95bd`

```dockerfile
```

-	Layers:
	-	`sha256:3d12f58e08eefe61f0ba37c703f5646cf255aac6449a7c65b2b43f5a7bacb48f`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:102aa9adbc4a30a8bab821dd4d77d548b6ea7a12f339b04a5f1c31747eca7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd05d7ce42a7ec76ac0d22af9a9659a44dca6a1cf2d735cd27fde215a0db0506`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:500b76d02a1b23c604281d5c714a2c35e9bb75cc592a66e885e0f5a6e37f01f7`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.0 MB (6019989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5024945048c8d9454d3d901d804208e05dee841a927428da15b56f6cda2dfe0f`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f4642d3b2d1c595bd38ad079f450119842676b9c767451642ba468377601232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4adb1d0380f2178fe3652a824902cb41144dc0865ce28afe86223e2ddffd7`

```dockerfile
```

-	Layers:
	-	`sha256:f45013d27d687c2029f50a853a6baa027e4a22520d0eebd6226cf9f5c6dc409b`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ea87c80ec3b41d7c75130d62bcef1a297124c3a88d268381ab2c37ba307d73ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c48211b5750cd5af18bc0f8b0cb7210dc7b7442b3dddff32f3ed46470a2da8c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ddc6cab03365e07f2c6d7f059130a7dc282d4412f564e8e2c0df08c8bc73b654`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.0 MB (6011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c437fd34339124b6d3297d0074974f27d9c07d30fe42d04fb34c41bef2c43d`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fffc88ae5d459abcedbd5c5d7e5f8d19b8794c52ca6188ca9f0c52afb76757d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add82b13529e611ce4c97b4933e0e140c7f8ebd67c1b6fc44ab3f06b3251fe1`

```dockerfile
```

-	Layers:
	-	`sha256:12a9e12b0405328b67372116138c73054a00281115d2f51f53d6ab18acd37481`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5af5adb666cd46b7cd6eaa3475636fd706a459a4c271c2bae0f663afa2e456d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f919a929c1e17f23640fb47e0fc43b05ad1b484c6197cad307207530716bd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84272a2e628924f03610b8c1c3c6e85b489ac87f290d0f685882def49de9ecd1`  
		Last Modified: Fri, 25 Apr 2025 09:28:47 GMT  
		Size: 5.8 MB (5796146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755f468e87f12862403c7a2d37f55dff1372e29f88136c0ba50bff80618988d`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ae261bb9805c736ed0d01a8af3f50ba6b75cd32b8a61a30bab0f3f38a7ad3397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f774c66ce1e2de4b74c2b0932ded1d5e97875334f0b5addf36ec617bdfcac`

```dockerfile
```

-	Layers:
	-	`sha256:6530cb0c6d8f35499127965fc373643eb042bd0291136f4fd82e137888b9cc27`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:f19a5e664bc3140ac051b51ff581345afc3974ca87e4377e64bcbbef2fc7837d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f90ce596ba2b9ffbe8c3d7836d7557f80f2eff80976acbda88bd45337bba78c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:edd6d59c7e29dc4aedef9eaa0785a9ced8aff83bf96b1f830e36dfa46f53be68`  
		Last Modified: Fri, 25 Apr 2025 09:28:46 GMT  
		Size: 5.8 MB (5775437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b27a2c43cc9286a86142e9071ba262afa4ac6a97ee4607fc43fa7f71ad97bc`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a758d3a359b53da7c6fed233fe42ef45b42a0dcd90f901aaa06a8d7c4b4f9590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605196d61046805754dda3246312272f529b7bd6a95a6b62b1e216d706c9f69`

```dockerfile
```

-	Layers:
	-	`sha256:9ce5dab5019211eb3c4213657f39f0272e6a0e24a6bfbbf1980a7fbd9a5bc11b`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:dea1543c1392e56a44b03ee62f370fc7bfbadb871a4387ae8fe199ec98a3ff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5035eb69783eaf7b9b82362cf68d01382ec0f326297e8878be99af8f9871e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1a8280710dc7fc73564b9f4f49fd6b32365882791aa95344c40d406b0a13f25`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.1 MB (6142593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033cc57448f08a332bf30589df2ea6255c2b00b7b7c31da4e1663a19dc06c9b`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9703f39141dc639788e95d00bfec218510dc9f2ab474dbb78470e2bc476212d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de3562e8db441250ba64bd95bc8b554fde7b751d0a567b223d312c5eaab6e00`

```dockerfile
```

-	Layers:
	-	`sha256:e260a2ca5c98ebac8d27b48ad48bdc5e6293498718316b387e725d6fed20cdf7`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:4ae66a1afca1485f7e5ef943f427685142d5ce607c4caecb5a0456e3a2625cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:864cd49a9319a3d243c7945cc4b1d847eeb62fc7ed3bff149dc06d3c11d80e98
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172714568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ee4030f14e129a49644c86c19599562d252f3c124fb474a5bb9ba9116a2acb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 17:53:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Apr 2025 17:53:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 17:53:18 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 17:53:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.2/nats-server-v2.11.2-windows-amd64.zip
# Fri, 25 Apr 2025 17:53:20 GMT
ENV NATS_SERVER_SHASUM=27bc84446495ed13983a86044d77cc24e4d5661a3ea3caaff3003c2d19dc3db8
# Fri, 25 Apr 2025 17:54:01 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Apr 2025 17:54:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 25 Apr 2025 17:54:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 17:54:22 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 17:54:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 17:54:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5220f32a15f4b9e4e60e00b789f7e5aed30ed16d768671ab81f2f7c847ce188`  
		Last Modified: Fri, 25 Apr 2025 17:54:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0adc223c6b3350c772df065f39904be980c1d151c04e822e6a524cae9a559b`  
		Last Modified: Fri, 25 Apr 2025 17:54:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e092e70456ee50a2b46c19beee1220448b3262ea35a4dc2762cf6dc92372d2`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe1399f73f5fcf68f18961cca3a08258165d8d8540bdeaabb55205a570b3ba0`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a098a1765813b5d39dd0a8b00f285c110efca73a5308620bad065b8fe9782`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9eb31776168317086fe75476b44574d1431a1e21f3d07a85279eafdd7341c`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 344.4 KB (344375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475c0b5a54a450e6b02e46614be9dfa7e5c0f7df6b4f4a34cf03889a90c6002`  
		Last Modified: Fri, 25 Apr 2025 17:54:27 GMT  
		Size: 6.8 MB (6832182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e6c6bd274e68a31e4fb7c629bd35c2bb6ef85a104202ba5864944cc76411b4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae5da4614649984507429fe2b6390a40f34095fd8fff099faee59172c99e03e`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc162497b3b567edf013a6577d06c352d56ab30ed7750e30f3161f5a2b5fa4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4ddd55fce7bccd5d5d53bfcb816dc5f0d980b8c904a6ef424c27bb6fc10a`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:4ae66a1afca1485f7e5ef943f427685142d5ce607c4caecb5a0456e3a2625cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:864cd49a9319a3d243c7945cc4b1d847eeb62fc7ed3bff149dc06d3c11d80e98
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172714568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ee4030f14e129a49644c86c19599562d252f3c124fb474a5bb9ba9116a2acb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 17:53:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Apr 2025 17:53:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 17:53:18 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 17:53:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.2/nats-server-v2.11.2-windows-amd64.zip
# Fri, 25 Apr 2025 17:53:20 GMT
ENV NATS_SERVER_SHASUM=27bc84446495ed13983a86044d77cc24e4d5661a3ea3caaff3003c2d19dc3db8
# Fri, 25 Apr 2025 17:54:01 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Apr 2025 17:54:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 25 Apr 2025 17:54:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 17:54:22 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 17:54:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 17:54:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5220f32a15f4b9e4e60e00b789f7e5aed30ed16d768671ab81f2f7c847ce188`  
		Last Modified: Fri, 25 Apr 2025 17:54:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0adc223c6b3350c772df065f39904be980c1d151c04e822e6a524cae9a559b`  
		Last Modified: Fri, 25 Apr 2025 17:54:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e092e70456ee50a2b46c19beee1220448b3262ea35a4dc2762cf6dc92372d2`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe1399f73f5fcf68f18961cca3a08258165d8d8540bdeaabb55205a570b3ba0`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a098a1765813b5d39dd0a8b00f285c110efca73a5308620bad065b8fe9782`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9eb31776168317086fe75476b44574d1431a1e21f3d07a85279eafdd7341c`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 344.4 KB (344375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475c0b5a54a450e6b02e46614be9dfa7e5c0f7df6b4f4a34cf03889a90c6002`  
		Last Modified: Fri, 25 Apr 2025 17:54:27 GMT  
		Size: 6.8 MB (6832182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e6c6bd274e68a31e4fb7c629bd35c2bb6ef85a104202ba5864944cc76411b4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae5da4614649984507429fe2b6390a40f34095fd8fff099faee59172c99e03e`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc162497b3b567edf013a6577d06c352d56ab30ed7750e30f3161f5a2b5fa4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4ddd55fce7bccd5d5d53bfcb816dc5f0d980b8c904a6ef424c27bb6fc10a`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:de8a0ec5bf9f9cf6c322cfa948c910bee7aa64b75616bd84bb76e35588314ed9
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
	-	windows version 10.0.17763.7249; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:eaf571fc0100a0ee76e11d2353ca377d212efc8a33f75461bc692e6e310c1b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6178040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12c4a3517b534660913af935eb15cb58445a73049cc3c01fb778d38d7894c3e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4779ea3d06793e5ee7df40a2fd3d380cf8df6613c1f1f988ef4681a958f7a0c6`  
		Last Modified: Fri, 25 Apr 2025 09:29:08 GMT  
		Size: 6.2 MB (6177532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9bd539d8c1dbf19649d6316e57d8cfcd9c1cc986190866c2020f4c9f912387`  
		Last Modified: Fri, 25 Apr 2025 18:08:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:880a58916b02b350c7beee04ee86dc613c877b08eb50462179d5d19414ec6136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ace0f0df0bcaa01724a87046df62bbe1370688ddbf546430f7f339cda1309`

```dockerfile
```

-	Layers:
	-	`sha256:c183ad4d81c3e121eb178559ebdb1e78eae93584ec799c4c40809600b07d65d2`  
		Last Modified: Fri, 25 Apr 2025 18:08:32 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:ddc9c9000ad317a03af7fecc696cccf7d4cd5720c897e7da7fa5ab0734b93b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ecb9cb13befacf96f86b47d962b42fc9e2c00622dc880f681e439f32e2ab8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6c7c5c29827cc69bd886bddab7d40d526e21cc35c93be7f4c59cc75710bdbb5`  
		Last Modified: Fri, 25 Apr 2025 09:29:05 GMT  
		Size: 5.9 MB (5898042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deedc781ff5df4da743193bd4ae1e42bfb99e1f62901b7b6355f8566cd9ec224`  
		Last Modified: Fri, 25 Apr 2025 17:49:29 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:7e997aefb9eaabcd5adfbc42e904003033fe31d30dbfefa961fb5b85b81f538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ead8a78a31ab07ca6e830be0cca119ca78a19a6af9cc521521e2cfcb599ef3`

```dockerfile
```

-	Layers:
	-	`sha256:ce4b2a7d6d955a30e061d690b8aeb8080d007ecf7413b1413eeb3cb778d617c6`  
		Last Modified: Fri, 25 Apr 2025 17:49:29 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:1d4e6085ee5b0adcfd6efa51f27e8219c95152e757c88559f88f90ef24629dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5890923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9216fb7144e80c5583c3797f100baee5876b7f71b897ff793af94b95ed8a66c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7ae3457f9383ac98813e8012d922aeee4f784560492589fbcb3f5e1ef32297f`  
		Last Modified: Fri, 25 Apr 2025 09:29:05 GMT  
		Size: 5.9 MB (5890413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ee6b50833faab4936a2f2794b8090c88b962e050ddc0a7ea135f77583fcffc`  
		Last Modified: Fri, 25 Apr 2025 18:08:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:70e06f22541254286f5b730c72df50a56cdab2954b6e0e4f305567df3301ba27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413f44894351e39163333fd207c9ad450be131c35513a129157ade8ece654ab3`

```dockerfile
```

-	Layers:
	-	`sha256:2d8f623d24ad145a6619923be7df438d3a3a69430a549a78267f2864c407c121`  
		Last Modified: Fri, 25 Apr 2025 18:08:00 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:39a8752b02ddbed41067a8549786ff837d4ee61d8a357dbeeaabdc8bd88f9dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d867b3d21036dab10cbebba95e5bf8136af218ff6c13b0211604a8310edf8ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:904ea9d4a0f96c5899ea12c2c3faf44410c9f77e4eaf169da90ed87878447de3`  
		Last Modified: Fri, 25 Apr 2025 09:29:05 GMT  
		Size: 5.7 MB (5681599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95498ed6497d4fdec93c68871823a7d9a13edaf6c7ae6a172a8c34c64b4505c`  
		Last Modified: Fri, 25 Apr 2025 17:52:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:9cba5858c30186758b9c4923c5342e0be72caed708cc7c259c181fa2979010bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85e22fb8c1734057ad52d781f6a48bf52bd827ec194eee4b55a987b0bd59486`

```dockerfile
```

-	Layers:
	-	`sha256:77c269374966f928e11db9f7b40d28ecae6c5577ab19b393785becfecc8e6370`  
		Last Modified: Fri, 25 Apr 2025 17:52:23 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:d4b03052f1d9d9090ab8e98e7b6ea1c99879b63cc2c2c67545b231540058ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b53adb121c06341d24c205535a3ea28e8f2a670bee94782211d586dc2e3347`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:699cb8e89ed804be32abbf966cec091cf40c1bc005c1149b0cd87137dd816ecf`  
		Last Modified: Fri, 25 Apr 2025 09:29:08 GMT  
		Size: 5.7 MB (5663241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41556a4ddc89bb9753d52a69fefd19998b1b6eb74190e0556ec07ef180c665f4`  
		Last Modified: Fri, 25 Apr 2025 18:08:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:7b3fc572fbcf016a4f6d69ce9038a9e3ad725ad118f9ed62a01ae07dc100302b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da692ba422bc8705942326828f77096df49dd12c8175627fe520e4a03c69dd0d`

```dockerfile
```

-	Layers:
	-	`sha256:b84f306fd992dd2529fc08c4efc16632cf19c8ce95437836a46c6ce5b1850dad`  
		Last Modified: Fri, 25 Apr 2025 18:08:49 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:1c6441d588f27945b54c4042c6b7b9d87c7ecbc4fcc23761790c3f68519faa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fd2b2a35e6fe798b1d92a40f41801a54dfdca2b32660ac261d21f6c24669ee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5fc300e6348c6f68ac2df0fec80c011ee32851a6a69a2f233f8315c0e2324703`  
		Last Modified: Fri, 25 Apr 2025 09:29:08 GMT  
		Size: 6.0 MB (6017145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae157577e66293ec3f12325663e0113e8c4b189b4496cc1424f6e6e0f137fd54`  
		Last Modified: Fri, 25 Apr 2025 18:08:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:f0ce3c62654b245a708cfafbc250d9d44be00d93e5b62d9b81f4674471e00c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b6c00361ff8ea9c2c50706e2b88febe1f92156735b165c78d1ee49d041da8c`

```dockerfile
```

-	Layers:
	-	`sha256:c72f82d912e3828cb992a04b17ba3d9d60df0eae0d3b1b360e2b8d7b504f82ae`  
		Last Modified: Fri, 25 Apr 2025 18:08:43 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:d414c1650bce52380b31db4e05cdbe1449e4157e9f6bf6b32a4828499b024abd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115056638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7730a58c199b1db5a73c7b454284ebd19ea94087c27875aa1b9e1decb9501e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:14:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:14:26 GMT
RUN cmd /S /C #(nop) COPY file:834fa0892aa92685c4ae904d9f5298c3695e3eb6f86773c2a8b99c1f19a22eae in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:14:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:14:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:14:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:14:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddcf97399e54fcd5d2599943cfadbe56fe4a468e1ff21c456d0d74988711721`  
		Last Modified: Fri, 25 Apr 2025 18:14:35 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ff6d4fa002fb6731abcdd14fe1dd1776d4233e0aedde9cf9787c8a43623ead`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 6.3 MB (6298157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e86c75b2594fcbe7282dc56d31bfc78e6e4adb96a7f856f72900cc1a91caf3`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf592a466c189aa46f25a643a6dc7e0ece333c36c1cc3875e4e3503ec973738`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342f0bda45bda3a27f7bcbe3488b0989d16e8f22af744d07aab05d53be287389`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d01e44cc79af4ccb7b82326e09731c27fefc9c1a36611d9a2f0799e58684a5`  
		Last Modified: Fri, 25 Apr 2025 18:14:33 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:309ddbe3e373d002d15c42575c95c632128c57e61e4189ba10e8b451ca3fa054
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
$ docker pull nats@sha256:103888bea542367b72c3ba989ea84d735c4592207b2956f2146f5ddb6a98ae38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ff90cda41d41180d9f1a28d0b83a1478ccaa14566f885f018a2706640d8e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909cff2c97366449285e54623d27baa31967eb1a41c82a84ac9cc0a8c44d4270`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 6.6 MB (6640205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6aa2f46be25983cd1812bcf685e2ec3a6c46e6b0c3f9f4e3dc0c1f257dbc4e`  
		Last Modified: Fri, 25 Apr 2025 17:48:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476136643f08acc200743e05a55cb718c7d23a86f4aaac348430960bb5cea289`  
		Last Modified: Fri, 25 Apr 2025 17:48:17 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8aa402584c0749a5ea50b8db21aa89e1d2890c5070489b4d0ac0b568988f1ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38959f095b3ace841262dbd601e81e1cf47b30a9bd666dcd934b1d41da2bae54`

```dockerfile
```

-	Layers:
	-	`sha256:534389edf52ca7a279d9b77ded3ec88949be96c06902271006ce0900e446f89b`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:f4af69c51467ad969030a6285656c53a491fc03b8e442c30b897b1691439c471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b314b737c1720f822adbbefbcae87909929bf35a02b8d28a76fa7aeb01bc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97974a6f36486b798da64002fc218b2233d353058852cffd0220594b01e269`  
		Last Modified: Fri, 25 Apr 2025 17:47:47 GMT  
		Size: 6.4 MB (6363595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb6a73b6e361505406303a8c7b3f3cfeba51010bf739aef7889bf7f0317a3b8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e222efd7d05fe8bcbda2e28970d7b05f8bb17ea70e7b7facf4701541d05df8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5d34c1d5bed5a36593535f90aa950998957ae6a3d449899399f891679fa4ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05763aa76d78f8542ea1a12d8d75d8fe560b0dc4580158377ec49947c2b6d9cb`

```dockerfile
```

-	Layers:
	-	`sha256:27aef148734276a47a22fea3a763eeb98084a6604242d969b88cfa2ebba41576`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:615589cc5b0fadc95d860ccd1c45f7c935329b0a55b180c62f7f9fee774b0bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9448927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56209644f7c0bd4ea6e7856533ee51cd1542c82591cbd261e7d3b46d0e28e180`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbe953e88cc3bf2f3993928acd202fd42ac79b27936ae590499ffaa38ce4d1c`  
		Last Modified: Fri, 25 Apr 2025 17:50:05 GMT  
		Size: 6.3 MB (6349833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169c3aac0c1268dcf99c69ef6f71d0fe444f5c235aa81d3ea7c998cc86f363cb`  
		Last Modified: Fri, 25 Apr 2025 17:50:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb96ee5b11624b1dc1de4eb7832f0357fef8589035169fc0883879c55e461924`  
		Last Modified: Fri, 25 Apr 2025 17:50:05 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a5475861c74695817f77f52b7218c118c286233b532f01ae1b98838d69c0e8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded60bb7e4e2db170c663a46e05c58d35a71ad81272d2c3f307d570c3c47f3c6`

```dockerfile
```

-	Layers:
	-	`sha256:6302be596e4266aa7d8c567c758b2e109143e783d4d703b8c98937854f42a819`  
		Last Modified: Fri, 25 Apr 2025 17:50:04 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb56b601a01e41e3fa3e1ec6882a5c7080064af2cbf8eebbe0aa8789057d7d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c20275401ac1b6354f9bceea70fdbc9ea6b248f61de5860e8a48f4b9fa13449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d88dec44185a51ca27621bbb65e75ccd454b3c28c91009b2dde51a8ff3b55e`  
		Last Modified: Fri, 25 Apr 2025 17:47:42 GMT  
		Size: 6.1 MB (6145926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf91e9429cda3e96e24922bd3640282bad3965a0d6209055ac549cc49b5e0f8a`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c6034f34091ef89d05c32fed01a7493f7c83cbbf10547c8aefac36a59fe368`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:770428e58483a9652ac1bc757a92b38fb475e7802a1661bd0ee9bdbcc99a1a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fafe954b8c08a5febfa3873a84d9f621009fd0e4dc99eecd3c7d0e8a2ee129`

```dockerfile
```

-	Layers:
	-	`sha256:3d1465d1edfad8a9d270db627b7ae6ba90ac0fe85ef2e09550f0bd2a9ff67820`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:0826fc9a3cd514371e9d26650089c73a7a3308232845fa80900c87f273cf1715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9701256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb1cf3f9d41ccf72cdadf9a8a038281e2bbb47dd8b9391beb8856772cf0c7ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7473e40ba51f74648b04be0b64ecc86458a4651a18a83c403f87a81264b7166a`  
		Last Modified: Fri, 25 Apr 2025 17:48:52 GMT  
		Size: 6.1 MB (6125940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4169367173cd67ccaae5d390125ae2f6b158888f42ea130b28eca618e077e377`  
		Last Modified: Fri, 25 Apr 2025 17:48:51 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e3edb66f2b218e51a019b80bd8baa17152dc3dc35eff72b1e1a04a8305317d`  
		Last Modified: Fri, 25 Apr 2025 17:48:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d42eb1070edb7bb4788b2b207b7327b103e78d52c8741b8b59ebb09a6c98b7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3647089a9dae12d3169e2e2047470b388399db468b55034a7b7a9dec4114a7b4`

```dockerfile
```

-	Layers:
	-	`sha256:191264e1ff4f4c1dc6f4c74512c9306511473757cde8009a49560b326af91ce6`  
		Last Modified: Fri, 25 Apr 2025 17:48:51 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:36955abe987fd5f6b2e2ab7ad9cd7074f4e6b697221554377415b6a5a2d4a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9951337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc31dff866e7d0df0d524921304ae2ed11fe1d8e8023901f3fde3ccf1c6edf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13be4b158267a02187d5d7cd652d2171c6ab1616201f8ecbde2bbf2521bbbde4`  
		Last Modified: Fri, 25 Apr 2025 17:48:38 GMT  
		Size: 6.5 MB (6482799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b9052fa0fcea21b90e03eea858fb3575ecb143a07768feb976ff7c3df22a14`  
		Last Modified: Fri, 25 Apr 2025 17:48:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88597b6f663e53f1d2512f2d0a95cb5e888053d6bbdb2a345b946cbbac8eb96e`  
		Last Modified: Fri, 25 Apr 2025 17:48:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fd4df52b364d971b8549fab971a8571704e338a98d5dae3bb28a0acf9e4d354d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89643ad3257bccbf1617163ac6a79e7a5248ed3553e0c46cf7ff9d44757dafc7`

```dockerfile
```

-	Layers:
	-	`sha256:335d17ba4ec15090eb2087d381237fd9f2757f512d87b26b029e1542fc3ff898`  
		Last Modified: Fri, 25 Apr 2025 17:48:38 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.21`

```console
$ docker pull nats@sha256:309ddbe3e373d002d15c42575c95c632128c57e61e4189ba10e8b451ca3fa054
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
$ docker pull nats@sha256:103888bea542367b72c3ba989ea84d735c4592207b2956f2146f5ddb6a98ae38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ff90cda41d41180d9f1a28d0b83a1478ccaa14566f885f018a2706640d8e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909cff2c97366449285e54623d27baa31967eb1a41c82a84ac9cc0a8c44d4270`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 6.6 MB (6640205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6aa2f46be25983cd1812bcf685e2ec3a6c46e6b0c3f9f4e3dc0c1f257dbc4e`  
		Last Modified: Fri, 25 Apr 2025 17:48:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476136643f08acc200743e05a55cb718c7d23a86f4aaac348430960bb5cea289`  
		Last Modified: Fri, 25 Apr 2025 17:48:17 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:8aa402584c0749a5ea50b8db21aa89e1d2890c5070489b4d0ac0b568988f1ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38959f095b3ace841262dbd601e81e1cf47b30a9bd666dcd934b1d41da2bae54`

```dockerfile
```

-	Layers:
	-	`sha256:534389edf52ca7a279d9b77ded3ec88949be96c06902271006ce0900e446f89b`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:f4af69c51467ad969030a6285656c53a491fc03b8e442c30b897b1691439c471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9729296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7b314b737c1720f822adbbefbcae87909929bf35a02b8d28a76fa7aeb01bc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e97974a6f36486b798da64002fc218b2233d353058852cffd0220594b01e269`  
		Last Modified: Fri, 25 Apr 2025 17:47:47 GMT  
		Size: 6.4 MB (6363595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb6a73b6e361505406303a8c7b3f3cfeba51010bf739aef7889bf7f0317a3b8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e222efd7d05fe8bcbda2e28970d7b05f8bb17ea70e7b7facf4701541d05df8`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:5d34c1d5bed5a36593535f90aa950998957ae6a3d449899399f891679fa4ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05763aa76d78f8542ea1a12d8d75d8fe560b0dc4580158377ec49947c2b6d9cb`

```dockerfile
```

-	Layers:
	-	`sha256:27aef148734276a47a22fea3a763eeb98084a6604242d969b88cfa2ebba41576`  
		Last Modified: Fri, 25 Apr 2025 17:47:46 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:615589cc5b0fadc95d860ccd1c45f7c935329b0a55b180c62f7f9fee774b0bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9448927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56209644f7c0bd4ea6e7856533ee51cd1542c82591cbd261e7d3b46d0e28e180`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbe953e88cc3bf2f3993928acd202fd42ac79b27936ae590499ffaa38ce4d1c`  
		Last Modified: Fri, 25 Apr 2025 17:50:05 GMT  
		Size: 6.3 MB (6349833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169c3aac0c1268dcf99c69ef6f71d0fe444f5c235aa81d3ea7c998cc86f363cb`  
		Last Modified: Fri, 25 Apr 2025 17:50:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb96ee5b11624b1dc1de4eb7832f0357fef8589035169fc0883879c55e461924`  
		Last Modified: Fri, 25 Apr 2025 17:50:05 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:a5475861c74695817f77f52b7218c118c286233b532f01ae1b98838d69c0e8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded60bb7e4e2db170c663a46e05c58d35a71ad81272d2c3f307d570c3c47f3c6`

```dockerfile
```

-	Layers:
	-	`sha256:6302be596e4266aa7d8c567c758b2e109143e783d4d703b8c98937854f42a819`  
		Last Modified: Fri, 25 Apr 2025 17:50:04 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:fb56b601a01e41e3fa3e1ec6882a5c7080064af2cbf8eebbe0aa8789057d7d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10139926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c20275401ac1b6354f9bceea70fdbc9ea6b248f61de5860e8a48f4b9fa13449`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d88dec44185a51ca27621bbb65e75ccd454b3c28c91009b2dde51a8ff3b55e`  
		Last Modified: Fri, 25 Apr 2025 17:47:42 GMT  
		Size: 6.1 MB (6145926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf91e9429cda3e96e24922bd3640282bad3965a0d6209055ac549cc49b5e0f8a`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c6034f34091ef89d05c32fed01a7493f7c83cbbf10547c8aefac36a59fe368`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:770428e58483a9652ac1bc757a92b38fb475e7802a1661bd0ee9bdbcc99a1a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fafe954b8c08a5febfa3873a84d9f621009fd0e4dc99eecd3c7d0e8a2ee129`

```dockerfile
```

-	Layers:
	-	`sha256:3d1465d1edfad8a9d270db627b7ae6ba90ac0fe85ef2e09550f0bd2a9ff67820`  
		Last Modified: Fri, 25 Apr 2025 17:47:41 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:0826fc9a3cd514371e9d26650089c73a7a3308232845fa80900c87f273cf1715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9701256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb1cf3f9d41ccf72cdadf9a8a038281e2bbb47dd8b9391beb8856772cf0c7ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7473e40ba51f74648b04be0b64ecc86458a4651a18a83c403f87a81264b7166a`  
		Last Modified: Fri, 25 Apr 2025 17:48:52 GMT  
		Size: 6.1 MB (6125940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4169367173cd67ccaae5d390125ae2f6b158888f42ea130b28eca618e077e377`  
		Last Modified: Fri, 25 Apr 2025 17:48:51 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e3edb66f2b218e51a019b80bd8baa17152dc3dc35eff72b1e1a04a8305317d`  
		Last Modified: Fri, 25 Apr 2025 17:48:51 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:d42eb1070edb7bb4788b2b207b7327b103e78d52c8741b8b59ebb09a6c98b7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3647089a9dae12d3169e2e2047470b388399db468b55034a7b7a9dec4114a7b4`

```dockerfile
```

-	Layers:
	-	`sha256:191264e1ff4f4c1dc6f4c74512c9306511473757cde8009a49560b326af91ce6`  
		Last Modified: Fri, 25 Apr 2025 17:48:51 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:36955abe987fd5f6b2e2ab7ad9cd7074f4e6b697221554377415b6a5a2d4a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9951337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc31dff866e7d0df0d524921304ae2ed11fe1d8e8023901f3fde3ccf1c6edf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='78f9b382d468f7b683bf8bdda2c6276de1fd230d9d19724485f48b327d7ed4c2' ;; 		armhf) natsArch='arm6'; sha256='2a29a87abdec21bff9fb19a30aa06af12a6db31ec32d0b3de1a7c8bdeeb74b19' ;; 		armv7) natsArch='arm7'; sha256='837db6e72894993bde7f0e402f6f9dc151d8452b0441cea630260764bafd4c84' ;; 		x86_64) natsArch='amd64'; sha256='52e3baee2bf9cb4f3d362e293538e9f11ccfdb22ac9fbbd2bcad790e3ba41e3e' ;; 		x86) natsArch='386'; sha256='ffabdd7c124951b68ed4501223d5a877c3e90c5da68c27c884a58806eaa1c369' ;; 		s390x) natsArch='s390x'; sha256='f5627e4db5746200f62e6d5d9212dcfc59a4d4dc9cee30abf8eafdafac5445a1' ;; 		ppc64le) natsArch='ppc64le'; sha256='096424d6958c7b2798027208d0cc0c2ea5632e5530fd94d66712d586ca6d6d27' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13be4b158267a02187d5d7cd652d2171c6ab1616201f8ecbde2bbf2521bbbde4`  
		Last Modified: Fri, 25 Apr 2025 17:48:38 GMT  
		Size: 6.5 MB (6482799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b9052fa0fcea21b90e03eea858fb3575ecb143a07768feb976ff7c3df22a14`  
		Last Modified: Fri, 25 Apr 2025 17:48:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88597b6f663e53f1d2512f2d0a95cb5e888053d6bbdb2a345b946cbbac8eb96e`  
		Last Modified: Fri, 25 Apr 2025 17:48:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fd4df52b364d971b8549fab971a8571704e338a98d5dae3bb28a0acf9e4d354d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89643ad3257bccbf1617163ac6a79e7a5248ed3553e0c46cf7ff9d44757dafc7`

```dockerfile
```

-	Layers:
	-	`sha256:335d17ba4ec15090eb2087d381237fd9f2757f512d87b26b029e1542fc3ff898`  
		Last Modified: Fri, 25 Apr 2025 17:48:38 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:4fd7079e6f94e98cd8f764ed1645d7381f285e3932074e476f835f495b9d8d64
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
$ docker pull nats@sha256:eaf571fc0100a0ee76e11d2353ca377d212efc8a33f75461bc692e6e310c1b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6178040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12c4a3517b534660913af935eb15cb58445a73049cc3c01fb778d38d7894c3e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4779ea3d06793e5ee7df40a2fd3d380cf8df6613c1f1f988ef4681a958f7a0c6`  
		Last Modified: Fri, 25 Apr 2025 09:29:08 GMT  
		Size: 6.2 MB (6177532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9bd539d8c1dbf19649d6316e57d8cfcd9c1cc986190866c2020f4c9f912387`  
		Last Modified: Fri, 25 Apr 2025 18:08:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:880a58916b02b350c7beee04ee86dc613c877b08eb50462179d5d19414ec6136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ace0f0df0bcaa01724a87046df62bbe1370688ddbf546430f7f339cda1309`

```dockerfile
```

-	Layers:
	-	`sha256:c183ad4d81c3e121eb178559ebdb1e78eae93584ec799c4c40809600b07d65d2`  
		Last Modified: Fri, 25 Apr 2025 18:08:32 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ddc9c9000ad317a03af7fecc696cccf7d4cd5720c897e7da7fa5ab0734b93b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ecb9cb13befacf96f86b47d962b42fc9e2c00622dc880f681e439f32e2ab8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6c7c5c29827cc69bd886bddab7d40d526e21cc35c93be7f4c59cc75710bdbb5`  
		Last Modified: Fri, 25 Apr 2025 09:29:05 GMT  
		Size: 5.9 MB (5898042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deedc781ff5df4da743193bd4ae1e42bfb99e1f62901b7b6355f8566cd9ec224`  
		Last Modified: Fri, 25 Apr 2025 17:49:29 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7e997aefb9eaabcd5adfbc42e904003033fe31d30dbfefa961fb5b85b81f538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ead8a78a31ab07ca6e830be0cca119ca78a19a6af9cc521521e2cfcb599ef3`

```dockerfile
```

-	Layers:
	-	`sha256:ce4b2a7d6d955a30e061d690b8aeb8080d007ecf7413b1413eeb3cb778d617c6`  
		Last Modified: Fri, 25 Apr 2025 17:49:29 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:1d4e6085ee5b0adcfd6efa51f27e8219c95152e757c88559f88f90ef24629dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5890923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9216fb7144e80c5583c3797f100baee5876b7f71b897ff793af94b95ed8a66c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7ae3457f9383ac98813e8012d922aeee4f784560492589fbcb3f5e1ef32297f`  
		Last Modified: Fri, 25 Apr 2025 09:29:05 GMT  
		Size: 5.9 MB (5890413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ee6b50833faab4936a2f2794b8090c88b962e050ddc0a7ea135f77583fcffc`  
		Last Modified: Fri, 25 Apr 2025 18:08:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:70e06f22541254286f5b730c72df50a56cdab2954b6e0e4f305567df3301ba27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413f44894351e39163333fd207c9ad450be131c35513a129157ade8ece654ab3`

```dockerfile
```

-	Layers:
	-	`sha256:2d8f623d24ad145a6619923be7df438d3a3a69430a549a78267f2864c407c121`  
		Last Modified: Fri, 25 Apr 2025 18:08:00 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:39a8752b02ddbed41067a8549786ff837d4ee61d8a357dbeeaabdc8bd88f9dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d867b3d21036dab10cbebba95e5bf8136af218ff6c13b0211604a8310edf8ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:904ea9d4a0f96c5899ea12c2c3faf44410c9f77e4eaf169da90ed87878447de3`  
		Last Modified: Fri, 25 Apr 2025 09:29:05 GMT  
		Size: 5.7 MB (5681599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95498ed6497d4fdec93c68871823a7d9a13edaf6c7ae6a172a8c34c64b4505c`  
		Last Modified: Fri, 25 Apr 2025 17:52:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9cba5858c30186758b9c4923c5342e0be72caed708cc7c259c181fa2979010bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85e22fb8c1734057ad52d781f6a48bf52bd827ec194eee4b55a987b0bd59486`

```dockerfile
```

-	Layers:
	-	`sha256:77c269374966f928e11db9f7b40d28ecae6c5577ab19b393785becfecc8e6370`  
		Last Modified: Fri, 25 Apr 2025 17:52:23 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d4b03052f1d9d9090ab8e98e7b6ea1c99879b63cc2c2c67545b231540058ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b53adb121c06341d24c205535a3ea28e8f2a670bee94782211d586dc2e3347`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:699cb8e89ed804be32abbf966cec091cf40c1bc005c1149b0cd87137dd816ecf`  
		Last Modified: Fri, 25 Apr 2025 09:29:08 GMT  
		Size: 5.7 MB (5663241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41556a4ddc89bb9753d52a69fefd19998b1b6eb74190e0556ec07ef180c665f4`  
		Last Modified: Fri, 25 Apr 2025 18:08:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7b3fc572fbcf016a4f6d69ce9038a9e3ad725ad118f9ed62a01ae07dc100302b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da692ba422bc8705942326828f77096df49dd12c8175627fe520e4a03c69dd0d`

```dockerfile
```

-	Layers:
	-	`sha256:b84f306fd992dd2529fc08c4efc16632cf19c8ce95437836a46c6ce5b1850dad`  
		Last Modified: Fri, 25 Apr 2025 18:08:49 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:1c6441d588f27945b54c4042c6b7b9d87c7ecbc4fcc23761790c3f68519faa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fd2b2a35e6fe798b1d92a40f41801a54dfdca2b32660ac261d21f6c24669ee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5fc300e6348c6f68ac2df0fec80c011ee32851a6a69a2f233f8315c0e2324703`  
		Last Modified: Fri, 25 Apr 2025 09:29:08 GMT  
		Size: 6.0 MB (6017145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae157577e66293ec3f12325663e0113e8c4b189b4496cc1424f6e6e0f137fd54`  
		Last Modified: Fri, 25 Apr 2025 18:08:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f0ce3c62654b245a708cfafbc250d9d44be00d93e5b62d9b81f4674471e00c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b6c00361ff8ea9c2c50706e2b88febe1f92156735b165c78d1ee49d041da8c`

```dockerfile
```

-	Layers:
	-	`sha256:c72f82d912e3828cb992a04b17ba3d9d60df0eae0d3b1b360e2b8d7b504f82ae`  
		Last Modified: Fri, 25 Apr 2025 18:08:43 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:36058f053d8a9ff22b67ce7d2890547fb9a9a7ea8ad1f3d4b817f155ca8c6cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:d414c1650bce52380b31db4e05cdbe1449e4157e9f6bf6b32a4828499b024abd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115056638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7730a58c199b1db5a73c7b454284ebd19ea94087c27875aa1b9e1decb9501e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:14:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:14:26 GMT
RUN cmd /S /C #(nop) COPY file:834fa0892aa92685c4ae904d9f5298c3695e3eb6f86773c2a8b99c1f19a22eae in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:14:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:14:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:14:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:14:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddcf97399e54fcd5d2599943cfadbe56fe4a468e1ff21c456d0d74988711721`  
		Last Modified: Fri, 25 Apr 2025 18:14:35 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ff6d4fa002fb6731abcdd14fe1dd1776d4233e0aedde9cf9787c8a43623ead`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 6.3 MB (6298157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e86c75b2594fcbe7282dc56d31bfc78e6e4adb96a7f856f72900cc1a91caf3`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf592a466c189aa46f25a643a6dc7e0ece333c36c1cc3875e4e3503ec973738`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342f0bda45bda3a27f7bcbe3488b0989d16e8f22af744d07aab05d53be287389`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d01e44cc79af4ccb7b82326e09731c27fefc9c1a36611d9a2f0799e58684a5`  
		Last Modified: Fri, 25 Apr 2025 18:14:33 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:36058f053d8a9ff22b67ce7d2890547fb9a9a7ea8ad1f3d4b817f155ca8c6cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:d414c1650bce52380b31db4e05cdbe1449e4157e9f6bf6b32a4828499b024abd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115056638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7730a58c199b1db5a73c7b454284ebd19ea94087c27875aa1b9e1decb9501e`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:14:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:14:26 GMT
RUN cmd /S /C #(nop) COPY file:834fa0892aa92685c4ae904d9f5298c3695e3eb6f86773c2a8b99c1f19a22eae in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:14:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:14:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:14:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:14:29 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddcf97399e54fcd5d2599943cfadbe56fe4a468e1ff21c456d0d74988711721`  
		Last Modified: Fri, 25 Apr 2025 18:14:35 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ff6d4fa002fb6731abcdd14fe1dd1776d4233e0aedde9cf9787c8a43623ead`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 6.3 MB (6298157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e86c75b2594fcbe7282dc56d31bfc78e6e4adb96a7f856f72900cc1a91caf3`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf592a466c189aa46f25a643a6dc7e0ece333c36c1cc3875e4e3503ec973738`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342f0bda45bda3a27f7bcbe3488b0989d16e8f22af744d07aab05d53be287389`  
		Last Modified: Fri, 25 Apr 2025 18:14:34 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d01e44cc79af4ccb7b82326e09731c27fefc9c1a36611d9a2f0799e58684a5`  
		Last Modified: Fri, 25 Apr 2025 18:14:33 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:4fd7079e6f94e98cd8f764ed1645d7381f285e3932074e476f835f495b9d8d64
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
$ docker pull nats@sha256:eaf571fc0100a0ee76e11d2353ca377d212efc8a33f75461bc692e6e310c1b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6178040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12c4a3517b534660913af935eb15cb58445a73049cc3c01fb778d38d7894c3e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4779ea3d06793e5ee7df40a2fd3d380cf8df6613c1f1f988ef4681a958f7a0c6`  
		Last Modified: Fri, 25 Apr 2025 09:29:08 GMT  
		Size: 6.2 MB (6177532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9bd539d8c1dbf19649d6316e57d8cfcd9c1cc986190866c2020f4c9f912387`  
		Last Modified: Fri, 25 Apr 2025 18:08:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:880a58916b02b350c7beee04ee86dc613c877b08eb50462179d5d19414ec6136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ace0f0df0bcaa01724a87046df62bbe1370688ddbf546430f7f339cda1309`

```dockerfile
```

-	Layers:
	-	`sha256:c183ad4d81c3e121eb178559ebdb1e78eae93584ec799c4c40809600b07d65d2`  
		Last Modified: Fri, 25 Apr 2025 18:08:32 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ddc9c9000ad317a03af7fecc696cccf7d4cd5720c897e7da7fa5ab0734b93b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ecb9cb13befacf96f86b47d962b42fc9e2c00622dc880f681e439f32e2ab8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b6c7c5c29827cc69bd886bddab7d40d526e21cc35c93be7f4c59cc75710bdbb5`  
		Last Modified: Fri, 25 Apr 2025 09:29:05 GMT  
		Size: 5.9 MB (5898042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deedc781ff5df4da743193bd4ae1e42bfb99e1f62901b7b6355f8566cd9ec224`  
		Last Modified: Fri, 25 Apr 2025 17:49:29 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7e997aefb9eaabcd5adfbc42e904003033fe31d30dbfefa961fb5b85b81f538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ead8a78a31ab07ca6e830be0cca119ca78a19a6af9cc521521e2cfcb599ef3`

```dockerfile
```

-	Layers:
	-	`sha256:ce4b2a7d6d955a30e061d690b8aeb8080d007ecf7413b1413eeb3cb778d617c6`  
		Last Modified: Fri, 25 Apr 2025 17:49:29 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:1d4e6085ee5b0adcfd6efa51f27e8219c95152e757c88559f88f90ef24629dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5890923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9216fb7144e80c5583c3797f100baee5876b7f71b897ff793af94b95ed8a66c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7ae3457f9383ac98813e8012d922aeee4f784560492589fbcb3f5e1ef32297f`  
		Last Modified: Fri, 25 Apr 2025 09:29:05 GMT  
		Size: 5.9 MB (5890413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ee6b50833faab4936a2f2794b8090c88b962e050ddc0a7ea135f77583fcffc`  
		Last Modified: Fri, 25 Apr 2025 18:08:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:70e06f22541254286f5b730c72df50a56cdab2954b6e0e4f305567df3301ba27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413f44894351e39163333fd207c9ad450be131c35513a129157ade8ece654ab3`

```dockerfile
```

-	Layers:
	-	`sha256:2d8f623d24ad145a6619923be7df438d3a3a69430a549a78267f2864c407c121`  
		Last Modified: Fri, 25 Apr 2025 18:08:00 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:39a8752b02ddbed41067a8549786ff837d4ee61d8a357dbeeaabdc8bd88f9dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d867b3d21036dab10cbebba95e5bf8136af218ff6c13b0211604a8310edf8ca`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:904ea9d4a0f96c5899ea12c2c3faf44410c9f77e4eaf169da90ed87878447de3`  
		Last Modified: Fri, 25 Apr 2025 09:29:05 GMT  
		Size: 5.7 MB (5681599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95498ed6497d4fdec93c68871823a7d9a13edaf6c7ae6a172a8c34c64b4505c`  
		Last Modified: Fri, 25 Apr 2025 17:52:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9cba5858c30186758b9c4923c5342e0be72caed708cc7c259c181fa2979010bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85e22fb8c1734057ad52d781f6a48bf52bd827ec194eee4b55a987b0bd59486`

```dockerfile
```

-	Layers:
	-	`sha256:77c269374966f928e11db9f7b40d28ecae6c5577ab19b393785becfecc8e6370`  
		Last Modified: Fri, 25 Apr 2025 17:52:23 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d4b03052f1d9d9090ab8e98e7b6ea1c99879b63cc2c2c67545b231540058ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b53adb121c06341d24c205535a3ea28e8f2a670bee94782211d586dc2e3347`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:699cb8e89ed804be32abbf966cec091cf40c1bc005c1149b0cd87137dd816ecf`  
		Last Modified: Fri, 25 Apr 2025 09:29:08 GMT  
		Size: 5.7 MB (5663241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41556a4ddc89bb9753d52a69fefd19998b1b6eb74190e0556ec07ef180c665f4`  
		Last Modified: Fri, 25 Apr 2025 18:08:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7b3fc572fbcf016a4f6d69ce9038a9e3ad725ad118f9ed62a01ae07dc100302b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da692ba422bc8705942326828f77096df49dd12c8175627fe520e4a03c69dd0d`

```dockerfile
```

-	Layers:
	-	`sha256:b84f306fd992dd2529fc08c4efc16632cf19c8ce95437836a46c6ce5b1850dad`  
		Last Modified: Fri, 25 Apr 2025 18:08:49 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:1c6441d588f27945b54c4042c6b7b9d87c7ecbc4fcc23761790c3f68519faa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fd2b2a35e6fe798b1d92a40f41801a54dfdca2b32660ac261d21f6c24669ee`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5fc300e6348c6f68ac2df0fec80c011ee32851a6a69a2f233f8315c0e2324703`  
		Last Modified: Fri, 25 Apr 2025 09:29:08 GMT  
		Size: 6.0 MB (6017145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae157577e66293ec3f12325663e0113e8c4b189b4496cc1424f6e6e0f137fd54`  
		Last Modified: Fri, 25 Apr 2025 18:08:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f0ce3c62654b245a708cfafbc250d9d44be00d93e5b62d9b81f4674471e00c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b6c00361ff8ea9c2c50706e2b88febe1f92156735b165c78d1ee49d041da8c`

```dockerfile
```

-	Layers:
	-	`sha256:c72f82d912e3828cb992a04b17ba3d9d60df0eae0d3b1b360e2b8d7b504f82ae`  
		Last Modified: Fri, 25 Apr 2025 18:08:43 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:8135c698d82ad1de505538338ea400f45f133591689e762afc7bf89360ec05ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:e553dd2df25d38f7c58c86916a6993a645db4aee95d621fd28621d010cbd4c39
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172513583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730c1c3823a4d7ec40c4ebea0fc753a14d18c46c6361f81bf3e112ba07697cd3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 17:56:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Apr 2025 17:56:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 17:56:08 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 17:56:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.28/nats-server-v2.10.28-windows-amd64.zip
# Fri, 25 Apr 2025 17:56:10 GMT
ENV NATS_SERVER_SHASUM=98b8571231b00ebe0445cc7f317f6425c1fbc2edecd455949d37022e04281657
# Fri, 25 Apr 2025 17:56:42 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Apr 2025 17:56:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 25 Apr 2025 17:56:59 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 17:56:59 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 17:57:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 17:57:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d19d00d2094f2c58d7934a50b6ee709e72fc4ad29b81ff2bd7756adcbe037f0`  
		Last Modified: Fri, 25 Apr 2025 17:57:06 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcbb5d10b04f2cd56c2e0d040797aec57c5839f4805ee8b10c5e421efbdd889`  
		Last Modified: Fri, 25 Apr 2025 17:57:06 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3874a74574bed47a99842f9aba1c049223abb1e039618bd8c34e1dc0b7ba105e`  
		Last Modified: Fri, 25 Apr 2025 17:57:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892c56b140e7f00e97775014c34bcc6ebc61457d2d773c3efff5ca3c7cd6955`  
		Last Modified: Fri, 25 Apr 2025 17:57:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814cad5131cce2c37f6fc3d6008c9ac2db70d82f4f51db8dd505bccb0d34a695`  
		Last Modified: Fri, 25 Apr 2025 17:57:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2e203debf29ff5da8090a7d10db82622a25c539410dee10d6f2f0896677e9`  
		Last Modified: Fri, 25 Apr 2025 17:57:05 GMT  
		Size: 333.4 KB (333428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eaee7236ce6097c1288a8835d6ab940bd25fa2c68f30cee5fcf9523a4da3fc`  
		Last Modified: Fri, 25 Apr 2025 17:57:04 GMT  
		Size: 6.6 MB (6642099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c4806f2cfa9d4c464bc1cde03b5f71635b46fcb9787a60f7751771198489dc`  
		Last Modified: Fri, 25 Apr 2025 17:57:03 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5fc082a86b29f034924923fea5310e03058ae72bcca5830ff62c98c9a2c87a`  
		Last Modified: Fri, 25 Apr 2025 17:57:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c329770998d0a5276e44d3c38ab2ff7c87a964996023c93c3007dee75d3c58c`  
		Last Modified: Fri, 25 Apr 2025 17:57:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c34b821668f733234ed002385791af28f4ea862a1ed172d1bc1a1d7bb8050c4`  
		Last Modified: Fri, 25 Apr 2025 17:57:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:8135c698d82ad1de505538338ea400f45f133591689e762afc7bf89360ec05ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:e553dd2df25d38f7c58c86916a6993a645db4aee95d621fd28621d010cbd4c39
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172513583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730c1c3823a4d7ec40c4ebea0fc753a14d18c46c6361f81bf3e112ba07697cd3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 17:56:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Apr 2025 17:56:08 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 17:56:08 GMT
ENV NATS_SERVER=2.10.28
# Fri, 25 Apr 2025 17:56:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.28/nats-server-v2.10.28-windows-amd64.zip
# Fri, 25 Apr 2025 17:56:10 GMT
ENV NATS_SERVER_SHASUM=98b8571231b00ebe0445cc7f317f6425c1fbc2edecd455949d37022e04281657
# Fri, 25 Apr 2025 17:56:42 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Apr 2025 17:56:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 25 Apr 2025 17:56:59 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 17:56:59 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 17:57:00 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 17:57:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d19d00d2094f2c58d7934a50b6ee709e72fc4ad29b81ff2bd7756adcbe037f0`  
		Last Modified: Fri, 25 Apr 2025 17:57:06 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcbb5d10b04f2cd56c2e0d040797aec57c5839f4805ee8b10c5e421efbdd889`  
		Last Modified: Fri, 25 Apr 2025 17:57:06 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3874a74574bed47a99842f9aba1c049223abb1e039618bd8c34e1dc0b7ba105e`  
		Last Modified: Fri, 25 Apr 2025 17:57:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892c56b140e7f00e97775014c34bcc6ebc61457d2d773c3efff5ca3c7cd6955`  
		Last Modified: Fri, 25 Apr 2025 17:57:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814cad5131cce2c37f6fc3d6008c9ac2db70d82f4f51db8dd505bccb0d34a695`  
		Last Modified: Fri, 25 Apr 2025 17:57:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2e203debf29ff5da8090a7d10db82622a25c539410dee10d6f2f0896677e9`  
		Last Modified: Fri, 25 Apr 2025 17:57:05 GMT  
		Size: 333.4 KB (333428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eaee7236ce6097c1288a8835d6ab940bd25fa2c68f30cee5fcf9523a4da3fc`  
		Last Modified: Fri, 25 Apr 2025 17:57:04 GMT  
		Size: 6.6 MB (6642099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c4806f2cfa9d4c464bc1cde03b5f71635b46fcb9787a60f7751771198489dc`  
		Last Modified: Fri, 25 Apr 2025 17:57:03 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5fc082a86b29f034924923fea5310e03058ae72bcca5830ff62c98c9a2c87a`  
		Last Modified: Fri, 25 Apr 2025 17:57:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c329770998d0a5276e44d3c38ab2ff7c87a964996023c93c3007dee75d3c58c`  
		Last Modified: Fri, 25 Apr 2025 17:57:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c34b821668f733234ed002385791af28f4ea862a1ed172d1bc1a1d7bb8050c4`  
		Last Modified: Fri, 25 Apr 2025 17:57:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29`

**does not exist** (yet?)

## `nats:2.10.29-alpine`

**does not exist** (yet?)

## `nats:2.10.29-alpine3.21`

**does not exist** (yet?)

## `nats:2.10.29-linux`

**does not exist** (yet?)

## `nats:2.10.29-nanoserver`

**does not exist** (yet?)

## `nats:2.10.29-nanoserver-1809`

**does not exist** (yet?)

## `nats:2.10.29-scratch`

**does not exist** (yet?)

## `nats:2.10.29-windowsservercore`

**does not exist** (yet?)

## `nats:2.10.29-windowsservercore-1809`

**does not exist** (yet?)

## `nats:2.11`

```console
$ docker pull nats@sha256:c234638526f0632617be436a8ea399a11214bb7579372d57060cb2a52d731d4e
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
	-	windows version 10.0.17763.7249; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:62b20bb99cf963ee9b0c78e26380a78a7dfa12eb8516d93bcf16b1f7eef252ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6305886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff853eebff5ea1827f264f2e22732dc892275c5bcd973db5058f4c4f0fe847e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d047c65ec95267487af401e091602880c16619e1ad4da3e7e962e8273ad589f3`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.3 MB (6305377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d3015f0a3ad1a5fecef389bb3fad1f3c80a49cbc71a62ab8d7db7516772ee`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:d6c4492d078b6bd4aeba68dd433b2a71adcb56e2e389703dc6af3f8a5af646ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663437ee61b0867cdc6f83e65e7751bb848af12bf9ccb7704573df8e32e95bd`

```dockerfile
```

-	Layers:
	-	`sha256:3d12f58e08eefe61f0ba37c703f5646cf255aac6449a7c65b2b43f5a7bacb48f`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:102aa9adbc4a30a8bab821dd4d77d548b6ea7a12f339b04a5f1c31747eca7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd05d7ce42a7ec76ac0d22af9a9659a44dca6a1cf2d735cd27fde215a0db0506`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:500b76d02a1b23c604281d5c714a2c35e9bb75cc592a66e885e0f5a6e37f01f7`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.0 MB (6019989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5024945048c8d9454d3d901d804208e05dee841a927428da15b56f6cda2dfe0f`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:f4642d3b2d1c595bd38ad079f450119842676b9c767451642ba468377601232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4adb1d0380f2178fe3652a824902cb41144dc0865ce28afe86223e2ddffd7`

```dockerfile
```

-	Layers:
	-	`sha256:f45013d27d687c2029f50a853a6baa027e4a22520d0eebd6226cf9f5c6dc409b`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:ea87c80ec3b41d7c75130d62bcef1a297124c3a88d268381ab2c37ba307d73ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c48211b5750cd5af18bc0f8b0cb7210dc7b7442b3dddff32f3ed46470a2da8c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ddc6cab03365e07f2c6d7f059130a7dc282d4412f564e8e2c0df08c8bc73b654`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.0 MB (6011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c437fd34339124b6d3297d0074974f27d9c07d30fe42d04fb34c41bef2c43d`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:fffc88ae5d459abcedbd5c5d7e5f8d19b8794c52ca6188ca9f0c52afb76757d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add82b13529e611ce4c97b4933e0e140c7f8ebd67c1b6fc44ab3f06b3251fe1`

```dockerfile
```

-	Layers:
	-	`sha256:12a9e12b0405328b67372116138c73054a00281115d2f51f53d6ab18acd37481`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5af5adb666cd46b7cd6eaa3475636fd706a459a4c271c2bae0f663afa2e456d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f919a929c1e17f23640fb47e0fc43b05ad1b484c6197cad307207530716bd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84272a2e628924f03610b8c1c3c6e85b489ac87f290d0f685882def49de9ecd1`  
		Last Modified: Fri, 25 Apr 2025 09:28:47 GMT  
		Size: 5.8 MB (5796146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755f468e87f12862403c7a2d37f55dff1372e29f88136c0ba50bff80618988d`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:ae261bb9805c736ed0d01a8af3f50ba6b75cd32b8a61a30bab0f3f38a7ad3397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f774c66ce1e2de4b74c2b0932ded1d5e97875334f0b5addf36ec617bdfcac`

```dockerfile
```

-	Layers:
	-	`sha256:6530cb0c6d8f35499127965fc373643eb042bd0291136f4fd82e137888b9cc27`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:f19a5e664bc3140ac051b51ff581345afc3974ca87e4377e64bcbbef2fc7837d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f90ce596ba2b9ffbe8c3d7836d7557f80f2eff80976acbda88bd45337bba78c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:edd6d59c7e29dc4aedef9eaa0785a9ced8aff83bf96b1f830e36dfa46f53be68`  
		Last Modified: Fri, 25 Apr 2025 09:28:46 GMT  
		Size: 5.8 MB (5775437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b27a2c43cc9286a86142e9071ba262afa4ac6a97ee4607fc43fa7f71ad97bc`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:a758d3a359b53da7c6fed233fe42ef45b42a0dcd90f901aaa06a8d7c4b4f9590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605196d61046805754dda3246312272f529b7bd6a95a6b62b1e216d706c9f69`

```dockerfile
```

-	Layers:
	-	`sha256:9ce5dab5019211eb3c4213657f39f0272e6a0e24a6bfbbf1980a7fbd9a5bc11b`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:dea1543c1392e56a44b03ee62f370fc7bfbadb871a4387ae8fe199ec98a3ff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5035eb69783eaf7b9b82362cf68d01382ec0f326297e8878be99af8f9871e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1a8280710dc7fc73564b9f4f49fd6b32365882791aa95344c40d406b0a13f25`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.1 MB (6142593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033cc57448f08a332bf30589df2ea6255c2b00b7b7c31da4e1663a19dc06c9b`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:9703f39141dc639788e95d00bfec218510dc9f2ab474dbb78470e2bc476212d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de3562e8db441250ba64bd95bc8b554fde7b751d0a567b223d312c5eaab6e00`

```dockerfile
```

-	Layers:
	-	`sha256:e260a2ca5c98ebac8d27b48ad48bdc5e6293498718316b387e725d6fed20cdf7`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de296657002e12709da3c23acf58143be37a698131dc288d4cc2c0309d43f108
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb13670aa8a73fbb2b50a99b8f822097b91002c77c9e1a26d7b154316e88ca0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:16:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:16:26 GMT
RUN cmd /S /C #(nop) COPY file:5e3840af0e267b510d2e54914f636d4b01f954b096bf81d459cc821ca4b3b468 in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b95fc9f036b2ce06ef6f75c0142446cf388b3fba5797ae076811cae5833b6`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be78d14ed5a916b3852e5c5b8f0c11c5ec282c35d533f16824dff33610aa794`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 6.5 MB (6479002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4903b008a32f8cb1eec6d3c17a357bb5a5292b67abdefef767f778101422a266`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48da8f54d5ccf3ef130af0a73b7b96919c2914ff036e75afef02bdbaa3434ad`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2a11075603c8b13618e5c581a166f4c1092208a1e0b6f6a1cd1cdd3e4d05d`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602c735353ba767b46b959a65eed16ad8ad55667c0a070c399b925fa4c2fea6`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:d66042bb0f58546eb0e075e0e09cfd8030c31775d48c4396d2b12aed8b5ba8dc
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
$ docker pull nats@sha256:cc459c48ef61cac3f0da86a77a704def265e4fff6cdeb187fff4809b25134243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b192c13111c95d3650c60ba63ec639b3b9ff0de658743bbe316c2c40ec87761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30972518cedbab8035d013f6db6bcf5c288a5fce5ac9f5c4a49ca2e2ff162a24`  
		Last Modified: Fri, 25 Apr 2025 17:48:19 GMT  
		Size: 6.8 MB (6765181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43044524251b03418bed238109a3814f628cc30699f91fc8ddb4e61d21600845`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11478db0daa336af1fe1f03f4d426ddc8348dfee6453c3739caf888706524ec2`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:117e29392d3bb1664288874dc5ce1a6743cefeb606a6586a2b6f1a800565b719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b540eafd19924a51341d6c7da202445ebab34b94b7cd9d88bb0c9c94fab48451`

```dockerfile
```

-	Layers:
	-	`sha256:43064c2c8a3ae9f3aee5a2655ad540820779e43c1ae8d89fe53fc27519ab0285`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:46fbf055d62fb4755f9183a500aadc9c4b044c87f5ce88626f2e1e1a986f0d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e3ef175b500d95e0c5dc1df1ba06def48741be20ac7f639752862b21a65093`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c836485cdab40ee18791138507d840e61a5dd6002da521973ae9f747f9cb341`  
		Last Modified: Fri, 25 Apr 2025 17:52:20 GMT  
		Size: 6.5 MB (6471410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3594a7da4ff92a9abd27dc550a385c8bbeb5e28fabc967958775a3df2a0f96`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d68568eb773d06ed29e95f236f5900e0f575a70c3ee006c543384607da0b11`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9d34bfb1916f9e9afecb9491c2e54a28cad04787d7b5e9317ee15100d051beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2490b80fcdf37dc28c990ea6049540776446b9c0973f77f88086356465f5cc0`

```dockerfile
```

-	Layers:
	-	`sha256:1b506a0fb93e704e1d6a0dbbac29ebc8f1dfb3cd813dd0f139df51422cc09052`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7aed6760d32ff60522af0fe9dbbf411bb35f190c908dd34c2e1c35918070388a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155e98f2eedb665b03ec44e3975582a728961e440a725c0f69f690fff44568db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a64ee773ee396bff692796312d9b7dcc7fb44f952d2c908b4d376f16d9581d`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 6.2 MB (6239702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af4a70c73af05cb86c61280f805804a2f0ace4ab434db07169117ce347ae30b`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1084beee85752d4193e9e16db34006162f5878a5031f7b0e7c7e5c80b8c6f27`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c691956323d34a6b74e2dfbe1ab1bab5de30fe964ff714970639a2a122dc0e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bba8ffd862cccff6f4f84b00f8c0f1017110269d10624b18160c9ce2909636`

```dockerfile
```

-	Layers:
	-	`sha256:39f5fb5aec21d1cc18c2b4652236b54c02c55583eafa99d8c1d100f42ea99352`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:5689e34a9410f0b3a43f78ac470d2064ad40e49d1f6dc79eeb818bd41a7be3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288603c30be026199e52b513d137fd803edbb3bae2c21940fd3ab4a9565d29bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776b5dd8bbdaa374387b6347dd990a3afb1db9fd111c9542ff347efb9e8e262`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 6.6 MB (6603909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b72da8f217ee883d534bf8b81b4968bfe98d01195019acf154437d744a24a30`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02335cc369df4703ddd8bc4151583583c53a1490c756e6665be8d4bf73e9232c`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b984b0eb744f6b7b434f640a3c00e4c0d780f4ec952703fd4369cbecbd8764f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0b39651391cbc684b373c09fe28338c152436a70a949d8a2ded08402f8fff2`

```dockerfile
```

-	Layers:
	-	`sha256:ae85806ecae7c531d7315c6ecefafc450b8facf67c31d55c74ace2c47cb0aa46`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.21`

```console
$ docker pull nats@sha256:d66042bb0f58546eb0e075e0e09cfd8030c31775d48c4396d2b12aed8b5ba8dc
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
$ docker pull nats@sha256:cc459c48ef61cac3f0da86a77a704def265e4fff6cdeb187fff4809b25134243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b192c13111c95d3650c60ba63ec639b3b9ff0de658743bbe316c2c40ec87761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30972518cedbab8035d013f6db6bcf5c288a5fce5ac9f5c4a49ca2e2ff162a24`  
		Last Modified: Fri, 25 Apr 2025 17:48:19 GMT  
		Size: 6.8 MB (6765181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43044524251b03418bed238109a3814f628cc30699f91fc8ddb4e61d21600845`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11478db0daa336af1fe1f03f4d426ddc8348dfee6453c3739caf888706524ec2`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:117e29392d3bb1664288874dc5ce1a6743cefeb606a6586a2b6f1a800565b719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b540eafd19924a51341d6c7da202445ebab34b94b7cd9d88bb0c9c94fab48451`

```dockerfile
```

-	Layers:
	-	`sha256:43064c2c8a3ae9f3aee5a2655ad540820779e43c1ae8d89fe53fc27519ab0285`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:46fbf055d62fb4755f9183a500aadc9c4b044c87f5ce88626f2e1e1a986f0d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e3ef175b500d95e0c5dc1df1ba06def48741be20ac7f639752862b21a65093`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c836485cdab40ee18791138507d840e61a5dd6002da521973ae9f747f9cb341`  
		Last Modified: Fri, 25 Apr 2025 17:52:20 GMT  
		Size: 6.5 MB (6471410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3594a7da4ff92a9abd27dc550a385c8bbeb5e28fabc967958775a3df2a0f96`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d68568eb773d06ed29e95f236f5900e0f575a70c3ee006c543384607da0b11`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:9d34bfb1916f9e9afecb9491c2e54a28cad04787d7b5e9317ee15100d051beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2490b80fcdf37dc28c990ea6049540776446b9c0973f77f88086356465f5cc0`

```dockerfile
```

-	Layers:
	-	`sha256:1b506a0fb93e704e1d6a0dbbac29ebc8f1dfb3cd813dd0f139df51422cc09052`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:7aed6760d32ff60522af0fe9dbbf411bb35f190c908dd34c2e1c35918070388a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155e98f2eedb665b03ec44e3975582a728961e440a725c0f69f690fff44568db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a64ee773ee396bff692796312d9b7dcc7fb44f952d2c908b4d376f16d9581d`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 6.2 MB (6239702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af4a70c73af05cb86c61280f805804a2f0ace4ab434db07169117ce347ae30b`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1084beee85752d4193e9e16db34006162f5878a5031f7b0e7c7e5c80b8c6f27`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c691956323d34a6b74e2dfbe1ab1bab5de30fe964ff714970639a2a122dc0e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bba8ffd862cccff6f4f84b00f8c0f1017110269d10624b18160c9ce2909636`

```dockerfile
```

-	Layers:
	-	`sha256:39f5fb5aec21d1cc18c2b4652236b54c02c55583eafa99d8c1d100f42ea99352`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:5689e34a9410f0b3a43f78ac470d2064ad40e49d1f6dc79eeb818bd41a7be3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288603c30be026199e52b513d137fd803edbb3bae2c21940fd3ab4a9565d29bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776b5dd8bbdaa374387b6347dd990a3afb1db9fd111c9542ff347efb9e8e262`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 6.6 MB (6603909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b72da8f217ee883d534bf8b81b4968bfe98d01195019acf154437d744a24a30`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02335cc369df4703ddd8bc4151583583c53a1490c756e6665be8d4bf73e9232c`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b984b0eb744f6b7b434f640a3c00e4c0d780f4ec952703fd4369cbecbd8764f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0b39651391cbc684b373c09fe28338c152436a70a949d8a2ded08402f8fff2`

```dockerfile
```

-	Layers:
	-	`sha256:ae85806ecae7c531d7315c6ecefafc450b8facf67c31d55c74ace2c47cb0aa46`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:960ff66153e19c70bd0c2f9f53fceb653b32381b2f6800e5a3b785ff73f650bd
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
$ docker pull nats@sha256:62b20bb99cf963ee9b0c78e26380a78a7dfa12eb8516d93bcf16b1f7eef252ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6305886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff853eebff5ea1827f264f2e22732dc892275c5bcd973db5058f4c4f0fe847e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d047c65ec95267487af401e091602880c16619e1ad4da3e7e962e8273ad589f3`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.3 MB (6305377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d3015f0a3ad1a5fecef389bb3fad1f3c80a49cbc71a62ab8d7db7516772ee`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d6c4492d078b6bd4aeba68dd433b2a71adcb56e2e389703dc6af3f8a5af646ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663437ee61b0867cdc6f83e65e7751bb848af12bf9ccb7704573df8e32e95bd`

```dockerfile
```

-	Layers:
	-	`sha256:3d12f58e08eefe61f0ba37c703f5646cf255aac6449a7c65b2b43f5a7bacb48f`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:102aa9adbc4a30a8bab821dd4d77d548b6ea7a12f339b04a5f1c31747eca7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd05d7ce42a7ec76ac0d22af9a9659a44dca6a1cf2d735cd27fde215a0db0506`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:500b76d02a1b23c604281d5c714a2c35e9bb75cc592a66e885e0f5a6e37f01f7`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.0 MB (6019989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5024945048c8d9454d3d901d804208e05dee841a927428da15b56f6cda2dfe0f`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f4642d3b2d1c595bd38ad079f450119842676b9c767451642ba468377601232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4adb1d0380f2178fe3652a824902cb41144dc0865ce28afe86223e2ddffd7`

```dockerfile
```

-	Layers:
	-	`sha256:f45013d27d687c2029f50a853a6baa027e4a22520d0eebd6226cf9f5c6dc409b`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ea87c80ec3b41d7c75130d62bcef1a297124c3a88d268381ab2c37ba307d73ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c48211b5750cd5af18bc0f8b0cb7210dc7b7442b3dddff32f3ed46470a2da8c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ddc6cab03365e07f2c6d7f059130a7dc282d4412f564e8e2c0df08c8bc73b654`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.0 MB (6011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c437fd34339124b6d3297d0074974f27d9c07d30fe42d04fb34c41bef2c43d`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:fffc88ae5d459abcedbd5c5d7e5f8d19b8794c52ca6188ca9f0c52afb76757d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add82b13529e611ce4c97b4933e0e140c7f8ebd67c1b6fc44ab3f06b3251fe1`

```dockerfile
```

-	Layers:
	-	`sha256:12a9e12b0405328b67372116138c73054a00281115d2f51f53d6ab18acd37481`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5af5adb666cd46b7cd6eaa3475636fd706a459a4c271c2bae0f663afa2e456d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f919a929c1e17f23640fb47e0fc43b05ad1b484c6197cad307207530716bd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84272a2e628924f03610b8c1c3c6e85b489ac87f290d0f685882def49de9ecd1`  
		Last Modified: Fri, 25 Apr 2025 09:28:47 GMT  
		Size: 5.8 MB (5796146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755f468e87f12862403c7a2d37f55dff1372e29f88136c0ba50bff80618988d`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ae261bb9805c736ed0d01a8af3f50ba6b75cd32b8a61a30bab0f3f38a7ad3397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f774c66ce1e2de4b74c2b0932ded1d5e97875334f0b5addf36ec617bdfcac`

```dockerfile
```

-	Layers:
	-	`sha256:6530cb0c6d8f35499127965fc373643eb042bd0291136f4fd82e137888b9cc27`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:f19a5e664bc3140ac051b51ff581345afc3974ca87e4377e64bcbbef2fc7837d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f90ce596ba2b9ffbe8c3d7836d7557f80f2eff80976acbda88bd45337bba78c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:edd6d59c7e29dc4aedef9eaa0785a9ced8aff83bf96b1f830e36dfa46f53be68`  
		Last Modified: Fri, 25 Apr 2025 09:28:46 GMT  
		Size: 5.8 MB (5775437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b27a2c43cc9286a86142e9071ba262afa4ac6a97ee4607fc43fa7f71ad97bc`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a758d3a359b53da7c6fed233fe42ef45b42a0dcd90f901aaa06a8d7c4b4f9590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605196d61046805754dda3246312272f529b7bd6a95a6b62b1e216d706c9f69`

```dockerfile
```

-	Layers:
	-	`sha256:9ce5dab5019211eb3c4213657f39f0272e6a0e24a6bfbbf1980a7fbd9a5bc11b`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:dea1543c1392e56a44b03ee62f370fc7bfbadb871a4387ae8fe199ec98a3ff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5035eb69783eaf7b9b82362cf68d01382ec0f326297e8878be99af8f9871e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1a8280710dc7fc73564b9f4f49fd6b32365882791aa95344c40d406b0a13f25`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.1 MB (6142593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033cc57448f08a332bf30589df2ea6255c2b00b7b7c31da4e1663a19dc06c9b`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9703f39141dc639788e95d00bfec218510dc9f2ab474dbb78470e2bc476212d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de3562e8db441250ba64bd95bc8b554fde7b751d0a567b223d312c5eaab6e00`

```dockerfile
```

-	Layers:
	-	`sha256:e260a2ca5c98ebac8d27b48ad48bdc5e6293498718316b387e725d6fed20cdf7`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:8ad5e6770c1df7c06e37c1855692061a4dec81c3bc4d289d3873a4554aa94d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.11-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de296657002e12709da3c23acf58143be37a698131dc288d4cc2c0309d43f108
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb13670aa8a73fbb2b50a99b8f822097b91002c77c9e1a26d7b154316e88ca0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:16:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:16:26 GMT
RUN cmd /S /C #(nop) COPY file:5e3840af0e267b510d2e54914f636d4b01f954b096bf81d459cc821ca4b3b468 in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b95fc9f036b2ce06ef6f75c0142446cf388b3fba5797ae076811cae5833b6`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be78d14ed5a916b3852e5c5b8f0c11c5ec282c35d533f16824dff33610aa794`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 6.5 MB (6479002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4903b008a32f8cb1eec6d3c17a357bb5a5292b67abdefef767f778101422a266`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48da8f54d5ccf3ef130af0a73b7b96919c2914ff036e75afef02bdbaa3434ad`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2a11075603c8b13618e5c581a166f4c1092208a1e0b6f6a1cd1cdd3e4d05d`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602c735353ba767b46b959a65eed16ad8ad55667c0a070c399b925fa4c2fea6`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-1809`

```console
$ docker pull nats@sha256:8ad5e6770c1df7c06e37c1855692061a4dec81c3bc4d289d3873a4554aa94d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.11-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de296657002e12709da3c23acf58143be37a698131dc288d4cc2c0309d43f108
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb13670aa8a73fbb2b50a99b8f822097b91002c77c9e1a26d7b154316e88ca0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:16:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:16:26 GMT
RUN cmd /S /C #(nop) COPY file:5e3840af0e267b510d2e54914f636d4b01f954b096bf81d459cc821ca4b3b468 in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b95fc9f036b2ce06ef6f75c0142446cf388b3fba5797ae076811cae5833b6`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be78d14ed5a916b3852e5c5b8f0c11c5ec282c35d533f16824dff33610aa794`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 6.5 MB (6479002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4903b008a32f8cb1eec6d3c17a357bb5a5292b67abdefef767f778101422a266`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48da8f54d5ccf3ef130af0a73b7b96919c2914ff036e75afef02bdbaa3434ad`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2a11075603c8b13618e5c581a166f4c1092208a1e0b6f6a1cd1cdd3e4d05d`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602c735353ba767b46b959a65eed16ad8ad55667c0a070c399b925fa4c2fea6`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:960ff66153e19c70bd0c2f9f53fceb653b32381b2f6800e5a3b785ff73f650bd
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
$ docker pull nats@sha256:62b20bb99cf963ee9b0c78e26380a78a7dfa12eb8516d93bcf16b1f7eef252ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6305886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff853eebff5ea1827f264f2e22732dc892275c5bcd973db5058f4c4f0fe847e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d047c65ec95267487af401e091602880c16619e1ad4da3e7e962e8273ad589f3`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.3 MB (6305377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d3015f0a3ad1a5fecef389bb3fad1f3c80a49cbc71a62ab8d7db7516772ee`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d6c4492d078b6bd4aeba68dd433b2a71adcb56e2e389703dc6af3f8a5af646ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663437ee61b0867cdc6f83e65e7751bb848af12bf9ccb7704573df8e32e95bd`

```dockerfile
```

-	Layers:
	-	`sha256:3d12f58e08eefe61f0ba37c703f5646cf255aac6449a7c65b2b43f5a7bacb48f`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:102aa9adbc4a30a8bab821dd4d77d548b6ea7a12f339b04a5f1c31747eca7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd05d7ce42a7ec76ac0d22af9a9659a44dca6a1cf2d735cd27fde215a0db0506`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:500b76d02a1b23c604281d5c714a2c35e9bb75cc592a66e885e0f5a6e37f01f7`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.0 MB (6019989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5024945048c8d9454d3d901d804208e05dee841a927428da15b56f6cda2dfe0f`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f4642d3b2d1c595bd38ad079f450119842676b9c767451642ba468377601232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4adb1d0380f2178fe3652a824902cb41144dc0865ce28afe86223e2ddffd7`

```dockerfile
```

-	Layers:
	-	`sha256:f45013d27d687c2029f50a853a6baa027e4a22520d0eebd6226cf9f5c6dc409b`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ea87c80ec3b41d7c75130d62bcef1a297124c3a88d268381ab2c37ba307d73ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c48211b5750cd5af18bc0f8b0cb7210dc7b7442b3dddff32f3ed46470a2da8c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ddc6cab03365e07f2c6d7f059130a7dc282d4412f564e8e2c0df08c8bc73b654`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.0 MB (6011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c437fd34339124b6d3297d0074974f27d9c07d30fe42d04fb34c41bef2c43d`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fffc88ae5d459abcedbd5c5d7e5f8d19b8794c52ca6188ca9f0c52afb76757d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add82b13529e611ce4c97b4933e0e140c7f8ebd67c1b6fc44ab3f06b3251fe1`

```dockerfile
```

-	Layers:
	-	`sha256:12a9e12b0405328b67372116138c73054a00281115d2f51f53d6ab18acd37481`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5af5adb666cd46b7cd6eaa3475636fd706a459a4c271c2bae0f663afa2e456d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f919a929c1e17f23640fb47e0fc43b05ad1b484c6197cad307207530716bd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84272a2e628924f03610b8c1c3c6e85b489ac87f290d0f685882def49de9ecd1`  
		Last Modified: Fri, 25 Apr 2025 09:28:47 GMT  
		Size: 5.8 MB (5796146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755f468e87f12862403c7a2d37f55dff1372e29f88136c0ba50bff80618988d`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ae261bb9805c736ed0d01a8af3f50ba6b75cd32b8a61a30bab0f3f38a7ad3397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f774c66ce1e2de4b74c2b0932ded1d5e97875334f0b5addf36ec617bdfcac`

```dockerfile
```

-	Layers:
	-	`sha256:6530cb0c6d8f35499127965fc373643eb042bd0291136f4fd82e137888b9cc27`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:f19a5e664bc3140ac051b51ff581345afc3974ca87e4377e64bcbbef2fc7837d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f90ce596ba2b9ffbe8c3d7836d7557f80f2eff80976acbda88bd45337bba78c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:edd6d59c7e29dc4aedef9eaa0785a9ced8aff83bf96b1f830e36dfa46f53be68`  
		Last Modified: Fri, 25 Apr 2025 09:28:46 GMT  
		Size: 5.8 MB (5775437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b27a2c43cc9286a86142e9071ba262afa4ac6a97ee4607fc43fa7f71ad97bc`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a758d3a359b53da7c6fed233fe42ef45b42a0dcd90f901aaa06a8d7c4b4f9590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605196d61046805754dda3246312272f529b7bd6a95a6b62b1e216d706c9f69`

```dockerfile
```

-	Layers:
	-	`sha256:9ce5dab5019211eb3c4213657f39f0272e6a0e24a6bfbbf1980a7fbd9a5bc11b`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:dea1543c1392e56a44b03ee62f370fc7bfbadb871a4387ae8fe199ec98a3ff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5035eb69783eaf7b9b82362cf68d01382ec0f326297e8878be99af8f9871e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1a8280710dc7fc73564b9f4f49fd6b32365882791aa95344c40d406b0a13f25`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.1 MB (6142593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033cc57448f08a332bf30589df2ea6255c2b00b7b7c31da4e1663a19dc06c9b`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9703f39141dc639788e95d00bfec218510dc9f2ab474dbb78470e2bc476212d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de3562e8db441250ba64bd95bc8b554fde7b751d0a567b223d312c5eaab6e00`

```dockerfile
```

-	Layers:
	-	`sha256:e260a2ca5c98ebac8d27b48ad48bdc5e6293498718316b387e725d6fed20cdf7`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:4ae66a1afca1485f7e5ef943f427685142d5ce607c4caecb5a0456e3a2625cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:864cd49a9319a3d243c7945cc4b1d847eeb62fc7ed3bff149dc06d3c11d80e98
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172714568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ee4030f14e129a49644c86c19599562d252f3c124fb474a5bb9ba9116a2acb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 17:53:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Apr 2025 17:53:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 17:53:18 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 17:53:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.2/nats-server-v2.11.2-windows-amd64.zip
# Fri, 25 Apr 2025 17:53:20 GMT
ENV NATS_SERVER_SHASUM=27bc84446495ed13983a86044d77cc24e4d5661a3ea3caaff3003c2d19dc3db8
# Fri, 25 Apr 2025 17:54:01 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Apr 2025 17:54:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 25 Apr 2025 17:54:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 17:54:22 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 17:54:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 17:54:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5220f32a15f4b9e4e60e00b789f7e5aed30ed16d768671ab81f2f7c847ce188`  
		Last Modified: Fri, 25 Apr 2025 17:54:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0adc223c6b3350c772df065f39904be980c1d151c04e822e6a524cae9a559b`  
		Last Modified: Fri, 25 Apr 2025 17:54:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e092e70456ee50a2b46c19beee1220448b3262ea35a4dc2762cf6dc92372d2`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe1399f73f5fcf68f18961cca3a08258165d8d8540bdeaabb55205a570b3ba0`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a098a1765813b5d39dd0a8b00f285c110efca73a5308620bad065b8fe9782`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9eb31776168317086fe75476b44574d1431a1e21f3d07a85279eafdd7341c`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 344.4 KB (344375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475c0b5a54a450e6b02e46614be9dfa7e5c0f7df6b4f4a34cf03889a90c6002`  
		Last Modified: Fri, 25 Apr 2025 17:54:27 GMT  
		Size: 6.8 MB (6832182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e6c6bd274e68a31e4fb7c629bd35c2bb6ef85a104202ba5864944cc76411b4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae5da4614649984507429fe2b6390a40f34095fd8fff099faee59172c99e03e`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc162497b3b567edf013a6577d06c352d56ab30ed7750e30f3161f5a2b5fa4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4ddd55fce7bccd5d5d53bfcb816dc5f0d980b8c904a6ef424c27bb6fc10a`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-1809`

```console
$ docker pull nats@sha256:4ae66a1afca1485f7e5ef943f427685142d5ce607c4caecb5a0456e3a2625cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:2.11-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:864cd49a9319a3d243c7945cc4b1d847eeb62fc7ed3bff149dc06d3c11d80e98
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172714568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ee4030f14e129a49644c86c19599562d252f3c124fb474a5bb9ba9116a2acb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 17:53:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Apr 2025 17:53:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 17:53:18 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 17:53:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.2/nats-server-v2.11.2-windows-amd64.zip
# Fri, 25 Apr 2025 17:53:20 GMT
ENV NATS_SERVER_SHASUM=27bc84446495ed13983a86044d77cc24e4d5661a3ea3caaff3003c2d19dc3db8
# Fri, 25 Apr 2025 17:54:01 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Apr 2025 17:54:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 25 Apr 2025 17:54:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 17:54:22 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 17:54:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 17:54:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5220f32a15f4b9e4e60e00b789f7e5aed30ed16d768671ab81f2f7c847ce188`  
		Last Modified: Fri, 25 Apr 2025 17:54:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0adc223c6b3350c772df065f39904be980c1d151c04e822e6a524cae9a559b`  
		Last Modified: Fri, 25 Apr 2025 17:54:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e092e70456ee50a2b46c19beee1220448b3262ea35a4dc2762cf6dc92372d2`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe1399f73f5fcf68f18961cca3a08258165d8d8540bdeaabb55205a570b3ba0`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a098a1765813b5d39dd0a8b00f285c110efca73a5308620bad065b8fe9782`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9eb31776168317086fe75476b44574d1431a1e21f3d07a85279eafdd7341c`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 344.4 KB (344375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475c0b5a54a450e6b02e46614be9dfa7e5c0f7df6b4f4a34cf03889a90c6002`  
		Last Modified: Fri, 25 Apr 2025 17:54:27 GMT  
		Size: 6.8 MB (6832182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e6c6bd274e68a31e4fb7c629bd35c2bb6ef85a104202ba5864944cc76411b4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae5da4614649984507429fe2b6390a40f34095fd8fff099faee59172c99e03e`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc162497b3b567edf013a6577d06c352d56ab30ed7750e30f3161f5a2b5fa4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4ddd55fce7bccd5d5d53bfcb816dc5f0d980b8c904a6ef424c27bb6fc10a`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.3`

**does not exist** (yet?)

## `nats:2.11.3-alpine`

**does not exist** (yet?)

## `nats:2.11.3-alpine3.21`

**does not exist** (yet?)

## `nats:2.11.3-linux`

**does not exist** (yet?)

## `nats:2.11.3-nanoserver`

**does not exist** (yet?)

## `nats:2.11.3-nanoserver-1809`

**does not exist** (yet?)

## `nats:2.11.3-scratch`

**does not exist** (yet?)

## `nats:2.11.3-windowsservercore`

**does not exist** (yet?)

## `nats:2.11.3-windowsservercore-1809`

**does not exist** (yet?)

## `nats:alpine`

```console
$ docker pull nats@sha256:d66042bb0f58546eb0e075e0e09cfd8030c31775d48c4396d2b12aed8b5ba8dc
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
$ docker pull nats@sha256:cc459c48ef61cac3f0da86a77a704def265e4fff6cdeb187fff4809b25134243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b192c13111c95d3650c60ba63ec639b3b9ff0de658743bbe316c2c40ec87761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30972518cedbab8035d013f6db6bcf5c288a5fce5ac9f5c4a49ca2e2ff162a24`  
		Last Modified: Fri, 25 Apr 2025 17:48:19 GMT  
		Size: 6.8 MB (6765181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43044524251b03418bed238109a3814f628cc30699f91fc8ddb4e61d21600845`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11478db0daa336af1fe1f03f4d426ddc8348dfee6453c3739caf888706524ec2`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:117e29392d3bb1664288874dc5ce1a6743cefeb606a6586a2b6f1a800565b719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b540eafd19924a51341d6c7da202445ebab34b94b7cd9d88bb0c9c94fab48451`

```dockerfile
```

-	Layers:
	-	`sha256:43064c2c8a3ae9f3aee5a2655ad540820779e43c1ae8d89fe53fc27519ab0285`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:46fbf055d62fb4755f9183a500aadc9c4b044c87f5ce88626f2e1e1a986f0d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e3ef175b500d95e0c5dc1df1ba06def48741be20ac7f639752862b21a65093`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c836485cdab40ee18791138507d840e61a5dd6002da521973ae9f747f9cb341`  
		Last Modified: Fri, 25 Apr 2025 17:52:20 GMT  
		Size: 6.5 MB (6471410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3594a7da4ff92a9abd27dc550a385c8bbeb5e28fabc967958775a3df2a0f96`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d68568eb773d06ed29e95f236f5900e0f575a70c3ee006c543384607da0b11`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9d34bfb1916f9e9afecb9491c2e54a28cad04787d7b5e9317ee15100d051beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2490b80fcdf37dc28c990ea6049540776446b9c0973f77f88086356465f5cc0`

```dockerfile
```

-	Layers:
	-	`sha256:1b506a0fb93e704e1d6a0dbbac29ebc8f1dfb3cd813dd0f139df51422cc09052`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:7aed6760d32ff60522af0fe9dbbf411bb35f190c908dd34c2e1c35918070388a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155e98f2eedb665b03ec44e3975582a728961e440a725c0f69f690fff44568db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a64ee773ee396bff692796312d9b7dcc7fb44f952d2c908b4d376f16d9581d`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 6.2 MB (6239702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af4a70c73af05cb86c61280f805804a2f0ace4ab434db07169117ce347ae30b`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1084beee85752d4193e9e16db34006162f5878a5031f7b0e7c7e5c80b8c6f27`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c691956323d34a6b74e2dfbe1ab1bab5de30fe964ff714970639a2a122dc0e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bba8ffd862cccff6f4f84b00f8c0f1017110269d10624b18160c9ce2909636`

```dockerfile
```

-	Layers:
	-	`sha256:39f5fb5aec21d1cc18c2b4652236b54c02c55583eafa99d8c1d100f42ea99352`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:5689e34a9410f0b3a43f78ac470d2064ad40e49d1f6dc79eeb818bd41a7be3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288603c30be026199e52b513d137fd803edbb3bae2c21940fd3ab4a9565d29bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776b5dd8bbdaa374387b6347dd990a3afb1db9fd111c9542ff347efb9e8e262`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 6.6 MB (6603909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b72da8f217ee883d534bf8b81b4968bfe98d01195019acf154437d744a24a30`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02335cc369df4703ddd8bc4151583583c53a1490c756e6665be8d4bf73e9232c`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b984b0eb744f6b7b434f640a3c00e4c0d780f4ec952703fd4369cbecbd8764f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0b39651391cbc684b373c09fe28338c152436a70a949d8a2ded08402f8fff2`

```dockerfile
```

-	Layers:
	-	`sha256:ae85806ecae7c531d7315c6ecefafc450b8facf67c31d55c74ace2c47cb0aa46`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.21`

```console
$ docker pull nats@sha256:d66042bb0f58546eb0e075e0e09cfd8030c31775d48c4396d2b12aed8b5ba8dc
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
$ docker pull nats@sha256:cc459c48ef61cac3f0da86a77a704def265e4fff6cdeb187fff4809b25134243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10408397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b192c13111c95d3650c60ba63ec639b3b9ff0de658743bbe316c2c40ec87761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30972518cedbab8035d013f6db6bcf5c288a5fce5ac9f5c4a49ca2e2ff162a24`  
		Last Modified: Fri, 25 Apr 2025 17:48:19 GMT  
		Size: 6.8 MB (6765181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43044524251b03418bed238109a3814f628cc30699f91fc8ddb4e61d21600845`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11478db0daa336af1fe1f03f4d426ddc8348dfee6453c3739caf888706524ec2`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:117e29392d3bb1664288874dc5ce1a6743cefeb606a6586a2b6f1a800565b719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b540eafd19924a51341d6c7da202445ebab34b94b7cd9d88bb0c9c94fab48451`

```dockerfile
```

-	Layers:
	-	`sha256:43064c2c8a3ae9f3aee5a2655ad540820779e43c1ae8d89fe53fc27519ab0285`  
		Last Modified: Fri, 25 Apr 2025 17:48:18 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:b25ce7d7cfb629d1a132ae08b8fd84da4ab34c224fc57a9366f4f7e8284a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9849553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc00749e465a4c423af0395ea8a620f5184198a26aa70c550afb018dcd620d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53314fd665bd0c97ace20b7fb2ca1b46ecfdd7426150f8745639bb7704613d5a`  
		Last Modified: Fri, 25 Apr 2025 17:47:34 GMT  
		Size: 6.5 MB (6483851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefa71e52d2f6e7b13aac0c8fe523facca0507ac8e8b180b168eeadfd046b89`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c198696667425fcef5f606fda093ce31277d14ed9b5dc1592fb47511143d5052`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:20a327f5442b5e1a069fb161658d8b9436e0f0ce2df3802ad9d74362036c2210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2f873973386278768ee962ed71409b2376682ae823894072e19be8cde68680`

```dockerfile
```

-	Layers:
	-	`sha256:9122357572edf020a23a1bbf0fbe37650762d41d728dfaccb594f7e5890cbd2d`  
		Last Modified: Fri, 25 Apr 2025 17:47:33 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:46fbf055d62fb4755f9183a500aadc9c4b044c87f5ce88626f2e1e1a986f0d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9570501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e3ef175b500d95e0c5dc1df1ba06def48741be20ac7f639752862b21a65093`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c836485cdab40ee18791138507d840e61a5dd6002da521973ae9f747f9cb341`  
		Last Modified: Fri, 25 Apr 2025 17:52:20 GMT  
		Size: 6.5 MB (6471410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3594a7da4ff92a9abd27dc550a385c8bbeb5e28fabc967958775a3df2a0f96`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d68568eb773d06ed29e95f236f5900e0f575a70c3ee006c543384607da0b11`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:9d34bfb1916f9e9afecb9491c2e54a28cad04787d7b5e9317ee15100d051beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2490b80fcdf37dc28c990ea6049540776446b9c0973f77f88086356465f5cc0`

```dockerfile
```

-	Layers:
	-	`sha256:1b506a0fb93e704e1d6a0dbbac29ebc8f1dfb3cd813dd0f139df51422cc09052`  
		Last Modified: Fri, 25 Apr 2025 17:52:19 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4fe60f222966727f3e81dbb3bf2aaec58c7c8b573afbe318f6cb2c70c19f37c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10254225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d5d918ca9a0f7dd7c056851f2898f207c48f854da7954fc8fafc8fd1aa3021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb0921652e8042f634bdcb7812f9a2ed40e073970e14a940960350b775dbf`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 6.3 MB (6260226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc226874bc3060e6e916fa3ef948812c54a012b6081a27eaab55addfec8b7473`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a33259d9c5e7a6a6b42c8482e8bc6930e1a713671c0cf2fd1b5c879eef01`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:fda84d5581ce64cec49def3b469b26e717bf64d28a817656b19e16da89e9ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a714d7bd3b6fd55a075f56b50fa0da44cf6616089161edf7a648ba47af3256`

```dockerfile
```

-	Layers:
	-	`sha256:5f55a5edc5478bd7d7c9bc7e0763ad4dee93ecffafd3ed2f7702e7ee06ae75b0`  
		Last Modified: Fri, 25 Apr 2025 17:47:30 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:7aed6760d32ff60522af0fe9dbbf411bb35f190c908dd34c2e1c35918070388a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9815017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155e98f2eedb665b03ec44e3975582a728961e440a725c0f69f690fff44568db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a64ee773ee396bff692796312d9b7dcc7fb44f952d2c908b4d376f16d9581d`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 6.2 MB (6239702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af4a70c73af05cb86c61280f805804a2f0ace4ab434db07169117ce347ae30b`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1084beee85752d4193e9e16db34006162f5878a5031f7b0e7c7e5c80b8c6f27`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:c691956323d34a6b74e2dfbe1ab1bab5de30fe964ff714970639a2a122dc0e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bba8ffd862cccff6f4f84b00f8c0f1017110269d10624b18160c9ce2909636`

```dockerfile
```

-	Layers:
	-	`sha256:39f5fb5aec21d1cc18c2b4652236b54c02c55583eafa99d8c1d100f42ea99352`  
		Last Modified: Fri, 25 Apr 2025 17:48:21 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:5689e34a9410f0b3a43f78ac470d2064ad40e49d1f6dc79eeb818bd41a7be3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10072448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288603c30be026199e52b513d137fd803edbb3bae2c21940fd3ab4a9565d29bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 09:27:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da0a4b9d57d2a4c2439f0c8731b7e1ef8f0a7f2a1edf643d5f50a73ffc0c31f9' ;; 		armhf) natsArch='arm6'; sha256='2370e8d794acb0f176be0f0885f9930fa9d8d1276f15162eb8db336467279bc1' ;; 		armv7) natsArch='arm7'; sha256='46b038e57ad586f05342dcd3b29a2c2597217c19172a916eef9187170f024ad8' ;; 		x86_64) natsArch='amd64'; sha256='a123c8e43abe5ca8f0bff9393547f20f4bbac6fc0fb3c586ec031855911c414a' ;; 		x86) natsArch='386'; sha256='03bf7db9323c453b1257c3a43a21fcd5a975a2cc136c4bbeab7c0e815939e37e' ;; 		s390x) natsArch='s390x'; sha256='eb40e4a843124198b7e8625b7cccbd52810d63db17e1557d59681f5f29be5a98' ;; 		ppc64le) natsArch='ppc64le'; sha256='28e2afbca41dffe453507a993291560bfc57c6f43fe435604f894c3d91426dd0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776b5dd8bbdaa374387b6347dd990a3afb1db9fd111c9542ff347efb9e8e262`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 6.6 MB (6603909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b72da8f217ee883d534bf8b81b4968bfe98d01195019acf154437d744a24a30`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02335cc369df4703ddd8bc4151583583c53a1490c756e6665be8d4bf73e9232c`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:b984b0eb744f6b7b434f640a3c00e4c0d780f4ec952703fd4369cbecbd8764f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0b39651391cbc684b373c09fe28338c152436a70a949d8a2ded08402f8fff2`

```dockerfile
```

-	Layers:
	-	`sha256:ae85806ecae7c531d7315c6ecefafc450b8facf67c31d55c74ace2c47cb0aa46`  
		Last Modified: Fri, 25 Apr 2025 17:48:14 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:c234638526f0632617be436a8ea399a11214bb7579372d57060cb2a52d731d4e
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
	-	windows version 10.0.17763.7249; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:62b20bb99cf963ee9b0c78e26380a78a7dfa12eb8516d93bcf16b1f7eef252ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6305886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff853eebff5ea1827f264f2e22732dc892275c5bcd973db5058f4c4f0fe847e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d047c65ec95267487af401e091602880c16619e1ad4da3e7e962e8273ad589f3`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.3 MB (6305377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d3015f0a3ad1a5fecef389bb3fad1f3c80a49cbc71a62ab8d7db7516772ee`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:d6c4492d078b6bd4aeba68dd433b2a71adcb56e2e389703dc6af3f8a5af646ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663437ee61b0867cdc6f83e65e7751bb848af12bf9ccb7704573df8e32e95bd`

```dockerfile
```

-	Layers:
	-	`sha256:3d12f58e08eefe61f0ba37c703f5646cf255aac6449a7c65b2b43f5a7bacb48f`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:102aa9adbc4a30a8bab821dd4d77d548b6ea7a12f339b04a5f1c31747eca7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd05d7ce42a7ec76ac0d22af9a9659a44dca6a1cf2d735cd27fde215a0db0506`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:500b76d02a1b23c604281d5c714a2c35e9bb75cc592a66e885e0f5a6e37f01f7`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.0 MB (6019989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5024945048c8d9454d3d901d804208e05dee841a927428da15b56f6cda2dfe0f`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f4642d3b2d1c595bd38ad079f450119842676b9c767451642ba468377601232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4adb1d0380f2178fe3652a824902cb41144dc0865ce28afe86223e2ddffd7`

```dockerfile
```

-	Layers:
	-	`sha256:f45013d27d687c2029f50a853a6baa027e4a22520d0eebd6226cf9f5c6dc409b`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:ea87c80ec3b41d7c75130d62bcef1a297124c3a88d268381ab2c37ba307d73ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c48211b5750cd5af18bc0f8b0cb7210dc7b7442b3dddff32f3ed46470a2da8c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ddc6cab03365e07f2c6d7f059130a7dc282d4412f564e8e2c0df08c8bc73b654`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.0 MB (6011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c437fd34339124b6d3297d0074974f27d9c07d30fe42d04fb34c41bef2c43d`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:fffc88ae5d459abcedbd5c5d7e5f8d19b8794c52ca6188ca9f0c52afb76757d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add82b13529e611ce4c97b4933e0e140c7f8ebd67c1b6fc44ab3f06b3251fe1`

```dockerfile
```

-	Layers:
	-	`sha256:12a9e12b0405328b67372116138c73054a00281115d2f51f53d6ab18acd37481`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5af5adb666cd46b7cd6eaa3475636fd706a459a4c271c2bae0f663afa2e456d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f919a929c1e17f23640fb47e0fc43b05ad1b484c6197cad307207530716bd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84272a2e628924f03610b8c1c3c6e85b489ac87f290d0f685882def49de9ecd1`  
		Last Modified: Fri, 25 Apr 2025 09:28:47 GMT  
		Size: 5.8 MB (5796146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755f468e87f12862403c7a2d37f55dff1372e29f88136c0ba50bff80618988d`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:ae261bb9805c736ed0d01a8af3f50ba6b75cd32b8a61a30bab0f3f38a7ad3397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f774c66ce1e2de4b74c2b0932ded1d5e97875334f0b5addf36ec617bdfcac`

```dockerfile
```

-	Layers:
	-	`sha256:6530cb0c6d8f35499127965fc373643eb042bd0291136f4fd82e137888b9cc27`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:f19a5e664bc3140ac051b51ff581345afc3974ca87e4377e64bcbbef2fc7837d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f90ce596ba2b9ffbe8c3d7836d7557f80f2eff80976acbda88bd45337bba78c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:edd6d59c7e29dc4aedef9eaa0785a9ced8aff83bf96b1f830e36dfa46f53be68`  
		Last Modified: Fri, 25 Apr 2025 09:28:46 GMT  
		Size: 5.8 MB (5775437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b27a2c43cc9286a86142e9071ba262afa4ac6a97ee4607fc43fa7f71ad97bc`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a758d3a359b53da7c6fed233fe42ef45b42a0dcd90f901aaa06a8d7c4b4f9590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605196d61046805754dda3246312272f529b7bd6a95a6b62b1e216d706c9f69`

```dockerfile
```

-	Layers:
	-	`sha256:9ce5dab5019211eb3c4213657f39f0272e6a0e24a6bfbbf1980a7fbd9a5bc11b`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:dea1543c1392e56a44b03ee62f370fc7bfbadb871a4387ae8fe199ec98a3ff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5035eb69783eaf7b9b82362cf68d01382ec0f326297e8878be99af8f9871e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1a8280710dc7fc73564b9f4f49fd6b32365882791aa95344c40d406b0a13f25`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.1 MB (6142593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033cc57448f08a332bf30589df2ea6255c2b00b7b7c31da4e1663a19dc06c9b`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:9703f39141dc639788e95d00bfec218510dc9f2ab474dbb78470e2bc476212d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de3562e8db441250ba64bd95bc8b554fde7b751d0a567b223d312c5eaab6e00`

```dockerfile
```

-	Layers:
	-	`sha256:e260a2ca5c98ebac8d27b48ad48bdc5e6293498718316b387e725d6fed20cdf7`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de296657002e12709da3c23acf58143be37a698131dc288d4cc2c0309d43f108
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb13670aa8a73fbb2b50a99b8f822097b91002c77c9e1a26d7b154316e88ca0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:16:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:16:26 GMT
RUN cmd /S /C #(nop) COPY file:5e3840af0e267b510d2e54914f636d4b01f954b096bf81d459cc821ca4b3b468 in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b95fc9f036b2ce06ef6f75c0142446cf388b3fba5797ae076811cae5833b6`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be78d14ed5a916b3852e5c5b8f0c11c5ec282c35d533f16824dff33610aa794`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 6.5 MB (6479002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4903b008a32f8cb1eec6d3c17a357bb5a5292b67abdefef767f778101422a266`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48da8f54d5ccf3ef130af0a73b7b96919c2914ff036e75afef02bdbaa3434ad`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2a11075603c8b13618e5c581a166f4c1092208a1e0b6f6a1cd1cdd3e4d05d`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602c735353ba767b46b959a65eed16ad8ad55667c0a070c399b925fa4c2fea6`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:960ff66153e19c70bd0c2f9f53fceb653b32381b2f6800e5a3b785ff73f650bd
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
$ docker pull nats@sha256:62b20bb99cf963ee9b0c78e26380a78a7dfa12eb8516d93bcf16b1f7eef252ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6305886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff853eebff5ea1827f264f2e22732dc892275c5bcd973db5058f4c4f0fe847e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d047c65ec95267487af401e091602880c16619e1ad4da3e7e962e8273ad589f3`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.3 MB (6305377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d3015f0a3ad1a5fecef389bb3fad1f3c80a49cbc71a62ab8d7db7516772ee`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:d6c4492d078b6bd4aeba68dd433b2a71adcb56e2e389703dc6af3f8a5af646ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663437ee61b0867cdc6f83e65e7751bb848af12bf9ccb7704573df8e32e95bd`

```dockerfile
```

-	Layers:
	-	`sha256:3d12f58e08eefe61f0ba37c703f5646cf255aac6449a7c65b2b43f5a7bacb48f`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:102aa9adbc4a30a8bab821dd4d77d548b6ea7a12f339b04a5f1c31747eca7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd05d7ce42a7ec76ac0d22af9a9659a44dca6a1cf2d735cd27fde215a0db0506`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:500b76d02a1b23c604281d5c714a2c35e9bb75cc592a66e885e0f5a6e37f01f7`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.0 MB (6019989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5024945048c8d9454d3d901d804208e05dee841a927428da15b56f6cda2dfe0f`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f4642d3b2d1c595bd38ad079f450119842676b9c767451642ba468377601232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4adb1d0380f2178fe3652a824902cb41144dc0865ce28afe86223e2ddffd7`

```dockerfile
```

-	Layers:
	-	`sha256:f45013d27d687c2029f50a853a6baa027e4a22520d0eebd6226cf9f5c6dc409b`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:ea87c80ec3b41d7c75130d62bcef1a297124c3a88d268381ab2c37ba307d73ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c48211b5750cd5af18bc0f8b0cb7210dc7b7442b3dddff32f3ed46470a2da8c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ddc6cab03365e07f2c6d7f059130a7dc282d4412f564e8e2c0df08c8bc73b654`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.0 MB (6011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c437fd34339124b6d3297d0074974f27d9c07d30fe42d04fb34c41bef2c43d`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:fffc88ae5d459abcedbd5c5d7e5f8d19b8794c52ca6188ca9f0c52afb76757d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add82b13529e611ce4c97b4933e0e140c7f8ebd67c1b6fc44ab3f06b3251fe1`

```dockerfile
```

-	Layers:
	-	`sha256:12a9e12b0405328b67372116138c73054a00281115d2f51f53d6ab18acd37481`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5af5adb666cd46b7cd6eaa3475636fd706a459a4c271c2bae0f663afa2e456d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f919a929c1e17f23640fb47e0fc43b05ad1b484c6197cad307207530716bd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84272a2e628924f03610b8c1c3c6e85b489ac87f290d0f685882def49de9ecd1`  
		Last Modified: Fri, 25 Apr 2025 09:28:47 GMT  
		Size: 5.8 MB (5796146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755f468e87f12862403c7a2d37f55dff1372e29f88136c0ba50bff80618988d`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:ae261bb9805c736ed0d01a8af3f50ba6b75cd32b8a61a30bab0f3f38a7ad3397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f774c66ce1e2de4b74c2b0932ded1d5e97875334f0b5addf36ec617bdfcac`

```dockerfile
```

-	Layers:
	-	`sha256:6530cb0c6d8f35499127965fc373643eb042bd0291136f4fd82e137888b9cc27`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:f19a5e664bc3140ac051b51ff581345afc3974ca87e4377e64bcbbef2fc7837d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f90ce596ba2b9ffbe8c3d7836d7557f80f2eff80976acbda88bd45337bba78c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:edd6d59c7e29dc4aedef9eaa0785a9ced8aff83bf96b1f830e36dfa46f53be68`  
		Last Modified: Fri, 25 Apr 2025 09:28:46 GMT  
		Size: 5.8 MB (5775437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b27a2c43cc9286a86142e9071ba262afa4ac6a97ee4607fc43fa7f71ad97bc`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:a758d3a359b53da7c6fed233fe42ef45b42a0dcd90f901aaa06a8d7c4b4f9590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605196d61046805754dda3246312272f529b7bd6a95a6b62b1e216d706c9f69`

```dockerfile
```

-	Layers:
	-	`sha256:9ce5dab5019211eb3c4213657f39f0272e6a0e24a6bfbbf1980a7fbd9a5bc11b`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:dea1543c1392e56a44b03ee62f370fc7bfbadb871a4387ae8fe199ec98a3ff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5035eb69783eaf7b9b82362cf68d01382ec0f326297e8878be99af8f9871e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1a8280710dc7fc73564b9f4f49fd6b32365882791aa95344c40d406b0a13f25`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.1 MB (6142593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033cc57448f08a332bf30589df2ea6255c2b00b7b7c31da4e1663a19dc06c9b`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:9703f39141dc639788e95d00bfec218510dc9f2ab474dbb78470e2bc476212d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de3562e8db441250ba64bd95bc8b554fde7b751d0a567b223d312c5eaab6e00`

```dockerfile
```

-	Layers:
	-	`sha256:e260a2ca5c98ebac8d27b48ad48bdc5e6293498718316b387e725d6fed20cdf7`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:8ad5e6770c1df7c06e37c1855692061a4dec81c3bc4d289d3873a4554aa94d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de296657002e12709da3c23acf58143be37a698131dc288d4cc2c0309d43f108
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb13670aa8a73fbb2b50a99b8f822097b91002c77c9e1a26d7b154316e88ca0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:16:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:16:26 GMT
RUN cmd /S /C #(nop) COPY file:5e3840af0e267b510d2e54914f636d4b01f954b096bf81d459cc821ca4b3b468 in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b95fc9f036b2ce06ef6f75c0142446cf388b3fba5797ae076811cae5833b6`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be78d14ed5a916b3852e5c5b8f0c11c5ec282c35d533f16824dff33610aa794`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 6.5 MB (6479002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4903b008a32f8cb1eec6d3c17a357bb5a5292b67abdefef767f778101422a266`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48da8f54d5ccf3ef130af0a73b7b96919c2914ff036e75afef02bdbaa3434ad`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2a11075603c8b13618e5c581a166f4c1092208a1e0b6f6a1cd1cdd3e4d05d`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602c735353ba767b46b959a65eed16ad8ad55667c0a070c399b925fa4c2fea6`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:8ad5e6770c1df7c06e37c1855692061a4dec81c3bc4d289d3873a4554aa94d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:de296657002e12709da3c23acf58143be37a698131dc288d4cc2c0309d43f108
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115237047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb13670aa8a73fbb2b50a99b8f822097b91002c77c9e1a26d7b154316e88ca0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 18:16:24 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 18:16:26 GMT
RUN cmd /S /C #(nop) COPY file:5e3840af0e267b510d2e54914f636d4b01f954b096bf81d459cc821ca4b3b468 in C:\nats-server.exe 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 18:16:27 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 18:16:28 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b95fc9f036b2ce06ef6f75c0142446cf388b3fba5797ae076811cae5833b6`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be78d14ed5a916b3852e5c5b8f0c11c5ec282c35d533f16824dff33610aa794`  
		Last Modified: Fri, 25 Apr 2025 18:16:33 GMT  
		Size: 6.5 MB (6479002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4903b008a32f8cb1eec6d3c17a357bb5a5292b67abdefef767f778101422a266`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48da8f54d5ccf3ef130af0a73b7b96919c2914ff036e75afef02bdbaa3434ad`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2a11075603c8b13618e5c581a166f4c1092208a1e0b6f6a1cd1cdd3e4d05d`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9602c735353ba767b46b959a65eed16ad8ad55667c0a070c399b925fa4c2fea6`  
		Last Modified: Fri, 25 Apr 2025 18:16:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:960ff66153e19c70bd0c2f9f53fceb653b32381b2f6800e5a3b785ff73f650bd
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
$ docker pull nats@sha256:62b20bb99cf963ee9b0c78e26380a78a7dfa12eb8516d93bcf16b1f7eef252ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6305886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff853eebff5ea1827f264f2e22732dc892275c5bcd973db5058f4c4f0fe847e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d047c65ec95267487af401e091602880c16619e1ad4da3e7e962e8273ad589f3`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.3 MB (6305377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d3015f0a3ad1a5fecef389bb3fad1f3c80a49cbc71a62ab8d7db7516772ee`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d6c4492d078b6bd4aeba68dd433b2a71adcb56e2e389703dc6af3f8a5af646ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663437ee61b0867cdc6f83e65e7751bb848af12bf9ccb7704573df8e32e95bd`

```dockerfile
```

-	Layers:
	-	`sha256:3d12f58e08eefe61f0ba37c703f5646cf255aac6449a7c65b2b43f5a7bacb48f`  
		Last Modified: Fri, 25 Apr 2025 18:08:26 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:102aa9adbc4a30a8bab821dd4d77d548b6ea7a12f339b04a5f1c31747eca7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6020498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd05d7ce42a7ec76ac0d22af9a9659a44dca6a1cf2d735cd27fde215a0db0506`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:500b76d02a1b23c604281d5c714a2c35e9bb75cc592a66e885e0f5a6e37f01f7`  
		Last Modified: Fri, 25 Apr 2025 09:28:48 GMT  
		Size: 6.0 MB (6019989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5024945048c8d9454d3d901d804208e05dee841a927428da15b56f6cda2dfe0f`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f4642d3b2d1c595bd38ad079f450119842676b9c767451642ba468377601232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4adb1d0380f2178fe3652a824902cb41144dc0865ce28afe86223e2ddffd7`

```dockerfile
```

-	Layers:
	-	`sha256:f45013d27d687c2029f50a853a6baa027e4a22520d0eebd6226cf9f5c6dc409b`  
		Last Modified: Fri, 25 Apr 2025 17:49:12 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:ea87c80ec3b41d7c75130d62bcef1a297124c3a88d268381ab2c37ba307d73ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6011602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c48211b5750cd5af18bc0f8b0cb7210dc7b7442b3dddff32f3ed46470a2da8c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ddc6cab03365e07f2c6d7f059130a7dc282d4412f564e8e2c0df08c8bc73b654`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.0 MB (6011093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c437fd34339124b6d3297d0074974f27d9c07d30fe42d04fb34c41bef2c43d`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fffc88ae5d459abcedbd5c5d7e5f8d19b8794c52ca6188ca9f0c52afb76757d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add82b13529e611ce4c97b4933e0e140c7f8ebd67c1b6fc44ab3f06b3251fe1`

```dockerfile
```

-	Layers:
	-	`sha256:12a9e12b0405328b67372116138c73054a00281115d2f51f53d6ab18acd37481`  
		Last Modified: Fri, 25 Apr 2025 18:07:48 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5af5adb666cd46b7cd6eaa3475636fd706a459a4c271c2bae0f663afa2e456d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5796656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f919a929c1e17f23640fb47e0fc43b05ad1b484c6197cad307207530716bd38`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84272a2e628924f03610b8c1c3c6e85b489ac87f290d0f685882def49de9ecd1`  
		Last Modified: Fri, 25 Apr 2025 09:28:47 GMT  
		Size: 5.8 MB (5796146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755f468e87f12862403c7a2d37f55dff1372e29f88136c0ba50bff80618988d`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ae261bb9805c736ed0d01a8af3f50ba6b75cd32b8a61a30bab0f3f38a7ad3397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08f774c66ce1e2de4b74c2b0932ded1d5e97875334f0b5addf36ec617bdfcac`

```dockerfile
```

-	Layers:
	-	`sha256:6530cb0c6d8f35499127965fc373643eb042bd0291136f4fd82e137888b9cc27`  
		Last Modified: Fri, 25 Apr 2025 17:52:13 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:f19a5e664bc3140ac051b51ff581345afc3974ca87e4377e64bcbbef2fc7837d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5775947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f90ce596ba2b9ffbe8c3d7836d7557f80f2eff80976acbda88bd45337bba78c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:edd6d59c7e29dc4aedef9eaa0785a9ced8aff83bf96b1f830e36dfa46f53be68`  
		Last Modified: Fri, 25 Apr 2025 09:28:46 GMT  
		Size: 5.8 MB (5775437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b27a2c43cc9286a86142e9071ba262afa4ac6a97ee4607fc43fa7f71ad97bc`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a758d3a359b53da7c6fed233fe42ef45b42a0dcd90f901aaa06a8d7c4b4f9590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b605196d61046805754dda3246312272f529b7bd6a95a6b62b1e216d706c9f69`

```dockerfile
```

-	Layers:
	-	`sha256:9ce5dab5019211eb3c4213657f39f0272e6a0e24a6bfbbf1980a7fbd9a5bc11b`  
		Last Modified: Fri, 25 Apr 2025 18:08:30 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:dea1543c1392e56a44b03ee62f370fc7bfbadb871a4387ae8fe199ec98a3ff56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6143101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f5035eb69783eaf7b9b82362cf68d01382ec0f326297e8878be99af8f9871e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 25 Apr 2025 09:27:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 25 Apr 2025 09:27:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 25 Apr 2025 09:27:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 25 Apr 2025 09:27:46 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 25 Apr 2025 09:27:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d1a8280710dc7fc73564b9f4f49fd6b32365882791aa95344c40d406b0a13f25`  
		Last Modified: Fri, 25 Apr 2025 09:28:49 GMT  
		Size: 6.1 MB (6142593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033cc57448f08a332bf30589df2ea6255c2b00b7b7c31da4e1663a19dc06c9b`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9703f39141dc639788e95d00bfec218510dc9f2ab474dbb78470e2bc476212d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de3562e8db441250ba64bd95bc8b554fde7b751d0a567b223d312c5eaab6e00`

```dockerfile
```

-	Layers:
	-	`sha256:e260a2ca5c98ebac8d27b48ad48bdc5e6293498718316b387e725d6fed20cdf7`  
		Last Modified: Fri, 25 Apr 2025 18:08:24 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:4ae66a1afca1485f7e5ef943f427685142d5ce607c4caecb5a0456e3a2625cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:864cd49a9319a3d243c7945cc4b1d847eeb62fc7ed3bff149dc06d3c11d80e98
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172714568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ee4030f14e129a49644c86c19599562d252f3c124fb474a5bb9ba9116a2acb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 17:53:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Apr 2025 17:53:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 17:53:18 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 17:53:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.2/nats-server-v2.11.2-windows-amd64.zip
# Fri, 25 Apr 2025 17:53:20 GMT
ENV NATS_SERVER_SHASUM=27bc84446495ed13983a86044d77cc24e4d5661a3ea3caaff3003c2d19dc3db8
# Fri, 25 Apr 2025 17:54:01 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Apr 2025 17:54:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 25 Apr 2025 17:54:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 17:54:22 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 17:54:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 17:54:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5220f32a15f4b9e4e60e00b789f7e5aed30ed16d768671ab81f2f7c847ce188`  
		Last Modified: Fri, 25 Apr 2025 17:54:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0adc223c6b3350c772df065f39904be980c1d151c04e822e6a524cae9a559b`  
		Last Modified: Fri, 25 Apr 2025 17:54:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e092e70456ee50a2b46c19beee1220448b3262ea35a4dc2762cf6dc92372d2`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe1399f73f5fcf68f18961cca3a08258165d8d8540bdeaabb55205a570b3ba0`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a098a1765813b5d39dd0a8b00f285c110efca73a5308620bad065b8fe9782`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9eb31776168317086fe75476b44574d1431a1e21f3d07a85279eafdd7341c`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 344.4 KB (344375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475c0b5a54a450e6b02e46614be9dfa7e5c0f7df6b4f4a34cf03889a90c6002`  
		Last Modified: Fri, 25 Apr 2025 17:54:27 GMT  
		Size: 6.8 MB (6832182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e6c6bd274e68a31e4fb7c629bd35c2bb6ef85a104202ba5864944cc76411b4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae5da4614649984507429fe2b6390a40f34095fd8fff099faee59172c99e03e`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc162497b3b567edf013a6577d06c352d56ab30ed7750e30f3161f5a2b5fa4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4ddd55fce7bccd5d5d53bfcb816dc5f0d980b8c904a6ef424c27bb6fc10a`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:4ae66a1afca1485f7e5ef943f427685142d5ce607c4caecb5a0456e3a2625cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull nats@sha256:864cd49a9319a3d243c7945cc4b1d847eeb62fc7ed3bff149dc06d3c11d80e98
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2172714568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ee4030f14e129a49644c86c19599562d252f3c124fb474a5bb9ba9116a2acb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 25 Apr 2025 17:53:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Apr 2025 17:53:17 GMT
ENV NATS_DOCKERIZED=1
# Fri, 25 Apr 2025 17:53:18 GMT
ENV NATS_SERVER=2.11.2
# Fri, 25 Apr 2025 17:53:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.2/nats-server-v2.11.2-windows-amd64.zip
# Fri, 25 Apr 2025 17:53:20 GMT
ENV NATS_SERVER_SHASUM=27bc84446495ed13983a86044d77cc24e4d5661a3ea3caaff3003c2d19dc3db8
# Fri, 25 Apr 2025 17:54:01 GMT
RUN Set-PSDebug -Trace 2
# Fri, 25 Apr 2025 17:54:20 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Fri, 25 Apr 2025 17:54:21 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Fri, 25 Apr 2025 17:54:22 GMT
EXPOSE 4222 6222 8222
# Fri, 25 Apr 2025 17:54:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Fri, 25 Apr 2025 17:54:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5220f32a15f4b9e4e60e00b789f7e5aed30ed16d768671ab81f2f7c847ce188`  
		Last Modified: Fri, 25 Apr 2025 17:54:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0adc223c6b3350c772df065f39904be980c1d151c04e822e6a524cae9a559b`  
		Last Modified: Fri, 25 Apr 2025 17:54:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e092e70456ee50a2b46c19beee1220448b3262ea35a4dc2762cf6dc92372d2`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe1399f73f5fcf68f18961cca3a08258165d8d8540bdeaabb55205a570b3ba0`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a098a1765813b5d39dd0a8b00f285c110efca73a5308620bad065b8fe9782`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9eb31776168317086fe75476b44574d1431a1e21f3d07a85279eafdd7341c`  
		Last Modified: Fri, 25 Apr 2025 17:54:28 GMT  
		Size: 344.4 KB (344375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475c0b5a54a450e6b02e46614be9dfa7e5c0f7df6b4f4a34cf03889a90c6002`  
		Last Modified: Fri, 25 Apr 2025 17:54:27 GMT  
		Size: 6.8 MB (6832182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e6c6bd274e68a31e4fb7c629bd35c2bb6ef85a104202ba5864944cc76411b4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae5da4614649984507429fe2b6390a40f34095fd8fff099faee59172c99e03e`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc162497b3b567edf013a6577d06c352d56ab30ed7750e30f3161f5a2b5fa4`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4b4ddd55fce7bccd5d5d53bfcb816dc5f0d980b8c904a6ef424c27bb6fc10a`  
		Last Modified: Fri, 25 Apr 2025 17:54:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
