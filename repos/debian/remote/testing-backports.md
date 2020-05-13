## `debian:testing-backports`

```console
$ docker pull debian@sha256:0c0a0fd25925ad3a9b3e32fcf08b95275bb1ad679af8339d55b7f3f6fa98eaa4
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:cbfa262d0bb0deb3022c38dd88990ba6fd8a3365fa222cf296e29afa0dc4d94f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51384921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1529a50f0060c5269ee8cf3ff81db8c2f1d141609c5bbd9cce1c8be6af71505a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:24:10 GMT
ADD file:938d55a7f9952b6fc3027163d5f884022164852a3f59a887cd72fb4abd480b23 in / 
# Wed, 13 May 2020 21:24:11 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:24:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d99ec7dde2bb00323766bedbab11c8b41f0df40356503056ed3719e70353c12e`  
		Last Modified: Wed, 13 May 2020 21:31:05 GMT  
		Size: 51.4 MB (51384699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9590650e16391149bcba892a5a9a6b020b8e338e8aeb000d9e5e34b48fc5294f`  
		Last Modified: Wed, 13 May 2020 21:31:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6ee66dfca3b661422ece8005adeb9b03b3eb2b7efcc874aaf659d855410f671f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49935741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244e1b0c71a1e335cd93b6d6434a7cbbe900213d9697c2087f927ea9f41e2b24`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:56:22 GMT
ADD file:23e48d55330902cde3c75947512dfd48297a3041d5406528a911d8f76f015868 in / 
# Thu, 23 Apr 2020 00:56:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:56:40 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aaffc966161dfb1fdc1c94db2cb9cef2a8cd914e343e958bca88fa431afedab5`  
		Last Modified: Thu, 23 Apr 2020 01:04:13 GMT  
		Size: 49.9 MB (49935516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23590c22a2089824170df1522b1ca96c8bfc7b25d2a0d1c4d1f8e11111522ad1`  
		Last Modified: Thu, 23 Apr 2020 01:04:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:cd141e80311ddd549e5306e68b2c3b4a2256c3866dc348e1cb919af9c5281643
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47162495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9e64235320fc597edbd75637889577fe22de9834b6b31f76296a8799dab7f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:19:48 GMT
ADD file:a6656c1767c3aa4fa4364e9255bf59baecf3e1b14d11c5e62bed663be2b60315 in / 
# Wed, 13 May 2020 21:19:51 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:20:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5f3745b1012d32d87e17173996f83b450f6566bac778d26d73bad946652d4408`  
		Last Modified: Wed, 13 May 2020 21:29:00 GMT  
		Size: 47.2 MB (47162271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142df78d5facdbf6b802e1daac4e27b5b7699b47a683a90bba681f93be3eb55a`  
		Last Modified: Wed, 13 May 2020 21:29:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:58d43bcb22f653b51d347349cf6833254a990b3ce80a4196bf2a6efcc58e2845
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50328550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560693efc43ed11a92d543eabc66efbc63a890b561eb3d6b362cef411804621f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:48:50 GMT
ADD file:fad35f66dbab8f1fa900228268afad338103bc98a5c9f92bc41bbc6bea004868 in / 
# Wed, 13 May 2020 21:48:58 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:49:11 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0445c2dc2fee2fa58135941f50318d855c2eebd7ce2e28ed459a7a498aae85b4`  
		Last Modified: Wed, 13 May 2020 21:56:47 GMT  
		Size: 50.3 MB (50328325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650158c9ed7a1de9dfa5f4459127f5765183016930c732ab2df880222f4e37a3`  
		Last Modified: Wed, 13 May 2020 21:56:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:6b8c638363dc50589150f65d99e82920e9936756b5187d87706e7eb8d8592aa0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52480502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e3a4acc3dc0f5b4938000ebbaa175f797fc899f3bf88a7957718db64afd0ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:58 GMT
ADD file:1391d6bcefa66d06d38c6d12cd42e7b8b9a6c9828759b465d6d7ed1d7c4f286d in / 
# Wed, 13 May 2020 21:42:58 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:43:04 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2ddce73e4c851a74eb19cb407063b2febe6d6c618c5a35001c4dcd11157cc283`  
		Last Modified: Wed, 13 May 2020 21:50:37 GMT  
		Size: 52.5 MB (52480280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c9d12fe635e6a732b61a99370f49f8e8287813c3154c97893285d1db36b072`  
		Last Modified: Wed, 13 May 2020 21:50:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:15a9357dc0574dcca3702045003cea303af8fecc4de2e7badd1621e096b793ff
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50694393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a0656a07eaad7289444a0dd0d5b2ff3fc4cdecd1c14098b76012841d7f1e2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:13:17 GMT
ADD file:8965afefe80113b22b46512994393e31ae3e3b6b28467833d110149837d0c6f0 in / 
# Thu, 23 Apr 2020 00:13:18 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:13:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aca473d24d99f30e88d712637b8d1cb5d936e098336de55bb3b14fddba634a60`  
		Last Modified: Thu, 23 Apr 2020 00:24:09 GMT  
		Size: 50.7 MB (50694169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d387ba1a35fbbb390416cd8e01b593063e759b186c3256053acad90c504d1197`  
		Last Modified: Thu, 23 Apr 2020 00:24:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:1c89e499a4ebe4d22bcb43b8403d3eba2d65ee2624e8ef2e0a93b0d2092c851d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55856011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7939d1e3eb777adb47c81ebedc71cf4e0ea0b636bc6f096efcfa7cab4331b1be`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:43:22 GMT
ADD file:0b5770852cbb6853e63220504c01299476f0a003cadc7c36be75e4f6be3547d7 in / 
# Thu, 23 Apr 2020 00:43:27 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:43:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e1e7c37f5d5721f0e34e1aa9562f02e2d7f67d315a93781dd32220d05ecb6163`  
		Last Modified: Thu, 23 Apr 2020 00:56:15 GMT  
		Size: 55.9 MB (55855786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c329fdc0a908be10eeda53e98c00688290c134805e81559677df4094fcb75c5`  
		Last Modified: Thu, 23 Apr 2020 00:56:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:4c03f1510ef05585245cadf16e425142f64cf255118ffda28d50c56d5d1fda45
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49994829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4e3ec9f62c768f3f9cb42e1b55cc95477fbdd4523fa5b7a0c0a65a848b8cd3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:44:50 GMT
ADD file:40041ed25d3ed86e018b850d0e45e1e094ba0affd730cbb11aea89a2387ac0b3 in / 
# Wed, 13 May 2020 21:44:52 GMT
CMD ["bash"]
# Wed, 13 May 2020 21:44:58 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:71e274023239ef09a855049eb6057cca73c68b812ba6c77921eca009476d9d21`  
		Last Modified: Wed, 13 May 2020 21:48:56 GMT  
		Size: 50.0 MB (49994606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9613baac64eea63e98093d15af81ec73c6767fb265b2e2268fa7ccf87d1372da`  
		Last Modified: Wed, 13 May 2020 21:49:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
