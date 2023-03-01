## `debian:testing-backports`

```console
$ docker pull debian@sha256:84c2e1cbaf432d492f7bac32c17f92079053d766e00fdb4c60a0b333170d64b9
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:e2d95eefc065e447643215c822ce8b28aa24cdb8d17059e92bb7e2653779b42c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacb81b5e85d92a71703bbc198614d75d12919e1b20b0649fc8016102b0d6699`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:11:42 GMT
ADD file:74681cecd762b2ba7998f4db71254724112eeeb0a1801289e92e9be9986fab3e in / 
# Wed, 01 Mar 2023 04:11:43 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:11:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bbf0dc8a79b520e97bfc1897d4020969033cda033c141208013b60015a6334e5`  
		Last Modified: Wed, 01 Mar 2023 04:16:58 GMT  
		Size: 49.2 MB (49237268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db4cabe2406c2ca2cc870fdbb1ba017edbd1b4c7d2e4e980e19c94fbe6b78fd`  
		Last Modified: Wed, 01 Mar 2023 04:17:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e8292f26ce78a896ae0c64fa23eefb753aa26c8a8b463aecbdcdaf01eba1734f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48073055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2334c7148c1590a9b2ede897e9ebb66510fa827a27bb86dac9d7abd4de8bc712`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:49:34 GMT
ADD file:2754fb0733bf053663be45fdf8749e4c88158b9b85a85403f9898c3dfb53215e in / 
# Wed, 01 Mar 2023 01:49:34 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:49:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3ec0704dfd86e01503ca7c8e58baaa3616684e2a382e2ae7ce46e3466830b2a1`  
		Last Modified: Wed, 01 Mar 2023 01:54:34 GMT  
		Size: 48.1 MB (48072831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2df0b944c64529f9142b7c44697dbabf1ad89eb38cbf101f8e7cf9c9f631e4d`  
		Last Modified: Wed, 01 Mar 2023 01:54:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a5c72bc480858008dce9e53be8987f2d867128717b34ca294b588dfcaeb96cca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45843511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef051962bd26553fbb717394fa6cbdd2fc88fce82d45c6290a15dd0a6c4911e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:59:11 GMT
ADD file:6820e6909f34bd7d88f849318c289d08246870bf48e194c42cbb0d2bfe92716d in / 
# Wed, 01 Mar 2023 01:59:11 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:59:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:26dc867e29a6399aa4a7d729a815dfe65dea3873cc63f402795055187cb4b88e`  
		Last Modified: Wed, 01 Mar 2023 02:06:03 GMT  
		Size: 45.8 MB (45843289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068607b3ca26ba811ce31d196a7341ea0ea63e14b171b5bcf9d2e0073fa18fbd`  
		Last Modified: Wed, 01 Mar 2023 02:06:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f3ca69490223e830099bfb2ff3762876cdd274971ff92fdae6f3d0781154537a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49274174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400ca32e84754d40369be03dbad1801a376e0d16def856baba61d9db50ae90ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:21:51 GMT
ADD file:c47730325f9bfe6686c928d0c7c46f6bd75a614ac9bb8bdffdcfef69b5cab2ff in / 
# Wed, 01 Mar 2023 02:21:51 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:21:54 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bd5a6f14a1228f25359ec5248195de6f015069b0c74dc6be8e415fc08ed74f38`  
		Last Modified: Wed, 01 Mar 2023 02:26:44 GMT  
		Size: 49.3 MB (49273951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34f82c07f7384068883b273ee1740f2d68d4c1256cebdacecaef1a34e646bc3`  
		Last Modified: Wed, 01 Mar 2023 02:26:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:b93391bc3f9f9c34d0c178f0b6d61424a42a686597469f89e6b8df11b1dcdaed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50273616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d244b2c2aa266070aee2c27912e0c1ef882553838465763805cec5407cc2aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:43 GMT
ADD file:c00d2713c83099ce3b5f05e27bf4f23d8f3d1234d35e526c414ad2a77fb2fe30 in / 
# Wed, 01 Mar 2023 01:40:43 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:40:48 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8026e865d4c7ec94ce5b33cfaad678239d3b21bb7b731be6e9adf74ed7eeef15`  
		Last Modified: Wed, 01 Mar 2023 01:48:02 GMT  
		Size: 50.3 MB (50273391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5311deae15dc2300ca2d470b7624df4e6b9266b1e37b4173fd0dd88565877a1`  
		Last Modified: Wed, 01 Mar 2023 01:48:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:10b6f73020588e97b4d6c35f65cbf479b1ab5110265e79e34fa80c2cb4f0416e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49245732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16940537906a118a74e5b233a78dbf1ccfb92383fafe7e6d9b7ba52d9d64f8aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:13:45 GMT
ADD file:1bf792d3c4330d4faf867dfb2e9689482bcfd0a8d9c641abd7cca9b6a218978f in / 
# Wed, 01 Mar 2023 02:13:50 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:14:01 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9abd347c7d1810d25b14d496d1aea23dffa3a1bdfd637405ff33a4f90244ddcc`  
		Last Modified: Wed, 01 Mar 2023 02:21:51 GMT  
		Size: 49.2 MB (49245506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1df3a413749712800dd37603aeba16f017976baed61398f73e1f2a83ce6ef8`  
		Last Modified: Wed, 01 Mar 2023 02:22:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:28adf9ba6e33bb79f122c1f341ef5babde4ba9ebc2a02303c5e2a29f2900cc32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53250400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea5f9e31ac248e0d284cf8a766cd348a80c299d37e9e94913c2057f1a4fabeb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:49:21 GMT
ADD file:802564bd8f691b73ccc068cc3c339c6a4c178bcf8383008e4f87a3774cb308b9 in / 
# Wed, 01 Mar 2023 04:49:24 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:49:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:adcb4bfc20e2eddc047aac97edc102514767c0f2b64f4f281f2e71651d1a97a9`  
		Last Modified: Wed, 01 Mar 2023 04:56:03 GMT  
		Size: 53.3 MB (53250177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b217a02928c343fd3b76cbda54988888d584c4cfc9e16ca62c30236316d6509`  
		Last Modified: Wed, 01 Mar 2023 04:56:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:d6ce6feae0b90783e1dc5248c5e6c7864794cf1f5bd9270d3b7a33a2fa661eb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47608261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8ddfd9c5afd4c174f7b8543a1a4f2ce473f730213ba8bc08d38a529d33ec32`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:51:38 GMT
ADD file:8439a18edae9de92ebeb6ca0b69fbd74a02cc73bd2ca22601f8258fa87e9d69a in / 
# Wed, 01 Mar 2023 02:51:41 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:51:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5cd18bb803f30053fbd73f7ae3e9f9955611d476d1cc5d8cd575f473f69eb5d3`  
		Last Modified: Wed, 01 Mar 2023 02:55:53 GMT  
		Size: 47.6 MB (47608038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d828400eff381b7fcbe109a64a73ef1a211c3a20843699322fddde6f341dcf`  
		Last Modified: Wed, 01 Mar 2023 02:56:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
