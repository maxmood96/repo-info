## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:9a2d81959552f406649e2bb884a54a18dfe990bfca7dfaeebd1eb09609c29fdf
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:d4715571597f03dbe710a13243653f1b13efb87a627a3ffcfc25b950a2bddbdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55090489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30774bb4287d6ecf23322952016252af0cc1b1afa424a8ae9c680bb7030769c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:51:03 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ad80a8cadcddf397467e6099cb1e23bee7a0e0d2fbf4fe7030cbabe8c82f11`  
		Last Modified: Wed, 10 Apr 2024 01:56:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ca4dd8e14c26692c9a69426bd202044d3df074a0c94c6a673219bd2f28dc0026
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52591861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc973b4c79195e21684c48fe1acba30fde4115e1ad447701e19b654e7fbc3bde`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:49:22 GMT
ADD file:1eb31b3bcff4decb2d77374005bc7e0451f76188c3586232986a3f72e069dd04 in / 
# Wed, 10 Apr 2024 00:49:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:49:28 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:73e28a24bff6aad570d221d844a24c5be13f1afcd4819e3c4842ae6b4ae928ed`  
		Last Modified: Wed, 10 Apr 2024 00:54:59 GMT  
		Size: 52.6 MB (52591634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730b17fa5e32f07f1d7cae27bb54b0f253c8b7ff262a512fa80771ef1311f621`  
		Last Modified: Wed, 10 Apr 2024 00:55:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:e1bb2532ba8af9e2fa93201be549306e83371d5c9c8d11473cf03682fcdd9489
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50246709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbccabd94d6387894821f946ba354d03773a605e7810000b134c0c1930b391b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:28 GMT
ADD file:eb53aade3ed19f72413045948cad3084902fe630cc20789d2c2b5bc334679575 in / 
# Wed, 10 Apr 2024 00:58:29 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:58:35 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:23ca580217f1a6b17dba868e7ec34ae7fff221e07640fca532510daca8ed46f6`  
		Last Modified: Wed, 10 Apr 2024 01:04:48 GMT  
		Size: 50.2 MB (50246481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21b2a609e8c6163767c9efaec14759ae59c7185e0e11ebc8396cec875c4672a`  
		Last Modified: Wed, 10 Apr 2024 01:05:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:08d036f020a3d6f88cc21c8b0fdd125e38785148954e4fd381a586edc9fa05a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53729401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1192b3964c9ccaa07d6dee3b590d83a2b216468f3f3f0f122c626e494c2df038`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:40:33 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c096a50eecfe8b92ee9e5d01471b11a66d5951c2c7fbd8c92f37e92397506ba`  
		Last Modified: Wed, 10 Apr 2024 00:44:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:aba5a41b7421fed7411d82c8c5c506e01a2e68cecc6cde4726c5044cc73386f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56066412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea84cd3f07d64001a1e64227cc92c8ea86d144d53a1a2ef0712f35e273980102`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:22 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
# Wed, 10 Apr 2024 00:57:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:57:26 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71f8bb4cd3145f4ede7ff6b094676b9055822a2200ecedc246765f3c43b1fca`  
		Last Modified: Wed, 10 Apr 2024 01:02:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:3a851788d23b42fc754a5e69a44ecff82b0e82d459ec74f8f0a14a939ccee8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53310031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b1933d53d5171ebe2b37721c974917647f883e8414c16ebcd7884450b29ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:10:45 GMT
ADD file:b9ae0499407c5db6a4d213452b2b485d2f0c9fae0792c77a629177988969faa3 in / 
# Wed, 10 Apr 2024 01:10:52 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:11:02 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eade21836c93150a05690be18ba07f9d56297d4f2b59f348647ec05e7c1435cc`  
		Last Modified: Wed, 10 Apr 2024 01:22:42 GMT  
		Size: 53.3 MB (53309804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c98017f1cac30146ddee07b91733318fb6673faeb17005149d42bf4b3c88a84`  
		Last Modified: Wed, 10 Apr 2024 01:22:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:0a69313e0ffe64167cdb1bce2bf350db605c5e2fd51d29bb7d302391e1240e51
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58959258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb99e00955998932a89a02498965e7f9b2a7e3a2db80b81dc2147de19d7a752a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:26:45 GMT
ADD file:774dc7f7db45435bfddcc1ff7bb4ae0716252e8f7c3d074ff7611070207b8314 in / 
# Wed, 10 Apr 2024 01:26:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:26:52 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eed533dbdbda3df66dcde8a75fb0ab317466f575d116ffa4e053da66ab0dd942`  
		Last Modified: Wed, 10 Apr 2024 01:31:35 GMT  
		Size: 59.0 MB (58959030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea4ebd656b6bfc969d786ee97e57e08e6fe4dd703004a7e5267d97efa8c5e6f`  
		Last Modified: Wed, 10 Apr 2024 01:31:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:548650bbac9140a6889d93fbf18b4db1f211d0e718b1060b70aef874c2481a9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53325163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348f4fdbef49f6b6ce512cadbf7df560eb74a802f60505170e815fc249137218`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:16:37 GMT
ADD file:ca4cd0bb2344426b8777da3ac3278e42efb1e15064ff144111d7ecacdf3cbd4a in / 
# Wed, 10 Apr 2024 01:16:44 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:18:29 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8d59905935c60c8e62d2bce55ff58a911d9ceda48b95f8209712af92b63b5ceb`  
		Last Modified: Wed, 10 Apr 2024 01:48:44 GMT  
		Size: 53.3 MB (53324935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19f01b148903e9d05dc32a223304bbff444788b5968c26e5864f6d4b541a047`  
		Last Modified: Wed, 10 Apr 2024 01:48:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
