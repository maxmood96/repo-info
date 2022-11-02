## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:d2decbd2a23d4f1c0a0851b7827c56ac19c623d88114b66072a41186ac8b64b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7d8a828ce727a01ec93816f31d6374277aafad228964555ab9a337c812983faa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37789653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a03272b4c8b35d63d754137af47cc3d661b597efdba12838e167136ffcf6dff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:46:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:46:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a586f3d84de83b25cb9ca6d0e733d37d5283da35a837917e355f58833d27462`  
		Last Modified: Wed, 02 Nov 2022 19:53:55 GMT  
		Size: 3.8 MB (3802823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac951de24f647413f348bfa4183b92c9962b167e0a3106d62300e97e4e88654`  
		Last Modified: Wed, 02 Nov 2022 19:53:55 GMT  
		Size: 3.6 MB (3561223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4f53f690e7e8318d8950f5a699c49130a2ac5633eb529db731cc33fc67c025eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34288196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df316602ddaea375f3bbf5a2671c03b2e0e083109d3c1707e9bc3fcc1e9044b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 17:58:54 GMT
ADD file:3acaa98e676fc52121edd2feea0fc71a60614dbf081f3db61809aab25af42a8c in / 
# Wed, 02 Nov 2022 17:58:54 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:19:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c3a947801223d5dd57236bed8663245ffddcbb4700ba3aec7edc7865fd8cd9d7`  
		Last Modified: Wed, 02 Nov 2022 18:00:26 GMT  
		Size: 27.0 MB (27020159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329f246e8eb0f4d084fb143dd06f4f248b073fee803ece3e73bb6ea2dcba87ef`  
		Last Modified: Wed, 02 Nov 2022 18:31:21 GMT  
		Size: 3.6 MB (3554320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c7170c78501751cb5226283dc973a618a5a7310348cbc5f1113accb24e02df`  
		Last Modified: Wed, 02 Nov 2022 18:31:21 GMT  
		Size: 3.7 MB (3713717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d452df4116286f7d7854c630fbd393211eaf3970dd7e7d6fa818c74fd5a00d07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35692220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cac5c8cc5d7001921c21c50e92a5fc71943ac10ed3f8148c0b4d68af6b2718a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:13:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:13:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d313e8e06ef8938592eca84285a9592b5da4d25cb766e00353478f2a1bd1dd8e`  
		Last Modified: Wed, 02 Nov 2022 20:21:47 GMT  
		Size: 3.8 MB (3774632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22acfa173fc250378a2f68d88a2bac0cfd1a06b5d9a844cf759b6411eb97fa48`  
		Last Modified: Wed, 02 Nov 2022 20:21:47 GMT  
		Size: 3.5 MB (3535434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:18eec1800f42f6f9cee3a3cd90c8f18890973877f8cd59a9fc95454a883fb817
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44218268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624eda47135f0ffa09584dcf7df45feb0917832027f18674ecac5fe96fc3cf07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:38:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0146503248458aa9ed6c98c856b6100417eed1ed7a6d9fbb1ea46336228f84f4`  
		Last Modified: Wed, 02 Nov 2022 18:51:40 GMT  
		Size: 4.3 MB (4276365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908b064950a725ee610984dbbaab21e4f858e343f0a1b568377ab1acdd88e86f`  
		Last Modified: Wed, 02 Nov 2022 18:51:39 GMT  
		Size: 4.2 MB (4234321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5e9a86ec84fd6a2af7edf8691278d781e1eb866030a81ec1b2924fa1bfa08d89
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35122244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b2d204d56e927404d40e910798a480a9230465eca239faf30877592996bb65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:13:02 GMT
ADD file:9ad3cc1ec1bb6343f9cfb63beae7e2c3a2d45964907d8875cf09990c01e744cc in / 
# Wed, 02 Nov 2022 18:13:04 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:579b80989d23b14161aaafa57e58df54a27eb0c04161d628bedf14c8140a6ac7`  
		Last Modified: Wed, 02 Nov 2022 18:28:04 GMT  
		Size: 27.7 MB (27747880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13dcc9e313d05f24642b1675849f9a88c8861d5b6d0305363755f68123b406a`  
		Last Modified: Wed, 02 Nov 2022 20:07:37 GMT  
		Size: 3.6 MB (3595863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb9366a41c8381f62ab5ded3cf45b3c1022cfed53926920dc0e154c3a3a056c`  
		Last Modified: Wed, 02 Nov 2022 20:07:36 GMT  
		Size: 3.8 MB (3778501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4f8200b6181b83c280f66ffc135daacb746ca5732256d8248952a25017c7378e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35923182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c56598138b5048e6631891ad1c6863110c507680ec3a1292418439bd0a22e0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:02:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:02:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb74ecff7620bcf0548d2f31de55b23efccd3fcb9c13978e3188a9d39ea2ad5`  
		Last Modified: Wed, 02 Nov 2022 19:13:47 GMT  
		Size: 3.8 MB (3809969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef39a63b26c2ea7fa435199fe326e706035ee226c72e64159b1c172c2077480c`  
		Last Modified: Wed, 02 Nov 2022 19:13:47 GMT  
		Size: 3.5 MB (3472457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
