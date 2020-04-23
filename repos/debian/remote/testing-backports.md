## `debian:testing-backports`

```console
$ docker pull debian@sha256:ab4ddf72f7a78969371d5f3af4c79612d6ab6a42e9b40ee1c02b5d68956aee94
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
$ docker pull debian@sha256:0544e5c816241880d5f106ea4e6d4285e6dce1632b0faa742ad857651462bb80
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51981441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11739e8e919a4028558b6c2e41cf64a4deace1adf075f522f0c89012eda9d791`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:15 GMT
ADD file:19296a07e1c4a35ef4bd6813edc5f8402d5c77ce03f19354ec6b9b7db5286aa5 in / 
# Thu, 23 Apr 2020 00:23:15 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:23:20 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2dffa903b83a05e8f7056f2d8f378ea21af1cbc9a30f68bb9f93f103520963cb`  
		Last Modified: Thu, 23 Apr 2020 00:27:59 GMT  
		Size: 52.0 MB (51981219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcba46f841681351a4185769b62f19610cf165ffd1d25594fd88dd88ff6f345`  
		Last Modified: Thu, 23 Apr 2020 00:28:04 GMT  
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
$ docker pull debian@sha256:106bcf93fd562fdc44e7fa1c75442601233b8a34979a9e7907cabd4f7fdc91cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47659391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b88d576034d2cc17d62d086b0a2967e5a3c34cb4c8045e52e978dc5c3f5c94`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:57 GMT
ADD file:80e89a07fc7421c4e328dc7a8468c471d8f592152869ee9dd558c38783bdf60d in / 
# Thu, 23 Apr 2020 01:08:00 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:08:08 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:57f0b66619e4e589524dbfad62b285e08c346345d8a3d21fc36aa590f2f547f3`  
		Last Modified: Thu, 23 Apr 2020 01:14:58 GMT  
		Size: 47.7 MB (47659166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b484fbb69968787ce2b0445575147ac6cce462f7683452fd6058d7b76737ae47`  
		Last Modified: Thu, 23 Apr 2020 01:15:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6754aff57cab0871c2726d320fbb1ca8b211f023831c9b112f3e9ccc77c98e0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50908368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5de26f6084f72132a9371d663401c0f416d001c909effa94b290f55dba9520c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:29 GMT
ADD file:8d6493850808494b9c8355d7605648137017d4ab385d5f2f709e2b004ae55495 in / 
# Thu, 23 Apr 2020 00:59:37 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:59:47 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9edc88ed1cd036e1398512e49d4ca915c1b089667581f9b64036651a5c5569f8`  
		Last Modified: Thu, 23 Apr 2020 01:06:34 GMT  
		Size: 50.9 MB (50908144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dcb3ff698c954dc2cf72381032e4e307dc41f9244d3f2dce1e4f0984da52f4`  
		Last Modified: Thu, 23 Apr 2020 01:06:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:8b95788867388515eb44ca5e04e7c27b587ad03e69bbf89595c1a23f296f4ffc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53125025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09658ced217763e2641de41d3307c5d79e035a81e3c6059bfc3f2521cb5c5d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:25 GMT
ADD file:66ce6a333e02ded4796aed0b73dca44eebdcd10d3276bfafd6e35cce8b33bad4 in / 
# Thu, 23 Apr 2020 00:42:26 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:42:32 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41e5514480560cfa8cd27b0138fe7133857c22a04253775d736219697aeed383`  
		Last Modified: Thu, 23 Apr 2020 00:47:58 GMT  
		Size: 53.1 MB (53124802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8ebb1596a647d5db3cf5badf6831601ac5c3076e05ea6493f45ba355f0c7a4`  
		Last Modified: Thu, 23 Apr 2020 00:48:03 GMT  
		Size: 223.0 B  
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
$ docker pull debian@sha256:947a94d3a6b113be10ee8a38bb4af3b6c84351a453c43a5119cffaf1596796de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50580150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b2e1f3d079e29f62373d8629813c07dea8aa82b98bad27ef31289b2aef8cf1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:53:57 GMT
ADD file:97140842c4b6f570aaf6d76200a8d90f86a0752d52190e946e3a796434e839b8 in / 
# Thu, 23 Apr 2020 00:53:59 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:54:05 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a98742adb13e5b8ab1a841db4b714a01eb6184aa8bfbf280e17ca739ba3b60e0`  
		Last Modified: Thu, 23 Apr 2020 00:57:49 GMT  
		Size: 50.6 MB (50579925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1557980f26cfa21b2e30a130c865ecc22d6518b728a35a9515db96f99fa617f`  
		Last Modified: Thu, 23 Apr 2020 00:57:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
