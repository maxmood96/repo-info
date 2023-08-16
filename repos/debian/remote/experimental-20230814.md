## `debian:experimental-20230814`

```console
$ docker pull debian@sha256:d4c1f430098a83ae9fbc355fb346bb3d798bb157b0498ec2660f01f14506a5e0
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

### `debian:experimental-20230814` - linux; amd64

```console
$ docker pull debian@sha256:56a5bdbaf8f475cbbbbefd96a5d818a5b546fb90b1d0a0d38b6135ff8eae1d06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49617559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0991746a03b1dfec162dd2939f6b3dae7bfba0c2416041ed80a66af17628afc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:02:54 GMT
ADD file:2a9cd6e99efb8a8424a19910ae355021abc8cddb18d85aaebbec132e1e554362 in / 
# Wed, 16 Aug 2023 01:02:55 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:03:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:1c76186e3ccc03a09c11e88d15883be9bc1c452b1a23af4e44260529dc1446e9`  
		Last Modified: Wed, 16 Aug 2023 01:09:32 GMT  
		Size: 49.6 MB (49617337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86cfeaf5dec1110cbdcff697ce3d2aa1d51cbb3e01d05c81a1985dacf32c64c`  
		Last Modified: Wed, 16 Aug 2023 01:09:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230814` - linux; arm variant v5

```console
$ docker pull debian@sha256:4b86cd45276b7f680bfad3f10a48f04ccff85951f78d71f7f7e795f10f1a9464
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47403994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ea2124f07b0bfb1f3006bfa559783e4410d5f93424331d8baf52d4b00806be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:50:12 GMT
ADD file:504bc03aed9d9b0c8d2abc5a3834187d2b4669e797f8779fcb28c91b70c56e92 in / 
# Tue, 15 Aug 2023 23:50:12 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:50:21 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ec4881df730a345ca8a4371baefd100cdc8229f27e78da7c4ebde074f0ae7a83`  
		Last Modified: Tue, 15 Aug 2023 23:55:17 GMT  
		Size: 47.4 MB (47403773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffedd9ca682ec5a721b6ea8d5076c60d3c02db8ce1cf1ec74929647c74c4bef3`  
		Last Modified: Tue, 15 Aug 2023 23:55:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230814` - linux; arm variant v7

```console
$ docker pull debian@sha256:5841c1545ce368db3a3dfb3cfd91e6ce583e2df6f57592a9c84eb3b4ebf90b2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45189484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1feaea6671415189e476314002a1cee15373d4afad5487821a9e7e040a71d5e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:19:56 GMT
ADD file:2b0c2128483bcff89cb8df905ad8e6474533a53ab65c41c95600e28bfcf81859 in / 
# Wed, 16 Aug 2023 00:19:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:20:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3ac3386c51ab2c9a1d8d628700e94eac2f682ab88e69566519f8df87a4ed8fcf`  
		Last Modified: Wed, 16 Aug 2023 00:26:13 GMT  
		Size: 45.2 MB (45189263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0efb679a0cc4b78844e4026276a05bacb66e33a86e24c9242ee78ff58cd241a`  
		Last Modified: Wed, 16 Aug 2023 00:26:34 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230814` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1303edae21b9ad23f308e7795cb17d9ab4924060b1420fa3aa442af814f2ef0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49531960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a561d5c6ee9d74e4d7e1fe4deee52605455bf1c541ac929e88a01a2ada677a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:57 GMT
ADD file:f7f66cacaa5bf03b093937f209a11e37f2d008bb08e132abdd2ee434a578dd33 in / 
# Tue, 15 Aug 2023 23:41:57 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:42:05 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7a7dc3ef489f656442578506e2ae36abe517286a1fb563b0f395042f47afdc43`  
		Last Modified: Tue, 15 Aug 2023 23:47:53 GMT  
		Size: 49.5 MB (49531739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0de22491d610db7ad434a0f7d3937f54f1e7065dbe4c7284f213e977b82cb8`  
		Last Modified: Tue, 15 Aug 2023 23:48:14 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230814` - linux; 386

```console
$ docker pull debian@sha256:013d8bce5c98907828a15aa8745ba916ec651f9794e8e0b08ece65ffe22b32e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50631557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d03024900047ff3414eabdeac88f04d786197f2a4b051e9b43f7fad79df5b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:52 GMT
ADD file:556295a396a49a6963ffdd0990c3d7ca7d2ff46f34a5de3b44a5e6db7beb29bf in / 
# Tue, 15 Aug 2023 23:41:53 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:42:03 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:efa40d40112205d1598dfd6ad6871586d4a5d9da03b720f86738b9cb4e3a0a4d`  
		Last Modified: Tue, 15 Aug 2023 23:49:00 GMT  
		Size: 50.6 MB (50631335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb15762113d7b642f458ddb8ae4b02bf0b4882df3f22f09a9c5eeaa0876be33`  
		Last Modified: Tue, 15 Aug 2023 23:49:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230814` - linux; mips64le

```console
$ docker pull debian@sha256:2bce1025f0f0496b4acedd98f850b522a650178cff438432a8c55c4dd6b9f308
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51cd9fd26e204f3ec9455cb7a503310f8c306015a99b87fd2359fd3b70be571`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:16:34 GMT
ADD file:23ec557c764d13f28545716ee3db40d3d44cb9af7c5de318d9418cec8f4661f5 in / 
# Wed, 16 Aug 2023 00:16:39 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:17:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:367c0e3894f4450b8c06a33a8accfcd15233ecc26e4bd9b1fa47d546eb90361d`  
		Last Modified: Wed, 16 Aug 2023 00:27:44 GMT  
		Size: 49.5 MB (49467668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ad64b643a326a72a66d24f05c69e40d8628fb63c1e3dc7e2f492292d9cd203`  
		Last Modified: Wed, 16 Aug 2023 00:28:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230814` - linux; ppc64le

```console
$ docker pull debian@sha256:7abd75b698e2ff75039db9d809605b52f428a11aa7a8ce43b8546d45a3089195
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53552090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157814a9106144319e50faff106015b447cd0410adf2e6f2f2ca88df61a2eff6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:13:31 GMT
ADD file:3c32612a2b966cd43a145cd3341dca379530f577b69f55e0cd0c09af1d3e2b3c in / 
# Wed, 16 Aug 2023 01:13:34 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:13:53 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a72331f708c06ca3176102f16b6aaed6580ae729555666bda786391bf7d43653`  
		Last Modified: Wed, 16 Aug 2023 01:21:52 GMT  
		Size: 53.6 MB (53551868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11260f6b50d0f560bf28c9f0d963885ee21cf47e219c32cfa51b82796264f4c4`  
		Last Modified: Wed, 16 Aug 2023 01:22:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230814` - linux; riscv64

```console
$ docker pull debian@sha256:5b0a5d2183530e241df2ef2d645bcad62f09936f4d2dea53752ceedc063fd5fe
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47907159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792f0d4ec80d3139583899e4cb97d601fd03b91533c5119c0858cc38535000b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:10:03 GMT
ADD file:0070178f3ec169f9e94a148e0e227924d3aaa6089bb9ce42033467eda02e2a4e in / 
# Wed, 16 Aug 2023 00:10:05 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:10:39 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6b6b58c880fe974b06db209f5366fefb6587eaee896a569cf4cc2b08bf9faef2`  
		Last Modified: Wed, 16 Aug 2023 00:13:11 GMT  
		Size: 47.9 MB (47906934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3aba780c209b39ea96b91d9ce14e35eff184b6667e26bc1a6adce7572e8422`  
		Last Modified: Wed, 16 Aug 2023 00:13:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20230814` - linux; s390x

```console
$ docker pull debian@sha256:acca5ec87a64d7629a9ed3efee010f2563fabb09e2a784a0b2616d3bfb8cd16e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48594634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6740d62f13a5459cb9aab108440af8d5c18099a18df4c34c93af77b6a253f4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:46:07 GMT
ADD file:4799bf241f52a34ad10d08811435683abe035fde25579c0d9f7dad45c87d36c5 in / 
# Tue, 15 Aug 2023 23:46:12 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:46:29 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e7cc139f643fe5614801ad4b3885730876a26d565c8f8df9c0f5d4a3a5b5b39d`  
		Last Modified: Tue, 15 Aug 2023 23:50:40 GMT  
		Size: 48.6 MB (48594413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9629d350dd0beffbd0d5cb4fa018a45e7669630a57bc654c0cb0ce06fbaa0ff0`  
		Last Modified: Tue, 15 Aug 2023 23:50:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
