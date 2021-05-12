## `debian:rc-buggy`

```console
$ docker pull debian@sha256:8316ad8aec2efde78dace28013cf004b972163d605a55454a3d87bc2dbd1df27
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:cafa8352aa300ea0912abc03dd115fd9b1c4af2913c4818a4090477c557308ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54896919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a795ec67f174055462959ec9bda1a5ca41792b24ed722b0174952d19473e6c46`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:22:07 GMT
ADD file:b00402c4b2c5828b18b251f8a057510f9f7da733f833cd147ed1a8fcb8d574db in / 
# Wed, 12 May 2021 01:22:08 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:24:35 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d2746b657344bbd3149c23794266413a61b32b44f53688f3619e485894c87b09`  
		Last Modified: Wed, 12 May 2021 01:28:33 GMT  
		Size: 54.9 MB (54896691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5b32552f844be01b0ea5aa2b368b04d95d295959e138c3985d987b469681ab`  
		Last Modified: Wed, 12 May 2021 01:32:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:5371348a941c2002cf5e0ffb30aec478fd2ffa415fa28061ae4ad1311de18509
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52438991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b384ffd71c12ba04b375d84b718b368320d14b9639800b1a3e0119f543079fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:57:58 GMT
ADD file:74d49eb3680e0d1e7268c77ac09aadc6a9eaca2541a1941d02c05771fce80430 in / 
# Wed, 12 May 2021 00:58:17 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:07:26 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:992a8499bbce77a1397237914a5f442e2a2d90912c4dcf8d75ced68fa669452a`  
		Last Modified: Wed, 12 May 2021 01:11:33 GMT  
		Size: 52.4 MB (52438763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11792444b9200dbcb47ffd9c518bc57208f5d27cce47e16af40a770e74d772fa`  
		Last Modified: Wed, 12 May 2021 01:14:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:9a165c38c95eaaffd4ccfcfbb7ccb9981c1f659e56f19314aa334b4d6bd2aab1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50098494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2653e1831f6c7f9526655cf26d4905a3ac58665e7d05cf8c4eba9e1fcae76d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:08:03 GMT
ADD file:45a139d5ba2871d3a6f990263a8fdb68998d0e072f5c70f796581383ed107962 in / 
# Wed, 12 May 2021 01:08:13 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:17:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:187ecf03b42c9078bbaf7c041564e40178e23f795d23634e11536955cfc64143`  
		Last Modified: Wed, 12 May 2021 01:20:07 GMT  
		Size: 50.1 MB (50098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98766449435d3f8dc21666fbb127c0cf2d0084825e27545ff867164586354e6a`  
		Last Modified: Wed, 12 May 2021 01:23:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cb297214b484967ad6ae714cb14153e4ad53e7861e6f4f094aeb1bbff9392689
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53579953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b943b1146da9d1060f8416f02548281ff9f646f5faa58efc7f362e483fc1bb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:54:16 GMT
ADD file:bffb08485a063deee6d89343a52bf604c1b25c42687e69b289d304c56a35e425 in / 
# Wed, 12 May 2021 00:54:20 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:59:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:187d6bdc2d3198067fb9a19db77a105ae346c5a0de7d9892597e87e77c9d4b2b`  
		Last Modified: Wed, 12 May 2021 01:03:04 GMT  
		Size: 53.6 MB (53579726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025045d7e0c95d12f3d4b42a2f0b5b4e212928f2066c82c4cfbfd758db737a16`  
		Last Modified: Wed, 12 May 2021 01:06:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:ed353d55f5d7dcad84b7d773495a55288e681ec7b5aac8c9481b8d4b62cb8435
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55915395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e274a845de996e6a857d7d1ee63360eeb10b76653ca3b42bbf993923278a532b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:40:40 GMT
ADD file:d1e0da16153884c1e8fed94b01ed7a0d6215598889cf4b3ecda3e4e8e01a8a73 in / 
# Wed, 12 May 2021 00:40:41 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:43:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d1831ab5654d838d70f399ab69140b583b6195b99074487f0f45c8b5e2391a70`  
		Last Modified: Wed, 12 May 2021 00:47:50 GMT  
		Size: 55.9 MB (55915170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b1b954c3cb7eb4763d89c3de1043237e8945e57f29220123d6aef0021e99bf`  
		Last Modified: Wed, 12 May 2021 00:51:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:01071b41bf2ff8c8c5b21559846d98e1b2acfaa054330b70be768d2c32b4e548
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53156024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fadaf5428772f6d95cc369a78b1b66c893764274f4b97e28b3f788cb5671efa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:10:15 GMT
ADD file:dca45bb65ee8f7144352f7ac752f805807e971fc676ede954cc095be23566bf7 in / 
# Wed, 12 May 2021 01:10:16 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:13:32 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:02e79e4ee7225612ac3aad55b918cb4257f8e4ea2821e093d61ce58205474706`  
		Last Modified: Wed, 12 May 2021 01:17:23 GMT  
		Size: 53.2 MB (53155797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5aee08f52b095e218ebf271dbf8babba3d3a3e4965674f5eed2e82ac6a848c`  
		Last Modified: Wed, 12 May 2021 01:22:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:05148ccd9bcba3f208e6d4afc4c794b74d9c64e6eee11cd7aac3911f15ad7c9c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58799073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de3f3220115dea34edfcb46cb08215279d42c069c2628075ff95cfea16367d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:35:19 GMT
ADD file:7d2dad47f7990dd0f8ed0b034505aa9c7d8afbd94956f80bb57feccf6f7e15fc in / 
# Wed, 12 May 2021 01:35:33 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:39:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ec00b4432728c9f962251efa3d91b6e0339e74ff656fbaad7adad52ce998ea8c`  
		Last Modified: Wed, 12 May 2021 01:45:35 GMT  
		Size: 58.8 MB (58798847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4d410a2cde59ecd9adacc88595415555fa106f3481f55860a57e8c93f339b8`  
		Last Modified: Wed, 12 May 2021 01:52:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:1c20e72148f521240ed2a44a5c877ccf7b7a8bea0d2dd9d8580c72f453fcb849
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53183876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6605aff67ed9cc79fe220306a3b580b44c5037573c17d6387b626b545e8804`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:43:58 GMT
ADD file:22b27fbf0808244bac39e39b8239caa784e78a6b5682c7978c1cb4fac0813a67 in / 
# Wed, 12 May 2021 00:44:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:46:29 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:55e7e62594640e8831f8e39a7fe34cbb94c1ebfb345106b49c32b7d6c7e81eae`  
		Last Modified: Wed, 12 May 2021 00:48:17 GMT  
		Size: 53.2 MB (53183650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e56c377f632ecbe523fa353cef831d0a27535f4d60d854bb1adfa8caf169f11`  
		Last Modified: Wed, 12 May 2021 00:50:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
