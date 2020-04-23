## `debian:stretch-backports`

```console
$ docker pull debian@sha256:e0603aa25797f933811d637f24d5b7069ebdd4e559195390b56e381f687b729c
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
$ docker pull debian@sha256:4b6ec644c29e4964a6f74543a5bf8c12bed6dec3d479e039936e4a37a8af9116
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45376174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9d46a3c72c4d9931a9e48154bb03ffc849d0b15dba1c46ac2dbfc412f38d52`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:22:48 GMT
ADD file:21bf6969c2166c361350c07b1089a1a4b34b7cd3e802a602385d83c49f44a7f6 in / 
# Thu, 23 Apr 2020 00:22:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:22:54 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:99760bc62448fbba69f6f0981d09bb4b7532e17362ecfb709141a7195d9b01d3`  
		Last Modified: Thu, 23 Apr 2020 00:27:35 GMT  
		Size: 45.4 MB (45375951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4ad6bb60d84bcfe3ccb3751298ee1a36e3aed64a0a6c34f0ee162ef0bdf401`  
		Last Modified: Thu, 23 Apr 2020 00:27:39 GMT  
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
$ docker pull debian@sha256:902a7dd3478b719f074b15b3522c95cef667aab1a571d408b5fa6866af49fae2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42101419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f7fcdb18c162fedd2bb3b3c63215af39115fe9cc1c12832a8fc909fc9c5e37`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:13 GMT
ADD file:af00fcaffcce2a55b74d080d33cbc9ce5bcf91faf659b887f508c06803fa64bd in / 
# Thu, 23 Apr 2020 01:07:15 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:07:23 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4168e46f368afa15fa660f5197fb2946df81a85078c82e37a76d2610fb3999f1`  
		Last Modified: Thu, 23 Apr 2020 01:14:13 GMT  
		Size: 42.1 MB (42101192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9912f191a8848bbacc1c39f9e319a2e62cac9d28ee0923c20577d5ee003622b3`  
		Last Modified: Thu, 23 Apr 2020 01:14:21 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b351492805fd0cd9b7e91d611cbb5a3f821a61bf6143ddda1845835e7a025274
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43159245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94638a29ffcc27a23d1bb6440df85ce3d3dc0a1bc53e5d4575d1266e6ad1cfe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:58:27 GMT
ADD file:4921b222c4914e830c4c018324aed1904bf1526e01493120ddc9c905373b2673 in / 
# Thu, 23 Apr 2020 00:58:29 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:58:41 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:decabe2933bfe1939dff94ad523be4904c90e7bea69033943dd32f459d115bab`  
		Last Modified: Thu, 23 Apr 2020 01:05:29 GMT  
		Size: 43.2 MB (43159022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fe8536fd2bb51cd0f86ddef491d9d4f00c58f6f4a141ce9133ba4ead9eb071`  
		Last Modified: Thu, 23 Apr 2020 01:05:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:ffb18c0ae1ceb403b4779623bcb1a5f15cb0f9ea579ba3a6527e99104e15c0e5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6516940f532f8ee733adccc843867b28769194c0907fc8d9d33856b392855794`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:41:58 GMT
ADD file:8306146558afbef9f6d47f7f076c52ab05fd05f1bcb39f7ff213202cd94dcd5f in / 
# Thu, 23 Apr 2020 00:41:59 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:42:04 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1486d1a476351a4d6b262062475bfc82bdeb3819a9b7a2f74f0f5a1e40d8ba98`  
		Last Modified: Thu, 23 Apr 2020 00:47:14 GMT  
		Size: 46.1 MB (46094994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1551e6777ef14de96d8df9a8089bbaab4c238866a4e4712a7aa34537d067b172`  
		Last Modified: Thu, 23 Apr 2020 00:47:20 GMT  
		Size: 224.0 B  
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
$ docker pull debian@sha256:4ba5de99cdb643ed223fd1aa26952ab372025f579f9608bad98859cd09854c01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45232863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fc7119c3e34a0b3cfb15277dbe731b975e1e0dd67cc3b67824c501cd91a9ef`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:53:27 GMT
ADD file:505239a2d83f5f92388d09d24e9986227124ecd0e399dd20dcba6fd8bf627ae9 in / 
# Thu, 23 Apr 2020 00:53:30 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:53:35 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0437d01f0067cccc35f82f17db47ec163f84931841fd7c98aab6f7eae6fee48c`  
		Last Modified: Thu, 23 Apr 2020 00:57:22 GMT  
		Size: 45.2 MB (45232639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb562af2d65e0a65110b2fc75114b2979dfbed3535eacc0161314826da39c10c`  
		Last Modified: Thu, 23 Apr 2020 00:57:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
