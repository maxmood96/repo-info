## `debian:trixie-backports`

```console
$ docker pull debian@sha256:97b050b24b04bacef6a4d3652627a5dc85fba35ff4c71db289017dd079a36d94
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:3168b88d2ef04836496da2e0f613077e94f15291f4f5340252c1b071e8749809
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49596909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab6b25e68689f589f9cdba17adf743b7131484e9daae056b569825bac3d8753`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:27:28 GMT
ADD file:8c4b165f14bf36d9d8615d86e330e2619791a9af4f7c82ed8489717ca4584aab in / 
# Thu, 27 Jul 2023 23:27:29 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:27:33 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c96befece94d6ccacf8c06c689180a6d127f115525a8914bcc579f9d88d893cb`  
		Last Modified: Thu, 27 Jul 2023 23:33:49 GMT  
		Size: 49.6 MB (49596684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51808ad42a6e4d118a4a9b1959c17a9756ca7115b1cc7d5bdec7e01b4fc4f530`  
		Last Modified: Thu, 27 Jul 2023 23:33:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:f679585d9a23b22788344e4478cb003f57cd0f4516d38483490cc187db9c7b75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47416044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0809dce835d2c50debbfd4084dd37dfaf6335ad6d887e34d8b161dff4dea46f1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:49:56 GMT
ADD file:b4373de1d38fa5e12e9cc988f4efe7d63fca5e7a0e4d1c3b0b0eb08a4785f706 in / 
# Thu, 27 Jul 2023 23:49:56 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:49:59 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cd27c4a7a2cf7bd1109907025d62ebee5f467867ff721581a5c9b771fa17669f`  
		Last Modified: Thu, 27 Jul 2023 23:54:43 GMT  
		Size: 47.4 MB (47415820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e278d5ece788d11cc72296db218d19da6562f3bf6e656e0fd5bb20ac1b077c`  
		Last Modified: Thu, 27 Jul 2023 23:54:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:15cd142db2228ac36dc64d7aef39daf015ea0ec8b17b822716c1600f482fe23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45212485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da9097ddd964572ed429bb0de17e1b182ba077acea0689b1aa2cce93119c2a3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Jul 2023 00:01:07 GMT
ADD file:e750a7c315188d832ff98e8e33a2e78c68efa5a12bb17c8f873d0b5644bfc544 in / 
# Fri, 28 Jul 2023 00:01:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:01:10 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6aa08574e3d848ebe16f5911815377a151ed265e55191125c00acdc60a10c7d7`  
		Last Modified: Fri, 28 Jul 2023 00:07:46 GMT  
		Size: 45.2 MB (45212257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b88498dfaecd471ee638a2d95c6dcf20f03143a0e6c209dbf9032a663c2cb7`  
		Last Modified: Fri, 28 Jul 2023 00:07:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:021e852e42b78f428508b82ca92c69486fa1abf5fef11746009c400d3eb1d455
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49590482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07820e37e2a7465ac17d00405bbb154b08a5d07317f30d262f3bf5dc15690fb5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:44:45 GMT
ADD file:7c59407fb2ce4cb0198f51f75389c35962666d99e2a6b6a30ef90c78d173fee3 in / 
# Thu, 27 Jul 2023 23:44:45 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:44:48 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7b2194c23e7d56383df64446ed0490bda2beff114552bba473429a3ffd56de30`  
		Last Modified: Thu, 27 Jul 2023 23:50:33 GMT  
		Size: 49.6 MB (49590259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba88256122cc7851f572c9db2ec7a1c1ebc9d5c43f775171a5e48d9fc0f723d`  
		Last Modified: Thu, 27 Jul 2023 23:50:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:e500c83d052ca7a6897f21c4388c37588c3259bda3a077383945bc48cd036757
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50617850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fcc4a4f064f0cbe81fc5079c3cc2b53cab705fc805040d59f68256f6433fcdf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:41:27 GMT
ADD file:050238708c98ec93b886e5080140f43fad857d506cc20876b80482c8f7ee6a6f in / 
# Thu, 27 Jul 2023 23:41:28 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:41:30 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:768fc44394e0b08515419e88ffb63b159e3effd48edfd3774d6e126caa07c623`  
		Last Modified: Thu, 27 Jul 2023 23:48:21 GMT  
		Size: 50.6 MB (50617627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c13c35a40c88ee66dbefe0ff363cc988830b9580db1d7bdfb43666f0fa2ae6`  
		Last Modified: Thu, 27 Jul 2023 23:48:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:6740522cc63cf9b024abf7076c74ebd311460a98abe2a7b8b1825cfc0e599294
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49544684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44faf8e5a10b39b992ec9436644ad71b09e84a56dfc7afc71ba6ffd254b1019b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:18:05 GMT
ADD file:dbad549f8e200f8f213a4e285bdfb551b16bfe40fb4f82e748ea3bda17afef8d in / 
# Thu, 27 Jul 2023 23:18:11 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:18:23 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:39f64a8ea6c4a8a8f170704f90e994bdc1c77dadd700a514aba55a887f406f57`  
		Last Modified: Thu, 27 Jul 2023 23:29:29 GMT  
		Size: 49.5 MB (49544459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aaa91b9eda6fc7f20c5d2a05db12085ce7bd4ea254771b8a2151aef6cd0738`  
		Last Modified: Thu, 27 Jul 2023 23:29:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:11fb93c4e082b3c3b5946fd9199ef067716b5556c36ab9ff16128e21766e6ce5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53583406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a945e51c9617a397ae0be4f81870d5ee7a2692e6e4be1afe1467328a2202b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:26:20 GMT
ADD file:cf2133276d37e9779bd1b7d4236ac343e5eed1d08f1cbdf946c8b89663de5d2c in / 
# Thu, 27 Jul 2023 23:26:23 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:26:28 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:658eb606329d6eacf175892b5aea3b47f025ce1b0299283b73efe3ae9409fa14`  
		Last Modified: Thu, 27 Jul 2023 23:34:27 GMT  
		Size: 53.6 MB (53583179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c605497e77247002a358a9277fdbc7b9adb40652931f00d791aabb426609950`  
		Last Modified: Thu, 27 Jul 2023 23:34:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:36b45d16a89e47e61d422359bbc048dbcf8c0c5cfb2935328b14d780105352e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48030128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286ffca61218d48bef0e43b0f39f292921621fc89302344266c6d559d04eee9b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:49:56 GMT
ADD file:91a05e34d13df82da490ed42e221f68e86c9c2b37a037788a2d750037f6eebcf in / 
# Thu, 27 Jul 2023 23:50:01 GMT
CMD ["bash"]
# Thu, 27 Jul 2023 23:50:10 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6d46133c263b5a972355fe9f583c449a149141b965583953dcc9739e046ecae7`  
		Last Modified: Thu, 27 Jul 2023 23:54:39 GMT  
		Size: 48.0 MB (48029905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e13a5bdd706dc54484f6c1e4d81ccdd1bf7606e8f9577610380906871dc590b`  
		Last Modified: Thu, 27 Jul 2023 23:54:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
