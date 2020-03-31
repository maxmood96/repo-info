## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:110b7a72f9bb2c35e85be3ca4c734f6a2769ff5c118d8f281dae9f1d69f2bc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:790e046d7d94efa0d895e27863c0a5914d7d22c507c797fcdca4760ab4e5d644
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45376163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7057e98a796b2d442e422efd22c22b9a1c9104fb3cbbee08bb98ed811118e394`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:22:14 GMT
ADD file:69f5027533cc1339a22a59ca6300ca7f9805aae39b104bc7910aecac86f212ab in / 
# Tue, 31 Mar 2020 01:22:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:22:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6d9d1acdfc21f12880d6ded21c7bf0d165bd42a39e5b0abd2f429e8d208ec4d0`  
		Last Modified: Tue, 31 Mar 2020 01:27:52 GMT  
		Size: 45.4 MB (45375937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a5951dc98a28279786b34b5ae0f8eee8aab6bafcbb288beb5016b92efaedc7`  
		Last Modified: Tue, 31 Mar 2020 01:27:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:7bebdc7eb817cc04524582782afa0b1346ed2bc8e13bcf56f1c7d04ac3e25461
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44066615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b50b5ed16cceef9396009a59498b23f46da5e5327b311afe26ce730af3d610`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:26:51 GMT
ADD file:94f4204e3c8ea359d329ec30d88e28d820e7a92f0f8e1d8a41bae1471bc7827c in / 
# Tue, 31 Mar 2020 01:26:54 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:27:05 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:46e969ea458005d33a932e9805bd6cd78a1821a6d654e4afae45a3fef9a61101`  
		Last Modified: Tue, 31 Mar 2020 01:34:45 GMT  
		Size: 44.1 MB (44066388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27595df776999ba0108f2cb0c0ca2dd3a1c11077e7216d5f55090cb5b91e462a`  
		Last Modified: Tue, 31 Mar 2020 01:34:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e7ff64813c3b748aa29b0d3ec469c8c03afcb34395e7610de16f35a2340d8158
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42100264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2410d32711eacbe0f3f42216e5559f76f792dd544d45139936c7ae59288e8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:50:01 GMT
ADD file:51b86ee6df84994a2b9d02ca32010998e2a4503b4f7ba1de1c1ca038048680f4 in / 
# Tue, 31 Mar 2020 01:50:03 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:50:11 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:53f26ebb0def979e770b7f9339d94909e3d53ce68232bbdfc55c7f9b59799b1e`  
		Last Modified: Tue, 31 Mar 2020 01:58:00 GMT  
		Size: 42.1 MB (42100039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b304d101ab823219bb6a8b4e86790eeacf27793da0a56cf129f16abc74537b34`  
		Last Modified: Tue, 31 Mar 2020 01:58:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:231206e9c584bb911c42c04bc93b8ef6ad3418e9fe75bfb577e59f6455798cf4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43158283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d644276d1c3328f1d917723092d43d35002d6f576446f2248af9af1dcf5f0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:53 GMT
ADD file:2fa68e91f233fe587be9748674cd776bca85a3c60ccaf7983699870d1838861b in / 
# Tue, 31 Mar 2020 02:05:56 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3e754ad4cd759ed3276bf3631cb87581678795e50d9ea29570f2e279876aa0ee`  
		Last Modified: Tue, 31 Mar 2020 02:12:34 GMT  
		Size: 43.2 MB (43158057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9278a83492400186ea2ff9e45bf5e9ba217f6fabfa85b06815f8910b2855aa83`  
		Last Modified: Tue, 31 Mar 2020 02:12:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:87b2c8c7b26e9be352053acad2df97166d416bc172d764fd50bb27eaacb59761
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb22481effecac4820b5513a0438147f4a2b4ccb0e1044049ecc497ea268876d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:40:58 GMT
ADD file:b489f99faea494de95b88e7ffd715f32c6869c152b6d74cba2fe56d3d1361b97 in / 
# Tue, 31 Mar 2020 00:40:59 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 00:41:04 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:74358beed00657e3379ed33bd54594508db48dcf1f67c0cb4d1d7f01b7c1fb9a`  
		Last Modified: Tue, 31 Mar 2020 00:46:54 GMT  
		Size: 46.1 MB (46095207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a336d41cb4ce9944c6cffab2e6a5a3aecf89a14d378b175415bc36dd9ced91eb`  
		Last Modified: Tue, 31 Mar 2020 00:46:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:51033e884c1fce852fae2ee0ba539ff165b5c8448743cc68ed406b073bd832e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45647419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e8e862785e4d78761e362730e130ae262d07de565694dabacbc00ebf8ee93c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:33:08 GMT
ADD file:2f212725d5637215e74f5b0c73be03ae91f62f01e77df0ec107e999e32bd39ee in / 
# Tue, 31 Mar 2020 01:33:14 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:33:31 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e73529c2317bb1c57cc675a54a51078ba8d01658c9dafa554c21724868386335`  
		Last Modified: Tue, 31 Mar 2020 01:47:09 GMT  
		Size: 45.6 MB (45647191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d215cae1df07d1efc7e33f1124a701381fe04d2bb0a84562cd319ab0cb17af`  
		Last Modified: Tue, 31 Mar 2020 01:47:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:7e427bed4cd8864f7f900f4c080004f58225608602137d7763f58f9d2c4d6282
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45233143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293497e1f5dbf11d5bc3b299fd80b92fe1fe24635856ad0f77495b2a15114db9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:09:10 GMT
ADD file:24d29625c5922133acc29fd4e08ad35185c237ec2e7d11e5f05d9a049eb61a70 in / 
# Tue, 31 Mar 2020 01:09:12 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:09:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:07f7cb0fe52922285978c9f1845890cf102f02c0841e1918e8e57c8cb067623d`  
		Last Modified: Tue, 31 Mar 2020 01:12:54 GMT  
		Size: 45.2 MB (45232918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf67ce00e4e7ee25aec87c206ee897d3b1995be280dac5277b961386afb16074`  
		Last Modified: Tue, 31 Mar 2020 01:12:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
