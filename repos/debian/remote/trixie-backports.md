## `debian:trixie-backports`

```console
$ docker pull debian@sha256:ad439b439009690813cc19ffc76468e7d08c0b5905ea79bd5f947838ca825d63
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:2585fb92d6c1825634649ec3d16ec8b4e6940fef5be31fff4151884d95e7b9ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52841411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd3c1e54e3b224ed2e91b476ce58e37fb879a85456a1c4cf252f7fbb002f815`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:11 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
# Tue, 13 Aug 2024 00:22:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:22:14 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f7ce7cfb7bcbdd2df9894d003b40548146e9ff4feeb04468fab999b96ee6ff`  
		Last Modified: Tue, 13 Aug 2024 00:26:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:817b745219f09d0cd7ce138a74031fbe274a4cd205006aba55dd0bc3b613fb51
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49871836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb3f31520895dd4f0ecabe4b11fb5366c39bfe6977a699f24ededc71d27f065`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:57 GMT
ADD file:368997aa7bc3d0c868f5058460057cbd845e2ba7a356c40f3a1573421e53e41d in / 
# Tue, 13 Aug 2024 00:56:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:57:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:12ffeaa53d9595553187a53d5abdc0f1c023c82e8a57f8058812fe9bc5e86aef`  
		Last Modified: Tue, 13 Aug 2024 01:01:44 GMT  
		Size: 49.9 MB (49871614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4215c06f07c609b90cfd348ddf468e15429601a205cfde34250e16f9e82c517c`  
		Last Modified: Tue, 13 Aug 2024 01:01:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b3a42b98ff1a425400cf219cd6159f7d097ffe2b344415231a3f9446200c8789
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47364351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffe14dfc9c97e98c698282a842cb4d8c0a7a409798a3bd998294f9f0c96be90`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:59:15 GMT
ADD file:99761e9b65792d17a2f1d115ea8ad35dbc2936acb0f636cbbbcf63ed20bf10c8 in / 
# Tue, 13 Aug 2024 00:59:16 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:59:20 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8bfff960de1d4efc80e46f547c59070161e89055685b260aa43880326ecea728`  
		Last Modified: Tue, 13 Aug 2024 01:03:57 GMT  
		Size: 47.4 MB (47364130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b690a77663848c2cda2c1691967b718573653a2dac327e4e43055a6247e1cfde`  
		Last Modified: Tue, 13 Aug 2024 01:04:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:dcced04e64402c9ade9ac784ae63b0f45e22f716ec426c6e4b8c288651c1a956
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53152665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3659ac6f4c4cc57bc59c20bb9e033c47c7bd01998cabc6f46aedda3f5c329617`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:41:11 GMT
ADD file:44df8bf38e0a6481ddb1093ad0c25ca4508a15c2b5d1c0733757db62627a7413 in / 
# Tue, 13 Aug 2024 00:41:12 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:41:15 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8858b14d914bd710ce161898770a04753f6d66b911364becd105945179fc07fa`  
		Last Modified: Tue, 13 Aug 2024 00:45:37 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd3f7359b97f99b7fc1908696ca6577a27f5a016dd44b04b31208bb4318c916`  
		Last Modified: Tue, 13 Aug 2024 00:45:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:e750a3c1af77f23d16c5bb50f474d100fa1cab9f478a6691937dc77f2238db63
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53777720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5c34ec25aed0946b773e185f06421c1f66a5933eff467abeb82a0cb14f722c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:40:59 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3993e22b22ca7e1392db9f7bb2e762ee383e0892938582f048e1b719fea488e8`  
		Last Modified: Tue, 13 Aug 2024 00:46:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:5c3759249a00549d3e82002b3ffefaa84fd3487704bc2a32bfb6e9d1ef42e56f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51717838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adee9796c280ce9192a9f383048abc06216f14709f8202e11d40eb6cf2756d97`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:18:15 GMT
ADD file:bcae38f0c6409385ec90f5e766061248a9443b81bfb083c2bb38b2fee95e3241 in / 
# Tue, 13 Aug 2024 00:18:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:18:34 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:75b1f153ec57b50eabb508ba15b89fcf272ebf8f1075f5358064b7d13318179d`  
		Last Modified: Tue, 13 Aug 2024 00:29:38 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9166ee5597f8c7a43937435086ff18bc97fc4792e4bd9a73180b1da9ab3144a9`  
		Last Modified: Tue, 13 Aug 2024 00:29:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ae651aa2ca3da22865d65f2946a9f852ba3afe31502afa03e058c155dac0ea6e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56775807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57372c7acf140b94a864591816c91852382b30c37b2d5006d8ce4db3bdd76932`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:24:25 GMT
ADD file:2ecbeb97ee4f1fa94ffb8d689b43061a3e219246a7cdcde111969dcdcac0aa81 in / 
# Tue, 13 Aug 2024 00:24:29 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:24:33 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7a059b294be9a535ead3acf658974bcf9ec161d20023a04804c129791e3dccbc`  
		Last Modified: Tue, 13 Aug 2024 00:30:11 GMT  
		Size: 56.8 MB (56775584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dcde752200e9308277b77f581c6f681f0b69f3395ed38f7acdb599a466c516`  
		Last Modified: Tue, 13 Aug 2024 00:30:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:a812c3bcae61f3700d231d79a0679b69c16962ece3df7dd03a8fb1e0d3d93f1b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51127453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfc1bb2a312815637f12f02afb703303293e014a146b690c7e09dbe8bd949d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:13:20 GMT
ADD file:83cbcb6055e53dd5bbbdb284d5c1129bd8ef0b02c2f174e4bad8a86a9a470700 in / 
# Tue, 13 Aug 2024 00:13:22 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:13:31 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:664f4e8f311a644728086c0fb1ccd2a113bc5c8af1174d6b42e68ae243e81646`  
		Last Modified: Tue, 13 Aug 2024 00:18:53 GMT  
		Size: 51.1 MB (51127228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758427a149e223d282ca6a4fc1598c1b14113db8e71e801e1bd2642cbf03596a`  
		Last Modified: Tue, 13 Aug 2024 00:19:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:f54637d4a583577d90d1cfca1b075df3500c53c06953ca1a969b2789262bdd25
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52481137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f21903e455f0d45b5cb2c561f818c794cff09ba7e884e7d2fb5ef298f0ee9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:45:25 GMT
ADD file:44d3a49280c3105abcfd85839c96a9ede97d8553a9bf4a53c274041f1929ef4b in / 
# Tue, 13 Aug 2024 00:45:28 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:45:35 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3b50b414b30fa7e2898d8a041d2ca183b6d95dae25e656b8d6bec87a2fd533b9`  
		Last Modified: Tue, 13 Aug 2024 00:49:42 GMT  
		Size: 52.5 MB (52480914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b798c453716dd6694094a9ba725c40d743fcd6992554b0bce2b9d727a9a3c6`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
