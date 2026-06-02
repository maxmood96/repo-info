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
-	[`nats:2.12.10`](#nats21210)
-	[`nats:2.12.10-alpine`](#nats21210-alpine)
-	[`nats:2.12.10-alpine3.22`](#nats21210-alpine322)
-	[`nats:2.12.10-linux`](#nats21210-linux)
-	[`nats:2.12.10-nanoserver`](#nats21210-nanoserver)
-	[`nats:2.12.10-nanoserver-ltsc2022`](#nats21210-nanoserver-ltsc2022)
-	[`nats:2.12.10-scratch`](#nats21210-scratch)
-	[`nats:2.12.10-windowsservercore`](#nats21210-windowsservercore)
-	[`nats:2.12.10-windowsservercore-ltsc2022`](#nats21210-windowsservercore-ltsc2022)
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
$ docker pull nats@sha256:a927133972a521a5b75cf8b85a336faeba2f13c000883122fbea1ffb45117f00
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
	-	windows version 10.0.20348.5139; amd64

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

### `nats:2` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
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
$ docker pull nats@sha256:cf022b2587f311e12ed65fe889c8bba19e90917216b0a4d822d642780af4ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:cf022b2587f311e12ed65fe889c8bba19e90917216b0a4d822d642780af4ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
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
$ docker pull nats@sha256:8b2a59ae57dabb40a530adeb549ffea14e796eb0bd68bc15a409f07e475ef4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:a25b38871b87a691f7c5c90cfa83f4d5437e88f040de6348cbf95733ba375ef1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ec1a6204be33c8779d1a1fcf3ab70fffb3bb380e02f6d1a3f84d2b8acb1bd0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:07:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:07:32 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:07:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:07:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:07:38 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 02 Jun 2026 19:07:40 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 02 Jun 2026 19:08:48 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:09:18 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:09:19 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:09:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:09:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8fbbec164e39825e72121dbf863209aaee281bb23d82eef45fb1b78af49bd`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5ccc46ac0cd69fc7e5f3ba3187243d7191826c5c174d7d1a9bdf7e37437430`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3be6447ed8966ff4760ab36a8f65bde11ddb128890296ca784007be596571`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0a04302c8e00c75114f3a2244ff5f034702d2bd875699c15d6aa753d729d94`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b68571adc336abfdc2b191feccc656c90c865b349c3419f6d4ca6392defa2`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755e2e1bb5b7b315f0510306d019a8ee93d6cba431bfe70f2fde14f269625d9`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8f4cf7f1be61cbdf08314357d2af1b7b697606166b30d6e09ad275f8c29a41`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 503.2 KB (503180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614768606c9a6a992dc318e3eedb9a3985d9320f1503b7b5001d9a916880349c`  
		Last Modified: Tue, 02 Jun 2026 19:09:25 GMT  
		Size: 7.4 MB (7396537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698093e1cf89fed3786ae358d5758de15cc759aaf437f55e51155301c09d115`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5276da588ba1823566c8e1634c157a72c38c9dbaab53122d796fb3207e83e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba365b70485c1a2db1e0c6856a41d0a634ba9ef55bd72ebd8b86f5e617508ede`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f660cf8c8ababe39a2710f184cc802c5ab5f133180075efd69d6ce35116e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:8b2a59ae57dabb40a530adeb549ffea14e796eb0bd68bc15a409f07e475ef4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:a25b38871b87a691f7c5c90cfa83f4d5437e88f040de6348cbf95733ba375ef1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ec1a6204be33c8779d1a1fcf3ab70fffb3bb380e02f6d1a3f84d2b8acb1bd0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:07:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:07:32 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:07:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:07:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:07:38 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 02 Jun 2026 19:07:40 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 02 Jun 2026 19:08:48 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:09:18 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:09:19 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:09:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:09:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8fbbec164e39825e72121dbf863209aaee281bb23d82eef45fb1b78af49bd`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5ccc46ac0cd69fc7e5f3ba3187243d7191826c5c174d7d1a9bdf7e37437430`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3be6447ed8966ff4760ab36a8f65bde11ddb128890296ca784007be596571`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0a04302c8e00c75114f3a2244ff5f034702d2bd875699c15d6aa753d729d94`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b68571adc336abfdc2b191feccc656c90c865b349c3419f6d4ca6392defa2`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755e2e1bb5b7b315f0510306d019a8ee93d6cba431bfe70f2fde14f269625d9`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8f4cf7f1be61cbdf08314357d2af1b7b697606166b30d6e09ad275f8c29a41`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 503.2 KB (503180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614768606c9a6a992dc318e3eedb9a3985d9320f1503b7b5001d9a916880349c`  
		Last Modified: Tue, 02 Jun 2026 19:09:25 GMT  
		Size: 7.4 MB (7396537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698093e1cf89fed3786ae358d5758de15cc759aaf437f55e51155301c09d115`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5276da588ba1823566c8e1634c157a72c38c9dbaab53122d796fb3207e83e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba365b70485c1a2db1e0c6856a41d0a634ba9ef55bd72ebd8b86f5e617508ede`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f660cf8c8ababe39a2710f184cc802c5ab5f133180075efd69d6ce35116e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12`

```console
$ docker pull nats@sha256:6c60db6746553c9a86cab6a0d72ce0772a318f6417520a2beacfa1cb6b5986f2
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
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12` - linux; amd64

```console
$ docker pull nats@sha256:8f28add5adb2c153256365636995d46fffa3f455dd57916c5f5f44714a305858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9799735f1f22a5ef57b31811ced6c4f81e53d54c8fda87eb1f4ca947ef998f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:18876dec4809be37458cff00f8e609069bd2bca761fb9ff09d5ff55e4184fba6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.6 MB (6643045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526ac1282a815254b3a1c2171453acd91c6dcc71f318c957c30c38cd035708eb`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:3506de968aab2c118e28f72b93ba6ed9984fae0a9c5bdb715336a3936347c208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195e9157f8ee09eba5827e2e9d4481c5347c9dd1c11ccd5f9135ed00eb37a27b`

```dockerfile
```

-	Layers:
	-	`sha256:0a15b99f76c0e857698c9cee49eea3ced2be9b606745f84acd4d48572f987d40`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:da17edc25803163cc03963704e7ebab5c85b815ae265df079f4d045949e76a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6385068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb2fe854f9e7821858066bfaf805c886cba17b44d0b64a1fa5511b183026d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1586e60a87db9483b365d693a94b0b9cd3803cb7f52b48560987019068a329a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6384558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44500101993883e121350f8921138f8b1c9cf39ddf412af5505fa541a3d35ca9`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:5c1283cfcbfb95d1bc6b8ca84a7573c3cf6c87429730fcc3fd5af598ea8612ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23afe236cd7885a2774b3aa87cd5dd0fbc9201b3d5881c9d440bb0207c118f9`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c431e32d44f3c647e12216db04bf78ca1c9b14a9119f886c5bfca084ad735`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:44505405acbedad03a5637d260b7c30e7bdf0bf3d50802d173859fcd8c877520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e02520e814643d7f0f37fa895e96942017e180847d8eddfb878a30c359dc4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed1ac3486c0dcc3fc243c07ea0d6cdcd8716854a98eecad524b2136405ebd2bc`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6373738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f3a4573412756753725e126d3b14ef49a9f937f6081ccd19971d2f8067c2e`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:d31fc95b7ad0f517999b64d4c030925cf5808f3c47b88f7d52808306128e5630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76eccbe3089b6e4625fb083728b1b8b91c6ef1e2fcbe0658f39dd424836d358`

```dockerfile
```

-	Layers:
	-	`sha256:d90856043232f7c9b3a179afc84bd48dacd9cf89e4f3993fc7934b74ac63a3ef`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0a81414fa2e078caeb7277143e838ed4f32d30aaf3ac570f671e53e21401c33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fddd30775b8b14b05708079c292fccd3992de07db9e7b19e2bfd21eb3be130`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:20 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d84c246082513a8061f42ff8da49cf789adc5eca7b95c90f1435d9a790c1f956`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.0 MB (6038460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c854d3de40b230b8b79acba47de6c4f7dc44bc42e694fd6c33ed4e8998c7bb`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:d7429c60e2ea6329f712e7e7b4f4a1814427351c126d4642f45ac52ac58fe8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985687160f5e1c9914e3bfa0397a4c93f0d13e9d366e63350c37a16446b7f4a`

```dockerfile
```

-	Layers:
	-	`sha256:26b9f084e02a8d4df87284ae7b86ab95cedeb50419138ea634c5b931c5ac59a7`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:154faf52f9aa6dc336dd5e8092d45c8070d8b0cc6d58771e07f13bf5ca4809ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e2d2a44e6cf20d3428760385a1aa85b932fede1d97d67c490fc2aa47cc62a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3454618d0a935d4a010dd9b43e1da58d3bfd610b3feaefa9b48d20c69485f1e6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.1 MB (6100313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:2bac0c82b418a6511b818f866ee90a7e6c482b797a310356daa20a0c40c77f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb1133f4e258937c57f36c05732fa70828394cd97e26e02b39d36a6e6448120`

```dockerfile
```

-	Layers:
	-	`sha256:9d50cbc892ad9ef250cf90c5ebb56ecda64204e8cf874cb7e23f751f6ff7d97c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:35c3c0f4522ab2165d0b75281e699fd3ff683d995bf0ff92b70f538604c02671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6492143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9690f17c37a4089ce520485856dda143a30c7db0b59fef9c3a58f48b7482035b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e482136cca5cd8c123ca286e70750a8f330b229161126e636d6c83cd0ea2c425`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.5 MB (6491634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c48e2303a1d5874a06654742c0b7a3a97d9b26de36c73712cc300bb1561a63b`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:9abe171b0531efdf8d5bdd795afec699370d4d4bb9bdefd3712225510db6aaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0bbe5236b40a8f29a66dab24436d1d105edbd85e6a24f5a7daa0d0bada5f0d`

```dockerfile
```

-	Layers:
	-	`sha256:7ef06a887bfdb7c088fa585baca020cd9457ba9be995ba3a5975d23235aa9903`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:39d25793e6d15e19426dd02c4d25ed2c016acecf4b47782673a7ee505cff0e86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133879048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a5ec1c55028a6ab1830e05c5213c02d40a2efce0cf45e6f23b190221a88088`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:35:21 GMT
RUN cmd /S /C #(nop) COPY file:af233a3c76b7394075d0614b7e8ef95f8fa05988355fe0dd0baf86674bb42544 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:35:22 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:35:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:35:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:35:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13dae843293123b4323c3f8c6d8415848ee9c4e91c20bbabc8dfecebadf080`  
		Last Modified: Tue, 02 Jun 2026 20:35:31 GMT  
		Size: 6.8 MB (6834312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18328777d38165b763c1ba80c1239fa3801d7e044755ff389174d2764a1e67e6`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdefc88a8a045c8efee21927672b420a6eca21d364bcd1859e74e9ea987adcd5`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f3dc9ec4372249ff881d6725329a9538241ff329d13620e314478366eb3b8c`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c2177fcb6b2fabee4664f6723e2b6bf098b9318bfd412cf85604661a7e3b82`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-alpine`

```console
$ docker pull nats@sha256:c6d2e1fb8650fdf66871950f4db2e7774b9ef7c3b1fa70dfe6a91b9e7a8ebc58
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
$ docker pull nats@sha256:b6a71c39a6da4501865de58710ad506ca54863899193d14c9297bf62ba2b0a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdd6d682d8b6284360c749088df23cdf9509a692e9e366b63ab7ecc01029ff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:33 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:05:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:05:33 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50e567e81618447703190dd03ff0fbfc29ea0636aed0208f1f319d5fc09a9fe`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 7.1 MB (7099394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080cccc3c11dcdd4d58cd850c5eb8906857178918f8e4a838e8201ef440e067e`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8357a86f315722a84b96104560dda71c40975dcd70325a25bf58a5d1d7f81944`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d9c66e8c9ebcc7d413513c77a9a36017360b04a97b060afa78333a92021db1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2b7f813657ec7d39046bef2d8b6e318c39114dd87d2b11a09a7af92809c783`

```dockerfile
```

-	Layers:
	-	`sha256:fd91acffaaaf5aaa9c1de8365140bd4de901b64f7ef838c075442fe9231f36b1`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:24fabd1ace3e94d33777c8c21bd0f21f19db90a58cdf7506b6045e63f44b9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10349068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f979428138f9a4962ca0d058e90783d3d6108a104e040d47daaa843e98e645f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:12 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:04:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:04:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3b9beeee6b2cdda03605043b6f94aa3252e8feb00c01141cb0c4b49b345d43`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 6.8 MB (6840714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd3c62d9c8719bf0ea83027fcde0cbf46e503cbbc0a5086a1dd55451c9bb1c`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7aae8c2c6bb04cf1c9fb53de42649342114d8cb1013a66f1c7094034cbfffff`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:709083256f1171eb80331d476728ee434b2b61d0390898bcc378639748fc94a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5000a5184456de9d7e4507e173523c636937c778c3d221daa48352a6bccd079b`

```dockerfile
```

-	Layers:
	-	`sha256:f6c98fa2ecdf759ea134966f4f94d6065f23cd469bfdbc2cbcbefc8a82612487`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:4e40162308deb867ff6a0dd79b105ded616633a717f988dacb91b3a53f2a8ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10056507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d8d108ce3a411d9811a37ce1b3c0c10932fef92501ff6eefa634538c6637ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:39 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:04:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:04:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728db8261941933d3a5cda8733191001036f08899a8d5390c2b9b7f02d59515`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 6.8 MB (6829704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6aaad7a52c96fd3ef62f1cdcacca8b7ec8a482e545aa5fe07a6bee4b16155f`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370d589826d9bc2d844e163401f62cf426fab3ed1a0da3fea0f16f6ed0862722`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5517a0095cb172531654d3283a04387c4f18470903c1bf6de302dc2d126d53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c3742f8ee6b06e626c5d0441ba6572d46086ffb6a7d360e217945489760230`

```dockerfile
```

-	Layers:
	-	`sha256:e151cac18f43d265ce732639a74574f0f66646f22c8375ec9b36e8b93d874d46`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b24c6b53fe130f3db79d4b20c4bfd4a5247539609bf9d8cdd7d167542e59d13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59905f63e78167267ae2548bfe131014e12bf660b7140109a6782671113eee00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:15 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:05:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:05:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5096975bf83abc79906ab4cfc59e4f7f8bfa7b9daae475c41cc31ccc0f706ad`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.5 MB (6499689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c4e6ae269d83563f8a6225ef681795404fdc7d3da82a93b5e387a02ba27ee2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec58bdc0ac9f532b14b5248200c7c5549830c07bb5d613171213d12e163377`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d7758bf81d1c2d99924aa3f1af785f8ac7f291d57e84e035d020a6114c658623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc20e97bf4135fec24ee963330e503ad7fe350b866e39e244ba8d8d3f57377f3`

```dockerfile
```

-	Layers:
	-	`sha256:ef8ad22eeb896c1a4cc1f5df9ea1ebb5bb6eb9210cae42cf9a93e2b915fe9e99`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:5dabc754392627ede15b35418d6d166f0e56c7feda224fd608a9498257649457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaf1140775061510f37bf1ebd82d5c2833b74c07ea2fabdce53ab554e6a760f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
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
	-	`sha256:fd07068adc97d358d1a12b48d6887d82ff42b85b826d1dc69304c634a2ee1d63`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.6 MB (6558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ccd2a146afb568eafbbb0af864dc45794d7a9962d4610e221e0f7113a2f3f`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882bef0d916deb554db3cec0a7b4fa4c130d8c54a8bfb7fe68388f0b62faac0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8216949f6f4ceb57e47a4ad0b91208c9b03c0521a6f39541c4e24ece3d6138b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f554bbc5b02d68cba8cbaba8483441396b2c8f8d0dea21d294d9c1b4f225f29`

```dockerfile
```

-	Layers:
	-	`sha256:39721e27270f525a4cf26d3881cae5d136191b0e9660db3b9cd2bcd75f8db4e9`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:398cbf61cd15d7ccf8f58247701e570a0b799bfb24b8bc78f2a00fc6941ed509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc6640cc6ad1b5e1318db5445f725e5300ba8c1f5dedbda1255cb1f23c5beaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:07:13 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:07:13 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:07:13 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e441093b19c2a00099623f697942f9396c0b58bb230d1694af84cab04a776df`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 7.0 MB (6950130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaff9c69f271e332ab9ddbccf67ddc7638d59e45ff000e82202b79796ab96f3`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929db5398d72a74b4338564fbf5668be5c7e3295108928aa3ec19d8efc5e455c`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6e272c47431d08d28e44b4576b20a89f70fc77bea4408a296c8dc60b873a176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b321483fe3a7d44b76a93990c758028511e923f0b262033e8bafe62727320e`

```dockerfile
```

-	Layers:
	-	`sha256:33b8f885a3469c6fa2c3419632ba8cbd562507eb4f6f616358b606e1f3433633`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:c6d2e1fb8650fdf66871950f4db2e7774b9ef7c3b1fa70dfe6a91b9e7a8ebc58
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
$ docker pull nats@sha256:b6a71c39a6da4501865de58710ad506ca54863899193d14c9297bf62ba2b0a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdd6d682d8b6284360c749088df23cdf9509a692e9e366b63ab7ecc01029ff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:33 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:05:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:05:33 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50e567e81618447703190dd03ff0fbfc29ea0636aed0208f1f319d5fc09a9fe`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 7.1 MB (7099394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080cccc3c11dcdd4d58cd850c5eb8906857178918f8e4a838e8201ef440e067e`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8357a86f315722a84b96104560dda71c40975dcd70325a25bf58a5d1d7f81944`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d9c66e8c9ebcc7d413513c77a9a36017360b04a97b060afa78333a92021db1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2b7f813657ec7d39046bef2d8b6e318c39114dd87d2b11a09a7af92809c783`

```dockerfile
```

-	Layers:
	-	`sha256:fd91acffaaaf5aaa9c1de8365140bd4de901b64f7ef838c075442fe9231f36b1`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:24fabd1ace3e94d33777c8c21bd0f21f19db90a58cdf7506b6045e63f44b9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10349068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f979428138f9a4962ca0d058e90783d3d6108a104e040d47daaa843e98e645f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:12 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:04:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:04:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3b9beeee6b2cdda03605043b6f94aa3252e8feb00c01141cb0c4b49b345d43`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 6.8 MB (6840714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd3c62d9c8719bf0ea83027fcde0cbf46e503cbbc0a5086a1dd55451c9bb1c`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7aae8c2c6bb04cf1c9fb53de42649342114d8cb1013a66f1c7094034cbfffff`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:709083256f1171eb80331d476728ee434b2b61d0390898bcc378639748fc94a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5000a5184456de9d7e4507e173523c636937c778c3d221daa48352a6bccd079b`

```dockerfile
```

-	Layers:
	-	`sha256:f6c98fa2ecdf759ea134966f4f94d6065f23cd469bfdbc2cbcbefc8a82612487`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:4e40162308deb867ff6a0dd79b105ded616633a717f988dacb91b3a53f2a8ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10056507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d8d108ce3a411d9811a37ce1b3c0c10932fef92501ff6eefa634538c6637ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:39 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:04:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:04:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728db8261941933d3a5cda8733191001036f08899a8d5390c2b9b7f02d59515`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 6.8 MB (6829704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6aaad7a52c96fd3ef62f1cdcacca8b7ec8a482e545aa5fe07a6bee4b16155f`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370d589826d9bc2d844e163401f62cf426fab3ed1a0da3fea0f16f6ed0862722`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5517a0095cb172531654d3283a04387c4f18470903c1bf6de302dc2d126d53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c3742f8ee6b06e626c5d0441ba6572d46086ffb6a7d360e217945489760230`

```dockerfile
```

-	Layers:
	-	`sha256:e151cac18f43d265ce732639a74574f0f66646f22c8375ec9b36e8b93d874d46`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b24c6b53fe130f3db79d4b20c4bfd4a5247539609bf9d8cdd7d167542e59d13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59905f63e78167267ae2548bfe131014e12bf660b7140109a6782671113eee00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:15 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:05:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:05:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5096975bf83abc79906ab4cfc59e4f7f8bfa7b9daae475c41cc31ccc0f706ad`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.5 MB (6499689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c4e6ae269d83563f8a6225ef681795404fdc7d3da82a93b5e387a02ba27ee2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec58bdc0ac9f532b14b5248200c7c5549830c07bb5d613171213d12e163377`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d7758bf81d1c2d99924aa3f1af785f8ac7f291d57e84e035d020a6114c658623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc20e97bf4135fec24ee963330e503ad7fe350b866e39e244ba8d8d3f57377f3`

```dockerfile
```

-	Layers:
	-	`sha256:ef8ad22eeb896c1a4cc1f5df9ea1ebb5bb6eb9210cae42cf9a93e2b915fe9e99`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:5dabc754392627ede15b35418d6d166f0e56c7feda224fd608a9498257649457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaf1140775061510f37bf1ebd82d5c2833b74c07ea2fabdce53ab554e6a760f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
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
	-	`sha256:fd07068adc97d358d1a12b48d6887d82ff42b85b826d1dc69304c634a2ee1d63`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.6 MB (6558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ccd2a146afb568eafbbb0af864dc45794d7a9962d4610e221e0f7113a2f3f`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882bef0d916deb554db3cec0a7b4fa4c130d8c54a8bfb7fe68388f0b62faac0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8216949f6f4ceb57e47a4ad0b91208c9b03c0521a6f39541c4e24ece3d6138b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f554bbc5b02d68cba8cbaba8483441396b2c8f8d0dea21d294d9c1b4f225f29`

```dockerfile
```

-	Layers:
	-	`sha256:39721e27270f525a4cf26d3881cae5d136191b0e9660db3b9cd2bcd75f8db4e9`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:398cbf61cd15d7ccf8f58247701e570a0b799bfb24b8bc78f2a00fc6941ed509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc6640cc6ad1b5e1318db5445f725e5300ba8c1f5dedbda1255cb1f23c5beaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:07:13 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:07:13 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:07:13 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e441093b19c2a00099623f697942f9396c0b58bb230d1694af84cab04a776df`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 7.0 MB (6950130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaff9c69f271e332ab9ddbccf67ddc7638d59e45ff000e82202b79796ab96f3`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929db5398d72a74b4338564fbf5668be5c7e3295108928aa3ec19d8efc5e455c`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6e272c47431d08d28e44b4576b20a89f70fc77bea4408a296c8dc60b873a176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b321483fe3a7d44b76a93990c758028511e923f0b262033e8bafe62727320e`

```dockerfile
```

-	Layers:
	-	`sha256:33b8f885a3469c6fa2c3419632ba8cbd562507eb4f6f616358b606e1f3433633`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:8c348ddd2df457decc824d39fc41cfd21133e60d048738073f33841e5272f872
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
$ docker pull nats@sha256:8f28add5adb2c153256365636995d46fffa3f455dd57916c5f5f44714a305858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9799735f1f22a5ef57b31811ced6c4f81e53d54c8fda87eb1f4ca947ef998f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:18876dec4809be37458cff00f8e609069bd2bca761fb9ff09d5ff55e4184fba6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.6 MB (6643045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526ac1282a815254b3a1c2171453acd91c6dcc71f318c957c30c38cd035708eb`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:3506de968aab2c118e28f72b93ba6ed9984fae0a9c5bdb715336a3936347c208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195e9157f8ee09eba5827e2e9d4481c5347c9dd1c11ccd5f9135ed00eb37a27b`

```dockerfile
```

-	Layers:
	-	`sha256:0a15b99f76c0e857698c9cee49eea3ced2be9b606745f84acd4d48572f987d40`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:da17edc25803163cc03963704e7ebab5c85b815ae265df079f4d045949e76a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6385068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb2fe854f9e7821858066bfaf805c886cba17b44d0b64a1fa5511b183026d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1586e60a87db9483b365d693a94b0b9cd3803cb7f52b48560987019068a329a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6384558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44500101993883e121350f8921138f8b1c9cf39ddf412af5505fa541a3d35ca9`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5c1283cfcbfb95d1bc6b8ca84a7573c3cf6c87429730fcc3fd5af598ea8612ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23afe236cd7885a2774b3aa87cd5dd0fbc9201b3d5881c9d440bb0207c118f9`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c431e32d44f3c647e12216db04bf78ca1c9b14a9119f886c5bfca084ad735`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:44505405acbedad03a5637d260b7c30e7bdf0bf3d50802d173859fcd8c877520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e02520e814643d7f0f37fa895e96942017e180847d8eddfb878a30c359dc4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed1ac3486c0dcc3fc243c07ea0d6cdcd8716854a98eecad524b2136405ebd2bc`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6373738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f3a4573412756753725e126d3b14ef49a9f937f6081ccd19971d2f8067c2e`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d31fc95b7ad0f517999b64d4c030925cf5808f3c47b88f7d52808306128e5630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76eccbe3089b6e4625fb083728b1b8b91c6ef1e2fcbe0658f39dd424836d358`

```dockerfile
```

-	Layers:
	-	`sha256:d90856043232f7c9b3a179afc84bd48dacd9cf89e4f3993fc7934b74ac63a3ef`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0a81414fa2e078caeb7277143e838ed4f32d30aaf3ac570f671e53e21401c33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fddd30775b8b14b05708079c292fccd3992de07db9e7b19e2bfd21eb3be130`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:20 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d84c246082513a8061f42ff8da49cf789adc5eca7b95c90f1435d9a790c1f956`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.0 MB (6038460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c854d3de40b230b8b79acba47de6c4f7dc44bc42e694fd6c33ed4e8998c7bb`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d7429c60e2ea6329f712e7e7b4f4a1814427351c126d4642f45ac52ac58fe8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985687160f5e1c9914e3bfa0397a4c93f0d13e9d366e63350c37a16446b7f4a`

```dockerfile
```

-	Layers:
	-	`sha256:26b9f084e02a8d4df87284ae7b86ab95cedeb50419138ea634c5b931c5ac59a7`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:154faf52f9aa6dc336dd5e8092d45c8070d8b0cc6d58771e07f13bf5ca4809ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e2d2a44e6cf20d3428760385a1aa85b932fede1d97d67c490fc2aa47cc62a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3454618d0a935d4a010dd9b43e1da58d3bfd610b3feaefa9b48d20c69485f1e6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.1 MB (6100313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2bac0c82b418a6511b818f866ee90a7e6c482b797a310356daa20a0c40c77f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb1133f4e258937c57f36c05732fa70828394cd97e26e02b39d36a6e6448120`

```dockerfile
```

-	Layers:
	-	`sha256:9d50cbc892ad9ef250cf90c5ebb56ecda64204e8cf874cb7e23f751f6ff7d97c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:35c3c0f4522ab2165d0b75281e699fd3ff683d995bf0ff92b70f538604c02671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6492143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9690f17c37a4089ce520485856dda143a30c7db0b59fef9c3a58f48b7482035b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e482136cca5cd8c123ca286e70750a8f330b229161126e636d6c83cd0ea2c425`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.5 MB (6491634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c48e2303a1d5874a06654742c0b7a3a97d9b26de36c73712cc300bb1561a63b`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9abe171b0531efdf8d5bdd795afec699370d4d4bb9bdefd3712225510db6aaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0bbe5236b40a8f29a66dab24436d1d105edbd85e6a24f5a7daa0d0bada5f0d`

```dockerfile
```

-	Layers:
	-	`sha256:7ef06a887bfdb7c088fa585baca020cd9457ba9be995ba3a5975d23235aa9903`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-nanoserver`

```console
$ docker pull nats@sha256:47fdbe945bea70d139e9bfddf9f962c2a8fae7ba08a4fc8a709312223484ca75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:39d25793e6d15e19426dd02c4d25ed2c016acecf4b47782673a7ee505cff0e86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133879048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a5ec1c55028a6ab1830e05c5213c02d40a2efce0cf45e6f23b190221a88088`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:35:21 GMT
RUN cmd /S /C #(nop) COPY file:af233a3c76b7394075d0614b7e8ef95f8fa05988355fe0dd0baf86674bb42544 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:35:22 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:35:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:35:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:35:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13dae843293123b4323c3f8c6d8415848ee9c4e91c20bbabc8dfecebadf080`  
		Last Modified: Tue, 02 Jun 2026 20:35:31 GMT  
		Size: 6.8 MB (6834312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18328777d38165b763c1ba80c1239fa3801d7e044755ff389174d2764a1e67e6`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdefc88a8a045c8efee21927672b420a6eca21d364bcd1859e74e9ea987adcd5`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f3dc9ec4372249ff881d6725329a9538241ff329d13620e314478366eb3b8c`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c2177fcb6b2fabee4664f6723e2b6bf098b9318bfd412cf85604661a7e3b82`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:47fdbe945bea70d139e9bfddf9f962c2a8fae7ba08a4fc8a709312223484ca75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:39d25793e6d15e19426dd02c4d25ed2c016acecf4b47782673a7ee505cff0e86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133879048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a5ec1c55028a6ab1830e05c5213c02d40a2efce0cf45e6f23b190221a88088`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:35:21 GMT
RUN cmd /S /C #(nop) COPY file:af233a3c76b7394075d0614b7e8ef95f8fa05988355fe0dd0baf86674bb42544 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:35:22 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:35:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:35:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:35:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13dae843293123b4323c3f8c6d8415848ee9c4e91c20bbabc8dfecebadf080`  
		Last Modified: Tue, 02 Jun 2026 20:35:31 GMT  
		Size: 6.8 MB (6834312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18328777d38165b763c1ba80c1239fa3801d7e044755ff389174d2764a1e67e6`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdefc88a8a045c8efee21927672b420a6eca21d364bcd1859e74e9ea987adcd5`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f3dc9ec4372249ff881d6725329a9538241ff329d13620e314478366eb3b8c`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c2177fcb6b2fabee4664f6723e2b6bf098b9318bfd412cf85604661a7e3b82`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-scratch`

```console
$ docker pull nats@sha256:8c348ddd2df457decc824d39fc41cfd21133e60d048738073f33841e5272f872
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
$ docker pull nats@sha256:8f28add5adb2c153256365636995d46fffa3f455dd57916c5f5f44714a305858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9799735f1f22a5ef57b31811ced6c4f81e53d54c8fda87eb1f4ca947ef998f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:18876dec4809be37458cff00f8e609069bd2bca761fb9ff09d5ff55e4184fba6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.6 MB (6643045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526ac1282a815254b3a1c2171453acd91c6dcc71f318c957c30c38cd035708eb`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3506de968aab2c118e28f72b93ba6ed9984fae0a9c5bdb715336a3936347c208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195e9157f8ee09eba5827e2e9d4481c5347c9dd1c11ccd5f9135ed00eb37a27b`

```dockerfile
```

-	Layers:
	-	`sha256:0a15b99f76c0e857698c9cee49eea3ced2be9b606745f84acd4d48572f987d40`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:da17edc25803163cc03963704e7ebab5c85b815ae265df079f4d045949e76a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6385068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb2fe854f9e7821858066bfaf805c886cba17b44d0b64a1fa5511b183026d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1586e60a87db9483b365d693a94b0b9cd3803cb7f52b48560987019068a329a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6384558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44500101993883e121350f8921138f8b1c9cf39ddf412af5505fa541a3d35ca9`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5c1283cfcbfb95d1bc6b8ca84a7573c3cf6c87429730fcc3fd5af598ea8612ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23afe236cd7885a2774b3aa87cd5dd0fbc9201b3d5881c9d440bb0207c118f9`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c431e32d44f3c647e12216db04bf78ca1c9b14a9119f886c5bfca084ad735`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:44505405acbedad03a5637d260b7c30e7bdf0bf3d50802d173859fcd8c877520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e02520e814643d7f0f37fa895e96942017e180847d8eddfb878a30c359dc4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed1ac3486c0dcc3fc243c07ea0d6cdcd8716854a98eecad524b2136405ebd2bc`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6373738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f3a4573412756753725e126d3b14ef49a9f937f6081ccd19971d2f8067c2e`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d31fc95b7ad0f517999b64d4c030925cf5808f3c47b88f7d52808306128e5630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76eccbe3089b6e4625fb083728b1b8b91c6ef1e2fcbe0658f39dd424836d358`

```dockerfile
```

-	Layers:
	-	`sha256:d90856043232f7c9b3a179afc84bd48dacd9cf89e4f3993fc7934b74ac63a3ef`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0a81414fa2e078caeb7277143e838ed4f32d30aaf3ac570f671e53e21401c33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fddd30775b8b14b05708079c292fccd3992de07db9e7b19e2bfd21eb3be130`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:20 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d84c246082513a8061f42ff8da49cf789adc5eca7b95c90f1435d9a790c1f956`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.0 MB (6038460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c854d3de40b230b8b79acba47de6c4f7dc44bc42e694fd6c33ed4e8998c7bb`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d7429c60e2ea6329f712e7e7b4f4a1814427351c126d4642f45ac52ac58fe8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985687160f5e1c9914e3bfa0397a4c93f0d13e9d366e63350c37a16446b7f4a`

```dockerfile
```

-	Layers:
	-	`sha256:26b9f084e02a8d4df87284ae7b86ab95cedeb50419138ea634c5b931c5ac59a7`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:154faf52f9aa6dc336dd5e8092d45c8070d8b0cc6d58771e07f13bf5ca4809ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e2d2a44e6cf20d3428760385a1aa85b932fede1d97d67c490fc2aa47cc62a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3454618d0a935d4a010dd9b43e1da58d3bfd610b3feaefa9b48d20c69485f1e6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.1 MB (6100313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2bac0c82b418a6511b818f866ee90a7e6c482b797a310356daa20a0c40c77f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb1133f4e258937c57f36c05732fa70828394cd97e26e02b39d36a6e6448120`

```dockerfile
```

-	Layers:
	-	`sha256:9d50cbc892ad9ef250cf90c5ebb56ecda64204e8cf874cb7e23f751f6ff7d97c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:35c3c0f4522ab2165d0b75281e699fd3ff683d995bf0ff92b70f538604c02671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6492143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9690f17c37a4089ce520485856dda143a30c7db0b59fef9c3a58f48b7482035b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e482136cca5cd8c123ca286e70750a8f330b229161126e636d6c83cd0ea2c425`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.5 MB (6491634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c48e2303a1d5874a06654742c0b7a3a97d9b26de36c73712cc300bb1561a63b`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9abe171b0531efdf8d5bdd795afec699370d4d4bb9bdefd3712225510db6aaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0bbe5236b40a8f29a66dab24436d1d105edbd85e6a24f5a7daa0d0bada5f0d`

```dockerfile
```

-	Layers:
	-	`sha256:7ef06a887bfdb7c088fa585baca020cd9457ba9be995ba3a5975d23235aa9903`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-windowsservercore`

```console
$ docker pull nats@sha256:bb6798ada732a526995b99c1ae7d55d154ddf6c720e1a25ee4c3d088446e06ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:800df5574a09300dd6439b0792a71cfc4405c3e5f095ee4d873947ab46630cc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130133721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2c9c4f34689d6d1449d9214517543a667847441322a9b9bc73dbb497febe45`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:10:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:10:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:10:41 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:10:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:10:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.10/nats-server-v2.12.10-windows-amd64.zip
# Tue, 02 Jun 2026 19:10:46 GMT
ENV NATS_SERVER_SHASUM=ab1a922f702fd44f1b372649155e13424f8c5b4a707bfa3db67525b46bbbaa08
# Tue, 02 Jun 2026 19:11:59 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:12:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:12:30 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:12:31 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:12:31 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:12:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff96a4ee3207d43902ba75954aa26e1ec02a16b3b716b64af6800356f0fa52`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92d038a54a3d29459f7ac9f048f7ad12ace2ca5d2b6c23d34feed128e7d335d`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebfbaff32e4140b8ddbbcfe714ac8ec46adecbbb4191be9b43746f5a9c4817d`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a80d907dc0a5cd45989b454969c1b7bb7fe5500f9d5b81d1bb063e900b4fa3f`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4732e1a64aeeb0f480495a8eb00ebbe7037cd95e134de10438a06c53501be5`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b873ec1d307eba90a6c8f595bb797c20028d3cbeee6e8a9c77005b53225bc8f3`  
		Last Modified: Tue, 02 Jun 2026 19:12:38 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe8654ee0292d6a4cb19b7760366e62dcfb45bea2e36524bd6d8811312cb262`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 503.0 KB (503027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01995e1b5d9b8d3e5134c8f9616b44bd473849058d3154a07a3c1406d27641d0`  
		Last Modified: Tue, 02 Jun 2026 19:12:41 GMT  
		Size: 7.2 MB (7196437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f98cf05a59ef999617c9fabfb2b7d721ef3d594e80eb6007e5bcec9d8c5312`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07e63af72ef52e0017d589c5b1f0165d7b54fb49d60f4cc21804d930862cdc3`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986f168c6501abbbe72ea31c71e1e911f46977f0cc57b9d3ae65a584cada1e9e`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eb2579dbe2d320d0b26cbae0928b3e97d81fa05756a5111593885eca6228d3`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:bb6798ada732a526995b99c1ae7d55d154ddf6c720e1a25ee4c3d088446e06ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:800df5574a09300dd6439b0792a71cfc4405c3e5f095ee4d873947ab46630cc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130133721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2c9c4f34689d6d1449d9214517543a667847441322a9b9bc73dbb497febe45`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:10:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:10:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:10:41 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:10:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:10:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.10/nats-server-v2.12.10-windows-amd64.zip
# Tue, 02 Jun 2026 19:10:46 GMT
ENV NATS_SERVER_SHASUM=ab1a922f702fd44f1b372649155e13424f8c5b4a707bfa3db67525b46bbbaa08
# Tue, 02 Jun 2026 19:11:59 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:12:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:12:30 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:12:31 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:12:31 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:12:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff96a4ee3207d43902ba75954aa26e1ec02a16b3b716b64af6800356f0fa52`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92d038a54a3d29459f7ac9f048f7ad12ace2ca5d2b6c23d34feed128e7d335d`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebfbaff32e4140b8ddbbcfe714ac8ec46adecbbb4191be9b43746f5a9c4817d`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a80d907dc0a5cd45989b454969c1b7bb7fe5500f9d5b81d1bb063e900b4fa3f`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4732e1a64aeeb0f480495a8eb00ebbe7037cd95e134de10438a06c53501be5`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b873ec1d307eba90a6c8f595bb797c20028d3cbeee6e8a9c77005b53225bc8f3`  
		Last Modified: Tue, 02 Jun 2026 19:12:38 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe8654ee0292d6a4cb19b7760366e62dcfb45bea2e36524bd6d8811312cb262`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 503.0 KB (503027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01995e1b5d9b8d3e5134c8f9616b44bd473849058d3154a07a3c1406d27641d0`  
		Last Modified: Tue, 02 Jun 2026 19:12:41 GMT  
		Size: 7.2 MB (7196437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f98cf05a59ef999617c9fabfb2b7d721ef3d594e80eb6007e5bcec9d8c5312`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07e63af72ef52e0017d589c5b1f0165d7b54fb49d60f4cc21804d930862cdc3`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986f168c6501abbbe72ea31c71e1e911f46977f0cc57b9d3ae65a584cada1e9e`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eb2579dbe2d320d0b26cbae0928b3e97d81fa05756a5111593885eca6228d3`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.10`

```console
$ docker pull nats@sha256:6c60db6746553c9a86cab6a0d72ce0772a318f6417520a2beacfa1cb6b5986f2
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
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.10` - linux; amd64

```console
$ docker pull nats@sha256:8f28add5adb2c153256365636995d46fffa3f455dd57916c5f5f44714a305858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9799735f1f22a5ef57b31811ced6c4f81e53d54c8fda87eb1f4ca947ef998f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:18876dec4809be37458cff00f8e609069bd2bca761fb9ff09d5ff55e4184fba6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.6 MB (6643045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526ac1282a815254b3a1c2171453acd91c6dcc71f318c957c30c38cd035708eb`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10` - unknown; unknown

```console
$ docker pull nats@sha256:3506de968aab2c118e28f72b93ba6ed9984fae0a9c5bdb715336a3936347c208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195e9157f8ee09eba5827e2e9d4481c5347c9dd1c11ccd5f9135ed00eb37a27b`

```dockerfile
```

-	Layers:
	-	`sha256:0a15b99f76c0e857698c9cee49eea3ced2be9b606745f84acd4d48572f987d40`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:da17edc25803163cc03963704e7ebab5c85b815ae265df079f4d045949e76a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6385068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb2fe854f9e7821858066bfaf805c886cba17b44d0b64a1fa5511b183026d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1586e60a87db9483b365d693a94b0b9cd3803cb7f52b48560987019068a329a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6384558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44500101993883e121350f8921138f8b1c9cf39ddf412af5505fa541a3d35ca9`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10` - unknown; unknown

```console
$ docker pull nats@sha256:5c1283cfcbfb95d1bc6b8ca84a7573c3cf6c87429730fcc3fd5af598ea8612ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23afe236cd7885a2774b3aa87cd5dd0fbc9201b3d5881c9d440bb0207c118f9`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c431e32d44f3c647e12216db04bf78ca1c9b14a9119f886c5bfca084ad735`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:44505405acbedad03a5637d260b7c30e7bdf0bf3d50802d173859fcd8c877520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e02520e814643d7f0f37fa895e96942017e180847d8eddfb878a30c359dc4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed1ac3486c0dcc3fc243c07ea0d6cdcd8716854a98eecad524b2136405ebd2bc`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6373738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f3a4573412756753725e126d3b14ef49a9f937f6081ccd19971d2f8067c2e`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10` - unknown; unknown

```console
$ docker pull nats@sha256:d31fc95b7ad0f517999b64d4c030925cf5808f3c47b88f7d52808306128e5630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76eccbe3089b6e4625fb083728b1b8b91c6ef1e2fcbe0658f39dd424836d358`

```dockerfile
```

-	Layers:
	-	`sha256:d90856043232f7c9b3a179afc84bd48dacd9cf89e4f3993fc7934b74ac63a3ef`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0a81414fa2e078caeb7277143e838ed4f32d30aaf3ac570f671e53e21401c33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fddd30775b8b14b05708079c292fccd3992de07db9e7b19e2bfd21eb3be130`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:20 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d84c246082513a8061f42ff8da49cf789adc5eca7b95c90f1435d9a790c1f956`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.0 MB (6038460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c854d3de40b230b8b79acba47de6c4f7dc44bc42e694fd6c33ed4e8998c7bb`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10` - unknown; unknown

```console
$ docker pull nats@sha256:d7429c60e2ea6329f712e7e7b4f4a1814427351c126d4642f45ac52ac58fe8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985687160f5e1c9914e3bfa0397a4c93f0d13e9d366e63350c37a16446b7f4a`

```dockerfile
```

-	Layers:
	-	`sha256:26b9f084e02a8d4df87284ae7b86ab95cedeb50419138ea634c5b931c5ac59a7`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10` - linux; ppc64le

```console
$ docker pull nats@sha256:154faf52f9aa6dc336dd5e8092d45c8070d8b0cc6d58771e07f13bf5ca4809ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e2d2a44e6cf20d3428760385a1aa85b932fede1d97d67c490fc2aa47cc62a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3454618d0a935d4a010dd9b43e1da58d3bfd610b3feaefa9b48d20c69485f1e6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.1 MB (6100313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10` - unknown; unknown

```console
$ docker pull nats@sha256:2bac0c82b418a6511b818f866ee90a7e6c482b797a310356daa20a0c40c77f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb1133f4e258937c57f36c05732fa70828394cd97e26e02b39d36a6e6448120`

```dockerfile
```

-	Layers:
	-	`sha256:9d50cbc892ad9ef250cf90c5ebb56ecda64204e8cf874cb7e23f751f6ff7d97c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10` - linux; s390x

```console
$ docker pull nats@sha256:35c3c0f4522ab2165d0b75281e699fd3ff683d995bf0ff92b70f538604c02671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6492143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9690f17c37a4089ce520485856dda143a30c7db0b59fef9c3a58f48b7482035b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e482136cca5cd8c123ca286e70750a8f330b229161126e636d6c83cd0ea2c425`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.5 MB (6491634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c48e2303a1d5874a06654742c0b7a3a97d9b26de36c73712cc300bb1561a63b`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10` - unknown; unknown

```console
$ docker pull nats@sha256:9abe171b0531efdf8d5bdd795afec699370d4d4bb9bdefd3712225510db6aaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0bbe5236b40a8f29a66dab24436d1d105edbd85e6a24f5a7daa0d0bada5f0d`

```dockerfile
```

-	Layers:
	-	`sha256:7ef06a887bfdb7c088fa585baca020cd9457ba9be995ba3a5975d23235aa9903`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:39d25793e6d15e19426dd02c4d25ed2c016acecf4b47782673a7ee505cff0e86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133879048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a5ec1c55028a6ab1830e05c5213c02d40a2efce0cf45e6f23b190221a88088`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:35:21 GMT
RUN cmd /S /C #(nop) COPY file:af233a3c76b7394075d0614b7e8ef95f8fa05988355fe0dd0baf86674bb42544 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:35:22 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:35:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:35:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:35:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13dae843293123b4323c3f8c6d8415848ee9c4e91c20bbabc8dfecebadf080`  
		Last Modified: Tue, 02 Jun 2026 20:35:31 GMT  
		Size: 6.8 MB (6834312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18328777d38165b763c1ba80c1239fa3801d7e044755ff389174d2764a1e67e6`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdefc88a8a045c8efee21927672b420a6eca21d364bcd1859e74e9ea987adcd5`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f3dc9ec4372249ff881d6725329a9538241ff329d13620e314478366eb3b8c`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c2177fcb6b2fabee4664f6723e2b6bf098b9318bfd412cf85604661a7e3b82`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.10-alpine`

```console
$ docker pull nats@sha256:c6d2e1fb8650fdf66871950f4db2e7774b9ef7c3b1fa70dfe6a91b9e7a8ebc58
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

### `nats:2.12.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:b6a71c39a6da4501865de58710ad506ca54863899193d14c9297bf62ba2b0a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdd6d682d8b6284360c749088df23cdf9509a692e9e366b63ab7ecc01029ff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:33 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:05:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:05:33 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50e567e81618447703190dd03ff0fbfc29ea0636aed0208f1f319d5fc09a9fe`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 7.1 MB (7099394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080cccc3c11dcdd4d58cd850c5eb8906857178918f8e4a838e8201ef440e067e`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8357a86f315722a84b96104560dda71c40975dcd70325a25bf58a5d1d7f81944`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d9c66e8c9ebcc7d413513c77a9a36017360b04a97b060afa78333a92021db1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2b7f813657ec7d39046bef2d8b6e318c39114dd87d2b11a09a7af92809c783`

```dockerfile
```

-	Layers:
	-	`sha256:fd91acffaaaf5aaa9c1de8365140bd4de901b64f7ef838c075442fe9231f36b1`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:24fabd1ace3e94d33777c8c21bd0f21f19db90a58cdf7506b6045e63f44b9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10349068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f979428138f9a4962ca0d058e90783d3d6108a104e040d47daaa843e98e645f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:12 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:04:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:04:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3b9beeee6b2cdda03605043b6f94aa3252e8feb00c01141cb0c4b49b345d43`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 6.8 MB (6840714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd3c62d9c8719bf0ea83027fcde0cbf46e503cbbc0a5086a1dd55451c9bb1c`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7aae8c2c6bb04cf1c9fb53de42649342114d8cb1013a66f1c7094034cbfffff`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:709083256f1171eb80331d476728ee434b2b61d0390898bcc378639748fc94a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5000a5184456de9d7e4507e173523c636937c778c3d221daa48352a6bccd079b`

```dockerfile
```

-	Layers:
	-	`sha256:f6c98fa2ecdf759ea134966f4f94d6065f23cd469bfdbc2cbcbefc8a82612487`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:4e40162308deb867ff6a0dd79b105ded616633a717f988dacb91b3a53f2a8ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10056507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d8d108ce3a411d9811a37ce1b3c0c10932fef92501ff6eefa634538c6637ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:39 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:04:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:04:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728db8261941933d3a5cda8733191001036f08899a8d5390c2b9b7f02d59515`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 6.8 MB (6829704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6aaad7a52c96fd3ef62f1cdcacca8b7ec8a482e545aa5fe07a6bee4b16155f`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370d589826d9bc2d844e163401f62cf426fab3ed1a0da3fea0f16f6ed0862722`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5517a0095cb172531654d3283a04387c4f18470903c1bf6de302dc2d126d53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c3742f8ee6b06e626c5d0441ba6572d46086ffb6a7d360e217945489760230`

```dockerfile
```

-	Layers:
	-	`sha256:e151cac18f43d265ce732639a74574f0f66646f22c8375ec9b36e8b93d874d46`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b24c6b53fe130f3db79d4b20c4bfd4a5247539609bf9d8cdd7d167542e59d13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59905f63e78167267ae2548bfe131014e12bf660b7140109a6782671113eee00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:15 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:05:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:05:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5096975bf83abc79906ab4cfc59e4f7f8bfa7b9daae475c41cc31ccc0f706ad`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.5 MB (6499689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c4e6ae269d83563f8a6225ef681795404fdc7d3da82a93b5e387a02ba27ee2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec58bdc0ac9f532b14b5248200c7c5549830c07bb5d613171213d12e163377`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d7758bf81d1c2d99924aa3f1af785f8ac7f291d57e84e035d020a6114c658623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc20e97bf4135fec24ee963330e503ad7fe350b866e39e244ba8d8d3f57377f3`

```dockerfile
```

-	Layers:
	-	`sha256:ef8ad22eeb896c1a4cc1f5df9ea1ebb5bb6eb9210cae42cf9a93e2b915fe9e99`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:5dabc754392627ede15b35418d6d166f0e56c7feda224fd608a9498257649457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaf1140775061510f37bf1ebd82d5c2833b74c07ea2fabdce53ab554e6a760f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
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
	-	`sha256:fd07068adc97d358d1a12b48d6887d82ff42b85b826d1dc69304c634a2ee1d63`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.6 MB (6558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ccd2a146afb568eafbbb0af864dc45794d7a9962d4610e221e0f7113a2f3f`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882bef0d916deb554db3cec0a7b4fa4c130d8c54a8bfb7fe68388f0b62faac0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8216949f6f4ceb57e47a4ad0b91208c9b03c0521a6f39541c4e24ece3d6138b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f554bbc5b02d68cba8cbaba8483441396b2c8f8d0dea21d294d9c1b4f225f29`

```dockerfile
```

-	Layers:
	-	`sha256:39721e27270f525a4cf26d3881cae5d136191b0e9660db3b9cd2bcd75f8db4e9`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:398cbf61cd15d7ccf8f58247701e570a0b799bfb24b8bc78f2a00fc6941ed509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc6640cc6ad1b5e1318db5445f725e5300ba8c1f5dedbda1255cb1f23c5beaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:07:13 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:07:13 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:07:13 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e441093b19c2a00099623f697942f9396c0b58bb230d1694af84cab04a776df`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 7.0 MB (6950130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaff9c69f271e332ab9ddbccf67ddc7638d59e45ff000e82202b79796ab96f3`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929db5398d72a74b4338564fbf5668be5c7e3295108928aa3ec19d8efc5e455c`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6e272c47431d08d28e44b4576b20a89f70fc77bea4408a296c8dc60b873a176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b321483fe3a7d44b76a93990c758028511e923f0b262033e8bafe62727320e`

```dockerfile
```

-	Layers:
	-	`sha256:33b8f885a3469c6fa2c3419632ba8cbd562507eb4f6f616358b606e1f3433633`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.10-alpine3.22`

```console
$ docker pull nats@sha256:c6d2e1fb8650fdf66871950f4db2e7774b9ef7c3b1fa70dfe6a91b9e7a8ebc58
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

### `nats:2.12.10-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:b6a71c39a6da4501865de58710ad506ca54863899193d14c9297bf62ba2b0a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10908556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdd6d682d8b6284360c749088df23cdf9509a692e9e366b63ab7ecc01029ff0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:33 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:05:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:05:33 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50e567e81618447703190dd03ff0fbfc29ea0636aed0208f1f319d5fc09a9fe`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 7.1 MB (7099394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080cccc3c11dcdd4d58cd850c5eb8906857178918f8e4a838e8201ef440e067e`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8357a86f315722a84b96104560dda71c40975dcd70325a25bf58a5d1d7f81944`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d9c66e8c9ebcc7d413513c77a9a36017360b04a97b060afa78333a92021db1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2b7f813657ec7d39046bef2d8b6e318c39114dd87d2b11a09a7af92809c783`

```dockerfile
```

-	Layers:
	-	`sha256:fd91acffaaaf5aaa9c1de8365140bd4de901b64f7ef838c075442fe9231f36b1`  
		Last Modified: Tue, 02 Jun 2026 19:05:37 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:24fabd1ace3e94d33777c8c21bd0f21f19db90a58cdf7506b6045e63f44b9d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10349068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f979428138f9a4962ca0d058e90783d3d6108a104e040d47daaa843e98e645f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:12 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:04:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:04:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3b9beeee6b2cdda03605043b6f94aa3252e8feb00c01141cb0c4b49b345d43`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 6.8 MB (6840714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd3c62d9c8719bf0ea83027fcde0cbf46e503cbbc0a5086a1dd55451c9bb1c`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7aae8c2c6bb04cf1c9fb53de42649342114d8cb1013a66f1c7094034cbfffff`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:709083256f1171eb80331d476728ee434b2b61d0390898bcc378639748fc94a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5000a5184456de9d7e4507e173523c636937c778c3d221daa48352a6bccd079b`

```dockerfile
```

-	Layers:
	-	`sha256:f6c98fa2ecdf759ea134966f4f94d6065f23cd469bfdbc2cbcbefc8a82612487`  
		Last Modified: Tue, 02 Jun 2026 19:04:17 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:4e40162308deb867ff6a0dd79b105ded616633a717f988dacb91b3a53f2a8ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10056507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d8d108ce3a411d9811a37ce1b3c0c10932fef92501ff6eefa634538c6637ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:39 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:04:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:04:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:04:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:04:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728db8261941933d3a5cda8733191001036f08899a8d5390c2b9b7f02d59515`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 6.8 MB (6829704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6aaad7a52c96fd3ef62f1cdcacca8b7ec8a482e545aa5fe07a6bee4b16155f`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370d589826d9bc2d844e163401f62cf426fab3ed1a0da3fea0f16f6ed0862722`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5517a0095cb172531654d3283a04387c4f18470903c1bf6de302dc2d126d53ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c3742f8ee6b06e626c5d0441ba6572d46086ffb6a7d360e217945489760230`

```dockerfile
```

-	Layers:
	-	`sha256:e151cac18f43d265ce732639a74574f0f66646f22c8375ec9b36e8b93d874d46`  
		Last Modified: Tue, 02 Jun 2026 19:04:43 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b24c6b53fe130f3db79d4b20c4bfd4a5247539609bf9d8cdd7d167542e59d13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10642552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59905f63e78167267ae2548bfe131014e12bf660b7140109a6782671113eee00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:05:15 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:05:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:05:15 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:05:15 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:05:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:05:15 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5096975bf83abc79906ab4cfc59e4f7f8bfa7b9daae475c41cc31ccc0f706ad`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 6.5 MB (6499689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c4e6ae269d83563f8a6225ef681795404fdc7d3da82a93b5e387a02ba27ee2`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec58bdc0ac9f532b14b5248200c7c5549830c07bb5d613171213d12e163377`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d7758bf81d1c2d99924aa3f1af785f8ac7f291d57e84e035d020a6114c658623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc20e97bf4135fec24ee963330e503ad7fe350b866e39e244ba8d8d3f57377f3`

```dockerfile
```

-	Layers:
	-	`sha256:ef8ad22eeb896c1a4cc1f5df9ea1ebb5bb6eb9210cae42cf9a93e2b915fe9e99`  
		Last Modified: Tue, 02 Jun 2026 19:05:19 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:5dabc754392627ede15b35418d6d166f0e56c7feda224fd608a9498257649457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaf1140775061510f37bf1ebd82d5c2833b74c07ea2fabdce53ab554e6a760f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:09:21 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:09:21 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:09:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
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
	-	`sha256:fd07068adc97d358d1a12b48d6887d82ff42b85b826d1dc69304c634a2ee1d63`  
		Last Modified: Tue, 02 Jun 2026 19:09:30 GMT  
		Size: 6.6 MB (6558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ccd2a146afb568eafbbb0af864dc45794d7a9962d4610e221e0f7113a2f3f`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7882bef0d916deb554db3cec0a7b4fa4c130d8c54a8bfb7fe68388f0b62faac0`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8216949f6f4ceb57e47a4ad0b91208c9b03c0521a6f39541c4e24ece3d6138b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f554bbc5b02d68cba8cbaba8483441396b2c8f8d0dea21d294d9c1b4f225f29`

```dockerfile
```

-	Layers:
	-	`sha256:39721e27270f525a4cf26d3881cae5d136191b0e9660db3b9cd2bcd75f8db4e9`  
		Last Modified: Tue, 02 Jun 2026 19:09:29 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:398cbf61cd15d7ccf8f58247701e570a0b799bfb24b8bc78f2a00fc6941ed509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc6640cc6ad1b5e1318db5445f725e5300ba8c1f5dedbda1255cb1f23c5beaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:07:13 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:07:13 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:07:13 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='33503268e1c2ef81a6b6f7c7b7d04ba74ded7072b57cc7e32b2bcefe73954e18' ;;     armhf) natsArch='arm6'; sha256='0564238518580288e49778b54aed7b348f4bf4a23ae45a817780eca955e48018' ;;     armv7) natsArch='arm7'; sha256='cd37c5a380c5764367e9f48378aa9c2db2d8b56ec625f546df3c2b24ac4302ad' ;;     x86_64) natsArch='amd64'; sha256='fd361ae17787e279c8262ea456dad0b1de3b0d3d7f9e94725fa3098626490dcf' ;;     x86) natsArch='386'; sha256='51433f2d42fbf1ace6a59a7df3f4ff367683053959496664a0f476c8a148f67f' ;;     s390x) natsArch='s390x'; sha256='ba62c43fd9946d0de2aa58ce07b656afa44a54594396f4b49343dc05b2b4ccce' ;;     ppc64le) natsArch='ppc64le'; sha256='44b5e25037e3187fe1a686da375d4fdfa7b074db77928e2865fe28c7d76227d3' ;;     loong64) natsArch='loong64'; sha256='f4f928d19e886f7521b22595ba9c4cf1391291f3945d123b8f026f3568b01504' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 02 Jun 2026 19:07:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 19:07:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e441093b19c2a00099623f697942f9396c0b58bb230d1694af84cab04a776df`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 7.0 MB (6950130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaff9c69f271e332ab9ddbccf67ddc7638d59e45ff000e82202b79796ab96f3`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929db5398d72a74b4338564fbf5668be5c7e3295108928aa3ec19d8efc5e455c`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6e272c47431d08d28e44b4576b20a89f70fc77bea4408a296c8dc60b873a176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b321483fe3a7d44b76a93990c758028511e923f0b262033e8bafe62727320e`

```dockerfile
```

-	Layers:
	-	`sha256:33b8f885a3469c6fa2c3419632ba8cbd562507eb4f6f616358b606e1f3433633`  
		Last Modified: Tue, 02 Jun 2026 19:07:21 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.10-linux`

```console
$ docker pull nats@sha256:8c348ddd2df457decc824d39fc41cfd21133e60d048738073f33841e5272f872
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

### `nats:2.12.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:8f28add5adb2c153256365636995d46fffa3f455dd57916c5f5f44714a305858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9799735f1f22a5ef57b31811ced6c4f81e53d54c8fda87eb1f4ca947ef998f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:18876dec4809be37458cff00f8e609069bd2bca761fb9ff09d5ff55e4184fba6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.6 MB (6643045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526ac1282a815254b3a1c2171453acd91c6dcc71f318c957c30c38cd035708eb`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:3506de968aab2c118e28f72b93ba6ed9984fae0a9c5bdb715336a3936347c208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195e9157f8ee09eba5827e2e9d4481c5347c9dd1c11ccd5f9135ed00eb37a27b`

```dockerfile
```

-	Layers:
	-	`sha256:0a15b99f76c0e857698c9cee49eea3ced2be9b606745f84acd4d48572f987d40`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:da17edc25803163cc03963704e7ebab5c85b815ae265df079f4d045949e76a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6385068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb2fe854f9e7821858066bfaf805c886cba17b44d0b64a1fa5511b183026d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1586e60a87db9483b365d693a94b0b9cd3803cb7f52b48560987019068a329a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6384558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44500101993883e121350f8921138f8b1c9cf39ddf412af5505fa541a3d35ca9`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5c1283cfcbfb95d1bc6b8ca84a7573c3cf6c87429730fcc3fd5af598ea8612ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23afe236cd7885a2774b3aa87cd5dd0fbc9201b3d5881c9d440bb0207c118f9`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c431e32d44f3c647e12216db04bf78ca1c9b14a9119f886c5bfca084ad735`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:44505405acbedad03a5637d260b7c30e7bdf0bf3d50802d173859fcd8c877520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e02520e814643d7f0f37fa895e96942017e180847d8eddfb878a30c359dc4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed1ac3486c0dcc3fc243c07ea0d6cdcd8716854a98eecad524b2136405ebd2bc`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6373738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f3a4573412756753725e126d3b14ef49a9f937f6081ccd19971d2f8067c2e`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d31fc95b7ad0f517999b64d4c030925cf5808f3c47b88f7d52808306128e5630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76eccbe3089b6e4625fb083728b1b8b91c6ef1e2fcbe0658f39dd424836d358`

```dockerfile
```

-	Layers:
	-	`sha256:d90856043232f7c9b3a179afc84bd48dacd9cf89e4f3993fc7934b74ac63a3ef`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0a81414fa2e078caeb7277143e838ed4f32d30aaf3ac570f671e53e21401c33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fddd30775b8b14b05708079c292fccd3992de07db9e7b19e2bfd21eb3be130`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:20 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d84c246082513a8061f42ff8da49cf789adc5eca7b95c90f1435d9a790c1f956`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.0 MB (6038460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c854d3de40b230b8b79acba47de6c4f7dc44bc42e694fd6c33ed4e8998c7bb`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d7429c60e2ea6329f712e7e7b4f4a1814427351c126d4642f45ac52ac58fe8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985687160f5e1c9914e3bfa0397a4c93f0d13e9d366e63350c37a16446b7f4a`

```dockerfile
```

-	Layers:
	-	`sha256:26b9f084e02a8d4df87284ae7b86ab95cedeb50419138ea634c5b931c5ac59a7`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:154faf52f9aa6dc336dd5e8092d45c8070d8b0cc6d58771e07f13bf5ca4809ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e2d2a44e6cf20d3428760385a1aa85b932fede1d97d67c490fc2aa47cc62a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3454618d0a935d4a010dd9b43e1da58d3bfd610b3feaefa9b48d20c69485f1e6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.1 MB (6100313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2bac0c82b418a6511b818f866ee90a7e6c482b797a310356daa20a0c40c77f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb1133f4e258937c57f36c05732fa70828394cd97e26e02b39d36a6e6448120`

```dockerfile
```

-	Layers:
	-	`sha256:9d50cbc892ad9ef250cf90c5ebb56ecda64204e8cf874cb7e23f751f6ff7d97c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:35c3c0f4522ab2165d0b75281e699fd3ff683d995bf0ff92b70f538604c02671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6492143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9690f17c37a4089ce520485856dda143a30c7db0b59fef9c3a58f48b7482035b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e482136cca5cd8c123ca286e70750a8f330b229161126e636d6c83cd0ea2c425`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.5 MB (6491634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c48e2303a1d5874a06654742c0b7a3a97d9b26de36c73712cc300bb1561a63b`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9abe171b0531efdf8d5bdd795afec699370d4d4bb9bdefd3712225510db6aaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0bbe5236b40a8f29a66dab24436d1d105edbd85e6a24f5a7daa0d0bada5f0d`

```dockerfile
```

-	Layers:
	-	`sha256:7ef06a887bfdb7c088fa585baca020cd9457ba9be995ba3a5975d23235aa9903`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.10-nanoserver`

```console
$ docker pull nats@sha256:47fdbe945bea70d139e9bfddf9f962c2a8fae7ba08a4fc8a709312223484ca75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.10-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:39d25793e6d15e19426dd02c4d25ed2c016acecf4b47782673a7ee505cff0e86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133879048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a5ec1c55028a6ab1830e05c5213c02d40a2efce0cf45e6f23b190221a88088`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:35:21 GMT
RUN cmd /S /C #(nop) COPY file:af233a3c76b7394075d0614b7e8ef95f8fa05988355fe0dd0baf86674bb42544 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:35:22 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:35:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:35:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:35:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13dae843293123b4323c3f8c6d8415848ee9c4e91c20bbabc8dfecebadf080`  
		Last Modified: Tue, 02 Jun 2026 20:35:31 GMT  
		Size: 6.8 MB (6834312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18328777d38165b763c1ba80c1239fa3801d7e044755ff389174d2764a1e67e6`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdefc88a8a045c8efee21927672b420a6eca21d364bcd1859e74e9ea987adcd5`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f3dc9ec4372249ff881d6725329a9538241ff329d13620e314478366eb3b8c`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c2177fcb6b2fabee4664f6723e2b6bf098b9318bfd412cf85604661a7e3b82`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.10-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:47fdbe945bea70d139e9bfddf9f962c2a8fae7ba08a4fc8a709312223484ca75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.10-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:39d25793e6d15e19426dd02c4d25ed2c016acecf4b47782673a7ee505cff0e86
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133879048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a5ec1c55028a6ab1830e05c5213c02d40a2efce0cf45e6f23b190221a88088`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:35:21 GMT
RUN cmd /S /C #(nop) COPY file:af233a3c76b7394075d0614b7e8ef95f8fa05988355fe0dd0baf86674bb42544 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:35:22 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:35:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:35:24 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:35:25 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a13dae843293123b4323c3f8c6d8415848ee9c4e91c20bbabc8dfecebadf080`  
		Last Modified: Tue, 02 Jun 2026 20:35:31 GMT  
		Size: 6.8 MB (6834312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18328777d38165b763c1ba80c1239fa3801d7e044755ff389174d2764a1e67e6`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdefc88a8a045c8efee21927672b420a6eca21d364bcd1859e74e9ea987adcd5`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f3dc9ec4372249ff881d6725329a9538241ff329d13620e314478366eb3b8c`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c2177fcb6b2fabee4664f6723e2b6bf098b9318bfd412cf85604661a7e3b82`  
		Last Modified: Tue, 02 Jun 2026 20:35:29 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.10-scratch`

```console
$ docker pull nats@sha256:8c348ddd2df457decc824d39fc41cfd21133e60d048738073f33841e5272f872
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

### `nats:2.12.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:8f28add5adb2c153256365636995d46fffa3f455dd57916c5f5f44714a305858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9799735f1f22a5ef57b31811ced6c4f81e53d54c8fda87eb1f4ca947ef998f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:05 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:05 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:05 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:05 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:18876dec4809be37458cff00f8e609069bd2bca761fb9ff09d5ff55e4184fba6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.6 MB (6643045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526ac1282a815254b3a1c2171453acd91c6dcc71f318c957c30c38cd035708eb`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3506de968aab2c118e28f72b93ba6ed9984fae0a9c5bdb715336a3936347c208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195e9157f8ee09eba5827e2e9d4481c5347c9dd1c11ccd5f9135ed00eb37a27b`

```dockerfile
```

-	Layers:
	-	`sha256:0a15b99f76c0e857698c9cee49eea3ced2be9b606745f84acd4d48572f987d40`  
		Last Modified: Tue, 02 Jun 2026 19:07:09 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:da17edc25803163cc03963704e7ebab5c85b815ae265df079f4d045949e76a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6385068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb2fe854f9e7821858066bfaf805c886cba17b44d0b64a1fa5511b183026d2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1586e60a87db9483b365d693a94b0b9cd3803cb7f52b48560987019068a329a8`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6384558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44500101993883e121350f8921138f8b1c9cf39ddf412af5505fa541a3d35ca9`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5c1283cfcbfb95d1bc6b8ca84a7573c3cf6c87429730fcc3fd5af598ea8612ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23afe236cd7885a2774b3aa87cd5dd0fbc9201b3d5881c9d440bb0207c118f9`

```dockerfile
```

-	Layers:
	-	`sha256:eb9c431e32d44f3c647e12216db04bf78ca1c9b14a9119f886c5bfca084ad735`  
		Last Modified: Tue, 02 Jun 2026 19:07:26 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:44505405acbedad03a5637d260b7c30e7bdf0bf3d50802d173859fcd8c877520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6374246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e02520e814643d7f0f37fa895e96942017e180847d8eddfb878a30c359dc4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ed1ac3486c0dcc3fc243c07ea0d6cdcd8716854a98eecad524b2136405ebd2bc`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.4 MB (6373738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74f3a4573412756753725e126d3b14ef49a9f937f6081ccd19971d2f8067c2e`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d31fc95b7ad0f517999b64d4c030925cf5808f3c47b88f7d52808306128e5630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76eccbe3089b6e4625fb083728b1b8b91c6ef1e2fcbe0658f39dd424836d358`

```dockerfile
```

-	Layers:
	-	`sha256:d90856043232f7c9b3a179afc84bd48dacd9cf89e4f3993fc7934b74ac63a3ef`  
		Last Modified: Tue, 02 Jun 2026 19:07:41 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:0a81414fa2e078caeb7277143e838ed4f32d30aaf3ac570f671e53e21401c33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6038968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fddd30775b8b14b05708079c292fccd3992de07db9e7b19e2bfd21eb3be130`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 19:07:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 19:07:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 19:07:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 19:07:20 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 19:07:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d84c246082513a8061f42ff8da49cf789adc5eca7b95c90f1435d9a790c1f956`  
		Last Modified: Tue, 02 Jun 2026 16:09:53 GMT  
		Size: 6.0 MB (6038460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c854d3de40b230b8b79acba47de6c4f7dc44bc42e694fd6c33ed4e8998c7bb`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d7429c60e2ea6329f712e7e7b4f4a1814427351c126d4642f45ac52ac58fe8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7985687160f5e1c9914e3bfa0397a4c93f0d13e9d366e63350c37a16446b7f4a`

```dockerfile
```

-	Layers:
	-	`sha256:26b9f084e02a8d4df87284ae7b86ab95cedeb50419138ea634c5b931c5ac59a7`  
		Last Modified: Tue, 02 Jun 2026 19:07:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:154faf52f9aa6dc336dd5e8092d45c8070d8b0cc6d58771e07f13bf5ca4809ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6100822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e2d2a44e6cf20d3428760385a1aa85b932fede1d97d67c490fc2aa47cc62a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3454618d0a935d4a010dd9b43e1da58d3bfd610b3feaefa9b48d20c69485f1e6`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.1 MB (6100313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22daa5be8ece75902191f486b79c13f899fc4438f5f169454c5565f2e906e5c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2bac0c82b418a6511b818f866ee90a7e6c482b797a310356daa20a0c40c77f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb1133f4e258937c57f36c05732fa70828394cd97e26e02b39d36a6e6448120`

```dockerfile
```

-	Layers:
	-	`sha256:9d50cbc892ad9ef250cf90c5ebb56ecda64204e8cf874cb7e23f751f6ff7d97c`  
		Last Modified: Tue, 02 Jun 2026 20:09:21 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:35c3c0f4522ab2165d0b75281e699fd3ff683d995bf0ff92b70f538604c02671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6492143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9690f17c37a4089ce520485856dda143a30c7db0b59fef9c3a58f48b7482035b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 02 Jun 2026 20:09:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 02 Jun 2026 20:09:30 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 02 Jun 2026 20:09:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 02 Jun 2026 20:09:30 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 02 Jun 2026 20:09:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e482136cca5cd8c123ca286e70750a8f330b229161126e636d6c83cd0ea2c425`  
		Last Modified: Tue, 02 Jun 2026 16:09:56 GMT  
		Size: 6.5 MB (6491634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c48e2303a1d5874a06654742c0b7a3a97d9b26de36c73712cc300bb1561a63b`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9abe171b0531efdf8d5bdd795afec699370d4d4bb9bdefd3712225510db6aaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0bbe5236b40a8f29a66dab24436d1d105edbd85e6a24f5a7daa0d0bada5f0d`

```dockerfile
```

-	Layers:
	-	`sha256:7ef06a887bfdb7c088fa585baca020cd9457ba9be995ba3a5975d23235aa9903`  
		Last Modified: Tue, 02 Jun 2026 20:09:38 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.10-windowsservercore`

```console
$ docker pull nats@sha256:bb6798ada732a526995b99c1ae7d55d154ddf6c720e1a25ee4c3d088446e06ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.10-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:800df5574a09300dd6439b0792a71cfc4405c3e5f095ee4d873947ab46630cc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130133721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2c9c4f34689d6d1449d9214517543a667847441322a9b9bc73dbb497febe45`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:10:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:10:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:10:41 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:10:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:10:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.10/nats-server-v2.12.10-windows-amd64.zip
# Tue, 02 Jun 2026 19:10:46 GMT
ENV NATS_SERVER_SHASUM=ab1a922f702fd44f1b372649155e13424f8c5b4a707bfa3db67525b46bbbaa08
# Tue, 02 Jun 2026 19:11:59 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:12:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:12:30 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:12:31 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:12:31 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:12:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff96a4ee3207d43902ba75954aa26e1ec02a16b3b716b64af6800356f0fa52`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92d038a54a3d29459f7ac9f048f7ad12ace2ca5d2b6c23d34feed128e7d335d`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebfbaff32e4140b8ddbbcfe714ac8ec46adecbbb4191be9b43746f5a9c4817d`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a80d907dc0a5cd45989b454969c1b7bb7fe5500f9d5b81d1bb063e900b4fa3f`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4732e1a64aeeb0f480495a8eb00ebbe7037cd95e134de10438a06c53501be5`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b873ec1d307eba90a6c8f595bb797c20028d3cbeee6e8a9c77005b53225bc8f3`  
		Last Modified: Tue, 02 Jun 2026 19:12:38 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe8654ee0292d6a4cb19b7760366e62dcfb45bea2e36524bd6d8811312cb262`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 503.0 KB (503027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01995e1b5d9b8d3e5134c8f9616b44bd473849058d3154a07a3c1406d27641d0`  
		Last Modified: Tue, 02 Jun 2026 19:12:41 GMT  
		Size: 7.2 MB (7196437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f98cf05a59ef999617c9fabfb2b7d721ef3d594e80eb6007e5bcec9d8c5312`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07e63af72ef52e0017d589c5b1f0165d7b54fb49d60f4cc21804d930862cdc3`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986f168c6501abbbe72ea31c71e1e911f46977f0cc57b9d3ae65a584cada1e9e`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eb2579dbe2d320d0b26cbae0928b3e97d81fa05756a5111593885eca6228d3`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.10-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:bb6798ada732a526995b99c1ae7d55d154ddf6c720e1a25ee4c3d088446e06ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.12.10-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:800df5574a09300dd6439b0792a71cfc4405c3e5f095ee4d873947ab46630cc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130133721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2c9c4f34689d6d1449d9214517543a667847441322a9b9bc73dbb497febe45`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:10:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:10:40 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:10:41 GMT
ENV NATS_SERVER=2.12.10
# Tue, 02 Jun 2026 19:10:43 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.10
# Tue, 02 Jun 2026 19:10:45 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.10/nats-server-v2.12.10-windows-amd64.zip
# Tue, 02 Jun 2026 19:10:46 GMT
ENV NATS_SERVER_SHASUM=ab1a922f702fd44f1b372649155e13424f8c5b4a707bfa3db67525b46bbbaa08
# Tue, 02 Jun 2026 19:11:59 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:12:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:12:30 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:12:31 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:12:31 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:12:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff96a4ee3207d43902ba75954aa26e1ec02a16b3b716b64af6800356f0fa52`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92d038a54a3d29459f7ac9f048f7ad12ace2ca5d2b6c23d34feed128e7d335d`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebfbaff32e4140b8ddbbcfe714ac8ec46adecbbb4191be9b43746f5a9c4817d`  
		Last Modified: Tue, 02 Jun 2026 19:12:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a80d907dc0a5cd45989b454969c1b7bb7fe5500f9d5b81d1bb063e900b4fa3f`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4732e1a64aeeb0f480495a8eb00ebbe7037cd95e134de10438a06c53501be5`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b873ec1d307eba90a6c8f595bb797c20028d3cbeee6e8a9c77005b53225bc8f3`  
		Last Modified: Tue, 02 Jun 2026 19:12:38 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe8654ee0292d6a4cb19b7760366e62dcfb45bea2e36524bd6d8811312cb262`  
		Last Modified: Tue, 02 Jun 2026 19:12:39 GMT  
		Size: 503.0 KB (503027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01995e1b5d9b8d3e5134c8f9616b44bd473849058d3154a07a3c1406d27641d0`  
		Last Modified: Tue, 02 Jun 2026 19:12:41 GMT  
		Size: 7.2 MB (7196437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f98cf05a59ef999617c9fabfb2b7d721ef3d594e80eb6007e5bcec9d8c5312`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07e63af72ef52e0017d589c5b1f0165d7b54fb49d60f4cc21804d930862cdc3`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986f168c6501abbbe72ea31c71e1e911f46977f0cc57b9d3ae65a584cada1e9e`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eb2579dbe2d320d0b26cbae0928b3e97d81fa05756a5111593885eca6228d3`  
		Last Modified: Tue, 02 Jun 2026 19:12:37 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14`

```console
$ docker pull nats@sha256:a927133972a521a5b75cf8b85a336faeba2f13c000883122fbea1ffb45117f00
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
	-	windows version 10.0.20348.5139; amd64

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

### `nats:2.14` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
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
$ docker pull nats@sha256:cf022b2587f311e12ed65fe889c8bba19e90917216b0a4d822d642780af4ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:cf022b2587f311e12ed65fe889c8bba19e90917216b0a4d822d642780af4ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
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
$ docker pull nats@sha256:8b2a59ae57dabb40a530adeb549ffea14e796eb0bd68bc15a409f07e475ef4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:a25b38871b87a691f7c5c90cfa83f4d5437e88f040de6348cbf95733ba375ef1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ec1a6204be33c8779d1a1fcf3ab70fffb3bb380e02f6d1a3f84d2b8acb1bd0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:07:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:07:32 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:07:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:07:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:07:38 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 02 Jun 2026 19:07:40 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 02 Jun 2026 19:08:48 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:09:18 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:09:19 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:09:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:09:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8fbbec164e39825e72121dbf863209aaee281bb23d82eef45fb1b78af49bd`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5ccc46ac0cd69fc7e5f3ba3187243d7191826c5c174d7d1a9bdf7e37437430`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3be6447ed8966ff4760ab36a8f65bde11ddb128890296ca784007be596571`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0a04302c8e00c75114f3a2244ff5f034702d2bd875699c15d6aa753d729d94`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b68571adc336abfdc2b191feccc656c90c865b349c3419f6d4ca6392defa2`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755e2e1bb5b7b315f0510306d019a8ee93d6cba431bfe70f2fde14f269625d9`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8f4cf7f1be61cbdf08314357d2af1b7b697606166b30d6e09ad275f8c29a41`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 503.2 KB (503180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614768606c9a6a992dc318e3eedb9a3985d9320f1503b7b5001d9a916880349c`  
		Last Modified: Tue, 02 Jun 2026 19:09:25 GMT  
		Size: 7.4 MB (7396537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698093e1cf89fed3786ae358d5758de15cc759aaf437f55e51155301c09d115`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5276da588ba1823566c8e1634c157a72c38c9dbaab53122d796fb3207e83e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba365b70485c1a2db1e0c6856a41d0a634ba9ef55bd72ebd8b86f5e617508ede`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f660cf8c8ababe39a2710f184cc802c5ab5f133180075efd69d6ce35116e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:8b2a59ae57dabb40a530adeb549ffea14e796eb0bd68bc15a409f07e475ef4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:a25b38871b87a691f7c5c90cfa83f4d5437e88f040de6348cbf95733ba375ef1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ec1a6204be33c8779d1a1fcf3ab70fffb3bb380e02f6d1a3f84d2b8acb1bd0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:07:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:07:32 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:07:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:07:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:07:38 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 02 Jun 2026 19:07:40 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 02 Jun 2026 19:08:48 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:09:18 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:09:19 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:09:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:09:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8fbbec164e39825e72121dbf863209aaee281bb23d82eef45fb1b78af49bd`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5ccc46ac0cd69fc7e5f3ba3187243d7191826c5c174d7d1a9bdf7e37437430`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3be6447ed8966ff4760ab36a8f65bde11ddb128890296ca784007be596571`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0a04302c8e00c75114f3a2244ff5f034702d2bd875699c15d6aa753d729d94`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b68571adc336abfdc2b191feccc656c90c865b349c3419f6d4ca6392defa2`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755e2e1bb5b7b315f0510306d019a8ee93d6cba431bfe70f2fde14f269625d9`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8f4cf7f1be61cbdf08314357d2af1b7b697606166b30d6e09ad275f8c29a41`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 503.2 KB (503180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614768606c9a6a992dc318e3eedb9a3985d9320f1503b7b5001d9a916880349c`  
		Last Modified: Tue, 02 Jun 2026 19:09:25 GMT  
		Size: 7.4 MB (7396537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698093e1cf89fed3786ae358d5758de15cc759aaf437f55e51155301c09d115`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5276da588ba1823566c8e1634c157a72c38c9dbaab53122d796fb3207e83e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba365b70485c1a2db1e0c6856a41d0a634ba9ef55bd72ebd8b86f5e617508ede`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f660cf8c8ababe39a2710f184cc802c5ab5f133180075efd69d6ce35116e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.2`

```console
$ docker pull nats@sha256:a927133972a521a5b75cf8b85a336faeba2f13c000883122fbea1ffb45117f00
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
	-	windows version 10.0.20348.5139; amd64

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

### `nats:2.14.2` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
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
$ docker pull nats@sha256:cf022b2587f311e12ed65fe889c8bba19e90917216b0a4d822d642780af4ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.2-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:cf022b2587f311e12ed65fe889c8bba19e90917216b0a4d822d642780af4ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.2-nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
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
$ docker pull nats@sha256:8b2a59ae57dabb40a530adeb549ffea14e796eb0bd68bc15a409f07e475ef4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.2-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:a25b38871b87a691f7c5c90cfa83f4d5437e88f040de6348cbf95733ba375ef1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ec1a6204be33c8779d1a1fcf3ab70fffb3bb380e02f6d1a3f84d2b8acb1bd0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:07:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:07:32 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:07:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:07:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:07:38 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 02 Jun 2026 19:07:40 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 02 Jun 2026 19:08:48 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:09:18 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:09:19 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:09:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:09:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8fbbec164e39825e72121dbf863209aaee281bb23d82eef45fb1b78af49bd`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5ccc46ac0cd69fc7e5f3ba3187243d7191826c5c174d7d1a9bdf7e37437430`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3be6447ed8966ff4760ab36a8f65bde11ddb128890296ca784007be596571`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0a04302c8e00c75114f3a2244ff5f034702d2bd875699c15d6aa753d729d94`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b68571adc336abfdc2b191feccc656c90c865b349c3419f6d4ca6392defa2`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755e2e1bb5b7b315f0510306d019a8ee93d6cba431bfe70f2fde14f269625d9`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8f4cf7f1be61cbdf08314357d2af1b7b697606166b30d6e09ad275f8c29a41`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 503.2 KB (503180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614768606c9a6a992dc318e3eedb9a3985d9320f1503b7b5001d9a916880349c`  
		Last Modified: Tue, 02 Jun 2026 19:09:25 GMT  
		Size: 7.4 MB (7396537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698093e1cf89fed3786ae358d5758de15cc759aaf437f55e51155301c09d115`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5276da588ba1823566c8e1634c157a72c38c9dbaab53122d796fb3207e83e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba365b70485c1a2db1e0c6856a41d0a634ba9ef55bd72ebd8b86f5e617508ede`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f660cf8c8ababe39a2710f184cc802c5ab5f133180075efd69d6ce35116e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:8b2a59ae57dabb40a530adeb549ffea14e796eb0bd68bc15a409f07e475ef4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:2.14.2-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:a25b38871b87a691f7c5c90cfa83f4d5437e88f040de6348cbf95733ba375ef1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ec1a6204be33c8779d1a1fcf3ab70fffb3bb380e02f6d1a3f84d2b8acb1bd0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:07:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:07:32 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:07:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:07:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:07:38 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 02 Jun 2026 19:07:40 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 02 Jun 2026 19:08:48 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:09:18 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:09:19 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:09:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:09:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8fbbec164e39825e72121dbf863209aaee281bb23d82eef45fb1b78af49bd`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5ccc46ac0cd69fc7e5f3ba3187243d7191826c5c174d7d1a9bdf7e37437430`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3be6447ed8966ff4760ab36a8f65bde11ddb128890296ca784007be596571`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0a04302c8e00c75114f3a2244ff5f034702d2bd875699c15d6aa753d729d94`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b68571adc336abfdc2b191feccc656c90c865b349c3419f6d4ca6392defa2`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755e2e1bb5b7b315f0510306d019a8ee93d6cba431bfe70f2fde14f269625d9`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8f4cf7f1be61cbdf08314357d2af1b7b697606166b30d6e09ad275f8c29a41`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 503.2 KB (503180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614768606c9a6a992dc318e3eedb9a3985d9320f1503b7b5001d9a916880349c`  
		Last Modified: Tue, 02 Jun 2026 19:09:25 GMT  
		Size: 7.4 MB (7396537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698093e1cf89fed3786ae358d5758de15cc759aaf437f55e51155301c09d115`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5276da588ba1823566c8e1634c157a72c38c9dbaab53122d796fb3207e83e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba365b70485c1a2db1e0c6856a41d0a634ba9ef55bd72ebd8b86f5e617508ede`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f660cf8c8ababe39a2710f184cc802c5ab5f133180075efd69d6ce35116e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1317 bytes)  
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
$ docker pull nats@sha256:a927133972a521a5b75cf8b85a336faeba2f13c000883122fbea1ffb45117f00
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
	-	windows version 10.0.20348.5139; amd64

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

### `nats:latest` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
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
$ docker pull nats@sha256:cf022b2587f311e12ed65fe889c8bba19e90917216b0a4d822d642780af4ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:cf022b2587f311e12ed65fe889c8bba19e90917216b0a4d822d642780af4ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:9c8306d58db81aec578d8f8608dd1810ec37eb66f313930dfed3705a273340c2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134077717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571ccdd84df318a66a3542be0255e50ed89fac5c31e291eb78a4c6922b1d0f4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 20:34:38 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 20:34:44 GMT
RUN cmd /S /C #(nop) COPY file:c16cf061312cb4f6851a17d8f87c727d98883350da7e2bf57e431d56182f9e21 in C:\nats-server.exe 
# Tue, 02 Jun 2026 20:34:45 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 20:34:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 20:34:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 20:34:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3272d64ab60d004409ba4ff0ccea8c9415691bc41fb66f7d25262c217e25c4`  
		Last Modified: Tue, 02 Jun 2026 20:34:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f1d4b2e0c2a25e116bc2015960c5bd645abc0dc9a5c1fdad16fe10246125`  
		Last Modified: Tue, 02 Jun 2026 20:34:57 GMT  
		Size: 7.0 MB (7032998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37713c173c029f17cecb0bceb3e6215689ce535ee6e61196e8c992cea727b30`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4774382157edcd50dffa50f6191a33311186e63f76eaf805e1152562d40d5`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f1a7ee19b6c413bdd71ab9151c6e9c11f11629e4b2a35b56a9506809a915b9`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67aaa2ffcef89a07cfc26f2bdef42aadccad542aa911fd97f3c755a4d419017`  
		Last Modified: Tue, 02 Jun 2026 20:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
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
$ docker pull nats@sha256:8b2a59ae57dabb40a530adeb549ffea14e796eb0bd68bc15a409f07e475ef4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:a25b38871b87a691f7c5c90cfa83f4d5437e88f040de6348cbf95733ba375ef1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ec1a6204be33c8779d1a1fcf3ab70fffb3bb380e02f6d1a3f84d2b8acb1bd0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:07:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:07:32 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:07:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:07:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:07:38 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 02 Jun 2026 19:07:40 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 02 Jun 2026 19:08:48 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:09:18 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:09:19 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:09:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:09:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8fbbec164e39825e72121dbf863209aaee281bb23d82eef45fb1b78af49bd`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5ccc46ac0cd69fc7e5f3ba3187243d7191826c5c174d7d1a9bdf7e37437430`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3be6447ed8966ff4760ab36a8f65bde11ddb128890296ca784007be596571`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0a04302c8e00c75114f3a2244ff5f034702d2bd875699c15d6aa753d729d94`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b68571adc336abfdc2b191feccc656c90c865b349c3419f6d4ca6392defa2`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755e2e1bb5b7b315f0510306d019a8ee93d6cba431bfe70f2fde14f269625d9`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8f4cf7f1be61cbdf08314357d2af1b7b697606166b30d6e09ad275f8c29a41`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 503.2 KB (503180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614768606c9a6a992dc318e3eedb9a3985d9320f1503b7b5001d9a916880349c`  
		Last Modified: Tue, 02 Jun 2026 19:09:25 GMT  
		Size: 7.4 MB (7396537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698093e1cf89fed3786ae358d5758de15cc759aaf437f55e51155301c09d115`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5276da588ba1823566c8e1634c157a72c38c9dbaab53122d796fb3207e83e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba365b70485c1a2db1e0c6856a41d0a634ba9ef55bd72ebd8b86f5e617508ede`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f660cf8c8ababe39a2710f184cc802c5ab5f133180075efd69d6ce35116e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:8b2a59ae57dabb40a530adeb549ffea14e796eb0bd68bc15a409f07e475ef4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull nats@sha256:a25b38871b87a691f7c5c90cfa83f4d5437e88f040de6348cbf95733ba375ef1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130333999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ec1a6204be33c8779d1a1fcf3ab70fffb3bb380e02f6d1a3f84d2b8acb1bd0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 19:07:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 02 Jun 2026 19:07:32 GMT
ENV NATS_DOCKERIZED=1
# Tue, 02 Jun 2026 19:07:34 GMT
ENV NATS_SERVER=2.14.2
# Tue, 02 Jun 2026 19:07:36 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.2
# Tue, 02 Jun 2026 19:07:38 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.2/nats-server-v2.14.2-windows-amd64.zip
# Tue, 02 Jun 2026 19:07:40 GMT
ENV NATS_SERVER_SHASUM=0ae94fc0626c89e76a95835445e36c8b1b595c00d71690966ad208f5f04392ae
# Tue, 02 Jun 2026 19:08:48 GMT
RUN Set-PSDebug -Trace 2
# Tue, 02 Jun 2026 19:09:18 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 02 Jun 2026 19:09:18 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 02 Jun 2026 19:09:19 GMT
EXPOSE 4222 6222 8222
# Tue, 02 Jun 2026 19:09:19 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 02 Jun 2026 19:09:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e8fbbec164e39825e72121dbf863209aaee281bb23d82eef45fb1b78af49bd`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5ccc46ac0cd69fc7e5f3ba3187243d7191826c5c174d7d1a9bdf7e37437430`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3be6447ed8966ff4760ab36a8f65bde11ddb128890296ca784007be596571`  
		Last Modified: Tue, 02 Jun 2026 19:09:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0a04302c8e00c75114f3a2244ff5f034702d2bd875699c15d6aa753d729d94`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b68571adc336abfdc2b191feccc656c90c865b349c3419f6d4ca6392defa2`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755e2e1bb5b7b315f0510306d019a8ee93d6cba431bfe70f2fde14f269625d9`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8f4cf7f1be61cbdf08314357d2af1b7b697606166b30d6e09ad275f8c29a41`  
		Last Modified: Tue, 02 Jun 2026 19:09:26 GMT  
		Size: 503.2 KB (503180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614768606c9a6a992dc318e3eedb9a3985d9320f1503b7b5001d9a916880349c`  
		Last Modified: Tue, 02 Jun 2026 19:09:25 GMT  
		Size: 7.4 MB (7396537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698093e1cf89fed3786ae358d5758de15cc759aaf437f55e51155301c09d115`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f5276da588ba1823566c8e1634c157a72c38c9dbaab53122d796fb3207e83e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba365b70485c1a2db1e0c6856a41d0a634ba9ef55bd72ebd8b86f5e617508ede`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2450f660cf8c8ababe39a2710f184cc802c5ab5f133180075efd69d6ce35116e`  
		Last Modified: Tue, 02 Jun 2026 19:09:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
