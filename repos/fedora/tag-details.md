<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fedora`

-	[`fedora:37`](#fedora37)
-	[`fedora:38`](#fedora38)
-	[`fedora:39`](#fedora39)
-	[`fedora:latest`](#fedoralatest)
-	[`fedora:rawhide`](#fedorarawhide)

## `fedora:37`

```console
$ docker pull fedora@sha256:73f79a16fc1ce983c5413fae5952d1d66e07e44b5ee63723ad02849ec725fcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:37` - linux; amd64

```console
$ docker pull fedora@sha256:dea1020c99cd29d19e34542bd3683b93a9abe04675873e53f15c705b7eac3e31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66506878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8ee309e6e9fc0f68614ef3756a5b6fd3e45f3740923dbb4339bbbbee1e60a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 20 Mar 2022 10:46:14 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Tue, 06 Jun 2023 20:19:54 GMT
ADD file:6a18849723415c37086d32f5129951c059025f04047c3ab7b03b78f575c721e3 in / 
# Tue, 06 Jun 2023 20:19:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d884362d3691889bc38b096277f1f5e10c9ea2f4d4cde1b7cf58a871fc308e69`  
		Last Modified: Tue, 06 Jun 2023 20:20:36 GMT  
		Size: 66.5 MB (66506878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:37` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:895e23d806091ba8e5183e4235c6d9d110cc620affb0bc59a479121d4d8d803c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64669791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f2e00d02bd534a8156237f0486d9246e266d835123c89d231cba76562da7b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:31 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Tue, 20 Jun 2023 22:40:52 GMT
ADD file:b7fe4ffc4ec2f3e5417c0e155587047783468a308a01321171773955c178cb8f in / 
# Tue, 20 Jun 2023 22:40:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3d2957f0a3a31457adb0574a5dc70706e8043a88c8d072164a802fb5260ce33b`  
		Last Modified: Tue, 20 Jun 2023 22:41:27 GMT  
		Size: 64.7 MB (64669791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:37` - linux; ppc64le

```console
$ docker pull fedora@sha256:a921772497c486445f7c868819eeba3d93d21abb7122426ab8817f8dc306cb1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72179663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca851a938ed84086f92e5a81583f68182fd26f8dd2bfc930126849c9c34bd119`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 11 Oct 2022 12:17:51 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Tue, 06 Jun 2023 20:17:09 GMT
ADD file:ba6cf46e7f1e3a51242da88525218173d0d5ad616a111f03ac8bcc72464e945e in / 
# Tue, 06 Jun 2023 20:17:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:489756bd2319ed3f0e92807620cfb9d74587f4876efdfc7540e92800fca03d4f`  
		Last Modified: Tue, 06 Jun 2023 20:18:39 GMT  
		Size: 72.2 MB (72179663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:37` - linux; s390x

```console
$ docker pull fedora@sha256:2f0d840fa8ebb85431fbcf44545fadb1ef8a87a5ab6bc0ce90ebe440f73c9601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63634063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4946009ae209a974e28d2386cc83bfe0b0236a6794098bdb97b60bfed8dfd5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sat, 19 Mar 2022 04:31:50 GMT
ENV DISTTAG=f37container FGC=f37 FBR=f37
# Tue, 20 Jun 2023 22:42:53 GMT
ADD file:bf33d94582611835c46f58999e36c8ed9227382255500b36ec78dc8a13bcb4a1 in / 
# Tue, 20 Jun 2023 22:42:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:21275fecc70503013d0eb08612dc3d6ca0dfe0d2602323d4103ef50caff7f61b`  
		Last Modified: Tue, 20 Jun 2023 22:44:09 GMT  
		Size: 63.6 MB (63634063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:38`

```console
$ docker pull fedora@sha256:e14a428003346bebc13cf03dc8ded0a15284167bc3454a1c40474e01508f8f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:38` - linux; amd64

```console
$ docker pull fedora@sha256:c23aeb3dd1b629e34b49bad4e6295bb5d6e9cb1413d95b2e113254d5ffaaa1eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68307864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795c8dbbab2db9f5858998d948189e2b646caa6f92b35b87a4b80d7634e88201`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:41:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 06 Jun 2023 20:20:05 GMT
ADD file:0f119e7993d70c8fa0b6eee79fccf645273ec8be97931d56c36e757c615f3e9f in / 
# Tue, 06 Jun 2023 20:20:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:be3ff91c5bee04b7d595eaaa1c798741cc8d27d3945cda381130972a22e2eeb8`  
		Last Modified: Tue, 06 Jun 2023 20:20:51 GMT  
		Size: 68.3 MB (68307864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:38` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:4fc1ddfb4c01afd5dbd1e34b554157235e14184adbed6222723700375b4d8649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67057126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba921a5e918410083549a2142da0ec063c6f1341db73b0901aaa392dcfd59d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:41 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 20 Jun 2023 22:41:00 GMT
ADD file:e1af2d14efd2bc54300585fa1ae9b7bf845e8d6a948db0ed61aa8c826a929305 in / 
# Tue, 20 Jun 2023 22:41:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9887f655ffe6443a8674e4433950b274e2a8b7265069a444db775d293cf74da`  
		Last Modified: Tue, 20 Jun 2023 22:41:40 GMT  
		Size: 67.1 MB (67057126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:38` - linux; ppc64le

```console
$ docker pull fedora@sha256:7fc8668a24d48d783da0785f22953f515e704011be60a34db027cdf9f590b7a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75013876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0b3305f34ebdf0bb09acf248f864948cb6205f762a4bfff52996413c9e57b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:19:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 06 Jun 2023 20:17:41 GMT
ADD file:929405ee3c8d4219a5fdf3808bbc8adab3b7afe6b27a55369e1701ddd935eff6 in / 
# Tue, 06 Jun 2023 20:17:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8d48c09810ab6be544595e74ca2b5a1101d17ca0e95a320e75019689da3a8ece`  
		Last Modified: Tue, 06 Jun 2023 20:19:04 GMT  
		Size: 75.0 MB (75013876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:38` - linux; s390x

```console
$ docker pull fedora@sha256:b766297005dfc4fa7b222386089601421c65bbd4af28203d6427a80cc3137a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68880144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4282604cdc90b4fb52329ce3dee4ceb3749dbd15ab590359e821a958dabe42d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:31:13 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 20 Jun 2023 22:43:13 GMT
ADD file:ca7ca36c3ae04ec89859c84588cf8c9c06ec3360cb66d180de209649826d7f5d in / 
# Tue, 20 Jun 2023 22:43:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8daeecf2a7f8b1e288ef0ba871a4a34acf6b97f092e964b48466bee3d8b924f6`  
		Last Modified: Tue, 20 Jun 2023 22:44:23 GMT  
		Size: 68.9 MB (68880144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:39`

```console
$ docker pull fedora@sha256:0d5881e95c30160ebccab1fb6a6904d59702a6f1834e9098d5c4d4bc260337ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:39` - linux; amd64

```console
$ docker pull fedora@sha256:649ec5c98d263f3cfeb4be02630ddbe7492f967f997986fa2706e83f5ccf6a88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68469901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e956bfeffc9c7a602b1c4d1f18a983d705ad673ba66a4f4e099e777279cf5b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 21:20:05 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 06 Jun 2023 20:20:17 GMT
ADD file:190f7eebffe7e3a50b341655317071726e82b8560aba1fdc0105e109a3275ad4 in / 
# Tue, 06 Jun 2023 20:20:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:83fb1a35b0ac26949417f38861aa80a70cd9d9ddc63ab13bc11f20c9365f7456`  
		Last Modified: Tue, 06 Jun 2023 20:21:09 GMT  
		Size: 68.5 MB (68469901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:39` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:72545d387095d2e7779da34faf9e63165a538cec374c9030b695bacfc93254a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67246922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ab1a980e248ec9e60528052cf2dc91943f50d500ce1e040b944284afec11a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 20:39:50 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 20 Jun 2023 22:41:10 GMT
ADD file:d7de6432f5e20fe69c1673a95c805b9f1c069807bf78fe1a4b5ab32f527216e3 in / 
# Tue, 20 Jun 2023 22:41:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1e6aa5d3508a9d83ffb532e3e2b40029f4ef8108972783be7c4f01041cbccc63`  
		Last Modified: Tue, 20 Jun 2023 22:41:56 GMT  
		Size: 67.2 MB (67246922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:39` - linux; ppc64le

```console
$ docker pull fedora@sha256:4c67fe09823af16107abbed153250649f5dc9db7c1ae15115ea6a1a5cc9f8c42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75132944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e49f96d77faee9414ff7290bf5d4f00c528e5281a60dfc0a6ae8d2fa4b78b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 21:18:04 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 06 Jun 2023 20:18:05 GMT
ADD file:dd1a39c61dcc82b463d39baeca4f2b8ddce1f438a841ddc889993f7c4e19d687 in / 
# Tue, 06 Jun 2023 20:18:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f83bdc4847e939bcfcde5a295a0d2f495e047e37f70ecf8b4872d75719ebb12e`  
		Last Modified: Tue, 06 Jun 2023 20:19:32 GMT  
		Size: 75.1 MB (75132944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:39` - linux; s390x

```console
$ docker pull fedora@sha256:19d3970a6317525f2ad33203a808c08ae451dff412017ba4b88f4ced6bee7682
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69240898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5700d648a30edea1116a5b9d61e638641cc027061c771ce7ec5cb47eb3c7de3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 20:43:12 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 20 Jun 2023 22:43:40 GMT
ADD file:ba0720025fa8b2492df2f93521dddd949b29ff7e1fbec79b4216535189fcbab5 in / 
# Tue, 20 Jun 2023 22:43:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6cdee05584756224e3ac70b526af143ae5829d688cc6f78203c900d4bed9f02`  
		Last Modified: Tue, 20 Jun 2023 22:44:38 GMT  
		Size: 69.2 MB (69240898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:latest`

```console
$ docker pull fedora@sha256:e14a428003346bebc13cf03dc8ded0a15284167bc3454a1c40474e01508f8f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:c23aeb3dd1b629e34b49bad4e6295bb5d6e9cb1413d95b2e113254d5ffaaa1eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68307864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795c8dbbab2db9f5858998d948189e2b646caa6f92b35b87a4b80d7634e88201`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 20:41:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 06 Jun 2023 20:20:05 GMT
ADD file:0f119e7993d70c8fa0b6eee79fccf645273ec8be97931d56c36e757c615f3e9f in / 
# Tue, 06 Jun 2023 20:20:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:be3ff91c5bee04b7d595eaaa1c798741cc8d27d3945cda381130972a22e2eeb8`  
		Last Modified: Tue, 06 Jun 2023 20:20:51 GMT  
		Size: 68.3 MB (68307864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:4fc1ddfb4c01afd5dbd1e34b554157235e14184adbed6222723700375b4d8649
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67057126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba921a5e918410083549a2142da0ec063c6f1341db73b0901aaa392dcfd59d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 19:58:41 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 20 Jun 2023 22:41:00 GMT
ADD file:e1af2d14efd2bc54300585fa1ae9b7bf845e8d6a948db0ed61aa8c826a929305 in / 
# Tue, 20 Jun 2023 22:41:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9887f655ffe6443a8674e4433950b274e2a8b7265069a444db775d293cf74da`  
		Last Modified: Tue, 20 Jun 2023 22:41:40 GMT  
		Size: 67.1 MB (67057126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:7fc8668a24d48d783da0785f22953f515e704011be60a34db027cdf9f590b7a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75013876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0b3305f34ebdf0bb09acf248f864948cb6205f762a4bfff52996413c9e57b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:19:02 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 06 Jun 2023 20:17:41 GMT
ADD file:929405ee3c8d4219a5fdf3808bbc8adab3b7afe6b27a55369e1701ddd935eff6 in / 
# Tue, 06 Jun 2023 20:17:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8d48c09810ab6be544595e74ca2b5a1101d17ca0e95a320e75019689da3a8ece`  
		Last Modified: Tue, 06 Jun 2023 20:19:04 GMT  
		Size: 75.0 MB (75013876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:b766297005dfc4fa7b222386089601421c65bbd4af28203d6427a80cc3137a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68880144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4282604cdc90b4fb52329ce3dee4ceb3749dbd15ab590359e821a958dabe42d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 03 Nov 2022 21:31:13 GMT
ENV DISTTAG=f38container FGC=f38 FBR=f38
# Tue, 20 Jun 2023 22:43:13 GMT
ADD file:ca7ca36c3ae04ec89859c84588cf8c9c06ec3360cb66d180de209649826d7f5d in / 
# Tue, 20 Jun 2023 22:43:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8daeecf2a7f8b1e288ef0ba871a4a34acf6b97f092e964b48466bee3d8b924f6`  
		Last Modified: Tue, 20 Jun 2023 22:44:23 GMT  
		Size: 68.9 MB (68880144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:rawhide`

```console
$ docker pull fedora@sha256:0d5881e95c30160ebccab1fb6a6904d59702a6f1834e9098d5c4d4bc260337ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:649ec5c98d263f3cfeb4be02630ddbe7492f967f997986fa2706e83f5ccf6a88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68469901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e956bfeffc9c7a602b1c4d1f18a983d705ad673ba66a4f4e099e777279cf5b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 21:20:05 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 06 Jun 2023 20:20:17 GMT
ADD file:190f7eebffe7e3a50b341655317071726e82b8560aba1fdc0105e109a3275ad4 in / 
# Tue, 06 Jun 2023 20:20:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:83fb1a35b0ac26949417f38861aa80a70cd9d9ddc63ab13bc11f20c9365f7456`  
		Last Modified: Tue, 06 Jun 2023 20:21:09 GMT  
		Size: 68.5 MB (68469901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:72545d387095d2e7779da34faf9e63165a538cec374c9030b695bacfc93254a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67246922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ab1a980e248ec9e60528052cf2dc91943f50d500ce1e040b944284afec11a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 20:39:50 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 20 Jun 2023 22:41:10 GMT
ADD file:d7de6432f5e20fe69c1673a95c805b9f1c069807bf78fe1a4b5ab32f527216e3 in / 
# Tue, 20 Jun 2023 22:41:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1e6aa5d3508a9d83ffb532e3e2b40029f4ef8108972783be7c4f01041cbccc63`  
		Last Modified: Tue, 20 Jun 2023 22:41:56 GMT  
		Size: 67.2 MB (67246922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:4c67fe09823af16107abbed153250649f5dc9db7c1ae15115ea6a1a5cc9f8c42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75132944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e49f96d77faee9414ff7290bf5d4f00c528e5281a60dfc0a6ae8d2fa4b78b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 21:18:04 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 06 Jun 2023 20:18:05 GMT
ADD file:dd1a39c61dcc82b463d39baeca4f2b8ddce1f438a841ddc889993f7c4e19d687 in / 
# Tue, 06 Jun 2023 20:18:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f83bdc4847e939bcfcde5a295a0d2f495e047e37f70ecf8b4872d75719ebb12e`  
		Last Modified: Tue, 06 Jun 2023 20:19:32 GMT  
		Size: 75.1 MB (75132944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:19d3970a6317525f2ad33203a808c08ae451dff412017ba4b88f4ced6bee7682
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69240898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5700d648a30edea1116a5b9d61e638641cc027061c771ce7ec5cb47eb3c7de3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 13 Mar 2023 20:43:12 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Tue, 20 Jun 2023 22:43:40 GMT
ADD file:ba0720025fa8b2492df2f93521dddd949b29ff7e1fbec79b4216535189fcbab5 in / 
# Tue, 20 Jun 2023 22:43:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6cdee05584756224e3ac70b526af143ae5829d688cc6f78203c900d4bed9f02`  
		Last Modified: Tue, 20 Jun 2023 22:44:38 GMT  
		Size: 69.2 MB (69240898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
