<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `amazonlinux`

-	[`amazonlinux:1`](#amazonlinux1)
-	[`amazonlinux:1-with-sources`](#amazonlinux1-with-sources)
-	[`amazonlinux:2`](#amazonlinux2)
-	[`amazonlinux:2-with-sources`](#amazonlinux2-with-sources)
-	[`amazonlinux:2.0.20220719.0`](#amazonlinux20202207190)
-	[`amazonlinux:2.0.20220719.0-with-sources`](#amazonlinux20202207190-with-sources)
-	[`amazonlinux:2018.03`](#amazonlinux201803)
-	[`amazonlinux:2018.03-with-sources`](#amazonlinux201803-with-sources)
-	[`amazonlinux:2018.03.0.20220705.1`](#amazonlinux2018030202207051)
-	[`amazonlinux:2018.03.0.20220705.1-with-sources`](#amazonlinux2018030202207051-with-sources)
-	[`amazonlinux:2022`](#amazonlinux2022)
-	[`amazonlinux:2022-with-sources`](#amazonlinux2022-with-sources)
-	[`amazonlinux:2022.0.20220817.0`](#amazonlinux20220202208170)
-	[`amazonlinux:2022.0.20220817.0-with-sources`](#amazonlinux20220202208170-with-sources)
-	[`amazonlinux:devel`](#amazonlinuxdevel)
-	[`amazonlinux:devel-with-sources`](#amazonlinuxdevel-with-sources)
-	[`amazonlinux:latest`](#amazonlinuxlatest)
-	[`amazonlinux:with-sources`](#amazonlinuxwith-sources)

## `amazonlinux:1`

```console
$ docker pull amazonlinux@sha256:4c2c7b34d4195b4de02111d15ff93b0b6df45f5514a4d13ef6fd6014fa02c091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7469889f01ba05936a481dec30931832c0887783ab94b82c557029d521cb2773
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62349761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5ab74eaa7e03d0ade2d3efb77c8adfb3f9dfd95002a9e098afd17f3c2e826d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Aug 2022 00:19:44 GMT
ADD file:578d048adbda4319c9c7a4cc58359e1b2120c1fea0bdd7af885085f085b76543 in / 
# Thu, 04 Aug 2022 00:19:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c99b462d7b9e003ee491b5822729d97c1a950b380b4ed0d31dd841909eaaa47`  
		Last Modified: Thu, 04 Aug 2022 00:20:52 GMT  
		Size: 62.3 MB (62349761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:4185f05daac0e029ed74065c968aa3550738e71f28f865afb203e48443d8f25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:d587f87e29ec3c73030808824cd64ffc259edf7ec172feafe2eeaab6452dfb79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1862d4c5d4530382c100d0ad62b44402dd8056ca13a22de7b6c7b0928fc06538`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Aug 2022 00:19:44 GMT
ADD file:578d048adbda4319c9c7a4cc58359e1b2120c1fea0bdd7af885085f085b76543 in / 
# Thu, 04 Aug 2022 00:19:45 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:20:11 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-88cdcaaae92c13e9b16f4e24733dac64044525869a4d99c16f84d49e67daaf62.tar.gz"     && echo "4f388bc0087173f93599d0e9c5b6548cfea6212e7e88c1955793515a6efdae5b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:0c99b462d7b9e003ee491b5822729d97c1a950b380b4ed0d31dd841909eaaa47`  
		Last Modified: Thu, 04 Aug 2022 00:20:52 GMT  
		Size: 62.3 MB (62349761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566b981add5da336c6f5f83b0f5e18f5360adace1960c3834dde438b258a012a`  
		Last Modified: Thu, 04 Aug 2022 00:21:21 GMT  
		Size: 452.7 MB (452685076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2`

```console
$ docker pull amazonlinux@sha256:3535ab19660e96ed538ae7814f12eda76606064e40e2b8775aa74613bc8e6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2` - linux; amd64

```console
$ docker pull amazonlinux@sha256:586ecf7413d0d53c0983872be242c371d8da2ee7a57d5cbdad7761b5824a74f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62316216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f341032df1f72651e5af72fefbc21a1d6859f825a8455bb890470b959d759faa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:4905bf6f6d5496b4d779775d341b0120522ff3c99566d934ef8699dcfb370299
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63927916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b142cd55b3b71d694d17f6ff0a9fa17decd265c53f0baa899c44062fc513f06a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:39:26 GMT
ADD file:3ec97c6bec2a8682b0b4088021da97853effeb7dfafb69329cfcb5686c3dee30 in / 
# Fri, 12 Aug 2022 00:39:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9f9c648afd7976bdc42d03595d6a1c1c502c47f18abb3f42a9a20b38e7d6e161`  
		Last Modified: Mon, 01 Aug 2022 22:09:01 GMT  
		Size: 63.9 MB (63927916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2-with-sources`

```console
$ docker pull amazonlinux@sha256:fd9b4eb6bf0f5ce0b9074867ebef131505ce4f4735e493f121aeebe8e1051067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:112e2657cefe343bb8d09ff30a6f4feec6eaf5c0813cb38c895fa3c43e402c4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486338250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255bdecc3d95276f497d739d3a60969d8f7802a30152ab824f3aef4116382d94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 00:20:41 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c49e40d8cbba1157c747e1483c3371ef9e59567ec7d1e3cc5f21cde9df7b4f9d.tar.gz"     && echo "66afed6d6747b523bcb2d9acb55c562107bdc4c5a06b822bd5c2c7775772824b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39a5207cea55497b8a954978bb7ea93401d4a5ad0f19d2629d2d0773b38c376`  
		Last Modified: Fri, 12 Aug 2022 00:21:51 GMT  
		Size: 424.0 MB (424022034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:89254f2eecdad7f0fa019a718f913a194297fd0b455df4b2783bb512bef3ac32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487949918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa933c5f77a29a0d263eb46994456ea32cff3c47ec93f82be70ed043212f888`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:39:26 GMT
ADD file:3ec97c6bec2a8682b0b4088021da97853effeb7dfafb69329cfcb5686c3dee30 in / 
# Fri, 12 Aug 2022 00:39:28 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 00:39:51 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c49e40d8cbba1157c747e1483c3371ef9e59567ec7d1e3cc5f21cde9df7b4f9d.tar.gz"     && echo "66afed6d6747b523bcb2d9acb55c562107bdc4c5a06b822bd5c2c7775772824b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:9f9c648afd7976bdc42d03595d6a1c1c502c47f18abb3f42a9a20b38e7d6e161`  
		Last Modified: Mon, 01 Aug 2022 22:09:01 GMT  
		Size: 63.9 MB (63927916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1f88192a4287bbbeeb2fd730a6ae32120d881986dfc6898b18084e3c4bb94`  
		Last Modified: Fri, 12 Aug 2022 00:41:18 GMT  
		Size: 424.0 MB (424022002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220719.0`

```console
$ docker pull amazonlinux@sha256:3535ab19660e96ed538ae7814f12eda76606064e40e2b8775aa74613bc8e6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220719.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:586ecf7413d0d53c0983872be242c371d8da2ee7a57d5cbdad7761b5824a74f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62316216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f341032df1f72651e5af72fefbc21a1d6859f825a8455bb890470b959d759faa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20220719.0` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:4905bf6f6d5496b4d779775d341b0120522ff3c99566d934ef8699dcfb370299
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63927916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b142cd55b3b71d694d17f6ff0a9fa17decd265c53f0baa899c44062fc513f06a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:39:26 GMT
ADD file:3ec97c6bec2a8682b0b4088021da97853effeb7dfafb69329cfcb5686c3dee30 in / 
# Fri, 12 Aug 2022 00:39:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9f9c648afd7976bdc42d03595d6a1c1c502c47f18abb3f42a9a20b38e7d6e161`  
		Last Modified: Mon, 01 Aug 2022 22:09:01 GMT  
		Size: 63.9 MB (63927916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2.0.20220719.0-with-sources`

```console
$ docker pull amazonlinux@sha256:fd9b4eb6bf0f5ce0b9074867ebef131505ce4f4735e493f121aeebe8e1051067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2.0.20220719.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:112e2657cefe343bb8d09ff30a6f4feec6eaf5c0813cb38c895fa3c43e402c4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486338250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255bdecc3d95276f497d739d3a60969d8f7802a30152ab824f3aef4116382d94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 00:20:41 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c49e40d8cbba1157c747e1483c3371ef9e59567ec7d1e3cc5f21cde9df7b4f9d.tar.gz"     && echo "66afed6d6747b523bcb2d9acb55c562107bdc4c5a06b822bd5c2c7775772824b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39a5207cea55497b8a954978bb7ea93401d4a5ad0f19d2629d2d0773b38c376`  
		Last Modified: Fri, 12 Aug 2022 00:21:51 GMT  
		Size: 424.0 MB (424022034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2.0.20220719.0-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:89254f2eecdad7f0fa019a718f913a194297fd0b455df4b2783bb512bef3ac32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487949918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa933c5f77a29a0d263eb46994456ea32cff3c47ec93f82be70ed043212f888`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:39:26 GMT
ADD file:3ec97c6bec2a8682b0b4088021da97853effeb7dfafb69329cfcb5686c3dee30 in / 
# Fri, 12 Aug 2022 00:39:28 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 00:39:51 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c49e40d8cbba1157c747e1483c3371ef9e59567ec7d1e3cc5f21cde9df7b4f9d.tar.gz"     && echo "66afed6d6747b523bcb2d9acb55c562107bdc4c5a06b822bd5c2c7775772824b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:9f9c648afd7976bdc42d03595d6a1c1c502c47f18abb3f42a9a20b38e7d6e161`  
		Last Modified: Mon, 01 Aug 2022 22:09:01 GMT  
		Size: 63.9 MB (63927916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1f88192a4287bbbeeb2fd730a6ae32120d881986dfc6898b18084e3c4bb94`  
		Last Modified: Fri, 12 Aug 2022 00:41:18 GMT  
		Size: 424.0 MB (424022002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03`

```console
$ docker pull amazonlinux@sha256:4c2c7b34d4195b4de02111d15ff93b0b6df45f5514a4d13ef6fd6014fa02c091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7469889f01ba05936a481dec30931832c0887783ab94b82c557029d521cb2773
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62349761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5ab74eaa7e03d0ade2d3efb77c8adfb3f9dfd95002a9e098afd17f3c2e826d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Aug 2022 00:19:44 GMT
ADD file:578d048adbda4319c9c7a4cc58359e1b2120c1fea0bdd7af885085f085b76543 in / 
# Thu, 04 Aug 2022 00:19:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c99b462d7b9e003ee491b5822729d97c1a950b380b4ed0d31dd841909eaaa47`  
		Last Modified: Thu, 04 Aug 2022 00:20:52 GMT  
		Size: 62.3 MB (62349761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03-with-sources`

```console
$ docker pull amazonlinux@sha256:4185f05daac0e029ed74065c968aa3550738e71f28f865afb203e48443d8f25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:d587f87e29ec3c73030808824cd64ffc259edf7ec172feafe2eeaab6452dfb79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1862d4c5d4530382c100d0ad62b44402dd8056ca13a22de7b6c7b0928fc06538`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Aug 2022 00:19:44 GMT
ADD file:578d048adbda4319c9c7a4cc58359e1b2120c1fea0bdd7af885085f085b76543 in / 
# Thu, 04 Aug 2022 00:19:45 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:20:11 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-88cdcaaae92c13e9b16f4e24733dac64044525869a4d99c16f84d49e67daaf62.tar.gz"     && echo "4f388bc0087173f93599d0e9c5b6548cfea6212e7e88c1955793515a6efdae5b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:0c99b462d7b9e003ee491b5822729d97c1a950b380b4ed0d31dd841909eaaa47`  
		Last Modified: Thu, 04 Aug 2022 00:20:52 GMT  
		Size: 62.3 MB (62349761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566b981add5da336c6f5f83b0f5e18f5360adace1960c3834dde438b258a012a`  
		Last Modified: Thu, 04 Aug 2022 00:21:21 GMT  
		Size: 452.7 MB (452685076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20220705.1`

```console
$ docker pull amazonlinux@sha256:4c2c7b34d4195b4de02111d15ff93b0b6df45f5514a4d13ef6fd6014fa02c091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20220705.1` - linux; amd64

```console
$ docker pull amazonlinux@sha256:7469889f01ba05936a481dec30931832c0887783ab94b82c557029d521cb2773
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62349761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5ab74eaa7e03d0ade2d3efb77c8adfb3f9dfd95002a9e098afd17f3c2e826d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Aug 2022 00:19:44 GMT
ADD file:578d048adbda4319c9c7a4cc58359e1b2120c1fea0bdd7af885085f085b76543 in / 
# Thu, 04 Aug 2022 00:19:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c99b462d7b9e003ee491b5822729d97c1a950b380b4ed0d31dd841909eaaa47`  
		Last Modified: Thu, 04 Aug 2022 00:20:52 GMT  
		Size: 62.3 MB (62349761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2018.03.0.20220705.1-with-sources`

```console
$ docker pull amazonlinux@sha256:4185f05daac0e029ed74065c968aa3550738e71f28f865afb203e48443d8f25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2018.03.0.20220705.1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:d587f87e29ec3c73030808824cd64ffc259edf7ec172feafe2eeaab6452dfb79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.0 MB (515034837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1862d4c5d4530382c100d0ad62b44402dd8056ca13a22de7b6c7b0928fc06538`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Aug 2022 00:19:44 GMT
ADD file:578d048adbda4319c9c7a4cc58359e1b2120c1fea0bdd7af885085f085b76543 in / 
# Thu, 04 Aug 2022 00:19:45 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:20:11 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-88cdcaaae92c13e9b16f4e24733dac64044525869a4d99c16f84d49e67daaf62.tar.gz"     && echo "4f388bc0087173f93599d0e9c5b6548cfea6212e7e88c1955793515a6efdae5b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:0c99b462d7b9e003ee491b5822729d97c1a950b380b4ed0d31dd841909eaaa47`  
		Last Modified: Thu, 04 Aug 2022 00:20:52 GMT  
		Size: 62.3 MB (62349761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566b981add5da336c6f5f83b0f5e18f5360adace1960c3834dde438b258a012a`  
		Last Modified: Thu, 04 Aug 2022 00:21:21 GMT  
		Size: 452.7 MB (452685076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022`

```console
$ docker pull amazonlinux@sha256:1fac625ba5096dca036f6b5050c8ef71cfb6f05cc2bd57dae8ab0fb234800f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022` - linux; amd64

```console
$ docker pull amazonlinux@sha256:b003fbc7bcd0feef87844ad9507a9b363b0214e40a37b131c35526dc24b4ebc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57844028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15df3378c8ae9a475706b1adb8771cfa61c4f0afec974ddb9581495d3f02da3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:19cc84ca97003c4e5b875be85dafbeb338403d29b71839548f9be31aac02e314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56641949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d4ca5ed86ff1a81bfc554b778d473a1f37d0a9fa36dccd554de26c08529b9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Aug 2022 12:14:13 GMT
ADD file:66d41fa1401574d2e46e90ac16b59303f71c7bf398ddb0922a8d1e901ff01a33 in / 
# Wed, 03 Aug 2022 12:14:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:71f53d65e46f63ed07b6ba9d631c781f35a9e3aa0c59d15d2a6b8cf540ea474c`  
		Last Modified: Wed, 03 Aug 2022 12:15:19 GMT  
		Size: 56.6 MB (56641949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022-with-sources`

```console
$ docker pull amazonlinux@sha256:f20fdb3ceb3a1ffaf6b8c6febde34ad55e4510a53c68a18ec7fd4f996dd73aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:2022-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:fa8b758e194c757f8da89ab20ca1bd5e9453e192a8c2052d719898dd8417c45e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392627347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef88d77fa23bb2a8b1cdffc716fe8eed289a8eef455f685579294f76c85f783`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 00:07:30 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224af1760478d3b5043995f3d5520957bbb16e82027bbe9e0378b6f5c95194a5`  
		Last Modified: Thu, 25 Aug 2022 00:08:30 GMT  
		Size: 334.8 MB (334783319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:2022-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:06237ff0de1785329f0428e83d7ee58d1430a5f0e33cbde4edcd9dddcf292d7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 MB (391374875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972d3f26f41b671359686ec38bc7ed11c9d2c6014e0da98b70e878a176bc0ae7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Aug 2022 12:14:13 GMT
ADD file:66d41fa1401574d2e46e90ac16b59303f71c7bf398ddb0922a8d1e901ff01a33 in / 
# Wed, 03 Aug 2022 12:14:14 GMT
CMD ["/bin/bash"]
# Wed, 03 Aug 2022 12:14:34 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-957d3ae3a19e9ce71b665e8cd92c84fbdd09ac787fc6fe6e529d2eb7dda57e9b.tar.gz"     && echo "e6514c0ba308c79d2d886e936bb17e7b6c5bc1761cc0264a8bf9c7b97d751f2d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:71f53d65e46f63ed07b6ba9d631c781f35a9e3aa0c59d15d2a6b8cf540ea474c`  
		Last Modified: Wed, 03 Aug 2022 12:15:19 GMT  
		Size: 56.6 MB (56641949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61cbc02f83028ec35f5475f7de55ed612be3498de9f4689424fd826a703e17c`  
		Last Modified: Wed, 03 Aug 2022 12:16:01 GMT  
		Size: 334.7 MB (334732926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20220817.0`

```console
$ docker pull amazonlinux@sha256:39eb305c394076975b203dabaf233e9fa8cac435547824cbd9a78c8425d0ffd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2022.0.20220817.0` - linux; amd64

```console
$ docker pull amazonlinux@sha256:b003fbc7bcd0feef87844ad9507a9b363b0214e40a37b131c35526dc24b4ebc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57844028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15df3378c8ae9a475706b1adb8771cfa61c4f0afec974ddb9581495d3f02da3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:2022.0.20220817.0-with-sources`

```console
$ docker pull amazonlinux@sha256:27c44d5752df4c71967d021da8c2502f52b3b5a2851c5b6e355822ebb415326b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazonlinux:2022.0.20220817.0-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:fa8b758e194c757f8da89ab20ca1bd5e9453e192a8c2052d719898dd8417c45e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392627347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef88d77fa23bb2a8b1cdffc716fe8eed289a8eef455f685579294f76c85f783`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 00:07:30 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224af1760478d3b5043995f3d5520957bbb16e82027bbe9e0378b6f5c95194a5`  
		Last Modified: Thu, 25 Aug 2022 00:08:30 GMT  
		Size: 334.8 MB (334783319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel`

```console
$ docker pull amazonlinux@sha256:1fac625ba5096dca036f6b5050c8ef71cfb6f05cc2bd57dae8ab0fb234800f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel` - linux; amd64

```console
$ docker pull amazonlinux@sha256:b003fbc7bcd0feef87844ad9507a9b363b0214e40a37b131c35526dc24b4ebc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57844028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15df3378c8ae9a475706b1adb8771cfa61c4f0afec974ddb9581495d3f02da3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:19cc84ca97003c4e5b875be85dafbeb338403d29b71839548f9be31aac02e314
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56641949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d4ca5ed86ff1a81bfc554b778d473a1f37d0a9fa36dccd554de26c08529b9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Aug 2022 12:14:13 GMT
ADD file:66d41fa1401574d2e46e90ac16b59303f71c7bf398ddb0922a8d1e901ff01a33 in / 
# Wed, 03 Aug 2022 12:14:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:71f53d65e46f63ed07b6ba9d631c781f35a9e3aa0c59d15d2a6b8cf540ea474c`  
		Last Modified: Wed, 03 Aug 2022 12:15:19 GMT  
		Size: 56.6 MB (56641949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:devel-with-sources`

```console
$ docker pull amazonlinux@sha256:f20fdb3ceb3a1ffaf6b8c6febde34ad55e4510a53c68a18ec7fd4f996dd73aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:devel-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:fa8b758e194c757f8da89ab20ca1bd5e9453e192a8c2052d719898dd8417c45e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392627347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef88d77fa23bb2a8b1cdffc716fe8eed289a8eef455f685579294f76c85f783`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Aug 2022 00:07:09 GMT
ADD file:973933f5bfbb47797fba401d5a567b4d027701ea267555d49a784535be555e8a in / 
# Thu, 25 Aug 2022 00:07:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Aug 2022 00:07:30 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-5ba8bbe3d45c38a9ad91077ce0863a4fc2420c4cf29a10555efe58006356e519.tar.gz"     && echo "ba130541440e6ff7ba42f594def1d78b3ca051634f53baff790ccec2e69d9cfa  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ed187b61026965b611c5538a4bb1db56a8cb34caee2478637c149a39347f28dd`  
		Last Modified: Sat, 20 Aug 2022 04:05:27 GMT  
		Size: 57.8 MB (57844028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224af1760478d3b5043995f3d5520957bbb16e82027bbe9e0378b6f5c95194a5`  
		Last Modified: Thu, 25 Aug 2022 00:08:30 GMT  
		Size: 334.8 MB (334783319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:devel-with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:06237ff0de1785329f0428e83d7ee58d1430a5f0e33cbde4edcd9dddcf292d7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 MB (391374875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972d3f26f41b671359686ec38bc7ed11c9d2c6014e0da98b70e878a176bc0ae7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Aug 2022 12:14:13 GMT
ADD file:66d41fa1401574d2e46e90ac16b59303f71c7bf398ddb0922a8d1e901ff01a33 in / 
# Wed, 03 Aug 2022 12:14:14 GMT
CMD ["/bin/bash"]
# Wed, 03 Aug 2022 12:14:34 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-957d3ae3a19e9ce71b665e8cd92c84fbdd09ac787fc6fe6e529d2eb7dda57e9b.tar.gz"     && echo "e6514c0ba308c79d2d886e936bb17e7b6c5bc1761cc0264a8bf9c7b97d751f2d  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:71f53d65e46f63ed07b6ba9d631c781f35a9e3aa0c59d15d2a6b8cf540ea474c`  
		Last Modified: Wed, 03 Aug 2022 12:15:19 GMT  
		Size: 56.6 MB (56641949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61cbc02f83028ec35f5475f7de55ed612be3498de9f4689424fd826a703e17c`  
		Last Modified: Wed, 03 Aug 2022 12:16:01 GMT  
		Size: 334.7 MB (334732926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:latest`

```console
$ docker pull amazonlinux@sha256:3535ab19660e96ed538ae7814f12eda76606064e40e2b8775aa74613bc8e6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:latest` - linux; amd64

```console
$ docker pull amazonlinux@sha256:586ecf7413d0d53c0983872be242c371d8da2ee7a57d5cbdad7761b5824a74f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62316216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f341032df1f72651e5af72fefbc21a1d6859f825a8455bb890470b959d759faa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:latest` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:4905bf6f6d5496b4d779775d341b0120522ff3c99566d934ef8699dcfb370299
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63927916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b142cd55b3b71d694d17f6ff0a9fa17decd265c53f0baa899c44062fc513f06a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:39:26 GMT
ADD file:3ec97c6bec2a8682b0b4088021da97853effeb7dfafb69329cfcb5686c3dee30 in / 
# Fri, 12 Aug 2022 00:39:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9f9c648afd7976bdc42d03595d6a1c1c502c47f18abb3f42a9a20b38e7d6e161`  
		Last Modified: Mon, 01 Aug 2022 22:09:01 GMT  
		Size: 63.9 MB (63927916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `amazonlinux:with-sources`

```console
$ docker pull amazonlinux@sha256:fd9b4eb6bf0f5ce0b9074867ebef131505ce4f4735e493f121aeebe8e1051067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazonlinux:with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:112e2657cefe343bb8d09ff30a6f4feec6eaf5c0813cb38c895fa3c43e402c4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486338250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255bdecc3d95276f497d739d3a60969d8f7802a30152ab824f3aef4116382d94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:20:15 GMT
ADD file:56a385790046ac5dfb85932009eb1e99c8593221e306b937274c477c05cc9886 in / 
# Fri, 12 Aug 2022 00:20:15 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 00:20:41 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c49e40d8cbba1157c747e1483c3371ef9e59567ec7d1e3cc5f21cde9df7b4f9d.tar.gz"     && echo "66afed6d6747b523bcb2d9acb55c562107bdc4c5a06b822bd5c2c7775772824b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:5e0be87f98fb0e8a6ecddb6b717178ddc6555638e6e89d39929d47654b79739d`  
		Last Modified: Mon, 01 Aug 2022 22:09:03 GMT  
		Size: 62.3 MB (62316216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39a5207cea55497b8a954978bb7ea93401d4a5ad0f19d2629d2d0773b38c376`  
		Last Modified: Fri, 12 Aug 2022 00:21:51 GMT  
		Size: 424.0 MB (424022034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazonlinux:with-sources` - linux; arm64 variant v8

```console
$ docker pull amazonlinux@sha256:89254f2eecdad7f0fa019a718f913a194297fd0b455df4b2783bb512bef3ac32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487949918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa933c5f77a29a0d263eb46994456ea32cff3c47ec93f82be70ed043212f888`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Aug 2022 00:39:26 GMT
ADD file:3ec97c6bec2a8682b0b4088021da97853effeb7dfafb69329cfcb5686c3dee30 in / 
# Fri, 12 Aug 2022 00:39:28 GMT
CMD ["/bin/bash"]
# Fri, 12 Aug 2022 00:39:51 GMT
RUN mkdir /usr/src/srpm     && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle-c49e40d8cbba1157c747e1483c3371ef9e59567ec7d1e3cc5f21cde9df7b4f9d.tar.gz"     && echo "66afed6d6747b523bcb2d9acb55c562107bdc4c5a06b822bd5c2c7775772824b  /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:9f9c648afd7976bdc42d03595d6a1c1c502c47f18abb3f42a9a20b38e7d6e161`  
		Last Modified: Mon, 01 Aug 2022 22:09:01 GMT  
		Size: 63.9 MB (63927916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d1f88192a4287bbbeeb2fd730a6ae32120d881986dfc6898b18084e3c4bb94`  
		Last Modified: Fri, 12 Aug 2022 00:41:18 GMT  
		Size: 424.0 MB (424022002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
