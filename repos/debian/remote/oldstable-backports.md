## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:528c638d5d2b21aa4a8e3a793af65327c6b5e186bf756af91259b60781638b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:8971deabea664a0b341f02fddbb5205a63e1470af5c0383a378a351e222d0930
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50441011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c513fb1a5dd666aaf5b745dbae58ff914487ca051b2cbae2f9ee11aa4cd210e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:21:14 GMT
ADD file:cc42a7d35200c41a033897dcc1bc1b1ddc70951895c7b7437852c8207ecdc432 in / 
# Thu, 23 Jun 2022 00:21:14 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:21:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a968030a9a193719b095406e53dc080102416bd788bf2ada491ec6974341e34e`  
		Last Modified: Thu, 23 Jun 2022 00:27:52 GMT  
		Size: 50.4 MB (50440787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1f7cd3cefbcfd2a79050bc6b56ab31120fc08a80a5b58f43e25fa0ddd966c5`  
		Last Modified: Thu, 23 Jun 2022 00:28:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:72cecc5d5a1a71bf50f6c9f5710d12c8ef473db1415323828b73d10e163e4a62
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48160934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8209dceaebc92a89bc054a78d195830c9320ebedec3eedee56a4cdc8ca86516`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:52:59 GMT
ADD file:19ddfe76cabb19b518b23185bca94f3281e30b56078415c5681d617a24489af2 in / 
# Thu, 23 Jun 2022 00:53:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:53:12 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c413e5d0c8a981d1baa42915636bbd91999e3585fcaf4ff4d380099ecd15c94a`  
		Last Modified: Thu, 23 Jun 2022 01:09:10 GMT  
		Size: 48.2 MB (48160707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2f8ec7fbae2f2ba4bab7e095e5e52bbb218219b77259dc046735766658e3ee`  
		Last Modified: Thu, 23 Jun 2022 01:09:21 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:980c785334e5f8d64f66588cd92b8c9798add485aa968267337ccdca52063540
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45915983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e47c37d98ae442c15f65452d511874186be7bd62251ef9abae47bc2e4e1c3a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:02:16 GMT
ADD file:28bcd1219a77728f9d7a74b36844de473d1b6400a2a87deb6fb0d7993f2ff790 in / 
# Thu, 23 Jun 2022 01:02:17 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:02:29 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c89ce61fc8b89745cd320b95306ded5dde5b9b933377da870a6ddfa045ed645a`  
		Last Modified: Thu, 23 Jun 2022 01:18:38 GMT  
		Size: 45.9 MB (45915756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3d2d9eab63b724b9675d8413f26d289917ecc7ffad0748a41f3d1a7fab63f8`  
		Last Modified: Thu, 23 Jun 2022 01:18:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1599ef0c6ff617d6348d50d1e583212155d4fa30408ece41001c5968639ead29
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49229291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0bd1305be5b4b9d0e66679a077b85447a529cbf546c7296ec0406fecd02ac1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:41 GMT
ADD file:61035f9f45de34d5d5d9041133a493828d3e6d587ef3a935a1a9fcddd5b903da in / 
# Thu, 23 Jun 2022 00:41:41 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:41:47 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5cb0cbe6f8df51aacc0d56f62105395fe085f2632b70bccc9b48e49f4ac93ef3`  
		Last Modified: Thu, 23 Jun 2022 00:49:17 GMT  
		Size: 49.2 MB (49229066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3cbe0726f9a4f07e7ba76ba8711d701f28f94b1c42ccdf78491cf4ba98f91b`  
		Last Modified: Thu, 23 Jun 2022 00:49:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:c8a2fc5cc585f21746c6814973637acb779a1defd955837cc154b1d0bf6269c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51204453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df853761279ce403b96a57e2677bd92d21096c6fde14dd2f472dd9d67dfef98`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:34 GMT
ADD file:325ae63a08ae7a80e6abd8a7180b7c60546a19321c0f26a04b4a7ede67deafa8 in / 
# Thu, 23 Jun 2022 00:40:35 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:40:41 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:da27a113be2ff193c5524b9b471aadf6f8dc53a2a8b0bfc1f33f72ca5918d392`  
		Last Modified: Thu, 23 Jun 2022 00:48:48 GMT  
		Size: 51.2 MB (51204228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd8f28d3252089b586f2ce27669251a247ec8d272b75a81da5c7b75e2f5f9a`  
		Last Modified: Thu, 23 Jun 2022 00:48:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:4cd7b9e8559eb855d50de480d01a5a55a340cda9e7f61fc300fc27cc759564d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49073591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4c614653b050569beec574f515aa0ffb39a98bf3f8ca6d84099cc46292583f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:12:54 GMT
ADD file:eb19dea96494052de4c2ea2ee51deb090eb008a2a39eaa9e1a623f1e7626e3ed in / 
# Sat, 28 May 2022 01:12:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:13:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d31bc4793744d8e909ed41c309a0633dea29816d12adde39b5f4b34fcafd2334`  
		Last Modified: Sat, 28 May 2022 01:23:40 GMT  
		Size: 49.1 MB (49073364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799d8ea474d0531b52435746317c28a54835bd3466eb05bdf0840d4dcc2e0584`  
		Last Modified: Sat, 28 May 2022 01:23:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f9b8defec7095603f88becd4a390a97a4f17b29a82b595fe7a9e0f6e4b2851cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54177244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27df5f3699a73c3703c831b2e2c3835dbc65a3e143e56ff0157951eea22c7dc5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:24:21 GMT
ADD file:f0f6279b8fd985287b5f3df9480f1840f5d0b4a3dc72e3f373b89757ef9a9077 in / 
# Sat, 28 May 2022 01:24:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:24:41 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a049936bd2803fc7c63adc8dfe2c2a7792bb32515dc427cf69787f3b0d352df`  
		Last Modified: Sat, 28 May 2022 01:33:59 GMT  
		Size: 54.2 MB (54177017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01444c9d05003105f5d9bccbf299bcf82a819ef0ef8f7fe3d31ed72d3b6b982f`  
		Last Modified: Sat, 28 May 2022 01:34:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:bb4c5ec020e060674e8be99a84ed75ab551b3f461c527c71a4a2803cf21b80a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49007446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4211e539912a38b60cff5e8900096ebc5ed3edfcdf776083056d7bf5b742a6c5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:44:26 GMT
ADD file:9878bc65a192de996310af72af80c3fa71f0b9dbe97131e78d523779ee4f2c02 in / 
# Thu, 23 Jun 2022 00:44:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:44:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5fa9cc6ae7561b5fb435d3b1c8606cfe94f56de5572ca9dea139e48cd048ee9b`  
		Last Modified: Thu, 23 Jun 2022 00:52:51 GMT  
		Size: 49.0 MB (49007218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2025d76481377b74938d85f1b67be5cea7d33b90343e006c62e437de6c96dc`  
		Last Modified: Thu, 23 Jun 2022 00:52:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
