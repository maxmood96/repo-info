## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:e11c59910d1dd7eea71571c5aaa4602b03abfaecdd158d0a2edfea1f2e148a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:644e380fcf6f318f966991277356b10bfc318734c26b7e07de314a324c8dbc68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45381532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960fa48868e2fbfb9c23c02b0f5c80994500a44a0395db955d3d2538a9c7430d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:14:08 GMT
ADD file:12ca75aeaa8bc075b3e66c6cae47b7d1366e748e9e6020c1e636d0eb6f44e108 in / 
# Tue, 01 Mar 2022 02:14:09 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:14:12 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0e9e73d6df7c89c01fc4efe2b52f644329682437b5564dbf1e5e4a391e507fb9`  
		Last Modified: Tue, 01 Mar 2022 02:20:27 GMT  
		Size: 45.4 MB (45381307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ded98fbf57e6c83cc181b0a5f7c99938cd8278f56416a8b99544edacce0ded`  
		Last Modified: Tue, 01 Mar 2022 02:20:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:22f9c94790c2cd8aedfbed1d34d4b4db9626a47dfcdbdee54f632f6d6df0ab59
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90db6656d4a4947ef89fb39ac63cc2b5f70827da4c93b623fee7622e61c8b2f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:04:24 GMT
ADD file:4496da4dac08bd7a3acee93f8beb43c53886ae0c8ab276fc5b5895b10c9cf1fd in / 
# Tue, 01 Mar 2022 02:04:25 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:04:38 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ba330ccb0e1e0c8726c0ff4a98243e9d5b5f94e50439af8783e68622f636005b`  
		Last Modified: Tue, 01 Mar 2022 02:20:49 GMT  
		Size: 44.1 MB (44091891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7c96db920cb3ebe508b85c51d45108dfc25675ba9af90c29c7b00302f7cd6e`  
		Last Modified: Tue, 01 Mar 2022 02:21:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:23d98e314b99078a654a2dca3bf3cfa391caa21b30c9a433dc2e7864579d9cea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d030146122d825ac63336040552cc741b3d5932c90c75f5bd5f3a5a527b1ab5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:04:38 GMT
ADD file:2de911706def6a70a727d0876f9b79b00ac67ac95eb77820c416c9382ed369da in / 
# Tue, 01 Mar 2022 02:04:38 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:04:52 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cf66fa9e634b7cb4e5375fa422382862d3fd22eb4117a81f61ce557b5343c656`  
		Last Modified: Tue, 01 Mar 2022 02:21:08 GMT  
		Size: 42.1 MB (42116978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e1599d29d749cda23ff62ff45cd7def4c3e6cad2d0f77668020204486001a`  
		Last Modified: Tue, 01 Mar 2022 02:21:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7c0e33b01b718b0140efb3ca229fcf806e28b6443327878a7e33a6b453441106
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43173987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2060d11997f7cbc78e33ab2ee658f99dc500a357c6fbaf0237ec309d0e68ede9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:12:08 GMT
ADD file:fc07f16f09671740c7c3828609a952c8c8b2fc43e27145fb76fd4bbf99ad4576 in / 
# Tue, 01 Mar 2022 02:12:09 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:12:15 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:867e2966ae0ca6581fd6e6a3142267a422769f77a5b5d07df94e43a263fae8c9`  
		Last Modified: Tue, 01 Mar 2022 02:19:37 GMT  
		Size: 43.2 MB (43173759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7348abf6ac5b5d2a752f226c6a5055c84924a009fad6eeae3a794814e8e7d497`  
		Last Modified: Tue, 01 Mar 2022 02:19:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:17e065e6d4cb9d69f49f1cb19aba55e0277304bee3d6822ae0dfc2a7147bbf25
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b28d02826bd624898d41d191371ba2e7f7c91c1dea8e3942e2f3c0d437215d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:08:18 GMT
ADD file:616b277ee8d6bc42ba695efe81130ef053a7977b5be00cb73cc4d39576a3d5a3 in / 
# Tue, 01 Mar 2022 02:08:18 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:08:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ca7163875bf6b80d6d02cf73a0d99447fb3509074bee6b59201a75f6abfcbfe6`  
		Last Modified: Tue, 01 Mar 2022 02:17:19 GMT  
		Size: 46.1 MB (46097767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb35d1c77179dfc0bc4360563009d2046c889d90c71b77aee5c7818175fed4a`  
		Last Modified: Tue, 01 Mar 2022 02:17:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
