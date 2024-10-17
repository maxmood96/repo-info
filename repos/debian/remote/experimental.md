## `debian:experimental`

```console
$ docker pull debian@sha256:7f6e83b657dadfc64edac22101939844642cceb5749d316aae900889df4db195
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:15258696b8fef401644241a42ab606b93e8b85910d83f8d5823828596ed28621
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53272098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322e1de3d0c0c606b0b7f8747db2cd43ad36b6ac297e35274a49daf214a62232`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:22:45 GMT
ADD file:344a17234e227a6dfa7b04784891c1537d678103d91d40841996e0355c691cd7 in / 
# Thu, 17 Oct 2024 00:22:45 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:22:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8158e735f4852d21000cf76f6872a1dc489fc2e307ba70c037a21e8a9b26a9bb`  
		Last Modified: Thu, 17 Oct 2024 00:27:25 GMT  
		Size: 53.3 MB (53271880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efff54737272af3f5af9d53ac46d031426fc2dc97bf383061907271f36468053`  
		Last Modified: Thu, 17 Oct 2024 00:27:44 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:9882549b0774f07d73fd59e753768b33591285258fe531dbf6b0bff63d147646
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50147816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946ae543859ea5651ae6a4567aac099f5b5db3663bf9d303bd9c4f7622019d71`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:56:16 GMT
ADD file:554322c0ec63d40c650e4a8fe2d49f827ed18c023a8362874dc4d169f68d91ae in / 
# Thu, 17 Oct 2024 00:56:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:56:30 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:859c2459faa82042e0d9d83a9a47b8a82df9185d1986dffd244e0b4a254e6169`  
		Last Modified: Thu, 17 Oct 2024 01:00:02 GMT  
		Size: 50.1 MB (50147597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a89af18f0c0edb22dceedb41b430e1bcfa23d0de14454a5e69bd3614f019be8`  
		Last Modified: Thu, 17 Oct 2024 01:00:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:4a9040e58fbcccee1a0e92e07403eb853a97bf6dd9f448a6081f0fd20e8bc926
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47657086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b5020334864bc5e7cd57e484028d93ed3e85897a318438d7a3dbaf830cd8c4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:16:05 GMT
ADD file:ee2f1ffef76f355c1bc3786a4cd225246fb084deb46f8f7a0ebb50e0a39678f9 in / 
# Fri, 27 Sep 2024 05:16:05 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:16:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:622ffd55c3dbb74d17226398ebea86b658a64d0757e987c80a410d1daf7a4e86`  
		Last Modified: Fri, 27 Sep 2024 05:20:33 GMT  
		Size: 47.7 MB (47656866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8cebc5d402e1185423a7b7204f5c06361024d2fa0f715e91d2c98b3cbad64e`  
		Last Modified: Fri, 27 Sep 2024 05:20:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8d61bae67a417195f375b1cf72ebf8b830d9ca83aed18574fa021ab98bb5f453
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53594466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4800ac03f1533bf0ce650216e23d4954937e0e4aa6fb0db0f91b29e6e071cad8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:39:52 GMT
ADD file:e014c06e0ee28a401f9a8a62b2b8a815ba9afafec7c84eb6b0795de0946fb7e9 in / 
# Fri, 27 Sep 2024 04:39:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:40:01 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a5d67d16dc00ba13dab5a84610c9eaab11745150f644c09325e9e8b822fcea80`  
		Last Modified: Fri, 27 Sep 2024 04:44:00 GMT  
		Size: 53.6 MB (53594246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ef1ab33c686b5598c5cf2d9fce64c8d0d6bd9a43d671c0a0350a476b04875b`  
		Last Modified: Fri, 27 Sep 2024 04:44:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:1b18c1c1397ef00d72d84511108a342252f0644a32e92cbafdf7aac6dccfa6dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54118201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4d25dad58fd6edf85fbd4880d60bd5b9652368bfd71218d2dbf697320ea0a8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:41:17 GMT
ADD file:aa65c5e8505403221c9db052fbc81b96cd9afc8ee1534405a8a50005a73b98d3 in / 
# Thu, 17 Oct 2024 00:41:18 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:41:30 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6fef21ff2cdae44e0d2057631ea5ea8ffb7f4f1057257e79ba71fe18c37d566e`  
		Last Modified: Thu, 17 Oct 2024 00:46:29 GMT  
		Size: 54.1 MB (54117984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa68d6988dc64883000bdff187324c6259207c07ea24e014c1749cf9eed74220`  
		Last Modified: Thu, 17 Oct 2024 00:46:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:629d81e5a8278d543632fd4a52b68fd51d6ebdb5dddf344d3afa067a503c8f77
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52125786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e37c43ceb8ee1a9021a8b0bf50806999666ec6c83a1bb97d9d2f611af7a01cc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:08:53 GMT
ADD file:50d986f5c0fae7061384d49b6eda414ee341848cf44d5b4ee3aef7532252bb88 in / 
# Fri, 27 Sep 2024 09:08:58 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 09:09:41 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:aca450ed4f4c217d3cacb085d1c8fe2b8207eeabf45360ac624c96082bec2ac0`  
		Last Modified: Fri, 27 Sep 2024 09:17:08 GMT  
		Size: 52.1 MB (52125566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c749bc4e657a422f4d8ee94b98f5bc4a6011ae4a623488691fc7709ede79f13c`  
		Last Modified: Fri, 27 Sep 2024 09:17:46 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:1ae383f1b02ef017574ee64c521036bb918c6459138407b424229e64b3fbe89c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57123375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878799a1f03ad719b4df114e9511dfdf2b16696ba3537efcc59fa5593ebde099`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:35:01 GMT
ADD file:2eed4107bf1f631a87c3f0ff4c7b82f747d5a594d8c9fe2fa4067f4e2a826e14 in / 
# Fri, 27 Sep 2024 05:35:04 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:35:20 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:256e99e676463da71c3f5fdc7aca05ec4eaffbb4baa444cd2609b955d401b342`  
		Last Modified: Fri, 27 Sep 2024 05:38:57 GMT  
		Size: 57.1 MB (57123152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7da5e6e8ea65b11e231f56c0137399b76cb381f11d510c7dfc94fd6092abcd`  
		Last Modified: Fri, 27 Sep 2024 05:39:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:b855d99eb7b8323f12bb01efded1328dc2121e7afe266dc90b26d16ba22ccee1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51526298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486feb23d11cec3555e1d3c1bcdc27f22af59f94583b7ab4cb833ed39dd75e3a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 12:28:32 GMT
ADD file:b97a5d39da2efa9f082066f841e2e25cafa49d5be3f837d69f5b63ef2d72be03 in / 
# Fri, 27 Sep 2024 12:28:34 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 12:29:12 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ea3e90bd63957c21923051facb9fa7012c2353adbebe393d47fe69fdf94bff77`  
		Last Modified: Fri, 27 Sep 2024 12:34:44 GMT  
		Size: 51.5 MB (51526079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755918cf7f3b9425652d30360d2ff8ce1d1f0394a26d679db766bb67f0654e1`  
		Last Modified: Fri, 27 Sep 2024 12:35:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:7cf547eb9bfe7b1b9ade0f03abd7b25b40cc04864234d89b8f3d8b527c13c05d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52808359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c81412ff602f20c4f08341254546635d424e4adee1f89b42e710e0486d87ee6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:45:56 GMT
ADD file:20427de214380a70658eb94ab60555c5a52f911b8a3754bfd34eae3a7387726c in / 
# Fri, 27 Sep 2024 02:45:58 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 02:46:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:bc3c84d7eec1449ed3e2007e849d064645c2eca9cfc41327102553e89c550f44`  
		Last Modified: Fri, 27 Sep 2024 02:49:16 GMT  
		Size: 52.8 MB (52808139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9712c795678d33d454dbba4df63f8d0417259f8181e963851ef44b36ab63b1f8`  
		Last Modified: Fri, 27 Sep 2024 02:49:31 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
