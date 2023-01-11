## `debian:experimental-20230109`

```console
$ docker pull debian@sha256:3565a8f66b25bb7b6b07416070e78ffbc4779217ad5361d9636bd8a85d38f86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; s390x

### `debian:experimental-20230109` - linux; amd64

```console
$ docker pull debian@sha256:61bb4c8b0a8a8925f81269d63dfa87985812776fb1e5de5f74a60d666952bef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49040961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954b2d3030589a7d68db242b93feb772405f1eab6bba877d02855b2cd4671b98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:36:48 GMT
ADD file:a472be541f4793676ca4459eecc1317f0a0a37318f675b0a0fcb25651bef94de in / 
# Wed, 11 Jan 2023 02:36:49 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:37:01 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2ea704eb82faab6fb3931c69ced55d3151ba782c09e34f82ee3f517a70bdf0de`  
		Last Modified: Wed, 11 Jan 2023 02:42:17 GMT  
		Size: 49.0 MB (49040739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15e7038da5a7a69a3e99e905d905d9a29f88e7fa5934495fa1e4ba2c25306a3`  
		Last Modified: Wed, 11 Jan 2023 02:42:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230109` - linux; arm variant v5

```console
$ docker pull debian@sha256:3179663a7e61b6b83eb09d8098b346007bb021c2aa34eba49690bfd3d3e70cda
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48018183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c9f2d7613eae444b27895c80fc3e1fcc0cb6d36cff3977bd8e71643eb66cea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 01:57:08 GMT
ADD file:f8addf0f27d3efc8283bc4e3a7ca9f06b6cc9b4fcbcd09ba7ed7d39c9c16c5a0 in / 
# Wed, 11 Jan 2023 01:57:09 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 01:57:23 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8b3394d1cdf2a55f5514dc0fddd06a144e5ef0a0ed6b78a11bb2363f9f66d3c5`  
		Last Modified: Wed, 11 Jan 2023 02:03:09 GMT  
		Size: 48.0 MB (48017961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a89375b610348f4f7c93b4fb7a666d3114a508d7b77c8e4e7e35861d6502201`  
		Last Modified: Wed, 11 Jan 2023 02:03:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230109` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:351770a99ee8f402e1e2134044921d7fff85aa4e5da47078e62f0161448ba98d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49084770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d884efce7a0826d706d0c490e79ef96a61d863429a3ff204d43da4e575834293`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:59:01 GMT
ADD file:340469c7e9d21ec908d8b07fb16fba1e70836f1b72c18a65eda82e4aa37d7084 in / 
# Wed, 11 Jan 2023 02:59:02 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:59:11 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:62cda9971d1a0fbbfef8e70c8535d75041604d167dfa6996f54b284133b006e6`  
		Last Modified: Wed, 11 Jan 2023 03:04:22 GMT  
		Size: 49.1 MB (49084549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97763a913c163086254eb5381b54a88ff1472cd717e097588c0c3cfed7b6375f`  
		Last Modified: Wed, 11 Jan 2023 03:04:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230109` - linux; s390x

```console
$ docker pull debian@sha256:b9cf6538294881b8d7727c53a17a525afddd2d464be92f9436e9faa97fa2a25f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47434307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa52dd895d0ea4b580208ac14a2b650d5053cf58a8315ff74363239763b7d4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Jan 2023 02:24:11 GMT
ADD file:8a39e7d372aafafec15540b4371fb3e5d10767a2938856a7ec6d49761815a2f5 in / 
# Wed, 11 Jan 2023 02:24:15 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:24:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:83741c7534d43b1ff77d8fd7a8f11f5add467189dec5a410d7310b6c372f90d2`  
		Last Modified: Wed, 11 Jan 2023 02:28:24 GMT  
		Size: 47.4 MB (47434087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4932f50c96a8d8f03b99575743a0d2b45c868e3b23953a2675fcb89af53b09`  
		Last Modified: Wed, 11 Jan 2023 02:28:41 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
