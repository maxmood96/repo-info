## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:2166b5db8f7ce138bc02f8d9b4ab81b633fff28739c5a9f766d066d62fa7e3ee
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
$ docker pull debian@sha256:b87474cef0d7460bc0745a4dbd17bd4298572716073ded71bb0e6163672546eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49576615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54747c51e84456d7641d158ed7ec1e048d96487b7d5ea5e0259bd510bc08dae0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:27:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8a4c01e3722f630febbd0069d803d3c08067c3a6a7ea599aedcedd6eb406ef`  
		Last Modified: Tue, 14 May 2024 01:32:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3284e0679aea8eabd9d2893f43b85850e522c5f0f4c496acd7a453d8b0ea4bb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47338520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd89e73aa04c0fdc1389830a7f79e978aa6f479ea4ac1fe14348681872307aed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:48:25 GMT
ADD file:cd62e5a70676cac6ab9314bf7583f7ed4056908c492f302f1243edbd35066bfd in / 
# Tue, 14 May 2024 00:48:26 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:48:29 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ec3129b1f3b893a7412a0ac12044f811ed32ddf7028d374141819005f9d4699f`  
		Last Modified: Tue, 14 May 2024 00:51:10 GMT  
		Size: 47.3 MB (47338294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264450a41877bbedea70813ab302095a5264322d1629abb95190f6294babb5e3`  
		Last Modified: Tue, 14 May 2024 00:51:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7667970cfbe00dc744e878f572b268ad57e3f74c0184fe371070392d68a3d5ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45174972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a4058fdb0a8b1558fcb55e951cc75f5d233f025dcf81d8718744931afced49`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:35 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Tue, 14 May 2024 01:08:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:08:39 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0759e81983b6d7f97a52e5eb4b13c1bcf67d39f9d7084a5c2565919fc65446`  
		Last Modified: Tue, 14 May 2024 01:12:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b5b59a0f5007ec06de92ce65c10ce460f08c0fc77fef040a8115b2bb86ecad18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49613615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc530be4d6c7d918902efb2fc2507f80d76da09e542b7bea51236203b0aec08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:39:36 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6312b17147fecd084ee79563f9d6113c28d5d2e3bf1d212be6fa19407c6807d5`  
		Last Modified: Tue, 14 May 2024 00:42:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:ffbf3d85a680f1ea36ad3ea0eb3fd7ff7ecab86695d419cf9c0555129fd04680
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26c7c31f8fd35432ce55475c0898aad6a41704c5a9e696313d161589f674fa3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:47:00 GMT
ADD file:35709674a3b845511a896af16ea37a6022e7d48992d3198d0760c0c3208fe4ed in / 
# Tue, 14 May 2024 00:47:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:47:05 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4f2f2f6205661e555e772749ae7fd294fb04fc0d06cbc67a50a11fbb4ef44242`  
		Last Modified: Tue, 14 May 2024 00:51:31 GMT  
		Size: 50.6 MB (50602424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d982c2487d56df00d96f1585500e09c6236d6aa5df794e078b2b7537079a8`  
		Last Modified: Tue, 14 May 2024 00:51:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:eb9cdc823cfcde235949ac482c2512274704db6eb1fbab73520e7dea897d4b2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49582565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5dc5f1e0f0c5d22cb0ad83a2e5f4574c295634e2d51b4e8ffc9ed0fcaeaa88`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:10:44 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465f60c82cb4dc8c21f9ec8784beca4482a3c94f6a2a6a8d6afb6e7a293648df`  
		Last Modified: Tue, 14 May 2024 01:21:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:072a2fcc480e839b477a78e98ee45a03e5b71a75f338ad1d699329eb0bdad0ba
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53579972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a4d29347197a58462c25569a84e9e7a8a6f14c9bb2457706036284c1ae68d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b19e789f0b072490b34d4347972912b27d7b97bf4ed00f4967f2cfdbd2f7395`  
		Last Modified: Tue, 14 May 2024 01:23:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:387996ffc7389f8bd2ae82bd334838c98f779fc09796c3b4888806aa7cd5c5eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47942416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3882c7e6c0b738760fabe079a3fa58b3a4ab3783176be3902f3b935b3fed5962`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:42:29 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041184b77f145e320d70b2fb2f463e8244934a6548f06f02daf42e4f36e1cb68`  
		Last Modified: Tue, 14 May 2024 00:47:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
