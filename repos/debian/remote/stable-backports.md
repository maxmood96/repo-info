## `debian:stable-backports`

```console
$ docker pull debian@sha256:8867298ef625e885ecf2d57bafe75b901dbd1d90866acfd2a177304569026444
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:f67d2ba3f6f027a9f480c6b9e0957eb06202d1979bb21d1d749743a96ba5a274
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54915181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1162604d338aa762554ad38f723a44c15aca88f28065bced673d6679c6b8c43d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:29 GMT
ADD file:d78d93eff67b18592997e4a9cfe93a931f491d5746b1395757900a8727a08e95 in / 
# Tue, 17 Aug 2021 01:25:30 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:25:35 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:605e0b7dff222134e8a75c955360e1f18f9d47f5126da3ba0944f0189b330254`  
		Last Modified: Tue, 17 Aug 2021 01:32:27 GMT  
		Size: 54.9 MB (54914960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd2e319ee0730e8c0305827411cd3fe8bc42e35b1c37f59a167385bd399ed36`  
		Last Modified: Tue, 17 Aug 2021 01:32:37 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b12a8b4f6c8f26f2a58fa09a36b1da49dacc6377d30f440ec797dc69e2a1079d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52452460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b15da2a2f2cc1c3a1e633398f2c8ac6059ef61d729b443ea985276014a3905`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:59:54 GMT
ADD file:09b4fba795efbd59c1ff740e62512562be4fe6bd0fffff325e9d65441f279bea in / 
# Tue, 17 Aug 2021 01:59:55 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 02:00:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:63c31ee77d62664e1ef5b52159b432fcbfb17f0becffaab4af05907ac03bf584`  
		Last Modified: Tue, 17 Aug 2021 02:17:21 GMT  
		Size: 52.5 MB (52452236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac68b019678d80936c46ce992eab3e80aa8dc3b885e6e518f750c56053ffc04`  
		Last Modified: Tue, 17 Aug 2021 02:17:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a9fffdfebe747a9f6963dc29fc7f0634fc503cd7feb7f5ce8bc0f61f7391b235
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50118742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868aefa075e2f279244ea08850a3ce17b7dc98111cc44122e5f25855a7d532ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 02:17:57 GMT
ADD file:c760254b3543f79b329514490ce5feaba795673bc67b9634dfb125d2a882d55e in / 
# Tue, 17 Aug 2021 02:17:58 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 02:18:10 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:27da5568e47d0918812339fc7b455d84d3a9ed79fc41697df08f754ade0cb388`  
		Last Modified: Tue, 17 Aug 2021 02:35:08 GMT  
		Size: 50.1 MB (50118520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc722d9357e315400657a0606fb64fdf0e10bcde3edfe2d5861e665e7fac6a32`  
		Last Modified: Tue, 17 Aug 2021 02:35:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:97aae2079e726c01f19591a111e11c4afb5d8cf8d8549b403694ba29259068eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53601225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf05362411b2bef2188c1180c32624a34d7ae018a58aecac24c03be5e9056ac5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:47:52 GMT
ADD file:de81648694d4fc136ce1e7412d72239cbec6e8455c5918bc0b8d46f986d63d65 in / 
# Tue, 17 Aug 2021 01:47:52 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:47:58 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:154de8a85bb9b01a3b352187948ebda6afa69804dd742e16999175d56152eabc`  
		Last Modified: Tue, 17 Aug 2021 01:56:50 GMT  
		Size: 53.6 MB (53601001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07770e691e32d4224909e3e1795f6cffedd1dd69e34218c99c5dea348f1e84ca`  
		Last Modified: Tue, 17 Aug 2021 01:57:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:231460bd9668a321b1c9a7fc82b791c1747fa0c533e17a5b18b1b93664cbd2cf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55922755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa0fc488da2236227534599c8d3d532572c7358341d25097b35694550dd96d7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:43:11 GMT
ADD file:b2099f8d884847bc5b33a0673bffc6772575c1036d40bde7ab9fb5febe3090e4 in / 
# Tue, 17 Aug 2021 01:43:12 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:43:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:47f762a2c1f73f6bd6f37f5bd1915187dfcfa6a7ac234aa970d396c3fbe82bc2`  
		Last Modified: Tue, 17 Aug 2021 01:53:49 GMT  
		Size: 55.9 MB (55922534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfecf490a9be6bbcbc77593e0a0a99b3e1b244004522f1ee869379cd63e21633`  
		Last Modified: Tue, 17 Aug 2021 01:54:01 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9e3f792a7a581003b39cea0565aa7374cb960a6862f8c016b624c55eaf31e478
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53167500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8336ba2c2f4b4b1adaa10a0940958a48ee254a322909807e73a92e495da57508`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:14:35 GMT
ADD file:2d7e0632e94c14e727abd071c43f507064f876f70d39ed72cf3a825dd6c33397 in / 
# Tue, 17 Aug 2021 01:14:36 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:14:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:31d8f82cc0e98ad1cbee58906296b760fe8981a49c1cbf4427c97b0474d29add`  
		Last Modified: Tue, 17 Aug 2021 01:25:01 GMT  
		Size: 53.2 MB (53167277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028686d946fdb8948161eeb156cfdb0bd415412eca3bbb7355b06aab6e9d2b1b`  
		Last Modified: Tue, 17 Aug 2021 01:25:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:81092ec107395dec013494f58845a3c46508c94a9d4404a0d880cecb40c25380
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58816237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b94f26ed9f397b877681d1649780b7b18d73cfd6bbe1d7e7821c6b6ab095ab8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:36:37 GMT
ADD file:23256073db29a84820d84edaab7d9504beac7b79915b10f6b32a888386c76a22 in / 
# Tue, 17 Aug 2021 01:36:46 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:37:01 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4119e80fa24a562e59928b2f97c1b3903499f386e7646a33350bf49807386b3`  
		Last Modified: Tue, 17 Aug 2021 01:54:20 GMT  
		Size: 58.8 MB (58816012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb07a04ff87ddb3cd0232af2bbcf2943c21904004ee6444e4266d5829f0c064`  
		Last Modified: Tue, 17 Aug 2021 01:54:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:8917ba2b2155212d68c6f076e295c90579f906f00a19c2799e8c30fa6ed0ff3f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53194231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4ee6c62c81a574548cbb80d0cb9ba9e9e71da999bb448e80fb7590ff9eca9f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:51:49 GMT
ADD file:d47faab4d1cf76f2d349a57092fb9c3a19ab807b4e06168f07bb61898ea9e2a0 in / 
# Tue, 17 Aug 2021 01:51:58 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 01:52:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:717611c3045b312153e954d5de5687ef4181fd17fd165c58a642a130ddd8124a`  
		Last Modified: Tue, 17 Aug 2021 01:59:29 GMT  
		Size: 53.2 MB (53194009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1172664fd51ca5ece28a28553a6b9b74a228f5f5979360549a523f0a043246`  
		Last Modified: Tue, 17 Aug 2021 01:59:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
