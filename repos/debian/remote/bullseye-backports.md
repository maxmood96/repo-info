## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:546e08a9f38721d1a56e85ea4d94c2d29b7a3fe194b40b2859810ebf0b35bc2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:c7ce60eb3cb82802a12e9725b0a523a24fbc2890a7acc906f13e1c4bc99b7e96
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55081618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e64fa326028fa56e52e93fa8dbd657f1d85bd14f47f2cafc7ae25d0a2d57034`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:29:47 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e7428c4083b46a801a7ff5acb5fe0ff7a2f1ef6a32957ae0c16c2f2745e05f`  
		Last Modified: Fri, 27 Sep 2024 04:33:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:54b21df3bc6b689553df5fba2cb37c9606934371b51dc1513b29aec642bdffa0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50240605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e018657cca65f1cc593927b4b0f177e350d5a69c75f2670a750eda1ea2b0ed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:13:58 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1b9328e2b5ff3492529ba7ccd7bd64e327b6cfdebff876d125ce2c62e967e0`  
		Last Modified: Fri, 27 Sep 2024 05:17:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8580633832ce5d0e075639792d4a19a284a90224b5cee1dad08e93107aa6189e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53734090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a7750227531927b07d17caf5c3ca530ea463bf24176cb6f3eeb80bbade1b20`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:38:27 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a143de137675c5a7cab210f67b90e2de5eb6460e6bbf6252548c4fa2399865e4`  
		Last Modified: Fri, 27 Sep 2024 04:41:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:d27f34cbd9b2eae3091df50f7542003e46a4e009220f398596453043d92b757d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56076731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3344f3039a9adebb7503f994a9c9ebf4b16560bd50fe6f8cf0e83b82f58b61e7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:11 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 27 Sep 2024 07:23:12 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:23:15 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add049adb5679ceaded679937d82e97165ce2b946877db2219868f3043882c2d`  
		Last Modified: Fri, 27 Sep 2024 07:27:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
