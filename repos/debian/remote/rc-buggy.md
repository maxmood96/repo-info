## `debian:rc-buggy`

```console
$ docker pull debian@sha256:a8b6cf41244ac4ab412f8986edaca7ad7c518c93b2834992a1603eba079e870a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:f7bda1fb6bd58fa2ee489e4755008f1e59ead8bba6057d526ddcae21402dcb97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49482952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b34b5d9bd870726f23fe84b40ffe4688d4b4a78cc1c0d8a7a00fe890c094a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:17 GMT
ADD file:bc0b5b71ee53adf6297821668404ace4f79c4256461b99497849721dbd8e86ae in / 
# Wed, 20 Sep 2023 04:57:18 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 04:58:52 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d036181e87bed9eb2432498f0ccbf7baa06719a2d8360c3bc9c496bd9f853a7c`  
		Last Modified: Wed, 20 Sep 2023 05:03:10 GMT  
		Size: 49.5 MB (49482728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9543f9ff840ec709f29824e47f1779f6ce05db7ea6fe7876b9a7acb8889084f`  
		Last Modified: Wed, 20 Sep 2023 05:05:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:4f7ce6d0d652b1487d9b618d38c61360383c47a8a036f8111bda223ba3ae4fa2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47166112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7c79e21ca55bb1956da3fed152891d52dcf8ef38007f7d616182bb778b2512`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:51:01 GMT
ADD file:4c775ca1c9a8c87b9e1d380ae08f73f13d6c554601a5b87aef7f73b399316a50 in / 
# Wed, 20 Sep 2023 00:51:02 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:53:07 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:af64b4d6568f99d4aba6c0cd1799711a18174e7c92ab564f1783b1b859742070`  
		Last Modified: Wed, 20 Sep 2023 00:56:46 GMT  
		Size: 47.2 MB (47165885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef5ee7f1773b1180abf295093ffe99722c416b7817855dddff569b108ba3ab1`  
		Last Modified: Wed, 20 Sep 2023 01:00:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:b5b56c364c5783a41ecba50a1f8be133ffecf875e9e2842a8fa5a8701417c6ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44956992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fba4f2c6af8cc47bef6345dc39b05ec246809f05934ac6bb7c362600d6a218`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:58:39 GMT
ADD file:bcf56497ef1c60145d8d33d6611db5afce8122c3b654e448011714e12ab569e2 in / 
# Wed, 20 Sep 2023 04:58:39 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 05:00:03 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:9d3df769ad992dc9a8483f18e8dddf99140307545a5d1930bf5937f68b3c1589`  
		Last Modified: Wed, 20 Sep 2023 05:04:05 GMT  
		Size: 45.0 MB (44956764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d6a7c8c2d59824968c8cf906df3407d90db915b028d479eccad5cf6fbc7ec7`  
		Last Modified: Wed, 20 Sep 2023 05:06:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:85e2564f5b21e054c934e406e5e33d820c323496bd166c1cfecfd390f4e593fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49450716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d133d098236a20aa09484102a2808aa91e01a011f45e27fef4507a981a6324`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:45:16 GMT
ADD file:3493f4ad2710629ee9ad4c981682b2afcc1d9964cb5034de77189556f0c0e810 in / 
# Wed, 20 Sep 2023 02:45:17 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:46:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d83e3b52cf7f7a250777a05d8d2d7960fd6dba8a6438beed3879ff3c389bb01b`  
		Last Modified: Wed, 20 Sep 2023 02:50:04 GMT  
		Size: 49.5 MB (49450488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb5191978a2e1433d7d932ed3bf3fb213113be6f09dca5a12e1a588f5c6ee7a`  
		Last Modified: Wed, 20 Sep 2023 02:52:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:6ce469c68e21c916aa9632af587b836f67d137866735be08be9cfb73c4d09f37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50483353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dabfd2a8f4bfcbf3090fe8144287dc60f26e249972cfcf447c867ad64bb67ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 00:43:36 GMT
ADD file:89a1cfdf26e23095cc168a8c054aaa8afe0cb7f1b748f0dbca755e9aad935ce8 in / 
# Wed, 20 Sep 2023 00:43:37 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 00:45:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a77a25e288eca9c35f0aeada81ba65e2f4beb3d0b739a139eb41bdd87309a97b`  
		Last Modified: Wed, 20 Sep 2023 00:50:06 GMT  
		Size: 50.5 MB (50483129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65acddf67d2eb98450a115639d2bcc9e755c36d058420daf8f24b08474f60324`  
		Last Modified: Wed, 20 Sep 2023 00:53:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:0675dc4b400945c546f3d7755b440cf6a909a9c052e13a1f2904715a18837ded
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49296134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4325fc661922c6aa4544aa6bc4c8b55f6117a6d78cdceb5a0e7b8d2438fae0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 03:13:05 GMT
ADD file:d3d484dbfd0f0dc6ecff269124b80444453666776b40afc16452523a3cc9dd00 in / 
# Wed, 20 Sep 2023 03:13:11 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 03:18:55 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3d916b18191c13bb0519a1e7808ab4f18b1becaa8745ab10fbd22162e95dd7c8`  
		Last Modified: Wed, 20 Sep 2023 03:24:25 GMT  
		Size: 49.3 MB (49295906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8f672c3253f51aeb7fc24ecd50b5c30434bd86a7ac0a3f50c0cde1a6315ec1`  
		Last Modified: Wed, 20 Sep 2023 03:30:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:0b201c53e85c1c31c1a52046f5e5f70b548da766227954cec93c5ec3507265de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53430051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02446067c4091cd97ebb6d00a8b124c0adca0e12d8b871f6e17180a9bd243ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:19:03 GMT
ADD file:0a03052b027b835521a56eb544f68d37afd082caf6b0f2a86d36ba3a4df23574 in / 
# Thu, 07 Sep 2023 00:19:07 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 00:21:56 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:61513ad4f292fbcfceaab5e01ed63b82ba881a99736b2ffd97579f96947c0829`  
		Last Modified: Thu, 07 Sep 2023 00:25:38 GMT  
		Size: 53.4 MB (53429824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fa69f9835a1f2c348460f80fe08b5f8f18414aeb954120e6a1429c38022615`  
		Last Modified: Thu, 07 Sep 2023 00:29:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:46abc0df6f9937cc7588360f715b1a3e81a56250938955792f058dc913409cc0
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47886231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90508f15e429e4b3f1811cb12897631267f4fc757bfa892661080b4501cbc60b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 01:10:40 GMT
ADD file:1f642efb72cdde4ae806c2daa6011fc8bf9064f9ca1495c204a2329c8224085e in / 
# Wed, 20 Sep 2023 01:10:42 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 01:12:28 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:dd92315c0266263460bbfc9a32f8e00d31dd51aaf5819be923d34de88ddf3545`  
		Last Modified: Wed, 20 Sep 2023 01:13:31 GMT  
		Size: 47.9 MB (47886004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bddbdd63848c4d04b14caf62c39cd997a14cdfe2add8c16bb4d882d36ee490`  
		Last Modified: Wed, 20 Sep 2023 01:15:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:1bf9fc9393923b6ebd6e46c9e6c88b29dbdfd561957f95c503e943492e9d7141
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48852906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f1786d5c9cc070e471cda8507660e8eff63ecb24483b02205c37bd364f2423`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:55:43 GMT
ADD file:aeb19ed2c9b92cbe76bb1e733b04de5bcb32489c00c1c06504aef79cd36c3c3f in / 
# Wed, 20 Sep 2023 02:55:50 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:58:28 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b1b4950b21705690e4b15e5257a0efcf7d334776307aaa893216166a5c37f2c0`  
		Last Modified: Wed, 20 Sep 2023 03:01:02 GMT  
		Size: 48.9 MB (48852678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbb598bcea03e6abf06908bd3a806ca2c446227b541282a7fc316d35d6f5b8c`  
		Last Modified: Wed, 20 Sep 2023 03:03:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
