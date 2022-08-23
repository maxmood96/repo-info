## `debian:buster-backports`

```console
$ docker pull debian@sha256:6f56e1bb8f8c053d3beac3bb6c2b8d5c88174931a961439e5d753ed5c434f1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:3734d9ee7c61df8085b59eb9446d1bb393cd2079be57203479a828ed7b10e641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50440495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108ca1d7eef73f186278e0c2561c89ab80090606357c464f7167f1c3a99eb299`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:00 GMT
ADD file:d420ffdf63082e03517284553796e5a100e425201458860f07b1aa8598c5929a in / 
# Tue, 23 Aug 2022 00:21:00 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:21:03 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:76dff75df4d9dbdf29a4459adaec745740bfb476cd915906e33eddd9cd94db93`  
		Last Modified: Tue, 23 Aug 2022 00:25:20 GMT  
		Size: 50.4 MB (50440273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91aca20e6874cdcad3f8cdf67991cc89dafc8b048a7661b55d470a5fe0208666`  
		Last Modified: Tue, 23 Aug 2022 00:25:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:010b00b994017d1c4e1fcb47595412860317c52943b7c91b3254aaa0e7883033
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45916043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4eacd71b15238fccaf985bfd5f84962980b9646eb51009bedcc2ce7a72618f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:59:20 GMT
ADD file:a2513870e4a875b6ed767406fe446e1a8548d12329dac6681bf0c22b728d7759 in / 
# Tue, 02 Aug 2022 00:59:20 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 00:59:29 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:25546c90dbccc03d19518f394bfd5bd231736bccd81adbc4903a9df5d94722b0`  
		Last Modified: Tue, 02 Aug 2022 01:07:16 GMT  
		Size: 45.9 MB (45915820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28b1ea75be11b49c46a39ebcf59c60185ef077d26a44847c8f68c82b7addeec`  
		Last Modified: Tue, 02 Aug 2022 01:07:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:383f3b30fcae9e314efd79313c69a485601bdee13648da2499731e917591fa65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49229275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4779c7889b0e167a5e86d62bc523d9b5ce610170f046423b2f724b89d75ca70c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:49 GMT
ADD file:dfd7e3791fa0512f0f7c9cc8530233d6bc1b0a586a3656fd3950ea386754808a in / 
# Tue, 02 Aug 2022 00:40:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 00:40:56 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:71209d5eb534b9e48223962276993c68559f68e230f73c8a0efc2a2998362bd9`  
		Last Modified: Tue, 02 Aug 2022 00:46:28 GMT  
		Size: 49.2 MB (49229053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d21acc4ec7f01836cddccc7bb60f543c395e7d92cb59322a1470c7f2d4f9126`  
		Last Modified: Tue, 02 Aug 2022 00:46:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:270b4b3129c41648ab52d87d626bcee0bc544db048c36f552b241ce9691139f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51204490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6783fc43fb1dd9a8fcd68db9c9b66a54d37d534ab0e7064e9e2ff6f00b7c1fdf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:31 GMT
ADD file:a25646092eaa55ba1e77da8bf292a71c17f8f54e6fa7a3cc057a8bd7d2febd63 in / 
# Tue, 02 Aug 2022 00:39:32 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 00:39:39 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:87423d7294b9d02dc4a6174f8947a28436937897c107e94249f27f8c987b91b5`  
		Last Modified: Tue, 02 Aug 2022 00:45:43 GMT  
		Size: 51.2 MB (51204266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ad03746b7e160bc76ca8b78ea72dca4504ec476c0d2246df4c7ef8eef81e89`  
		Last Modified: Tue, 02 Aug 2022 00:46:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
