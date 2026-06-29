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
-	[`nats:2.12`](#nats212)
-	[`nats:2.12-alpine`](#nats212-alpine)
-	[`nats:2.12-alpine3.22`](#nats212-alpine322)
-	[`nats:2.12-linux`](#nats212-linux)
-	[`nats:2.12-nanoserver`](#nats212-nanoserver)
-	[`nats:2.12-nanoserver-ltsc2022`](#nats212-nanoserver-ltsc2022)
-	[`nats:2.12-scratch`](#nats212-scratch)
-	[`nats:2.12-windowsservercore`](#nats212-windowsservercore)
-	[`nats:2.12-windowsservercore-ltsc2022`](#nats212-windowsservercore-ltsc2022)
-	[`nats:2.12.12`](#nats21212)
-	[`nats:2.12.12-alpine`](#nats21212-alpine)
-	[`nats:2.12.12-alpine3.22`](#nats21212-alpine322)
-	[`nats:2.12.12-linux`](#nats21212-linux)
-	[`nats:2.12.12-nanoserver`](#nats21212-nanoserver)
-	[`nats:2.12.12-nanoserver-ltsc2022`](#nats21212-nanoserver-ltsc2022)
-	[`nats:2.12.12-scratch`](#nats21212-scratch)
-	[`nats:2.12.12-windowsservercore`](#nats21212-windowsservercore)
-	[`nats:2.12.12-windowsservercore-ltsc2022`](#nats21212-windowsservercore-ltsc2022)
-	[`nats:2.14`](#nats214)
-	[`nats:2.14-alpine`](#nats214-alpine)
-	[`nats:2.14-alpine3.22`](#nats214-alpine322)
-	[`nats:2.14-linux`](#nats214-linux)
-	[`nats:2.14-nanoserver`](#nats214-nanoserver)
-	[`nats:2.14-nanoserver-ltsc2022`](#nats214-nanoserver-ltsc2022)
-	[`nats:2.14-scratch`](#nats214-scratch)
-	[`nats:2.14-windowsservercore`](#nats214-windowsservercore)
-	[`nats:2.14-windowsservercore-ltsc2022`](#nats214-windowsservercore-ltsc2022)
-	[`nats:2.14.3`](#nats2143)
-	[`nats:2.14.3-alpine`](#nats2143-alpine)
-	[`nats:2.14.3-alpine3.22`](#nats2143-alpine322)
-	[`nats:2.14.3-linux`](#nats2143-linux)
-	[`nats:2.14.3-nanoserver`](#nats2143-nanoserver)
-	[`nats:2.14.3-nanoserver-ltsc2022`](#nats2143-nanoserver-ltsc2022)
-	[`nats:2.14.3-scratch`](#nats2143-scratch)
-	[`nats:2.14.3-windowsservercore`](#nats2143-windowsservercore)
-	[`nats:2.14.3-windowsservercore-ltsc2022`](#nats2143-windowsservercore-ltsc2022)
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
$ docker pull nats@sha256:bbfbb6c4cdaeb8a2e3ca57d3de30463a66a6c5181f324f3b680bcf858833d377
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
	-	windows version 10.0.20348.5256; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:65713a1834b75d00256f847cc7b8db5fea12121bbf341edfff76f84a76b56ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29535378bebe76ff33b25a0ee21ab0fe2346cb9bbd179ece59ab2f37f36e3c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b33128ccd2d9960d0a0ac0d31682c1928d1d17ca25caf107fa914eee12f346`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:82f0a5ca9b68dc2a87b53a0f1f9e9f5121208dbd998d0b36d56e9d11aba98464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ed450408ac2b61ff0b451c4f09ce61f26a1b3eb58a44c10cc2082ca924201`

```dockerfile
```

-	Layers:
	-	`sha256:4c738c96a15989941f46c5a6a4392bfbc566b311520062f8d56aa0637d39400a`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:340c3f31c2400ff9ce93e99a056a2f65376bb08bb66291dd626c08ce54ca68d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558fc4503cb023f4b5007d465ea651c8f3af04a4b3a5b6348ccd9c78575dfe55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:18 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055cbd39cde58dda5cd03328a647a1e169ff8116a012137ce777d015565a44d7`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:4f0459213b2c44994bdbfc9af813a5f71ef1d00fba9c4e79cb15c7e2beefb67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63163d0fb60b2575e901b5e80f128020e9f3a5a2c610f865f3a750ea54a7fcdb`

```dockerfile
```

-	Layers:
	-	`sha256:527462491f781bce7f70496c4c9f2301b87cd5239c9f3ef5e83120fdb7370326`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7b3118869b74523b091cdec795dac3a3e7f7a69b0da2a0b5e1c4efbacb592fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6521bf98b02b2cf398c50c51930a34edf1c9da6a12a609b5d4ab2c01aab4f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:43:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:43:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:44:00 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:44:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3113ca534280e6c8acb2de55307064e1f8c2dce3fbe561d92a361be6754b8a`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:237ed08805072b07e68a19e104f07b16b22f4d8df845090f99164f396c4b7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf263674818d6f6280a468f63ff41db03882ca617c12d4e40e13f8920327b702`

```dockerfile
```

-	Layers:
	-	`sha256:db257913eec8f718988e940693bf52d60408882e903f08f9f45925a0f08e79e7`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cfd028112c875c7eda23860b3554e5e990356a1057bb17dd09a20a243372f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3cf3c1e911779b9fbfe69ca703bb69a2b7407e6227e3f9b70ebbca6f0a54d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:33 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:33 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46654056ed2549b3cbb7f0ff49c14926dda4483bfcae2e5b2ae45112ce5291d0`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:99443208695008b0853014ff29715108f78d0ab8da563be4c3e5e722cf8e3b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2669aa13c7dc6695ab85bcc4e2eca03332d9e1771e9a50b9d6b5155f28a0110b`

```dockerfile
```

-	Layers:
	-	`sha256:fe5804167a3e8df278aea8ff5b75538f93e08c74ce18b116e6b7a40f075195e8`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:52e2eb5749be9656b0a896ee1e1791cdf66fc1efc72030d918ce83f28c1f4b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0846d8047c28872a68ffbc2831a19d2d15e0289633332b837db0f98247d37b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:6db89f1127caa8acb7e34214a9efc141739ecc0f49277d1680be7ab685b74a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe761e7f1baacb1015ae345dadf921feb545775f29fa241d4656fc0b7b0e944`

```dockerfile
```

-	Layers:
	-	`sha256:815bb78a9d851bd4d69340210b112479e7ac60e52474e9a946253c2311a5e235`  
		Last Modified: Mon, 22 Jun 2026 21:47:18 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:fdd9c60e91e3e32e1d99b1e31894da2950c99194fb8a6ec7f24bc0ed7f490049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6e32f278fd364210b5378b9c775f37669ca37425057b87159a3fe2d10fd82d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:03 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba8cfbf4bada82bc12acb2b704ab7a199791bf0fb2e58d599e28f76ebe3d6`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:7e8a69f4f646da4a5a0227992c72916a23aab04732d77ebc784c36f884b53ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56240e620c437c2607b84cf23a0fcbe4e1c4d843764c2fcae214dc17dea78285`

```dockerfile
```

-	Layers:
	-	`sha256:122ffef264b9f423559e1565ffdf589e592490e2a938e73680b7bb7ed7542d9a`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:0badb754748fd4de2327f7cca2a86ef00b94e6c26569e80e707b706f27325db5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131036450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47805c9ad0d2cf7cad50fc23b59da1d61256f0205ddc87a79286268a11862c2a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:30 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5ccd531a60c4bbb1082621a0a21646b6494b0e2f612e79a6778943268beed`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c651bbee8aea515b8055fcdde339bcbf1c6bb43eec92b29e344e9f52afb2d`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 7.0 MB (7032997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944c27da9e6c3f4181c98a5de2c3e6ac2ba74a492184ddf9cb918f6077e0ed1`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bb394cd41fc7b65a1b4279ab910c2b79893e79ff5968ec47b31269a7f6886c`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a49be050f1fb2cdeb4cdc180ef6c139faf00bc0adf3dda61f6e7b185ebed5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c55e36e6b13a9d983ce1406964734930adac2e1fa2707cebafdef63520d5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:3c66911d53d63e76dd733c7994ca544c28602cafc68f27fbf47dbb8e37205e57
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
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:afa0021fd5534b5898b5a146edea9264c8db26144b792c10a5315a35bbbac5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10482561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b85446ce3f424e4511a6ec5bcc77ecab084eb56464f1f1d28046674ab67a651`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677c5f86a68cf2ce1fdf51d3b53c56b92e7fbe3b67443d993c093aac9e6a00f`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 7.0 MB (6986793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea037dcf8136a7791f9e560bda59f20a5e40ee8d447c9b81a75253956c52d2c`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91efd4d63f2001f13a850754a14e04788257c1dbe8f26cf095f7cc64ca2b5913`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7d4eebf896ed7b471bfb246e8823a02079e74eb6195ffc6edbc4246539be1a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4004102106793942ddb14115cf0e0684cc23e759a6ffca0eb4c60dd06d05b2fc`

```dockerfile
```

-	Layers:
	-	`sha256:cd7784700079db7a9f22cc194e5d89197a178370899405a829e82b5a633e3afe`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:91683fb37479895c178784386781a757532946afd57131bb405b062581ebef75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10188544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49ae72c112bb15690a11d8a5b7aa735cd4245c99549bce10acb4dc49a476ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8b795a8aa2f5335674b36741b17ce192443d940da95f3bbd597b70531689e3`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 7.0 MB (6977963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5097219f08bd67d8fa2e25a5a479e8bd0385d6216ab6343a4aa1875eb26304`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8e33bc51c0528dbfa912e61fdcfc8e25b5a0c5ed8ff2e87ebc145a65aa1605`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:753a5ea794f4139e119be983748b07d2258ba219fca43ac667a4533c6e30a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b52454a96ab80fa5715d09b55b91072a66c893f75f0d94f5e43b01767f6c542`

```dockerfile
```

-	Layers:
	-	`sha256:a85da325cca4163e5d72d726f4f96a446323aa0b460ea8f228953398ba6b6171`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4267586f8d1941e8955323b0014cba3b61f65881b4c4c20de688fbe1c5fea804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10724412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f145de50057f413858c406b87310468fc4bd3effd1f88e329cf02fea0239e1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cfbf804236b512a4b9944ec56130b32a28b0a4b77458c90970f66f3a589254`  
		Last Modified: Mon, 22 Jun 2026 19:47:17 GMT  
		Size: 6.6 MB (6602958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c950a70aceecc1179a9c484d238f8ec42132ddf44f71978023a2ac0e56fc0`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f2ccaf61966a62729b5a1cfbdf7e05d864310ac230029a8a9cf60d0967ec7`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5deeca0a3264b5d656b04246f1c17f72ca74115b5de8e356adbe225c80c755bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51798bd8628e715c409906689a2cf6fac8b1fee280fd2920de1e6a379bc4c6`

```dockerfile
```

-	Layers:
	-	`sha256:f0614b048154314f9962518fc36f249b39de8d985648d33ef1ce4bb9369f3f4a`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:3c66911d53d63e76dd733c7994ca544c28602cafc68f27fbf47dbb8e37205e57
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
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:afa0021fd5534b5898b5a146edea9264c8db26144b792c10a5315a35bbbac5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10482561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b85446ce3f424e4511a6ec5bcc77ecab084eb56464f1f1d28046674ab67a651`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677c5f86a68cf2ce1fdf51d3b53c56b92e7fbe3b67443d993c093aac9e6a00f`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 7.0 MB (6986793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea037dcf8136a7791f9e560bda59f20a5e40ee8d447c9b81a75253956c52d2c`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91efd4d63f2001f13a850754a14e04788257c1dbe8f26cf095f7cc64ca2b5913`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7d4eebf896ed7b471bfb246e8823a02079e74eb6195ffc6edbc4246539be1a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4004102106793942ddb14115cf0e0684cc23e759a6ffca0eb4c60dd06d05b2fc`

```dockerfile
```

-	Layers:
	-	`sha256:cd7784700079db7a9f22cc194e5d89197a178370899405a829e82b5a633e3afe`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:91683fb37479895c178784386781a757532946afd57131bb405b062581ebef75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10188544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49ae72c112bb15690a11d8a5b7aa735cd4245c99549bce10acb4dc49a476ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8b795a8aa2f5335674b36741b17ce192443d940da95f3bbd597b70531689e3`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 7.0 MB (6977963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5097219f08bd67d8fa2e25a5a479e8bd0385d6216ab6343a4aa1875eb26304`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8e33bc51c0528dbfa912e61fdcfc8e25b5a0c5ed8ff2e87ebc145a65aa1605`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:753a5ea794f4139e119be983748b07d2258ba219fca43ac667a4533c6e30a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b52454a96ab80fa5715d09b55b91072a66c893f75f0d94f5e43b01767f6c542`

```dockerfile
```

-	Layers:
	-	`sha256:a85da325cca4163e5d72d726f4f96a446323aa0b460ea8f228953398ba6b6171`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4267586f8d1941e8955323b0014cba3b61f65881b4c4c20de688fbe1c5fea804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10724412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f145de50057f413858c406b87310468fc4bd3effd1f88e329cf02fea0239e1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cfbf804236b512a4b9944ec56130b32a28b0a4b77458c90970f66f3a589254`  
		Last Modified: Mon, 22 Jun 2026 19:47:17 GMT  
		Size: 6.6 MB (6602958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c950a70aceecc1179a9c484d238f8ec42132ddf44f71978023a2ac0e56fc0`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f2ccaf61966a62729b5a1cfbdf7e05d864310ac230029a8a9cf60d0967ec7`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5deeca0a3264b5d656b04246f1c17f72ca74115b5de8e356adbe225c80c755bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51798bd8628e715c409906689a2cf6fac8b1fee280fd2920de1e6a379bc4c6`

```dockerfile
```

-	Layers:
	-	`sha256:f0614b048154314f9962518fc36f249b39de8d985648d33ef1ce4bb9369f3f4a`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:3b7b5f689b8b9055b95f9eedc3448de69c16808d427fa6295e5a6df3fb45e910
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
$ docker pull nats@sha256:65713a1834b75d00256f847cc7b8db5fea12121bbf341edfff76f84a76b56ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29535378bebe76ff33b25a0ee21ab0fe2346cb9bbd179ece59ab2f37f36e3c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b33128ccd2d9960d0a0ac0d31682c1928d1d17ca25caf107fa914eee12f346`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:82f0a5ca9b68dc2a87b53a0f1f9e9f5121208dbd998d0b36d56e9d11aba98464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ed450408ac2b61ff0b451c4f09ce61f26a1b3eb58a44c10cc2082ca924201`

```dockerfile
```

-	Layers:
	-	`sha256:4c738c96a15989941f46c5a6a4392bfbc566b311520062f8d56aa0637d39400a`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:340c3f31c2400ff9ce93e99a056a2f65376bb08bb66291dd626c08ce54ca68d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558fc4503cb023f4b5007d465ea651c8f3af04a4b3a5b6348ccd9c78575dfe55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:18 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055cbd39cde58dda5cd03328a647a1e169ff8116a012137ce777d015565a44d7`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4f0459213b2c44994bdbfc9af813a5f71ef1d00fba9c4e79cb15c7e2beefb67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63163d0fb60b2575e901b5e80f128020e9f3a5a2c610f865f3a750ea54a7fcdb`

```dockerfile
```

-	Layers:
	-	`sha256:527462491f781bce7f70496c4c9f2301b87cd5239c9f3ef5e83120fdb7370326`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7b3118869b74523b091cdec795dac3a3e7f7a69b0da2a0b5e1c4efbacb592fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6521bf98b02b2cf398c50c51930a34edf1c9da6a12a609b5d4ab2c01aab4f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:43:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:43:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:44:00 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:44:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3113ca534280e6c8acb2de55307064e1f8c2dce3fbe561d92a361be6754b8a`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:237ed08805072b07e68a19e104f07b16b22f4d8df845090f99164f396c4b7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf263674818d6f6280a468f63ff41db03882ca617c12d4e40e13f8920327b702`

```dockerfile
```

-	Layers:
	-	`sha256:db257913eec8f718988e940693bf52d60408882e903f08f9f45925a0f08e79e7`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cfd028112c875c7eda23860b3554e5e990356a1057bb17dd09a20a243372f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3cf3c1e911779b9fbfe69ca703bb69a2b7407e6227e3f9b70ebbca6f0a54d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:33 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:33 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46654056ed2549b3cbb7f0ff49c14926dda4483bfcae2e5b2ae45112ce5291d0`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:99443208695008b0853014ff29715108f78d0ab8da563be4c3e5e722cf8e3b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2669aa13c7dc6695ab85bcc4e2eca03332d9e1771e9a50b9d6b5155f28a0110b`

```dockerfile
```

-	Layers:
	-	`sha256:fe5804167a3e8df278aea8ff5b75538f93e08c74ce18b116e6b7a40f075195e8`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:52e2eb5749be9656b0a896ee1e1791cdf66fc1efc72030d918ce83f28c1f4b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0846d8047c28872a68ffbc2831a19d2d15e0289633332b837db0f98247d37b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6db89f1127caa8acb7e34214a9efc141739ecc0f49277d1680be7ab685b74a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe761e7f1baacb1015ae345dadf921feb545775f29fa241d4656fc0b7b0e944`

```dockerfile
```

-	Layers:
	-	`sha256:815bb78a9d851bd4d69340210b112479e7ac60e52474e9a946253c2311a5e235`  
		Last Modified: Mon, 22 Jun 2026 21:47:18 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:fdd9c60e91e3e32e1d99b1e31894da2950c99194fb8a6ec7f24bc0ed7f490049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6e32f278fd364210b5378b9c775f37669ca37425057b87159a3fe2d10fd82d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:03 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba8cfbf4bada82bc12acb2b704ab7a199791bf0fb2e58d599e28f76ebe3d6`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7e8a69f4f646da4a5a0227992c72916a23aab04732d77ebc784c36f884b53ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56240e620c437c2607b84cf23a0fcbe4e1c4d843764c2fcae214dc17dea78285`

```dockerfile
```

-	Layers:
	-	`sha256:122ffef264b9f423559e1565ffdf589e592490e2a938e73680b7bb7ed7542d9a`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:9622b8c98b2488b8efd76eefe88e2b019d542d6de0e04db7af8d21e067f39ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:0badb754748fd4de2327f7cca2a86ef00b94e6c26569e80e707b706f27325db5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131036450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47805c9ad0d2cf7cad50fc23b59da1d61256f0205ddc87a79286268a11862c2a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:30 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5ccd531a60c4bbb1082621a0a21646b6494b0e2f612e79a6778943268beed`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c651bbee8aea515b8055fcdde339bcbf1c6bb43eec92b29e344e9f52afb2d`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 7.0 MB (7032997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944c27da9e6c3f4181c98a5de2c3e6ac2ba74a492184ddf9cb918f6077e0ed1`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bb394cd41fc7b65a1b4279ab910c2b79893e79ff5968ec47b31269a7f6886c`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a49be050f1fb2cdeb4cdc180ef6c139faf00bc0adf3dda61f6e7b185ebed5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c55e36e6b13a9d983ce1406964734930adac2e1fa2707cebafdef63520d5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:9622b8c98b2488b8efd76eefe88e2b019d542d6de0e04db7af8d21e067f39ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:0badb754748fd4de2327f7cca2a86ef00b94e6c26569e80e707b706f27325db5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131036450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47805c9ad0d2cf7cad50fc23b59da1d61256f0205ddc87a79286268a11862c2a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:30 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5ccd531a60c4bbb1082621a0a21646b6494b0e2f612e79a6778943268beed`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c651bbee8aea515b8055fcdde339bcbf1c6bb43eec92b29e344e9f52afb2d`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 7.0 MB (7032997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944c27da9e6c3f4181c98a5de2c3e6ac2ba74a492184ddf9cb918f6077e0ed1`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bb394cd41fc7b65a1b4279ab910c2b79893e79ff5968ec47b31269a7f6886c`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a49be050f1fb2cdeb4cdc180ef6c139faf00bc0adf3dda61f6e7b185ebed5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c55e36e6b13a9d983ce1406964734930adac2e1fa2707cebafdef63520d5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:3b7b5f689b8b9055b95f9eedc3448de69c16808d427fa6295e5a6df3fb45e910
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
$ docker pull nats@sha256:65713a1834b75d00256f847cc7b8db5fea12121bbf341edfff76f84a76b56ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29535378bebe76ff33b25a0ee21ab0fe2346cb9bbd179ece59ab2f37f36e3c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b33128ccd2d9960d0a0ac0d31682c1928d1d17ca25caf107fa914eee12f346`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:82f0a5ca9b68dc2a87b53a0f1f9e9f5121208dbd998d0b36d56e9d11aba98464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ed450408ac2b61ff0b451c4f09ce61f26a1b3eb58a44c10cc2082ca924201`

```dockerfile
```

-	Layers:
	-	`sha256:4c738c96a15989941f46c5a6a4392bfbc566b311520062f8d56aa0637d39400a`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:340c3f31c2400ff9ce93e99a056a2f65376bb08bb66291dd626c08ce54ca68d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558fc4503cb023f4b5007d465ea651c8f3af04a4b3a5b6348ccd9c78575dfe55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:18 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055cbd39cde58dda5cd03328a647a1e169ff8116a012137ce777d015565a44d7`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4f0459213b2c44994bdbfc9af813a5f71ef1d00fba9c4e79cb15c7e2beefb67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63163d0fb60b2575e901b5e80f128020e9f3a5a2c610f865f3a750ea54a7fcdb`

```dockerfile
```

-	Layers:
	-	`sha256:527462491f781bce7f70496c4c9f2301b87cd5239c9f3ef5e83120fdb7370326`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7b3118869b74523b091cdec795dac3a3e7f7a69b0da2a0b5e1c4efbacb592fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6521bf98b02b2cf398c50c51930a34edf1c9da6a12a609b5d4ab2c01aab4f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:43:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:43:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:44:00 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:44:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3113ca534280e6c8acb2de55307064e1f8c2dce3fbe561d92a361be6754b8a`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:237ed08805072b07e68a19e104f07b16b22f4d8df845090f99164f396c4b7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf263674818d6f6280a468f63ff41db03882ca617c12d4e40e13f8920327b702`

```dockerfile
```

-	Layers:
	-	`sha256:db257913eec8f718988e940693bf52d60408882e903f08f9f45925a0f08e79e7`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cfd028112c875c7eda23860b3554e5e990356a1057bb17dd09a20a243372f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3cf3c1e911779b9fbfe69ca703bb69a2b7407e6227e3f9b70ebbca6f0a54d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:33 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:33 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46654056ed2549b3cbb7f0ff49c14926dda4483bfcae2e5b2ae45112ce5291d0`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:99443208695008b0853014ff29715108f78d0ab8da563be4c3e5e722cf8e3b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2669aa13c7dc6695ab85bcc4e2eca03332d9e1771e9a50b9d6b5155f28a0110b`

```dockerfile
```

-	Layers:
	-	`sha256:fe5804167a3e8df278aea8ff5b75538f93e08c74ce18b116e6b7a40f075195e8`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:52e2eb5749be9656b0a896ee1e1791cdf66fc1efc72030d918ce83f28c1f4b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0846d8047c28872a68ffbc2831a19d2d15e0289633332b837db0f98247d37b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6db89f1127caa8acb7e34214a9efc141739ecc0f49277d1680be7ab685b74a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe761e7f1baacb1015ae345dadf921feb545775f29fa241d4656fc0b7b0e944`

```dockerfile
```

-	Layers:
	-	`sha256:815bb78a9d851bd4d69340210b112479e7ac60e52474e9a946253c2311a5e235`  
		Last Modified: Mon, 22 Jun 2026 21:47:18 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:fdd9c60e91e3e32e1d99b1e31894da2950c99194fb8a6ec7f24bc0ed7f490049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6e32f278fd364210b5378b9c775f37669ca37425057b87159a3fe2d10fd82d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:03 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba8cfbf4bada82bc12acb2b704ab7a199791bf0fb2e58d599e28f76ebe3d6`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7e8a69f4f646da4a5a0227992c72916a23aab04732d77ebc784c36f884b53ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56240e620c437c2607b84cf23a0fcbe4e1c4d843764c2fcae214dc17dea78285`

```dockerfile
```

-	Layers:
	-	`sha256:122ffef264b9f423559e1565ffdf589e592490e2a938e73680b7bb7ed7542d9a`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:30c6818895521b905434c83a874393e80e00eeb16c99cb406aabc52f6e841305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:d40e99fe0996b55c987f43318922f0126afdf833dc64b80e4f671b914e531139
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140004525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f698c6ee75b2e0c38f746a238c8b58fc571f69d8b228708313334088f21b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:09:23 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 22:09:25 GMT
ENV NATS_SERVER=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 09 Jun 2026 22:09:30 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 09 Jun 2026 22:09:49 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Jun 2026 22:10:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Jun 2026 22:10:13 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 22:10:14 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 22:10:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 22:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09f22a9628ef0d5b0cc16feadb876572bfdd0fed92378ff8e8777f451c62ae3`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a64864617250f652dc21c56c17bc9e201bd6efaaaada8ecb0a289739097c68d`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963c12e26fa7cc56f2895b0da6e1e2d663354df97d44ac2608b1b8a1e2efa36f`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1b3ab9ee4bdedf123268ce980d9b19d98aa3d3de2daf1d225b362a2d2ec90f`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080f2b59d6248c1199ff79acaba8ff2fa41389c65f9a3408b946e558476599ce`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8304c7e0c6a110a2e1de5b1db6ee30548c1f9b35cdb8bf2dc2d8943f8e98ece`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faefef94c2375e90b22da5d12ab47156f4ee851848a1c5659e082cf88d307f1b`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 482.4 KB (482407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6105388623f6f433b4ca5aa8d008cd1aa1e17cbfc5fe71d61e59bb6dc076eeb8`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 7.4 MB (7382856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f98553f597398b2c6201727d08ba6c5c0f84e754f2ea050675bb48eba199a8`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6358666bb0ef21de38462ae43661dca2ddf92df690f233904c8846efeea044af`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed5830658244188816a211d85b730ad98d8a17d9356480f8b99bbf4249b58c`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462c0f6d3e6997ffe7696032948f9230f3093a8323b995cb6636f7fab7a04bb9`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:30c6818895521b905434c83a874393e80e00eeb16c99cb406aabc52f6e841305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:d40e99fe0996b55c987f43318922f0126afdf833dc64b80e4f671b914e531139
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140004525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f698c6ee75b2e0c38f746a238c8b58fc571f69d8b228708313334088f21b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:09:23 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 22:09:25 GMT
ENV NATS_SERVER=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 09 Jun 2026 22:09:30 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 09 Jun 2026 22:09:49 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Jun 2026 22:10:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Jun 2026 22:10:13 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 22:10:14 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 22:10:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 22:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09f22a9628ef0d5b0cc16feadb876572bfdd0fed92378ff8e8777f451c62ae3`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a64864617250f652dc21c56c17bc9e201bd6efaaaada8ecb0a289739097c68d`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963c12e26fa7cc56f2895b0da6e1e2d663354df97d44ac2608b1b8a1e2efa36f`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1b3ab9ee4bdedf123268ce980d9b19d98aa3d3de2daf1d225b362a2d2ec90f`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080f2b59d6248c1199ff79acaba8ff2fa41389c65f9a3408b946e558476599ce`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8304c7e0c6a110a2e1de5b1db6ee30548c1f9b35cdb8bf2dc2d8943f8e98ece`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faefef94c2375e90b22da5d12ab47156f4ee851848a1c5659e082cf88d307f1b`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 482.4 KB (482407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6105388623f6f433b4ca5aa8d008cd1aa1e17cbfc5fe71d61e59bb6dc076eeb8`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 7.4 MB (7382856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f98553f597398b2c6201727d08ba6c5c0f84e754f2ea050675bb48eba199a8`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6358666bb0ef21de38462ae43661dca2ddf92df690f233904c8846efeea044af`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed5830658244188816a211d85b730ad98d8a17d9356480f8b99bbf4249b58c`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462c0f6d3e6997ffe7696032948f9230f3093a8323b995cb6636f7fab7a04bb9`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12`

```console
$ docker pull nats@sha256:d2e5bde3a006b860c6ec5411d2b0fbdb171dc52a4d4b7513c48ffe4a36caddd0
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
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12` - linux; amd64

```console
$ docker pull nats@sha256:4e0a163207760a2fafd706a02dc45a41c527679b06d65334d0fed8e3dc34edfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db612b4679049c1d296b87c540fc2d8ab9de5913e58ddceafb0ddf1d115887e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88913724d1d8e74f3f1ff6a60b00a7acb8450d4f1888012fc2a1719b0f571279`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.6 MB (6643520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e79d9e2c0917682470cfb3521cc2d6e6614ee7de3bb603e8dac076bca2c63c2`  
		Last Modified: Mon, 22 Jun 2026 20:17:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:df2f04b1d745ea86b414ed58c42cc3fb1fe4bbd30356845e58be5f15beddb3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530e6769062f26d7d2489e52da9bb0493acedf2f9da170d1a0f5c30d206f585e`

```dockerfile
```

-	Layers:
	-	`sha256:5211da7b940bfc01615b3c3dc028808b20dc715897a582f4af0e2ff86613bc8c`  
		Last Modified: Mon, 22 Jun 2026 20:17:15 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:b550149296fdbb198eda9bb923e604fac2c60228f0ca1c0f7cdcd14910bd2784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf1493de4b938c327f35a2ef948f2ce77a190a4f4c1e07d6fb7453dddbff787`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:28 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:28 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:28 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:56ed75683f9b5db33f8ad9a299605af0eae8a9ebe1c30ef8e894bea87d5de05d`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.4 MB (6384400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ed116a50499eb0150f3f46b9c3c18632896d2117b94eea68efae20cc5a29cf`  
		Last Modified: Mon, 22 Jun 2026 20:32:33 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:45580745e4122b9576049c091cd3eab9b183d5d46cc76e56073c8967bf7c8f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e3be9f99fb5618bd408d6f609e3e42018c5d5db98dbf565cfabe4bfe7e526d`

```dockerfile
```

-	Layers:
	-	`sha256:3aeddc8f878a40de7076296b55dfcbf74de7e00a839ffc8c46bb813a30e33570`  
		Last Modified: Mon, 22 Jun 2026 20:32:33 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:b5bab4a7f9566bce4f88761f1062bcc7948bf4ce322650d25842df8f8f04aa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8688c1e096fdaf59c4260a04b277ea3d2c924abdc4264b9e86e60e215e23a3db`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:52:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:52:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:52:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:52:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e982c114a13138e2685668359ca9e0582e26abafe5549dac8de6da9ec5a4812`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.4 MB (6374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b264b8dba345183a3269c5dc3b9e9ad5b6dfbec83ae04b7028ef69075a4f93`  
		Last Modified: Mon, 22 Jun 2026 21:52:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:082890466e1576d44847fc6f542adf06a9ef1a83d4afd50c695abaff61a1c65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875e0dc7374071702c6bf7808db464228515b75440db0fc3b18c9d362a12b073`

```dockerfile
```

-	Layers:
	-	`sha256:79b726f02a4557e7f1a3638dbe494ca7c0801d018ad052097fc3a68d7fb174a4`  
		Last Modified: Mon, 22 Jun 2026 21:52:23 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f654c5ce219e937c11aefac2e51d0430ba59ceaf641a7231825352040b492a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36a5b283a0aef587cd18eb9d09eac28eae275e041c89b283d340d23b317e46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:45 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:45 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dbab1ffdd888ab70dbb64d3905f68ffaad15b074fb768ff177945584a4da2979`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.0 MB (6038038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f62e3171d85c49194b56aed5d9105ec29345087fd3d7ee6c936fd63af8e8f9`  
		Last Modified: Mon, 22 Jun 2026 20:52:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:fa9f04a07c15d9f5ee0f22c29894e86dad69fef0f7e20dd9812d65c5b49f5809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec0a09b9b4aaeb0e052b09f2c10c58378f43617ac361d056ce6191a72f87561`

```dockerfile
```

-	Layers:
	-	`sha256:2ba93393850be4931acfd2a6a3337d1d2532b626b0210338761e5cd884043e6e`  
		Last Modified: Mon, 22 Jun 2026 20:52:49 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:220f73509d994a462021cb865baef1029f282a0cfe148d2c18646d2fff683310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6101131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8b604430e51193cbb4b6e679b32aa10ebc56bf86292195708a273e69aa8889`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:10 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3c8128190e1f74d677c2c6c27f17e58287ea869b0ac83a3ec8d948f9864be4`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.1 MB (6100622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:03d0820d0df6f5a1fbe7e6602afb7fbfaa07ba86136f8a914e4ffa0d06817a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11abbe8846ddadbbe6fbc6e75743137e6f360d57ffc884cc14db3de984b7a4ec`

```dockerfile
```

-	Layers:
	-	`sha256:eeb154955b1fd11cd5f8b79f018cde705c4b3783c5460484b0a026a8de4f0787`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 8.7 KB (8719 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:fcd48ce7444ab8beb2e858b6384549b9fc912c0e6e03b8d1913a0f0f46de9787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513735f0326702bbec3998aab0ac174d16067fde2a559153de79cf879c163945`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:07 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7af0e8a091b6b9b365d51014f398aea3666f8e453d6f97753b7042a611b1ef7`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.5 MB (6491236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1836135d3946a373ca3c67a256ad5a92bf1858c9304f6c1931cb49489abf4f4a`  
		Last Modified: Mon, 22 Jun 2026 21:13:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:4b93a5d801794fd86dff1142d68e775e8efc5c4b3a922e659555680e9d5d1432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03843a066bf335a9c94b555e1a7f838ab36c1c9079a182d8b2459e9c99572c9`

```dockerfile
```

-	Layers:
	-	`sha256:88c57bcecf6646d7c767a89088f19007e17f98b06d5e56c2a489ffc4709076dc`  
		Last Modified: Mon, 22 Jun 2026 21:13:15 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:f14342eee8aa62c5c5a5a750873434fbd4655428647f234ae3d6c372bcc4ba41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130837994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d83c9d65fa00cba8f00f11e0987227f25c591aeb2c03ca9a2092fac753c4412`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:34 GMT
RUN cmd /S /C #(nop) COPY file:031de465d263e81c8d37319c2c6d0de810f1fac238bd84131ee9b27c1f3e1384 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:35 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:36 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:38 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b064e7ee88c23f35363e7eea39250397bf468a13883ba8e2995014dc1b3f39ce`  
		Last Modified: Tue, 09 Jun 2026 23:20:43 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484d3e19dad17b590789c9b3da549d712dfe9edee2dc4ff40cd78a984cb79096`  
		Last Modified: Tue, 09 Jun 2026 23:20:43 GMT  
		Size: 6.8 MB (6834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36cab282fa804a2e5eb479c4ddf6d2376c94244206919ef981ed5dec089a1f0`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e405e74eebdc48eaaa5348d2e7cc73ddc27cee150377269308c6aefdd221c4`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b37c792525d791c9b53853f0aa22eb2436ac9c09a19bb1f8992419ec4791dfb`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8620d2f77af631033225fcd805c78c423779e302371dcbe57b25c2784d21b26`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-alpine`

```console
$ docker pull nats@sha256:a84f34eb0c293f2fc108af826df76fc5add8b75108cc455a847eb25693e96458
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
$ docker pull nats@sha256:425d3d24ac3b92b88cda1b153cc72f9535bfd1c0bcdd8f67740d9b22220e30f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4df4dc451af97c3499db640c4a6e0d6d6faa100799fe727d9e7e8be2f85756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f302f59e4314d1878834e19e5b71b17be0ae76d484bf8d2d1d2e13a49e87ffd`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 7.1 MB (7068014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d50079454fd127c8d11556ad65e8ae8d330d9b23fdebfbf84a7a2e1ef81830`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91585d73d765544cfc68e45bf7451cdcc41e98760273b1c14b994ea65a9421ca`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:627fc61f544347aee1241d88a072aaf2f482f3fe6d7dcae343a3386a0f71b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7dfec1367766e5087363e33ace912bc5cecf9d000ff7a9fcfc32e5edd3a827`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9967d703c4696f237199b5172918a071980ff994625807ad12b66209342e7`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2436f067b0994e145c846db59494022ced6409044a2aa87f972cc93ad507dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e462f80e44ff8333707c0bcc148ec82862c4181efb31597fa0c78c4bdd4fd85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:23 GMT
ENV NATS_SERVER=2.12.11
# Mon, 22 Jun 2026 19:46:23 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Mon, 22 Jun 2026 19:46:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:46:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:46:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:46:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:46:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a5c9d4dbf2cd13e85a5431f5da839d645119fee16d8ababbec8ccbb0fc9be8`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 6.8 MB (6796811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbddbd513806ed52f3ea698b307ff5c20215c021fd719fd7aaa9cf749613563`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202eb1221097aa9d3886233291ee5337ba925cdaf5edaf4f12073f07f9b750f9`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:fb6a1d5a469ff030aa27383bc4d656f9dfce59e319042bc6db9a6b3cffaec6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add775b3729cae73fb214448ba07c00333d2d3bae37a85ae8d979e597f286852`

```dockerfile
```

-	Layers:
	-	`sha256:7e74b341cbf5b87dabff8769d296a9252e45205fdefcc018b300860de19dca5a`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:474a34857fcc26216691f4e7e16a4d98275c2c650c5fe6654a702e246f5c4099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9994619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4f6bdfe56ac179b4e01549d15dd8ffbb4b07116a15d7c47257130cf1d42a3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:07:59 GMT
ENV NATS_SERVER=2.12.11
# Mon, 22 Jun 2026 20:07:59 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Mon, 22 Jun 2026 20:07:59 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 20:07:59 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:07:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 20:07:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:07:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:07:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764549d2bf83f7b867a29476aa5e45f75b2802a7d7867486a73f99fa3f53c765`  
		Last Modified: Mon, 22 Jun 2026 20:08:04 GMT  
		Size: 6.8 MB (6784038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d0853ca020010c228f72a6946472c76c5bd448655df1dbda6c2f63e9ca89f2`  
		Last Modified: Mon, 22 Jun 2026 20:08:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0d13aeb7df2038046a88ce2dd6c48c66a6bdb612a84664a62861cecdff2b41`  
		Last Modified: Mon, 22 Jun 2026 20:08:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83022762bb769542342eb1d5d171989a5a1d36904efaec0436cbd904d0053596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76226c52ca2fb47b4570830329ffef8eb8f904faf77175e6e0f85e241acc4ff3`

```dockerfile
```

-	Layers:
	-	`sha256:ab3be884dae8db89d3703029c6643b0df21877f60a3f8709d6e95c9ea526b9a4`  
		Last Modified: Mon, 22 Jun 2026 20:08:04 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:079686e9ce3165457ec62ad77a4928a1c7239676f8b7585b1f396d95592f4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10572280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7c04e64b1c946d5ed4689a119000bc8bdf05b4b8ae488f787be9e5d4e60ea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
ENV NATS_SERVER=2.12.11
# Mon, 22 Jun 2026 19:47:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Mon, 22 Jun 2026 19:47:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc324c5c8b044a216f6f8f8f9e4c7ba7321d9446e8d8d98e1f06adc4896fd612`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 6.5 MB (6450826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b27751f92c1020e7bf6a9716d13b9393fc561fdadb3fe63e2c192247ce3375`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c2276172a454cfa3b1fdb03b14772c81643c8d5b745ab7c580f0b3d8b2b619`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9d16b100021509fb8e43d15f6120ca0d7c4b1df6b96d15b20dc7621c629cfbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a85a973840e77fc2ed92c6fd518fb9090e109f3cad1157efc7f5e7b1a758152`

```dockerfile
```

-	Layers:
	-	`sha256:765423c8f9638bc5d58043b44b1f9237abbc2a06a0a369b6df5bd15d160e07ef`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:79ab02351c08527aa75a4f0dcf0bcabf8313986a36b2974702bd8fb4980b9898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10248160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd4063f85a19f911d9ce871702a6b298f8a8f7bdb6cdd70bf271565cbd0383e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e590177a1f3832404927d73f703cd9b6de1bc6aa1c0a4071f73e62d61d6ff4d`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.5 MB (6527958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ea17abc7bdf67861515d4ae06c070fb7748d0cbec44453db6d05495a7af96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a7741b38aa0865f53f2bc0c633a5727a70c07676d5f11582cbba4e5271703`

```dockerfile
```

-	Layers:
	-	`sha256:7c420f60382849b143e37e5624177f950ae9e5734cb82ee3cfc5487a594894d2`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:e416ac70e75c57154afc11270f4b79b26064bec8c6f45b33cc149de9369e4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10555129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f5c696629dedfa3f5d4827265a0ce1a254b61e328c4016a252e05fd6cd5d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2bc2f93033c9b7f596631cea725b6923dfa8204a1fbd0cad289cfb66ad686`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 6.9 MB (6917070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3319d5c969f4b3502a099f99e8b9d1c3bac616a3bddc3b10057dc687980fd7b1`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6498ad1fc5102f83402c9c078f53d9db7682b83a100cdf63606f711bce0f5d43`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9334e0829fc5846fd017385aec07371d829e8066ddd077be9208d80db65f9383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4430ea02178620fe9c9abc8a148ece6e6ef63f14d072c1c0f4852d54c98d2aa9`

```dockerfile
```

-	Layers:
	-	`sha256:f2d6fd7f8df0496ec5b02bad43bdccebdd9d1165cffbb23b9526bc4f3e6dbbdf`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:a84f34eb0c293f2fc108af826df76fc5add8b75108cc455a847eb25693e96458
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
$ docker pull nats@sha256:425d3d24ac3b92b88cda1b153cc72f9535bfd1c0bcdd8f67740d9b22220e30f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4df4dc451af97c3499db640c4a6e0d6d6faa100799fe727d9e7e8be2f85756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f302f59e4314d1878834e19e5b71b17be0ae76d484bf8d2d1d2e13a49e87ffd`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 7.1 MB (7068014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d50079454fd127c8d11556ad65e8ae8d330d9b23fdebfbf84a7a2e1ef81830`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91585d73d765544cfc68e45bf7451cdcc41e98760273b1c14b994ea65a9421ca`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:627fc61f544347aee1241d88a072aaf2f482f3fe6d7dcae343a3386a0f71b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7dfec1367766e5087363e33ace912bc5cecf9d000ff7a9fcfc32e5edd3a827`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9967d703c4696f237199b5172918a071980ff994625807ad12b66209342e7`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:2436f067b0994e145c846db59494022ced6409044a2aa87f972cc93ad507dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10292579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e462f80e44ff8333707c0bcc148ec82862c4181efb31597fa0c78c4bdd4fd85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:23 GMT
ENV NATS_SERVER=2.12.11
# Mon, 22 Jun 2026 19:46:23 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Mon, 22 Jun 2026 19:46:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:46:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:46:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:46:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:46:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a5c9d4dbf2cd13e85a5431f5da839d645119fee16d8ababbec8ccbb0fc9be8`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 6.8 MB (6796811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbddbd513806ed52f3ea698b307ff5c20215c021fd719fd7aaa9cf749613563`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202eb1221097aa9d3886233291ee5337ba925cdaf5edaf4f12073f07f9b750f9`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:fb6a1d5a469ff030aa27383bc4d656f9dfce59e319042bc6db9a6b3cffaec6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add775b3729cae73fb214448ba07c00333d2d3bae37a85ae8d979e597f286852`

```dockerfile
```

-	Layers:
	-	`sha256:7e74b341cbf5b87dabff8769d296a9252e45205fdefcc018b300860de19dca5a`  
		Last Modified: Mon, 22 Jun 2026 19:46:27 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:474a34857fcc26216691f4e7e16a4d98275c2c650c5fe6654a702e246f5c4099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9994619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4f6bdfe56ac179b4e01549d15dd8ffbb4b07116a15d7c47257130cf1d42a3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:07:59 GMT
ENV NATS_SERVER=2.12.11
# Mon, 22 Jun 2026 20:07:59 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Mon, 22 Jun 2026 20:07:59 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 20:07:59 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:07:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 20:07:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:07:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:07:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764549d2bf83f7b867a29476aa5e45f75b2802a7d7867486a73f99fa3f53c765`  
		Last Modified: Mon, 22 Jun 2026 20:08:04 GMT  
		Size: 6.8 MB (6784038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d0853ca020010c228f72a6946472c76c5bd448655df1dbda6c2f63e9ca89f2`  
		Last Modified: Mon, 22 Jun 2026 20:08:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0d13aeb7df2038046a88ce2dd6c48c66a6bdb612a84664a62861cecdff2b41`  
		Last Modified: Mon, 22 Jun 2026 20:08:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83022762bb769542342eb1d5d171989a5a1d36904efaec0436cbd904d0053596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76226c52ca2fb47b4570830329ffef8eb8f904faf77175e6e0f85e241acc4ff3`

```dockerfile
```

-	Layers:
	-	`sha256:ab3be884dae8db89d3703029c6643b0df21877f60a3f8709d6e95c9ea526b9a4`  
		Last Modified: Mon, 22 Jun 2026 20:08:04 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:079686e9ce3165457ec62ad77a4928a1c7239676f8b7585b1f396d95592f4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10572280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7c04e64b1c946d5ed4689a119000bc8bdf05b4b8ae488f787be9e5d4e60ea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
ENV NATS_SERVER=2.12.11
# Mon, 22 Jun 2026 19:47:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Mon, 22 Jun 2026 19:47:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc324c5c8b044a216f6f8f8f9e4c7ba7321d9446e8d8d98e1f06adc4896fd612`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 6.5 MB (6450826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b27751f92c1020e7bf6a9716d13b9393fc561fdadb3fe63e2c192247ce3375`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c2276172a454cfa3b1fdb03b14772c81643c8d5b745ab7c580f0b3d8b2b619`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9d16b100021509fb8e43d15f6120ca0d7c4b1df6b96d15b20dc7621c629cfbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a85a973840e77fc2ed92c6fd518fb9090e109f3cad1157efc7f5e7b1a758152`

```dockerfile
```

-	Layers:
	-	`sha256:765423c8f9638bc5d58043b44b1f9237abbc2a06a0a369b6df5bd15d160e07ef`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:79ab02351c08527aa75a4f0dcf0bcabf8313986a36b2974702bd8fb4980b9898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10248160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd4063f85a19f911d9ce871702a6b298f8a8f7bdb6cdd70bf271565cbd0383e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e590177a1f3832404927d73f703cd9b6de1bc6aa1c0a4071f73e62d61d6ff4d`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.5 MB (6527958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ea17abc7bdf67861515d4ae06c070fb7748d0cbec44453db6d05495a7af96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a7741b38aa0865f53f2bc0c633a5727a70c07676d5f11582cbba4e5271703`

```dockerfile
```

-	Layers:
	-	`sha256:7c420f60382849b143e37e5624177f950ae9e5734cb82ee3cfc5487a594894d2`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:e416ac70e75c57154afc11270f4b79b26064bec8c6f45b33cc149de9369e4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10555129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f5c696629dedfa3f5d4827265a0ce1a254b61e328c4016a252e05fd6cd5d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2bc2f93033c9b7f596631cea725b6923dfa8204a1fbd0cad289cfb66ad686`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 6.9 MB (6917070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3319d5c969f4b3502a099f99e8b9d1c3bac616a3bddc3b10057dc687980fd7b1`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6498ad1fc5102f83402c9c078f53d9db7682b83a100cdf63606f711bce0f5d43`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9334e0829fc5846fd017385aec07371d829e8066ddd077be9208d80db65f9383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4430ea02178620fe9c9abc8a148ece6e6ef63f14d072c1c0f4852d54c98d2aa9`

```dockerfile
```

-	Layers:
	-	`sha256:f2d6fd7f8df0496ec5b02bad43bdccebdd9d1165cffbb23b9526bc4f3e6dbbdf`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:070dd9de66967d27d3b7281c2a9e0a6ac076cce4431e86c05778b0ae328f75a1
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
$ docker pull nats@sha256:4e0a163207760a2fafd706a02dc45a41c527679b06d65334d0fed8e3dc34edfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db612b4679049c1d296b87c540fc2d8ab9de5913e58ddceafb0ddf1d115887e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88913724d1d8e74f3f1ff6a60b00a7acb8450d4f1888012fc2a1719b0f571279`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.6 MB (6643520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e79d9e2c0917682470cfb3521cc2d6e6614ee7de3bb603e8dac076bca2c63c2`  
		Last Modified: Mon, 22 Jun 2026 20:17:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:df2f04b1d745ea86b414ed58c42cc3fb1fe4bbd30356845e58be5f15beddb3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530e6769062f26d7d2489e52da9bb0493acedf2f9da170d1a0f5c30d206f585e`

```dockerfile
```

-	Layers:
	-	`sha256:5211da7b940bfc01615b3c3dc028808b20dc715897a582f4af0e2ff86613bc8c`  
		Last Modified: Mon, 22 Jun 2026 20:17:15 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:b550149296fdbb198eda9bb923e604fac2c60228f0ca1c0f7cdcd14910bd2784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf1493de4b938c327f35a2ef948f2ce77a190a4f4c1e07d6fb7453dddbff787`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:28 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:28 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:28 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:56ed75683f9b5db33f8ad9a299605af0eae8a9ebe1c30ef8e894bea87d5de05d`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.4 MB (6384400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ed116a50499eb0150f3f46b9c3c18632896d2117b94eea68efae20cc5a29cf`  
		Last Modified: Mon, 22 Jun 2026 20:32:33 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:45580745e4122b9576049c091cd3eab9b183d5d46cc76e56073c8967bf7c8f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e3be9f99fb5618bd408d6f609e3e42018c5d5db98dbf565cfabe4bfe7e526d`

```dockerfile
```

-	Layers:
	-	`sha256:3aeddc8f878a40de7076296b55dfcbf74de7e00a839ffc8c46bb813a30e33570`  
		Last Modified: Mon, 22 Jun 2026 20:32:33 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:b5bab4a7f9566bce4f88761f1062bcc7948bf4ce322650d25842df8f8f04aa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8688c1e096fdaf59c4260a04b277ea3d2c924abdc4264b9e86e60e215e23a3db`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:52:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:52:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:52:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:52:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e982c114a13138e2685668359ca9e0582e26abafe5549dac8de6da9ec5a4812`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.4 MB (6374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b264b8dba345183a3269c5dc3b9e9ad5b6dfbec83ae04b7028ef69075a4f93`  
		Last Modified: Mon, 22 Jun 2026 21:52:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:082890466e1576d44847fc6f542adf06a9ef1a83d4afd50c695abaff61a1c65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875e0dc7374071702c6bf7808db464228515b75440db0fc3b18c9d362a12b073`

```dockerfile
```

-	Layers:
	-	`sha256:79b726f02a4557e7f1a3638dbe494ca7c0801d018ad052097fc3a68d7fb174a4`  
		Last Modified: Mon, 22 Jun 2026 21:52:23 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f654c5ce219e937c11aefac2e51d0430ba59ceaf641a7231825352040b492a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36a5b283a0aef587cd18eb9d09eac28eae275e041c89b283d340d23b317e46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:45 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:45 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dbab1ffdd888ab70dbb64d3905f68ffaad15b074fb768ff177945584a4da2979`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.0 MB (6038038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f62e3171d85c49194b56aed5d9105ec29345087fd3d7ee6c936fd63af8e8f9`  
		Last Modified: Mon, 22 Jun 2026 20:52:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:fa9f04a07c15d9f5ee0f22c29894e86dad69fef0f7e20dd9812d65c5b49f5809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec0a09b9b4aaeb0e052b09f2c10c58378f43617ac361d056ce6191a72f87561`

```dockerfile
```

-	Layers:
	-	`sha256:2ba93393850be4931acfd2a6a3337d1d2532b626b0210338761e5cd884043e6e`  
		Last Modified: Mon, 22 Jun 2026 20:52:49 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:220f73509d994a462021cb865baef1029f282a0cfe148d2c18646d2fff683310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6101131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8b604430e51193cbb4b6e679b32aa10ebc56bf86292195708a273e69aa8889`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:10 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3c8128190e1f74d677c2c6c27f17e58287ea869b0ac83a3ec8d948f9864be4`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.1 MB (6100622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:03d0820d0df6f5a1fbe7e6602afb7fbfaa07ba86136f8a914e4ffa0d06817a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11abbe8846ddadbbe6fbc6e75743137e6f360d57ffc884cc14db3de984b7a4ec`

```dockerfile
```

-	Layers:
	-	`sha256:eeb154955b1fd11cd5f8b79f018cde705c4b3783c5460484b0a026a8de4f0787`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 8.7 KB (8719 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:fcd48ce7444ab8beb2e858b6384549b9fc912c0e6e03b8d1913a0f0f46de9787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513735f0326702bbec3998aab0ac174d16067fde2a559153de79cf879c163945`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:07 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7af0e8a091b6b9b365d51014f398aea3666f8e453d6f97753b7042a611b1ef7`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.5 MB (6491236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1836135d3946a373ca3c67a256ad5a92bf1858c9304f6c1931cb49489abf4f4a`  
		Last Modified: Mon, 22 Jun 2026 21:13:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4b93a5d801794fd86dff1142d68e775e8efc5c4b3a922e659555680e9d5d1432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03843a066bf335a9c94b555e1a7f838ab36c1c9079a182d8b2459e9c99572c9`

```dockerfile
```

-	Layers:
	-	`sha256:88c57bcecf6646d7c767a89088f19007e17f98b06d5e56c2a489ffc4709076dc`  
		Last Modified: Mon, 22 Jun 2026 21:13:15 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-nanoserver`

```console
$ docker pull nats@sha256:f12c13db6817ccdfb1762de51624e0ac1a8a6d4f0ca86de3f349181eeabab5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:f14342eee8aa62c5c5a5a750873434fbd4655428647f234ae3d6c372bcc4ba41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130837994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d83c9d65fa00cba8f00f11e0987227f25c591aeb2c03ca9a2092fac753c4412`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:34 GMT
RUN cmd /S /C #(nop) COPY file:031de465d263e81c8d37319c2c6d0de810f1fac238bd84131ee9b27c1f3e1384 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:35 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:36 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:38 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b064e7ee88c23f35363e7eea39250397bf468a13883ba8e2995014dc1b3f39ce`  
		Last Modified: Tue, 09 Jun 2026 23:20:43 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484d3e19dad17b590789c9b3da549d712dfe9edee2dc4ff40cd78a984cb79096`  
		Last Modified: Tue, 09 Jun 2026 23:20:43 GMT  
		Size: 6.8 MB (6834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36cab282fa804a2e5eb479c4ddf6d2376c94244206919ef981ed5dec089a1f0`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e405e74eebdc48eaaa5348d2e7cc73ddc27cee150377269308c6aefdd221c4`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b37c792525d791c9b53853f0aa22eb2436ac9c09a19bb1f8992419ec4791dfb`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8620d2f77af631033225fcd805c78c423779e302371dcbe57b25c2784d21b26`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:f12c13db6817ccdfb1762de51624e0ac1a8a6d4f0ca86de3f349181eeabab5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:f14342eee8aa62c5c5a5a750873434fbd4655428647f234ae3d6c372bcc4ba41
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130837994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d83c9d65fa00cba8f00f11e0987227f25c591aeb2c03ca9a2092fac753c4412`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:34 GMT
RUN cmd /S /C #(nop) COPY file:031de465d263e81c8d37319c2c6d0de810f1fac238bd84131ee9b27c1f3e1384 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:35 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:36 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:37 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:38 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b064e7ee88c23f35363e7eea39250397bf468a13883ba8e2995014dc1b3f39ce`  
		Last Modified: Tue, 09 Jun 2026 23:20:43 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484d3e19dad17b590789c9b3da549d712dfe9edee2dc4ff40cd78a984cb79096`  
		Last Modified: Tue, 09 Jun 2026 23:20:43 GMT  
		Size: 6.8 MB (6834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36cab282fa804a2e5eb479c4ddf6d2376c94244206919ef981ed5dec089a1f0`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.7 KB (1671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e405e74eebdc48eaaa5348d2e7cc73ddc27cee150377269308c6aefdd221c4`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b37c792525d791c9b53853f0aa22eb2436ac9c09a19bb1f8992419ec4791dfb`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8620d2f77af631033225fcd805c78c423779e302371dcbe57b25c2784d21b26`  
		Last Modified: Tue, 09 Jun 2026 23:20:42 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-scratch`

```console
$ docker pull nats@sha256:070dd9de66967d27d3b7281c2a9e0a6ac076cce4431e86c05778b0ae328f75a1
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
$ docker pull nats@sha256:4e0a163207760a2fafd706a02dc45a41c527679b06d65334d0fed8e3dc34edfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db612b4679049c1d296b87c540fc2d8ab9de5913e58ddceafb0ddf1d115887e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88913724d1d8e74f3f1ff6a60b00a7acb8450d4f1888012fc2a1719b0f571279`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.6 MB (6643520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e79d9e2c0917682470cfb3521cc2d6e6614ee7de3bb603e8dac076bca2c63c2`  
		Last Modified: Mon, 22 Jun 2026 20:17:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:df2f04b1d745ea86b414ed58c42cc3fb1fe4bbd30356845e58be5f15beddb3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530e6769062f26d7d2489e52da9bb0493acedf2f9da170d1a0f5c30d206f585e`

```dockerfile
```

-	Layers:
	-	`sha256:5211da7b940bfc01615b3c3dc028808b20dc715897a582f4af0e2ff86613bc8c`  
		Last Modified: Mon, 22 Jun 2026 20:17:15 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b550149296fdbb198eda9bb923e604fac2c60228f0ca1c0f7cdcd14910bd2784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf1493de4b938c327f35a2ef948f2ce77a190a4f4c1e07d6fb7453dddbff787`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:28 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:28 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:28 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:56ed75683f9b5db33f8ad9a299605af0eae8a9ebe1c30ef8e894bea87d5de05d`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.4 MB (6384400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ed116a50499eb0150f3f46b9c3c18632896d2117b94eea68efae20cc5a29cf`  
		Last Modified: Mon, 22 Jun 2026 20:32:33 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:45580745e4122b9576049c091cd3eab9b183d5d46cc76e56073c8967bf7c8f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e3be9f99fb5618bd408d6f609e3e42018c5d5db98dbf565cfabe4bfe7e526d`

```dockerfile
```

-	Layers:
	-	`sha256:3aeddc8f878a40de7076296b55dfcbf74de7e00a839ffc8c46bb813a30e33570`  
		Last Modified: Mon, 22 Jun 2026 20:32:33 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:b5bab4a7f9566bce4f88761f1062bcc7948bf4ce322650d25842df8f8f04aa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8688c1e096fdaf59c4260a04b277ea3d2c924abdc4264b9e86e60e215e23a3db`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:52:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:52:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:52:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:52:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:52:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:52:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e982c114a13138e2685668359ca9e0582e26abafe5549dac8de6da9ec5a4812`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.4 MB (6374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b264b8dba345183a3269c5dc3b9e9ad5b6dfbec83ae04b7028ef69075a4f93`  
		Last Modified: Mon, 22 Jun 2026 21:52:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:082890466e1576d44847fc6f542adf06a9ef1a83d4afd50c695abaff61a1c65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875e0dc7374071702c6bf7808db464228515b75440db0fc3b18c9d362a12b073`

```dockerfile
```

-	Layers:
	-	`sha256:79b726f02a4557e7f1a3638dbe494ca7c0801d018ad052097fc3a68d7fb174a4`  
		Last Modified: Mon, 22 Jun 2026 21:52:23 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f654c5ce219e937c11aefac2e51d0430ba59ceaf641a7231825352040b492a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36a5b283a0aef587cd18eb9d09eac28eae275e041c89b283d340d23b317e46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:45 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:45 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:45 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dbab1ffdd888ab70dbb64d3905f68ffaad15b074fb768ff177945584a4da2979`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.0 MB (6038038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f62e3171d85c49194b56aed5d9105ec29345087fd3d7ee6c936fd63af8e8f9`  
		Last Modified: Mon, 22 Jun 2026 20:52:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:fa9f04a07c15d9f5ee0f22c29894e86dad69fef0f7e20dd9812d65c5b49f5809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec0a09b9b4aaeb0e052b09f2c10c58378f43617ac361d056ce6191a72f87561`

```dockerfile
```

-	Layers:
	-	`sha256:2ba93393850be4931acfd2a6a3337d1d2532b626b0210338761e5cd884043e6e`  
		Last Modified: Mon, 22 Jun 2026 20:52:49 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:220f73509d994a462021cb865baef1029f282a0cfe148d2c18646d2fff683310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6101131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8b604430e51193cbb4b6e679b32aa10ebc56bf86292195708a273e69aa8889`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:10 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3c8128190e1f74d677c2c6c27f17e58287ea869b0ac83a3ec8d948f9864be4`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.1 MB (6100622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:03d0820d0df6f5a1fbe7e6602afb7fbfaa07ba86136f8a914e4ffa0d06817a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11abbe8846ddadbbe6fbc6e75743137e6f360d57ffc884cc14db3de984b7a4ec`

```dockerfile
```

-	Layers:
	-	`sha256:eeb154955b1fd11cd5f8b79f018cde705c4b3783c5460484b0a026a8de4f0787`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 8.7 KB (8719 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:fcd48ce7444ab8beb2e858b6384549b9fc912c0e6e03b8d1913a0f0f46de9787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513735f0326702bbec3998aab0ac174d16067fde2a559153de79cf879c163945`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:07 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7af0e8a091b6b9b365d51014f398aea3666f8e453d6f97753b7042a611b1ef7`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.5 MB (6491236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1836135d3946a373ca3c67a256ad5a92bf1858c9304f6c1931cb49489abf4f4a`  
		Last Modified: Mon, 22 Jun 2026 21:13:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4b93a5d801794fd86dff1142d68e775e8efc5c4b3a922e659555680e9d5d1432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03843a066bf335a9c94b555e1a7f838ab36c1c9079a182d8b2459e9c99572c9`

```dockerfile
```

-	Layers:
	-	`sha256:88c57bcecf6646d7c767a89088f19007e17f98b06d5e56c2a489ffc4709076dc`  
		Last Modified: Mon, 22 Jun 2026 21:13:15 GMT  
		Size: 8.7 KB (8667 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-windowsservercore`

```console
$ docker pull nats@sha256:edccb8294b3e618c23c5b8f1a4d7cc24f79a79c3267b1b870579feaaccfc286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:fa39afd5ebf48293fe2526597beed94a038444fc0121a1d3e146c55cc86442fe
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139800913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6755853a5fdbc2781bc2dddd66bac3f5084dd58b4c3c72e4d31a10bd8d7cd787`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:09:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 22:09:15 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 22:09:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 22:09:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.11/nats-server-v2.12.11-windows-amd64.zip
# Tue, 09 Jun 2026 22:09:20 GMT
ENV NATS_SERVER_SHASUM=b9867cefc59c75daadf3341ce803ba83bbb4b70cf0ddbed2349c57096ad88d1c
# Tue, 09 Jun 2026 22:09:42 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Jun 2026 22:10:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Jun 2026 22:10:02 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 22:10:03 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 22:10:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 22:10:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e808aa6c6b5a1a33b32b30c17940667b0a64179e41df6c3ae1dfc6c89aa7bf2`  
		Last Modified: Tue, 09 Jun 2026 22:10:13 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d709f0271c65fae7070b703766a93621f6de51558d98571e209cabee76a8243`  
		Last Modified: Tue, 09 Jun 2026 22:10:13 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688d7d9618fe61421fa65782e7999c759d967c3113e76cfc5c0253f03429b71f`  
		Last Modified: Tue, 09 Jun 2026 22:10:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a041b906108d8d6b20e644fe9acf186814a0ac28a663773c929e1872aec1f2e`  
		Last Modified: Tue, 09 Jun 2026 22:10:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ff12400f76e27b8f2f45c8207424ab8fa198b8dd6a99fa4e43105395715d4a`  
		Last Modified: Tue, 09 Jun 2026 22:10:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4540e1594bef40e73bed12e0b3dbab6f79331c74522a604a1734e5fe6dd608`  
		Last Modified: Tue, 09 Jun 2026 22:10:11 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d955800564aed82bf86544fa0afa750b11d30c3a3696d5632583c83d80c014d`  
		Last Modified: Tue, 09 Jun 2026 22:10:11 GMT  
		Size: 481.0 KB (480967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78555efdd0b7893da6424790ebf6d4102ef9dda95333efa6f72eb709e3a56560`  
		Last Modified: Tue, 09 Jun 2026 22:10:13 GMT  
		Size: 7.2 MB (7180777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c462848051630691f1206c5fb9158a28fc0c554b51861618a1706af162250646`  
		Last Modified: Tue, 09 Jun 2026 22:10:09 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203cb1efb87c7ea8c3ae9ca38402b5a09e8516ac820b51cbb09748acb07e7bdb`  
		Last Modified: Tue, 09 Jun 2026 22:10:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c18a9fda7693a720f4d40d6a86f777d1502f1de7288cef3861af817b107760b`  
		Last Modified: Tue, 09 Jun 2026 22:10:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395eec9345054f06f98f6a6e7f82718ea962bc820a8eae3bfc12bf4c76020d92`  
		Last Modified: Tue, 09 Jun 2026 22:10:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:edccb8294b3e618c23c5b8f1a4d7cc24f79a79c3267b1b870579feaaccfc286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:fa39afd5ebf48293fe2526597beed94a038444fc0121a1d3e146c55cc86442fe
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139800913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6755853a5fdbc2781bc2dddd66bac3f5084dd58b4c3c72e4d31a10bd8d7cd787`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:09:13 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 22:09:15 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 22:09:17 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 22:09:19 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.11/nats-server-v2.12.11-windows-amd64.zip
# Tue, 09 Jun 2026 22:09:20 GMT
ENV NATS_SERVER_SHASUM=b9867cefc59c75daadf3341ce803ba83bbb4b70cf0ddbed2349c57096ad88d1c
# Tue, 09 Jun 2026 22:09:42 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Jun 2026 22:10:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Jun 2026 22:10:02 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 22:10:03 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 22:10:04 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 22:10:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e808aa6c6b5a1a33b32b30c17940667b0a64179e41df6c3ae1dfc6c89aa7bf2`  
		Last Modified: Tue, 09 Jun 2026 22:10:13 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d709f0271c65fae7070b703766a93621f6de51558d98571e209cabee76a8243`  
		Last Modified: Tue, 09 Jun 2026 22:10:13 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688d7d9618fe61421fa65782e7999c759d967c3113e76cfc5c0253f03429b71f`  
		Last Modified: Tue, 09 Jun 2026 22:10:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a041b906108d8d6b20e644fe9acf186814a0ac28a663773c929e1872aec1f2e`  
		Last Modified: Tue, 09 Jun 2026 22:10:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ff12400f76e27b8f2f45c8207424ab8fa198b8dd6a99fa4e43105395715d4a`  
		Last Modified: Tue, 09 Jun 2026 22:10:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4540e1594bef40e73bed12e0b3dbab6f79331c74522a604a1734e5fe6dd608`  
		Last Modified: Tue, 09 Jun 2026 22:10:11 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d955800564aed82bf86544fa0afa750b11d30c3a3696d5632583c83d80c014d`  
		Last Modified: Tue, 09 Jun 2026 22:10:11 GMT  
		Size: 481.0 KB (480967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78555efdd0b7893da6424790ebf6d4102ef9dda95333efa6f72eb709e3a56560`  
		Last Modified: Tue, 09 Jun 2026 22:10:13 GMT  
		Size: 7.2 MB (7180777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c462848051630691f1206c5fb9158a28fc0c554b51861618a1706af162250646`  
		Last Modified: Tue, 09 Jun 2026 22:10:09 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203cb1efb87c7ea8c3ae9ca38402b5a09e8516ac820b51cbb09748acb07e7bdb`  
		Last Modified: Tue, 09 Jun 2026 22:10:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c18a9fda7693a720f4d40d6a86f777d1502f1de7288cef3861af817b107760b`  
		Last Modified: Tue, 09 Jun 2026 22:10:09 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395eec9345054f06f98f6a6e7f82718ea962bc820a8eae3bfc12bf4c76020d92`  
		Last Modified: Tue, 09 Jun 2026 22:10:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.12`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.12-alpine`

```console
$ docker pull nats@sha256:8b25d83ad3c8d4afd8850f8cc419ff4f17e486bb54f727c462ce70e319c6e43f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12.12-alpine` - linux; amd64

```console
$ docker pull nats@sha256:425d3d24ac3b92b88cda1b153cc72f9535bfd1c0bcdd8f67740d9b22220e30f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4df4dc451af97c3499db640c4a6e0d6d6faa100799fe727d9e7e8be2f85756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f302f59e4314d1878834e19e5b71b17be0ae76d484bf8d2d1d2e13a49e87ffd`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 7.1 MB (7068014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d50079454fd127c8d11556ad65e8ae8d330d9b23fdebfbf84a7a2e1ef81830`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91585d73d765544cfc68e45bf7451cdcc41e98760273b1c14b994ea65a9421ca`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:627fc61f544347aee1241d88a072aaf2f482f3fe6d7dcae343a3386a0f71b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7dfec1367766e5087363e33ace912bc5cecf9d000ff7a9fcfc32e5edd3a827`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9967d703c4696f237199b5172918a071980ff994625807ad12b66209342e7`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:79ab02351c08527aa75a4f0dcf0bcabf8313986a36b2974702bd8fb4980b9898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10248160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd4063f85a19f911d9ce871702a6b298f8a8f7bdb6cdd70bf271565cbd0383e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e590177a1f3832404927d73f703cd9b6de1bc6aa1c0a4071f73e62d61d6ff4d`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.5 MB (6527958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ea17abc7bdf67861515d4ae06c070fb7748d0cbec44453db6d05495a7af96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a7741b38aa0865f53f2bc0c633a5727a70c07676d5f11582cbba4e5271703`

```dockerfile
```

-	Layers:
	-	`sha256:7c420f60382849b143e37e5624177f950ae9e5734cb82ee3cfc5487a594894d2`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:e416ac70e75c57154afc11270f4b79b26064bec8c6f45b33cc149de9369e4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10555129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f5c696629dedfa3f5d4827265a0ce1a254b61e328c4016a252e05fd6cd5d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2bc2f93033c9b7f596631cea725b6923dfa8204a1fbd0cad289cfb66ad686`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 6.9 MB (6917070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3319d5c969f4b3502a099f99e8b9d1c3bac616a3bddc3b10057dc687980fd7b1`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6498ad1fc5102f83402c9c078f53d9db7682b83a100cdf63606f711bce0f5d43`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9334e0829fc5846fd017385aec07371d829e8066ddd077be9208d80db65f9383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4430ea02178620fe9c9abc8a148ece6e6ef63f14d072c1c0f4852d54c98d2aa9`

```dockerfile
```

-	Layers:
	-	`sha256:f2d6fd7f8df0496ec5b02bad43bdccebdd9d1165cffbb23b9526bc4f3e6dbbdf`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.12-alpine3.22`

```console
$ docker pull nats@sha256:8b25d83ad3c8d4afd8850f8cc419ff4f17e486bb54f727c462ce70e319c6e43f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12.12-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:425d3d24ac3b92b88cda1b153cc72f9535bfd1c0bcdd8f67740d9b22220e30f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4df4dc451af97c3499db640c4a6e0d6d6faa100799fe727d9e7e8be2f85756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f302f59e4314d1878834e19e5b71b17be0ae76d484bf8d2d1d2e13a49e87ffd`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 7.1 MB (7068014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d50079454fd127c8d11556ad65e8ae8d330d9b23fdebfbf84a7a2e1ef81830`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91585d73d765544cfc68e45bf7451cdcc41e98760273b1c14b994ea65a9421ca`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:627fc61f544347aee1241d88a072aaf2f482f3fe6d7dcae343a3386a0f71b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7dfec1367766e5087363e33ace912bc5cecf9d000ff7a9fcfc32e5edd3a827`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9967d703c4696f237199b5172918a071980ff994625807ad12b66209342e7`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:79ab02351c08527aa75a4f0dcf0bcabf8313986a36b2974702bd8fb4980b9898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10248160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd4063f85a19f911d9ce871702a6b298f8a8f7bdb6cdd70bf271565cbd0383e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e590177a1f3832404927d73f703cd9b6de1bc6aa1c0a4071f73e62d61d6ff4d`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.5 MB (6527958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ea17abc7bdf67861515d4ae06c070fb7748d0cbec44453db6d05495a7af96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a7741b38aa0865f53f2bc0c633a5727a70c07676d5f11582cbba4e5271703`

```dockerfile
```

-	Layers:
	-	`sha256:7c420f60382849b143e37e5624177f950ae9e5734cb82ee3cfc5487a594894d2`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:e416ac70e75c57154afc11270f4b79b26064bec8c6f45b33cc149de9369e4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10555129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f5c696629dedfa3f5d4827265a0ce1a254b61e328c4016a252e05fd6cd5d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2bc2f93033c9b7f596631cea725b6923dfa8204a1fbd0cad289cfb66ad686`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 6.9 MB (6917070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3319d5c969f4b3502a099f99e8b9d1c3bac616a3bddc3b10057dc687980fd7b1`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6498ad1fc5102f83402c9c078f53d9db7682b83a100cdf63606f711bce0f5d43`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9334e0829fc5846fd017385aec07371d829e8066ddd077be9208d80db65f9383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4430ea02178620fe9c9abc8a148ece6e6ef63f14d072c1c0f4852d54c98d2aa9`

```dockerfile
```

-	Layers:
	-	`sha256:f2d6fd7f8df0496ec5b02bad43bdccebdd9d1165cffbb23b9526bc4f3e6dbbdf`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.12-linux`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.12-nanoserver`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.12-scratch`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.12-windowsservercore`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.12.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14`

```console
$ docker pull nats@sha256:bbfbb6c4cdaeb8a2e3ca57d3de30463a66a6c5181f324f3b680bcf858833d377
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
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14` - linux; amd64

```console
$ docker pull nats@sha256:65713a1834b75d00256f847cc7b8db5fea12121bbf341edfff76f84a76b56ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29535378bebe76ff33b25a0ee21ab0fe2346cb9bbd179ece59ab2f37f36e3c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b33128ccd2d9960d0a0ac0d31682c1928d1d17ca25caf107fa914eee12f346`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:82f0a5ca9b68dc2a87b53a0f1f9e9f5121208dbd998d0b36d56e9d11aba98464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ed450408ac2b61ff0b451c4f09ce61f26a1b3eb58a44c10cc2082ca924201`

```dockerfile
```

-	Layers:
	-	`sha256:4c738c96a15989941f46c5a6a4392bfbc566b311520062f8d56aa0637d39400a`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:340c3f31c2400ff9ce93e99a056a2f65376bb08bb66291dd626c08ce54ca68d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558fc4503cb023f4b5007d465ea651c8f3af04a4b3a5b6348ccd9c78575dfe55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:18 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055cbd39cde58dda5cd03328a647a1e169ff8116a012137ce777d015565a44d7`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:4f0459213b2c44994bdbfc9af813a5f71ef1d00fba9c4e79cb15c7e2beefb67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63163d0fb60b2575e901b5e80f128020e9f3a5a2c610f865f3a750ea54a7fcdb`

```dockerfile
```

-	Layers:
	-	`sha256:527462491f781bce7f70496c4c9f2301b87cd5239c9f3ef5e83120fdb7370326`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7b3118869b74523b091cdec795dac3a3e7f7a69b0da2a0b5e1c4efbacb592fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6521bf98b02b2cf398c50c51930a34edf1c9da6a12a609b5d4ab2c01aab4f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:43:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:43:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:44:00 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:44:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3113ca534280e6c8acb2de55307064e1f8c2dce3fbe561d92a361be6754b8a`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:237ed08805072b07e68a19e104f07b16b22f4d8df845090f99164f396c4b7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf263674818d6f6280a468f63ff41db03882ca617c12d4e40e13f8920327b702`

```dockerfile
```

-	Layers:
	-	`sha256:db257913eec8f718988e940693bf52d60408882e903f08f9f45925a0f08e79e7`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cfd028112c875c7eda23860b3554e5e990356a1057bb17dd09a20a243372f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3cf3c1e911779b9fbfe69ca703bb69a2b7407e6227e3f9b70ebbca6f0a54d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:33 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:33 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46654056ed2549b3cbb7f0ff49c14926dda4483bfcae2e5b2ae45112ce5291d0`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:99443208695008b0853014ff29715108f78d0ab8da563be4c3e5e722cf8e3b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2669aa13c7dc6695ab85bcc4e2eca03332d9e1771e9a50b9d6b5155f28a0110b`

```dockerfile
```

-	Layers:
	-	`sha256:fe5804167a3e8df278aea8ff5b75538f93e08c74ce18b116e6b7a40f075195e8`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; ppc64le

```console
$ docker pull nats@sha256:52e2eb5749be9656b0a896ee1e1791cdf66fc1efc72030d918ce83f28c1f4b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0846d8047c28872a68ffbc2831a19d2d15e0289633332b837db0f98247d37b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:6db89f1127caa8acb7e34214a9efc141739ecc0f49277d1680be7ab685b74a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe761e7f1baacb1015ae345dadf921feb545775f29fa241d4656fc0b7b0e944`

```dockerfile
```

-	Layers:
	-	`sha256:815bb78a9d851bd4d69340210b112479e7ac60e52474e9a946253c2311a5e235`  
		Last Modified: Mon, 22 Jun 2026 21:47:18 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; s390x

```console
$ docker pull nats@sha256:fdd9c60e91e3e32e1d99b1e31894da2950c99194fb8a6ec7f24bc0ed7f490049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6e32f278fd364210b5378b9c775f37669ca37425057b87159a3fe2d10fd82d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:03 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba8cfbf4bada82bc12acb2b704ab7a199791bf0fb2e58d599e28f76ebe3d6`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:7e8a69f4f646da4a5a0227992c72916a23aab04732d77ebc784c36f884b53ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56240e620c437c2607b84cf23a0fcbe4e1c4d843764c2fcae214dc17dea78285`

```dockerfile
```

-	Layers:
	-	`sha256:122ffef264b9f423559e1565ffdf589e592490e2a938e73680b7bb7ed7542d9a`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:0badb754748fd4de2327f7cca2a86ef00b94e6c26569e80e707b706f27325db5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131036450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47805c9ad0d2cf7cad50fc23b59da1d61256f0205ddc87a79286268a11862c2a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:30 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5ccd531a60c4bbb1082621a0a21646b6494b0e2f612e79a6778943268beed`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c651bbee8aea515b8055fcdde339bcbf1c6bb43eec92b29e344e9f52afb2d`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 7.0 MB (7032997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944c27da9e6c3f4181c98a5de2c3e6ac2ba74a492184ddf9cb918f6077e0ed1`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bb394cd41fc7b65a1b4279ab910c2b79893e79ff5968ec47b31269a7f6886c`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a49be050f1fb2cdeb4cdc180ef6c139faf00bc0adf3dda61f6e7b185ebed5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c55e36e6b13a9d983ce1406964734930adac2e1fa2707cebafdef63520d5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-alpine`

```console
$ docker pull nats@sha256:3c66911d53d63e76dd733c7994ca544c28602cafc68f27fbf47dbb8e37205e57
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

### `nats:2.14-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:afa0021fd5534b5898b5a146edea9264c8db26144b792c10a5315a35bbbac5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10482561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b85446ce3f424e4511a6ec5bcc77ecab084eb56464f1f1d28046674ab67a651`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677c5f86a68cf2ce1fdf51d3b53c56b92e7fbe3b67443d993c093aac9e6a00f`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 7.0 MB (6986793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea037dcf8136a7791f9e560bda59f20a5e40ee8d447c9b81a75253956c52d2c`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91efd4d63f2001f13a850754a14e04788257c1dbe8f26cf095f7cc64ca2b5913`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7d4eebf896ed7b471bfb246e8823a02079e74eb6195ffc6edbc4246539be1a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4004102106793942ddb14115cf0e0684cc23e759a6ffca0eb4c60dd06d05b2fc`

```dockerfile
```

-	Layers:
	-	`sha256:cd7784700079db7a9f22cc194e5d89197a178370899405a829e82b5a633e3afe`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:91683fb37479895c178784386781a757532946afd57131bb405b062581ebef75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10188544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49ae72c112bb15690a11d8a5b7aa735cd4245c99549bce10acb4dc49a476ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8b795a8aa2f5335674b36741b17ce192443d940da95f3bbd597b70531689e3`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 7.0 MB (6977963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5097219f08bd67d8fa2e25a5a479e8bd0385d6216ab6343a4aa1875eb26304`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8e33bc51c0528dbfa912e61fdcfc8e25b5a0c5ed8ff2e87ebc145a65aa1605`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:753a5ea794f4139e119be983748b07d2258ba219fca43ac667a4533c6e30a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b52454a96ab80fa5715d09b55b91072a66c893f75f0d94f5e43b01767f6c542`

```dockerfile
```

-	Layers:
	-	`sha256:a85da325cca4163e5d72d726f4f96a446323aa0b460ea8f228953398ba6b6171`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4267586f8d1941e8955323b0014cba3b61f65881b4c4c20de688fbe1c5fea804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10724412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f145de50057f413858c406b87310468fc4bd3effd1f88e329cf02fea0239e1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cfbf804236b512a4b9944ec56130b32a28b0a4b77458c90970f66f3a589254`  
		Last Modified: Mon, 22 Jun 2026 19:47:17 GMT  
		Size: 6.6 MB (6602958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c950a70aceecc1179a9c484d238f8ec42132ddf44f71978023a2ac0e56fc0`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f2ccaf61966a62729b5a1cfbdf7e05d864310ac230029a8a9cf60d0967ec7`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5deeca0a3264b5d656b04246f1c17f72ca74115b5de8e356adbe225c80c755bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51798bd8628e715c409906689a2cf6fac8b1fee280fd2920de1e6a379bc4c6`

```dockerfile
```

-	Layers:
	-	`sha256:f0614b048154314f9962518fc36f249b39de8d985648d33ef1ce4bb9369f3f4a`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-alpine3.22`

```console
$ docker pull nats@sha256:3c66911d53d63e76dd733c7994ca544c28602cafc68f27fbf47dbb8e37205e57
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

### `nats:2.14-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:afa0021fd5534b5898b5a146edea9264c8db26144b792c10a5315a35bbbac5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10482561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b85446ce3f424e4511a6ec5bcc77ecab084eb56464f1f1d28046674ab67a651`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677c5f86a68cf2ce1fdf51d3b53c56b92e7fbe3b67443d993c093aac9e6a00f`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 7.0 MB (6986793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea037dcf8136a7791f9e560bda59f20a5e40ee8d447c9b81a75253956c52d2c`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91efd4d63f2001f13a850754a14e04788257c1dbe8f26cf095f7cc64ca2b5913`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7d4eebf896ed7b471bfb246e8823a02079e74eb6195ffc6edbc4246539be1a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4004102106793942ddb14115cf0e0684cc23e759a6ffca0eb4c60dd06d05b2fc`

```dockerfile
```

-	Layers:
	-	`sha256:cd7784700079db7a9f22cc194e5d89197a178370899405a829e82b5a633e3afe`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:91683fb37479895c178784386781a757532946afd57131bb405b062581ebef75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10188544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49ae72c112bb15690a11d8a5b7aa735cd4245c99549bce10acb4dc49a476ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8b795a8aa2f5335674b36741b17ce192443d940da95f3bbd597b70531689e3`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 7.0 MB (6977963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5097219f08bd67d8fa2e25a5a479e8bd0385d6216ab6343a4aa1875eb26304`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8e33bc51c0528dbfa912e61fdcfc8e25b5a0c5ed8ff2e87ebc145a65aa1605`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:753a5ea794f4139e119be983748b07d2258ba219fca43ac667a4533c6e30a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b52454a96ab80fa5715d09b55b91072a66c893f75f0d94f5e43b01767f6c542`

```dockerfile
```

-	Layers:
	-	`sha256:a85da325cca4163e5d72d726f4f96a446323aa0b460ea8f228953398ba6b6171`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4267586f8d1941e8955323b0014cba3b61f65881b4c4c20de688fbe1c5fea804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10724412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f145de50057f413858c406b87310468fc4bd3effd1f88e329cf02fea0239e1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cfbf804236b512a4b9944ec56130b32a28b0a4b77458c90970f66f3a589254`  
		Last Modified: Mon, 22 Jun 2026 19:47:17 GMT  
		Size: 6.6 MB (6602958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c950a70aceecc1179a9c484d238f8ec42132ddf44f71978023a2ac0e56fc0`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f2ccaf61966a62729b5a1cfbdf7e05d864310ac230029a8a9cf60d0967ec7`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5deeca0a3264b5d656b04246f1c17f72ca74115b5de8e356adbe225c80c755bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51798bd8628e715c409906689a2cf6fac8b1fee280fd2920de1e6a379bc4c6`

```dockerfile
```

-	Layers:
	-	`sha256:f0614b048154314f9962518fc36f249b39de8d985648d33ef1ce4bb9369f3f4a`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-linux`

```console
$ docker pull nats@sha256:3b7b5f689b8b9055b95f9eedc3448de69c16808d427fa6295e5a6df3fb45e910
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

### `nats:2.14-linux` - linux; amd64

```console
$ docker pull nats@sha256:65713a1834b75d00256f847cc7b8db5fea12121bbf341edfff76f84a76b56ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29535378bebe76ff33b25a0ee21ab0fe2346cb9bbd179ece59ab2f37f36e3c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b33128ccd2d9960d0a0ac0d31682c1928d1d17ca25caf107fa914eee12f346`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:82f0a5ca9b68dc2a87b53a0f1f9e9f5121208dbd998d0b36d56e9d11aba98464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ed450408ac2b61ff0b451c4f09ce61f26a1b3eb58a44c10cc2082ca924201`

```dockerfile
```

-	Layers:
	-	`sha256:4c738c96a15989941f46c5a6a4392bfbc566b311520062f8d56aa0637d39400a`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:340c3f31c2400ff9ce93e99a056a2f65376bb08bb66291dd626c08ce54ca68d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558fc4503cb023f4b5007d465ea651c8f3af04a4b3a5b6348ccd9c78575dfe55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:18 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055cbd39cde58dda5cd03328a647a1e169ff8116a012137ce777d015565a44d7`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4f0459213b2c44994bdbfc9af813a5f71ef1d00fba9c4e79cb15c7e2beefb67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63163d0fb60b2575e901b5e80f128020e9f3a5a2c610f865f3a750ea54a7fcdb`

```dockerfile
```

-	Layers:
	-	`sha256:527462491f781bce7f70496c4c9f2301b87cd5239c9f3ef5e83120fdb7370326`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7b3118869b74523b091cdec795dac3a3e7f7a69b0da2a0b5e1c4efbacb592fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6521bf98b02b2cf398c50c51930a34edf1c9da6a12a609b5d4ab2c01aab4f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:43:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:43:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:44:00 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:44:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3113ca534280e6c8acb2de55307064e1f8c2dce3fbe561d92a361be6754b8a`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:237ed08805072b07e68a19e104f07b16b22f4d8df845090f99164f396c4b7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf263674818d6f6280a468f63ff41db03882ca617c12d4e40e13f8920327b702`

```dockerfile
```

-	Layers:
	-	`sha256:db257913eec8f718988e940693bf52d60408882e903f08f9f45925a0f08e79e7`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cfd028112c875c7eda23860b3554e5e990356a1057bb17dd09a20a243372f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3cf3c1e911779b9fbfe69ca703bb69a2b7407e6227e3f9b70ebbca6f0a54d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:33 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:33 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46654056ed2549b3cbb7f0ff49c14926dda4483bfcae2e5b2ae45112ce5291d0`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:99443208695008b0853014ff29715108f78d0ab8da563be4c3e5e722cf8e3b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2669aa13c7dc6695ab85bcc4e2eca03332d9e1771e9a50b9d6b5155f28a0110b`

```dockerfile
```

-	Layers:
	-	`sha256:fe5804167a3e8df278aea8ff5b75538f93e08c74ce18b116e6b7a40f075195e8`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:52e2eb5749be9656b0a896ee1e1791cdf66fc1efc72030d918ce83f28c1f4b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0846d8047c28872a68ffbc2831a19d2d15e0289633332b837db0f98247d37b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6db89f1127caa8acb7e34214a9efc141739ecc0f49277d1680be7ab685b74a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe761e7f1baacb1015ae345dadf921feb545775f29fa241d4656fc0b7b0e944`

```dockerfile
```

-	Layers:
	-	`sha256:815bb78a9d851bd4d69340210b112479e7ac60e52474e9a946253c2311a5e235`  
		Last Modified: Mon, 22 Jun 2026 21:47:18 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; s390x

```console
$ docker pull nats@sha256:fdd9c60e91e3e32e1d99b1e31894da2950c99194fb8a6ec7f24bc0ed7f490049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6e32f278fd364210b5378b9c775f37669ca37425057b87159a3fe2d10fd82d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:03 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba8cfbf4bada82bc12acb2b704ab7a199791bf0fb2e58d599e28f76ebe3d6`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7e8a69f4f646da4a5a0227992c72916a23aab04732d77ebc784c36f884b53ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56240e620c437c2607b84cf23a0fcbe4e1c4d843764c2fcae214dc17dea78285`

```dockerfile
```

-	Layers:
	-	`sha256:122ffef264b9f423559e1565ffdf589e592490e2a938e73680b7bb7ed7542d9a`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-nanoserver`

```console
$ docker pull nats@sha256:9622b8c98b2488b8efd76eefe88e2b019d542d6de0e04db7af8d21e067f39ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:0badb754748fd4de2327f7cca2a86ef00b94e6c26569e80e707b706f27325db5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131036450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47805c9ad0d2cf7cad50fc23b59da1d61256f0205ddc87a79286268a11862c2a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:30 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5ccd531a60c4bbb1082621a0a21646b6494b0e2f612e79a6778943268beed`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c651bbee8aea515b8055fcdde339bcbf1c6bb43eec92b29e344e9f52afb2d`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 7.0 MB (7032997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944c27da9e6c3f4181c98a5de2c3e6ac2ba74a492184ddf9cb918f6077e0ed1`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bb394cd41fc7b65a1b4279ab910c2b79893e79ff5968ec47b31269a7f6886c`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a49be050f1fb2cdeb4cdc180ef6c139faf00bc0adf3dda61f6e7b185ebed5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c55e36e6b13a9d983ce1406964734930adac2e1fa2707cebafdef63520d5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:9622b8c98b2488b8efd76eefe88e2b019d542d6de0e04db7af8d21e067f39ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:0badb754748fd4de2327f7cca2a86ef00b94e6c26569e80e707b706f27325db5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131036450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47805c9ad0d2cf7cad50fc23b59da1d61256f0205ddc87a79286268a11862c2a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:30 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5ccd531a60c4bbb1082621a0a21646b6494b0e2f612e79a6778943268beed`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c651bbee8aea515b8055fcdde339bcbf1c6bb43eec92b29e344e9f52afb2d`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 7.0 MB (7032997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944c27da9e6c3f4181c98a5de2c3e6ac2ba74a492184ddf9cb918f6077e0ed1`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bb394cd41fc7b65a1b4279ab910c2b79893e79ff5968ec47b31269a7f6886c`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a49be050f1fb2cdeb4cdc180ef6c139faf00bc0adf3dda61f6e7b185ebed5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c55e36e6b13a9d983ce1406964734930adac2e1fa2707cebafdef63520d5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-scratch`

```console
$ docker pull nats@sha256:3b7b5f689b8b9055b95f9eedc3448de69c16808d427fa6295e5a6df3fb45e910
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

### `nats:2.14-scratch` - linux; amd64

```console
$ docker pull nats@sha256:65713a1834b75d00256f847cc7b8db5fea12121bbf341edfff76f84a76b56ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29535378bebe76ff33b25a0ee21ab0fe2346cb9bbd179ece59ab2f37f36e3c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b33128ccd2d9960d0a0ac0d31682c1928d1d17ca25caf107fa914eee12f346`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:82f0a5ca9b68dc2a87b53a0f1f9e9f5121208dbd998d0b36d56e9d11aba98464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ed450408ac2b61ff0b451c4f09ce61f26a1b3eb58a44c10cc2082ca924201`

```dockerfile
```

-	Layers:
	-	`sha256:4c738c96a15989941f46c5a6a4392bfbc566b311520062f8d56aa0637d39400a`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:340c3f31c2400ff9ce93e99a056a2f65376bb08bb66291dd626c08ce54ca68d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558fc4503cb023f4b5007d465ea651c8f3af04a4b3a5b6348ccd9c78575dfe55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:18 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055cbd39cde58dda5cd03328a647a1e169ff8116a012137ce777d015565a44d7`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4f0459213b2c44994bdbfc9af813a5f71ef1d00fba9c4e79cb15c7e2beefb67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63163d0fb60b2575e901b5e80f128020e9f3a5a2c610f865f3a750ea54a7fcdb`

```dockerfile
```

-	Layers:
	-	`sha256:527462491f781bce7f70496c4c9f2301b87cd5239c9f3ef5e83120fdb7370326`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7b3118869b74523b091cdec795dac3a3e7f7a69b0da2a0b5e1c4efbacb592fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6521bf98b02b2cf398c50c51930a34edf1c9da6a12a609b5d4ab2c01aab4f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:43:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:43:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:44:00 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:44:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3113ca534280e6c8acb2de55307064e1f8c2dce3fbe561d92a361be6754b8a`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:237ed08805072b07e68a19e104f07b16b22f4d8df845090f99164f396c4b7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf263674818d6f6280a468f63ff41db03882ca617c12d4e40e13f8920327b702`

```dockerfile
```

-	Layers:
	-	`sha256:db257913eec8f718988e940693bf52d60408882e903f08f9f45925a0f08e79e7`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cfd028112c875c7eda23860b3554e5e990356a1057bb17dd09a20a243372f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3cf3c1e911779b9fbfe69ca703bb69a2b7407e6227e3f9b70ebbca6f0a54d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:33 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:33 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46654056ed2549b3cbb7f0ff49c14926dda4483bfcae2e5b2ae45112ce5291d0`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:99443208695008b0853014ff29715108f78d0ab8da563be4c3e5e722cf8e3b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2669aa13c7dc6695ab85bcc4e2eca03332d9e1771e9a50b9d6b5155f28a0110b`

```dockerfile
```

-	Layers:
	-	`sha256:fe5804167a3e8df278aea8ff5b75538f93e08c74ce18b116e6b7a40f075195e8`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:52e2eb5749be9656b0a896ee1e1791cdf66fc1efc72030d918ce83f28c1f4b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0846d8047c28872a68ffbc2831a19d2d15e0289633332b837db0f98247d37b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6db89f1127caa8acb7e34214a9efc141739ecc0f49277d1680be7ab685b74a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe761e7f1baacb1015ae345dadf921feb545775f29fa241d4656fc0b7b0e944`

```dockerfile
```

-	Layers:
	-	`sha256:815bb78a9d851bd4d69340210b112479e7ac60e52474e9a946253c2311a5e235`  
		Last Modified: Mon, 22 Jun 2026 21:47:18 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; s390x

```console
$ docker pull nats@sha256:fdd9c60e91e3e32e1d99b1e31894da2950c99194fb8a6ec7f24bc0ed7f490049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6e32f278fd364210b5378b9c775f37669ca37425057b87159a3fe2d10fd82d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:03 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba8cfbf4bada82bc12acb2b704ab7a199791bf0fb2e58d599e28f76ebe3d6`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7e8a69f4f646da4a5a0227992c72916a23aab04732d77ebc784c36f884b53ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56240e620c437c2607b84cf23a0fcbe4e1c4d843764c2fcae214dc17dea78285`

```dockerfile
```

-	Layers:
	-	`sha256:122ffef264b9f423559e1565ffdf589e592490e2a938e73680b7bb7ed7542d9a`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-windowsservercore`

```console
$ docker pull nats@sha256:30c6818895521b905434c83a874393e80e00eeb16c99cb406aabc52f6e841305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:d40e99fe0996b55c987f43318922f0126afdf833dc64b80e4f671b914e531139
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140004525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f698c6ee75b2e0c38f746a238c8b58fc571f69d8b228708313334088f21b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:09:23 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 22:09:25 GMT
ENV NATS_SERVER=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 09 Jun 2026 22:09:30 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 09 Jun 2026 22:09:49 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Jun 2026 22:10:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Jun 2026 22:10:13 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 22:10:14 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 22:10:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 22:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09f22a9628ef0d5b0cc16feadb876572bfdd0fed92378ff8e8777f451c62ae3`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a64864617250f652dc21c56c17bc9e201bd6efaaaada8ecb0a289739097c68d`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963c12e26fa7cc56f2895b0da6e1e2d663354df97d44ac2608b1b8a1e2efa36f`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1b3ab9ee4bdedf123268ce980d9b19d98aa3d3de2daf1d225b362a2d2ec90f`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080f2b59d6248c1199ff79acaba8ff2fa41389c65f9a3408b946e558476599ce`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8304c7e0c6a110a2e1de5b1db6ee30548c1f9b35cdb8bf2dc2d8943f8e98ece`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faefef94c2375e90b22da5d12ab47156f4ee851848a1c5659e082cf88d307f1b`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 482.4 KB (482407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6105388623f6f433b4ca5aa8d008cd1aa1e17cbfc5fe71d61e59bb6dc076eeb8`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 7.4 MB (7382856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f98553f597398b2c6201727d08ba6c5c0f84e754f2ea050675bb48eba199a8`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6358666bb0ef21de38462ae43661dca2ddf92df690f233904c8846efeea044af`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed5830658244188816a211d85b730ad98d8a17d9356480f8b99bbf4249b58c`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462c0f6d3e6997ffe7696032948f9230f3093a8323b995cb6636f7fab7a04bb9`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:30c6818895521b905434c83a874393e80e00eeb16c99cb406aabc52f6e841305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:d40e99fe0996b55c987f43318922f0126afdf833dc64b80e4f671b914e531139
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140004525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f698c6ee75b2e0c38f746a238c8b58fc571f69d8b228708313334088f21b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:09:23 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 22:09:25 GMT
ENV NATS_SERVER=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 09 Jun 2026 22:09:30 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 09 Jun 2026 22:09:49 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Jun 2026 22:10:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Jun 2026 22:10:13 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 22:10:14 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 22:10:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 22:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09f22a9628ef0d5b0cc16feadb876572bfdd0fed92378ff8e8777f451c62ae3`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a64864617250f652dc21c56c17bc9e201bd6efaaaada8ecb0a289739097c68d`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963c12e26fa7cc56f2895b0da6e1e2d663354df97d44ac2608b1b8a1e2efa36f`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1b3ab9ee4bdedf123268ce980d9b19d98aa3d3de2daf1d225b362a2d2ec90f`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080f2b59d6248c1199ff79acaba8ff2fa41389c65f9a3408b946e558476599ce`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8304c7e0c6a110a2e1de5b1db6ee30548c1f9b35cdb8bf2dc2d8943f8e98ece`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faefef94c2375e90b22da5d12ab47156f4ee851848a1c5659e082cf88d307f1b`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 482.4 KB (482407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6105388623f6f433b4ca5aa8d008cd1aa1e17cbfc5fe71d61e59bb6dc076eeb8`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 7.4 MB (7382856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f98553f597398b2c6201727d08ba6c5c0f84e754f2ea050675bb48eba199a8`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6358666bb0ef21de38462ae43661dca2ddf92df690f233904c8846efeea044af`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed5830658244188816a211d85b730ad98d8a17d9356480f8b99bbf4249b58c`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462c0f6d3e6997ffe7696032948f9230f3093a8323b995cb6636f7fab7a04bb9`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.3`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.3-alpine`

```console
$ docker pull nats@sha256:ca6e0b64f0caee7e1edd17bfa8a31161e73aa35c112b01b7ba6fc762ffa9dc01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.14.3-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.3-alpine3.22`

```console
$ docker pull nats@sha256:ca6e0b64f0caee7e1edd17bfa8a31161e73aa35c112b01b7ba6fc762ffa9dc01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.14.3-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.3-linux`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.3-nanoserver`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.3-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.3-scratch`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.3-windowsservercore`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:2.14.3-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `nats:alpine`

```console
$ docker pull nats@sha256:3c66911d53d63e76dd733c7994ca544c28602cafc68f27fbf47dbb8e37205e57
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
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:afa0021fd5534b5898b5a146edea9264c8db26144b792c10a5315a35bbbac5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10482561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b85446ce3f424e4511a6ec5bcc77ecab084eb56464f1f1d28046674ab67a651`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677c5f86a68cf2ce1fdf51d3b53c56b92e7fbe3b67443d993c093aac9e6a00f`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 7.0 MB (6986793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea037dcf8136a7791f9e560bda59f20a5e40ee8d447c9b81a75253956c52d2c`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91efd4d63f2001f13a850754a14e04788257c1dbe8f26cf095f7cc64ca2b5913`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:7d4eebf896ed7b471bfb246e8823a02079e74eb6195ffc6edbc4246539be1a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4004102106793942ddb14115cf0e0684cc23e759a6ffca0eb4c60dd06d05b2fc`

```dockerfile
```

-	Layers:
	-	`sha256:cd7784700079db7a9f22cc194e5d89197a178370899405a829e82b5a633e3afe`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:91683fb37479895c178784386781a757532946afd57131bb405b062581ebef75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10188544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49ae72c112bb15690a11d8a5b7aa735cd4245c99549bce10acb4dc49a476ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8b795a8aa2f5335674b36741b17ce192443d940da95f3bbd597b70531689e3`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 7.0 MB (6977963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5097219f08bd67d8fa2e25a5a479e8bd0385d6216ab6343a4aa1875eb26304`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8e33bc51c0528dbfa912e61fdcfc8e25b5a0c5ed8ff2e87ebc145a65aa1605`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:753a5ea794f4139e119be983748b07d2258ba219fca43ac667a4533c6e30a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b52454a96ab80fa5715d09b55b91072a66c893f75f0d94f5e43b01767f6c542`

```dockerfile
```

-	Layers:
	-	`sha256:a85da325cca4163e5d72d726f4f96a446323aa0b460ea8f228953398ba6b6171`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4267586f8d1941e8955323b0014cba3b61f65881b4c4c20de688fbe1c5fea804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10724412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f145de50057f413858c406b87310468fc4bd3effd1f88e329cf02fea0239e1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cfbf804236b512a4b9944ec56130b32a28b0a4b77458c90970f66f3a589254`  
		Last Modified: Mon, 22 Jun 2026 19:47:17 GMT  
		Size: 6.6 MB (6602958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c950a70aceecc1179a9c484d238f8ec42132ddf44f71978023a2ac0e56fc0`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f2ccaf61966a62729b5a1cfbdf7e05d864310ac230029a8a9cf60d0967ec7`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5deeca0a3264b5d656b04246f1c17f72ca74115b5de8e356adbe225c80c755bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51798bd8628e715c409906689a2cf6fac8b1fee280fd2920de1e6a379bc4c6`

```dockerfile
```

-	Layers:
	-	`sha256:f0614b048154314f9962518fc36f249b39de8d985648d33ef1ce4bb9369f3f4a`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:3c66911d53d63e76dd733c7994ca544c28602cafc68f27fbf47dbb8e37205e57
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
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:afa0021fd5534b5898b5a146edea9264c8db26144b792c10a5315a35bbbac5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10482561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b85446ce3f424e4511a6ec5bcc77ecab084eb56464f1f1d28046674ab67a651`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:46:05 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:46:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:46:05 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677c5f86a68cf2ce1fdf51d3b53c56b92e7fbe3b67443d993c093aac9e6a00f`  
		Last Modified: Mon, 22 Jun 2026 19:46:10 GMT  
		Size: 7.0 MB (6986793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea037dcf8136a7791f9e560bda59f20a5e40ee8d447c9b81a75253956c52d2c`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91efd4d63f2001f13a850754a14e04788257c1dbe8f26cf095f7cc64ca2b5913`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7d4eebf896ed7b471bfb246e8823a02079e74eb6195ffc6edbc4246539be1a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4004102106793942ddb14115cf0e0684cc23e759a6ffca0eb4c60dd06d05b2fc`

```dockerfile
```

-	Layers:
	-	`sha256:cd7784700079db7a9f22cc194e5d89197a178370899405a829e82b5a633e3afe`  
		Last Modified: Mon, 22 Jun 2026 19:46:09 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:91683fb37479895c178784386781a757532946afd57131bb405b062581ebef75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10188544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df49ae72c112bb15690a11d8a5b7aa735cd4245c99549bce10acb4dc49a476ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:55:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:55:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:55:16 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8b795a8aa2f5335674b36741b17ce192443d940da95f3bbd597b70531689e3`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 7.0 MB (6977963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5097219f08bd67d8fa2e25a5a479e8bd0385d6216ab6343a4aa1875eb26304`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8e33bc51c0528dbfa912e61fdcfc8e25b5a0c5ed8ff2e87ebc145a65aa1605`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:753a5ea794f4139e119be983748b07d2258ba219fca43ac667a4533c6e30a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b52454a96ab80fa5715d09b55b91072a66c893f75f0d94f5e43b01767f6c542`

```dockerfile
```

-	Layers:
	-	`sha256:a85da325cca4163e5d72d726f4f96a446323aa0b460ea8f228953398ba6b6171`  
		Last Modified: Mon, 22 Jun 2026 19:55:20 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4267586f8d1941e8955323b0014cba3b61f65881b4c4c20de688fbe1c5fea804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10724412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f145de50057f413858c406b87310468fc4bd3effd1f88e329cf02fea0239e1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
ENV NATS_SERVER=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Mon, 22 Jun 2026 19:47:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Jun 2026 19:47:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 19:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:47:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cfbf804236b512a4b9944ec56130b32a28b0a4b77458c90970f66f3a589254`  
		Last Modified: Mon, 22 Jun 2026 19:47:17 GMT  
		Size: 6.6 MB (6602958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c950a70aceecc1179a9c484d238f8ec42132ddf44f71978023a2ac0e56fc0`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8f2ccaf61966a62729b5a1cfbdf7e05d864310ac230029a8a9cf60d0967ec7`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5deeca0a3264b5d656b04246f1c17f72ca74115b5de8e356adbe225c80c755bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a51798bd8628e715c409906689a2cf6fac8b1fee280fd2920de1e6a379bc4c6`

```dockerfile
```

-	Layers:
	-	`sha256:f0614b048154314f9962518fc36f249b39de8d985648d33ef1ce4bb9369f3f4a`  
		Last Modified: Mon, 22 Jun 2026 19:47:16 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:bbfbb6c4cdaeb8a2e3ca57d3de30463a66a6c5181f324f3b680bcf858833d377
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
	-	windows version 10.0.20348.5256; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:65713a1834b75d00256f847cc7b8db5fea12121bbf341edfff76f84a76b56ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29535378bebe76ff33b25a0ee21ab0fe2346cb9bbd179ece59ab2f37f36e3c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b33128ccd2d9960d0a0ac0d31682c1928d1d17ca25caf107fa914eee12f346`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:82f0a5ca9b68dc2a87b53a0f1f9e9f5121208dbd998d0b36d56e9d11aba98464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ed450408ac2b61ff0b451c4f09ce61f26a1b3eb58a44c10cc2082ca924201`

```dockerfile
```

-	Layers:
	-	`sha256:4c738c96a15989941f46c5a6a4392bfbc566b311520062f8d56aa0637d39400a`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:340c3f31c2400ff9ce93e99a056a2f65376bb08bb66291dd626c08ce54ca68d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558fc4503cb023f4b5007d465ea651c8f3af04a4b3a5b6348ccd9c78575dfe55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:18 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055cbd39cde58dda5cd03328a647a1e169ff8116a012137ce777d015565a44d7`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:4f0459213b2c44994bdbfc9af813a5f71ef1d00fba9c4e79cb15c7e2beefb67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63163d0fb60b2575e901b5e80f128020e9f3a5a2c610f865f3a750ea54a7fcdb`

```dockerfile
```

-	Layers:
	-	`sha256:527462491f781bce7f70496c4c9f2301b87cd5239c9f3ef5e83120fdb7370326`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7b3118869b74523b091cdec795dac3a3e7f7a69b0da2a0b5e1c4efbacb592fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6521bf98b02b2cf398c50c51930a34edf1c9da6a12a609b5d4ab2c01aab4f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:43:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:43:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:44:00 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:44:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3113ca534280e6c8acb2de55307064e1f8c2dce3fbe561d92a361be6754b8a`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:237ed08805072b07e68a19e104f07b16b22f4d8df845090f99164f396c4b7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf263674818d6f6280a468f63ff41db03882ca617c12d4e40e13f8920327b702`

```dockerfile
```

-	Layers:
	-	`sha256:db257913eec8f718988e940693bf52d60408882e903f08f9f45925a0f08e79e7`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cfd028112c875c7eda23860b3554e5e990356a1057bb17dd09a20a243372f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3cf3c1e911779b9fbfe69ca703bb69a2b7407e6227e3f9b70ebbca6f0a54d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:33 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:33 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46654056ed2549b3cbb7f0ff49c14926dda4483bfcae2e5b2ae45112ce5291d0`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:99443208695008b0853014ff29715108f78d0ab8da563be4c3e5e722cf8e3b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2669aa13c7dc6695ab85bcc4e2eca03332d9e1771e9a50b9d6b5155f28a0110b`

```dockerfile
```

-	Layers:
	-	`sha256:fe5804167a3e8df278aea8ff5b75538f93e08c74ce18b116e6b7a40f075195e8`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:52e2eb5749be9656b0a896ee1e1791cdf66fc1efc72030d918ce83f28c1f4b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0846d8047c28872a68ffbc2831a19d2d15e0289633332b837db0f98247d37b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:6db89f1127caa8acb7e34214a9efc141739ecc0f49277d1680be7ab685b74a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe761e7f1baacb1015ae345dadf921feb545775f29fa241d4656fc0b7b0e944`

```dockerfile
```

-	Layers:
	-	`sha256:815bb78a9d851bd4d69340210b112479e7ac60e52474e9a946253c2311a5e235`  
		Last Modified: Mon, 22 Jun 2026 21:47:18 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:fdd9c60e91e3e32e1d99b1e31894da2950c99194fb8a6ec7f24bc0ed7f490049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6e32f278fd364210b5378b9c775f37669ca37425057b87159a3fe2d10fd82d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:03 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba8cfbf4bada82bc12acb2b704ab7a199791bf0fb2e58d599e28f76ebe3d6`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:7e8a69f4f646da4a5a0227992c72916a23aab04732d77ebc784c36f884b53ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56240e620c437c2607b84cf23a0fcbe4e1c4d843764c2fcae214dc17dea78285`

```dockerfile
```

-	Layers:
	-	`sha256:122ffef264b9f423559e1565ffdf589e592490e2a938e73680b7bb7ed7542d9a`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:0badb754748fd4de2327f7cca2a86ef00b94e6c26569e80e707b706f27325db5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131036450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47805c9ad0d2cf7cad50fc23b59da1d61256f0205ddc87a79286268a11862c2a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:30 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5ccd531a60c4bbb1082621a0a21646b6494b0e2f612e79a6778943268beed`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c651bbee8aea515b8055fcdde339bcbf1c6bb43eec92b29e344e9f52afb2d`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 7.0 MB (7032997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944c27da9e6c3f4181c98a5de2c3e6ac2ba74a492184ddf9cb918f6077e0ed1`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bb394cd41fc7b65a1b4279ab910c2b79893e79ff5968ec47b31269a7f6886c`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a49be050f1fb2cdeb4cdc180ef6c139faf00bc0adf3dda61f6e7b185ebed5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c55e36e6b13a9d983ce1406964734930adac2e1fa2707cebafdef63520d5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:3b7b5f689b8b9055b95f9eedc3448de69c16808d427fa6295e5a6df3fb45e910
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
$ docker pull nats@sha256:65713a1834b75d00256f847cc7b8db5fea12121bbf341edfff76f84a76b56ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29535378bebe76ff33b25a0ee21ab0fe2346cb9bbd179ece59ab2f37f36e3c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b33128ccd2d9960d0a0ac0d31682c1928d1d17ca25caf107fa914eee12f346`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:82f0a5ca9b68dc2a87b53a0f1f9e9f5121208dbd998d0b36d56e9d11aba98464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ed450408ac2b61ff0b451c4f09ce61f26a1b3eb58a44c10cc2082ca924201`

```dockerfile
```

-	Layers:
	-	`sha256:4c738c96a15989941f46c5a6a4392bfbc566b311520062f8d56aa0637d39400a`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:340c3f31c2400ff9ce93e99a056a2f65376bb08bb66291dd626c08ce54ca68d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558fc4503cb023f4b5007d465ea651c8f3af04a4b3a5b6348ccd9c78575dfe55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:18 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055cbd39cde58dda5cd03328a647a1e169ff8116a012137ce777d015565a44d7`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:4f0459213b2c44994bdbfc9af813a5f71ef1d00fba9c4e79cb15c7e2beefb67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63163d0fb60b2575e901b5e80f128020e9f3a5a2c610f865f3a750ea54a7fcdb`

```dockerfile
```

-	Layers:
	-	`sha256:527462491f781bce7f70496c4c9f2301b87cd5239c9f3ef5e83120fdb7370326`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7b3118869b74523b091cdec795dac3a3e7f7a69b0da2a0b5e1c4efbacb592fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6521bf98b02b2cf398c50c51930a34edf1c9da6a12a609b5d4ab2c01aab4f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:43:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:43:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:44:00 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:44:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3113ca534280e6c8acb2de55307064e1f8c2dce3fbe561d92a361be6754b8a`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:237ed08805072b07e68a19e104f07b16b22f4d8df845090f99164f396c4b7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf263674818d6f6280a468f63ff41db03882ca617c12d4e40e13f8920327b702`

```dockerfile
```

-	Layers:
	-	`sha256:db257913eec8f718988e940693bf52d60408882e903f08f9f45925a0f08e79e7`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cfd028112c875c7eda23860b3554e5e990356a1057bb17dd09a20a243372f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3cf3c1e911779b9fbfe69ca703bb69a2b7407e6227e3f9b70ebbca6f0a54d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:33 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:33 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46654056ed2549b3cbb7f0ff49c14926dda4483bfcae2e5b2ae45112ce5291d0`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:99443208695008b0853014ff29715108f78d0ab8da563be4c3e5e722cf8e3b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2669aa13c7dc6695ab85bcc4e2eca03332d9e1771e9a50b9d6b5155f28a0110b`

```dockerfile
```

-	Layers:
	-	`sha256:fe5804167a3e8df278aea8ff5b75538f93e08c74ce18b116e6b7a40f075195e8`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:52e2eb5749be9656b0a896ee1e1791cdf66fc1efc72030d918ce83f28c1f4b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0846d8047c28872a68ffbc2831a19d2d15e0289633332b837db0f98247d37b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:6db89f1127caa8acb7e34214a9efc141739ecc0f49277d1680be7ab685b74a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe761e7f1baacb1015ae345dadf921feb545775f29fa241d4656fc0b7b0e944`

```dockerfile
```

-	Layers:
	-	`sha256:815bb78a9d851bd4d69340210b112479e7ac60e52474e9a946253c2311a5e235`  
		Last Modified: Mon, 22 Jun 2026 21:47:18 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:fdd9c60e91e3e32e1d99b1e31894da2950c99194fb8a6ec7f24bc0ed7f490049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6e32f278fd364210b5378b9c775f37669ca37425057b87159a3fe2d10fd82d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:03 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba8cfbf4bada82bc12acb2b704ab7a199791bf0fb2e58d599e28f76ebe3d6`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:7e8a69f4f646da4a5a0227992c72916a23aab04732d77ebc784c36f884b53ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56240e620c437c2607b84cf23a0fcbe4e1c4d843764c2fcae214dc17dea78285`

```dockerfile
```

-	Layers:
	-	`sha256:122ffef264b9f423559e1565ffdf589e592490e2a938e73680b7bb7ed7542d9a`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:9622b8c98b2488b8efd76eefe88e2b019d542d6de0e04db7af8d21e067f39ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:0badb754748fd4de2327f7cca2a86ef00b94e6c26569e80e707b706f27325db5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131036450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47805c9ad0d2cf7cad50fc23b59da1d61256f0205ddc87a79286268a11862c2a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:30 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5ccd531a60c4bbb1082621a0a21646b6494b0e2f612e79a6778943268beed`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c651bbee8aea515b8055fcdde339bcbf1c6bb43eec92b29e344e9f52afb2d`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 7.0 MB (7032997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944c27da9e6c3f4181c98a5de2c3e6ac2ba74a492184ddf9cb918f6077e0ed1`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bb394cd41fc7b65a1b4279ab910c2b79893e79ff5968ec47b31269a7f6886c`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a49be050f1fb2cdeb4cdc180ef6c139faf00bc0adf3dda61f6e7b185ebed5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c55e36e6b13a9d983ce1406964734930adac2e1fa2707cebafdef63520d5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:9622b8c98b2488b8efd76eefe88e2b019d542d6de0e04db7af8d21e067f39ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:0badb754748fd4de2327f7cca2a86ef00b94e6c26569e80e707b706f27325db5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131036450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47805c9ad0d2cf7cad50fc23b59da1d61256f0205ddc87a79286268a11862c2a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:20:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 23:20:30 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 23:20:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 23:20:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 23:20:33 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5ccd531a60c4bbb1082621a0a21646b6494b0e2f612e79a6778943268beed`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2c651bbee8aea515b8055fcdde339bcbf1c6bb43eec92b29e344e9f52afb2d`  
		Last Modified: Tue, 09 Jun 2026 23:20:39 GMT  
		Size: 7.0 MB (7032997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944c27da9e6c3f4181c98a5de2c3e6ac2ba74a492184ddf9cb918f6077e0ed1`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bb394cd41fc7b65a1b4279ab910c2b79893e79ff5968ec47b31269a7f6886c`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64a49be050f1fb2cdeb4cdc180ef6c139faf00bc0adf3dda61f6e7b185ebed5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f77c55e36e6b13a9d983ce1406964734930adac2e1fa2707cebafdef63520d5`  
		Last Modified: Tue, 09 Jun 2026 23:20:37 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:3b7b5f689b8b9055b95f9eedc3448de69c16808d427fa6295e5a6df3fb45e910
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
$ docker pull nats@sha256:65713a1834b75d00256f847cc7b8db5fea12121bbf341edfff76f84a76b56ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29535378bebe76ff33b25a0ee21ab0fe2346cb9bbd179ece59ab2f37f36e3c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:17:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:17:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:17:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:17:12 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:17:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b33128ccd2d9960d0a0ac0d31682c1928d1d17ca25caf107fa914eee12f346`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:82f0a5ca9b68dc2a87b53a0f1f9e9f5121208dbd998d0b36d56e9d11aba98464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ed450408ac2b61ff0b451c4f09ce61f26a1b3eb58a44c10cc2082ca924201`

```dockerfile
```

-	Layers:
	-	`sha256:4c738c96a15989941f46c5a6a4392bfbc566b311520062f8d56aa0637d39400a`  
		Last Modified: Mon, 22 Jun 2026 20:17:17 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:340c3f31c2400ff9ce93e99a056a2f65376bb08bb66291dd626c08ce54ca68d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558fc4503cb023f4b5007d465ea651c8f3af04a4b3a5b6348ccd9c78575dfe55`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:32:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:32:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:32:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:32:18 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:32:18 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055cbd39cde58dda5cd03328a647a1e169ff8116a012137ce777d015565a44d7`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4f0459213b2c44994bdbfc9af813a5f71ef1d00fba9c4e79cb15c7e2beefb67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63163d0fb60b2575e901b5e80f128020e9f3a5a2c610f865f3a750ea54a7fcdb`

```dockerfile
```

-	Layers:
	-	`sha256:527462491f781bce7f70496c4c9f2301b87cd5239c9f3ef5e83120fdb7370326`  
		Last Modified: Mon, 22 Jun 2026 20:32:22 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7b3118869b74523b091cdec795dac3a3e7f7a69b0da2a0b5e1c4efbacb592fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6521bf98b02b2cf398c50c51930a34edf1c9da6a12a609b5d4ab2c01aab4f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:43:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:43:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:44:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:44:00 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:44:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3113ca534280e6c8acb2de55307064e1f8c2dce3fbe561d92a361be6754b8a`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:237ed08805072b07e68a19e104f07b16b22f4d8df845090f99164f396c4b7393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf263674818d6f6280a468f63ff41db03882ca617c12d4e40e13f8920327b702`

```dockerfile
```

-	Layers:
	-	`sha256:db257913eec8f718988e940693bf52d60408882e903f08f9f45925a0f08e79e7`  
		Last Modified: Mon, 22 Jun 2026 20:44:04 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cfd028112c875c7eda23860b3554e5e990356a1057bb17dd09a20a243372f064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff3cf3c1e911779b9fbfe69ca703bb69a2b7407e6227e3f9b70ebbca6f0a54d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 20:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 20:52:33 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 20:52:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 20:52:33 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 20:52:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46654056ed2549b3cbb7f0ff49c14926dda4483bfcae2e5b2ae45112ce5291d0`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:99443208695008b0853014ff29715108f78d0ab8da563be4c3e5e722cf8e3b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2669aa13c7dc6695ab85bcc4e2eca03332d9e1771e9a50b9d6b5155f28a0110b`

```dockerfile
```

-	Layers:
	-	`sha256:fe5804167a3e8df278aea8ff5b75538f93e08c74ce18b116e6b7a40f075195e8`  
		Last Modified: Mon, 22 Jun 2026 20:52:37 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:52e2eb5749be9656b0a896ee1e1791cdf66fc1efc72030d918ce83f28c1f4b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0846d8047c28872a68ffbc2831a19d2d15e0289633332b837db0f98247d37b2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:47:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:47:11 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:47:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:47:11 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:47:11 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd27332a0709a7869d40b2bf3db90d4ccd7181a72955d26d374d1820f74692`  
		Last Modified: Mon, 22 Jun 2026 21:47:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6db89f1127caa8acb7e34214a9efc141739ecc0f49277d1680be7ab685b74a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe761e7f1baacb1015ae345dadf921feb545775f29fa241d4656fc0b7b0e944`

```dockerfile
```

-	Layers:
	-	`sha256:815bb78a9d851bd4d69340210b112479e7ac60e52474e9a946253c2311a5e235`  
		Last Modified: Mon, 22 Jun 2026 21:47:18 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:fdd9c60e91e3e32e1d99b1e31894da2950c99194fb8a6ec7f24bc0ed7f490049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6e32f278fd364210b5378b9c775f37669ca37425057b87159a3fe2d10fd82d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 21:13:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 22 Jun 2026 21:13:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 22 Jun 2026 21:13:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Jun 2026 21:13:03 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 22 Jun 2026 21:13:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba8cfbf4bada82bc12acb2b704ab7a199791bf0fb2e58d599e28f76ebe3d6`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7e8a69f4f646da4a5a0227992c72916a23aab04732d77ebc784c36f884b53ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56240e620c437c2607b84cf23a0fcbe4e1c4d843764c2fcae214dc17dea78285`

```dockerfile
```

-	Layers:
	-	`sha256:122ffef264b9f423559e1565ffdf589e592490e2a938e73680b7bb7ed7542d9a`  
		Last Modified: Mon, 22 Jun 2026 21:13:10 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:30c6818895521b905434c83a874393e80e00eeb16c99cb406aabc52f6e841305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:d40e99fe0996b55c987f43318922f0126afdf833dc64b80e4f671b914e531139
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140004525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f698c6ee75b2e0c38f746a238c8b58fc571f69d8b228708313334088f21b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:09:23 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 22:09:25 GMT
ENV NATS_SERVER=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 09 Jun 2026 22:09:30 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 09 Jun 2026 22:09:49 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Jun 2026 22:10:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Jun 2026 22:10:13 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 22:10:14 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 22:10:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 22:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09f22a9628ef0d5b0cc16feadb876572bfdd0fed92378ff8e8777f451c62ae3`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a64864617250f652dc21c56c17bc9e201bd6efaaaada8ecb0a289739097c68d`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963c12e26fa7cc56f2895b0da6e1e2d663354df97d44ac2608b1b8a1e2efa36f`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1b3ab9ee4bdedf123268ce980d9b19d98aa3d3de2daf1d225b362a2d2ec90f`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080f2b59d6248c1199ff79acaba8ff2fa41389c65f9a3408b946e558476599ce`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8304c7e0c6a110a2e1de5b1db6ee30548c1f9b35cdb8bf2dc2d8943f8e98ece`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faefef94c2375e90b22da5d12ab47156f4ee851848a1c5659e082cf88d307f1b`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 482.4 KB (482407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6105388623f6f433b4ca5aa8d008cd1aa1e17cbfc5fe71d61e59bb6dc076eeb8`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 7.4 MB (7382856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f98553f597398b2c6201727d08ba6c5c0f84e754f2ea050675bb48eba199a8`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6358666bb0ef21de38462ae43661dca2ddf92df690f233904c8846efeea044af`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed5830658244188816a211d85b730ad98d8a17d9356480f8b99bbf4249b58c`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462c0f6d3e6997ffe7696032948f9230f3093a8323b995cb6636f7fab7a04bb9`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:30c6818895521b905434c83a874393e80e00eeb16c99cb406aabc52f6e841305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:d40e99fe0996b55c987f43318922f0126afdf833dc64b80e4f671b914e531139
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140004525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f698c6ee75b2e0c38f746a238c8b58fc571f69d8b228708313334088f21b5`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:09:23 GMT
ENV NATS_DOCKERIZED=1
# Tue, 09 Jun 2026 22:09:25 GMT
ENV NATS_SERVER=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 09 Jun 2026 22:09:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 09 Jun 2026 22:09:30 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 09 Jun 2026 22:09:49 GMT
RUN Set-PSDebug -Trace 2
# Tue, 09 Jun 2026 22:10:13 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 09 Jun 2026 22:10:13 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 09 Jun 2026 22:10:14 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Jun 2026 22:10:15 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 09 Jun 2026 22:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09f22a9628ef0d5b0cc16feadb876572bfdd0fed92378ff8e8777f451c62ae3`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a64864617250f652dc21c56c17bc9e201bd6efaaaada8ecb0a289739097c68d`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963c12e26fa7cc56f2895b0da6e1e2d663354df97d44ac2608b1b8a1e2efa36f`  
		Last Modified: Tue, 09 Jun 2026 22:10:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1b3ab9ee4bdedf123268ce980d9b19d98aa3d3de2daf1d225b362a2d2ec90f`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080f2b59d6248c1199ff79acaba8ff2fa41389c65f9a3408b946e558476599ce`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8304c7e0c6a110a2e1de5b1db6ee30548c1f9b35cdb8bf2dc2d8943f8e98ece`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faefef94c2375e90b22da5d12ab47156f4ee851848a1c5659e082cf88d307f1b`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 482.4 KB (482407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6105388623f6f433b4ca5aa8d008cd1aa1e17cbfc5fe71d61e59bb6dc076eeb8`  
		Last Modified: Tue, 09 Jun 2026 22:10:22 GMT  
		Size: 7.4 MB (7382856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f98553f597398b2c6201727d08ba6c5c0f84e754f2ea050675bb48eba199a8`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6358666bb0ef21de38462ae43661dca2ddf92df690f233904c8846efeea044af`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed5830658244188816a211d85b730ad98d8a17d9356480f8b99bbf4249b58c`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462c0f6d3e6997ffe7696032948f9230f3093a8323b995cb6636f7fab7a04bb9`  
		Last Modified: Tue, 09 Jun 2026 22:10:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
