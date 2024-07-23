## `debian:stable-backports`

```console
$ docker pull debian@sha256:ad35bba298b7b6c4b75b789059fd65d0446599a8fcf1660cdfe10c6133ba42d3
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
$ docker pull debian@sha256:e96dd2c734871899fa7cbe1be63080011b296abc124db15fdc09846f8a70be7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49554296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c9bd39ab76d48f675eaed5b53d5d5ed7849636f463a64c2024e4c984b6808c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:26:16 GMT
ADD file:213de1af48b6d18cba944529abd780af1a9ebea6f32558e442e88a1521fcf01d in / 
# Tue, 02 Jul 2024 01:26:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:21 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7752f0ba46cc8263552f036c7e8e5194360d5d56286b9c8fda5416fc84a9bcff`  
		Last Modified: Tue, 02 Jul 2024 01:30:43 GMT  
		Size: 49.6 MB (49554074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4a3b08964b0ca066855fed0a58d8c1995ef686901afb4caa56a22afd6ea479`  
		Last Modified: Tue, 02 Jul 2024 01:30:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dd43ce25ca256375a7f692a1a2076d3314896907f301b0da2a8abe66018464c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47320560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f955c02d3f196b51f9d5410c5c11e0019a350b05e2101bd84c9c6b30d9d7eef2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:58:25 GMT
ADD file:96c16e2a5b0f354a34704f6c5349c0b886f6bcc9873b497a6798c92d99d6c083 in / 
# Mon, 22 Jul 2024 23:58:26 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 23:58:31 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:46078a3d0c8b8370839d00725d49531249f17c1b2cf595efc2f337d0f0364cd8`  
		Last Modified: Tue, 23 Jul 2024 00:03:31 GMT  
		Size: 47.3 MB (47320337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeff9534d6b15c8f85b828474c42dc9206ebc1ae47406c43fd3403b9bdb6ab71`  
		Last Modified: Tue, 23 Jul 2024 00:03:39 GMT  
		Size: 223.0 B  
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
$ docker pull debian@sha256:e82b3c3e9d32dc4ab25cef927a343ccee308b1cde52d11dbbb7f409bbfa4474d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49563389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45aab5f9edd251d2be94d0f02fb5e26044305e3a9f9e18216499a380c00e1df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:22:38 GMT
ADD file:b5ebd9b70817b0ed66fdb428223a9fd27b2d2b2c2662c514a973c26b2e67aab2 in / 
# Tue, 02 Jul 2024 01:22:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:22:59 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41d85e0ce859faab3764c3e4ddabef729ab2936a814aad9909fe4a8fe5eec74b`  
		Last Modified: Tue, 02 Jul 2024 01:34:01 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553bbfdc52f60d41fc412e658f3f21eea853825856d9d7b2c818858284efab1a`  
		Last Modified: Tue, 02 Jul 2024 01:34:10 GMT  
		Size: 223.0 B  
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
