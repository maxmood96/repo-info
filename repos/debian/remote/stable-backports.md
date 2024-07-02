## `debian:stable-backports`

```console
$ docker pull debian@sha256:dc918c4741b401f93e11654ba40e0d160c29f0bb630e3f29d701fa3a816f3591
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
$ docker pull debian@sha256:6ba50ad26f82c106f3daabbe00314dfaf0d0de2507a8d318677e67dd7f7015f8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49576867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4312ebf8ee6823fb3692d9958aec8ef8cae42e4dad6fcc7dcb99f68fc38c6026`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:22:48 GMT
ADD file:a97e929c314c6cd646d7ea12e7bf8ba9f6d14ebda7dbdedf866cbe4c4e8854aa in / 
# Thu, 13 Jun 2024 01:22:49 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:206929d2bade528278ec19d162f49bb6cb90d835addd10f7d4b8be7e68fbfbf0`  
		Last Modified: Thu, 13 Jun 2024 01:28:35 GMT  
		Size: 49.6 MB (49576647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a823c1643675343272dc85763c0859562e451fc76be0f16981df4b3c3bccbbe9`  
		Last Modified: Thu, 13 Jun 2024 01:28:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5848bd4dc32c2064d5f84d5052668dfd6bd58df5447fdfb2ef83fdb9bc5def68
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47320526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a10cef45d41d78c95e8eeb92f8d9b8797b62573d1e986d21f7f759632f3f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:49:20 GMT
ADD file:e3ddfd05267dfede31acf013acc6cd1fd83f83bfd43e1e910c2cc82d721c0b4a in / 
# Tue, 02 Jul 2024 00:49:21 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:49:24 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0f8dca44421a074863186da79fc0c09902599fa7be614d1835aea72e023fa41a`  
		Last Modified: Tue, 02 Jul 2024 00:53:35 GMT  
		Size: 47.3 MB (47320304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8066cdd1eb64fe352abe4e0c9fd347d0ff25b3098afc5bb0bc35957153010e`  
		Last Modified: Tue, 02 Jul 2024 00:53:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d3b9c0cb343f9d01b6a0802ad4d346342593621437ddffaf47c8a7f268b9feab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22086729f9bd1e66d5ea09752817f165dbab7d45b6192fe35974acef56cf09a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:01:08 GMT
ADD file:13b80b4d654db259112da31962c017548a9dc6c812c6af081ed10226e4d2037b in / 
# Tue, 02 Jul 2024 01:01:09 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:01:11 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:66c658dfd87595b8323536aa57d9c8586347e616c2e2ee6896b3351c203d6bcf`  
		Last Modified: Tue, 02 Jul 2024 01:05:16 GMT  
		Size: 45.1 MB (45148127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ca43e1a94cefa8de5e06a20bf448aa341cc45c37099b6a931bc4869c88c8d`  
		Last Modified: Tue, 02 Jul 2024 01:05:24 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ecd62c9b532c062dbd1cf8ebcccc67a912f2bda1b4b5b7d8ae1c4c13e334035a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49588664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c8e17124222006db131839841085caccc3aed16b84198420e1f3feb34f586d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:26 GMT
ADD file:fd907743f6505b73bcc7d3b66ce062008bff02f12d1b59a8f272641290c5e474 in / 
# Tue, 02 Jul 2024 00:40:27 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:40:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dcf4a1279be907cb629c2e75ab78e4c71a46e913164b2ffd9e497af49b3546e5`  
		Last Modified: Tue, 02 Jul 2024 00:44:20 GMT  
		Size: 49.6 MB (49588443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4d95fdf6f87e7379db649999a4bca4b981d6428f04fffceff784d6a32008ef`  
		Last Modified: Tue, 02 Jul 2024 00:44:29 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:da1ac816b45b6da4055b8768b9a3c7ef64ac62239818fcba269540d7fab1b43e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50579595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3902d6160b35e61a4538b04c818b15c172fb54b023a1d299d9df01995e96b78`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:09 GMT
ADD file:719475a86e4db858893e00e280f5f64d3bf4792a4574b86c81c85508fd416684 in / 
# Tue, 02 Jul 2024 00:40:10 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:40:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:13e6fc1fe429d73324141864ce3ae03564cbd7f6f808bef1240e2b514bb2b09d`  
		Last Modified: Tue, 02 Jul 2024 00:44:56 GMT  
		Size: 50.6 MB (50579374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac81b22efdacebe89a2b69e52ec23324ad6c432010c0aad81ce0b81ce27a05d`  
		Last Modified: Tue, 02 Jul 2024 00:45:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:f265e0ad02a2c7c5d3312c15f0b1ab097815fbc0a9c770e9da60a8741d5385f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49582935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9722aa4a6824b850c7432e2b1a3b13a3789912095e54b2847e4fa49783646029`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:14:51 GMT
ADD file:80d218cef18aba8e0d2af99a9d9a92184c2edd106a58c972edba150b49a56b0a in / 
# Thu, 13 Jun 2024 01:14:57 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:15:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:356c630782ec3338f52aa63f535a94e3e3c208291194b75677b5424e3d70e9a6`  
		Last Modified: Thu, 13 Jun 2024 01:26:30 GMT  
		Size: 49.6 MB (49582710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6384e7e97f4f61d4ddf271f97a4d804d9c98e126b9db7cc3da6900ec3545254f`  
		Last Modified: Thu, 13 Jun 2024 01:26:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:20f0c87b7488d468f503a745e0a6dc854584ef3ca4c672ee155505f3339dd811
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53557201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc999591cc94cab77648129a1839b75982920d6b9d1ac76174bef017e8519f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:19:03 GMT
ADD file:73a5be306e2b4aeadca7a57dc1500781d8d08b6ba9129c9b3f79e532f4b20683 in / 
# Tue, 02 Jul 2024 01:19:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:19:11 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0600e43fb2120735d6913dbd4e633f63391623e35e7438464b0743eb2c38c7fd`  
		Last Modified: Tue, 02 Jul 2024 01:24:14 GMT  
		Size: 53.6 MB (53556980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e23b8b1cc1cc28f5b9295f2fa45eec6d5ac5a4b632742d0cbde94ccd5e511d9`  
		Last Modified: Tue, 02 Jul 2024 01:24:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:d2e894b090a21bf4b25f8c669447df40c56341846fc0b26b64d5fc9e63269091
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47931657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effdc74e95de515cd61b5af552b8b72606bc35bbd585c82269fc4631d6c29e66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:45:19 GMT
ADD file:37288813a03d763f6f5510bc225247aca8be431fea523b7329f20be0935435bf in / 
# Tue, 02 Jul 2024 00:45:21 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:45:28 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b6ebd8ea5520cafbcb1bb3782860e45675262ad151c4c9a6d280b391ed816a2c`  
		Last Modified: Tue, 02 Jul 2024 00:50:14 GMT  
		Size: 47.9 MB (47931437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d32f26d8585b9f0f0cdbdf6ab4176b93ab51ea108f1fa863f336824068390d7`  
		Last Modified: Tue, 02 Jul 2024 00:50:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
