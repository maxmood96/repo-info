## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:8bdab9c98547dc8cdabfe63036b92c7a80e988eb84c8cc7af10ec84265bbc6d7
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:7df948cda922346a152453e8c5221bc485994a673d93bb9186aa5ae9dbc76f5d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49556925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21f8d0691a2b62d3c7ede39f89fa69444757567b8b7537e2c7dc5b6cb580323`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:39 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4078a8d2540026e08753e643da1f12f1d734119d95c402e7ec9de2301957f8a`  
		Last Modified: Wed, 04 Sep 2024 22:34:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:0d76cdb02fbff56c5c96e594f5246d8d0dee1215c4b6447fc3183b57047a71c0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47333419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef60ffb71324a69d2b6083c36aa1077ba665b67963ffc93d196d767ea4fbed63`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:22 GMT
ADD file:7ffef6fd95a7091f8058ff29f285ea1ff980523eddf5b8cbcd5ced08753075c5 in / 
# Wed, 04 Sep 2024 21:48:22 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:48:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c9500290eb8f2377c9935666a66a6f2f71959169f4c4c62904bd950e7f1cb1cf`  
		Last Modified: Wed, 04 Sep 2024 21:51:08 GMT  
		Size: 47.3 MB (47333195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c24f84b1545bd355240fc6e859c4816363bf2ca615bad411164010580b31c2`  
		Last Modified: Wed, 04 Sep 2024 21:51:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:78bb92d413b4c7b8771b87bffb849db48944266d228ebd065fccab3af0281d57
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a2de59a0bfedd462cba014bce645d8bab83b925a323965e908674e5c7a9a36`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:57:56 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Wed, 04 Sep 2024 21:57:56 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:58:02 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904c52c73be85fe6f8e90287088a74d62e59c9b3e89a39d912b7e6d520e7182c`  
		Last Modified: Wed, 04 Sep 2024 22:01:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b11bb7a6f3ad3ce46bf74876e5f2e611a8f489bf695cb98aa09881e66cf14a6e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49585847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2937618af9f59c27930764e9b405e5bf23c6ec3c067ba5f9c35ca3846ffac2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:39:47 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5e3ccc15c551a1ad31980971f380be7d600b14de827e8a22cf995ce2fecf5d`  
		Last Modified: Wed, 04 Sep 2024 21:42:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:47844f87ff5aa70a34d6f164128ebd11bfeea16bcdcc1bed4da9fe4254a01b07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50574832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28284a2d7d4f4d34fff009675d7bc8e1b94c6f4eb46d2e5048f927f567b8a111`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:24 GMT
ADD file:c4052556120bbd9469f83c0cbc2abed04e22bd316491de6954bbbee12ae8b9bf in / 
# Wed, 04 Sep 2024 22:44:25 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:44:27 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e9d39ee40700085571f0a8e492b9b3a1fc65d55e5816aeed53fa9575b0013a98`  
		Last Modified: Wed, 04 Sep 2024 22:47:45 GMT  
		Size: 50.6 MB (50574606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17af8ace8ee2d1d4d65f3b01ee84bc4ce6bd1723fe418adbdb010162ceb06d5`  
		Last Modified: Wed, 04 Sep 2024 22:47:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:f9a1bf0b544e10c053c53036dd714cc325c0d1e1dd7a13e5163f4401b9ff8c83
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49562230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84caa71ba7cc852167a3f13ecb7ad573ca243790ffae2defd7b94c7fde14d5cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:14:59 GMT
ADD file:7a12db48c47f9e4ffb57061ade21f94ff0eb0791886ef60b56a9820f096b39a2 in / 
# Wed, 04 Sep 2024 22:15:05 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:15:22 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:15bebfb1ce6517765581a89c1270a3039857497f5393a3a53eb55a6cf6c3b9e9`  
		Last Modified: Wed, 04 Sep 2024 22:23:29 GMT  
		Size: 49.6 MB (49562002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0787c411c1074225173fc9c94b223733df1ba8e4348fefdcba9a1e268c99d9a0`  
		Last Modified: Wed, 04 Sep 2024 22:23:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:72cdaadf6234eb24c114eafc38e937a8c91798c71cfd03a36b6ba74b2d746c84
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53554171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019ac59c7b79b65161abf83b018bcb7f887b2b5a3f965aa4d14fca0c2bee9637`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:38 GMT
ADD file:c5d3aa6402ede77c4a443935fc6572b655c0144f8f41a2967e2e2b55b4c3343e in / 
# Wed, 04 Sep 2024 22:25:40 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:25:45 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d0634fe6314ffdff41b21ba805323138b719229ae2c5a32bda44147f688ed49c`  
		Last Modified: Wed, 04 Sep 2024 22:29:47 GMT  
		Size: 53.6 MB (53553949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e31a0656c33be087f2d6e85d0cd87788216492f90ef677379d706bcb40ae7c`  
		Last Modified: Wed, 04 Sep 2024 22:30:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:1c3668c596498a2fc9cd0461fdea2a41469a9a71685f42f207060ea6858d8603
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47939500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483712f42cc6fbcb99641ccce36a34c7cb503e957ae49e527c6069a23ef8e222`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:25 GMT
ADD file:61b2bf58d4b2b852e6903b24131c8a331d7a1afe2cc99c4dd08ddffc91545071 in / 
# Wed, 04 Sep 2024 21:42:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:42:40 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1f3378e3b07f08dbf0b6ce13220a2997d788ba77fb8aa9394ce275771f49ec7a`  
		Last Modified: Wed, 04 Sep 2024 21:47:26 GMT  
		Size: 47.9 MB (47939277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9c0b773b42d2d67bae9b502cdebce3cc01ae622889b0148e24329183b0b4af`  
		Last Modified: Wed, 04 Sep 2024 21:47:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
