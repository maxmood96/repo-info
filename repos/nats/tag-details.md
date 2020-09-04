<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2.1`](#nats21)
-	[`nats:2.1.8`](#nats218)
-	[`nats:2.1.8-alpine`](#nats218-alpine)
-	[`nats:2.1.8-alpine3.11`](#nats218-alpine311)
-	[`nats:2.1.8-linux`](#nats218-linux)
-	[`nats:2.1.8-nanoserver`](#nats218-nanoserver)
-	[`nats:2.1.8-nanoserver-1809`](#nats218-nanoserver-1809)
-	[`nats:2.1.8-scratch`](#nats218-scratch)
-	[`nats:2.1.8-windowsservercore`](#nats218-windowsservercore)
-	[`nats:2.1.8-windowsservercore-1809`](#nats218-windowsservercore-1809)
-	[`nats:2.1.8-windowsservercore-ltsc2016`](#nats218-windowsservercore-ltsc2016)
-	[`nats:2.1-alpine`](#nats21-alpine)
-	[`nats:2.1-alpine3.11`](#nats21-alpine311)
-	[`nats:2.1-linux`](#nats21-linux)
-	[`nats:2.1-nanoserver`](#nats21-nanoserver)
-	[`nats:2.1-nanoserver-1809`](#nats21-nanoserver-1809)
-	[`nats:2.1-scratch`](#nats21-scratch)
-	[`nats:2.1-windowsservercore`](#nats21-windowsservercore)
-	[`nats:2.1-windowsservercore-1809`](#nats21-windowsservercore-1809)
-	[`nats:2.1-windowsservercore-ltsc2016`](#nats21-windowsservercore-ltsc2016)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.11`](#nats2-alpine311)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.11`](#natsalpine311)
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
$ docker pull nats@sha256:86b28d48aa026c39a3d8b119b2dd56089d501c147727f5d5ed7a000a18cbb262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1397; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:6aace730d886f9719841c60ec11f826e494b8fcc631378b32f5e01ca32d87ab9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e93a56bc1852bb18d91f1741edde016c59b49c92f7ad91960d583ee0486ebf3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 09:47:58 GMT
COPY file:27ab63fb5115ca3cb7456a256d6d6dab7ba864d8806821652fbe569f4f845df5 in /nats-server 
# Sat, 16 May 2020 09:47:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 09:47:59 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 09:47:59 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 09:47:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b509577c042697add820579de13ceed535b1c02ec7fa460b892d6c63941390a7`  
		Last Modified: Sat, 16 May 2020 09:48:21 GMT  
		Size: 4.1 MB (4087491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ce65065eb7bc6684476be5937b3d0d4046e7cc7241bc5017d70488d0edbfe3`  
		Last Modified: Sat, 16 May 2020 09:48:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:707f02b7c81a3f071abba9ce0a74b1cf0bf7a664e0220ab6cae112f2721a24bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f2220669ef3621c45d5e4fd8460e7378e258044eb57003584ce55db5bdd9b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 04:26:09 GMT
COPY file:3320edcd8f0db9551469809c752244493d1c6cf3be0287714c8a507e339283b2 in /nats-server 
# Sat, 16 May 2020 04:26:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 04:26:11 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 04:26:12 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 04:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ceefb66163b74f9719728ecace35bd406e85998a252d90c9e07a02582c7b6f1`  
		Last Modified: Sat, 16 May 2020 04:26:55 GMT  
		Size: 3.8 MB (3791795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db182fe235e1ef3b80de633e39d8ab9040cef44127adee97dbc4513df27dacfe`  
		Last Modified: Sat, 16 May 2020 04:26:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8cb2b90d45f90f3bdfb841b4a1399ff3a1b0a835e54664ee375ef309ff4c4398
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffbb615827376dda1ad45bce22763d7cdc858675e4eafc55deb2d134f813338`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 29 Jul 2020 22:41:42 GMT
COPY file:67a03d7df05756de9c16c4cd22dfaf6ed9cc9a43b78a90ebfaa81ee7ebbc7abf in /nats-server 
# Wed, 29 Jul 2020 22:41:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 29 Jul 2020 22:41:44 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 29 Jul 2020 22:41:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:39a183ba93759b5fab08b0cb81f1f1a4c9f5a95c3746b031082c6bc3a57441b3`  
		Last Modified: Wed, 29 Jul 2020 22:42:18 GMT  
		Size: 3.8 MB (3776492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a510a0d87b5b915212ee2a5e5d877dced1c30164c0e82d6e60951d00374fe7`  
		Last Modified: Wed, 29 Jul 2020 22:42:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:fab4ee5c94bd9c5b51af3443a5e1256a21fbb5c5ee86a16019a9a829d595cc5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df67809471568873f0b55fa2d9279ecd2de972502b1adce9bf5057aa042eeca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:37 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Wed, 12 Aug 2020 15:13:38 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf155fe2305c82a23507253332f17d7aeb14c022ac7a52f5155ae5aa5de1d45f`  
		Last Modified: Wed, 12 Aug 2020 15:17:29 GMT  
		Size: 4.1 MB (4056411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d108e9f2e737a24742707fdf007fe8f7ca13bcedfd9129b96e0e5479628da`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74184b55b68844992dafa04e9428b3ee68812f3aeccaf54c77110f259dc95818`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c0906cabdee780b68928e7fe89c9f700cd0b67b45da2e0dd16565fa396749`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6a501b122f4b08c277b1526120f7c530e499393cefca21279714f60aeaf2d`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1`

```console
$ docker pull nats@sha256:86b28d48aa026c39a3d8b119b2dd56089d501c147727f5d5ed7a000a18cbb262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1397; amd64

### `nats:2.1` - linux; amd64

```console
$ docker pull nats@sha256:6aace730d886f9719841c60ec11f826e494b8fcc631378b32f5e01ca32d87ab9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e93a56bc1852bb18d91f1741edde016c59b49c92f7ad91960d583ee0486ebf3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 09:47:58 GMT
COPY file:27ab63fb5115ca3cb7456a256d6d6dab7ba864d8806821652fbe569f4f845df5 in /nats-server 
# Sat, 16 May 2020 09:47:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 09:47:59 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 09:47:59 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 09:47:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b509577c042697add820579de13ceed535b1c02ec7fa460b892d6c63941390a7`  
		Last Modified: Sat, 16 May 2020 09:48:21 GMT  
		Size: 4.1 MB (4087491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ce65065eb7bc6684476be5937b3d0d4046e7cc7241bc5017d70488d0edbfe3`  
		Last Modified: Sat, 16 May 2020 09:48:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm variant v7

```console
$ docker pull nats@sha256:707f02b7c81a3f071abba9ce0a74b1cf0bf7a664e0220ab6cae112f2721a24bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f2220669ef3621c45d5e4fd8460e7378e258044eb57003584ce55db5bdd9b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 04:26:09 GMT
COPY file:3320edcd8f0db9551469809c752244493d1c6cf3be0287714c8a507e339283b2 in /nats-server 
# Sat, 16 May 2020 04:26:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 04:26:11 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 04:26:12 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 04:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ceefb66163b74f9719728ecace35bd406e85998a252d90c9e07a02582c7b6f1`  
		Last Modified: Sat, 16 May 2020 04:26:55 GMT  
		Size: 3.8 MB (3791795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db182fe235e1ef3b80de633e39d8ab9040cef44127adee97dbc4513df27dacfe`  
		Last Modified: Sat, 16 May 2020 04:26:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8cb2b90d45f90f3bdfb841b4a1399ff3a1b0a835e54664ee375ef309ff4c4398
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffbb615827376dda1ad45bce22763d7cdc858675e4eafc55deb2d134f813338`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 29 Jul 2020 22:41:42 GMT
COPY file:67a03d7df05756de9c16c4cd22dfaf6ed9cc9a43b78a90ebfaa81ee7ebbc7abf in /nats-server 
# Wed, 29 Jul 2020 22:41:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 29 Jul 2020 22:41:44 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 29 Jul 2020 22:41:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:39a183ba93759b5fab08b0cb81f1f1a4c9f5a95c3746b031082c6bc3a57441b3`  
		Last Modified: Wed, 29 Jul 2020 22:42:18 GMT  
		Size: 3.8 MB (3776492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a510a0d87b5b915212ee2a5e5d877dced1c30164c0e82d6e60951d00374fe7`  
		Last Modified: Wed, 29 Jul 2020 22:42:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:fab4ee5c94bd9c5b51af3443a5e1256a21fbb5c5ee86a16019a9a829d595cc5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df67809471568873f0b55fa2d9279ecd2de972502b1adce9bf5057aa042eeca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:37 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Wed, 12 Aug 2020 15:13:38 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf155fe2305c82a23507253332f17d7aeb14c022ac7a52f5155ae5aa5de1d45f`  
		Last Modified: Wed, 12 Aug 2020 15:17:29 GMT  
		Size: 4.1 MB (4056411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d108e9f2e737a24742707fdf007fe8f7ca13bcedfd9129b96e0e5479628da`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74184b55b68844992dafa04e9428b3ee68812f3aeccaf54c77110f259dc95818`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c0906cabdee780b68928e7fe89c9f700cd0b67b45da2e0dd16565fa396749`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6a501b122f4b08c277b1526120f7c530e499393cefca21279714f60aeaf2d`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1.8`

**does not exist** (yet?)

## `nats:2.1.8-alpine`

**does not exist** (yet?)

## `nats:2.1.8-alpine3.11`

**does not exist** (yet?)

## `nats:2.1.8-linux`

**does not exist** (yet?)

## `nats:2.1.8-nanoserver`

**does not exist** (yet?)

## `nats:2.1.8-nanoserver-1809`

**does not exist** (yet?)

## `nats:2.1.8-scratch`

**does not exist** (yet?)

## `nats:2.1.8-windowsservercore`

**does not exist** (yet?)

## `nats:2.1.8-windowsservercore-1809`

**does not exist** (yet?)

## `nats:2.1.8-windowsservercore-ltsc2016`

**does not exist** (yet?)

## `nats:2.1-alpine`

```console
$ docker pull nats@sha256:2ca671f95f6f5c4d9144a701d8b7be77a1830041d86766e2e193fb58b00af449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-alpine` - linux; amd64

```console
$ docker pull nats@sha256:c1c1159e76d03431b2c612d378a62fc914f0817df3f9a8092adddb589ac74e53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54acd9cf4794435761c0462aba37d41e69e9581a77daeef4d16255b6a579f2c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 09:47:11 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:25:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:25:42 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:25:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:25:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eebfe9509bcbfcefadbc17c68fa103be7b7cf978f08ea01527a6aba38c5554`  
		Last Modified: Wed, 29 Jul 2020 23:26:16 GMT  
		Size: 4.4 MB (4388967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab62a5d69bc21353fa665e0b7fbf8e6a4a5d3fda0e87d58c02073999f76ff43f`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a297d716cd17565b8a6331222fe5c2bcf967f50c6e424f62a5051e864941e2`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:fee67afb8a9c6c38c60a5b90f51b6a6dfdb607b13d04240cf4faae9f8235d69d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6717777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5af24d85d20ca2ddf1a257d6667c94e32ad6c1f381964f6ea48833ebc6eb39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:02:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:02:36 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:02:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:02:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0546a69fc010fc7d9fdae3cd6ff1eb8d7d7471a3561d782f6bb2bebcb079ad`  
		Last Modified: Wed, 29 Jul 2020 23:03:02 GMT  
		Size: 4.1 MB (4096870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc6927e9f4f4d185c4420481f8b1e06d55f058ad32ac4c0a9fc2ca3c2e0e64`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6963e293037e1e7ddf702b89cf5a9441918b610e877f1710001b055560f92901`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:197a92e111811ad767369a9bd75175ecb906fa57009400e78fa5d07ff8b0b47d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6515331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4546538a81c298be13378de43d24f5778e46917a8c2e6feca95287f8695e7d82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 04:17:01 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:11:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:11:47 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:11:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4572ecf34c0bc5aa1ca0925f8f3c17e07cdf857ae8e31be72e5360711b24016`  
		Last Modified: Wed, 29 Jul 2020 23:15:57 GMT  
		Size: 4.1 MB (4092296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67632d2c07c7d161703500f1b0fa040775c8cb0c4474b8749a8ea961b5964f7e`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f50a8c5ae0937cd72ab745aacf65d53e62fed9a22d0de4fb3fe2f3d88a9b6`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e3338a58db906f99cb91860cf607e3670e8b6676026d2eb70d26100b26bfcd5f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79bcc07d57e06d12e6ae92a95f16c0dfe72401e9efdc3a3869273d02110feda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:28:21 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 22:41:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 22:41:31 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:41:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e23520311eff0ccb9b4116bad00040e13d45013d01d87ee89bba20b01b5e536`  
		Last Modified: Wed, 29 Jul 2020 22:42:03 GMT  
		Size: 4.1 MB (4078060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bd55073b3a781fd6af08f7e29facaf7e8d37e977fc7b8a7bcb57098c1dc49b`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2eb0d8170b7670bd8ae9406d3cc6298a0cc3b8f3ec7434dd09ec858f8701183`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-alpine3.11`

```console
$ docker pull nats@sha256:2ca671f95f6f5c4d9144a701d8b7be77a1830041d86766e2e193fb58b00af449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:c1c1159e76d03431b2c612d378a62fc914f0817df3f9a8092adddb589ac74e53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54acd9cf4794435761c0462aba37d41e69e9581a77daeef4d16255b6a579f2c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 09:47:11 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:25:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:25:42 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:25:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:25:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eebfe9509bcbfcefadbc17c68fa103be7b7cf978f08ea01527a6aba38c5554`  
		Last Modified: Wed, 29 Jul 2020 23:26:16 GMT  
		Size: 4.4 MB (4388967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab62a5d69bc21353fa665e0b7fbf8e6a4a5d3fda0e87d58c02073999f76ff43f`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a297d716cd17565b8a6331222fe5c2bcf967f50c6e424f62a5051e864941e2`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:fee67afb8a9c6c38c60a5b90f51b6a6dfdb607b13d04240cf4faae9f8235d69d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6717777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5af24d85d20ca2ddf1a257d6667c94e32ad6c1f381964f6ea48833ebc6eb39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:02:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:02:36 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:02:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:02:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0546a69fc010fc7d9fdae3cd6ff1eb8d7d7471a3561d782f6bb2bebcb079ad`  
		Last Modified: Wed, 29 Jul 2020 23:03:02 GMT  
		Size: 4.1 MB (4096870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc6927e9f4f4d185c4420481f8b1e06d55f058ad32ac4c0a9fc2ca3c2e0e64`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6963e293037e1e7ddf702b89cf5a9441918b610e877f1710001b055560f92901`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:197a92e111811ad767369a9bd75175ecb906fa57009400e78fa5d07ff8b0b47d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6515331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4546538a81c298be13378de43d24f5778e46917a8c2e6feca95287f8695e7d82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 04:17:01 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:11:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:11:47 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:11:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4572ecf34c0bc5aa1ca0925f8f3c17e07cdf857ae8e31be72e5360711b24016`  
		Last Modified: Wed, 29 Jul 2020 23:15:57 GMT  
		Size: 4.1 MB (4092296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67632d2c07c7d161703500f1b0fa040775c8cb0c4474b8749a8ea961b5964f7e`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f50a8c5ae0937cd72ab745aacf65d53e62fed9a22d0de4fb3fe2f3d88a9b6`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e3338a58db906f99cb91860cf607e3670e8b6676026d2eb70d26100b26bfcd5f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79bcc07d57e06d12e6ae92a95f16c0dfe72401e9efdc3a3869273d02110feda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:28:21 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 22:41:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 22:41:31 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:41:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e23520311eff0ccb9b4116bad00040e13d45013d01d87ee89bba20b01b5e536`  
		Last Modified: Wed, 29 Jul 2020 22:42:03 GMT  
		Size: 4.1 MB (4078060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bd55073b3a781fd6af08f7e29facaf7e8d37e977fc7b8a7bcb57098c1dc49b`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2eb0d8170b7670bd8ae9406d3cc6298a0cc3b8f3ec7434dd09ec858f8701183`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-linux`

```console
$ docker pull nats@sha256:7a3219e049b4d8b10a7ff389fa689c8d08d5732fe37dcf9c5a72fda463d6c6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-linux` - linux; amd64

```console
$ docker pull nats@sha256:6aace730d886f9719841c60ec11f826e494b8fcc631378b32f5e01ca32d87ab9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e93a56bc1852bb18d91f1741edde016c59b49c92f7ad91960d583ee0486ebf3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 09:47:58 GMT
COPY file:27ab63fb5115ca3cb7456a256d6d6dab7ba864d8806821652fbe569f4f845df5 in /nats-server 
# Sat, 16 May 2020 09:47:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 09:47:59 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 09:47:59 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 09:47:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b509577c042697add820579de13ceed535b1c02ec7fa460b892d6c63941390a7`  
		Last Modified: Sat, 16 May 2020 09:48:21 GMT  
		Size: 4.1 MB (4087491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ce65065eb7bc6684476be5937b3d0d4046e7cc7241bc5017d70488d0edbfe3`  
		Last Modified: Sat, 16 May 2020 09:48:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:707f02b7c81a3f071abba9ce0a74b1cf0bf7a664e0220ab6cae112f2721a24bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f2220669ef3621c45d5e4fd8460e7378e258044eb57003584ce55db5bdd9b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 04:26:09 GMT
COPY file:3320edcd8f0db9551469809c752244493d1c6cf3be0287714c8a507e339283b2 in /nats-server 
# Sat, 16 May 2020 04:26:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 04:26:11 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 04:26:12 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 04:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ceefb66163b74f9719728ecace35bd406e85998a252d90c9e07a02582c7b6f1`  
		Last Modified: Sat, 16 May 2020 04:26:55 GMT  
		Size: 3.8 MB (3791795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db182fe235e1ef3b80de633e39d8ab9040cef44127adee97dbc4513df27dacfe`  
		Last Modified: Sat, 16 May 2020 04:26:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8cb2b90d45f90f3bdfb841b4a1399ff3a1b0a835e54664ee375ef309ff4c4398
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffbb615827376dda1ad45bce22763d7cdc858675e4eafc55deb2d134f813338`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 29 Jul 2020 22:41:42 GMT
COPY file:67a03d7df05756de9c16c4cd22dfaf6ed9cc9a43b78a90ebfaa81ee7ebbc7abf in /nats-server 
# Wed, 29 Jul 2020 22:41:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 29 Jul 2020 22:41:44 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 29 Jul 2020 22:41:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:39a183ba93759b5fab08b0cb81f1f1a4c9f5a95c3746b031082c6bc3a57441b3`  
		Last Modified: Wed, 29 Jul 2020 22:42:18 GMT  
		Size: 3.8 MB (3776492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a510a0d87b5b915212ee2a5e5d877dced1c30164c0e82d6e60951d00374fe7`  
		Last Modified: Wed, 29 Jul 2020 22:42:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver`

```console
$ docker pull nats@sha256:687e2e9d2a37d8697ee65d4a50e5afd58fa5db82f2750ab60ba88dd2ee6ca0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:2.1-nanoserver` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:fab4ee5c94bd9c5b51af3443a5e1256a21fbb5c5ee86a16019a9a829d595cc5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df67809471568873f0b55fa2d9279ecd2de972502b1adce9bf5057aa042eeca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:37 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Wed, 12 Aug 2020 15:13:38 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf155fe2305c82a23507253332f17d7aeb14c022ac7a52f5155ae5aa5de1d45f`  
		Last Modified: Wed, 12 Aug 2020 15:17:29 GMT  
		Size: 4.1 MB (4056411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d108e9f2e737a24742707fdf007fe8f7ca13bcedfd9129b96e0e5479628da`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74184b55b68844992dafa04e9428b3ee68812f3aeccaf54c77110f259dc95818`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c0906cabdee780b68928e7fe89c9f700cd0b67b45da2e0dd16565fa396749`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6a501b122f4b08c277b1526120f7c530e499393cefca21279714f60aeaf2d`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-nanoserver-1809`

```console
$ docker pull nats@sha256:687e2e9d2a37d8697ee65d4a50e5afd58fa5db82f2750ab60ba88dd2ee6ca0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:2.1-nanoserver-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:fab4ee5c94bd9c5b51af3443a5e1256a21fbb5c5ee86a16019a9a829d595cc5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df67809471568873f0b55fa2d9279ecd2de972502b1adce9bf5057aa042eeca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:37 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Wed, 12 Aug 2020 15:13:38 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf155fe2305c82a23507253332f17d7aeb14c022ac7a52f5155ae5aa5de1d45f`  
		Last Modified: Wed, 12 Aug 2020 15:17:29 GMT  
		Size: 4.1 MB (4056411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d108e9f2e737a24742707fdf007fe8f7ca13bcedfd9129b96e0e5479628da`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74184b55b68844992dafa04e9428b3ee68812f3aeccaf54c77110f259dc95818`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c0906cabdee780b68928e7fe89c9f700cd0b67b45da2e0dd16565fa396749`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6a501b122f4b08c277b1526120f7c530e499393cefca21279714f60aeaf2d`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-scratch`

```console
$ docker pull nats@sha256:7a3219e049b4d8b10a7ff389fa689c8d08d5732fe37dcf9c5a72fda463d6c6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.1-scratch` - linux; amd64

```console
$ docker pull nats@sha256:6aace730d886f9719841c60ec11f826e494b8fcc631378b32f5e01ca32d87ab9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e93a56bc1852bb18d91f1741edde016c59b49c92f7ad91960d583ee0486ebf3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 09:47:58 GMT
COPY file:27ab63fb5115ca3cb7456a256d6d6dab7ba864d8806821652fbe569f4f845df5 in /nats-server 
# Sat, 16 May 2020 09:47:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 09:47:59 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 09:47:59 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 09:47:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b509577c042697add820579de13ceed535b1c02ec7fa460b892d6c63941390a7`  
		Last Modified: Sat, 16 May 2020 09:48:21 GMT  
		Size: 4.1 MB (4087491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ce65065eb7bc6684476be5937b3d0d4046e7cc7241bc5017d70488d0edbfe3`  
		Last Modified: Sat, 16 May 2020 09:48:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:707f02b7c81a3f071abba9ce0a74b1cf0bf7a664e0220ab6cae112f2721a24bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f2220669ef3621c45d5e4fd8460e7378e258044eb57003584ce55db5bdd9b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 04:26:09 GMT
COPY file:3320edcd8f0db9551469809c752244493d1c6cf3be0287714c8a507e339283b2 in /nats-server 
# Sat, 16 May 2020 04:26:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 04:26:11 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 04:26:12 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 04:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ceefb66163b74f9719728ecace35bd406e85998a252d90c9e07a02582c7b6f1`  
		Last Modified: Sat, 16 May 2020 04:26:55 GMT  
		Size: 3.8 MB (3791795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db182fe235e1ef3b80de633e39d8ab9040cef44127adee97dbc4513df27dacfe`  
		Last Modified: Sat, 16 May 2020 04:26:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8cb2b90d45f90f3bdfb841b4a1399ff3a1b0a835e54664ee375ef309ff4c4398
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffbb615827376dda1ad45bce22763d7cdc858675e4eafc55deb2d134f813338`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 29 Jul 2020 22:41:42 GMT
COPY file:67a03d7df05756de9c16c4cd22dfaf6ed9cc9a43b78a90ebfaa81ee7ebbc7abf in /nats-server 
# Wed, 29 Jul 2020 22:41:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 29 Jul 2020 22:41:44 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 29 Jul 2020 22:41:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:39a183ba93759b5fab08b0cb81f1f1a4c9f5a95c3746b031082c6bc3a57441b3`  
		Last Modified: Wed, 29 Jul 2020 22:42:18 GMT  
		Size: 3.8 MB (3776492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a510a0d87b5b915212ee2a5e5d877dced1c30164c0e82d6e60951d00374fe7`  
		Last Modified: Wed, 29 Jul 2020 22:42:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore`

```console
$ docker pull nats@sha256:3a169f34fc3f83e1d0b59a1e68d4e025b44c3fb7c86abf4821928a855b46bd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64
	-	windows version 10.0.14393.3866; amd64

### `nats:2.1-windowsservercore` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:4c298769615507fe26f26020eea1cadc0788d08b44e0375645292f7911fa8b68
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353839627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4815bfd4dca6cf258612f47848b3c6db32948cc50d1ce31085ac18bde7c31458`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:11:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:11:55 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:12:24 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:13:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:13:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:28 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1840e546a26b2d59dbfc9a31aa86b2dc8fed4c6c60f0f0a25921348b74423217`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ef50a643fce3c45da04f46fba8dca6f1f41a9d5ea4fddfaa06d4f9dfbe72a`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc9ff799390763d0a47806bfea8cfd0977acfe08dc0599806dbf48ebf777af`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb34b8a7d4aca227c853d019d08c475ab4d8c7b6389a75ee87d3101ddcba027`  
		Last Modified: Wed, 12 Aug 2020 15:17:08 GMT  
		Size: 4.8 MB (4795357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45b278790355e87ce684853f27667cd2e065c810b1123a9b4780ffbf146f646`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 13.2 MB (13166872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b984d8306d2ab511b3c646042d026055ffd2a68d00c99018060274f9cff2dd71`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d251bd0057684d214966948626fc693cc70910f6b968b672a7f4e73d3a277f98`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b110dedd427f4f8d4225ee04b10e8fd25c81021570b244aa5faa8b9118793320`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353c39efe6277128c4ae85f52840603d117b2e2af79fcb4eafa0bedaf6f6a616`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.1-windowsservercore` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats@sha256:0bface4bb75895f9199eb5d6c903d4dfd6b33de95397efa57b8a68ec24d27c24
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5757484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96755e6aa9687beb1cbc44dbd19b93506cee5eee3735391e15cf738d0cbde5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:13:48 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:14:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:16:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:16:27 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:16:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff217b5d5bc8c8fb41e01c3eba376734cd65c568cbbdbad4f1b8ccb343094e`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6904aa06a0a62b5c80e74f511a5c8873ab6cb3f831cb07b8cb7d11c1dce548`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4e430ecc8ccbf747007a59ada2a242e3bd877de9f9f8340b68fe64dc16006`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f21f629b2ebf35877201ffedc54c17cc42ed1ff6d5a1b103cbc509fad733de8`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 5.4 MB (5391292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc789bee248747dae7caa25fcef8fe71174cbda62c0fb0ce6cb3ad9614312de3`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 13.9 MB (13935154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55d61fc54488846a758ce45ea5d71a778d33da5666007bdd5ed760d5387bf20`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043116cc2890a72214497abfc0adc7a287ea917ad5c29d71c63318e068e9d4e`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f6d4aab762740fae48f892182795785925e79465defac676880314cdeec2f`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994575a0eb610ea577e32ef234217e7cc59a26bd3cfe05726ddbfb9b7df25e93`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-1809`

```console
$ docker pull nats@sha256:a6ded0763c8f2024e25a5ab402647507373f70ad5c710a10b460a1c7ccd46470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:2.1-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:4c298769615507fe26f26020eea1cadc0788d08b44e0375645292f7911fa8b68
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353839627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4815bfd4dca6cf258612f47848b3c6db32948cc50d1ce31085ac18bde7c31458`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:11:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:11:55 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:12:24 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:13:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:13:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:28 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1840e546a26b2d59dbfc9a31aa86b2dc8fed4c6c60f0f0a25921348b74423217`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ef50a643fce3c45da04f46fba8dca6f1f41a9d5ea4fddfaa06d4f9dfbe72a`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc9ff799390763d0a47806bfea8cfd0977acfe08dc0599806dbf48ebf777af`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb34b8a7d4aca227c853d019d08c475ab4d8c7b6389a75ee87d3101ddcba027`  
		Last Modified: Wed, 12 Aug 2020 15:17:08 GMT  
		Size: 4.8 MB (4795357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45b278790355e87ce684853f27667cd2e065c810b1123a9b4780ffbf146f646`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 13.2 MB (13166872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b984d8306d2ab511b3c646042d026055ffd2a68d00c99018060274f9cff2dd71`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d251bd0057684d214966948626fc693cc70910f6b968b672a7f4e73d3a277f98`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b110dedd427f4f8d4225ee04b10e8fd25c81021570b244aa5faa8b9118793320`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353c39efe6277128c4ae85f52840603d117b2e2af79fcb4eafa0bedaf6f6a616`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.1-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:bf19d4980ecf00f544f3dbf73f06c7bd88adf27b537b1bc2d9d48ba37a850395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `nats:2.1-windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats@sha256:0bface4bb75895f9199eb5d6c903d4dfd6b33de95397efa57b8a68ec24d27c24
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5757484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96755e6aa9687beb1cbc44dbd19b93506cee5eee3735391e15cf738d0cbde5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:13:48 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:14:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:16:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:16:27 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:16:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff217b5d5bc8c8fb41e01c3eba376734cd65c568cbbdbad4f1b8ccb343094e`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6904aa06a0a62b5c80e74f511a5c8873ab6cb3f831cb07b8cb7d11c1dce548`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4e430ecc8ccbf747007a59ada2a242e3bd877de9f9f8340b68fe64dc16006`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f21f629b2ebf35877201ffedc54c17cc42ed1ff6d5a1b103cbc509fad733de8`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 5.4 MB (5391292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc789bee248747dae7caa25fcef8fe71174cbda62c0fb0ce6cb3ad9614312de3`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 13.9 MB (13935154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55d61fc54488846a758ce45ea5d71a778d33da5666007bdd5ed760d5387bf20`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043116cc2890a72214497abfc0adc7a287ea917ad5c29d71c63318e068e9d4e`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f6d4aab762740fae48f892182795785925e79465defac676880314cdeec2f`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994575a0eb610ea577e32ef234217e7cc59a26bd3cfe05726ddbfb9b7df25e93`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:2ca671f95f6f5c4d9144a701d8b7be77a1830041d86766e2e193fb58b00af449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:c1c1159e76d03431b2c612d378a62fc914f0817df3f9a8092adddb589ac74e53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54acd9cf4794435761c0462aba37d41e69e9581a77daeef4d16255b6a579f2c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 09:47:11 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:25:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:25:42 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:25:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:25:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eebfe9509bcbfcefadbc17c68fa103be7b7cf978f08ea01527a6aba38c5554`  
		Last Modified: Wed, 29 Jul 2020 23:26:16 GMT  
		Size: 4.4 MB (4388967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab62a5d69bc21353fa665e0b7fbf8e6a4a5d3fda0e87d58c02073999f76ff43f`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a297d716cd17565b8a6331222fe5c2bcf967f50c6e424f62a5051e864941e2`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:fee67afb8a9c6c38c60a5b90f51b6a6dfdb607b13d04240cf4faae9f8235d69d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6717777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5af24d85d20ca2ddf1a257d6667c94e32ad6c1f381964f6ea48833ebc6eb39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:02:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:02:36 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:02:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:02:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0546a69fc010fc7d9fdae3cd6ff1eb8d7d7471a3561d782f6bb2bebcb079ad`  
		Last Modified: Wed, 29 Jul 2020 23:03:02 GMT  
		Size: 4.1 MB (4096870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc6927e9f4f4d185c4420481f8b1e06d55f058ad32ac4c0a9fc2ca3c2e0e64`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6963e293037e1e7ddf702b89cf5a9441918b610e877f1710001b055560f92901`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:197a92e111811ad767369a9bd75175ecb906fa57009400e78fa5d07ff8b0b47d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6515331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4546538a81c298be13378de43d24f5778e46917a8c2e6feca95287f8695e7d82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 04:17:01 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:11:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:11:47 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:11:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4572ecf34c0bc5aa1ca0925f8f3c17e07cdf857ae8e31be72e5360711b24016`  
		Last Modified: Wed, 29 Jul 2020 23:15:57 GMT  
		Size: 4.1 MB (4092296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67632d2c07c7d161703500f1b0fa040775c8cb0c4474b8749a8ea961b5964f7e`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f50a8c5ae0937cd72ab745aacf65d53e62fed9a22d0de4fb3fe2f3d88a9b6`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e3338a58db906f99cb91860cf607e3670e8b6676026d2eb70d26100b26bfcd5f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79bcc07d57e06d12e6ae92a95f16c0dfe72401e9efdc3a3869273d02110feda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:28:21 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 22:41:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 22:41:31 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:41:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e23520311eff0ccb9b4116bad00040e13d45013d01d87ee89bba20b01b5e536`  
		Last Modified: Wed, 29 Jul 2020 22:42:03 GMT  
		Size: 4.1 MB (4078060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bd55073b3a781fd6af08f7e29facaf7e8d37e977fc7b8a7bcb57098c1dc49b`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2eb0d8170b7670bd8ae9406d3cc6298a0cc3b8f3ec7434dd09ec858f8701183`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.11`

```console
$ docker pull nats@sha256:2ca671f95f6f5c4d9144a701d8b7be77a1830041d86766e2e193fb58b00af449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:c1c1159e76d03431b2c612d378a62fc914f0817df3f9a8092adddb589ac74e53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54acd9cf4794435761c0462aba37d41e69e9581a77daeef4d16255b6a579f2c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 09:47:11 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:25:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:25:42 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:25:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:25:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eebfe9509bcbfcefadbc17c68fa103be7b7cf978f08ea01527a6aba38c5554`  
		Last Modified: Wed, 29 Jul 2020 23:26:16 GMT  
		Size: 4.4 MB (4388967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab62a5d69bc21353fa665e0b7fbf8e6a4a5d3fda0e87d58c02073999f76ff43f`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a297d716cd17565b8a6331222fe5c2bcf967f50c6e424f62a5051e864941e2`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:fee67afb8a9c6c38c60a5b90f51b6a6dfdb607b13d04240cf4faae9f8235d69d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6717777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5af24d85d20ca2ddf1a257d6667c94e32ad6c1f381964f6ea48833ebc6eb39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:02:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:02:36 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:02:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:02:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0546a69fc010fc7d9fdae3cd6ff1eb8d7d7471a3561d782f6bb2bebcb079ad`  
		Last Modified: Wed, 29 Jul 2020 23:03:02 GMT  
		Size: 4.1 MB (4096870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc6927e9f4f4d185c4420481f8b1e06d55f058ad32ac4c0a9fc2ca3c2e0e64`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6963e293037e1e7ddf702b89cf5a9441918b610e877f1710001b055560f92901`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:197a92e111811ad767369a9bd75175ecb906fa57009400e78fa5d07ff8b0b47d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6515331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4546538a81c298be13378de43d24f5778e46917a8c2e6feca95287f8695e7d82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 04:17:01 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:11:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:11:47 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:11:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4572ecf34c0bc5aa1ca0925f8f3c17e07cdf857ae8e31be72e5360711b24016`  
		Last Modified: Wed, 29 Jul 2020 23:15:57 GMT  
		Size: 4.1 MB (4092296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67632d2c07c7d161703500f1b0fa040775c8cb0c4474b8749a8ea961b5964f7e`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f50a8c5ae0937cd72ab745aacf65d53e62fed9a22d0de4fb3fe2f3d88a9b6`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e3338a58db906f99cb91860cf607e3670e8b6676026d2eb70d26100b26bfcd5f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79bcc07d57e06d12e6ae92a95f16c0dfe72401e9efdc3a3869273d02110feda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:28:21 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 22:41:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 22:41:31 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:41:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e23520311eff0ccb9b4116bad00040e13d45013d01d87ee89bba20b01b5e536`  
		Last Modified: Wed, 29 Jul 2020 22:42:03 GMT  
		Size: 4.1 MB (4078060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bd55073b3a781fd6af08f7e29facaf7e8d37e977fc7b8a7bcb57098c1dc49b`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2eb0d8170b7670bd8ae9406d3cc6298a0cc3b8f3ec7434dd09ec858f8701183`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:7a3219e049b4d8b10a7ff389fa689c8d08d5732fe37dcf9c5a72fda463d6c6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:6aace730d886f9719841c60ec11f826e494b8fcc631378b32f5e01ca32d87ab9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e93a56bc1852bb18d91f1741edde016c59b49c92f7ad91960d583ee0486ebf3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 09:47:58 GMT
COPY file:27ab63fb5115ca3cb7456a256d6d6dab7ba864d8806821652fbe569f4f845df5 in /nats-server 
# Sat, 16 May 2020 09:47:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 09:47:59 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 09:47:59 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 09:47:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b509577c042697add820579de13ceed535b1c02ec7fa460b892d6c63941390a7`  
		Last Modified: Sat, 16 May 2020 09:48:21 GMT  
		Size: 4.1 MB (4087491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ce65065eb7bc6684476be5937b3d0d4046e7cc7241bc5017d70488d0edbfe3`  
		Last Modified: Sat, 16 May 2020 09:48:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:707f02b7c81a3f071abba9ce0a74b1cf0bf7a664e0220ab6cae112f2721a24bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f2220669ef3621c45d5e4fd8460e7378e258044eb57003584ce55db5bdd9b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 04:26:09 GMT
COPY file:3320edcd8f0db9551469809c752244493d1c6cf3be0287714c8a507e339283b2 in /nats-server 
# Sat, 16 May 2020 04:26:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 04:26:11 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 04:26:12 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 04:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ceefb66163b74f9719728ecace35bd406e85998a252d90c9e07a02582c7b6f1`  
		Last Modified: Sat, 16 May 2020 04:26:55 GMT  
		Size: 3.8 MB (3791795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db182fe235e1ef3b80de633e39d8ab9040cef44127adee97dbc4513df27dacfe`  
		Last Modified: Sat, 16 May 2020 04:26:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8cb2b90d45f90f3bdfb841b4a1399ff3a1b0a835e54664ee375ef309ff4c4398
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffbb615827376dda1ad45bce22763d7cdc858675e4eafc55deb2d134f813338`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 29 Jul 2020 22:41:42 GMT
COPY file:67a03d7df05756de9c16c4cd22dfaf6ed9cc9a43b78a90ebfaa81ee7ebbc7abf in /nats-server 
# Wed, 29 Jul 2020 22:41:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 29 Jul 2020 22:41:44 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 29 Jul 2020 22:41:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:39a183ba93759b5fab08b0cb81f1f1a4c9f5a95c3746b031082c6bc3a57441b3`  
		Last Modified: Wed, 29 Jul 2020 22:42:18 GMT  
		Size: 3.8 MB (3776492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a510a0d87b5b915212ee2a5e5d877dced1c30164c0e82d6e60951d00374fe7`  
		Last Modified: Wed, 29 Jul 2020 22:42:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:687e2e9d2a37d8697ee65d4a50e5afd58fa5db82f2750ab60ba88dd2ee6ca0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:fab4ee5c94bd9c5b51af3443a5e1256a21fbb5c5ee86a16019a9a829d595cc5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df67809471568873f0b55fa2d9279ecd2de972502b1adce9bf5057aa042eeca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:37 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Wed, 12 Aug 2020 15:13:38 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf155fe2305c82a23507253332f17d7aeb14c022ac7a52f5155ae5aa5de1d45f`  
		Last Modified: Wed, 12 Aug 2020 15:17:29 GMT  
		Size: 4.1 MB (4056411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d108e9f2e737a24742707fdf007fe8f7ca13bcedfd9129b96e0e5479628da`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74184b55b68844992dafa04e9428b3ee68812f3aeccaf54c77110f259dc95818`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c0906cabdee780b68928e7fe89c9f700cd0b67b45da2e0dd16565fa396749`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6a501b122f4b08c277b1526120f7c530e499393cefca21279714f60aeaf2d`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:687e2e9d2a37d8697ee65d4a50e5afd58fa5db82f2750ab60ba88dd2ee6ca0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:fab4ee5c94bd9c5b51af3443a5e1256a21fbb5c5ee86a16019a9a829d595cc5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df67809471568873f0b55fa2d9279ecd2de972502b1adce9bf5057aa042eeca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:37 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Wed, 12 Aug 2020 15:13:38 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf155fe2305c82a23507253332f17d7aeb14c022ac7a52f5155ae5aa5de1d45f`  
		Last Modified: Wed, 12 Aug 2020 15:17:29 GMT  
		Size: 4.1 MB (4056411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d108e9f2e737a24742707fdf007fe8f7ca13bcedfd9129b96e0e5479628da`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74184b55b68844992dafa04e9428b3ee68812f3aeccaf54c77110f259dc95818`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c0906cabdee780b68928e7fe89c9f700cd0b67b45da2e0dd16565fa396749`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6a501b122f4b08c277b1526120f7c530e499393cefca21279714f60aeaf2d`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:7a3219e049b4d8b10a7ff389fa689c8d08d5732fe37dcf9c5a72fda463d6c6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:6aace730d886f9719841c60ec11f826e494b8fcc631378b32f5e01ca32d87ab9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e93a56bc1852bb18d91f1741edde016c59b49c92f7ad91960d583ee0486ebf3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 09:47:58 GMT
COPY file:27ab63fb5115ca3cb7456a256d6d6dab7ba864d8806821652fbe569f4f845df5 in /nats-server 
# Sat, 16 May 2020 09:47:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 09:47:59 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 09:47:59 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 09:47:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b509577c042697add820579de13ceed535b1c02ec7fa460b892d6c63941390a7`  
		Last Modified: Sat, 16 May 2020 09:48:21 GMT  
		Size: 4.1 MB (4087491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ce65065eb7bc6684476be5937b3d0d4046e7cc7241bc5017d70488d0edbfe3`  
		Last Modified: Sat, 16 May 2020 09:48:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:707f02b7c81a3f071abba9ce0a74b1cf0bf7a664e0220ab6cae112f2721a24bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f2220669ef3621c45d5e4fd8460e7378e258044eb57003584ce55db5bdd9b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 04:26:09 GMT
COPY file:3320edcd8f0db9551469809c752244493d1c6cf3be0287714c8a507e339283b2 in /nats-server 
# Sat, 16 May 2020 04:26:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 04:26:11 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 04:26:12 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 04:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ceefb66163b74f9719728ecace35bd406e85998a252d90c9e07a02582c7b6f1`  
		Last Modified: Sat, 16 May 2020 04:26:55 GMT  
		Size: 3.8 MB (3791795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db182fe235e1ef3b80de633e39d8ab9040cef44127adee97dbc4513df27dacfe`  
		Last Modified: Sat, 16 May 2020 04:26:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8cb2b90d45f90f3bdfb841b4a1399ff3a1b0a835e54664ee375ef309ff4c4398
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffbb615827376dda1ad45bce22763d7cdc858675e4eafc55deb2d134f813338`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 29 Jul 2020 22:41:42 GMT
COPY file:67a03d7df05756de9c16c4cd22dfaf6ed9cc9a43b78a90ebfaa81ee7ebbc7abf in /nats-server 
# Wed, 29 Jul 2020 22:41:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 29 Jul 2020 22:41:44 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 29 Jul 2020 22:41:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:39a183ba93759b5fab08b0cb81f1f1a4c9f5a95c3746b031082c6bc3a57441b3`  
		Last Modified: Wed, 29 Jul 2020 22:42:18 GMT  
		Size: 3.8 MB (3776492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a510a0d87b5b915212ee2a5e5d877dced1c30164c0e82d6e60951d00374fe7`  
		Last Modified: Wed, 29 Jul 2020 22:42:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:3a169f34fc3f83e1d0b59a1e68d4e025b44c3fb7c86abf4821928a855b46bd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64
	-	windows version 10.0.14393.3866; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:4c298769615507fe26f26020eea1cadc0788d08b44e0375645292f7911fa8b68
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353839627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4815bfd4dca6cf258612f47848b3c6db32948cc50d1ce31085ac18bde7c31458`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:11:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:11:55 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:12:24 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:13:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:13:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:28 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1840e546a26b2d59dbfc9a31aa86b2dc8fed4c6c60f0f0a25921348b74423217`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ef50a643fce3c45da04f46fba8dca6f1f41a9d5ea4fddfaa06d4f9dfbe72a`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc9ff799390763d0a47806bfea8cfd0977acfe08dc0599806dbf48ebf777af`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb34b8a7d4aca227c853d019d08c475ab4d8c7b6389a75ee87d3101ddcba027`  
		Last Modified: Wed, 12 Aug 2020 15:17:08 GMT  
		Size: 4.8 MB (4795357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45b278790355e87ce684853f27667cd2e065c810b1123a9b4780ffbf146f646`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 13.2 MB (13166872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b984d8306d2ab511b3c646042d026055ffd2a68d00c99018060274f9cff2dd71`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d251bd0057684d214966948626fc693cc70910f6b968b672a7f4e73d3a277f98`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b110dedd427f4f8d4225ee04b10e8fd25c81021570b244aa5faa8b9118793320`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353c39efe6277128c4ae85f52840603d117b2e2af79fcb4eafa0bedaf6f6a616`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats@sha256:0bface4bb75895f9199eb5d6c903d4dfd6b33de95397efa57b8a68ec24d27c24
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5757484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96755e6aa9687beb1cbc44dbd19b93506cee5eee3735391e15cf738d0cbde5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:13:48 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:14:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:16:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:16:27 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:16:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff217b5d5bc8c8fb41e01c3eba376734cd65c568cbbdbad4f1b8ccb343094e`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6904aa06a0a62b5c80e74f511a5c8873ab6cb3f831cb07b8cb7d11c1dce548`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4e430ecc8ccbf747007a59ada2a242e3bd877de9f9f8340b68fe64dc16006`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f21f629b2ebf35877201ffedc54c17cc42ed1ff6d5a1b103cbc509fad733de8`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 5.4 MB (5391292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc789bee248747dae7caa25fcef8fe71174cbda62c0fb0ce6cb3ad9614312de3`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 13.9 MB (13935154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55d61fc54488846a758ce45ea5d71a778d33da5666007bdd5ed760d5387bf20`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043116cc2890a72214497abfc0adc7a287ea917ad5c29d71c63318e068e9d4e`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f6d4aab762740fae48f892182795785925e79465defac676880314cdeec2f`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994575a0eb610ea577e32ef234217e7cc59a26bd3cfe05726ddbfb9b7df25e93`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:a6ded0763c8f2024e25a5ab402647507373f70ad5c710a10b460a1c7ccd46470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:4c298769615507fe26f26020eea1cadc0788d08b44e0375645292f7911fa8b68
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353839627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4815bfd4dca6cf258612f47848b3c6db32948cc50d1ce31085ac18bde7c31458`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:11:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:11:55 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:12:24 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:13:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:13:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:28 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1840e546a26b2d59dbfc9a31aa86b2dc8fed4c6c60f0f0a25921348b74423217`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ef50a643fce3c45da04f46fba8dca6f1f41a9d5ea4fddfaa06d4f9dfbe72a`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc9ff799390763d0a47806bfea8cfd0977acfe08dc0599806dbf48ebf777af`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb34b8a7d4aca227c853d019d08c475ab4d8c7b6389a75ee87d3101ddcba027`  
		Last Modified: Wed, 12 Aug 2020 15:17:08 GMT  
		Size: 4.8 MB (4795357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45b278790355e87ce684853f27667cd2e065c810b1123a9b4780ffbf146f646`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 13.2 MB (13166872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b984d8306d2ab511b3c646042d026055ffd2a68d00c99018060274f9cff2dd71`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d251bd0057684d214966948626fc693cc70910f6b968b672a7f4e73d3a277f98`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b110dedd427f4f8d4225ee04b10e8fd25c81021570b244aa5faa8b9118793320`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353c39efe6277128c4ae85f52840603d117b2e2af79fcb4eafa0bedaf6f6a616`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:bf19d4980ecf00f544f3dbf73f06c7bd88adf27b537b1bc2d9d48ba37a850395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats@sha256:0bface4bb75895f9199eb5d6c903d4dfd6b33de95397efa57b8a68ec24d27c24
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5757484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96755e6aa9687beb1cbc44dbd19b93506cee5eee3735391e15cf738d0cbde5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:13:48 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:14:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:16:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:16:27 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:16:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff217b5d5bc8c8fb41e01c3eba376734cd65c568cbbdbad4f1b8ccb343094e`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6904aa06a0a62b5c80e74f511a5c8873ab6cb3f831cb07b8cb7d11c1dce548`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4e430ecc8ccbf747007a59ada2a242e3bd877de9f9f8340b68fe64dc16006`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f21f629b2ebf35877201ffedc54c17cc42ed1ff6d5a1b103cbc509fad733de8`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 5.4 MB (5391292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc789bee248747dae7caa25fcef8fe71174cbda62c0fb0ce6cb3ad9614312de3`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 13.9 MB (13935154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55d61fc54488846a758ce45ea5d71a778d33da5666007bdd5ed760d5387bf20`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043116cc2890a72214497abfc0adc7a287ea917ad5c29d71c63318e068e9d4e`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f6d4aab762740fae48f892182795785925e79465defac676880314cdeec2f`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994575a0eb610ea577e32ef234217e7cc59a26bd3cfe05726ddbfb9b7df25e93`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:2ca671f95f6f5c4d9144a701d8b7be77a1830041d86766e2e193fb58b00af449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:c1c1159e76d03431b2c612d378a62fc914f0817df3f9a8092adddb589ac74e53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54acd9cf4794435761c0462aba37d41e69e9581a77daeef4d16255b6a579f2c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 09:47:11 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:25:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:25:42 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:25:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:25:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eebfe9509bcbfcefadbc17c68fa103be7b7cf978f08ea01527a6aba38c5554`  
		Last Modified: Wed, 29 Jul 2020 23:26:16 GMT  
		Size: 4.4 MB (4388967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab62a5d69bc21353fa665e0b7fbf8e6a4a5d3fda0e87d58c02073999f76ff43f`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a297d716cd17565b8a6331222fe5c2bcf967f50c6e424f62a5051e864941e2`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:fee67afb8a9c6c38c60a5b90f51b6a6dfdb607b13d04240cf4faae9f8235d69d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6717777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5af24d85d20ca2ddf1a257d6667c94e32ad6c1f381964f6ea48833ebc6eb39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:02:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:02:36 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:02:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:02:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0546a69fc010fc7d9fdae3cd6ff1eb8d7d7471a3561d782f6bb2bebcb079ad`  
		Last Modified: Wed, 29 Jul 2020 23:03:02 GMT  
		Size: 4.1 MB (4096870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc6927e9f4f4d185c4420481f8b1e06d55f058ad32ac4c0a9fc2ca3c2e0e64`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6963e293037e1e7ddf702b89cf5a9441918b610e877f1710001b055560f92901`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:197a92e111811ad767369a9bd75175ecb906fa57009400e78fa5d07ff8b0b47d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6515331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4546538a81c298be13378de43d24f5778e46917a8c2e6feca95287f8695e7d82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 04:17:01 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:11:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:11:47 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:11:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4572ecf34c0bc5aa1ca0925f8f3c17e07cdf857ae8e31be72e5360711b24016`  
		Last Modified: Wed, 29 Jul 2020 23:15:57 GMT  
		Size: 4.1 MB (4092296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67632d2c07c7d161703500f1b0fa040775c8cb0c4474b8749a8ea961b5964f7e`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f50a8c5ae0937cd72ab745aacf65d53e62fed9a22d0de4fb3fe2f3d88a9b6`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e3338a58db906f99cb91860cf607e3670e8b6676026d2eb70d26100b26bfcd5f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79bcc07d57e06d12e6ae92a95f16c0dfe72401e9efdc3a3869273d02110feda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:28:21 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 22:41:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 22:41:31 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:41:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e23520311eff0ccb9b4116bad00040e13d45013d01d87ee89bba20b01b5e536`  
		Last Modified: Wed, 29 Jul 2020 22:42:03 GMT  
		Size: 4.1 MB (4078060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bd55073b3a781fd6af08f7e29facaf7e8d37e977fc7b8a7bcb57098c1dc49b`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2eb0d8170b7670bd8ae9406d3cc6298a0cc3b8f3ec7434dd09ec858f8701183`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.11`

```console
$ docker pull nats@sha256:2ca671f95f6f5c4d9144a701d8b7be77a1830041d86766e2e193fb58b00af449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.11` - linux; amd64

```console
$ docker pull nats@sha256:c1c1159e76d03431b2c612d378a62fc914f0817df3f9a8092adddb589ac74e53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54acd9cf4794435761c0462aba37d41e69e9581a77daeef4d16255b6a579f2c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 09:47:11 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:25:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:25:41 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:25:42 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:25:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:25:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eebfe9509bcbfcefadbc17c68fa103be7b7cf978f08ea01527a6aba38c5554`  
		Last Modified: Wed, 29 Jul 2020 23:26:16 GMT  
		Size: 4.4 MB (4388967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab62a5d69bc21353fa665e0b7fbf8e6a4a5d3fda0e87d58c02073999f76ff43f`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a297d716cd17565b8a6331222fe5c2bcf967f50c6e424f62a5051e864941e2`  
		Last Modified: Wed, 29 Jul 2020 23:26:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:fee67afb8a9c6c38c60a5b90f51b6a6dfdb607b13d04240cf4faae9f8235d69d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6717777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5af24d85d20ca2ddf1a257d6667c94e32ad6c1f381964f6ea48833ebc6eb39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2020 19:50:13 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:02:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:02:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:02:36 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:02:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:02:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0546a69fc010fc7d9fdae3cd6ff1eb8d7d7471a3561d782f6bb2bebcb079ad`  
		Last Modified: Wed, 29 Jul 2020 23:03:02 GMT  
		Size: 4.1 MB (4096870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc6927e9f4f4d185c4420481f8b1e06d55f058ad32ac4c0a9fc2ca3c2e0e64`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6963e293037e1e7ddf702b89cf5a9441918b610e877f1710001b055560f92901`  
		Last Modified: Wed, 29 Jul 2020 23:03:01 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:197a92e111811ad767369a9bd75175ecb906fa57009400e78fa5d07ff8b0b47d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6515331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4546538a81c298be13378de43d24f5778e46917a8c2e6feca95287f8695e7d82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2020 04:17:01 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 23:11:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 23:11:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 23:11:47 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 23:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 23:11:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4572ecf34c0bc5aa1ca0925f8f3c17e07cdf857ae8e31be72e5360711b24016`  
		Last Modified: Wed, 29 Jul 2020 23:15:57 GMT  
		Size: 4.1 MB (4092296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67632d2c07c7d161703500f1b0fa040775c8cb0c4474b8749a8ea961b5964f7e`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f50a8c5ae0937cd72ab745aacf65d53e62fed9a22d0de4fb3fe2f3d88a9b6`  
		Last Modified: Wed, 29 Jul 2020 23:15:56 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e3338a58db906f99cb91860cf607e3670e8b6676026d2eb70d26100b26bfcd5f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79bcc07d57e06d12e6ae92a95f16c0dfe72401e9efdc3a3869273d02110feda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Jul 2020 16:28:21 GMT
ENV NATS_SERVER=2.1.7
# Wed, 29 Jul 2020 22:41:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a08d7ce0399df8701d3e3cd4c36744180c3a566cdb38efeccc12a364f0083705' ;; 		armhf) natsArch='arm6'; sha256='987c23f758842fb09c0d4500f632c5302aedc61d218f03998444b94074aabddb' ;; 		armv7) natsArch='arm7'; sha256='077fd1647aa25865ade5acc3d6ee5f542d2c62feb2fb41ec6d1dd83294bea05e' ;; 		x86_64) natsArch='amd64'; sha256='23cce53fe7f628f203dbbeadf434c3480d094690aba6ff0b1d374b8f2f9ffd8c' ;; 		x86) natsArch='386'; sha256='64e271690782af823930c95574db0f701d06a36ff42b9272c04841d4611bcd15' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 29 Jul 2020 22:41:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 29 Jul 2020 22:41:31 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jul 2020 22:41:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e23520311eff0ccb9b4116bad00040e13d45013d01d87ee89bba20b01b5e536`  
		Last Modified: Wed, 29 Jul 2020 22:42:03 GMT  
		Size: 4.1 MB (4078060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bd55073b3a781fd6af08f7e29facaf7e8d37e977fc7b8a7bcb57098c1dc49b`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2eb0d8170b7670bd8ae9406d3cc6298a0cc3b8f3ec7434dd09ec858f8701183`  
		Last Modified: Wed, 29 Jul 2020 22:42:02 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:86b28d48aa026c39a3d8b119b2dd56089d501c147727f5d5ed7a000a18cbb262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1397; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:6aace730d886f9719841c60ec11f826e494b8fcc631378b32f5e01ca32d87ab9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e93a56bc1852bb18d91f1741edde016c59b49c92f7ad91960d583ee0486ebf3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 09:47:58 GMT
COPY file:27ab63fb5115ca3cb7456a256d6d6dab7ba864d8806821652fbe569f4f845df5 in /nats-server 
# Sat, 16 May 2020 09:47:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 09:47:59 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 09:47:59 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 09:47:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b509577c042697add820579de13ceed535b1c02ec7fa460b892d6c63941390a7`  
		Last Modified: Sat, 16 May 2020 09:48:21 GMT  
		Size: 4.1 MB (4087491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ce65065eb7bc6684476be5937b3d0d4046e7cc7241bc5017d70488d0edbfe3`  
		Last Modified: Sat, 16 May 2020 09:48:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:707f02b7c81a3f071abba9ce0a74b1cf0bf7a664e0220ab6cae112f2721a24bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f2220669ef3621c45d5e4fd8460e7378e258044eb57003584ce55db5bdd9b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 04:26:09 GMT
COPY file:3320edcd8f0db9551469809c752244493d1c6cf3be0287714c8a507e339283b2 in /nats-server 
# Sat, 16 May 2020 04:26:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 04:26:11 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 04:26:12 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 04:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ceefb66163b74f9719728ecace35bd406e85998a252d90c9e07a02582c7b6f1`  
		Last Modified: Sat, 16 May 2020 04:26:55 GMT  
		Size: 3.8 MB (3791795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db182fe235e1ef3b80de633e39d8ab9040cef44127adee97dbc4513df27dacfe`  
		Last Modified: Sat, 16 May 2020 04:26:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8cb2b90d45f90f3bdfb841b4a1399ff3a1b0a835e54664ee375ef309ff4c4398
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffbb615827376dda1ad45bce22763d7cdc858675e4eafc55deb2d134f813338`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 29 Jul 2020 22:41:42 GMT
COPY file:67a03d7df05756de9c16c4cd22dfaf6ed9cc9a43b78a90ebfaa81ee7ebbc7abf in /nats-server 
# Wed, 29 Jul 2020 22:41:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 29 Jul 2020 22:41:44 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 29 Jul 2020 22:41:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:39a183ba93759b5fab08b0cb81f1f1a4c9f5a95c3746b031082c6bc3a57441b3`  
		Last Modified: Wed, 29 Jul 2020 22:42:18 GMT  
		Size: 3.8 MB (3776492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a510a0d87b5b915212ee2a5e5d877dced1c30164c0e82d6e60951d00374fe7`  
		Last Modified: Wed, 29 Jul 2020 22:42:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:fab4ee5c94bd9c5b51af3443a5e1256a21fbb5c5ee86a16019a9a829d595cc5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df67809471568873f0b55fa2d9279ecd2de972502b1adce9bf5057aa042eeca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:37 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Wed, 12 Aug 2020 15:13:38 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf155fe2305c82a23507253332f17d7aeb14c022ac7a52f5155ae5aa5de1d45f`  
		Last Modified: Wed, 12 Aug 2020 15:17:29 GMT  
		Size: 4.1 MB (4056411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d108e9f2e737a24742707fdf007fe8f7ca13bcedfd9129b96e0e5479628da`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74184b55b68844992dafa04e9428b3ee68812f3aeccaf54c77110f259dc95818`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c0906cabdee780b68928e7fe89c9f700cd0b67b45da2e0dd16565fa396749`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6a501b122f4b08c277b1526120f7c530e499393cefca21279714f60aeaf2d`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:7a3219e049b4d8b10a7ff389fa689c8d08d5732fe37dcf9c5a72fda463d6c6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:6aace730d886f9719841c60ec11f826e494b8fcc631378b32f5e01ca32d87ab9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e93a56bc1852bb18d91f1741edde016c59b49c92f7ad91960d583ee0486ebf3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 09:47:58 GMT
COPY file:27ab63fb5115ca3cb7456a256d6d6dab7ba864d8806821652fbe569f4f845df5 in /nats-server 
# Sat, 16 May 2020 09:47:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 09:47:59 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 09:47:59 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 09:47:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b509577c042697add820579de13ceed535b1c02ec7fa460b892d6c63941390a7`  
		Last Modified: Sat, 16 May 2020 09:48:21 GMT  
		Size: 4.1 MB (4087491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ce65065eb7bc6684476be5937b3d0d4046e7cc7241bc5017d70488d0edbfe3`  
		Last Modified: Sat, 16 May 2020 09:48:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:707f02b7c81a3f071abba9ce0a74b1cf0bf7a664e0220ab6cae112f2721a24bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f2220669ef3621c45d5e4fd8460e7378e258044eb57003584ce55db5bdd9b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 04:26:09 GMT
COPY file:3320edcd8f0db9551469809c752244493d1c6cf3be0287714c8a507e339283b2 in /nats-server 
# Sat, 16 May 2020 04:26:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 04:26:11 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 04:26:12 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 04:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ceefb66163b74f9719728ecace35bd406e85998a252d90c9e07a02582c7b6f1`  
		Last Modified: Sat, 16 May 2020 04:26:55 GMT  
		Size: 3.8 MB (3791795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db182fe235e1ef3b80de633e39d8ab9040cef44127adee97dbc4513df27dacfe`  
		Last Modified: Sat, 16 May 2020 04:26:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8cb2b90d45f90f3bdfb841b4a1399ff3a1b0a835e54664ee375ef309ff4c4398
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffbb615827376dda1ad45bce22763d7cdc858675e4eafc55deb2d134f813338`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 29 Jul 2020 22:41:42 GMT
COPY file:67a03d7df05756de9c16c4cd22dfaf6ed9cc9a43b78a90ebfaa81ee7ebbc7abf in /nats-server 
# Wed, 29 Jul 2020 22:41:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 29 Jul 2020 22:41:44 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 29 Jul 2020 22:41:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:39a183ba93759b5fab08b0cb81f1f1a4c9f5a95c3746b031082c6bc3a57441b3`  
		Last Modified: Wed, 29 Jul 2020 22:42:18 GMT  
		Size: 3.8 MB (3776492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a510a0d87b5b915212ee2a5e5d877dced1c30164c0e82d6e60951d00374fe7`  
		Last Modified: Wed, 29 Jul 2020 22:42:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:687e2e9d2a37d8697ee65d4a50e5afd58fa5db82f2750ab60ba88dd2ee6ca0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:nanoserver` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:fab4ee5c94bd9c5b51af3443a5e1256a21fbb5c5ee86a16019a9a829d595cc5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df67809471568873f0b55fa2d9279ecd2de972502b1adce9bf5057aa042eeca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:37 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Wed, 12 Aug 2020 15:13:38 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf155fe2305c82a23507253332f17d7aeb14c022ac7a52f5155ae5aa5de1d45f`  
		Last Modified: Wed, 12 Aug 2020 15:17:29 GMT  
		Size: 4.1 MB (4056411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d108e9f2e737a24742707fdf007fe8f7ca13bcedfd9129b96e0e5479628da`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74184b55b68844992dafa04e9428b3ee68812f3aeccaf54c77110f259dc95818`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c0906cabdee780b68928e7fe89c9f700cd0b67b45da2e0dd16565fa396749`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6a501b122f4b08c277b1526120f7c530e499393cefca21279714f60aeaf2d`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:687e2e9d2a37d8697ee65d4a50e5afd58fa5db82f2750ab60ba88dd2ee6ca0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:fab4ee5c94bd9c5b51af3443a5e1256a21fbb5c5ee86a16019a9a829d595cc5e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df67809471568873f0b55fa2d9279ecd2de972502b1adce9bf5057aa042eeca`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:13:36 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:37 GMT
RUN cmd /S /C #(nop) COPY file:18561b827240029ad80d0e3d25142efae62905c30cc520fc37cfc68e7d889848 in C:\nats-server.exe 
# Wed, 12 Aug 2020 15:13:38 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:39 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:40 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07499a9e4ee2f1cb045788b6e555000daa9000613380cb70f067c5287b55a61`  
		Last Modified: Wed, 12 Aug 2020 15:17:30 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf155fe2305c82a23507253332f17d7aeb14c022ac7a52f5155ae5aa5de1d45f`  
		Last Modified: Wed, 12 Aug 2020 15:17:29 GMT  
		Size: 4.1 MB (4056411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4d108e9f2e737a24742707fdf007fe8f7ca13bcedfd9129b96e0e5479628da`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74184b55b68844992dafa04e9428b3ee68812f3aeccaf54c77110f259dc95818`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053c0906cabdee780b68928e7fe89c9f700cd0b67b45da2e0dd16565fa396749`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 834.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6a501b122f4b08c277b1526120f7c530e499393cefca21279714f60aeaf2d`  
		Last Modified: Wed, 12 Aug 2020 15:17:27 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:7a3219e049b4d8b10a7ff389fa689c8d08d5732fe37dcf9c5a72fda463d6c6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:6aace730d886f9719841c60ec11f826e494b8fcc631378b32f5e01ca32d87ab9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e93a56bc1852bb18d91f1741edde016c59b49c92f7ad91960d583ee0486ebf3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 09:47:58 GMT
COPY file:27ab63fb5115ca3cb7456a256d6d6dab7ba864d8806821652fbe569f4f845df5 in /nats-server 
# Sat, 16 May 2020 09:47:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 09:47:59 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 09:47:59 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 09:47:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b509577c042697add820579de13ceed535b1c02ec7fa460b892d6c63941390a7`  
		Last Modified: Sat, 16 May 2020 09:48:21 GMT  
		Size: 4.1 MB (4087491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ce65065eb7bc6684476be5937b3d0d4046e7cc7241bc5017d70488d0edbfe3`  
		Last Modified: Sat, 16 May 2020 09:48:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:e8b59aabb2b6838ced59a3125ba4216cc8a4d0622f8b8c1e9e40fb30cd63a135
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8116ee7998ff454ed4eaa153438504925828993f56f26fb96fd11b31c9dc2128`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 15 May 2020 19:53:42 GMT
COPY file:9951c1b4ae20021f4d6efd6c039d0f0d0044470572e81beae625f15ffa13d2f1 in /nats-server 
# Fri, 15 May 2020 19:53:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 15 May 2020 19:53:44 GMT
EXPOSE 4222 6222 8222
# Fri, 15 May 2020 19:53:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 15 May 2020 19:53:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7976dc3d59fddf78c4ca25d0692135431e63b9fb744ae2c3d02b7a8214b5bfd9`  
		Last Modified: Fri, 15 May 2020 19:54:21 GMT  
		Size: 3.8 MB (3795898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b520f7415a5fab1b4a83eb7a8259e321475f75f5b06bfe95493b598c9ee9f4`  
		Last Modified: Fri, 15 May 2020 19:54:20 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:707f02b7c81a3f071abba9ce0a74b1cf0bf7a664e0220ab6cae112f2721a24bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3792273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2f2220669ef3621c45d5e4fd8460e7378e258044eb57003584ce55db5bdd9b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 May 2020 04:26:09 GMT
COPY file:3320edcd8f0db9551469809c752244493d1c6cf3be0287714c8a507e339283b2 in /nats-server 
# Sat, 16 May 2020 04:26:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 16 May 2020 04:26:11 GMT
EXPOSE 4222 6222 8222
# Sat, 16 May 2020 04:26:12 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 May 2020 04:26:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7ceefb66163b74f9719728ecace35bd406e85998a252d90c9e07a02582c7b6f1`  
		Last Modified: Sat, 16 May 2020 04:26:55 GMT  
		Size: 3.8 MB (3791795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db182fe235e1ef3b80de633e39d8ab9040cef44127adee97dbc4513df27dacfe`  
		Last Modified: Sat, 16 May 2020 04:26:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8cb2b90d45f90f3bdfb841b4a1399ff3a1b0a835e54664ee375ef309ff4c4398
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffbb615827376dda1ad45bce22763d7cdc858675e4eafc55deb2d134f813338`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 29 Jul 2020 22:41:42 GMT
COPY file:67a03d7df05756de9c16c4cd22dfaf6ed9cc9a43b78a90ebfaa81ee7ebbc7abf in /nats-server 
# Wed, 29 Jul 2020 22:41:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 29 Jul 2020 22:41:44 GMT
EXPOSE 4222 6222 8222
# Wed, 29 Jul 2020 22:41:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 29 Jul 2020 22:41:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:39a183ba93759b5fab08b0cb81f1f1a4c9f5a95c3746b031082c6bc3a57441b3`  
		Last Modified: Wed, 29 Jul 2020 22:42:18 GMT  
		Size: 3.8 MB (3776492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a510a0d87b5b915212ee2a5e5d877dced1c30164c0e82d6e60951d00374fe7`  
		Last Modified: Wed, 29 Jul 2020 22:42:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:3a169f34fc3f83e1d0b59a1e68d4e025b44c3fb7c86abf4821928a855b46bd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64
	-	windows version 10.0.14393.3866; amd64

### `nats:windowsservercore` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:4c298769615507fe26f26020eea1cadc0788d08b44e0375645292f7911fa8b68
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353839627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4815bfd4dca6cf258612f47848b3c6db32948cc50d1ce31085ac18bde7c31458`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:11:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:11:55 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:12:24 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:13:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:13:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:28 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1840e546a26b2d59dbfc9a31aa86b2dc8fed4c6c60f0f0a25921348b74423217`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ef50a643fce3c45da04f46fba8dca6f1f41a9d5ea4fddfaa06d4f9dfbe72a`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc9ff799390763d0a47806bfea8cfd0977acfe08dc0599806dbf48ebf777af`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb34b8a7d4aca227c853d019d08c475ab4d8c7b6389a75ee87d3101ddcba027`  
		Last Modified: Wed, 12 Aug 2020 15:17:08 GMT  
		Size: 4.8 MB (4795357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45b278790355e87ce684853f27667cd2e065c810b1123a9b4780ffbf146f646`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 13.2 MB (13166872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b984d8306d2ab511b3c646042d026055ffd2a68d00c99018060274f9cff2dd71`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d251bd0057684d214966948626fc693cc70910f6b968b672a7f4e73d3a277f98`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b110dedd427f4f8d4225ee04b10e8fd25c81021570b244aa5faa8b9118793320`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353c39efe6277128c4ae85f52840603d117b2e2af79fcb4eafa0bedaf6f6a616`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats@sha256:0bface4bb75895f9199eb5d6c903d4dfd6b33de95397efa57b8a68ec24d27c24
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5757484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96755e6aa9687beb1cbc44dbd19b93506cee5eee3735391e15cf738d0cbde5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:13:48 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:14:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:16:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:16:27 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:16:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff217b5d5bc8c8fb41e01c3eba376734cd65c568cbbdbad4f1b8ccb343094e`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6904aa06a0a62b5c80e74f511a5c8873ab6cb3f831cb07b8cb7d11c1dce548`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4e430ecc8ccbf747007a59ada2a242e3bd877de9f9f8340b68fe64dc16006`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f21f629b2ebf35877201ffedc54c17cc42ed1ff6d5a1b103cbc509fad733de8`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 5.4 MB (5391292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc789bee248747dae7caa25fcef8fe71174cbda62c0fb0ce6cb3ad9614312de3`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 13.9 MB (13935154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55d61fc54488846a758ce45ea5d71a778d33da5666007bdd5ed760d5387bf20`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043116cc2890a72214497abfc0adc7a287ea917ad5c29d71c63318e068e9d4e`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f6d4aab762740fae48f892182795785925e79465defac676880314cdeec2f`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994575a0eb610ea577e32ef234217e7cc59a26bd3cfe05726ddbfb9b7df25e93`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:a6ded0763c8f2024e25a5ab402647507373f70ad5c710a10b460a1c7ccd46470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull nats@sha256:4c298769615507fe26f26020eea1cadc0788d08b44e0375645292f7911fa8b68
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353839627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4815bfd4dca6cf258612f47848b3c6db32948cc50d1ce31085ac18bde7c31458`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Wed, 12 Aug 2020 12:15:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:11:53 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:11:54 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:11:55 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:12:24 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:13:26 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:13:27 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:13:28 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:13:29 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:13:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0465a83fdc9bb4320b7a8d4235d585e19f98779b5153f47841875a388f1e8a9`  
		Last Modified: Wed, 12 Aug 2020 14:51:50 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b7d15821cd04fba111e9927f3bdbdbc621fd70bca1502f9460991f9d58bb45`  
		Last Modified: Wed, 12 Aug 2020 15:17:11 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1840e546a26b2d59dbfc9a31aa86b2dc8fed4c6c60f0f0a25921348b74423217`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ef50a643fce3c45da04f46fba8dca6f1f41a9d5ea4fddfaa06d4f9dfbe72a`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc9ff799390763d0a47806bfea8cfd0977acfe08dc0599806dbf48ebf777af`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb34b8a7d4aca227c853d019d08c475ab4d8c7b6389a75ee87d3101ddcba027`  
		Last Modified: Wed, 12 Aug 2020 15:17:08 GMT  
		Size: 4.8 MB (4795357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45b278790355e87ce684853f27667cd2e065c810b1123a9b4780ffbf146f646`  
		Last Modified: Wed, 12 Aug 2020 15:17:07 GMT  
		Size: 13.2 MB (13166872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b984d8306d2ab511b3c646042d026055ffd2a68d00c99018060274f9cff2dd71`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d251bd0057684d214966948626fc693cc70910f6b968b672a7f4e73d3a277f98`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b110dedd427f4f8d4225ee04b10e8fd25c81021570b244aa5faa8b9118793320`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353c39efe6277128c4ae85f52840603d117b2e2af79fcb4eafa0bedaf6f6a616`  
		Last Modified: Wed, 12 Aug 2020 15:17:04 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:bf19d4980ecf00f544f3dbf73f06c7bd88adf27b537b1bc2d9d48ba37a850395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull nats@sha256:0bface4bb75895f9199eb5d6c903d4dfd6b33de95397efa57b8a68ec24d27c24
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5757484291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96755e6aa9687beb1cbc44dbd19b93506cee5eee3735391e15cf738d0cbde5c`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 Aug 2020 12:23:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Aug 2020 15:13:46 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER=2.1.7
# Wed, 12 Aug 2020 15:13:47 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.1.7/nats-server-v2.1.7-windows-amd64.zip
# Wed, 12 Aug 2020 15:13:48 GMT
ENV GIT_DOWNLOAD_SHA256=1e1ad5c00929cc145341fd65f8b0a41a38e942b9b9fd9fdb0216c47654afdc8f
# Wed, 12 Aug 2020 15:14:51 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Aug 2020 15:16:25 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 12 Aug 2020 15:16:26 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 12 Aug 2020 15:16:27 GMT
EXPOSE 4222 6222 8222
# Wed, 12 Aug 2020 15:16:28 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 12 Aug 2020 15:16:28 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:44c31749d2d4be3aede3e54780d9e54b5a7eeaa617e1adf027e92fce2ebf0f2a`  
		Last Modified: Wed, 12 Aug 2020 14:52:35 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966377bd81e347a691363116c353d48b02f40befd2b38ce2a9f31459dfe79978`  
		Last Modified: Wed, 12 Aug 2020 15:17:51 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ff217b5d5bc8c8fb41e01c3eba376734cd65c568cbbdbad4f1b8ccb343094e`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6904aa06a0a62b5c80e74f511a5c8873ab6cb3f831cb07b8cb7d11c1dce548`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a4e430ecc8ccbf747007a59ada2a242e3bd877de9f9f8340b68fe64dc16006`  
		Last Modified: Wed, 12 Aug 2020 15:17:48 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f21f629b2ebf35877201ffedc54c17cc42ed1ff6d5a1b103cbc509fad733de8`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 5.4 MB (5391292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc789bee248747dae7caa25fcef8fe71174cbda62c0fb0ce6cb3ad9614312de3`  
		Last Modified: Wed, 12 Aug 2020 15:17:49 GMT  
		Size: 13.9 MB (13935154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55d61fc54488846a758ce45ea5d71a778d33da5666007bdd5ed760d5387bf20`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043116cc2890a72214497abfc0adc7a287ea917ad5c29d71c63318e068e9d4e`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6f6d4aab762740fae48f892182795785925e79465defac676880314cdeec2f`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994575a0eb610ea577e32ef234217e7cc59a26bd3cfe05726ddbfb9b7df25e93`  
		Last Modified: Wed, 12 Aug 2020 15:17:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
