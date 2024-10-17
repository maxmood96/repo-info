## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:4011e3482239f971a622e0920c4adb50546b93b55611151bc9644902698ba1dd
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
$ docker pull debian@sha256:b3b77b2cbf5b64d02f92d9ceb7e9e846d033d3f91dd3d942177212688e7467ac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49555248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2629de5247de053ddd7e512cff7c8d5714c7ae77ae151435fcb7d81491b680d9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:17 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 17 Oct 2024 00:20:17 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:20:22 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cbd7ed1971391b93f5289b75626f89d81cbf61f97f87a62e924f693d9d5fa4`  
		Last Modified: Thu, 17 Oct 2024 00:23:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:005eb6def7a0877b6769797ea3f1949f561bfaddf21e43cf1a221567597f84a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47330747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936a0e17c3cdcbf02c9b987c3b4772547b8b66347b791e4f3609bd032f628d84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:12 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Thu, 17 Oct 2024 00:54:13 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:54:19 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf2bca8acd294df1dc44dc5c47a5a85038d1be3207686d1ddb7c18b1364e69`  
		Last Modified: Thu, 17 Oct 2024 00:57:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:657f0faf4061cbaf70e8e5e8c97de0d7341ee020d6dc89b89ec6d33b6a00134e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2c0b28c70be266115bbf3efc65bc34e001ddb75aa4e7cb0a9299cf8c4674d7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:11 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Thu, 17 Oct 2024 03:03:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:03:15 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8030fd8404db095ba869a95fa12ee89f1b1426331675235157d03adc33637824`  
		Last Modified: Thu, 17 Oct 2024 03:06:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:64235642e5aba6bffb8e816c4bccfca8c2cd7d90fea0ea4e09d00051e1d61920
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49585201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7287342d10278348c2dfefc82dcb7d91c84699bbf595a0e70f95718ed5d70639`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:49 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 17 Oct 2024 01:11:50 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:11:54 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d83d723f2beaf3193d2d949d5379608be2bc72257349668848f3c9b49f8b6ed`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:d486bb56ea436bc26e19cfb917026d86cb55eba8ba9a5d5225951fde6c0c7345
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50577056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ee78b0de9892376ee72f566555b1798e81315849303cb5d4bb542c918767a4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:42 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Thu, 17 Oct 2024 00:38:45 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:38:49 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51bd45ec812fbe99b0b9ac227201b5bb38e4d4bfdfe6ef5d8e780d62ae9590a`  
		Last Modified: Thu, 17 Oct 2024 00:42:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:8211138d434b5c8426043180b4069128bda405791b77c1dfb5f7a048799b7500
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49561843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a8840a38ba3f21e765ff714dd798a55f692a9ea60cc6be8e1a897947a65639`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:08:45 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Thu, 17 Oct 2024 01:08:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:09:11 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5117c142c650f80511270864bc0dfb90a0c3abf732b3ac8a75823d1b8b0dd2d1`  
		Last Modified: Thu, 17 Oct 2024 01:17:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9742c151a6d367e2cf0cd3fe539dfc2fabfbc22a069046262b176444f8cfae54
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53555822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316493ff061c8119fc805ef0f77a83ef08bed00f4ab664cdb7db8db9c6ca95a9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:38 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Thu, 17 Oct 2024 01:18:40 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:18:47 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced7f13b296b93cbd86a39635414db3dbc1f579bed746b4dc659d626363c8082`  
		Last Modified: Thu, 17 Oct 2024 01:21:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:c701ad885fbac3bf858a2e61e7b196b745dfb8b39a5827ef0f50ec296f987058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47938670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ea732d380758301de6b1270bd89fe2d1c2af4e1d1d79334b2da627d0c3c12b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:45:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Thu, 17 Oct 2024 01:46:00 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:46:09 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1c4de3688a41819bce5afbed8a082abb79ff6e5b892b9026e8fe606aa8420d`  
		Last Modified: Thu, 17 Oct 2024 01:50:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
