## `debian:buster-backports`

```console
$ docker pull debian@sha256:f3439c3b42fea92387d0cea70d7c849245527bd5d9340f5f33a4cd177edba1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:0a32123fb8ef69eb6adf196279d607ab0ff37fc40d17dd70613a8ced047f16f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50501021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5705d659165653a45f7ceb36e233a2e6bc0e22defb41216bdb5140ac14da2bf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:33 GMT
ADD file:4c836bb72137197bf8963c1982aba28db2b125a4276307783f46668bb4189f34 in / 
# Tue, 12 Mar 2024 01:21:34 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:21:38 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a9a7bf5145e4a86e137c0a7612407b53eb4b97f73f4d6f15a64c2d52c682b500`  
		Last Modified: Tue, 12 Mar 2024 01:26:38 GMT  
		Size: 50.5 MB (50500797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542cffba015c94d9509593cf7a8292eaa141733173d7df99f893ac7b9be8bef8`  
		Last Modified: Tue, 12 Mar 2024 01:26:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c83d4a5e1144464dc6ed442704ca7738adc07fd698fbd47ca173719a6076b502
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45967492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada747c4a28a52cf6530ae9b226eed05433b033f3c27f8097ca923d80af9cde8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:59:51 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288920e25a021a417b06c68052ca167d371e90847107bb56aa90ceeb4e8282c`  
		Last Modified: Tue, 12 Mar 2024 01:04:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4c8d897f5bfeded74e8b6f38ca5e7b5af1860a12eb7609705022292a00a3d5ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49290057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d422ffc743668296aa17ece6e9a80357d34cdcd1a40ed0e1ba6c0eedb4e5e54d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:46:01 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53894a29dce12b83ec96b9f04c7bbf661605d830aba6e0cd2767585f831db023`  
		Last Modified: Tue, 12 Mar 2024 00:49:59 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:2bd6fb23c096bad178c61871ca1fb2b632923852687a83162ee495e58df9a5cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51255813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd0ea04b2772bfd903c0185f48ae8818c87c8ebda701535f8b34a043405cab3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:33 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
# Tue, 12 Mar 2024 00:58:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:58:37 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34df42f72f06538a3f41d1b6032431594ccec9ca21567697ca80b206e5198ccb`  
		Last Modified: Tue, 12 Mar 2024 01:04:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
