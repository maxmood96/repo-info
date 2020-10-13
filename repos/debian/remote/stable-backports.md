## `debian:stable-backports`

```console
$ docker pull debian@sha256:06cfffa5072d9f1eb52c4daa63104ea19f7bd5ea669d4036bb125fec13849a43
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:6ca369829ac04693416b29f1e2c38833d28cfc0e4f160df8a853692e18f30762
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50396138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332762cbad3b2b27efcded4d27a147d59ca8954dd699f76c6ce0efaef6c8382e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 00:28:58 GMT
ADD file:ac8c004b00b846c70e0c3fea536b0cc5a0937a2a243e58a7f976e25e0c8ac8f6 in / 
# Thu, 10 Sep 2020 00:28:58 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 00:29:04 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1c2ec57f6e809a5a8cb8436deaa50ee728bb8636363f918f2b03b688d86b8bdd`  
		Last Modified: Thu, 10 Sep 2020 00:36:36 GMT  
		Size: 50.4 MB (50395915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ed1d4a3df80d18dcf7e080767b9d81123827aa66d37caab18a0d6930df6fd2`  
		Last Modified: Thu, 10 Sep 2020 00:36:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:10b3eb76c6bb0a0b34d12b48864cbc37361133bc34b44618a4069163dc67aa95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48109048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d34e663ba2ef2f608a7f025d94c5a815afe52c01bcdd6fd876399b571736ccd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:57:28 GMT
ADD file:7cfa8b499a5aa63a12d5f28d8d514bbfcf5c1d6c0337d16268573660c7225d36 in / 
# Wed, 09 Sep 2020 23:57:29 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:57:37 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4f4b05c6d3fc827d8aaf69e25e815677182776cf17196a89cc6a1efbac58608a`  
		Last Modified: Thu, 10 Sep 2020 00:06:05 GMT  
		Size: 48.1 MB (48108823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47169f5fca4df1fc8fa48abca7aa4da19ae98ca7a982e260f66de72cb0a12fd`  
		Last Modified: Thu, 10 Sep 2020 00:06:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:828d66565164fc1b808c94da052313ae41ab37d7bbe8f306f9c6c233632d741c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45869501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271b9c8a4b877a054825a7208329c7bb4f2c729b3115f821fa064758bae08898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:03:11 GMT
ADD file:e80347b3fe9a358cbcac1ef9642378d9468193000ac4c7675c3093a6c1246fbe in / 
# Tue, 13 Oct 2020 01:03:13 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:03:23 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:975a7da0a330d9dc8df9bca417eae2c60f70b757d657d5618e9f740001725ce1`  
		Last Modified: Tue, 13 Oct 2020 01:11:46 GMT  
		Size: 45.9 MB (45869275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15f9d852b973d2943af0a2d575ac34b25c91b6ab67f0252b7221c82dd8ae489`  
		Last Modified: Tue, 13 Oct 2020 01:11:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1fca4cb499e75d74a14a1e22023c9910f9f400e024418d681b63951f1a500ad8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49175603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ebf3ae5b65b0ad945d274fc39971de3f35c2a5a5044888174bbf504025f582`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:58 GMT
ADD file:5ca7b9d0c7fd89e638c6a9846a2a949742adbcc50cb3800e3feb6c57c368f7a4 in / 
# Tue, 13 Oct 2020 01:43:00 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:43:08 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c6fb6a7a2dca6918398028c24cd1a0d68872503c88a6e42c5bcf5ba80db42253`  
		Last Modified: Tue, 13 Oct 2020 01:50:04 GMT  
		Size: 49.2 MB (49175379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741f6f3bbd737c6e1dfc4bb74d2b34d67380ffe149d177194704a4e1d2a9e69f`  
		Last Modified: Tue, 13 Oct 2020 01:50:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:4b89cc57fc501f5c48223badcd8fea23939bb89d9ccb62a641bce5f59d30875c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51159061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b3820a92a2c0eb32cdf875e0a55b363d5bdf69302b6a1a63b0f02a55443a3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 09 Sep 2020 23:42:53 GMT
ADD file:f53d6d30c5583ebd7cb9f766672adba665371a0b50ca4c8e893fb1dbc4dc1230 in / 
# Wed, 09 Sep 2020 23:42:54 GMT
CMD ["bash"]
# Wed, 09 Sep 2020 23:43:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6e1b49f0102f71c537cf980dee0cd10f130f215e1b1e8f8c4ed41051621f4a92`  
		Last Modified: Wed, 09 Sep 2020 23:48:32 GMT  
		Size: 51.2 MB (51158836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e109d306558867d16cbd744d3852eab50447aba21f256569cdc8989c99cc35`  
		Last Modified: Wed, 09 Sep 2020 23:48:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:3eeb2f48730292b2e2636ba3bf1d58e1d0bce5084fbdd3bbd6890f52c3f8fc93
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49017412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d21624baede0abbea429191f7b4cd3d994a0f67103896a1c92c3fe79afff8ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:11:09 GMT
ADD file:72cdfa882f679ce8fa8feeb0c4b3a3c5a11bea9d8274050044345f4c13128c38 in / 
# Tue, 13 Oct 2020 01:11:10 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:11:16 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9335550774ea0cf524a99090bc694ff244784028cd8555713ab381ba13044414`  
		Last Modified: Tue, 13 Oct 2020 01:18:35 GMT  
		Size: 49.0 MB (49017187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd5f6a5dd1c60361d5cd31d2c74f4d66af157fa2d5b2d7c48aeb19dc83bec9b`  
		Last Modified: Tue, 13 Oct 2020 01:18:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9fc1584d499f087a23085a000a3ceebd60cfe4b5b9d5fe5e80e77b30a9ece7be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54142899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d8a60618ae068c213c405ed39348ed4367996520eef73645c567cc465b6639`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 10 Sep 2020 01:12:48 GMT
ADD file:15f2ae61c3ede81266445658025f8a3fedcede47cbe4edf69d9f1bcbfc6a9956 in / 
# Thu, 10 Sep 2020 01:13:01 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 01:13:27 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6f54d1f5e319b13e0551ebcd7777a13d9e19724b15014565cfae5050ee142a4c`  
		Last Modified: Thu, 10 Sep 2020 01:33:22 GMT  
		Size: 54.1 MB (54142675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3d4ea8e9946a7ae66ca055361e4458dc97806c7e32014c2f227bb78c53b98c`  
		Last Modified: Thu, 10 Sep 2020 01:33:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:4c7cbaecc512ac0580d9938e46f9194c23a2ada48bca45966d793936c9827ce1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48966523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd2ddb629e4c8a13a3b4fac9b447404d3311d7c080c1584a829991c30476b45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:06 GMT
ADD file:28305c36d665c50658295c3a602abc666c49508f0f3f70990069301ca55e0955 in / 
# Tue, 13 Oct 2020 01:43:09 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:43:15 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e23aafa7a2b18d2384e5ffd2a190a16a7836547db442d77848d031e439c9a609`  
		Last Modified: Tue, 13 Oct 2020 01:46:32 GMT  
		Size: 49.0 MB (48966299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687e3217c7c19a9dd87022b667f7f6f2f516ce96f9196d7666c7e2bc104c81de`  
		Last Modified: Tue, 13 Oct 2020 01:46:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
