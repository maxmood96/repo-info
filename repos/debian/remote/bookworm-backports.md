## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:557cea5837c253c607ea720589620a1b6506f503f2fad9e8156dde12cb0a75ab
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
$ docker pull debian@sha256:1ecdabb4a97d0563e556918aa4ac94b526dc487441d40d6d9b3ea63ad7de0afa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49582452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce73d0ac23d76c6ff9f7e4aa1c6bf9a354a69bd078e0388e6b64c9c0fe03d9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:34:43 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc4be1c28e7f9edc37540ad8e4e7e11da61ff9ca5805632c2babe6ab4c127a1`  
		Last Modified: Wed, 11 Oct 2023 18:39:25 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:18e92b71d2b5f72a3b3c962335b2c6dcd51e85de718d546b221619c3102310f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47355974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4c71a45b200d827cd7c5fb68ffc4f6f68831935c79223204d546f9bd0524b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:37:30 GMT
ADD file:c07cf5c750a3e3c7ff84a3a3b8fc6087c9c5e0639d7bf638f0556d0a94309919 in / 
# Wed, 11 Oct 2023 17:37:35 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:37:38 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b7ec6536594e6c45ab234eecb51aacd85440ddc0e6da5873de23938ff146b5ec`  
		Last Modified: Wed, 11 Oct 2023 17:40:19 GMT  
		Size: 47.4 MB (47355749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c0f1f60b1f61dd88e782684665a86490b6ba2631de0300cbdaab26a4297203`  
		Last Modified: Wed, 11 Oct 2023 17:40:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:313621e7fe302ace08f43fd49553df103ba146a13f8e635bbda840eaffed6a4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cf110ef200b1e28de1adb1ada0ef815bbd7ef256349ea58253efa816ddc2f3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:59 GMT
ADD file:914e8a43f38c44fe9a6aabf05bbf3ebad5530966a354c8e7bb873c0842d35256 in / 
# Wed, 11 Oct 2023 17:42:00 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:42:04 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:65b9f3344eccdad2292cc7eec885befe05a52ec1136e145130c849441428eee6`  
		Last Modified: Wed, 11 Oct 2023 17:45:56 GMT  
		Size: 45.2 MB (45180287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad05fc3290f9b03514ecf984de423228535efe8ffad479fdb804f91eef9a25b`  
		Last Modified: Wed, 11 Oct 2023 17:46:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:96d8c76d2a66d083717f4bf9c95f43fc5e4073d271298c26cd53b877720fdc98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49612802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d7cb233cdd89bb22ef37130567aa2486bdfa455ab9a90a162346381a9f521b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:24:46 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c106472958c2e0269b25dfb7a6a57949bf7449f6d6487718029de810efa40ea`  
		Last Modified: Wed, 11 Oct 2023 18:28:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:aa77a20c71f2004605bb2b0faf69dfc43c0366815414e00ae2cadd381dde4228
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50601015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6e6e4351fbcb7ca2b8313fe742207561a3055219cb55928ab2df2e75b9efff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:40:29 GMT
ADD file:0b6fc66d778d0cd8ae8b17b92945d98cc34f9c7008cda864ed0a54b5e40b9cb0 in / 
# Wed, 11 Oct 2023 17:40:32 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:40:34 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:501a599c15b6def048b2e00cfdf6c658061c00a504305ef2075fb1009a62c1e2`  
		Last Modified: Wed, 11 Oct 2023 17:45:01 GMT  
		Size: 50.6 MB (50600791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e624c761a6cf1f825fb104093a419040253ad9d0b73f352a35144f2899b807`  
		Last Modified: Wed, 11 Oct 2023 17:45:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:430d1c1cafd37c8879ca8b62a9aaa0e14a23c9d7fa21afdfdbdbe5e1713d2b6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49569485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa00295adfca70a332e3daaec63ea72918b5bb836486739fa1f1d97676a569a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:48:50 GMT
ADD file:b081db8d48290ef5b5f477edb85d8f04d62a6995ec09bdb516d66dbe19b98137 in / 
# Wed, 11 Oct 2023 17:48:55 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:49:10 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:54dda4e4d31846b7324172a7fda3d0bdc7d8a2105ab27e9a92c2db43f35f9e5d`  
		Last Modified: Wed, 11 Oct 2023 17:59:53 GMT  
		Size: 49.6 MB (49569257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a024b6b548fea662a613ddf8b1be7821a1987b896790b8a9cf7f093c7503fc8`  
		Last Modified: Wed, 11 Oct 2023 18:00:18 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:eeb425c5cba278113579065b670025180779a990182a1be1dc65f83f2561b3b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53576210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299d62aad320b90cd228ff769136b4004020470ad5aafae5a03594406b8a3c47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:01 GMT
ADD file:ed515e1aef8321271c6544e30cbeb31257e9640979e8f68a9e490cb25d3525fd in / 
# Wed, 11 Oct 2023 17:44:04 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:44:09 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f137383853e717724a59e86aa526d31eabb4a5d45a259cd1ade68d93b3f45ae9`  
		Last Modified: Wed, 11 Oct 2023 17:49:27 GMT  
		Size: 53.6 MB (53575984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca97215dc13174c10ff3f5186cb53f25d946baa701f9a7b589be6639014d8a97`  
		Last Modified: Wed, 11 Oct 2023 17:49:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:c86955e8c0fa2dc71fd57bad702c36e7cd814972cc875e158f543e36b3379144
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47943159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5c64a5fc5420977f70144416b6f0e530923596cc08a0a361e65336a137678d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:07 GMT
ADD file:2dc117136732884ad4b058065700dd66cc49d6ce56b0fdbb672915e3ad8adb84 in / 
# Wed, 11 Oct 2023 17:50:10 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 17:50:19 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ad5e374600bf40a929dfe51e52737e4ca04aba83f499656760ba938841fb6552`  
		Last Modified: Wed, 11 Oct 2023 17:55:18 GMT  
		Size: 47.9 MB (47942934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cd061ac3f880eccbc30a19115d3749f1a82433edd55eb56a5124210b488f8d`  
		Last Modified: Wed, 11 Oct 2023 17:55:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
