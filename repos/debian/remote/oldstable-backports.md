## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:5e3e54a9127c5a873e71ac9b8e0a1f67f3de160d16ae785ca2703b7cdcb95a53
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
$ docker pull debian@sha256:090d624c00c6d35a1c0d7c9769d597aa9bd6f5bb2729ba00501d5d61fcad5099
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c6d8dde0261da4805aba0cc0c3bcefab70189817d555ef12f4251b4fa3b40f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:05:24 GMT
ADD file:f088582b640055822650ee946d0e4f52000b7b204fbd5c3025c09d47e749a6fb in / 
# Thu, 17 Mar 2022 04:05:25 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 04:05:32 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e17b66e2bda290339e10ed5e261d111341c3a883af04b5bc32472a2dc2493e29`  
		Last Modified: Thu, 17 Mar 2022 04:11:50 GMT  
		Size: 50.4 MB (50437306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8501198b0e4029d1c1164b0515aa0808a0c591143d0c1fbd9e7efd00bb0862`  
		Last Modified: Thu, 17 Mar 2022 04:11:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ec50bd6d6d66970b20b97bce992f6199c72b5366828d8d9b5a97b32a37742216
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48154420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde261ca60f82e3a1efd2ada92dba1d9046ae849233aad3b51076bef1b5fe263`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:22:07 GMT
ADD file:bc76173a9d5671ebcd9b0fb088b13005794d4114e1bdd970f8d2bd654ecb7e23 in / 
# Thu, 17 Mar 2022 05:22:08 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 05:22:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7ca6e4eb2aabeb3e74996dd83c8c63e253e0b6917cab4c85a4d515523e2c7cee`  
		Last Modified: Thu, 17 Mar 2022 05:38:24 GMT  
		Size: 48.2 MB (48154193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43794d5f02b4d5be8aee8bbc955a0551deb5ee3a2927acfd05f8d0fe9640526b`  
		Last Modified: Thu, 17 Mar 2022 05:38:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:df07eaba7684af4416a4586a8e5e2eadd793b5cf9e78c82ebc4294bff6a1976c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45918389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30c37c70cdfbb479b0ba26f3350ee7410ccf28b7f759f0e91d4f6f7a018995c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:33:33 GMT
ADD file:395ce20dac2bd94688a9dd481222d5279410ce7cd1a3f4ae1eea631c3f49cc2a in / 
# Thu, 17 Mar 2022 09:33:33 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:33:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a00a2be74d30413203cd0c72d41dde557e12f57905d392401bab26e4ba0f92e0`  
		Last Modified: Thu, 17 Mar 2022 09:49:48 GMT  
		Size: 45.9 MB (45918164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702d04f9d8dd6470c0f9167ff4d71381700e12102944c1dc87ca63efe993430f`  
		Last Modified: Thu, 17 Mar 2022 09:50:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:023ee03e38d182afe336db37ab208911c016e061676a59daa51d3c2d26bad737
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49223195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f8a95ddb1f7b9ed35413cc9883e7296d11d81bd2474717dc9dee5d8573a3f8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:55 GMT
ADD file:091e77eae3a3e761352bb6399c06e8ff9aa6f1617066fbb569b90b231d93f1b8 in / 
# Thu, 17 Mar 2022 03:22:56 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:23:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:78e88037a755029af79d082742692ea236c1222ed964a028b0d5148e85bf5bc6`  
		Last Modified: Thu, 17 Mar 2022 03:30:30 GMT  
		Size: 49.2 MB (49222970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df4a19ee593db6788bb0685de88de2fc1bfe721aad165c071fb111da2a24a4c`  
		Last Modified: Thu, 17 Mar 2022 03:30:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:60335ea611da5eaf95753a9c7d00587236e338f611f9260a81f5246ddf72d7d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7083f42735b8093fef1884733263865603fb63af0793aaa9c624178295d421e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:17:07 GMT
ADD file:9b242f08f93ff006a8ca62f4675016ce22b8b9c371b7b3fbb8a10699a6e026f6 in / 
# Thu, 17 Mar 2022 08:17:07 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:17:12 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:15aa61d19692b4cae4621db3dd2cbeba928cceb365fe0258643247ef31bf2824`  
		Last Modified: Thu, 17 Mar 2022 08:26:13 GMT  
		Size: 51.2 MB (51207751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53774d79ec86d49ad77df96a9321d5d3cde99938d4af2bac453b04db860504b3`  
		Last Modified: Thu, 17 Mar 2022 08:26:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:96ab65094f23a278709492e8500a406cf38f1fdefef8cd7c0e309ffd7f437385
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49079664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a5b9a738c5af015b5294a418e4ed268d4bf0f77e26a2a61f1ef468cac61bff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:54:41 GMT
ADD file:41bcb19aa2a6925b18a880af7a7e39bbcda297219288ee55dc9780b5922f5377 in / 
# Thu, 17 Mar 2022 08:54:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:54:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7c6ce6359b3d8d3857b088c56fe16bd48b385032bc4ecd48dc843839daa0475b`  
		Last Modified: Thu, 17 Mar 2022 10:45:21 GMT  
		Size: 49.1 MB (49079438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4bf93fbe8db05e51eb4742b72a1eb2200add805af38d396e71d7828db63ce3`  
		Last Modified: Thu, 17 Mar 2022 10:45:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d2e9962a461e43032c5f1a510826bbee95aa5140ff637c8cc6a7c65d28be7c34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54184025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbca74321db0e2a0dca0e8cd68fcd1771008cdee2e4cc1ea8505f2e3e57b772b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:19:29 GMT
ADD file:6cec06134f68ff9dc8c3ad81aa9b9f661f8c0e845c0f5008c005ea6cf9926604 in / 
# Thu, 17 Mar 2022 11:19:35 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 11:19:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c47aa63066714f3b52c556cbec845f549ff1cbad0e6532b4489a1ad3f98a2180`  
		Last Modified: Thu, 17 Mar 2022 11:29:49 GMT  
		Size: 54.2 MB (54183798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6f4ca7b8ada241dcb67b07f072db85a7ff47c76b38bef96414f47e716f3fe3`  
		Last Modified: Thu, 17 Mar 2022 11:30:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:4056b6a1d8761f412e04ea25b47735424a05d48dfd0d119fdb90047cb5144c6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49005708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cc1c46268211fadb687e317f6a6a7feee012c4738bd98057697423cb7d6a61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:07:42 GMT
ADD file:14f85005f266ff4f60fcb6a5a40a8d009da5bdd7231cf0511cf415643c2c2f32 in / 
# Thu, 17 Mar 2022 03:07:45 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:07:52 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b4c86672ac6b975dc8b43c5e06d045ec7c39051f9839fcbbedec05f187f9bd05`  
		Last Modified: Thu, 17 Mar 2022 03:13:32 GMT  
		Size: 49.0 MB (49005484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e242e8057d0fd93fd1bf406f1ac8ae98d3372bd7ea545e41fdec47383fbc9b61`  
		Last Modified: Thu, 17 Mar 2022 03:13:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
