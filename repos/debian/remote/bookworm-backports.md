## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:9048c997284a45707670b6efdfcf5f85d166cc3ded16c8ce7aa5635d89f2e9cd
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
$ docker pull debian@sha256:1d8f26f94269c544c3c690fdd880ef33a026561fd2ded3114e70fcd8357580a6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55599028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5554a6f460ec002fa1d82751f3015d5779c9ddb82aa5f7e6cdbaa4ff9ce09dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:09 GMT
ADD file:15e5b0a35c4fc7a5ae0bf08f713bde738d2cfb06a30b8bd5780fabafb91d934c in / 
# Tue, 21 Dec 2021 01:22:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:22:15 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9aa4f47c6909274e4d7f0b2429a7ad24598b19c01da78245a16a3176f9acf847`  
		Last Modified: Tue, 21 Dec 2021 01:26:44 GMT  
		Size: 55.6 MB (55598801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2099a22743fb705d95cc1f13086e834534ff8bd3a71afc9c2dec3dea55e3c96`  
		Last Modified: Tue, 21 Dec 2021 01:26:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:7d56543eaba8e307e816df58150f0042a4b313f4b8049d62d7bd4db9b3702029
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53058775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84c7029d7768546426397242ac0333262c34a13399a6e1874761051f8bff66a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:48:58 GMT
ADD file:06611eba7b36a7e9c8c68f1d8c97d596b024eefb00a7b0638c9ccbeb8a6f9142 in / 
# Tue, 21 Dec 2021 01:48:59 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:49:12 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:13e93eb93ae4e3d37ac97bb105a341f9c56baf0c8b9fe4707b27ad57f5633247`  
		Last Modified: Tue, 21 Dec 2021 02:03:43 GMT  
		Size: 53.1 MB (53058545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9e64d64d05d715e319d8ece4129f593caac7ab6ef497e3d80cc31c845b4d3c`  
		Last Modified: Tue, 21 Dec 2021 02:03:56 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d4c89e4c97054b068de5d021530ebcbfcc173725252191e5d9aa0bc184945961
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50699124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7922d534b777e517a26af25241087757ceb5f03827af6f0c2d099099ffc9ac3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:58:11 GMT
ADD file:7ed54a4a4704538f37ad0755a81034bc1bd04ec05d6e2a10f3dc44aab517bd3d in / 
# Tue, 21 Dec 2021 01:58:12 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:58:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:661d8e50ead70cdfa65f1e6cee609c2fd7cee22ad5c09bb02a88c7d51c60da27`  
		Last Modified: Tue, 21 Dec 2021 02:13:26 GMT  
		Size: 50.7 MB (50698897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0bb26f83017de8580c6065b3c25569e5419d8deda63b3a6c527b98bdc0fc33`  
		Last Modified: Tue, 21 Dec 2021 02:13:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ef92d8dd8869716c25c8211f004ad7fb81b17536f5f01e4a6c6471b36844188d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54598302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f4a49f9f3d9135af0761def00dcb9fd3943451307f014576279da2ef2ed78e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:41:45 GMT
ADD file:c64482c2e0b0935b000b024e468499d2586b78ca5c64b035ded7ce33f1dabe14 in / 
# Tue, 21 Dec 2021 01:41:45 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:41:51 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:be902f523b4c4ddf53ea157e340cd7ce836ec2a0952d6f18602467352524e312`  
		Last Modified: Tue, 21 Dec 2021 01:47:42 GMT  
		Size: 54.6 MB (54598073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d613d2f08ea4778422bd2ba397bee84eaebf30ab00a6f71dd8a839176e4be3e`  
		Last Modified: Tue, 21 Dec 2021 01:47:53 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:340665a87da6a9ceecdb7323b9ed73f1bb71ea74f6fc3d461ce72e3cc86e2c4b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56659109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc238df9b2c65d0ba3edbfc1c0c15bbeaada1afecc84fd894ea1e695617a9ae5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:39:06 GMT
ADD file:f5394800b665e61b6f319d6dffbccd66c1172d4e9fd1db6ba962ef5aa177c353 in / 
# Tue, 21 Dec 2021 01:39:06 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:39:14 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:75388d3fd5f848339be12f5cd41cdf79effd086f4656396bfbac934b7f1f715c`  
		Last Modified: Tue, 21 Dec 2021 01:47:16 GMT  
		Size: 56.7 MB (56658883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40897c697d656807f44be27613477b212da6f33281e2ed10edabecf54fbbc485`  
		Last Modified: Tue, 21 Dec 2021 01:47:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:0d201dca8e5f66a51583d68e73ae951ceeec98946d4baa32226440c669c46b85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54302957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8400de8203a3c494543ea366d719f3ac0660702cfd9e5d561f7ff6f0cc08b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:07:47 GMT
ADD file:41547ce5cf30425be5612cd827fbdd2cf3e3190ecb39bf4c5a634512db860237 in / 
# Tue, 21 Dec 2021 02:07:48 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:07:54 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:847df5d6ab10ba0e4a41a13ce3d04aa9d5b5c826a90bc36162239e7587e48cee`  
		Last Modified: Tue, 21 Dec 2021 02:15:49 GMT  
		Size: 54.3 MB (54302729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad91b0233a764ab492f3f265758ab3610f29af0c055bf68b136f596e0d40e8d3`  
		Last Modified: Tue, 21 Dec 2021 02:16:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6d0d88b393d7ecd6090bc5f8811555be62e48d68532e5e5c62bccc5ef2149f6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59991993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc3713e969c50674ed7a676ed4b5beb96bede6d8ae2413f039a61dd1fe094c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:18:58 GMT
ADD file:b2445892db6f22a700090e84ea01cec8156666af13bbd1943ff76648f9b45fa7 in / 
# Tue, 21 Dec 2021 02:19:03 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:19:26 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:acf94744ccb1210214c86a9a0cddb19c2809171609310c507f8e988f1e399199`  
		Last Modified: Tue, 21 Dec 2021 02:27:45 GMT  
		Size: 60.0 MB (59991767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6cb348d385089098e06717eb5c4f4cc400a315989d95d0ca53e3ebf2a35005`  
		Last Modified: Tue, 21 Dec 2021 02:27:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:b0f107fe07dc3ae4711e2e13552787614cb3fdde491d3b2f61d8719d4d96d9b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53888670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464b229ccf544e5937092177ec5c892b18376a61d8639dc4dc55aeed45e9e3de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:41:36 GMT
ADD file:c9626c75e4b53a0e71f37a2a3df45699d003ae102e7e3eedc97afe7897f82180 in / 
# Tue, 21 Dec 2021 01:41:42 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:41:49 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:341c5a56ba0f7b7f22f0613addb31ee3342e410686dda8753a049d0bd1f319f3`  
		Last Modified: Tue, 21 Dec 2021 01:47:23 GMT  
		Size: 53.9 MB (53888441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3798eab2774bbc8f051eeed888c6fdc1837bd54d7fae09de3dd744090b1da02`  
		Last Modified: Tue, 21 Dec 2021 01:47:30 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
