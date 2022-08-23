## `debian:testing-backports`

```console
$ docker pull debian@sha256:c5e0598c992792e8577c4aee034880e38634c0539fe6e7e71f285a36942fe71f
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:065300942d15b1ebc37d42fc9e6289d3314d074f9f6e177f01b1099abc8fbcff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52725936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975fd0fe254189d5a73a5f3caa63807c47e71dd3658dc1d2481e2ab73b979ccc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:22:16 GMT
ADD file:46ac30e868d9fa053938dfd03bd5a6d46502ac44f64d96a4c75a40348ab45066 in / 
# Tue, 23 Aug 2022 00:22:17 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:22:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bc2ca2f3fe9546b1f10765241eb47f197756a844ebd3f82ecb85477801779ba5`  
		Last Modified: Tue, 23 Aug 2022 00:27:47 GMT  
		Size: 52.7 MB (52725712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041ff16a1c23fe5925f1940b68819d80c38456ce721bdfab893552e8df3a1a6d`  
		Last Modified: Tue, 23 Aug 2022 00:27:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b0657a1d6a1aed60a95a81a81c9f4983e2139aa2ab9af3c3e2c0118e5681bc99
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51814280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a0f9b9f2b84a6ee2bca8b3ed534658878218f6867a8429ef349e5d061f7163`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:18:38 GMT
ADD file:f6ae241f3c501de7b69ce668d8e100dc91b43dd4738fedfc5b7c210b10cb3326 in / 
# Tue, 23 Aug 2022 01:18:38 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:18:44 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5c866ac365b30c758a4a9a46c1da0657db06a86a29434c9ef3215cac6bf808ea`  
		Last Modified: Tue, 23 Aug 2022 01:24:53 GMT  
		Size: 51.8 MB (51814059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f824406f3e2bd147eca2130c5c57ac588fdbff71b4475f77d751c95e2e53b91a`  
		Last Modified: Tue, 23 Aug 2022 01:25:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:5e8ae8ef450d8760d94d4bb97f4649fe79ebed6eb5680c83b7d1c65131068047
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49555336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de06ac825bcda6eb595a6acc050957e57b394ca449c08dbcbdb4eec4d95259`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:45:36 GMT
ADD file:3a189fabd18a25649202e19fada53edc913c92c596b1234c0936cc621226692e in / 
# Tue, 23 Aug 2022 01:45:37 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:45:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7e1855cae120824d8b8b204aac8c76fd1d169615db57ced1ccd3cf0ca1e6368f`  
		Last Modified: Tue, 23 Aug 2022 01:53:32 GMT  
		Size: 49.6 MB (49555114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a352c50971ca235c107977bdd43496a7770bc4e3690a32031688d878d16bba5e`  
		Last Modified: Tue, 23 Aug 2022 01:53:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:160d736f2ef7e330b8078c43e0036e4a203c319013afbc317cd03542d5dd48d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53117767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e067891fe7465a1ea278d099a68ef8ce0b9a5cb27174a37c72a7a868be6b66fe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:54:16 GMT
ADD file:5feea900f1cb717b9ea13acbf6f2d7be123e4b83e550e0121c44dcffeeca226e in / 
# Tue, 23 Aug 2022 01:54:17 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:54:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2d7e20893a70b321d1c8a4b612d35a510efd826cfb1d665534f9dd1cd15eb956`  
		Last Modified: Tue, 23 Aug 2022 02:01:03 GMT  
		Size: 53.1 MB (53117542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dec2ba65d5fc88472d7857f5d7c1fb8aecaae8d2e2451c51afa7b10008238d`  
		Last Modified: Tue, 23 Aug 2022 02:01:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:e47ffefe9d77f96dc1368d77eb1c30deea4eb35906ca103e2af9dd733383d447
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54097252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13dce6c9081c8b1e766c46f2fafe5d145f6d1d5d29bdaf40eadfa04bf4fa95c5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:04:28 GMT
ADD file:364ffb1c2691887de798917d234954fb0eb7c72137489822bd12bd6194cfdec1 in / 
# Tue, 23 Aug 2022 01:04:29 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:04:35 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06240d8d46075ea69ca3a286305ca352bcd6ccf14658ebad53126670dbd52354`  
		Last Modified: Tue, 23 Aug 2022 01:11:41 GMT  
		Size: 54.1 MB (54097027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d33488b435129476641a474c0ff40d216bc3ed0cc765db6615bc700be026931`  
		Last Modified: Tue, 23 Aug 2022 01:11:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:00a0b943ca8239fa64cf723d4582429321a5972222072cbe7405fa03d2c14cc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53119599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e037922a85e4a5eacf097d342491014b01d0d0920e6160ea6e286179cd7e93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:14:12 GMT
ADD file:f3e9e580221d3e94f0fb61e58fcbf318bc042add830bcdd71dd0983d138c3b0a in / 
# Tue, 23 Aug 2022 00:14:18 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:14:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d67983489079eeb3b8ecef40d659bc0761c151e192dc6a219e80b494d3ef1685`  
		Last Modified: Tue, 23 Aug 2022 00:22:47 GMT  
		Size: 53.1 MB (53119374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54e598f2f73878c653030f8a3e0d9ad2e90e0e2b6ac805e5f30e37094a4c9fc`  
		Last Modified: Tue, 23 Aug 2022 00:22:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:51c5ee4b9c7bf2e3ac8a739eb211125de1f22e01272ec1fad62572e7d82bab26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57290098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a218f72898ab59522e72852fce60592021339abc05f8c2a4cc80bb543fdba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:26:21 GMT
ADD file:35daf34d4b9f7c9f63a3058d75300b029515bed52adbc8b7a87a5c09a93019fe in / 
# Tue, 23 Aug 2022 01:26:24 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:26:30 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0fcef4ef26ce0a4602ae0238ad72b59e19d865c22413f6b751fbedb72875c424`  
		Last Modified: Tue, 23 Aug 2022 01:32:45 GMT  
		Size: 57.3 MB (57289874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e71cff04e78161bf3d173a360cb86ebe0758b75c0268fbbfff029a9583420a`  
		Last Modified: Tue, 23 Aug 2022 01:32:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:01afef8e4433c3e7702f20e8d4c8df79fb468d264059039d26d2384343c806b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51559783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff425e590daf3bc71e17d5f87b2b1d1ae9cfc44a277052e32885754d8404d56d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:55:05 GMT
ADD file:cadf094a1d6082add0bf2676908ac8b6840011da1c0b8dbfea3ab032d5b2c34e in / 
# Tue, 23 Aug 2022 00:55:08 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:55:14 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:82d1ba4a21c98b7422a82a6f3b0a187fd387550e3801b784d043655072916c8e`  
		Last Modified: Tue, 23 Aug 2022 01:13:13 GMT  
		Size: 51.6 MB (51559560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e591f0b2cf5187f37d6a29ecf0497a938b1b46764e0cfcc1420b6ecaade0d32`  
		Last Modified: Tue, 23 Aug 2022 01:14:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
