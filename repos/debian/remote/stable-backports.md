## `debian:stable-backports`

```console
$ docker pull debian@sha256:1a8788b1505e82376a964bb92e62aa1d6227495902750bd43af87c86a456566e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
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
$ docker pull debian@sha256:e0a39b787fd0f970995e0dcea96096671c71d0640c37bc805c5e8d219e5505c7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50400437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ddb2aad3cbd6205fd6d8ac75161e26e98bf5928ea8306d72dc4c222045f340`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:22:46 GMT
ADD file:553358c6a785658d6f6910c7b3436552220631fc8b498dd0a0c9e4a487596dfb in / 
# Tue, 09 Feb 2021 02:22:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:22:53 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:def129c803cdc32e16bbbe6ef2e99f4c669ea2e5d721effc50cd34e73ba22047`  
		Last Modified: Tue, 09 Feb 2021 02:28:52 GMT  
		Size: 50.4 MB (50400213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1871420e1437c26122980dce0cfe47fbdfbfb1d0966a9d1d219586ff608b5a21`  
		Last Modified: Tue, 09 Feb 2021 02:28:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:7de909076a9ab96ad597131c7a25b59793bdf1233a061c7d5942549097d8b369
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48111713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae6407d7abe5aa5a7b8531359b04a873819a970ff86c151e5c1f810484ab66`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:53:37 GMT
ADD file:104ccf9925c7dd48c319db6b2a0c34383adf4d6fe8a73e4296108c1cab24a5c6 in / 
# Tue, 09 Feb 2021 02:53:38 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:53:49 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8237af1497a2267733281183ef9e42af97a986df017bd712a11584c8d16b677d`  
		Last Modified: Tue, 09 Feb 2021 03:02:09 GMT  
		Size: 48.1 MB (48111488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c4cdcb77e650b75cc051e9f0172c62ab4e2a2e1c8ac9e3dd05cb38a16279aa`  
		Last Modified: Tue, 09 Feb 2021 03:02:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:42cf04f7515e131d63d02c7c89e5aad91b6290bd84b4c4c3e24926596ba1bb34
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45867299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d8b0120b90fc6fe05e2e63c6ad3e7e1775f984b504415cdd32828f2463a8c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:04:09 GMT
ADD file:e330e94e6637dafc3b44bcd88834f0f5ab1b6389f876f3bf54e3e2deedec7743 in / 
# Tue, 09 Feb 2021 03:04:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:04:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:de2a37c6322328b5dc46bdee12af4f73e6416815303d229c7fe63ff5c9010699`  
		Last Modified: Tue, 09 Feb 2021 03:12:47 GMT  
		Size: 45.9 MB (45867074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15355c9a1ae74c20df7866ac903fdd911c09ef8592afdacef48b90dc71052b7`  
		Last Modified: Tue, 09 Feb 2021 03:12:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1af3974c0dfd8846dd243b3ad8196003da76aa1a326a1b711f41f117da366b8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49183454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ac22b37c81c38914b40779ff3dd5dd0af461c5a73718f78f2411142737d941`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:39 GMT
ADD file:d31bd7f49ff4fdebfb80be411d09de1d312b2116c53be8ac33323d1574235166 in / 
# Tue, 09 Feb 2021 02:42:41 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:42:49 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ab77a5f7ca321082c34e4921db6d3400b9e3f65a0e2a60d2cbd82d9e0354c9da`  
		Last Modified: Tue, 09 Feb 2021 02:49:00 GMT  
		Size: 49.2 MB (49183231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7f0854e6d7930447e20a5fa5f17625f80f3b1751a848b57b9403cd29211b81`  
		Last Modified: Tue, 09 Feb 2021 02:49:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:312b2fc41df4c4f7d20b68e6bd9b6eeafd46b2e7ee06119ea17a33b6e9ab3440
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51163374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43fb6c38c62b82ec441138549c976629f9ca8e2e2f99b2635a68a3e0ac36d86`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:42 GMT
ADD file:6322e1487249f07479dc81837dccee553691380f8644169ed571b8eb5dd3a0ca in / 
# Tue, 09 Feb 2021 02:41:43 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:41:47 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6ad4a0b0940a81308c41060a0163cd7afa53fc50f186e6ef9567218928c6871b`  
		Last Modified: Tue, 09 Feb 2021 02:48:47 GMT  
		Size: 51.2 MB (51163151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d798b834573e07e3e501981fb7570f9132b2c531de8d6dd7c9a99d585655d942`  
		Last Modified: Tue, 09 Feb 2021 02:48:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:fdb9364d51b0cf9de645d06b0d9f5f158a455be28c5c2e62768694a98b69069f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49028217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec411c410494b69d1ebeb7926223880658a1972e6c45d986fa56d6e962aec3c0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:10:34 GMT
ADD file:0429c5fe153d8db983e57652cf5056de0e4051c137395c30a19f88a28f68ca1d in / 
# Tue, 09 Feb 2021 03:10:35 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:10:42 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:64b858773999e03f076a33c9d0afd61a9c86e1cc9ff59b17d737894febf2ff56`  
		Last Modified: Tue, 09 Feb 2021 03:17:54 GMT  
		Size: 49.0 MB (49027994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e117664196a64a1e66d4801b7e3002954c1fb1047097909e9072dcaed2de31`  
		Last Modified: Tue, 09 Feb 2021 03:18:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:23a4481530f4ae10aff8ab2cbe4e1f16f107963e1422f2e068cca30782c8a1c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54136062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97888c66fa8e29d7873115fb7ef9bdec2f6980bfdf04df64b94996d593fce7ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:84de81f112f052e64d0c773a08a4eb379cd4218f4fbe786e02639cdb62bd8806 in / 
# Tue, 09 Feb 2021 02:20:52 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:21:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:493202a0b1402027b2bd18dcaef8d0fed32f85dd47c3b08093bcc1453fb071f7`  
		Last Modified: Tue, 09 Feb 2021 02:29:10 GMT  
		Size: 54.1 MB (54135838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cd205b347f5b7098fcf74cdb28f87753ac270f9dd90baeb3b219a88bc555ea`  
		Last Modified: Tue, 09 Feb 2021 02:29:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:aaa091baf6a042edf6fd898389fbb788f238232653628affc0bbdbabf793e354
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48970612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e47de42fe55dc95e34b62d0986ec3832ea6c3ebb24a71be3cfb4bfedf0e1cd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:42 GMT
ADD file:87718cd50a4d34a2a05215578ce84d948a8a1a74187225e33112578384b37998 in / 
# Tue, 09 Feb 2021 02:42:45 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:42:50 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:74d4bc628eae6b3f16dee054df1e8c8c8a2b4752c291af5cb419f5a354a71c13`  
		Last Modified: Tue, 09 Feb 2021 02:46:08 GMT  
		Size: 49.0 MB (48970391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f45a52053ca2b9ae647d1fce0c89d929c67c9c67686fc0fdf9d3083286a215`  
		Last Modified: Tue, 09 Feb 2021 02:46:15 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
