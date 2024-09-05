## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:2cac1a0860692d635f0ad986d30376aafa968d4b298b19444d2ffcf39f701cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:587c5237c1e5dcc34ec56b86e7e99f1483e7d0961409223ca4885fb9f87c1ae6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55081554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96222013099acc06a8cdab30238fcfd8b96e1a7cdec4e8ae0c290d0f068a7830`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:31:01 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5242fee86d0d06ed9d60be701bfce4941547befcaa9895a766d67c2721633d68`  
		Last Modified: Wed, 04 Sep 2024 22:34:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5f19863cc42ca28cde7eb0d686a1550a9346a72eff8a5aeb84b0a7896494c903
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52582978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14716fbfe160ee6ca09c32970f1ab51568c1d6d7bf5701af3d7a8c36d8c28115`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:39 GMT
ADD file:f6ccc0737bdcac3d7694a1fd4ab0609c22377d55dbc283a021ed8df0d5ee807d in / 
# Wed, 04 Sep 2024 21:48:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:48:43 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9fc6954b7a342e92200747f4676bd2b9223d22aee96dec921c2d55657e0bdaeb`  
		Last Modified: Wed, 04 Sep 2024 21:51:52 GMT  
		Size: 52.6 MB (52582753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e3dfc7fdf05b83c7cd2f0cae4485fdd8ea29596cb0b94cd36f3db772a10ab4`  
		Last Modified: Wed, 04 Sep 2024 21:52:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:335838d0609d9add7fcd697f469b3316c1da7f8bc3bf4693eb76025af95b2b0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50240500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae57fa2550ed4cdbc81baae2e63d194e4c93a614e0192bce45301223fd1d020`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:17 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Wed, 04 Sep 2024 21:58:19 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:58:23 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d65d1653752b7dc0dbb4dce6af742732f48cc4edc718fabfcc94e091965b9a`  
		Last Modified: Wed, 04 Sep 2024 22:02:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ebddd62f54fcc5fdb535f48f66fbe0ddcb5b31373a97e9d3c2ceac5b344485d2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53731844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37768909c0dd4f8b4ee5a31940c12dd7949e64fe34aa706cca6a16061ccf97b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:40:03 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e521936ffcc25ff5e098e2a719f2b4421eafc65ef511668c6de4e9a030a9571`  
		Last Modified: Wed, 04 Sep 2024 21:43:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:21da4059ff47c37ef7a4a6ba48b424bb32fab747f02a23a3c4e725700dcbd41b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56076394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75402b4a916ee50eec8b2a447a97902877a2f6e1604011acb4aae62597dc4edd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:44 GMT
ADD file:1d8ae4e7067486ce0279b3d90aaecbc5973872ad64266d252bfa3fd5e4fc2e5f in / 
# Wed, 04 Sep 2024 22:44:45 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:44:49 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c6549675a9e3cbb8e77f08089828d3b4f24a06d332dc86c4d140aa273748ba57`  
		Last Modified: Wed, 04 Sep 2024 22:48:29 GMT  
		Size: 56.1 MB (56076167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081f3e2acb198b98e76ffbf754df57c0cdc911109c6694d14243ade2e17920be`  
		Last Modified: Wed, 04 Sep 2024 22:48:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d5351da9c30198fb2159cd5a152bf4782269b9eab5c0debd3f1cb14f61ed60bd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a959c3d70d038d357bcb27561e48d94101bc995c2eb05c8fe1b5e347df34fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:03 GMT
ADD file:af2c25052aab46bab5ee70bf1b7f7c8d0339d147a2bd4daeb04ec25bd34e4799 in / 
# Wed, 04 Sep 2024 22:26:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:10 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a8e5e0425eb7845f41056f6e5fe36c228a23a602de31f39d88868def2b2bf980`  
		Last Modified: Wed, 04 Sep 2024 22:30:31 GMT  
		Size: 59.0 MB (58950090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f9d5271e63ef01e701a2e95ee8c10aa9a85a454fa3463cacb1d224629e0025`  
		Last Modified: Wed, 04 Sep 2024 22:30:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:bc46a64ba6d77cc7e75e70ff63a0599fe59cacc170aaa8e329cacfe73b32fd51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53317424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09b992875b6321f1e421b8f18da5b660b50baf4265cdba2b44e73150eb5dfad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:05 GMT
ADD file:855e3f68f57762c16941f4426d4c9911e4dcaf77abfb6d1993bd8c8f0d7e83b5 in / 
# Wed, 04 Sep 2024 21:43:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:43:16 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:52560ec7a98b7f8127e927ecee98fe2d97be23a6a2ec8ffbbb0b71455e06dc54`  
		Last Modified: Wed, 04 Sep 2024 21:47:54 GMT  
		Size: 53.3 MB (53317200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e56952e14d49ea8bfe83adbf445431965d325f4cc698a760db03ddf20ae687`  
		Last Modified: Wed, 04 Sep 2024 21:48:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
