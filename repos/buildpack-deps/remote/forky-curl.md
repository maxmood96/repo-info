## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:a3ec9e9e18fa044912af95ff9abcd1290045cf1d2149540f7067e572a4b41abd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:forky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:54144638b4d968bb3f443b9102cbf29a938d6238c4d558955525bc4a2fe30724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75675833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586f446ca20f617dc1e56fc09c98e7e764791703f3cd8cbabec9cf4b32064b51`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:186ca733686ffcaca03fdc512b51c9498f39b93235775cf08154b1ff0b143901`  
		Last Modified: Tue, 04 Nov 2025 00:12:56 GMT  
		Size: 48.5 MB (48481364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a5d3d8f7f036c72a68099d4e5f2152d5ebac52f060fec3d2009131f12e2ee6`  
		Last Modified: Tue, 04 Nov 2025 00:28:30 GMT  
		Size: 27.2 MB (27194469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9ee07e6f859494b6abde305ad7423e76a112c7901994e7145c053c4cdecaa8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4105084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17f036fc51f4afb86310eeaf1eb4bc76c0e347036a48e9d0a83dfc1e195ac24`

```dockerfile
```

-	Layers:
	-	`sha256:88c9080b904016abe340bcb22c8b21647dd9da4d2164dbf53e8c191fb13d0df8`  
		Last Modified: Tue, 04 Nov 2025 11:21:26 GMT  
		Size: 4.1 MB (4098311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e97be3320a85207dac4cc7d7e67c6d2297ac6e32a49a538be2bda84e6aae871e`  
		Last Modified: Tue, 04 Nov 2025 11:21:27 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:36eb1a2de050d60edfced6b4dc697edf380b3f50b8f983a0874324d587e6638a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69915659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20513b649eb4fd4d11ea5d56dbb516e367da5dc531b9457fd4343d2d20b4aef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a3f9ca9ddd6f8d1ee0ddc59ad7ed9255992d14a1e28dcd6f3a00557f6d1c188`  
		Last Modified: Tue, 04 Nov 2025 00:12:42 GMT  
		Size: 45.0 MB (44987650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e3d8e8af8f367c36a3d87550dc3267b3259f0235ff915d84427b289652d3b6`  
		Last Modified: Tue, 04 Nov 2025 00:40:06 GMT  
		Size: 24.9 MB (24928009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fdd89681e990d0d55163a95a33190bc9ed17298feb479af8b3ac97e23d9e3cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc5150f4f1ac95ddc61cde4fcac37bde898ee456fe361bad793dc32c7d58e89`

```dockerfile
```

-	Layers:
	-	`sha256:2c7bd5877d2dfec37e7ab9b8dada2e2916c57f2fc7fdee421d87146c76796080`  
		Last Modified: Tue, 04 Nov 2025 11:21:31 GMT  
		Size: 4.1 MB (4099807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d34341aa42e5109300c12e8cc48222cf220e08b5836c39a685b95ba87e03aa11`  
		Last Modified: Tue, 04 Nov 2025 11:21:32 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c6b61521a941b9d44ffc04bc128afc3a5b1e8894d2a4e68462f755e3e3d96b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75042688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d897c19f8febbd920bd18f5750937c32cc5c8645965ce2600c621ab014b469`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:29:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:52d2706ca00f3431b3c37b306b3eb6cc4989781e31180bfdf93c4dd4108e1e3c`  
		Last Modified: Tue, 04 Nov 2025 00:13:40 GMT  
		Size: 48.6 MB (48583638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1dc65111912cace804df53935fa607cbdf8cea0c2d3c79b97f575ff17a44e`  
		Last Modified: Tue, 04 Nov 2025 01:29:59 GMT  
		Size: 26.5 MB (26459050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:331d99fefe9d771a52db5d1b9885bf0fa3a3280639ae0c7e183916e2c6e1a9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19980b7c4fbb1d8fcdf4162bc0a9692f9ce0742a83b43c1c4c2440927c5d1ee`

```dockerfile
```

-	Layers:
	-	`sha256:1666c89b6c557b77f16b34a2ea791c813d48a5afad15c95f8f48aa1baa9d65d0`  
		Last Modified: Tue, 04 Nov 2025 11:21:36 GMT  
		Size: 4.1 MB (4099204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6256eb74575cc01c0ec8e254a283feda39a829aabd8a13c82b13332b6de7660c`  
		Last Modified: Tue, 04 Nov 2025 11:21:37 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7fd03c183e40b4c7e1d5bcf82444b4fe325a779107b49945816a5c5846a8577f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78242212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc51f0ce27beacd27eb554081ac9d67fd211670cecec27049938c8bba555d1a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:31:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd86ecb6d3ac97cad4df6e0aeedefdf1790afb18f99112bd09ea68844e318978`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 49.8 MB (49809500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56f22c9a3cedb803ef4ecfe9678d058c62ff4867aa23b90c8aad3b86d75d98e`  
		Last Modified: Tue, 04 Nov 2025 01:31:56 GMT  
		Size: 28.4 MB (28432712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85adeb3d270ec3bd8d51a5892bbef0c79268a163799dc3f83fbb520b594ea330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b0da3c3ca5958db4395e688b1ebbfc3e8e32533c3f6cafa4589704ca74329b`

```dockerfile
```

-	Layers:
	-	`sha256:c529a1d11881c71efe92f53dfd6562cf75767d99fdb5c44c05607aa90227e752`  
		Last Modified: Tue, 04 Nov 2025 11:21:41 GMT  
		Size: 4.1 MB (4095430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fbdd28baf29a1916833b05a27313f97b41d31ff458cd8709a7be816764c2124`  
		Last Modified: Tue, 04 Nov 2025 11:21:42 GMT  
		Size: 6.8 KB (6750 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cbf949821e731c813f8bc8ae85811fe99f1bc7f6d7a0e1063797d9f3dedbf97e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82113616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807bf6ab5043807f97ccbe53cf2fe2650736ea154e97bd353858dd0bc99bb506`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 06:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9422d47ff8508a211c5181db20a5b72bab47758f9bcd0687b05752ead1b35a5a`  
		Last Modified: Tue, 04 Nov 2025 00:14:32 GMT  
		Size: 53.3 MB (53315240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aed674c331384a39236b4b411559b275037202a43d78e434b1d5c25b1e6d72`  
		Last Modified: Tue, 04 Nov 2025 06:26:53 GMT  
		Size: 28.8 MB (28798376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ad08b61ff416410a9fb4cd5e96b8381245cf53969171833704caf14736975d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bea5b276cac62e39382bdc193166cc22f2ece72df87509bb722c9763e45ee72`

```dockerfile
```

-	Layers:
	-	`sha256:e930d45be413860229058e733278d8cdc2af65b2b8cd2effab256f4f4d369567`  
		Last Modified: Tue, 04 Nov 2025 08:21:23 GMT  
		Size: 4.1 MB (4102144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcbe52b3945b27eaacae78ee63ab431b37f5001439075376f95312dfcf3f958`  
		Last Modified: Tue, 04 Nov 2025 08:21:25 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d480fcb1575053f3a5cf53b23a8d63eab46b3ef0e3a6c1ab0ff58ab52bc3612a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73178808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c332f7af4f5202dea8607c4e8e42fe02bcf40c8bf43e0b4c20b88bba1f460021`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1762202650'
# Wed, 05 Nov 2025 11:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:81afe9ed9d72ebbd06999820f64e36aa62bc978725062b4cc32efc39c6a99213`  
		Last Modified: Tue, 04 Nov 2025 00:13:41 GMT  
		Size: 46.8 MB (46791125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de80c58c6e8800ea08ee90fdc845007e21de17aea53e05a410b042fb2c91d58`  
		Last Modified: Wed, 05 Nov 2025 11:57:49 GMT  
		Size: 26.4 MB (26387683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db799b3e39dd67e84a205a60d008ba363f68e0a7b0329e26b0ca5e14c362eae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4097599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de28e8cfbfab3209e05b61d3c8ed5f18449c082af137070b93da8a2a95e12331`

```dockerfile
```

-	Layers:
	-	`sha256:894f6991a47d370443ea819ea5c8ddacfee745d6b4f2b75de66b4931017131a2`  
		Last Modified: Wed, 05 Nov 2025 14:28:23 GMT  
		Size: 4.1 MB (4090794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01db41eb62d6112049c14a994577218631abdb8c741c4b93ec9e369e0844e88a`  
		Last Modified: Wed, 05 Nov 2025 14:28:21 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:08db80185f67989e298c8d984b75489b8042c10a9dd37e15342ccbb498b783c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76662791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4e5962a3d5891729435c6ab1ac7f14f836e9d1b539585b154ae657bf10a3c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 10:00:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aa89048d1c3c931b297cf2d408ea7138528530c43e452af625223e71f97282b3`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 48.3 MB (48343062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd290c851a8e221175041f9832e015aa1560214f438629f7d489ba726030d3`  
		Last Modified: Tue, 04 Nov 2025 10:01:24 GMT  
		Size: 28.3 MB (28319729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:92341ca4516557d0c062abbea24ab7feb9028cb08083ddfbfe7928211ecaea1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd364556de0143d3b1140ddb6ee2d69e4fddefc1366fb4aeb88e86224e56103`

```dockerfile
```

-	Layers:
	-	`sha256:e59260715e496668dd2a49ff5cdd8032329caac3077c360b743577deb601d850`  
		Last Modified: Tue, 04 Nov 2025 11:21:53 GMT  
		Size: 4.1 MB (4099720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a9dc0d82f1030d3a38cc70978729e8dcca82a146d2e93e8f3d1ffc3187e976`  
		Last Modified: Tue, 04 Nov 2025 11:21:53 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
