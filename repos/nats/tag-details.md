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
-	[`nats:2.12.11`](#nats21211)
-	[`nats:2.12.11-alpine`](#nats21211-alpine)
-	[`nats:2.12.11-alpine3.22`](#nats21211-alpine322)
-	[`nats:2.12.11-linux`](#nats21211-linux)
-	[`nats:2.12.11-nanoserver`](#nats21211-nanoserver)
-	[`nats:2.12.11-nanoserver-ltsc2022`](#nats21211-nanoserver-ltsc2022)
-	[`nats:2.12.11-scratch`](#nats21211-scratch)
-	[`nats:2.12.11-windowsservercore`](#nats21211-windowsservercore)
-	[`nats:2.12.11-windowsservercore-ltsc2022`](#nats21211-windowsservercore-ltsc2022)
-	[`nats:2.14`](#nats214)
-	[`nats:2.14-alpine`](#nats214-alpine)
-	[`nats:2.14-alpine3.22`](#nats214-alpine322)
-	[`nats:2.14-linux`](#nats214-linux)
-	[`nats:2.14-nanoserver`](#nats214-nanoserver)
-	[`nats:2.14-nanoserver-ltsc2022`](#nats214-nanoserver-ltsc2022)
-	[`nats:2.14-scratch`](#nats214-scratch)
-	[`nats:2.14-windowsservercore`](#nats214-windowsservercore)
-	[`nats:2.14-windowsservercore-ltsc2022`](#nats214-windowsservercore-ltsc2022)
-	[`nats:2.14.2`](#nats2142)
-	[`nats:2.14.2-alpine`](#nats2142-alpine)
-	[`nats:2.14.2-alpine3.22`](#nats2142-alpine322)
-	[`nats:2.14.2-linux`](#nats2142-linux)
-	[`nats:2.14.2-nanoserver`](#nats2142-nanoserver)
-	[`nats:2.14.2-nanoserver-ltsc2022`](#nats2142-nanoserver-ltsc2022)
-	[`nats:2.14.2-scratch`](#nats2142-scratch)
-	[`nats:2.14.2-windowsservercore`](#nats2142-windowsservercore)
-	[`nats:2.14.2-windowsservercore-ltsc2022`](#nats2142-windowsservercore-ltsc2022)
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
$ docker pull nats@sha256:771149b0d90eca2137d24c8d205521fec157e38510f2b46e9fc370e54ae4262f
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
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
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
$ docker pull nats@sha256:b039b46715673a9436989cfc49dde04e6bd57e205347478a58214789baf5efdc
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
$ docker pull nats@sha256:f0679b55723570b245b735087116f40b61209f9419a052555911d92ba92db3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f2c459fccd79c9b1768d7235853736817cc95553a4a77e0fcc60d748ded94c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91149e471871c2ede088818330273446a46a28fa17ab6019c347e827f3d88e`  
		Last Modified: Tue, 02 Jun 2026 19:05:14 GMT  
		Size: 7.3 MB (7294356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1780775af23cf70b20cc6730511246e7e72d42ce7d668c73c18b90d48a67a01`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db4d3abeff2b99495264a4eee8c173e4cddac6f2562cf176849969f8bfeb6f5`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:433ad5e1cd4d4638ba012ef6d511de6ada4d25848d45a59a419c4e8c8f212504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5457ab88186ec095f87e6383750982f83261069aa7d81add3cf4e931d5bd8b8d`

```dockerfile
```

-	Layers:
	-	`sha256:97908037527cfc59a216bfe62a51d23f134332356fa5e4b7cb247741bdd17194`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bd43cfbbeacf6edb2b475c63866eb39de3639ff98c7ba4b2e864136daf55afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10542108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb38008b73bdfef49b080f538c56c59c970defde4adf819ce4be46eb115f13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4134644628fbe8c80ca77808206ab4ff2c01c11c3c49f656c7120757e9b9d8`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 7.0 MB (7033752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37f54e57d50f3a9c76dd3ddbf500d95b6c7e85c7c07aa48147c6cdd9defbe4`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f867e1babe5c47998841c28bded391ef496d71feb54b61f4545d87f5a646cba`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:41db50f6cc4d9bfd6ec2c46f419eed60136e695a19f5892004fc8e16f9e4c958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacd6b789756bea2927e2e1131c952cd3ad9c48cb279eb3eb6303fc9ab294d2f`

```dockerfile
```

-	Layers:
	-	`sha256:5e30d67018b50219cf111359b9c01c0f494e08d2b3f8569dcc5fd3c1ee5c1d73`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:ad14dda00ccf242342a93cc85db34a56bb25d3e296ecdace5147c1966b5b3b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10247947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec25b1ccdde1f720071b74505ffdf00e039ab69a2fd75f71d020027bd2c0a7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9df1ef32961e68a3939cd854cdbbf23eadb85878e7a2924c8e8b55ed686db`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 7.0 MB (7021143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3a2252f7f49291e414a088e7d5d7d5b1ed30e39570d7aaaddefe72ad7ec45`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f706a5b129742a751a90778c239816e2f65e8da796265eea974d0684885fe`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:37cb5f4f11c03e9635452373f12b4933fd563eb9d9b579fa4d81074c310b783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8831237e5b1eb42138b1b533eac461905370c52864faa74ad64aa64ee6929ea9`

```dockerfile
```

-	Layers:
	-	`sha256:8b0c0c197e4c11be4cea42928534aba725c08e8453c25ec9bc3b3d17f826cd06`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:611c3dbd05ff98e9f9f562b4ecc89822c2b0367847d932a4932c1ed966bc9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10792301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a4b2095da890cb3d5ca21aa5d61d37c4ca5fd0cde2e2037c3552e8b346140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967f1732be2cea3277e46b05ada1d6dc6dc0c9d759046c2618be783fee259b3`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.6 MB (6649438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729dba32d18e040f985909e362d966b7bdd5bb98293da5c5b092b2db7b1ad6c`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd385b5d9562cba05d122624afc347bf04e331b1039428b62bfa34329ae6fc`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83650089aa5af8edeacd31f9575f51c4865f49f4658f5e4783da1893cbd73665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ea3db6409708bdb914b77d4ccc8d0aeb240671d5247e30d10994a292bed6a`

```dockerfile
```

-	Layers:
	-	`sha256:0e0bb2fa8f0c108b876e46f52d13f30f36c80387b8275abc10d23d94c3c159f2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:03cac3b8dd8dfa41d75112c2ae5b94fec0af6f5814730e5330012354cf7f0827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447bf89722c6586ace97b811cfa21359201cf2f9713c5e1fef6213a7acc2650e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:09:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:09:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a55d0eaca97f0390033ffa8d9134bc7a0079525bf40c87025873115014fab03`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.7 MB (6712091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e475251befa77978ceea2dd486692601fdf578dc6cf93f6f34db105424faa429`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd101bdee386ea23d9751c471412ed9d61e7b3bb95fa9c4c09dcf11b393862b0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:878c6cd3e6ca2b63e8e7c9012c4a51e6f964a8e1f17a510c05f7000a2ee3c3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b43654f9754af02840c24097bead60f9bda1a56f0d0331c1cdb97492d058d1d`

```dockerfile
```

-	Layers:
	-	`sha256:277a9558e629945d4f89fbecb1fece232afa05343087d445fab71410b96445a5`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:841b7ad0b071063eab531f42992071e88a18027757dc688943e9b6be84f30b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10758432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8d5496bf4f8dc7bc2e68a44462403d27657a08420f26e155ef56c4b875cd1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9e1c021cb6668546fbd3caeb13392781503722c1117940072299d8a401f78`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 7.1 MB (7103589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7207403655133bcd046b16235270ff4b177f4e43d2903766cfb7a82d247e914`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107699ca626db0b1dca70dd8b094467bb9da6bad2e7b07a3e817e656f0528716`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d93ecdc48d72d516e5b6b434a8f943f9a0a356ea2e81c18a79d46fa97dac3cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e2b39405c34660d72439c24d374ad63c17ff6072b7967c16a05e3d681f075e`

```dockerfile
```

-	Layers:
	-	`sha256:73ea22818eaf35e7185adc8c19baf720eec4e2f32f9e2f8eefc0ae10f85ea059`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:b039b46715673a9436989cfc49dde04e6bd57e205347478a58214789baf5efdc
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
$ docker pull nats@sha256:f0679b55723570b245b735087116f40b61209f9419a052555911d92ba92db3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f2c459fccd79c9b1768d7235853736817cc95553a4a77e0fcc60d748ded94c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91149e471871c2ede088818330273446a46a28fa17ab6019c347e827f3d88e`  
		Last Modified: Tue, 02 Jun 2026 19:05:14 GMT  
		Size: 7.3 MB (7294356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1780775af23cf70b20cc6730511246e7e72d42ce7d668c73c18b90d48a67a01`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db4d3abeff2b99495264a4eee8c173e4cddac6f2562cf176849969f8bfeb6f5`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:433ad5e1cd4d4638ba012ef6d511de6ada4d25848d45a59a419c4e8c8f212504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5457ab88186ec095f87e6383750982f83261069aa7d81add3cf4e931d5bd8b8d`

```dockerfile
```

-	Layers:
	-	`sha256:97908037527cfc59a216bfe62a51d23f134332356fa5e4b7cb247741bdd17194`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:bd43cfbbeacf6edb2b475c63866eb39de3639ff98c7ba4b2e864136daf55afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10542108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb38008b73bdfef49b080f538c56c59c970defde4adf819ce4be46eb115f13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4134644628fbe8c80ca77808206ab4ff2c01c11c3c49f656c7120757e9b9d8`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 7.0 MB (7033752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37f54e57d50f3a9c76dd3ddbf500d95b6c7e85c7c07aa48147c6cdd9defbe4`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f867e1babe5c47998841c28bded391ef496d71feb54b61f4545d87f5a646cba`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:41db50f6cc4d9bfd6ec2c46f419eed60136e695a19f5892004fc8e16f9e4c958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacd6b789756bea2927e2e1131c952cd3ad9c48cb279eb3eb6303fc9ab294d2f`

```dockerfile
```

-	Layers:
	-	`sha256:5e30d67018b50219cf111359b9c01c0f494e08d2b3f8569dcc5fd3c1ee5c1d73`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:ad14dda00ccf242342a93cc85db34a56bb25d3e296ecdace5147c1966b5b3b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10247947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec25b1ccdde1f720071b74505ffdf00e039ab69a2fd75f71d020027bd2c0a7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9df1ef32961e68a3939cd854cdbbf23eadb85878e7a2924c8e8b55ed686db`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 7.0 MB (7021143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3a2252f7f49291e414a088e7d5d7d5b1ed30e39570d7aaaddefe72ad7ec45`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f706a5b129742a751a90778c239816e2f65e8da796265eea974d0684885fe`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:37cb5f4f11c03e9635452373f12b4933fd563eb9d9b579fa4d81074c310b783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8831237e5b1eb42138b1b533eac461905370c52864faa74ad64aa64ee6929ea9`

```dockerfile
```

-	Layers:
	-	`sha256:8b0c0c197e4c11be4cea42928534aba725c08e8453c25ec9bc3b3d17f826cd06`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:611c3dbd05ff98e9f9f562b4ecc89822c2b0367847d932a4932c1ed966bc9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10792301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a4b2095da890cb3d5ca21aa5d61d37c4ca5fd0cde2e2037c3552e8b346140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967f1732be2cea3277e46b05ada1d6dc6dc0c9d759046c2618be783fee259b3`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.6 MB (6649438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729dba32d18e040f985909e362d966b7bdd5bb98293da5c5b092b2db7b1ad6c`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd385b5d9562cba05d122624afc347bf04e331b1039428b62bfa34329ae6fc`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83650089aa5af8edeacd31f9575f51c4865f49f4658f5e4783da1893cbd73665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ea3db6409708bdb914b77d4ccc8d0aeb240671d5247e30d10994a292bed6a`

```dockerfile
```

-	Layers:
	-	`sha256:0e0bb2fa8f0c108b876e46f52d13f30f36c80387b8275abc10d23d94c3c159f2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:03cac3b8dd8dfa41d75112c2ae5b94fec0af6f5814730e5330012354cf7f0827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447bf89722c6586ace97b811cfa21359201cf2f9713c5e1fef6213a7acc2650e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:09:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:09:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a55d0eaca97f0390033ffa8d9134bc7a0079525bf40c87025873115014fab03`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.7 MB (6712091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e475251befa77978ceea2dd486692601fdf578dc6cf93f6f34db105424faa429`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd101bdee386ea23d9751c471412ed9d61e7b3bb95fa9c4c09dcf11b393862b0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:878c6cd3e6ca2b63e8e7c9012c4a51e6f964a8e1f17a510c05f7000a2ee3c3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b43654f9754af02840c24097bead60f9bda1a56f0d0331c1cdb97492d058d1d`

```dockerfile
```

-	Layers:
	-	`sha256:277a9558e629945d4f89fbecb1fece232afa05343087d445fab71410b96445a5`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:841b7ad0b071063eab531f42992071e88a18027757dc688943e9b6be84f30b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10758432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8d5496bf4f8dc7bc2e68a44462403d27657a08420f26e155ef56c4b875cd1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9e1c021cb6668546fbd3caeb13392781503722c1117940072299d8a401f78`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 7.1 MB (7103589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7207403655133bcd046b16235270ff4b177f4e43d2903766cfb7a82d247e914`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107699ca626db0b1dca70dd8b094467bb9da6bad2e7b07a3e817e656f0528716`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d93ecdc48d72d516e5b6b434a8f943f9a0a356ea2e81c18a79d46fa97dac3cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e2b39405c34660d72439c24d374ad63c17ff6072b7967c16a05e3d681f075e`

```dockerfile
```

-	Layers:
	-	`sha256:73ea22818eaf35e7185adc8c19baf720eec4e2f32f9e2f8eefc0ae10f85ea059`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:d6519b375b05bc720d5a10240e23ecec1fcb559f2d48b9d13fe6408331a52e7a
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
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
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
$ docker pull nats@sha256:d6519b375b05bc720d5a10240e23ecec1fcb559f2d48b9d13fe6408331a52e7a
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
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
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
$ docker pull nats@sha256:71f522d77eb96fe73fcccaca505e246e2406c68fe76498c78f9ce83064cffb9c
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
$ docker pull nats@sha256:2ab08148b4ee24429eebb667e21f80941ce1657f8afa979f10af4f05d91b8292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f0275e3d5bf0a174d1028cfb9d9471a1ccd982804f878e52da3866108aa1f8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88913724d1d8e74f3f1ff6a60b00a7acb8450d4f1888012fc2a1719b0f571279`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.6 MB (6643520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cd67fdee0900fa1ef3862345a62480b27fc2a450a7d0eda5c82bff946cab6`  
		Last Modified: Tue, 09 Jun 2026 18:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:5b402cfa502a3b2d8c31c1c4fc6bd3276940b02322d4c5b7658a0e4cee7a35ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f5a4fa862a018d0d9ba5c3e56399da46ce4aa8e5dbdc872e229aab637a451d`

```dockerfile
```

-	Layers:
	-	`sha256:d0b54ff432fb5083ca7878e58ca4d396e73dba72f176038440a90e5d48050517`  
		Last Modified: Tue, 09 Jun 2026 18:12:33 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:4671c4b21974e9ee77abf49375a0e76797e78b96f3b100b39fdfb136a364401a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c272b02c9e1c0b607d2bc944c19679af6b223d549448d295df5d3a30a441b4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:08:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:08:48 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:08:48 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:08:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:56ed75683f9b5db33f8ad9a299605af0eae8a9ebe1c30ef8e894bea87d5de05d`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.4 MB (6384400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e6eb06c3eafc85d4885514c3a9d4eaeb2bbd393908999e4e1c2cfab855ba12`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:cdbef24ab485faaa912abc481a6a6111586123d3dacd25e94430199ef8927b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053cc83c694a5cfe4650f76daed30bd4ea101f71fc1ead69b6fe3d39f6497f4`

```dockerfile
```

-	Layers:
	-	`sha256:50bceea36393d1b0fea8cac19e67d2f748122f613e976f8d48e8d5e360914291`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:f42ef7fe1a4cb7d4fec579ed9fe2e3732177d98b0c46bc9359c4727c4844a34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c781a0b177c52554f87b8adc28116cad47cac515449e3b0d8fe93124667a2a0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e982c114a13138e2685668359ca9e0582e26abafe5549dac8de6da9ec5a4812`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.4 MB (6374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a62dc33b5ce9228790b002e0f1f443db4eb3c933b74f7fde40672a56a02e631`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:0df3bc19acaa140730a4b021933fd9fa7643dcd678497e981ca04643be7180e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95eb5ef4c403726c81fa2dd926bb831b92f13393dca29987e551f6a940637b58`

```dockerfile
```

-	Layers:
	-	`sha256:b650fc90dc66830f3dc69eee5084e1526a32f36e96c99b03ea9ae1b3a19a5639`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:316df87993501b7d4394c6b1b9dfd4976526a779e280876525025286599ff684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651baae8fed97cb865aefef1560828eab06acca8a268b65ca72f6527265b8347`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dbab1ffdd888ab70dbb64d3905f68ffaad15b074fb768ff177945584a4da2979`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.0 MB (6038038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8045fe26152996b1c25cf1b69933f764bf3664850d2b4be0556bbdc395ba6de2`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:d09c06c30cc3b40485410a0197b49119e223d0447330bbe33e5ef2e490e60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6db17398ff64e2610c75eee6813ea209398c776e29c9b3a4d2c88c74ac6061`

```dockerfile
```

-	Layers:
	-	`sha256:c1ad2a823e70e752b8e707ba2e6f79d061bd6513e9048a5d3ba1b0dcebd8fdb7`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:500376f0032cee55f7b622d44d14ae96c78ce53f784ad0ddef4199174c89eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6101131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f548d07e5f7bc1f81d5bee95f9bd3381ca511a036e8a7936d12d8a2e4d7e69b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:11:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:11:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:11:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:11:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3c8128190e1f74d677c2c6c27f17e58287ea869b0ac83a3ec8d948f9864be4`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.1 MB (6100622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42409a8650a26777b9e5dd74e0df3bd3748139444b14c796f069d3c16de2f127`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:a2067ef8c3e73eb50d26fbfa7596ad1fa0a6f11eee80691723cb2572685ce98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bbed2722880584cc7603d06f5af5f1b4bccc740b2cb624f1a06d10d6698f72`

```dockerfile
```

-	Layers:
	-	`sha256:d734a1f9d3be60b9a5b7b1a162fa81127a103df769ce8ee78bd5c9a088595b9b`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:d45b83fd088c8a12f4b9d20fcacb17b0f2d508bb6dd6fe140622651eb24ad21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4d2b317e4704fab7645f76695aee5985f04c2004740e64e3c9b147824715a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7af0e8a091b6b9b365d51014f398aea3666f8e453d6f97753b7042a611b1ef7`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.5 MB (6491236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce8719bf0358a3223ffb862bd466323c56a5840bbe43d8756f3c7d527c0cfcc`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:791c562ec98ec32eb1e725744aad93054ed5266e94c2d8ff82317b8995f8cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a338d714fbe0106f3a32fe785c578007bbbc750feb73a10baa3cce1e7ad43bc`

```dockerfile
```

-	Layers:
	-	`sha256:66e8efa3e7bdb303fe57fd3586c3ef4b0163d79e3d434683180afca7a23659f7`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 8.7 KB (8668 bytes)  
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
$ docker pull nats@sha256:006a95e54643c0a2a33dfcee4654e9115f7540ebb8804822d3e2d82bf8515f61
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
$ docker pull nats@sha256:667fc3e01c66ffcc81d9c1681cd1c827489c95ab23c56efe86fab2efedc6d894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3632298dbedee01f65820723dab517bd7e943f57e56c92a210da80d0b89c0a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:57:00 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:57:00 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:57:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:57:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235a90c5463fcfa5372a6c8644c6e2fc1ca8ef5cecd250a1a8db1ebe086a0ae0`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 7.1 MB (7099935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44496ffb8caf47b857ae5b00106a10d9ccd7bc34008b2513d8a3041096bc2c10`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79f6b33c409585e418d938e461c9726d28d6e200af2665bb3e6a0f943248e8e`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8746def77d09c6290e97bc340a399547cc38b39008671e769f0f505de1d168a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50ca4d6c44d4b12302b79a3c37ea9b6dcb675a3dd6e5b935606d9597832e210`

```dockerfile
```

-	Layers:
	-	`sha256:c9d69d01e84f0d6e0d85832fcf3c13c47e787aeeef74a5f3a777524026826611`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:e7bd06f699d0ab70225fe3416a5e827b9f1f953aa7f17c72bdd94076b01781c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644c3a7818568b008b0c4bbb017abc3b788ed5a1486a2a200fdbfee0f761214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:56:25 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:56:25 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:56:25 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:56:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:56:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bbf192882921771a72bda287f052d36e5b993914bafeaf34b1d6bff0791dbe`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 6.8 MB (6840587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096ccec94f7cf45a5358598f561ef38dd5d27902ff5edd232e1979ab6b27d1a`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896fb5129d73b813476a3a5eb6c1b85786e02e428291b88c08db1d38d83c5bda`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9370e82d4426e1bd5e5d8f6db3faa70eaf847e56004bfee1e88ea62f49fdb02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb367bf74e1a0f52f3d2a4e29a0f885a90e71aedf9778431aad7054d942adae0`

```dockerfile
```

-	Layers:
	-	`sha256:39cdce52281c49947e6ad0f900534efa551633cc03568f951f05eb5b9e5cbf48`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7c8098f5bf8bd30e7534699f8cbf21be8a9ea0391177d3cd9f0901c0c22dcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10056624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54a68d00c16259ee9fc895f4942e657fde25cc36ee28c612601abd7fc4e4f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:57:11 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:57:11 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:57:11 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:57:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea1af83e27d62e7f43afc13feda520937b84f945826ac0aa32c26a4bb3fdca8`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 6.8 MB (6829824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810cf0f43ded98229f46561594c32d47d795855d81c06e6850efc16842595f21`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c93c2a67d325fe34312213eafdd0acb33a28b3abb65d5b70b2ba6c8a17be1c`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5de365fa26e4aecd403f54976c5fad79f39fe41d8f6cca20b44d4d3c3cb93723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee28da77c9c62323f46a2a8bb862aacc34133bd099ea048108f4c40143bb219`

```dockerfile
```

-	Layers:
	-	`sha256:39fe506bef03d07656e58a3eafb8c434eb88f5084483914866b86d4a1a9b6bc5`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:37ca2a684fea5dc6345bf2ae2500bb02e0f3103b01c7df7f1b9f22a6ece0a26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d31bdd9017bcd6ddecc66ecaf6e2031a6ce7f1724d0883de4829cf59288a51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:56:10 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:56:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:56:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:56:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:56:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bebbcb9868fa8d0cfe7322cd7a719d07093fe6e07142978299bda3a55dcdcd`  
		Last Modified: Tue, 09 Jun 2026 17:56:17 GMT  
		Size: 6.5 MB (6499909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5edf12b37c4400cddc119d5015614f08d0da6869f66b3e98b9e112ee040d83`  
		Last Modified: Tue, 09 Jun 2026 17:56:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d5d999025e759addd4aa9536ed88337eb4650522d24635a76aac01946b2521`  
		Last Modified: Tue, 09 Jun 2026 17:56:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8001fe043b532d74bf09d9c6e17b09bce10171970ba817946b1d284a3628a95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2efc4db87f8aeaab288d0f2e9e7551f003b844fc05c0859a97e6714eefcfc3e`

```dockerfile
```

-	Layers:
	-	`sha256:43b8af40a92a079ea6e76c551c23c97dec02db64efae84144b2bec64ba54801d`  
		Last Modified: Tue, 09 Jun 2026 17:56:17 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:141d12c9ef6e8ad9c2e4a0f2861e6fc0a31167b613e095d0929b58cabe7797de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c6ae88574031752351291d97426f742f8114dbdbebb863cb9f9947919471a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:55:49 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:55:49 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:55:49 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:55:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9802f89779b0668d002d49e3c14c6fe68c68af7035a6f1cd7774fd3d3ba3ccc4`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 6.6 MB (6558686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d16b548fb19914f9ad97d4d4d5d97118a87ab7f3f1cbc2ed405785f08d5aee5`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc01568e65624d5ce3bf2230259e4b78af726ac84c2240c357e10a7ccab7e70`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0c47c7b2dd9effba4858b8b022c440409813f3d098b7a67ff422463a224ee1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5b7655bf0a76bc77c19843b63366f4c75c20e6f2e0bc0da223461e81d47b79`

```dockerfile
```

-	Layers:
	-	`sha256:b92625365acace95de8d47a275ed8f063d86d35e12661da6769c6636813fcc7d`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:875295d3cfd8708bfd6fac260a0e08755ebe295419b661d7b8dc6877702f891a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545afd9d4b531da8c759c31c0301a0a9867bcacf938339afe973eb99b032a72d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:55:08 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:55:08 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:55:08 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:55:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:55:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3d41b6aefa04dfab1d2e59ae78889794f513c31768844ce2406f6dd714e8cd`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 6.9 MB (6949820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a043ea6170b9849386debf4f93270f06819a50f38654128996c172c26eda1b23`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db89bedf06d2bcc7b20402af5213ae0557ca6caef37e2338fd4dc34e1984bf0`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:485f5dc678132a8c267e8eb0a16ff3891231fad5639e58e7cbeab734f5f2c2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f6115342469152fefab2a9cd0349dbc1913384c0a55ce6c96141a0b60e1db0`

```dockerfile
```

-	Layers:
	-	`sha256:0426cbe49dbe1b6affa5e3b3a4d67c3c4e850e497a10ac4565bca74eca731636`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:006a95e54643c0a2a33dfcee4654e9115f7540ebb8804822d3e2d82bf8515f61
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
$ docker pull nats@sha256:667fc3e01c66ffcc81d9c1681cd1c827489c95ab23c56efe86fab2efedc6d894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3632298dbedee01f65820723dab517bd7e943f57e56c92a210da80d0b89c0a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:57:00 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:57:00 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:57:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:57:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235a90c5463fcfa5372a6c8644c6e2fc1ca8ef5cecd250a1a8db1ebe086a0ae0`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 7.1 MB (7099935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44496ffb8caf47b857ae5b00106a10d9ccd7bc34008b2513d8a3041096bc2c10`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79f6b33c409585e418d938e461c9726d28d6e200af2665bb3e6a0f943248e8e`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8746def77d09c6290e97bc340a399547cc38b39008671e769f0f505de1d168a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50ca4d6c44d4b12302b79a3c37ea9b6dcb675a3dd6e5b935606d9597832e210`

```dockerfile
```

-	Layers:
	-	`sha256:c9d69d01e84f0d6e0d85832fcf3c13c47e787aeeef74a5f3a777524026826611`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:e7bd06f699d0ab70225fe3416a5e827b9f1f953aa7f17c72bdd94076b01781c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644c3a7818568b008b0c4bbb017abc3b788ed5a1486a2a200fdbfee0f761214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:56:25 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:56:25 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:56:25 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:56:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:56:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bbf192882921771a72bda287f052d36e5b993914bafeaf34b1d6bff0791dbe`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 6.8 MB (6840587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096ccec94f7cf45a5358598f561ef38dd5d27902ff5edd232e1979ab6b27d1a`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896fb5129d73b813476a3a5eb6c1b85786e02e428291b88c08db1d38d83c5bda`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9370e82d4426e1bd5e5d8f6db3faa70eaf847e56004bfee1e88ea62f49fdb02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb367bf74e1a0f52f3d2a4e29a0f885a90e71aedf9778431aad7054d942adae0`

```dockerfile
```

-	Layers:
	-	`sha256:39cdce52281c49947e6ad0f900534efa551633cc03568f951f05eb5b9e5cbf48`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7c8098f5bf8bd30e7534699f8cbf21be8a9ea0391177d3cd9f0901c0c22dcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10056624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54a68d00c16259ee9fc895f4942e657fde25cc36ee28c612601abd7fc4e4f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:57:11 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:57:11 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:57:11 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:57:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea1af83e27d62e7f43afc13feda520937b84f945826ac0aa32c26a4bb3fdca8`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 6.8 MB (6829824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810cf0f43ded98229f46561594c32d47d795855d81c06e6850efc16842595f21`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c93c2a67d325fe34312213eafdd0acb33a28b3abb65d5b70b2ba6c8a17be1c`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5de365fa26e4aecd403f54976c5fad79f39fe41d8f6cca20b44d4d3c3cb93723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee28da77c9c62323f46a2a8bb862aacc34133bd099ea048108f4c40143bb219`

```dockerfile
```

-	Layers:
	-	`sha256:39fe506bef03d07656e58a3eafb8c434eb88f5084483914866b86d4a1a9b6bc5`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:37ca2a684fea5dc6345bf2ae2500bb02e0f3103b01c7df7f1b9f22a6ece0a26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d31bdd9017bcd6ddecc66ecaf6e2031a6ce7f1724d0883de4829cf59288a51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:56:10 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:56:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:56:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:56:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:56:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bebbcb9868fa8d0cfe7322cd7a719d07093fe6e07142978299bda3a55dcdcd`  
		Last Modified: Tue, 09 Jun 2026 17:56:17 GMT  
		Size: 6.5 MB (6499909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5edf12b37c4400cddc119d5015614f08d0da6869f66b3e98b9e112ee040d83`  
		Last Modified: Tue, 09 Jun 2026 17:56:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d5d999025e759addd4aa9536ed88337eb4650522d24635a76aac01946b2521`  
		Last Modified: Tue, 09 Jun 2026 17:56:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8001fe043b532d74bf09d9c6e17b09bce10171970ba817946b1d284a3628a95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2efc4db87f8aeaab288d0f2e9e7551f003b844fc05c0859a97e6714eefcfc3e`

```dockerfile
```

-	Layers:
	-	`sha256:43b8af40a92a079ea6e76c551c23c97dec02db64efae84144b2bec64ba54801d`  
		Last Modified: Tue, 09 Jun 2026 17:56:17 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:141d12c9ef6e8ad9c2e4a0f2861e6fc0a31167b613e095d0929b58cabe7797de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c6ae88574031752351291d97426f742f8114dbdbebb863cb9f9947919471a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:55:49 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:55:49 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:55:49 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:55:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9802f89779b0668d002d49e3c14c6fe68c68af7035a6f1cd7774fd3d3ba3ccc4`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 6.6 MB (6558686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d16b548fb19914f9ad97d4d4d5d97118a87ab7f3f1cbc2ed405785f08d5aee5`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc01568e65624d5ce3bf2230259e4b78af726ac84c2240c357e10a7ccab7e70`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:0c47c7b2dd9effba4858b8b022c440409813f3d098b7a67ff422463a224ee1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5b7655bf0a76bc77c19843b63366f4c75c20e6f2e0bc0da223461e81d47b79`

```dockerfile
```

-	Layers:
	-	`sha256:b92625365acace95de8d47a275ed8f063d86d35e12661da6769c6636813fcc7d`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:875295d3cfd8708bfd6fac260a0e08755ebe295419b661d7b8dc6877702f891a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545afd9d4b531da8c759c31c0301a0a9867bcacf938339afe973eb99b032a72d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:55:08 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:55:08 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:55:08 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:55:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:55:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3d41b6aefa04dfab1d2e59ae78889794f513c31768844ce2406f6dd714e8cd`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 6.9 MB (6949820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a043ea6170b9849386debf4f93270f06819a50f38654128996c172c26eda1b23`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db89bedf06d2bcc7b20402af5213ae0557ca6caef37e2338fd4dc34e1984bf0`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:485f5dc678132a8c267e8eb0a16ff3891231fad5639e58e7cbeab734f5f2c2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f6115342469152fefab2a9cd0349dbc1913384c0a55ce6c96141a0b60e1db0`

```dockerfile
```

-	Layers:
	-	`sha256:0426cbe49dbe1b6affa5e3b3a4d67c3c4e850e497a10ac4565bca74eca731636`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:a5e6ee541d62c5962207eb78d5127eb6cbdb49a9a4095bf08ba0b659ee3b8309
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
$ docker pull nats@sha256:2ab08148b4ee24429eebb667e21f80941ce1657f8afa979f10af4f05d91b8292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f0275e3d5bf0a174d1028cfb9d9471a1ccd982804f878e52da3866108aa1f8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88913724d1d8e74f3f1ff6a60b00a7acb8450d4f1888012fc2a1719b0f571279`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.6 MB (6643520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cd67fdee0900fa1ef3862345a62480b27fc2a450a7d0eda5c82bff946cab6`  
		Last Modified: Tue, 09 Jun 2026 18:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5b402cfa502a3b2d8c31c1c4fc6bd3276940b02322d4c5b7658a0e4cee7a35ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f5a4fa862a018d0d9ba5c3e56399da46ce4aa8e5dbdc872e229aab637a451d`

```dockerfile
```

-	Layers:
	-	`sha256:d0b54ff432fb5083ca7878e58ca4d396e73dba72f176038440a90e5d48050517`  
		Last Modified: Tue, 09 Jun 2026 18:12:33 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4671c4b21974e9ee77abf49375a0e76797e78b96f3b100b39fdfb136a364401a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c272b02c9e1c0b607d2bc944c19679af6b223d549448d295df5d3a30a441b4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:08:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:08:48 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:08:48 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:08:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:56ed75683f9b5db33f8ad9a299605af0eae8a9ebe1c30ef8e894bea87d5de05d`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.4 MB (6384400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e6eb06c3eafc85d4885514c3a9d4eaeb2bbd393908999e4e1c2cfab855ba12`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:cdbef24ab485faaa912abc481a6a6111586123d3dacd25e94430199ef8927b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053cc83c694a5cfe4650f76daed30bd4ea101f71fc1ead69b6fe3d39f6497f4`

```dockerfile
```

-	Layers:
	-	`sha256:50bceea36393d1b0fea8cac19e67d2f748122f613e976f8d48e8d5e360914291`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f42ef7fe1a4cb7d4fec579ed9fe2e3732177d98b0c46bc9359c4727c4844a34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c781a0b177c52554f87b8adc28116cad47cac515449e3b0d8fe93124667a2a0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e982c114a13138e2685668359ca9e0582e26abafe5549dac8de6da9ec5a4812`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.4 MB (6374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a62dc33b5ce9228790b002e0f1f443db4eb3c933b74f7fde40672a56a02e631`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0df3bc19acaa140730a4b021933fd9fa7643dcd678497e981ca04643be7180e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95eb5ef4c403726c81fa2dd926bb831b92f13393dca29987e551f6a940637b58`

```dockerfile
```

-	Layers:
	-	`sha256:b650fc90dc66830f3dc69eee5084e1526a32f36e96c99b03ea9ae1b3a19a5639`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:316df87993501b7d4394c6b1b9dfd4976526a779e280876525025286599ff684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651baae8fed97cb865aefef1560828eab06acca8a268b65ca72f6527265b8347`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dbab1ffdd888ab70dbb64d3905f68ffaad15b074fb768ff177945584a4da2979`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.0 MB (6038038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8045fe26152996b1c25cf1b69933f764bf3664850d2b4be0556bbdc395ba6de2`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d09c06c30cc3b40485410a0197b49119e223d0447330bbe33e5ef2e490e60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6db17398ff64e2610c75eee6813ea209398c776e29c9b3a4d2c88c74ac6061`

```dockerfile
```

-	Layers:
	-	`sha256:c1ad2a823e70e752b8e707ba2e6f79d061bd6513e9048a5d3ba1b0dcebd8fdb7`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:500376f0032cee55f7b622d44d14ae96c78ce53f784ad0ddef4199174c89eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6101131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f548d07e5f7bc1f81d5bee95f9bd3381ca511a036e8a7936d12d8a2e4d7e69b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:11:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:11:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:11:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:11:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3c8128190e1f74d677c2c6c27f17e58287ea869b0ac83a3ec8d948f9864be4`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.1 MB (6100622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42409a8650a26777b9e5dd74e0df3bd3748139444b14c796f069d3c16de2f127`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a2067ef8c3e73eb50d26fbfa7596ad1fa0a6f11eee80691723cb2572685ce98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bbed2722880584cc7603d06f5af5f1b4bccc740b2cb624f1a06d10d6698f72`

```dockerfile
```

-	Layers:
	-	`sha256:d734a1f9d3be60b9a5b7b1a162fa81127a103df769ce8ee78bd5c9a088595b9b`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:d45b83fd088c8a12f4b9d20fcacb17b0f2d508bb6dd6fe140622651eb24ad21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4d2b317e4704fab7645f76695aee5985f04c2004740e64e3c9b147824715a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7af0e8a091b6b9b365d51014f398aea3666f8e453d6f97753b7042a611b1ef7`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.5 MB (6491236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce8719bf0358a3223ffb862bd466323c56a5840bbe43d8756f3c7d527c0cfcc`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:791c562ec98ec32eb1e725744aad93054ed5266e94c2d8ff82317b8995f8cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a338d714fbe0106f3a32fe785c578007bbbc750feb73a10baa3cce1e7ad43bc`

```dockerfile
```

-	Layers:
	-	`sha256:66e8efa3e7bdb303fe57fd3586c3ef4b0163d79e3d434683180afca7a23659f7`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 8.7 KB (8668 bytes)  
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
$ docker pull nats@sha256:a5e6ee541d62c5962207eb78d5127eb6cbdb49a9a4095bf08ba0b659ee3b8309
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
$ docker pull nats@sha256:2ab08148b4ee24429eebb667e21f80941ce1657f8afa979f10af4f05d91b8292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f0275e3d5bf0a174d1028cfb9d9471a1ccd982804f878e52da3866108aa1f8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88913724d1d8e74f3f1ff6a60b00a7acb8450d4f1888012fc2a1719b0f571279`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.6 MB (6643520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cd67fdee0900fa1ef3862345a62480b27fc2a450a7d0eda5c82bff946cab6`  
		Last Modified: Tue, 09 Jun 2026 18:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5b402cfa502a3b2d8c31c1c4fc6bd3276940b02322d4c5b7658a0e4cee7a35ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f5a4fa862a018d0d9ba5c3e56399da46ce4aa8e5dbdc872e229aab637a451d`

```dockerfile
```

-	Layers:
	-	`sha256:d0b54ff432fb5083ca7878e58ca4d396e73dba72f176038440a90e5d48050517`  
		Last Modified: Tue, 09 Jun 2026 18:12:33 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4671c4b21974e9ee77abf49375a0e76797e78b96f3b100b39fdfb136a364401a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c272b02c9e1c0b607d2bc944c19679af6b223d549448d295df5d3a30a441b4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:08:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:08:48 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:08:48 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:08:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:56ed75683f9b5db33f8ad9a299605af0eae8a9ebe1c30ef8e894bea87d5de05d`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.4 MB (6384400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e6eb06c3eafc85d4885514c3a9d4eaeb2bbd393908999e4e1c2cfab855ba12`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cdbef24ab485faaa912abc481a6a6111586123d3dacd25e94430199ef8927b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053cc83c694a5cfe4650f76daed30bd4ea101f71fc1ead69b6fe3d39f6497f4`

```dockerfile
```

-	Layers:
	-	`sha256:50bceea36393d1b0fea8cac19e67d2f748122f613e976f8d48e8d5e360914291`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f42ef7fe1a4cb7d4fec579ed9fe2e3732177d98b0c46bc9359c4727c4844a34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c781a0b177c52554f87b8adc28116cad47cac515449e3b0d8fe93124667a2a0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e982c114a13138e2685668359ca9e0582e26abafe5549dac8de6da9ec5a4812`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.4 MB (6374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a62dc33b5ce9228790b002e0f1f443db4eb3c933b74f7fde40672a56a02e631`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0df3bc19acaa140730a4b021933fd9fa7643dcd678497e981ca04643be7180e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95eb5ef4c403726c81fa2dd926bb831b92f13393dca29987e551f6a940637b58`

```dockerfile
```

-	Layers:
	-	`sha256:b650fc90dc66830f3dc69eee5084e1526a32f36e96c99b03ea9ae1b3a19a5639`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:316df87993501b7d4394c6b1b9dfd4976526a779e280876525025286599ff684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651baae8fed97cb865aefef1560828eab06acca8a268b65ca72f6527265b8347`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dbab1ffdd888ab70dbb64d3905f68ffaad15b074fb768ff177945584a4da2979`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.0 MB (6038038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8045fe26152996b1c25cf1b69933f764bf3664850d2b4be0556bbdc395ba6de2`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d09c06c30cc3b40485410a0197b49119e223d0447330bbe33e5ef2e490e60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6db17398ff64e2610c75eee6813ea209398c776e29c9b3a4d2c88c74ac6061`

```dockerfile
```

-	Layers:
	-	`sha256:c1ad2a823e70e752b8e707ba2e6f79d061bd6513e9048a5d3ba1b0dcebd8fdb7`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:500376f0032cee55f7b622d44d14ae96c78ce53f784ad0ddef4199174c89eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6101131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f548d07e5f7bc1f81d5bee95f9bd3381ca511a036e8a7936d12d8a2e4d7e69b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:11:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:11:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:11:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:11:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3c8128190e1f74d677c2c6c27f17e58287ea869b0ac83a3ec8d948f9864be4`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.1 MB (6100622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42409a8650a26777b9e5dd74e0df3bd3748139444b14c796f069d3c16de2f127`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a2067ef8c3e73eb50d26fbfa7596ad1fa0a6f11eee80691723cb2572685ce98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bbed2722880584cc7603d06f5af5f1b4bccc740b2cb624f1a06d10d6698f72`

```dockerfile
```

-	Layers:
	-	`sha256:d734a1f9d3be60b9a5b7b1a162fa81127a103df769ce8ee78bd5c9a088595b9b`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d45b83fd088c8a12f4b9d20fcacb17b0f2d508bb6dd6fe140622651eb24ad21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4d2b317e4704fab7645f76695aee5985f04c2004740e64e3c9b147824715a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7af0e8a091b6b9b365d51014f398aea3666f8e453d6f97753b7042a611b1ef7`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.5 MB (6491236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce8719bf0358a3223ffb862bd466323c56a5840bbe43d8756f3c7d527c0cfcc`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:791c562ec98ec32eb1e725744aad93054ed5266e94c2d8ff82317b8995f8cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a338d714fbe0106f3a32fe785c578007bbbc750feb73a10baa3cce1e7ad43bc`

```dockerfile
```

-	Layers:
	-	`sha256:66e8efa3e7bdb303fe57fd3586c3ef4b0163d79e3d434683180afca7a23659f7`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 8.7 KB (8668 bytes)  
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

## `nats:2.12.11`

```console
$ docker pull nats@sha256:71f522d77eb96fe73fcccaca505e246e2406c68fe76498c78f9ce83064cffb9c
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

### `nats:2.12.11` - linux; amd64

```console
$ docker pull nats@sha256:2ab08148b4ee24429eebb667e21f80941ce1657f8afa979f10af4f05d91b8292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f0275e3d5bf0a174d1028cfb9d9471a1ccd982804f878e52da3866108aa1f8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88913724d1d8e74f3f1ff6a60b00a7acb8450d4f1888012fc2a1719b0f571279`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.6 MB (6643520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cd67fdee0900fa1ef3862345a62480b27fc2a450a7d0eda5c82bff946cab6`  
		Last Modified: Tue, 09 Jun 2026 18:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11` - unknown; unknown

```console
$ docker pull nats@sha256:5b402cfa502a3b2d8c31c1c4fc6bd3276940b02322d4c5b7658a0e4cee7a35ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f5a4fa862a018d0d9ba5c3e56399da46ce4aa8e5dbdc872e229aab637a451d`

```dockerfile
```

-	Layers:
	-	`sha256:d0b54ff432fb5083ca7878e58ca4d396e73dba72f176038440a90e5d48050517`  
		Last Modified: Tue, 09 Jun 2026 18:12:33 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:4671c4b21974e9ee77abf49375a0e76797e78b96f3b100b39fdfb136a364401a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c272b02c9e1c0b607d2bc944c19679af6b223d549448d295df5d3a30a441b4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:08:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:08:48 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:08:48 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:08:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:56ed75683f9b5db33f8ad9a299605af0eae8a9ebe1c30ef8e894bea87d5de05d`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.4 MB (6384400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e6eb06c3eafc85d4885514c3a9d4eaeb2bbd393908999e4e1c2cfab855ba12`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11` - unknown; unknown

```console
$ docker pull nats@sha256:cdbef24ab485faaa912abc481a6a6111586123d3dacd25e94430199ef8927b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053cc83c694a5cfe4650f76daed30bd4ea101f71fc1ead69b6fe3d39f6497f4`

```dockerfile
```

-	Layers:
	-	`sha256:50bceea36393d1b0fea8cac19e67d2f748122f613e976f8d48e8d5e360914291`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:f42ef7fe1a4cb7d4fec579ed9fe2e3732177d98b0c46bc9359c4727c4844a34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c781a0b177c52554f87b8adc28116cad47cac515449e3b0d8fe93124667a2a0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e982c114a13138e2685668359ca9e0582e26abafe5549dac8de6da9ec5a4812`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.4 MB (6374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a62dc33b5ce9228790b002e0f1f443db4eb3c933b74f7fde40672a56a02e631`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11` - unknown; unknown

```console
$ docker pull nats@sha256:0df3bc19acaa140730a4b021933fd9fa7643dcd678497e981ca04643be7180e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95eb5ef4c403726c81fa2dd926bb831b92f13393dca29987e551f6a940637b58`

```dockerfile
```

-	Layers:
	-	`sha256:b650fc90dc66830f3dc69eee5084e1526a32f36e96c99b03ea9ae1b3a19a5639`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:316df87993501b7d4394c6b1b9dfd4976526a779e280876525025286599ff684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651baae8fed97cb865aefef1560828eab06acca8a268b65ca72f6527265b8347`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dbab1ffdd888ab70dbb64d3905f68ffaad15b074fb768ff177945584a4da2979`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.0 MB (6038038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8045fe26152996b1c25cf1b69933f764bf3664850d2b4be0556bbdc395ba6de2`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11` - unknown; unknown

```console
$ docker pull nats@sha256:d09c06c30cc3b40485410a0197b49119e223d0447330bbe33e5ef2e490e60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6db17398ff64e2610c75eee6813ea209398c776e29c9b3a4d2c88c74ac6061`

```dockerfile
```

-	Layers:
	-	`sha256:c1ad2a823e70e752b8e707ba2e6f79d061bd6513e9048a5d3ba1b0dcebd8fdb7`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11` - linux; ppc64le

```console
$ docker pull nats@sha256:500376f0032cee55f7b622d44d14ae96c78ce53f784ad0ddef4199174c89eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6101131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f548d07e5f7bc1f81d5bee95f9bd3381ca511a036e8a7936d12d8a2e4d7e69b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:11:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:11:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:11:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:11:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3c8128190e1f74d677c2c6c27f17e58287ea869b0ac83a3ec8d948f9864be4`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.1 MB (6100622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42409a8650a26777b9e5dd74e0df3bd3748139444b14c796f069d3c16de2f127`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11` - unknown; unknown

```console
$ docker pull nats@sha256:a2067ef8c3e73eb50d26fbfa7596ad1fa0a6f11eee80691723cb2572685ce98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bbed2722880584cc7603d06f5af5f1b4bccc740b2cb624f1a06d10d6698f72`

```dockerfile
```

-	Layers:
	-	`sha256:d734a1f9d3be60b9a5b7b1a162fa81127a103df769ce8ee78bd5c9a088595b9b`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11` - linux; s390x

```console
$ docker pull nats@sha256:d45b83fd088c8a12f4b9d20fcacb17b0f2d508bb6dd6fe140622651eb24ad21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4d2b317e4704fab7645f76695aee5985f04c2004740e64e3c9b147824715a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7af0e8a091b6b9b365d51014f398aea3666f8e453d6f97753b7042a611b1ef7`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.5 MB (6491236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce8719bf0358a3223ffb862bd466323c56a5840bbe43d8756f3c7d527c0cfcc`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11` - unknown; unknown

```console
$ docker pull nats@sha256:791c562ec98ec32eb1e725744aad93054ed5266e94c2d8ff82317b8995f8cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a338d714fbe0106f3a32fe785c578007bbbc750feb73a10baa3cce1e7ad43bc`

```dockerfile
```

-	Layers:
	-	`sha256:66e8efa3e7bdb303fe57fd3586c3ef4b0163d79e3d434683180afca7a23659f7`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11` - windows version 10.0.20348.5256; amd64

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

## `nats:2.12.11-alpine`

```console
$ docker pull nats@sha256:006a95e54643c0a2a33dfcee4654e9115f7540ebb8804822d3e2d82bf8515f61
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

### `nats:2.12.11-alpine` - linux; amd64

```console
$ docker pull nats@sha256:667fc3e01c66ffcc81d9c1681cd1c827489c95ab23c56efe86fab2efedc6d894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3632298dbedee01f65820723dab517bd7e943f57e56c92a210da80d0b89c0a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:57:00 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:57:00 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:57:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:57:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235a90c5463fcfa5372a6c8644c6e2fc1ca8ef5cecd250a1a8db1ebe086a0ae0`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 7.1 MB (7099935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44496ffb8caf47b857ae5b00106a10d9ccd7bc34008b2513d8a3041096bc2c10`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79f6b33c409585e418d938e461c9726d28d6e200af2665bb3e6a0f943248e8e`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8746def77d09c6290e97bc340a399547cc38b39008671e769f0f505de1d168a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50ca4d6c44d4b12302b79a3c37ea9b6dcb675a3dd6e5b935606d9597832e210`

```dockerfile
```

-	Layers:
	-	`sha256:c9d69d01e84f0d6e0d85832fcf3c13c47e787aeeef74a5f3a777524026826611`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:e7bd06f699d0ab70225fe3416a5e827b9f1f953aa7f17c72bdd94076b01781c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644c3a7818568b008b0c4bbb017abc3b788ed5a1486a2a200fdbfee0f761214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:56:25 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:56:25 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:56:25 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:56:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:56:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bbf192882921771a72bda287f052d36e5b993914bafeaf34b1d6bff0791dbe`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 6.8 MB (6840587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096ccec94f7cf45a5358598f561ef38dd5d27902ff5edd232e1979ab6b27d1a`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896fb5129d73b813476a3a5eb6c1b85786e02e428291b88c08db1d38d83c5bda`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9370e82d4426e1bd5e5d8f6db3faa70eaf847e56004bfee1e88ea62f49fdb02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb367bf74e1a0f52f3d2a4e29a0f885a90e71aedf9778431aad7054d942adae0`

```dockerfile
```

-	Layers:
	-	`sha256:39cdce52281c49947e6ad0f900534efa551633cc03568f951f05eb5b9e5cbf48`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7c8098f5bf8bd30e7534699f8cbf21be8a9ea0391177d3cd9f0901c0c22dcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10056624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54a68d00c16259ee9fc895f4942e657fde25cc36ee28c612601abd7fc4e4f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:57:11 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:57:11 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:57:11 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:57:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea1af83e27d62e7f43afc13feda520937b84f945826ac0aa32c26a4bb3fdca8`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 6.8 MB (6829824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810cf0f43ded98229f46561594c32d47d795855d81c06e6850efc16842595f21`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c93c2a67d325fe34312213eafdd0acb33a28b3abb65d5b70b2ba6c8a17be1c`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5de365fa26e4aecd403f54976c5fad79f39fe41d8f6cca20b44d4d3c3cb93723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee28da77c9c62323f46a2a8bb862aacc34133bd099ea048108f4c40143bb219`

```dockerfile
```

-	Layers:
	-	`sha256:39fe506bef03d07656e58a3eafb8c434eb88f5084483914866b86d4a1a9b6bc5`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:37ca2a684fea5dc6345bf2ae2500bb02e0f3103b01c7df7f1b9f22a6ece0a26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d31bdd9017bcd6ddecc66ecaf6e2031a6ce7f1724d0883de4829cf59288a51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:56:10 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:56:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:56:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:56:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:56:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bebbcb9868fa8d0cfe7322cd7a719d07093fe6e07142978299bda3a55dcdcd`  
		Last Modified: Tue, 09 Jun 2026 17:56:17 GMT  
		Size: 6.5 MB (6499909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5edf12b37c4400cddc119d5015614f08d0da6869f66b3e98b9e112ee040d83`  
		Last Modified: Tue, 09 Jun 2026 17:56:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d5d999025e759addd4aa9536ed88337eb4650522d24635a76aac01946b2521`  
		Last Modified: Tue, 09 Jun 2026 17:56:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8001fe043b532d74bf09d9c6e17b09bce10171970ba817946b1d284a3628a95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2efc4db87f8aeaab288d0f2e9e7551f003b844fc05c0859a97e6714eefcfc3e`

```dockerfile
```

-	Layers:
	-	`sha256:43b8af40a92a079ea6e76c551c23c97dec02db64efae84144b2bec64ba54801d`  
		Last Modified: Tue, 09 Jun 2026 17:56:17 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:141d12c9ef6e8ad9c2e4a0f2861e6fc0a31167b613e095d0929b58cabe7797de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c6ae88574031752351291d97426f742f8114dbdbebb863cb9f9947919471a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:55:49 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:55:49 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:55:49 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:55:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9802f89779b0668d002d49e3c14c6fe68c68af7035a6f1cd7774fd3d3ba3ccc4`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 6.6 MB (6558686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d16b548fb19914f9ad97d4d4d5d97118a87ab7f3f1cbc2ed405785f08d5aee5`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc01568e65624d5ce3bf2230259e4b78af726ac84c2240c357e10a7ccab7e70`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:0c47c7b2dd9effba4858b8b022c440409813f3d098b7a67ff422463a224ee1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5b7655bf0a76bc77c19843b63366f4c75c20e6f2e0bc0da223461e81d47b79`

```dockerfile
```

-	Layers:
	-	`sha256:b92625365acace95de8d47a275ed8f063d86d35e12661da6769c6636813fcc7d`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:875295d3cfd8708bfd6fac260a0e08755ebe295419b661d7b8dc6877702f891a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545afd9d4b531da8c759c31c0301a0a9867bcacf938339afe973eb99b032a72d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:55:08 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:55:08 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:55:08 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:55:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:55:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3d41b6aefa04dfab1d2e59ae78889794f513c31768844ce2406f6dd714e8cd`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 6.9 MB (6949820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a043ea6170b9849386debf4f93270f06819a50f38654128996c172c26eda1b23`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db89bedf06d2bcc7b20402af5213ae0557ca6caef37e2338fd4dc34e1984bf0`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:485f5dc678132a8c267e8eb0a16ff3891231fad5639e58e7cbeab734f5f2c2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f6115342469152fefab2a9cd0349dbc1913384c0a55ce6c96141a0b60e1db0`

```dockerfile
```

-	Layers:
	-	`sha256:0426cbe49dbe1b6affa5e3b3a4d67c3c4e850e497a10ac4565bca74eca731636`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.11-alpine3.22`

```console
$ docker pull nats@sha256:006a95e54643c0a2a33dfcee4654e9115f7540ebb8804822d3e2d82bf8515f61
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

### `nats:2.12.11-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:667fc3e01c66ffcc81d9c1681cd1c827489c95ab23c56efe86fab2efedc6d894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10909095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3632298dbedee01f65820723dab517bd7e943f57e56c92a210da80d0b89c0a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:57:00 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:57:00 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:57:00 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:57:00 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:57:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235a90c5463fcfa5372a6c8644c6e2fc1ca8ef5cecd250a1a8db1ebe086a0ae0`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 7.1 MB (7099935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44496ffb8caf47b857ae5b00106a10d9ccd7bc34008b2513d8a3041096bc2c10`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79f6b33c409585e418d938e461c9726d28d6e200af2665bb3e6a0f943248e8e`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8746def77d09c6290e97bc340a399547cc38b39008671e769f0f505de1d168a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50ca4d6c44d4b12302b79a3c37ea9b6dcb675a3dd6e5b935606d9597832e210`

```dockerfile
```

-	Layers:
	-	`sha256:c9d69d01e84f0d6e0d85832fcf3c13c47e787aeeef74a5f3a777524026826611`  
		Last Modified: Tue, 09 Jun 2026 17:57:05 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:e7bd06f699d0ab70225fe3416a5e827b9f1f953aa7f17c72bdd94076b01781c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644c3a7818568b008b0c4bbb017abc3b788ed5a1486a2a200fdbfee0f761214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:56:25 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:56:25 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:56:25 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:56:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:56:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:56:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bbf192882921771a72bda287f052d36e5b993914bafeaf34b1d6bff0791dbe`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 6.8 MB (6840587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1096ccec94f7cf45a5358598f561ef38dd5d27902ff5edd232e1979ab6b27d1a`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896fb5129d73b813476a3a5eb6c1b85786e02e428291b88c08db1d38d83c5bda`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9370e82d4426e1bd5e5d8f6db3faa70eaf847e56004bfee1e88ea62f49fdb02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb367bf74e1a0f52f3d2a4e29a0f885a90e71aedf9778431aad7054d942adae0`

```dockerfile
```

-	Layers:
	-	`sha256:39cdce52281c49947e6ad0f900534efa551633cc03568f951f05eb5b9e5cbf48`  
		Last Modified: Tue, 09 Jun 2026 17:56:29 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:e7c8098f5bf8bd30e7534699f8cbf21be8a9ea0391177d3cd9f0901c0c22dcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10056624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54a68d00c16259ee9fc895f4942e657fde25cc36ee28c612601abd7fc4e4f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:57:11 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:57:11 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:57:11 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:57:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:57:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea1af83e27d62e7f43afc13feda520937b84f945826ac0aa32c26a4bb3fdca8`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 6.8 MB (6829824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810cf0f43ded98229f46561594c32d47d795855d81c06e6850efc16842595f21`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c93c2a67d325fe34312213eafdd0acb33a28b3abb65d5b70b2ba6c8a17be1c`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5de365fa26e4aecd403f54976c5fad79f39fe41d8f6cca20b44d4d3c3cb93723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee28da77c9c62323f46a2a8bb862aacc34133bd099ea048108f4c40143bb219`

```dockerfile
```

-	Layers:
	-	`sha256:39fe506bef03d07656e58a3eafb8c434eb88f5084483914866b86d4a1a9b6bc5`  
		Last Modified: Tue, 09 Jun 2026 17:57:15 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:37ca2a684fea5dc6345bf2ae2500bb02e0f3103b01c7df7f1b9f22a6ece0a26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d31bdd9017bcd6ddecc66ecaf6e2031a6ce7f1724d0883de4829cf59288a51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:56:10 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:56:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:56:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:56:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:56:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:56:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bebbcb9868fa8d0cfe7322cd7a719d07093fe6e07142978299bda3a55dcdcd`  
		Last Modified: Tue, 09 Jun 2026 17:56:17 GMT  
		Size: 6.5 MB (6499909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5edf12b37c4400cddc119d5015614f08d0da6869f66b3e98b9e112ee040d83`  
		Last Modified: Tue, 09 Jun 2026 17:56:16 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d5d999025e759addd4aa9536ed88337eb4650522d24635a76aac01946b2521`  
		Last Modified: Tue, 09 Jun 2026 17:56:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8001fe043b532d74bf09d9c6e17b09bce10171970ba817946b1d284a3628a95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2efc4db87f8aeaab288d0f2e9e7551f003b844fc05c0859a97e6714eefcfc3e`

```dockerfile
```

-	Layers:
	-	`sha256:43b8af40a92a079ea6e76c551c23c97dec02db64efae84144b2bec64ba54801d`  
		Last Modified: Tue, 09 Jun 2026 17:56:17 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:141d12c9ef6e8ad9c2e4a0f2861e6fc0a31167b613e095d0929b58cabe7797de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c6ae88574031752351291d97426f742f8114dbdbebb863cb9f9947919471a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:55:49 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:55:49 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:55:49 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:55:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:55:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9802f89779b0668d002d49e3c14c6fe68c68af7035a6f1cd7774fd3d3ba3ccc4`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 6.6 MB (6558686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d16b548fb19914f9ad97d4d4d5d97118a87ab7f3f1cbc2ed405785f08d5aee5`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc01568e65624d5ce3bf2230259e4b78af726ac84c2240c357e10a7ccab7e70`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:0c47c7b2dd9effba4858b8b022c440409813f3d098b7a67ff422463a224ee1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5b7655bf0a76bc77c19843b63366f4c75c20e6f2e0bc0da223461e81d47b79`

```dockerfile
```

-	Layers:
	-	`sha256:b92625365acace95de8d47a275ed8f063d86d35e12661da6769c6636813fcc7d`  
		Last Modified: Tue, 09 Jun 2026 17:55:56 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:875295d3cfd8708bfd6fac260a0e08755ebe295419b661d7b8dc6877702f891a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545afd9d4b531da8c759c31c0301a0a9867bcacf938339afe973eb99b032a72d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 17:55:08 GMT
ENV NATS_SERVER=2.12.11
# Tue, 09 Jun 2026 17:55:08 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.11
# Tue, 09 Jun 2026 17:55:08 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='5789a9319a2ff637a24d5b11513c901515e06d7b35349651e812e5f947a04852' ;;     armhf) natsArch='arm6'; sha256='a0ed106cdf08e9e46b290f59364424294e97aa966444e1668369c8d9c08bf926' ;;     armv7) natsArch='arm7'; sha256='88a9f40d3883bac61cb078fc73559e2c59edae863d34fd8bee8cf4e26610afca' ;;     x86_64) natsArch='amd64'; sha256='5921d9d18c404e9565170d4fe29478dc11c164efdb3933f63001650f7c01e26f' ;;     x86) natsArch='386'; sha256='81efd2c17bccddb8613abd0704bfd13820fee0a589ca80db9ba0ebe7ad268ecc' ;;     s390x) natsArch='s390x'; sha256='99dcfb555ccf1a226ba74b62ccb3c3250e7c2fe663da12b04a5bc9b588052bf6' ;;     ppc64le) natsArch='ppc64le'; sha256='890f55a6aee3a8019a4fd2d59528b563ebf4a3e1e9964e85815f0f700f9bc8b9' ;;     loong64) natsArch='loong64'; sha256='1df8dc0903a3c700a80c85ea8ced8c15e1e6ec72a44af6f35126c1f65a95c409' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 09 Jun 2026 17:55:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 17:55:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 17:55:08 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3d41b6aefa04dfab1d2e59ae78889794f513c31768844ce2406f6dd714e8cd`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 6.9 MB (6949820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a043ea6170b9849386debf4f93270f06819a50f38654128996c172c26eda1b23`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db89bedf06d2bcc7b20402af5213ae0557ca6caef37e2338fd4dc34e1984bf0`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:485f5dc678132a8c267e8eb0a16ff3891231fad5639e58e7cbeab734f5f2c2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f6115342469152fefab2a9cd0349dbc1913384c0a55ce6c96141a0b60e1db0`

```dockerfile
```

-	Layers:
	-	`sha256:0426cbe49dbe1b6affa5e3b3a4d67c3c4e850e497a10ac4565bca74eca731636`  
		Last Modified: Tue, 09 Jun 2026 17:55:16 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.11-linux`

```console
$ docker pull nats@sha256:a5e6ee541d62c5962207eb78d5127eb6cbdb49a9a4095bf08ba0b659ee3b8309
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

### `nats:2.12.11-linux` - linux; amd64

```console
$ docker pull nats@sha256:2ab08148b4ee24429eebb667e21f80941ce1657f8afa979f10af4f05d91b8292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f0275e3d5bf0a174d1028cfb9d9471a1ccd982804f878e52da3866108aa1f8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88913724d1d8e74f3f1ff6a60b00a7acb8450d4f1888012fc2a1719b0f571279`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.6 MB (6643520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cd67fdee0900fa1ef3862345a62480b27fc2a450a7d0eda5c82bff946cab6`  
		Last Modified: Tue, 09 Jun 2026 18:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5b402cfa502a3b2d8c31c1c4fc6bd3276940b02322d4c5b7658a0e4cee7a35ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f5a4fa862a018d0d9ba5c3e56399da46ce4aa8e5dbdc872e229aab637a451d`

```dockerfile
```

-	Layers:
	-	`sha256:d0b54ff432fb5083ca7878e58ca4d396e73dba72f176038440a90e5d48050517`  
		Last Modified: Tue, 09 Jun 2026 18:12:33 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:4671c4b21974e9ee77abf49375a0e76797e78b96f3b100b39fdfb136a364401a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c272b02c9e1c0b607d2bc944c19679af6b223d549448d295df5d3a30a441b4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:08:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:08:48 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:08:48 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:08:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:56ed75683f9b5db33f8ad9a299605af0eae8a9ebe1c30ef8e894bea87d5de05d`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.4 MB (6384400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e6eb06c3eafc85d4885514c3a9d4eaeb2bbd393908999e4e1c2cfab855ba12`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:cdbef24ab485faaa912abc481a6a6111586123d3dacd25e94430199ef8927b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053cc83c694a5cfe4650f76daed30bd4ea101f71fc1ead69b6fe3d39f6497f4`

```dockerfile
```

-	Layers:
	-	`sha256:50bceea36393d1b0fea8cac19e67d2f748122f613e976f8d48e8d5e360914291`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f42ef7fe1a4cb7d4fec579ed9fe2e3732177d98b0c46bc9359c4727c4844a34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c781a0b177c52554f87b8adc28116cad47cac515449e3b0d8fe93124667a2a0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e982c114a13138e2685668359ca9e0582e26abafe5549dac8de6da9ec5a4812`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.4 MB (6374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a62dc33b5ce9228790b002e0f1f443db4eb3c933b74f7fde40672a56a02e631`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0df3bc19acaa140730a4b021933fd9fa7643dcd678497e981ca04643be7180e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95eb5ef4c403726c81fa2dd926bb831b92f13393dca29987e551f6a940637b58`

```dockerfile
```

-	Layers:
	-	`sha256:b650fc90dc66830f3dc69eee5084e1526a32f36e96c99b03ea9ae1b3a19a5639`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:316df87993501b7d4394c6b1b9dfd4976526a779e280876525025286599ff684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651baae8fed97cb865aefef1560828eab06acca8a268b65ca72f6527265b8347`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dbab1ffdd888ab70dbb64d3905f68ffaad15b074fb768ff177945584a4da2979`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.0 MB (6038038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8045fe26152996b1c25cf1b69933f764bf3664850d2b4be0556bbdc395ba6de2`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d09c06c30cc3b40485410a0197b49119e223d0447330bbe33e5ef2e490e60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6db17398ff64e2610c75eee6813ea209398c776e29c9b3a4d2c88c74ac6061`

```dockerfile
```

-	Layers:
	-	`sha256:c1ad2a823e70e752b8e707ba2e6f79d061bd6513e9048a5d3ba1b0dcebd8fdb7`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:500376f0032cee55f7b622d44d14ae96c78ce53f784ad0ddef4199174c89eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6101131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f548d07e5f7bc1f81d5bee95f9bd3381ca511a036e8a7936d12d8a2e4d7e69b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:11:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:11:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:11:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:11:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3c8128190e1f74d677c2c6c27f17e58287ea869b0ac83a3ec8d948f9864be4`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.1 MB (6100622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42409a8650a26777b9e5dd74e0df3bd3748139444b14c796f069d3c16de2f127`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a2067ef8c3e73eb50d26fbfa7596ad1fa0a6f11eee80691723cb2572685ce98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bbed2722880584cc7603d06f5af5f1b4bccc740b2cb624f1a06d10d6698f72`

```dockerfile
```

-	Layers:
	-	`sha256:d734a1f9d3be60b9a5b7b1a162fa81127a103df769ce8ee78bd5c9a088595b9b`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:d45b83fd088c8a12f4b9d20fcacb17b0f2d508bb6dd6fe140622651eb24ad21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4d2b317e4704fab7645f76695aee5985f04c2004740e64e3c9b147824715a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7af0e8a091b6b9b365d51014f398aea3666f8e453d6f97753b7042a611b1ef7`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.5 MB (6491236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce8719bf0358a3223ffb862bd466323c56a5840bbe43d8756f3c7d527c0cfcc`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:791c562ec98ec32eb1e725744aad93054ed5266e94c2d8ff82317b8995f8cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a338d714fbe0106f3a32fe785c578007bbbc750feb73a10baa3cce1e7ad43bc`

```dockerfile
```

-	Layers:
	-	`sha256:66e8efa3e7bdb303fe57fd3586c3ef4b0163d79e3d434683180afca7a23659f7`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.11-nanoserver`

```console
$ docker pull nats@sha256:f12c13db6817ccdfb1762de51624e0ac1a8a6d4f0ca86de3f349181eeabab5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12.11-nanoserver` - windows version 10.0.20348.5256; amd64

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

## `nats:2.12.11-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:f12c13db6817ccdfb1762de51624e0ac1a8a6d4f0ca86de3f349181eeabab5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12.11-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

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

## `nats:2.12.11-scratch`

```console
$ docker pull nats@sha256:a5e6ee541d62c5962207eb78d5127eb6cbdb49a9a4095bf08ba0b659ee3b8309
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

### `nats:2.12.11-scratch` - linux; amd64

```console
$ docker pull nats@sha256:2ab08148b4ee24429eebb667e21f80941ce1657f8afa979f10af4f05d91b8292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f0275e3d5bf0a174d1028cfb9d9471a1ccd982804f878e52da3866108aa1f8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88913724d1d8e74f3f1ff6a60b00a7acb8450d4f1888012fc2a1719b0f571279`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.6 MB (6643520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cd67fdee0900fa1ef3862345a62480b27fc2a450a7d0eda5c82bff946cab6`  
		Last Modified: Tue, 09 Jun 2026 18:12:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5b402cfa502a3b2d8c31c1c4fc6bd3276940b02322d4c5b7658a0e4cee7a35ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f5a4fa862a018d0d9ba5c3e56399da46ce4aa8e5dbdc872e229aab637a451d`

```dockerfile
```

-	Layers:
	-	`sha256:d0b54ff432fb5083ca7878e58ca4d396e73dba72f176038440a90e5d48050517`  
		Last Modified: Tue, 09 Jun 2026 18:12:33 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:4671c4b21974e9ee77abf49375a0e76797e78b96f3b100b39fdfb136a364401a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6384909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c272b02c9e1c0b607d2bc944c19679af6b223d549448d295df5d3a30a441b4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:08:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:08:48 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:08:48 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:08:48 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:08:48 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:56ed75683f9b5db33f8ad9a299605af0eae8a9ebe1c30ef8e894bea87d5de05d`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.4 MB (6384400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e6eb06c3eafc85d4885514c3a9d4eaeb2bbd393908999e4e1c2cfab855ba12`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:cdbef24ab485faaa912abc481a6a6111586123d3dacd25e94430199ef8927b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053cc83c694a5cfe4650f76daed30bd4ea101f71fc1ead69b6fe3d39f6497f4`

```dockerfile
```

-	Layers:
	-	`sha256:50bceea36393d1b0fea8cac19e67d2f748122f613e976f8d48e8d5e360914291`  
		Last Modified: Tue, 09 Jun 2026 18:08:52 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f42ef7fe1a4cb7d4fec579ed9fe2e3732177d98b0c46bc9359c4727c4844a34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c781a0b177c52554f87b8adc28116cad47cac515449e3b0d8fe93124667a2a0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:21 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:21 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:21 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e982c114a13138e2685668359ca9e0582e26abafe5549dac8de6da9ec5a4812`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.4 MB (6374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a62dc33b5ce9228790b002e0f1f443db4eb3c933b74f7fde40672a56a02e631`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0df3bc19acaa140730a4b021933fd9fa7643dcd678497e981ca04643be7180e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95eb5ef4c403726c81fa2dd926bb831b92f13393dca29987e551f6a940637b58`

```dockerfile
```

-	Layers:
	-	`sha256:b650fc90dc66830f3dc69eee5084e1526a32f36e96c99b03ea9ae1b3a19a5639`  
		Last Modified: Tue, 09 Jun 2026 18:09:25 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:316df87993501b7d4394c6b1b9dfd4976526a779e280876525025286599ff684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651baae8fed97cb865aefef1560828eab06acca8a268b65ca72f6527265b8347`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dbab1ffdd888ab70dbb64d3905f68ffaad15b074fb768ff177945584a4da2979`  
		Last Modified: Tue, 09 Jun 2026 15:35:49 GMT  
		Size: 6.0 MB (6038038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8045fe26152996b1c25cf1b69933f764bf3664850d2b4be0556bbdc395ba6de2`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d09c06c30cc3b40485410a0197b49119e223d0447330bbe33e5ef2e490e60737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6db17398ff64e2610c75eee6813ea209398c776e29c9b3a4d2c88c74ac6061`

```dockerfile
```

-	Layers:
	-	`sha256:c1ad2a823e70e752b8e707ba2e6f79d061bd6513e9048a5d3ba1b0dcebd8fdb7`  
		Last Modified: Tue, 09 Jun 2026 18:09:07 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:500376f0032cee55f7b622d44d14ae96c78ce53f784ad0ddef4199174c89eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6101131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f548d07e5f7bc1f81d5bee95f9bd3381ca511a036e8a7936d12d8a2e4d7e69b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:11:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:11:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:11:03 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:11:03 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:11:03 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f3c8128190e1f74d677c2c6c27f17e58287ea869b0ac83a3ec8d948f9864be4`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.1 MB (6100622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42409a8650a26777b9e5dd74e0df3bd3748139444b14c796f069d3c16de2f127`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a2067ef8c3e73eb50d26fbfa7596ad1fa0a6f11eee80691723cb2572685ce98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bbed2722880584cc7603d06f5af5f1b4bccc740b2cb624f1a06d10d6698f72`

```dockerfile
```

-	Layers:
	-	`sha256:d734a1f9d3be60b9a5b7b1a162fa81127a103df769ce8ee78bd5c9a088595b9b`  
		Last Modified: Tue, 09 Jun 2026 18:11:10 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:d45b83fd088c8a12f4b9d20fcacb17b0f2d508bb6dd6fe140622651eb24ad21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6491746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4d2b317e4704fab7645f76695aee5985f04c2004740e64e3c9b147824715a4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 09 Jun 2026 18:09:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 09 Jun 2026 18:09:49 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 09 Jun 2026 18:09:49 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 09 Jun 2026 18:09:49 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 09 Jun 2026 18:09:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a7af0e8a091b6b9b365d51014f398aea3666f8e453d6f97753b7042a611b1ef7`  
		Last Modified: Tue, 09 Jun 2026 15:35:52 GMT  
		Size: 6.5 MB (6491236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce8719bf0358a3223ffb862bd466323c56a5840bbe43d8756f3c7d527c0cfcc`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:791c562ec98ec32eb1e725744aad93054ed5266e94c2d8ff82317b8995f8cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a338d714fbe0106f3a32fe785c578007bbbc750feb73a10baa3cce1e7ad43bc`

```dockerfile
```

-	Layers:
	-	`sha256:66e8efa3e7bdb303fe57fd3586c3ef4b0163d79e3d434683180afca7a23659f7`  
		Last Modified: Tue, 09 Jun 2026 18:09:57 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.11-windowsservercore`

```console
$ docker pull nats@sha256:edccb8294b3e618c23c5b8f1a4d7cc24f79a79c3267b1b870579feaaccfc286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12.11-windowsservercore` - windows version 10.0.20348.5256; amd64

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

## `nats:2.12.11-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:edccb8294b3e618c23c5b8f1a4d7cc24f79a79c3267b1b870579feaaccfc286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12.11-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

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

## `nats:2.14`

```console
$ docker pull nats@sha256:771149b0d90eca2137d24c8d205521fec157e38510f2b46e9fc370e54ae4262f
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
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
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
$ docker pull nats@sha256:b039b46715673a9436989cfc49dde04e6bd57e205347478a58214789baf5efdc
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
$ docker pull nats@sha256:f0679b55723570b245b735087116f40b61209f9419a052555911d92ba92db3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f2c459fccd79c9b1768d7235853736817cc95553a4a77e0fcc60d748ded94c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91149e471871c2ede088818330273446a46a28fa17ab6019c347e827f3d88e`  
		Last Modified: Tue, 02 Jun 2026 19:05:14 GMT  
		Size: 7.3 MB (7294356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1780775af23cf70b20cc6730511246e7e72d42ce7d668c73c18b90d48a67a01`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db4d3abeff2b99495264a4eee8c173e4cddac6f2562cf176849969f8bfeb6f5`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:433ad5e1cd4d4638ba012ef6d511de6ada4d25848d45a59a419c4e8c8f212504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5457ab88186ec095f87e6383750982f83261069aa7d81add3cf4e931d5bd8b8d`

```dockerfile
```

-	Layers:
	-	`sha256:97908037527cfc59a216bfe62a51d23f134332356fa5e4b7cb247741bdd17194`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bd43cfbbeacf6edb2b475c63866eb39de3639ff98c7ba4b2e864136daf55afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10542108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb38008b73bdfef49b080f538c56c59c970defde4adf819ce4be46eb115f13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4134644628fbe8c80ca77808206ab4ff2c01c11c3c49f656c7120757e9b9d8`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 7.0 MB (7033752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37f54e57d50f3a9c76dd3ddbf500d95b6c7e85c7c07aa48147c6cdd9defbe4`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f867e1babe5c47998841c28bded391ef496d71feb54b61f4545d87f5a646cba`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:41db50f6cc4d9bfd6ec2c46f419eed60136e695a19f5892004fc8e16f9e4c958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacd6b789756bea2927e2e1131c952cd3ad9c48cb279eb3eb6303fc9ab294d2f`

```dockerfile
```

-	Layers:
	-	`sha256:5e30d67018b50219cf111359b9c01c0f494e08d2b3f8569dcc5fd3c1ee5c1d73`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:ad14dda00ccf242342a93cc85db34a56bb25d3e296ecdace5147c1966b5b3b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10247947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec25b1ccdde1f720071b74505ffdf00e039ab69a2fd75f71d020027bd2c0a7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9df1ef32961e68a3939cd854cdbbf23eadb85878e7a2924c8e8b55ed686db`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 7.0 MB (7021143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3a2252f7f49291e414a088e7d5d7d5b1ed30e39570d7aaaddefe72ad7ec45`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f706a5b129742a751a90778c239816e2f65e8da796265eea974d0684885fe`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:37cb5f4f11c03e9635452373f12b4933fd563eb9d9b579fa4d81074c310b783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8831237e5b1eb42138b1b533eac461905370c52864faa74ad64aa64ee6929ea9`

```dockerfile
```

-	Layers:
	-	`sha256:8b0c0c197e4c11be4cea42928534aba725c08e8453c25ec9bc3b3d17f826cd06`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:611c3dbd05ff98e9f9f562b4ecc89822c2b0367847d932a4932c1ed966bc9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10792301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a4b2095da890cb3d5ca21aa5d61d37c4ca5fd0cde2e2037c3552e8b346140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967f1732be2cea3277e46b05ada1d6dc6dc0c9d759046c2618be783fee259b3`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.6 MB (6649438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729dba32d18e040f985909e362d966b7bdd5bb98293da5c5b092b2db7b1ad6c`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd385b5d9562cba05d122624afc347bf04e331b1039428b62bfa34329ae6fc`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83650089aa5af8edeacd31f9575f51c4865f49f4658f5e4783da1893cbd73665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ea3db6409708bdb914b77d4ccc8d0aeb240671d5247e30d10994a292bed6a`

```dockerfile
```

-	Layers:
	-	`sha256:0e0bb2fa8f0c108b876e46f52d13f30f36c80387b8275abc10d23d94c3c159f2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:03cac3b8dd8dfa41d75112c2ae5b94fec0af6f5814730e5330012354cf7f0827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447bf89722c6586ace97b811cfa21359201cf2f9713c5e1fef6213a7acc2650e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:09:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:09:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a55d0eaca97f0390033ffa8d9134bc7a0079525bf40c87025873115014fab03`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.7 MB (6712091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e475251befa77978ceea2dd486692601fdf578dc6cf93f6f34db105424faa429`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd101bdee386ea23d9751c471412ed9d61e7b3bb95fa9c4c09dcf11b393862b0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:878c6cd3e6ca2b63e8e7c9012c4a51e6f964a8e1f17a510c05f7000a2ee3c3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b43654f9754af02840c24097bead60f9bda1a56f0d0331c1cdb97492d058d1d`

```dockerfile
```

-	Layers:
	-	`sha256:277a9558e629945d4f89fbecb1fece232afa05343087d445fab71410b96445a5`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; s390x

```console
$ docker pull nats@sha256:841b7ad0b071063eab531f42992071e88a18027757dc688943e9b6be84f30b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10758432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8d5496bf4f8dc7bc2e68a44462403d27657a08420f26e155ef56c4b875cd1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9e1c021cb6668546fbd3caeb13392781503722c1117940072299d8a401f78`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 7.1 MB (7103589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7207403655133bcd046b16235270ff4b177f4e43d2903766cfb7a82d247e914`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107699ca626db0b1dca70dd8b094467bb9da6bad2e7b07a3e817e656f0528716`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d93ecdc48d72d516e5b6b434a8f943f9a0a356ea2e81c18a79d46fa97dac3cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e2b39405c34660d72439c24d374ad63c17ff6072b7967c16a05e3d681f075e`

```dockerfile
```

-	Layers:
	-	`sha256:73ea22818eaf35e7185adc8c19baf720eec4e2f32f9e2f8eefc0ae10f85ea059`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-alpine3.22`

```console
$ docker pull nats@sha256:b039b46715673a9436989cfc49dde04e6bd57e205347478a58214789baf5efdc
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
$ docker pull nats@sha256:f0679b55723570b245b735087116f40b61209f9419a052555911d92ba92db3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f2c459fccd79c9b1768d7235853736817cc95553a4a77e0fcc60d748ded94c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91149e471871c2ede088818330273446a46a28fa17ab6019c347e827f3d88e`  
		Last Modified: Tue, 02 Jun 2026 19:05:14 GMT  
		Size: 7.3 MB (7294356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1780775af23cf70b20cc6730511246e7e72d42ce7d668c73c18b90d48a67a01`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db4d3abeff2b99495264a4eee8c173e4cddac6f2562cf176849969f8bfeb6f5`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:433ad5e1cd4d4638ba012ef6d511de6ada4d25848d45a59a419c4e8c8f212504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5457ab88186ec095f87e6383750982f83261069aa7d81add3cf4e931d5bd8b8d`

```dockerfile
```

-	Layers:
	-	`sha256:97908037527cfc59a216bfe62a51d23f134332356fa5e4b7cb247741bdd17194`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:bd43cfbbeacf6edb2b475c63866eb39de3639ff98c7ba4b2e864136daf55afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10542108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb38008b73bdfef49b080f538c56c59c970defde4adf819ce4be46eb115f13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4134644628fbe8c80ca77808206ab4ff2c01c11c3c49f656c7120757e9b9d8`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 7.0 MB (7033752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37f54e57d50f3a9c76dd3ddbf500d95b6c7e85c7c07aa48147c6cdd9defbe4`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f867e1babe5c47998841c28bded391ef496d71feb54b61f4545d87f5a646cba`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:41db50f6cc4d9bfd6ec2c46f419eed60136e695a19f5892004fc8e16f9e4c958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacd6b789756bea2927e2e1131c952cd3ad9c48cb279eb3eb6303fc9ab294d2f`

```dockerfile
```

-	Layers:
	-	`sha256:5e30d67018b50219cf111359b9c01c0f494e08d2b3f8569dcc5fd3c1ee5c1d73`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:ad14dda00ccf242342a93cc85db34a56bb25d3e296ecdace5147c1966b5b3b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10247947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec25b1ccdde1f720071b74505ffdf00e039ab69a2fd75f71d020027bd2c0a7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9df1ef32961e68a3939cd854cdbbf23eadb85878e7a2924c8e8b55ed686db`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 7.0 MB (7021143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3a2252f7f49291e414a088e7d5d7d5b1ed30e39570d7aaaddefe72ad7ec45`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f706a5b129742a751a90778c239816e2f65e8da796265eea974d0684885fe`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:37cb5f4f11c03e9635452373f12b4933fd563eb9d9b579fa4d81074c310b783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8831237e5b1eb42138b1b533eac461905370c52864faa74ad64aa64ee6929ea9`

```dockerfile
```

-	Layers:
	-	`sha256:8b0c0c197e4c11be4cea42928534aba725c08e8453c25ec9bc3b3d17f826cd06`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:611c3dbd05ff98e9f9f562b4ecc89822c2b0367847d932a4932c1ed966bc9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10792301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a4b2095da890cb3d5ca21aa5d61d37c4ca5fd0cde2e2037c3552e8b346140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967f1732be2cea3277e46b05ada1d6dc6dc0c9d759046c2618be783fee259b3`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.6 MB (6649438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729dba32d18e040f985909e362d966b7bdd5bb98293da5c5b092b2db7b1ad6c`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd385b5d9562cba05d122624afc347bf04e331b1039428b62bfa34329ae6fc`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83650089aa5af8edeacd31f9575f51c4865f49f4658f5e4783da1893cbd73665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ea3db6409708bdb914b77d4ccc8d0aeb240671d5247e30d10994a292bed6a`

```dockerfile
```

-	Layers:
	-	`sha256:0e0bb2fa8f0c108b876e46f52d13f30f36c80387b8275abc10d23d94c3c159f2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:03cac3b8dd8dfa41d75112c2ae5b94fec0af6f5814730e5330012354cf7f0827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447bf89722c6586ace97b811cfa21359201cf2f9713c5e1fef6213a7acc2650e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:09:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:09:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a55d0eaca97f0390033ffa8d9134bc7a0079525bf40c87025873115014fab03`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.7 MB (6712091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e475251befa77978ceea2dd486692601fdf578dc6cf93f6f34db105424faa429`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd101bdee386ea23d9751c471412ed9d61e7b3bb95fa9c4c09dcf11b393862b0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:878c6cd3e6ca2b63e8e7c9012c4a51e6f964a8e1f17a510c05f7000a2ee3c3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b43654f9754af02840c24097bead60f9bda1a56f0d0331c1cdb97492d058d1d`

```dockerfile
```

-	Layers:
	-	`sha256:277a9558e629945d4f89fbecb1fece232afa05343087d445fab71410b96445a5`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:841b7ad0b071063eab531f42992071e88a18027757dc688943e9b6be84f30b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10758432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8d5496bf4f8dc7bc2e68a44462403d27657a08420f26e155ef56c4b875cd1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9e1c021cb6668546fbd3caeb13392781503722c1117940072299d8a401f78`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 7.1 MB (7103589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7207403655133bcd046b16235270ff4b177f4e43d2903766cfb7a82d247e914`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107699ca626db0b1dca70dd8b094467bb9da6bad2e7b07a3e817e656f0528716`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d93ecdc48d72d516e5b6b434a8f943f9a0a356ea2e81c18a79d46fa97dac3cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e2b39405c34660d72439c24d374ad63c17ff6072b7967c16a05e3d681f075e`

```dockerfile
```

-	Layers:
	-	`sha256:73ea22818eaf35e7185adc8c19baf720eec4e2f32f9e2f8eefc0ae10f85ea059`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-linux`

```console
$ docker pull nats@sha256:d6519b375b05bc720d5a10240e23ecec1fcb559f2d48b9d13fe6408331a52e7a
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
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
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
$ docker pull nats@sha256:d6519b375b05bc720d5a10240e23ecec1fcb559f2d48b9d13fe6408331a52e7a
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
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
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

## `nats:2.14.2`

```console
$ docker pull nats@sha256:771149b0d90eca2137d24c8d205521fec157e38510f2b46e9fc370e54ae4262f
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

### `nats:2.14.2` - linux; amd64

```console
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2` - windows version 10.0.20348.5256; amd64

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

## `nats:2.14.2-alpine`

```console
$ docker pull nats@sha256:b039b46715673a9436989cfc49dde04e6bd57e205347478a58214789baf5efdc
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

### `nats:2.14.2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:f0679b55723570b245b735087116f40b61209f9419a052555911d92ba92db3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f2c459fccd79c9b1768d7235853736817cc95553a4a77e0fcc60d748ded94c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91149e471871c2ede088818330273446a46a28fa17ab6019c347e827f3d88e`  
		Last Modified: Tue, 02 Jun 2026 19:05:14 GMT  
		Size: 7.3 MB (7294356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1780775af23cf70b20cc6730511246e7e72d42ce7d668c73c18b90d48a67a01`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db4d3abeff2b99495264a4eee8c173e4cddac6f2562cf176849969f8bfeb6f5`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:433ad5e1cd4d4638ba012ef6d511de6ada4d25848d45a59a419c4e8c8f212504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5457ab88186ec095f87e6383750982f83261069aa7d81add3cf4e931d5bd8b8d`

```dockerfile
```

-	Layers:
	-	`sha256:97908037527cfc59a216bfe62a51d23f134332356fa5e4b7cb247741bdd17194`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bd43cfbbeacf6edb2b475c63866eb39de3639ff98c7ba4b2e864136daf55afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10542108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb38008b73bdfef49b080f538c56c59c970defde4adf819ce4be46eb115f13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4134644628fbe8c80ca77808206ab4ff2c01c11c3c49f656c7120757e9b9d8`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 7.0 MB (7033752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37f54e57d50f3a9c76dd3ddbf500d95b6c7e85c7c07aa48147c6cdd9defbe4`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f867e1babe5c47998841c28bded391ef496d71feb54b61f4545d87f5a646cba`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:41db50f6cc4d9bfd6ec2c46f419eed60136e695a19f5892004fc8e16f9e4c958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacd6b789756bea2927e2e1131c952cd3ad9c48cb279eb3eb6303fc9ab294d2f`

```dockerfile
```

-	Layers:
	-	`sha256:5e30d67018b50219cf111359b9c01c0f494e08d2b3f8569dcc5fd3c1ee5c1d73`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:ad14dda00ccf242342a93cc85db34a56bb25d3e296ecdace5147c1966b5b3b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10247947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec25b1ccdde1f720071b74505ffdf00e039ab69a2fd75f71d020027bd2c0a7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9df1ef32961e68a3939cd854cdbbf23eadb85878e7a2924c8e8b55ed686db`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 7.0 MB (7021143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3a2252f7f49291e414a088e7d5d7d5b1ed30e39570d7aaaddefe72ad7ec45`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f706a5b129742a751a90778c239816e2f65e8da796265eea974d0684885fe`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:37cb5f4f11c03e9635452373f12b4933fd563eb9d9b579fa4d81074c310b783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8831237e5b1eb42138b1b533eac461905370c52864faa74ad64aa64ee6929ea9`

```dockerfile
```

-	Layers:
	-	`sha256:8b0c0c197e4c11be4cea42928534aba725c08e8453c25ec9bc3b3d17f826cd06`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:611c3dbd05ff98e9f9f562b4ecc89822c2b0367847d932a4932c1ed966bc9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10792301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a4b2095da890cb3d5ca21aa5d61d37c4ca5fd0cde2e2037c3552e8b346140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967f1732be2cea3277e46b05ada1d6dc6dc0c9d759046c2618be783fee259b3`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.6 MB (6649438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729dba32d18e040f985909e362d966b7bdd5bb98293da5c5b092b2db7b1ad6c`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd385b5d9562cba05d122624afc347bf04e331b1039428b62bfa34329ae6fc`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83650089aa5af8edeacd31f9575f51c4865f49f4658f5e4783da1893cbd73665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ea3db6409708bdb914b77d4ccc8d0aeb240671d5247e30d10994a292bed6a`

```dockerfile
```

-	Layers:
	-	`sha256:0e0bb2fa8f0c108b876e46f52d13f30f36c80387b8275abc10d23d94c3c159f2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:03cac3b8dd8dfa41d75112c2ae5b94fec0af6f5814730e5330012354cf7f0827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447bf89722c6586ace97b811cfa21359201cf2f9713c5e1fef6213a7acc2650e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:09:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:09:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a55d0eaca97f0390033ffa8d9134bc7a0079525bf40c87025873115014fab03`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.7 MB (6712091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e475251befa77978ceea2dd486692601fdf578dc6cf93f6f34db105424faa429`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd101bdee386ea23d9751c471412ed9d61e7b3bb95fa9c4c09dcf11b393862b0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:878c6cd3e6ca2b63e8e7c9012c4a51e6f964a8e1f17a510c05f7000a2ee3c3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b43654f9754af02840c24097bead60f9bda1a56f0d0331c1cdb97492d058d1d`

```dockerfile
```

-	Layers:
	-	`sha256:277a9558e629945d4f89fbecb1fece232afa05343087d445fab71410b96445a5`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:841b7ad0b071063eab531f42992071e88a18027757dc688943e9b6be84f30b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10758432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8d5496bf4f8dc7bc2e68a44462403d27657a08420f26e155ef56c4b875cd1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9e1c021cb6668546fbd3caeb13392781503722c1117940072299d8a401f78`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 7.1 MB (7103589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7207403655133bcd046b16235270ff4b177f4e43d2903766cfb7a82d247e914`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107699ca626db0b1dca70dd8b094467bb9da6bad2e7b07a3e817e656f0528716`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d93ecdc48d72d516e5b6b434a8f943f9a0a356ea2e81c18a79d46fa97dac3cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e2b39405c34660d72439c24d374ad63c17ff6072b7967c16a05e3d681f075e`

```dockerfile
```

-	Layers:
	-	`sha256:73ea22818eaf35e7185adc8c19baf720eec4e2f32f9e2f8eefc0ae10f85ea059`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.2-alpine3.22`

```console
$ docker pull nats@sha256:b039b46715673a9436989cfc49dde04e6bd57e205347478a58214789baf5efdc
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

### `nats:2.14.2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:f0679b55723570b245b735087116f40b61209f9419a052555911d92ba92db3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f2c459fccd79c9b1768d7235853736817cc95553a4a77e0fcc60d748ded94c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91149e471871c2ede088818330273446a46a28fa17ab6019c347e827f3d88e`  
		Last Modified: Tue, 02 Jun 2026 19:05:14 GMT  
		Size: 7.3 MB (7294356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1780775af23cf70b20cc6730511246e7e72d42ce7d668c73c18b90d48a67a01`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db4d3abeff2b99495264a4eee8c173e4cddac6f2562cf176849969f8bfeb6f5`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:433ad5e1cd4d4638ba012ef6d511de6ada4d25848d45a59a419c4e8c8f212504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5457ab88186ec095f87e6383750982f83261069aa7d81add3cf4e931d5bd8b8d`

```dockerfile
```

-	Layers:
	-	`sha256:97908037527cfc59a216bfe62a51d23f134332356fa5e4b7cb247741bdd17194`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:bd43cfbbeacf6edb2b475c63866eb39de3639ff98c7ba4b2e864136daf55afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10542108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb38008b73bdfef49b080f538c56c59c970defde4adf819ce4be46eb115f13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4134644628fbe8c80ca77808206ab4ff2c01c11c3c49f656c7120757e9b9d8`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 7.0 MB (7033752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37f54e57d50f3a9c76dd3ddbf500d95b6c7e85c7c07aa48147c6cdd9defbe4`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f867e1babe5c47998841c28bded391ef496d71feb54b61f4545d87f5a646cba`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:41db50f6cc4d9bfd6ec2c46f419eed60136e695a19f5892004fc8e16f9e4c958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacd6b789756bea2927e2e1131c952cd3ad9c48cb279eb3eb6303fc9ab294d2f`

```dockerfile
```

-	Layers:
	-	`sha256:5e30d67018b50219cf111359b9c01c0f494e08d2b3f8569dcc5fd3c1ee5c1d73`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:ad14dda00ccf242342a93cc85db34a56bb25d3e296ecdace5147c1966b5b3b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10247947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec25b1ccdde1f720071b74505ffdf00e039ab69a2fd75f71d020027bd2c0a7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9df1ef32961e68a3939cd854cdbbf23eadb85878e7a2924c8e8b55ed686db`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 7.0 MB (7021143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3a2252f7f49291e414a088e7d5d7d5b1ed30e39570d7aaaddefe72ad7ec45`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f706a5b129742a751a90778c239816e2f65e8da796265eea974d0684885fe`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:37cb5f4f11c03e9635452373f12b4933fd563eb9d9b579fa4d81074c310b783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8831237e5b1eb42138b1b533eac461905370c52864faa74ad64aa64ee6929ea9`

```dockerfile
```

-	Layers:
	-	`sha256:8b0c0c197e4c11be4cea42928534aba725c08e8453c25ec9bc3b3d17f826cd06`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:611c3dbd05ff98e9f9f562b4ecc89822c2b0367847d932a4932c1ed966bc9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10792301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a4b2095da890cb3d5ca21aa5d61d37c4ca5fd0cde2e2037c3552e8b346140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967f1732be2cea3277e46b05ada1d6dc6dc0c9d759046c2618be783fee259b3`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.6 MB (6649438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729dba32d18e040f985909e362d966b7bdd5bb98293da5c5b092b2db7b1ad6c`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd385b5d9562cba05d122624afc347bf04e331b1039428b62bfa34329ae6fc`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83650089aa5af8edeacd31f9575f51c4865f49f4658f5e4783da1893cbd73665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ea3db6409708bdb914b77d4ccc8d0aeb240671d5247e30d10994a292bed6a`

```dockerfile
```

-	Layers:
	-	`sha256:0e0bb2fa8f0c108b876e46f52d13f30f36c80387b8275abc10d23d94c3c159f2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:03cac3b8dd8dfa41d75112c2ae5b94fec0af6f5814730e5330012354cf7f0827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447bf89722c6586ace97b811cfa21359201cf2f9713c5e1fef6213a7acc2650e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:09:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:09:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a55d0eaca97f0390033ffa8d9134bc7a0079525bf40c87025873115014fab03`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.7 MB (6712091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e475251befa77978ceea2dd486692601fdf578dc6cf93f6f34db105424faa429`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd101bdee386ea23d9751c471412ed9d61e7b3bb95fa9c4c09dcf11b393862b0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:878c6cd3e6ca2b63e8e7c9012c4a51e6f964a8e1f17a510c05f7000a2ee3c3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b43654f9754af02840c24097bead60f9bda1a56f0d0331c1cdb97492d058d1d`

```dockerfile
```

-	Layers:
	-	`sha256:277a9558e629945d4f89fbecb1fece232afa05343087d445fab71410b96445a5`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:841b7ad0b071063eab531f42992071e88a18027757dc688943e9b6be84f30b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10758432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8d5496bf4f8dc7bc2e68a44462403d27657a08420f26e155ef56c4b875cd1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9e1c021cb6668546fbd3caeb13392781503722c1117940072299d8a401f78`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 7.1 MB (7103589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7207403655133bcd046b16235270ff4b177f4e43d2903766cfb7a82d247e914`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107699ca626db0b1dca70dd8b094467bb9da6bad2e7b07a3e817e656f0528716`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d93ecdc48d72d516e5b6b434a8f943f9a0a356ea2e81c18a79d46fa97dac3cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e2b39405c34660d72439c24d374ad63c17ff6072b7967c16a05e3d681f075e`

```dockerfile
```

-	Layers:
	-	`sha256:73ea22818eaf35e7185adc8c19baf720eec4e2f32f9e2f8eefc0ae10f85ea059`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.2-linux`

```console
$ docker pull nats@sha256:d6519b375b05bc720d5a10240e23ecec1fcb559f2d48b9d13fe6408331a52e7a
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

### `nats:2.14.2-linux` - linux; amd64

```console
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-linux` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.2-nanoserver`

```console
$ docker pull nats@sha256:9622b8c98b2488b8efd76eefe88e2b019d542d6de0e04db7af8d21e067f39ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14.2-nanoserver` - windows version 10.0.20348.5256; amd64

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

## `nats:2.14.2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:9622b8c98b2488b8efd76eefe88e2b019d542d6de0e04db7af8d21e067f39ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14.2-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

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

## `nats:2.14.2-scratch`

```console
$ docker pull nats@sha256:d6519b375b05bc720d5a10240e23ecec1fcb559f2d48b9d13fe6408331a52e7a
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

### `nats:2.14.2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.2-windowsservercore`

```console
$ docker pull nats@sha256:30c6818895521b905434c83a874393e80e00eeb16c99cb406aabc52f6e841305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14.2-windowsservercore` - windows version 10.0.20348.5256; amd64

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

## `nats:2.14.2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:30c6818895521b905434c83a874393e80e00eeb16c99cb406aabc52f6e841305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14.2-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

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

## `nats:alpine`

```console
$ docker pull nats@sha256:b039b46715673a9436989cfc49dde04e6bd57e205347478a58214789baf5efdc
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
$ docker pull nats@sha256:f0679b55723570b245b735087116f40b61209f9419a052555911d92ba92db3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f2c459fccd79c9b1768d7235853736817cc95553a4a77e0fcc60d748ded94c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91149e471871c2ede088818330273446a46a28fa17ab6019c347e827f3d88e`  
		Last Modified: Tue, 02 Jun 2026 19:05:14 GMT  
		Size: 7.3 MB (7294356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1780775af23cf70b20cc6730511246e7e72d42ce7d668c73c18b90d48a67a01`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db4d3abeff2b99495264a4eee8c173e4cddac6f2562cf176849969f8bfeb6f5`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:433ad5e1cd4d4638ba012ef6d511de6ada4d25848d45a59a419c4e8c8f212504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5457ab88186ec095f87e6383750982f83261069aa7d81add3cf4e931d5bd8b8d`

```dockerfile
```

-	Layers:
	-	`sha256:97908037527cfc59a216bfe62a51d23f134332356fa5e4b7cb247741bdd17194`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bd43cfbbeacf6edb2b475c63866eb39de3639ff98c7ba4b2e864136daf55afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10542108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb38008b73bdfef49b080f538c56c59c970defde4adf819ce4be46eb115f13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4134644628fbe8c80ca77808206ab4ff2c01c11c3c49f656c7120757e9b9d8`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 7.0 MB (7033752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37f54e57d50f3a9c76dd3ddbf500d95b6c7e85c7c07aa48147c6cdd9defbe4`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f867e1babe5c47998841c28bded391ef496d71feb54b61f4545d87f5a646cba`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:41db50f6cc4d9bfd6ec2c46f419eed60136e695a19f5892004fc8e16f9e4c958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacd6b789756bea2927e2e1131c952cd3ad9c48cb279eb3eb6303fc9ab294d2f`

```dockerfile
```

-	Layers:
	-	`sha256:5e30d67018b50219cf111359b9c01c0f494e08d2b3f8569dcc5fd3c1ee5c1d73`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:ad14dda00ccf242342a93cc85db34a56bb25d3e296ecdace5147c1966b5b3b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10247947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec25b1ccdde1f720071b74505ffdf00e039ab69a2fd75f71d020027bd2c0a7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9df1ef32961e68a3939cd854cdbbf23eadb85878e7a2924c8e8b55ed686db`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 7.0 MB (7021143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3a2252f7f49291e414a088e7d5d7d5b1ed30e39570d7aaaddefe72ad7ec45`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f706a5b129742a751a90778c239816e2f65e8da796265eea974d0684885fe`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:37cb5f4f11c03e9635452373f12b4933fd563eb9d9b579fa4d81074c310b783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8831237e5b1eb42138b1b533eac461905370c52864faa74ad64aa64ee6929ea9`

```dockerfile
```

-	Layers:
	-	`sha256:8b0c0c197e4c11be4cea42928534aba725c08e8453c25ec9bc3b3d17f826cd06`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:611c3dbd05ff98e9f9f562b4ecc89822c2b0367847d932a4932c1ed966bc9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10792301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a4b2095da890cb3d5ca21aa5d61d37c4ca5fd0cde2e2037c3552e8b346140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967f1732be2cea3277e46b05ada1d6dc6dc0c9d759046c2618be783fee259b3`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.6 MB (6649438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729dba32d18e040f985909e362d966b7bdd5bb98293da5c5b092b2db7b1ad6c`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd385b5d9562cba05d122624afc347bf04e331b1039428b62bfa34329ae6fc`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:83650089aa5af8edeacd31f9575f51c4865f49f4658f5e4783da1893cbd73665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ea3db6409708bdb914b77d4ccc8d0aeb240671d5247e30d10994a292bed6a`

```dockerfile
```

-	Layers:
	-	`sha256:0e0bb2fa8f0c108b876e46f52d13f30f36c80387b8275abc10d23d94c3c159f2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:03cac3b8dd8dfa41d75112c2ae5b94fec0af6f5814730e5330012354cf7f0827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447bf89722c6586ace97b811cfa21359201cf2f9713c5e1fef6213a7acc2650e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:09:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:09:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a55d0eaca97f0390033ffa8d9134bc7a0079525bf40c87025873115014fab03`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.7 MB (6712091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e475251befa77978ceea2dd486692601fdf578dc6cf93f6f34db105424faa429`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd101bdee386ea23d9751c471412ed9d61e7b3bb95fa9c4c09dcf11b393862b0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:878c6cd3e6ca2b63e8e7c9012c4a51e6f964a8e1f17a510c05f7000a2ee3c3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b43654f9754af02840c24097bead60f9bda1a56f0d0331c1cdb97492d058d1d`

```dockerfile
```

-	Layers:
	-	`sha256:277a9558e629945d4f89fbecb1fece232afa05343087d445fab71410b96445a5`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:841b7ad0b071063eab531f42992071e88a18027757dc688943e9b6be84f30b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10758432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8d5496bf4f8dc7bc2e68a44462403d27657a08420f26e155ef56c4b875cd1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9e1c021cb6668546fbd3caeb13392781503722c1117940072299d8a401f78`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 7.1 MB (7103589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7207403655133bcd046b16235270ff4b177f4e43d2903766cfb7a82d247e914`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107699ca626db0b1dca70dd8b094467bb9da6bad2e7b07a3e817e656f0528716`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d93ecdc48d72d516e5b6b434a8f943f9a0a356ea2e81c18a79d46fa97dac3cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e2b39405c34660d72439c24d374ad63c17ff6072b7967c16a05e3d681f075e`

```dockerfile
```

-	Layers:
	-	`sha256:73ea22818eaf35e7185adc8c19baf720eec4e2f32f9e2f8eefc0ae10f85ea059`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:b039b46715673a9436989cfc49dde04e6bd57e205347478a58214789baf5efdc
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
$ docker pull nats@sha256:f0679b55723570b245b735087116f40b61209f9419a052555911d92ba92db3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11103519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f2c459fccd79c9b1768d7235853736817cc95553a4a77e0fcc60d748ded94c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91149e471871c2ede088818330273446a46a28fa17ab6019c347e827f3d88e`  
		Last Modified: Tue, 02 Jun 2026 19:05:14 GMT  
		Size: 7.3 MB (7294356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1780775af23cf70b20cc6730511246e7e72d42ce7d668c73c18b90d48a67a01`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db4d3abeff2b99495264a4eee8c173e4cddac6f2562cf176849969f8bfeb6f5`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:433ad5e1cd4d4638ba012ef6d511de6ada4d25848d45a59a419c4e8c8f212504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5457ab88186ec095f87e6383750982f83261069aa7d81add3cf4e931d5bd8b8d`

```dockerfile
```

-	Layers:
	-	`sha256:97908037527cfc59a216bfe62a51d23f134332356fa5e4b7cb247741bdd17194`  
		Last Modified: Tue, 02 Jun 2026 19:05:13 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:bd43cfbbeacf6edb2b475c63866eb39de3639ff98c7ba4b2e864136daf55afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10542108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb38008b73bdfef49b080f538c56c59c970defde4adf819ce4be46eb115f13f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:03:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:03:34 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:03:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4134644628fbe8c80ca77808206ab4ff2c01c11c3c49f656c7120757e9b9d8`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 7.0 MB (7033752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37f54e57d50f3a9c76dd3ddbf500d95b6c7e85c7c07aa48147c6cdd9defbe4`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f867e1babe5c47998841c28bded391ef496d71feb54b61f4545d87f5a646cba`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:41db50f6cc4d9bfd6ec2c46f419eed60136e695a19f5892004fc8e16f9e4c958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacd6b789756bea2927e2e1131c952cd3ad9c48cb279eb3eb6303fc9ab294d2f`

```dockerfile
```

-	Layers:
	-	`sha256:5e30d67018b50219cf111359b9c01c0f494e08d2b3f8569dcc5fd3c1ee5c1d73`  
		Last Modified: Tue, 02 Jun 2026 19:03:38 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:ad14dda00ccf242342a93cc85db34a56bb25d3e296ecdace5147c1966b5b3b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10247947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec25b1ccdde1f720071b74505ffdf00e039ab69a2fd75f71d020027bd2c0a7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:04:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9df1ef32961e68a3939cd854cdbbf23eadb85878e7a2924c8e8b55ed686db`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 7.0 MB (7021143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3a2252f7f49291e414a088e7d5d7d5b1ed30e39570d7aaaddefe72ad7ec45`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8f706a5b129742a751a90778c239816e2f65e8da796265eea974d0684885fe`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:37cb5f4f11c03e9635452373f12b4933fd563eb9d9b579fa4d81074c310b783b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8831237e5b1eb42138b1b533eac461905370c52864faa74ad64aa64ee6929ea9`

```dockerfile
```

-	Layers:
	-	`sha256:8b0c0c197e4c11be4cea42928534aba725c08e8453c25ec9bc3b3d17f826cd06`  
		Last Modified: Tue, 02 Jun 2026 19:04:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:611c3dbd05ff98e9f9f562b4ecc89822c2b0367847d932a4932c1ed966bc9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10792301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849a4b2095da890cb3d5ca21aa5d61d37c4ca5fd0cde2e2037c3552e8b346140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:05:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0967f1732be2cea3277e46b05ada1d6dc6dc0c9d759046c2618be783fee259b3`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.6 MB (6649438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b729dba32d18e040f985909e362d966b7bdd5bb98293da5c5b092b2db7b1ad6c`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bd385b5d9562cba05d122624afc347bf04e331b1039428b62bfa34329ae6fc`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:83650089aa5af8edeacd31f9575f51c4865f49f4658f5e4783da1893cbd73665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ea3db6409708bdb914b77d4ccc8d0aeb240671d5247e30d10994a292bed6a`

```dockerfile
```

-	Layers:
	-	`sha256:0e0bb2fa8f0c108b876e46f52d13f30f36c80387b8275abc10d23d94c3c159f2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:03cac3b8dd8dfa41d75112c2ae5b94fec0af6f5814730e5330012354cf7f0827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447bf89722c6586ace97b811cfa21359201cf2f9713c5e1fef6213a7acc2650e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:09:21 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:09:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:09:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a55d0eaca97f0390033ffa8d9134bc7a0079525bf40c87025873115014fab03`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.7 MB (6712091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e475251befa77978ceea2dd486692601fdf578dc6cf93f6f34db105424faa429`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd101bdee386ea23d9751c471412ed9d61e7b3bb95fa9c4c09dcf11b393862b0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:878c6cd3e6ca2b63e8e7c9012c4a51e6f964a8e1f17a510c05f7000a2ee3c3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b43654f9754af02840c24097bead60f9bda1a56f0d0331c1cdb97492d058d1d`

```dockerfile
```

-	Layers:
	-	`sha256:277a9558e629945d4f89fbecb1fece232afa05343087d445fab71410b96445a5`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:841b7ad0b071063eab531f42992071e88a18027757dc688943e9b6be84f30b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10758432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8d5496bf4f8dc7bc2e68a44462403d27657a08420f26e155ef56c4b875cd1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:06:58 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='15fd0c3438e7178e5316e63be68373ad581c8d78db26e649113aa303b74e5e58' ;;     armhf) natsArch='arm6'; sha256='1c2a2b9c52d9232b58ce092ba093c46c5da6f47b1ce9b1342e3ae9465de6e758' ;;     armv7) natsArch='arm7'; sha256='6bc20a6f439d72f71dae981ffe3430197eb6e64c0d2c6000b4b4b105904fbd3c' ;;     x86_64) natsArch='amd64'; sha256='b3e7b14eb10c895fd90c2dacdb6b65bd3208adcc9524dd7689ba2c1024e6b97a' ;;     x86) natsArch='386'; sha256='654a79c090daa27dc9bc638c09e28cb0bdbed5b24e075608357b475367d47edb' ;;     s390x) natsArch='s390x'; sha256='acb6081c49e101119fb35a3cb2d77e7970440e968583c61aedf6e64e4f5023d3' ;;     ppc64le) natsArch='ppc64le'; sha256='05733a36a22ece31a23059147fbb7a9b27bb86e9770ffb1b6ba7478603b75330' ;;     loong64) natsArch='loong64'; sha256='0a31d33cc3430ec9f2b51f789afee4a21fb5d28447d52c661acfd9ea46f5d7fb' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:06:58 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:06:58 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9e1c021cb6668546fbd3caeb13392781503722c1117940072299d8a401f78`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 7.1 MB (7103589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7207403655133bcd046b16235270ff4b177f4e43d2903766cfb7a82d247e914`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107699ca626db0b1dca70dd8b094467bb9da6bad2e7b07a3e817e656f0528716`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d93ecdc48d72d516e5b6b434a8f943f9a0a356ea2e81c18a79d46fa97dac3cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e2b39405c34660d72439c24d374ad63c17ff6072b7967c16a05e3d681f075e`

```dockerfile
```

-	Layers:
	-	`sha256:73ea22818eaf35e7185adc8c19baf720eec4e2f32f9e2f8eefc0ae10f85ea059`  
		Last Modified: Tue, 02 Jun 2026 19:07:06 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:771149b0d90eca2137d24c8d205521fec157e38510f2b46e9fc370e54ae4262f
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
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
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
$ docker pull nats@sha256:d6519b375b05bc720d5a10240e23ecec1fcb559f2d48b9d13fe6408331a52e7a
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
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
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
$ docker pull nats@sha256:d6519b375b05bc720d5a10240e23ecec1fcb559f2d48b9d13fe6408331a52e7a
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
$ docker pull nats@sha256:5944d914891fd8995813c3ffc74e7d24d904a433c9e24dec22a3e399099f5a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6838181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980935de25535451a6667c56db36effe6337feefdc20bf25fbe7c1474d86dc61`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2d4994951dfb170eaa33c29ae96625d4d628d0d2be3520f9ffabe13131199649`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.8 MB (6837672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2515e56d45aed1e0d93235479d1dc7c653c83afe0e0c853cddc785afa7458f9`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a3c486cfdfa007385b5a199ab67e01e9350ea946c9c792545fbb91df9e73907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2bb5b536f5f43b26105c737c248d986e1184c282201ff705afd9f35017a6fd`

```dockerfile
```

-	Layers:
	-	`sha256:302938c243b992315e2496c34c70d4a985cca567c413f4266f6d34ee07c8d667`  
		Last Modified: Tue, 02 Jun 2026 19:07:14 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9ba7e88b90b597424b711a3dae0d0cf6a9de4549bfdeb99179427c731ccea61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6575841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8621bc56fc94685c7a1421900ee5a6d91d10a65c756d7622bb724c13b53481b1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:06:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:06:55 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:06:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:06:55 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:06:55 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0ece34849fb2fe161531b2aa23f49f651d08e6b538d055ae13608fc03e9fa664`  
		Last Modified: Tue, 02 Jun 2026 16:09:49 GMT  
		Size: 6.6 MB (6575331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c4ff68ebef1a8fde2778609c5458fbc9c64e2b570c36ee3739b618575ce0e`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:475e0a7afe9bee0662f1b7b0cbc11c0dade66b1e39ce5dafa24a8801494c3066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad5cc5866d0a6de9315e88fe48fc867687ed33661af65a90f5cbc4c9b820c74`

```dockerfile
```

-	Layers:
	-	`sha256:687cd737e82798bcb38af14f283166d19b21bb55c5a458173863357c86f6ee72`  
		Last Modified: Tue, 02 Jun 2026 19:06:59 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:2ae1d5ceca19e1c69e973566bf5be106779096df023d52885e4a356988ea118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6567436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33294f65cb3fcbe6c9ea314f08a17a19884676642dcef1e579b2ada89317268b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:54 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:54 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c11fb5ecdb03b4b9888bf3079fbf1715c482d1c6f95ff8287a2482b076f1011c`  
		Last Modified: Tue, 02 Jun 2026 16:09:48 GMT  
		Size: 6.6 MB (6566927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cd8a1a29373426a964a844fe1b46766fff43403c82b13a6630cc3c7dabbd91`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b7cc2bfd0899cca9c29676160a6a902fc9e261066f0fbed96a774de02a01ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0458111063e5d5644f364f56445f377998520df0a8db9175631174e45ab413`

```dockerfile
```

-	Layers:
	-	`sha256:a81d950cfd6029cfc68649c687e46d7a189097db506dd5d0b17accdab6cb77ca`  
		Last Modified: Tue, 02 Jun 2026 19:07:58 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:c36a4de088d69daa5f6e7a85fe6929c15ab31e2ccb77d93ce4d68ad80833696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6190835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308344e5cc3b557286ba217429eb714263ea5e93e1faaf71cb7c8dfee7d64be1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:24 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b8a235a7bedcb372707120ddf7a57a7e8e913ce5d4aa5f887cdc999160ee08d0`  
		Last Modified: Tue, 02 Jun 2026 16:09:47 GMT  
		Size: 6.2 MB (6190325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f221fb6b7b5d1897556ab5bbc261d53a256b2b732ea7a0ede30b9a4f9148410`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7f137158c0632bc59017307a598abf5713efc9b4f519aaff6e0ef89d94c777d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7128bb8703819d81c4d464409991636d5637213e5d58f6192f2d8b524bd2728c`

```dockerfile
```

-	Layers:
	-	`sha256:07888ee89127b382df75e88cb29b925869c42c3ff2483ebefafd11011628d738`  
		Last Modified: Tue, 02 Jun 2026 19:07:28 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:c1676737ef02364110b94f9decd587566bf61ebfad79a6c336ee5e52bfeb3c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d161756d4514909692560828cbd3e096881ce788f23f6dfbd1059ad0a9753711`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:28add1390642a18c406c4bd7b6a2502aa2d3eee6af1b637bb20acd8f2181882b`  
		Last Modified: Tue, 02 Jun 2026 16:09:52 GMT  
		Size: 6.3 MB (6254548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8421315da2d27925303852459e4818afdefed6ff83b0eaa149ae9e58ffb3ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6863115086fbbbf714599e20d91598385f4d53a85a9d68ba745714a498ff51e1`

```dockerfile
```

-	Layers:
	-	`sha256:3e597b389935011087771fd20b432b4a10257716a20b52aca4a24075c37ae202`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:1c3f4e4be95991c21cb0c1be5a78e804138bd7c6a4a2a4ec0809ae47e54cbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6651706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c1d8148727b2be5b0c9cc31fcc9970c55dc867b67331276d24e22b99b86df`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce7cc5b528715399273308d58cf16e20e55359559238d29b05bff1fa68b102a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.7 MB (6651197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b670bd58d739026226b929729de4512c7575fb3cc4fd2e73cb2251c0ddd12770`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7340b5bf9a21150e3230ea95028e2b7404d654f9ab14a7d6a4b6fbadc4ab98bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b305fa2032ba50fee9cffd30b8f0eeecb9780e7a8314b5aca9648b2bdec169`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d234634fb982ff4cfb44a5b64ed5afb9635850ce8c6ac0112664e1274906a`  
		Last Modified: Tue, 02 Jun 2026 20:09:34 GMT  
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
