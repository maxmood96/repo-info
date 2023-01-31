## `buildpack-deps:lunar-curl`

```console
$ docker pull buildpack-deps@sha256:8b449e48a0f659e92f474fc6bace2c8174f4449194bef4b9549c24a7ca26d6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:lunar-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0cb54895d0edc925d32858e904c44ea1a439970bf15742c03d34df1a9e214719
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37703238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c217d1c58e594b732dd8af1f45e215c169aa14f6d2e00e117373ba1d60a8840`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jan 2023 14:47:05 GMT
ARG RELEASE
# Wed, 25 Jan 2023 14:47:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 25 Jan 2023 14:47:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 25 Jan 2023 14:47:05 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 25 Jan 2023 14:47:07 GMT
ADD file:5a9904395b52775ee7c10a49efc741d32b587e2cd447b8deb66811c3fb3b37a4 in / 
# Wed, 25 Jan 2023 14:47:07 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:56:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:56:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:538756765743bd18143e090b14dcdccf38e7b5a5b0c6c120c45ca6adf9bb5940`  
		Last Modified: Tue, 31 Jan 2023 00:04:01 GMT  
		Size: 27.4 MB (27378222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd833ab4892c4d028b18ca553e758acb20a73c46e21456f3a20ef3254e01c3`  
		Last Modified: Tue, 31 Jan 2023 18:04:36 GMT  
		Size: 6.6 MB (6634866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727a0b8a10350ace4289f7f5e67c83669729989985586d1002c6088e18a823e`  
		Last Modified: Tue, 31 Jan 2023 18:04:36 GMT  
		Size: 3.7 MB (3690150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9fa2581ab75a395616d5cd495d2c906d22fd5cf19fac7e3ffc02bda7606656ec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35579633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce96af203a23ac00a8d7b294393b911222db929d0e1bd88ba4bfb40580316be9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jan 2023 14:38:25 GMT
ARG RELEASE
# Wed, 25 Jan 2023 14:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 25 Jan 2023 14:38:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 25 Jan 2023 14:38:26 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 25 Jan 2023 14:38:35 GMT
ADD file:c01025be735c65553980246358cbe7c563769d7ffc886d18be817582a0d29b5c in / 
# Wed, 25 Jan 2023 14:38:36 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:07:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:71f87b47f8b635d25197bdfbf54515fa4ac6c36f9a35642d84d3c0b31fd0344e`  
		Last Modified: Tue, 31 Jan 2023 18:18:47 GMT  
		Size: 25.9 MB (25921790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee28ebe3784a255cc3e6775ce6f89b8846b8982aeed7c3e5f84fc71f50d542c7`  
		Last Modified: Tue, 31 Jan 2023 18:18:44 GMT  
		Size: 5.8 MB (5806473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708c008decd03d5ead737257e49ac93799beaceb7dc6e5c0b3123918c0f8221e`  
		Last Modified: Tue, 31 Jan 2023 18:18:43 GMT  
		Size: 3.9 MB (3851370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5da8c91a69c9ed4f2df69b0b0b8f16234ffe240dba7021d7dd0d8fd5f123a484
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36843692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff1a073cf3267cf342e36a6b3b05141b2165c287b48e5da82b91559bb9b411d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jan 2023 14:42:22 GMT
ARG RELEASE
# Wed, 25 Jan 2023 14:42:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 25 Jan 2023 14:42:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 25 Jan 2023 14:42:23 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 25 Jan 2023 14:42:31 GMT
ADD file:6713306ff9bcc18c79430d43aafbbe519176e76b7232c563993ebda6c8caf738 in / 
# Wed, 25 Jan 2023 14:42:32 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:28:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:048f92e449ba1ae941d3c632e2265209df67f8160670f7a6435172704f94ae02`  
		Last Modified: Tue, 31 Jan 2023 18:36:32 GMT  
		Size: 26.7 MB (26724812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883e487aa72ee290950def79721f6dcaa23f86e25b8e337c6ec4a3354e13cb41`  
		Last Modified: Tue, 31 Jan 2023 18:36:29 GMT  
		Size: 6.5 MB (6469058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b34ce0f93baf1d541b41cedfb282a8c632b47a2e301480af6364419606311f`  
		Last Modified: Tue, 31 Jan 2023 18:36:29 GMT  
		Size: 3.6 MB (3649822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:510da3c57d42f51519cd1b6cf352a8f4726dc51fd8a4dc619cd7a9ee02b4c773
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43960944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0413894f5b6b97128c7c5a3f9d046c9063c5f2a60d147597b6402a6d284610fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jan 2023 14:48:03 GMT
ARG RELEASE
# Wed, 25 Jan 2023 14:48:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 25 Jan 2023 14:48:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 25 Jan 2023 14:48:04 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 25 Jan 2023 14:48:07 GMT
ADD file:5002466754dcd29080099171ab20675c9bcc55f0befbe928008127d14c027297 in / 
# Wed, 25 Jan 2023 14:48:07 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:05:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f1cf3bfdd097ddcb6ab4d5644d9dc62216fd38716af0e31a6b458a7b40a85afa`  
		Last Modified: Tue, 31 Jan 2023 18:19:51 GMT  
		Size: 31.9 MB (31946855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23d3ffbdb8d698537e125a57e30e32a5dcddebe76a194b0bdea9def30e2729f`  
		Last Modified: Tue, 31 Jan 2023 18:19:46 GMT  
		Size: 7.6 MB (7605256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd335e4704b6e26586fbc557b7ecca9442aeed0ed883ab9a6d60009a6bd8f843`  
		Last Modified: Tue, 31 Jan 2023 18:19:45 GMT  
		Size: 4.4 MB (4408833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:938de68415e6cc78e92fe817118355b3460a9cbb7606bec81eafab61645d712f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35736168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17f38e1710caf22f06fdaf6fa2662e50be8e3018a2dadaa8985cc817c33dd0e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Jan 2023 18:09:01 GMT
ADD file:512505c2df26db88aeeb5025ff073a2d8e98d995422df61a5cad94d79ef22a42 in / 
# Mon, 02 Jan 2023 18:09:02 GMT
CMD ["bash"]
# Mon, 02 Jan 2023 18:29:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 02 Jan 2023 18:30:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ada5e428c090bd736690979612e7bece7c31ff1f1701ca35de4d1899e835e69a`  
		Last Modified: Mon, 02 Jan 2023 18:09:56 GMT  
		Size: 25.7 MB (25669058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e756f227648e5a559b1f2387229c92d1fd4b83589d63631f0d177d76e2c6e34`  
		Last Modified: Mon, 02 Jan 2023 18:38:32 GMT  
		Size: 5.9 MB (5925890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb3fe222b3eac428f3f8b9fff7621e4aa631ace7d402b5590058b150e5b19b2`  
		Last Modified: Mon, 02 Jan 2023 18:38:28 GMT  
		Size: 4.1 MB (4141220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fda9c3700adea9ebf2a25f69e3fb0d16144aab609db1bfd6941240a782053fa0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35981625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3e33f499598c717b571c0a2865c0a1ccb50eed2db40726fac004cf45a99164`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jan 2023 14:49:06 GMT
ARG RELEASE
# Wed, 25 Jan 2023 14:49:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 25 Jan 2023 14:49:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 25 Jan 2023 14:49:06 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 25 Jan 2023 14:49:08 GMT
ADD file:81c93bf9ec11b910a5bae8b977a82a78cb327c7bf9d0991542c9b6847cf19210 in / 
# Wed, 25 Jan 2023 14:49:12 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:48:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:48:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:baee7507e081825c5b8092bafec6f28ca06c374ba10b4b532df29c9f65e5c418`  
		Last Modified: Tue, 31 Jan 2023 17:57:05 GMT  
		Size: 26.0 MB (25988814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c8f82b0c7a188f1ec218ba8403f1b6a34d7a9c8e8ed19ba33be8c40cbdd1bf`  
		Last Modified: Tue, 31 Jan 2023 17:57:03 GMT  
		Size: 6.3 MB (6318088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48821d942fce639c03055802ef51131f9e24c67fef4c693ca3673e3aaafbdc77`  
		Last Modified: Tue, 31 Jan 2023 17:57:03 GMT  
		Size: 3.7 MB (3674723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
