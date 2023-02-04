## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:dee145faeca2f6e46abf8b584b3255128169e784a6667e987caf68fdfce68839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:2199380521b2113d6e4daf3557d86e86deaa3ec5f3f8284958dfc69422f08fae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50449322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb209f8db83b4e1c59670ca7d330a9d3775ebd074f98491d7f802340ed50a36d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:18 GMT
ADD file:0a3c5d05d0bddb6fb5cb4ddbe51c8974ce10d81363b989f85f07704c84166ffe in / 
# Sat, 04 Feb 2023 06:52:18 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:52:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9601128e4d377ac224967c21a126d3a4561b76647f26976d8de1f496a25fea10`  
		Last Modified: Sat, 04 Feb 2023 06:57:17 GMT  
		Size: 50.4 MB (50449097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a678b76b76c16a3cf7b9bee96520a2fa7d6a68c89d2704a227e284230d454e0`  
		Last Modified: Sat, 04 Feb 2023 06:57:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b0005fa57a61e834ccefe3beb64aac86daf00cea70d12cf1c8102bfa703f2085
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b481121ddc17720fae5c4d4a84a1f145a34dd5fa2132c6a73ca0e2fcf66c4d98`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 10:00:21 GMT
ADD file:e57b072389ec9e66f0357e15adc45e73ca2fc0ea2691c9ca290fc24f4c0ab669 in / 
# Sat, 04 Feb 2023 10:00:22 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:00:27 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d86d3cf2d692b7c4950efe13261c152649078f1e681ed507837ecb23d90b25d1`  
		Last Modified: Sat, 04 Feb 2023 10:07:41 GMT  
		Size: 45.9 MB (45915787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbba320524f30be451c699070981adc922f09c574363b4b90ff67f9107bb7685`  
		Last Modified: Sat, 04 Feb 2023 10:07:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:df723560e85a4bb9c66f4933e29f0ed24db08e612295cce0c0b570d2efd90386
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49239588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1876345d76d11df663af84aa4989a71487e8837d7ea024ed7df9b339b8ec6ad`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 06:18:02 GMT
ADD file:ed8fcd4462ae87c740984104ce116c9e633432638bb1d93418ea69a39f2fa120 in / 
# Sat, 04 Feb 2023 06:18:02 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:18:04 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:962aa44f1075264b7b37c588ed4e76daf41573db552192cb330f62f7ad208810`  
		Last Modified: Sat, 04 Feb 2023 06:22:21 GMT  
		Size: 49.2 MB (49239364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d252aef8b3b0c01d5778dc868d109e464b9cf02a4edc4c4e9c08efdd022963b`  
		Last Modified: Sat, 04 Feb 2023 06:22:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:b5435309d94a8339f723e9d92e5e674c77f452693ecca59d045ab8322cd0fe80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2d1269e138760a42dfe96d6b568b021912b3979548789eae3f04d5b9b086fa`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:59 GMT
ADD file:09cee105151d95c2e15eacee8803ba5a44a2bf8b6e29a2390f424fe677ee9122 in / 
# Sat, 04 Feb 2023 07:50:00 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:50:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fe16db46e3396ef38850aa05ff1811778e5f85ddd3fed7559ccc867e54a3a3f6`  
		Last Modified: Sat, 04 Feb 2023 07:56:14 GMT  
		Size: 51.2 MB (51207654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c7104789d6edadaa4051ebd514f0804d3b8367544ed6df99150e9cea609ccb`  
		Last Modified: Sat, 04 Feb 2023 07:56:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
