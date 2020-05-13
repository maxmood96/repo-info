## `debian:stretch-backports`

```console
$ docker pull debian@sha256:fda9db449fe5affcf8744b84b80bc4bd50f52d434e1bc4328aab633f8fc111e7
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

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:2a99c76d99ff78530bb062185d63964e1ad786a1b819149e1cb5505d119ff568
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45376159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3776cb1214157d66ec82aa9bfe7832d71eadc131b2e91055b9458fb837b1ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:23:35 GMT
ADD file:82e0eb87c6ff97b66f86c9fee44884c4cf1b08f5721f36878fc7a15a125b5079 in / 
# Wed, 13 May 2020 21:23:35 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:23:41 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e6ce7b04634a37b5c20274b3cc1469490cb28f734448d2c84d01454465418e1f`  
		Last Modified: Wed, 13 May 2020 21:29:57 GMT  
		Size: 45.4 MB (45375936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a60e9291474a48588e74a7e95f8a0d0b34dd0f2194f183ef185a2d2338a1baf`  
		Last Modified: Wed, 13 May 2020 21:30:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:34c0ba5a604591d3c3e6afa23b7a5ddad989980f5959fadb90623e12bf8aa925
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44068103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e1ea0d66ae74b0ba7d9349775d279951bc1f7fcde8ebed3b879e6fbd460577`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:55:43 GMT
ADD file:bb686d526196c26500d5e67c5a78c2c48ae413944284d9d6033badae95f1eedf in / 
# Thu, 23 Apr 2020 00:55:44 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:55:53 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:df25bd9cf66a2cc82d5c860f1d1b588ac0a2e23e54eebf8851bae7cdc1b637db`  
		Last Modified: Thu, 23 Apr 2020 01:03:34 GMT  
		Size: 44.1 MB (44067879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fd60c1b2ce9108db317582ca9aedecec302e3db93a9178da7a0b6418820dae`  
		Last Modified: Thu, 23 Apr 2020 01:03:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b50f05cf1d2fff91c8b40f94f1f43365d983ba9ae26ab7fe76694fa5e6f4485d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42101330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c6227bac356cd16baf2ae54cffc7d869796cec994ad0ebf22ce8a2a9b7071e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:18:55 GMT
ADD file:22401e33698b1bb830736dfb4dcfcae97faee4aeb57fbc910c50a0806fb726e3 in / 
# Wed, 13 May 2020 21:18:57 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:19:06 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6d01aee5144e594ba9bd007624dc3b8437510d15e6c34689c8475bf2d6b5c3e4`  
		Last Modified: Wed, 13 May 2020 21:28:12 GMT  
		Size: 42.1 MB (42101107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61579d0860cc3d2f9df0f144e27a919837b9f031175ce1a7076d2632487f1fab`  
		Last Modified: Wed, 13 May 2020 21:28:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1e7e55120add01c2acceaee252750bdc623dec07a1d18b021131a13629362e04
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43159201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e633ba98a25b626d89c7b72d84c2f9b961149d61114758c2c70121a1a1b8b4ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:47:38 GMT
ADD file:e7776aac0b87be303e31e5947db89f835a4e17175e339ec23becf5fe4a9548a5 in / 
# Wed, 13 May 2020 21:47:41 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:47:50 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0480c895dd1d5b237cb931426f18706cbe8dac16e19ed583f3010f3655094efa`  
		Last Modified: Wed, 13 May 2020 21:56:03 GMT  
		Size: 43.2 MB (43158976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95577346c562a1f777b63f880a6ac354a1dad120dfc943ff6b8785db80e5fd53`  
		Last Modified: Wed, 13 May 2020 21:56:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:b6d02edceede28b540ed5b71fca163391e23a2f1e0e03934a91cf431c883cf63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770660eed773babb60d96d175dc66e51c0ec920c14f7396e3a709aca9890c46b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:23 GMT
ADD file:0d501ab6846646b4793ce31bd08a81ee75bf7ca50e44fad4f41d38ea73217f94 in / 
# Wed, 13 May 2020 21:42:23 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:42:28 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:738ccd27fcd21d91d1826e5bb5ee29ef3a82a770de7e1407c86b04395fdd1335`  
		Last Modified: Wed, 13 May 2020 21:49:47 GMT  
		Size: 46.1 MB (46095041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d67272d3cab0be41ce90e33f0d03c5335478fbf14e5331b84d746bcc563eeec`  
		Last Modified: Wed, 13 May 2020 21:49:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; mips64le

```console
$ docker pull debian@sha256:b5873e8ec6d80c3632af7a8f8fba2ac72e137415672f9708e680325b6b55896e
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45049044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d3d4f212599655e403c6ae4f6f21fa401b3469a908589515ed7d5f350fe632`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:12:30 GMT
ADD file:076cd21ba96c7d91a0af4f716c8309a9b092cbbcd4c11f5ead2e2a91dae43736 in / 
# Thu, 23 Apr 2020 00:12:31 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:12:38 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3535f2056d5540d877f08809fd21e68e9db2ecaa1af00cb85b4522a16c35e414`  
		Last Modified: Thu, 23 Apr 2020 00:22:41 GMT  
		Size: 45.0 MB (45048818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748819e0cea413afd210989e30212caff00696ffc3bcc4f90ef3feb9281380d1`  
		Last Modified: Thu, 23 Apr 2020 00:22:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d357faff470b1fd1951d74b90ef248217170ee754bc7f0b903c7315e77e26721
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45646322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635d83715e70b362d0b194bbe9afb30f064b54fe790f1db35f6ba0f3f66e1ccf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:41:48 GMT
ADD file:b7acf2b2b981f87e5f10fe000e64273a621d414c7434c4168273a1639751a765 in / 
# Thu, 23 Apr 2020 00:41:52 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:42:01 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4cde65f7be4b1cfe64760c957dd5bd9fcb4d8704337ab159a9e83eae83a02b4c`  
		Last Modified: Thu, 23 Apr 2020 00:54:57 GMT  
		Size: 45.6 MB (45646096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12027288beff8482df092f6b9d38e65f2dd5583d72b85d6b387ee7df85cd81c5`  
		Last Modified: Thu, 23 Apr 2020 00:55:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; s390x

```console
$ docker pull debian@sha256:1ad7b378b36d3773754b6a9cd2223b241a2ae4e45adde3fc9a97b1b89e7af288
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45232927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd552688db98f03a0e460758009f4460b6040ff6735d2155bc5aaa12fa3a8e27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:44:18 GMT
ADD file:80db5381a461bb249455c6e92a06f91a777c0d8db654106cc55f91d6252c3c44 in / 
# Wed, 13 May 2020 21:44:20 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:44:27 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dd38adf1f4e3b358b79e0f6559fa135ec376d7abbcc3f8bf0b62a2d19d972cbc`  
		Last Modified: Wed, 13 May 2020 21:48:31 GMT  
		Size: 45.2 MB (45232705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219274ce4fd79a171235fb9d0227daa3357320b8e40aa03f4e37a6f6ca5de3cb`  
		Last Modified: Wed, 13 May 2020 21:48:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
