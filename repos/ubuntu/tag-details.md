<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:24.04`](#ubuntu2404)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20240410`](#ubuntufocal-20240410)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20240405`](#ubuntujammy-20240405)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20240405`](#ubuntumantic-20240405)
-	[`ubuntu:noble`](#ubuntunoble)
-	[`ubuntu:noble-20240407.1`](#ubuntunoble-202404071)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:71b82b8e734f5cd0b3533a16f40ca1271f28d87343972bb4cd6bd6c38f1bd38e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:39e6324487ef503ef36c38bf0b57935d639398ca0d6081fd20a17f90b956a7a4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33985b2ba010a084175876629b280ed9ae49965e9ee5d30b79896cad707bf350`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bd8a5c42887492c47adc873b855753158392742c0d9155c6bc2a0c5d0e3dcd82
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a13b0a84dab9cf0b088f39766fab7ba58ba42d1414ccf0ead6203f371923788`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:78102c38ae65613b2ee783b6958bab73ce162f03487b33a21174bee44d9fb37a`  
		Last Modified: Wed, 10 Apr 2024 19:19:31 GMT  
		Size: 23.6 MB (23622898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d40777b9a5329d3611f7bc40738b4cd459c8b1508fa8cc7c1555674c40671598
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcc83a51b0096c961e9431235462f6402e148368c77d99392a51a0da5b9b8b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ef596418082f13191304a313d8b6aa0d292c5e1135f16d811866555593867175
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3b4511576ff9171ba7363af64dd3bba1a8983bf9218fa63369dbd13a6283c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:04:56 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:04:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:04:59 GMT
ADD file:8efe37e124c3eb7c9e2b3ba1f33a019526490b9a49cbe8997abf72caf6bb7ece in / 
# Wed, 10 Apr 2024 19:04:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1dff51f344fcb2f57b1b40c521798a8e8ccde4d330528f16250dde1506790c1e`  
		Last Modified: Wed, 10 Apr 2024 19:19:37 GMT  
		Size: 32.1 MB (32076803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:7faa8d7f57e4188578989d11813405b5ae04bc1ae3340758bcc0b8f82a04696a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26366699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e707f53d2a103ac02d37a169339f3ed9df99e027f994f7d0335a5ad237067da6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:51:34 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:51:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:51:38 GMT
ADD file:c91b061ad49bce1f6e2860bfe87ed2e94cc280b915289f041d2dd5ce3ef385ad in / 
# Wed, 10 Apr 2024 18:51:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9c9043abb8ba47bd083fee5b16d1e0d6dbb7f1455978a8812b11443832ed103`  
		Last Modified: Wed, 10 Apr 2024 19:19:43 GMT  
		Size: 26.4 MB (26366699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:1b8d8ff4777f36f19bfe73ee4df61e3a0b789caeff29caa019539ec7c9a57f95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:6f6ec53d36a9504f01e3636cf68e0e03761a3b6947a95ba430ae553ee3aaf4d9
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af9ba4f0a47d9bc8b1ffa492c6b0276476f1889cf4e699fba2236924e5932ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c645031de2917ade93ec54b118d5d3e45de72ef580b8f419a8cdc41e01d042c`  
		Last Modified: Wed, 10 Apr 2024 19:20:48 GMT  
		Size: 29.5 MB (29533419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4eb00f9a877cbabfc91d271a91855278df10f2c1bf80fd56cf210c14fc1f5618
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27715f1115e575122d6207d7d6303b3866f01feda96fdee851618a997ebfe8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:04 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:15 GMT
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 10 Apr 2024 19:09:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b693c0578bb86a6111c6b9770eb9fd6826cee6d2825b5869e3aa66e53454166a`  
		Last Modified: Wed, 10 Apr 2024 19:21:01 GMT  
		Size: 26.6 MB (26637579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c427cc251a507a2459eacd770fe2cd7e451f883b077e09b2d27fa6f129b29d81
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27359551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbcc2701b935fa13b53ee525549d83c27c3560055c578768f1f4d4f1b8bde32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:69f4713b4192f088af1d22bb4bf672a763f1f96b82d968737807bd8bb4257662
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34458220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750476767bb499f755c183d1a7f5c083c5952944171ee1eef61bdc4ff8958d72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:90934b7f1f0e926037c726882dd3c20ca2b4436c3073523643b82e02f5fe7dd3`  
		Last Modified: Wed, 10 Apr 2024 19:21:07 GMT  
		Size: 34.5 MB (34458220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:c194ef08b0f8dadd78c9932865553ec3e045e20b07daba9364fd98a7c2de19fe
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cd3ff2b0480cdac7c482efce325c5612a005e4a743f55822537548a8dcfefc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:05 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 10 Apr 2024 19:09:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6e1eba39e4ebf768879e23d5cbf0eb1ad6db055027ddec35427160ce576c3d4`  
		Last Modified: Wed, 10 Apr 2024 19:21:13 GMT  
		Size: 28.0 MB (28000125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:008c4aa50da87ad7bc586a47787491f76c79c62cc5bdbee29121ee9e02c03f3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:667a63093579bd2ffe501ff9ae68eab2674b9aa5d5b908ed59f901d57333ff49
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93816ef1ab9007d690d5e88dbb2646b371d52f27a44605fee6561519afc15d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:08 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:08 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:10 GMT
ADD file:e20f41d92fb02981d800b49f0872a5a0bc05c8b9f7dc569390c26af4b8d41caa in / 
# Fri, 12 Apr 2024 15:51:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:41771a47f3dbb290996e87044de7dcf7c3bfb29ee4259366c74b5c74a58b0354`  
		Last Modified: Fri, 12 Apr 2024 15:59:58 GMT  
		Size: 27.2 MB (27233527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d2ef4d29f07d2e34e02bd3edbecd7e97c066a5ac1eddaf726d4dab7b4fd30abd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24887415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a6f00029030e4f1fd73079a98f46caac7940db908032c0e53a2dd347ef6fa2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:42 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:48 GMT
ADD file:7ae24dbfcd35eb56c9df6cfe135ee0660ec7885c25b732bd820de74e6e977e91 in / 
# Fri, 12 Apr 2024 15:50:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a032cb47dd8d01b6383603fb581fd99c856b139e1a013415d969e9421b6803bc`  
		Last Modified: Fri, 12 Apr 2024 16:00:11 GMT  
		Size: 24.9 MB (24887415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1e4c25185533d7bed7864744d2a5b2c43bf1ac7a7f6427267c72828712e4e16a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26413454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be742dd48b8ce1c5254b2f75a0f28a5ad54d5cdffe7f198217d9f11618a8f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:942a35531af124aa3c3906d47e8dd6472cec1bfa9ec398abfea155f72c64cc96`  
		Last Modified: Fri, 12 Apr 2024 16:00:05 GMT  
		Size: 26.4 MB (26413454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dfd506bb0626da0d2b3c2b7ac631fb3652efbd1fa781fff75213eb2c7bbe642b
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31364169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc86e239e5f03573f0c9009dd87077ea94c27ae6840005fc08e42f252d28da7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:38 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:42 GMT
ADD file:a8da603c55c74defd91d533f7d8ae1989fdabaffbd1dffc9bda21c86eb06e0dd in / 
# Fri, 12 Apr 2024 15:50:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c8a56c06da37682f6872182646d36c2c9d77b6b1578a4acecf0128467910316b`  
		Last Modified: Fri, 12 Apr 2024 16:00:17 GMT  
		Size: 31.4 MB (31364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:fb8daccea84b4657e01ec61e5a1d9dbb75739c8096a2580f9ae1e379846feb54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f300c99459926efcebd5cacdab52ee0900534912b1c75db2556cfec826f1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2867589a33d86d4239850bd34e12ff3064467a71264788d2dd5d807347b0f1c7`  
		Last Modified: Fri, 12 Apr 2024 16:00:25 GMT  
		Size: 27.3 MB (27331928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:24.04`

```console
$ docker pull ubuntu@sha256:5b582c80ed6832665ffb6181ab4d3e5e70c30c2548fbcea1de8a0a51f161be8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:24.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:1f84a3ed33b02bf3ccd75b06654a5dc1e0faa02b2beac4c37013859f0a26eb52
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28860028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31181e6ba2cef926292d50d592b15d745a9fb256013df363db1810e7060ab49f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e10c600007064e23f53bb653e9e837ccb78fac36df467e76704df73ffac52678`  
		Last Modified: Sun, 07 Apr 2024 17:19:05 GMT  
		Size: 28.9 MB (28860028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b1bac55096baf00b115c63c90d652bc3b61881fa892fcf907d93ac9813b94614
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26102916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab356d34f77ef44955e18cf6d2158771582951f7abef1cf8dbe21f65aa1a8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:55 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:08:04 GMT
ADD file:969299ec7ff65f7cea645f47c5b49e4d321bc39113984c894021da377f00b25a in / 
# Sun, 07 Apr 2024 17:08:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6361534ea0ef9c51acf151b33e52b03a45660ec66315943c40ec2d02634f99bc`  
		Last Modified: Sun, 07 Apr 2024 17:19:17 GMT  
		Size: 26.1 MB (26102916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b61c7c7b34921e6805388eb4cd2bd7adb40f842af583c7af8eb28d3c50e6ea97
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (27980097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daa4940cd722b5042f615f16a268ba712e96f0be896c7dd0cf9310c545a5c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:27 GMT
ADD file:517341670501a6ab8690a40210b8029b114b534a5061f599304cff1e6fd8ad07 in / 
# Sun, 07 Apr 2024 17:00:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43c7ec942a10b2818754e030a717ceb80881eef105a2efc304a3afeb2421e78c`  
		Last Modified: Sun, 07 Apr 2024 17:19:11 GMT  
		Size: 28.0 MB (27980097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:97fd25490e87e94c266c99b5a83e9d5b1be53cf6c509a9fa5b40011842814261
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33445880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b6286411794163651f4e78f7d12209bef2bb473935a52ace8a21905ffd3921`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:29 GMT
ADD file:4ed9f2ccb9342fb3acaaec8d21d9bf5029a86619c6c8878425eadc78e18003b5 in / 
# Sun, 07 Apr 2024 17:00:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8869b87a1c47aa026e7ce2df38a0a3412ebfcfe85bd377c65513aa7fc771d`  
		Last Modified: Sun, 07 Apr 2024 17:19:23 GMT  
		Size: 33.4 MB (33445880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:24.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:63c1538627e447932daae84283e194b14c6323c16a29d9bdbe071e8744c5f0b4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29113387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f38b99e0ca2a6f55155893071f008bb5b14f2d2afb0a48ded1f22e085ccfcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf319107486d1a8ff3845cc8abca0de71f7437518fe348fce75fb7db345a555`  
		Last Modified: Sun, 07 Apr 2024 17:19:30 GMT  
		Size: 29.1 MB (29113387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:5b582c80ed6832665ffb6181ab4d3e5e70c30c2548fbcea1de8a0a51f161be8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:1f84a3ed33b02bf3ccd75b06654a5dc1e0faa02b2beac4c37013859f0a26eb52
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28860028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31181e6ba2cef926292d50d592b15d745a9fb256013df363db1810e7060ab49f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e10c600007064e23f53bb653e9e837ccb78fac36df467e76704df73ffac52678`  
		Last Modified: Sun, 07 Apr 2024 17:19:05 GMT  
		Size: 28.9 MB (28860028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b1bac55096baf00b115c63c90d652bc3b61881fa892fcf907d93ac9813b94614
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26102916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab356d34f77ef44955e18cf6d2158771582951f7abef1cf8dbe21f65aa1a8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:55 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:08:04 GMT
ADD file:969299ec7ff65f7cea645f47c5b49e4d321bc39113984c894021da377f00b25a in / 
# Sun, 07 Apr 2024 17:08:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6361534ea0ef9c51acf151b33e52b03a45660ec66315943c40ec2d02634f99bc`  
		Last Modified: Sun, 07 Apr 2024 17:19:17 GMT  
		Size: 26.1 MB (26102916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b61c7c7b34921e6805388eb4cd2bd7adb40f842af583c7af8eb28d3c50e6ea97
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (27980097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daa4940cd722b5042f615f16a268ba712e96f0be896c7dd0cf9310c545a5c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:27 GMT
ADD file:517341670501a6ab8690a40210b8029b114b534a5061f599304cff1e6fd8ad07 in / 
# Sun, 07 Apr 2024 17:00:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43c7ec942a10b2818754e030a717ceb80881eef105a2efc304a3afeb2421e78c`  
		Last Modified: Sun, 07 Apr 2024 17:19:11 GMT  
		Size: 28.0 MB (27980097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:97fd25490e87e94c266c99b5a83e9d5b1be53cf6c509a9fa5b40011842814261
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33445880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b6286411794163651f4e78f7d12209bef2bb473935a52ace8a21905ffd3921`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:29 GMT
ADD file:4ed9f2ccb9342fb3acaaec8d21d9bf5029a86619c6c8878425eadc78e18003b5 in / 
# Sun, 07 Apr 2024 17:00:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8869b87a1c47aa026e7ce2df38a0a3412ebfcfe85bd377c65513aa7fc771d`  
		Last Modified: Sun, 07 Apr 2024 17:19:23 GMT  
		Size: 33.4 MB (33445880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:63c1538627e447932daae84283e194b14c6323c16a29d9bdbe071e8744c5f0b4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29113387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f38b99e0ca2a6f55155893071f008bb5b14f2d2afb0a48ded1f22e085ccfcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf319107486d1a8ff3845cc8abca0de71f7437518fe348fce75fb7db345a555`  
		Last Modified: Sun, 07 Apr 2024 17:19:30 GMT  
		Size: 29.1 MB (29113387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:71b82b8e734f5cd0b3533a16f40ca1271f28d87343972bb4cd6bd6c38f1bd38e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:39e6324487ef503ef36c38bf0b57935d639398ca0d6081fd20a17f90b956a7a4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33985b2ba010a084175876629b280ed9ae49965e9ee5d30b79896cad707bf350`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bd8a5c42887492c47adc873b855753158392742c0d9155c6bc2a0c5d0e3dcd82
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a13b0a84dab9cf0b088f39766fab7ba58ba42d1414ccf0ead6203f371923788`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:78102c38ae65613b2ee783b6958bab73ce162f03487b33a21174bee44d9fb37a`  
		Last Modified: Wed, 10 Apr 2024 19:19:31 GMT  
		Size: 23.6 MB (23622898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d40777b9a5329d3611f7bc40738b4cd459c8b1508fa8cc7c1555674c40671598
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcc83a51b0096c961e9431235462f6402e148368c77d99392a51a0da5b9b8b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ef596418082f13191304a313d8b6aa0d292c5e1135f16d811866555593867175
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3b4511576ff9171ba7363af64dd3bba1a8983bf9218fa63369dbd13a6283c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:04:56 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:04:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:04:59 GMT
ADD file:8efe37e124c3eb7c9e2b3ba1f33a019526490b9a49cbe8997abf72caf6bb7ece in / 
# Wed, 10 Apr 2024 19:04:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1dff51f344fcb2f57b1b40c521798a8e8ccde4d330528f16250dde1506790c1e`  
		Last Modified: Wed, 10 Apr 2024 19:19:37 GMT  
		Size: 32.1 MB (32076803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:7faa8d7f57e4188578989d11813405b5ae04bc1ae3340758bcc0b8f82a04696a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26366699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e707f53d2a103ac02d37a169339f3ed9df99e027f994f7d0335a5ad237067da6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:51:34 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:51:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:51:38 GMT
ADD file:c91b061ad49bce1f6e2860bfe87ed2e94cc280b915289f041d2dd5ce3ef385ad in / 
# Wed, 10 Apr 2024 18:51:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9c9043abb8ba47bd083fee5b16d1e0d6dbb7f1455978a8812b11443832ed103`  
		Last Modified: Wed, 10 Apr 2024 19:19:43 GMT  
		Size: 26.4 MB (26366699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20240410`

```console
$ docker pull ubuntu@sha256:71b82b8e734f5cd0b3533a16f40ca1271f28d87343972bb4cd6bd6c38f1bd38e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20240410` - linux; amd64

```console
$ docker pull ubuntu@sha256:39e6324487ef503ef36c38bf0b57935d639398ca0d6081fd20a17f90b956a7a4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27511841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33985b2ba010a084175876629b280ed9ae49965e9ee5d30b79896cad707bf350`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240410` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bd8a5c42887492c47adc873b855753158392742c0d9155c6bc2a0c5d0e3dcd82
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23622898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a13b0a84dab9cf0b088f39766fab7ba58ba42d1414ccf0ead6203f371923788`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:40 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:41 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:52:51 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Wed, 10 Apr 2024 18:52:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:78102c38ae65613b2ee783b6958bab73ce162f03487b33a21174bee44d9fb37a`  
		Last Modified: Wed, 10 Apr 2024 19:19:31 GMT  
		Size: 23.6 MB (23622898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240410` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d40777b9a5329d3611f7bc40738b4cd459c8b1508fa8cc7c1555674c40671598
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcc83a51b0096c961e9431235462f6402e148368c77d99392a51a0da5b9b8b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240410` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ef596418082f13191304a313d8b6aa0d292c5e1135f16d811866555593867175
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32076803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3b4511576ff9171ba7363af64dd3bba1a8983bf9218fa63369dbd13a6283c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:04:56 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:04:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:04:56 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:04:59 GMT
ADD file:8efe37e124c3eb7c9e2b3ba1f33a019526490b9a49cbe8997abf72caf6bb7ece in / 
# Wed, 10 Apr 2024 19:04:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1dff51f344fcb2f57b1b40c521798a8e8ccde4d330528f16250dde1506790c1e`  
		Last Modified: Wed, 10 Apr 2024 19:19:37 GMT  
		Size: 32.1 MB (32076803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20240410` - linux; s390x

```console
$ docker pull ubuntu@sha256:7faa8d7f57e4188578989d11813405b5ae04bc1ae3340758bcc0b8f82a04696a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26366699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e707f53d2a103ac02d37a169339f3ed9df99e027f994f7d0335a5ad237067da6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:51:34 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:51:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:51:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:51:38 GMT
ADD file:c91b061ad49bce1f6e2860bfe87ed2e94cc280b915289f041d2dd5ce3ef385ad in / 
# Wed, 10 Apr 2024 18:51:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b9c9043abb8ba47bd083fee5b16d1e0d6dbb7f1455978a8812b11443832ed103`  
		Last Modified: Wed, 10 Apr 2024 19:19:43 GMT  
		Size: 26.4 MB (26366699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:1b8d8ff4777f36f19bfe73ee4df61e3a0b789caeff29caa019539ec7c9a57f95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy` - linux; amd64

```console
$ docker pull ubuntu@sha256:6f6ec53d36a9504f01e3636cf68e0e03761a3b6947a95ba430ae553ee3aaf4d9
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af9ba4f0a47d9bc8b1ffa492c6b0276476f1889cf4e699fba2236924e5932ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c645031de2917ade93ec54b118d5d3e45de72ef580b8f419a8cdc41e01d042c`  
		Last Modified: Wed, 10 Apr 2024 19:20:48 GMT  
		Size: 29.5 MB (29533419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4eb00f9a877cbabfc91d271a91855278df10f2c1bf80fd56cf210c14fc1f5618
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27715f1115e575122d6207d7d6303b3866f01feda96fdee851618a997ebfe8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:04 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:15 GMT
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 10 Apr 2024 19:09:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b693c0578bb86a6111c6b9770eb9fd6826cee6d2825b5869e3aa66e53454166a`  
		Last Modified: Wed, 10 Apr 2024 19:21:01 GMT  
		Size: 26.6 MB (26637579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c427cc251a507a2459eacd770fe2cd7e451f883b077e09b2d27fa6f129b29d81
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27359551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbcc2701b935fa13b53ee525549d83c27c3560055c578768f1f4d4f1b8bde32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:69f4713b4192f088af1d22bb4bf672a763f1f96b82d968737807bd8bb4257662
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34458220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750476767bb499f755c183d1a7f5c083c5952944171ee1eef61bdc4ff8958d72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:90934b7f1f0e926037c726882dd3c20ca2b4436c3073523643b82e02f5fe7dd3`  
		Last Modified: Wed, 10 Apr 2024 19:21:07 GMT  
		Size: 34.5 MB (34458220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:c194ef08b0f8dadd78c9932865553ec3e045e20b07daba9364fd98a7c2de19fe
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cd3ff2b0480cdac7c482efce325c5612a005e4a743f55822537548a8dcfefc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:05 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 10 Apr 2024 19:09:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6e1eba39e4ebf768879e23d5cbf0eb1ad6db055027ddec35427160ce576c3d4`  
		Last Modified: Wed, 10 Apr 2024 19:21:13 GMT  
		Size: 28.0 MB (28000125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20240405`

```console
$ docker pull ubuntu@sha256:1b8d8ff4777f36f19bfe73ee4df61e3a0b789caeff29caa019539ec7c9a57f95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20240405` - linux; amd64

```console
$ docker pull ubuntu@sha256:6f6ec53d36a9504f01e3636cf68e0e03761a3b6947a95ba430ae553ee3aaf4d9
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af9ba4f0a47d9bc8b1ffa492c6b0276476f1889cf4e699fba2236924e5932ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c645031de2917ade93ec54b118d5d3e45de72ef580b8f419a8cdc41e01d042c`  
		Last Modified: Wed, 10 Apr 2024 19:20:48 GMT  
		Size: 29.5 MB (29533419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240405` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4eb00f9a877cbabfc91d271a91855278df10f2c1bf80fd56cf210c14fc1f5618
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27715f1115e575122d6207d7d6303b3866f01feda96fdee851618a997ebfe8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:04 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:15 GMT
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 10 Apr 2024 19:09:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b693c0578bb86a6111c6b9770eb9fd6826cee6d2825b5869e3aa66e53454166a`  
		Last Modified: Wed, 10 Apr 2024 19:21:01 GMT  
		Size: 26.6 MB (26637579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240405` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c427cc251a507a2459eacd770fe2cd7e451f883b077e09b2d27fa6f129b29d81
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27359551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbcc2701b935fa13b53ee525549d83c27c3560055c578768f1f4d4f1b8bde32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240405` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:69f4713b4192f088af1d22bb4bf672a763f1f96b82d968737807bd8bb4257662
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34458220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750476767bb499f755c183d1a7f5c083c5952944171ee1eef61bdc4ff8958d72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:90934b7f1f0e926037c726882dd3c20ca2b4436c3073523643b82e02f5fe7dd3`  
		Last Modified: Wed, 10 Apr 2024 19:21:07 GMT  
		Size: 34.5 MB (34458220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20240405` - linux; s390x

```console
$ docker pull ubuntu@sha256:c194ef08b0f8dadd78c9932865553ec3e045e20b07daba9364fd98a7c2de19fe
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cd3ff2b0480cdac7c482efce325c5612a005e4a743f55822537548a8dcfefc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:05 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 10 Apr 2024 19:09:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6e1eba39e4ebf768879e23d5cbf0eb1ad6db055027ddec35427160ce576c3d4`  
		Last Modified: Wed, 10 Apr 2024 19:21:13 GMT  
		Size: 28.0 MB (28000125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:1b8d8ff4777f36f19bfe73ee4df61e3a0b789caeff29caa019539ec7c9a57f95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:6f6ec53d36a9504f01e3636cf68e0e03761a3b6947a95ba430ae553ee3aaf4d9
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af9ba4f0a47d9bc8b1ffa492c6b0276476f1889cf4e699fba2236924e5932ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3c645031de2917ade93ec54b118d5d3e45de72ef580b8f419a8cdc41e01d042c`  
		Last Modified: Wed, 10 Apr 2024 19:20:48 GMT  
		Size: 29.5 MB (29533419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:4eb00f9a877cbabfc91d271a91855278df10f2c1bf80fd56cf210c14fc1f5618
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27715f1115e575122d6207d7d6303b3866f01feda96fdee851618a997ebfe8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:04 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:15 GMT
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 10 Apr 2024 19:09:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b693c0578bb86a6111c6b9770eb9fd6826cee6d2825b5869e3aa66e53454166a`  
		Last Modified: Wed, 10 Apr 2024 19:21:01 GMT  
		Size: 26.6 MB (26637579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c427cc251a507a2459eacd770fe2cd7e451f883b077e09b2d27fa6f129b29d81
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 MB (27359551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbcc2701b935fa13b53ee525549d83c27c3560055c578768f1f4d4f1b8bde32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:69f4713b4192f088af1d22bb4bf672a763f1f96b82d968737807bd8bb4257662
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34458220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750476767bb499f755c183d1a7f5c083c5952944171ee1eef61bdc4ff8958d72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:90934b7f1f0e926037c726882dd3c20ca2b4436c3073523643b82e02f5fe7dd3`  
		Last Modified: Wed, 10 Apr 2024 19:21:07 GMT  
		Size: 34.5 MB (34458220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:c194ef08b0f8dadd78c9932865553ec3e045e20b07daba9364fd98a7c2de19fe
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28000125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cd3ff2b0480cdac7c482efce325c5612a005e4a743f55822537548a8dcfefc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:05 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Wed, 10 Apr 2024 19:09:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6e1eba39e4ebf768879e23d5cbf0eb1ad6db055027ddec35427160ce576c3d4`  
		Last Modified: Wed, 10 Apr 2024 19:21:13 GMT  
		Size: 28.0 MB (28000125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:008c4aa50da87ad7bc586a47787491f76c79c62cc5bdbee29121ee9e02c03f3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic` - linux; amd64

```console
$ docker pull ubuntu@sha256:667a63093579bd2ffe501ff9ae68eab2674b9aa5d5b908ed59f901d57333ff49
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93816ef1ab9007d690d5e88dbb2646b371d52f27a44605fee6561519afc15d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:08 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:08 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:10 GMT
ADD file:e20f41d92fb02981d800b49f0872a5a0bc05c8b9f7dc569390c26af4b8d41caa in / 
# Fri, 12 Apr 2024 15:51:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:41771a47f3dbb290996e87044de7dcf7c3bfb29ee4259366c74b5c74a58b0354`  
		Last Modified: Fri, 12 Apr 2024 15:59:58 GMT  
		Size: 27.2 MB (27233527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d2ef4d29f07d2e34e02bd3edbecd7e97c066a5ac1eddaf726d4dab7b4fd30abd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24887415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a6f00029030e4f1fd73079a98f46caac7940db908032c0e53a2dd347ef6fa2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:42 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:48 GMT
ADD file:7ae24dbfcd35eb56c9df6cfe135ee0660ec7885c25b732bd820de74e6e977e91 in / 
# Fri, 12 Apr 2024 15:50:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a032cb47dd8d01b6383603fb581fd99c856b139e1a013415d969e9421b6803bc`  
		Last Modified: Fri, 12 Apr 2024 16:00:11 GMT  
		Size: 24.9 MB (24887415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1e4c25185533d7bed7864744d2a5b2c43bf1ac7a7f6427267c72828712e4e16a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26413454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be742dd48b8ce1c5254b2f75a0f28a5ad54d5cdffe7f198217d9f11618a8f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:942a35531af124aa3c3906d47e8dd6472cec1bfa9ec398abfea155f72c64cc96`  
		Last Modified: Fri, 12 Apr 2024 16:00:05 GMT  
		Size: 26.4 MB (26413454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dfd506bb0626da0d2b3c2b7ac631fb3652efbd1fa781fff75213eb2c7bbe642b
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31364169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc86e239e5f03573f0c9009dd87077ea94c27ae6840005fc08e42f252d28da7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:38 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:42 GMT
ADD file:a8da603c55c74defd91d533f7d8ae1989fdabaffbd1dffc9bda21c86eb06e0dd in / 
# Fri, 12 Apr 2024 15:50:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c8a56c06da37682f6872182646d36c2c9d77b6b1578a4acecf0128467910316b`  
		Last Modified: Fri, 12 Apr 2024 16:00:17 GMT  
		Size: 31.4 MB (31364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:fb8daccea84b4657e01ec61e5a1d9dbb75739c8096a2580f9ae1e379846feb54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f300c99459926efcebd5cacdab52ee0900534912b1c75db2556cfec826f1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2867589a33d86d4239850bd34e12ff3064467a71264788d2dd5d807347b0f1c7`  
		Last Modified: Fri, 12 Apr 2024 16:00:25 GMT  
		Size: 27.3 MB (27331928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20240405`

```console
$ docker pull ubuntu@sha256:008c4aa50da87ad7bc586a47787491f76c79c62cc5bdbee29121ee9e02c03f3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic-20240405` - linux; amd64

```console
$ docker pull ubuntu@sha256:667a63093579bd2ffe501ff9ae68eab2674b9aa5d5b908ed59f901d57333ff49
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93816ef1ab9007d690d5e88dbb2646b371d52f27a44605fee6561519afc15d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:08 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:08 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:10 GMT
ADD file:e20f41d92fb02981d800b49f0872a5a0bc05c8b9f7dc569390c26af4b8d41caa in / 
# Fri, 12 Apr 2024 15:51:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:41771a47f3dbb290996e87044de7dcf7c3bfb29ee4259366c74b5c74a58b0354`  
		Last Modified: Fri, 12 Apr 2024 15:59:58 GMT  
		Size: 27.2 MB (27233527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240405` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d2ef4d29f07d2e34e02bd3edbecd7e97c066a5ac1eddaf726d4dab7b4fd30abd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24887415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a6f00029030e4f1fd73079a98f46caac7940db908032c0e53a2dd347ef6fa2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:42 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:48 GMT
ADD file:7ae24dbfcd35eb56c9df6cfe135ee0660ec7885c25b732bd820de74e6e977e91 in / 
# Fri, 12 Apr 2024 15:50:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a032cb47dd8d01b6383603fb581fd99c856b139e1a013415d969e9421b6803bc`  
		Last Modified: Fri, 12 Apr 2024 16:00:11 GMT  
		Size: 24.9 MB (24887415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240405` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1e4c25185533d7bed7864744d2a5b2c43bf1ac7a7f6427267c72828712e4e16a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26413454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be742dd48b8ce1c5254b2f75a0f28a5ad54d5cdffe7f198217d9f11618a8f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:942a35531af124aa3c3906d47e8dd6472cec1bfa9ec398abfea155f72c64cc96`  
		Last Modified: Fri, 12 Apr 2024 16:00:05 GMT  
		Size: 26.4 MB (26413454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240405` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dfd506bb0626da0d2b3c2b7ac631fb3652efbd1fa781fff75213eb2c7bbe642b
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31364169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc86e239e5f03573f0c9009dd87077ea94c27ae6840005fc08e42f252d28da7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:38 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:42 GMT
ADD file:a8da603c55c74defd91d533f7d8ae1989fdabaffbd1dffc9bda21c86eb06e0dd in / 
# Fri, 12 Apr 2024 15:50:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c8a56c06da37682f6872182646d36c2c9d77b6b1578a4acecf0128467910316b`  
		Last Modified: Fri, 12 Apr 2024 16:00:17 GMT  
		Size: 31.4 MB (31364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20240405` - linux; s390x

```console
$ docker pull ubuntu@sha256:fb8daccea84b4657e01ec61e5a1d9dbb75739c8096a2580f9ae1e379846feb54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f300c99459926efcebd5cacdab52ee0900534912b1c75db2556cfec826f1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2867589a33d86d4239850bd34e12ff3064467a71264788d2dd5d807347b0f1c7`  
		Last Modified: Fri, 12 Apr 2024 16:00:25 GMT  
		Size: 27.3 MB (27331928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble`

```console
$ docker pull ubuntu@sha256:5b582c80ed6832665ffb6181ab4d3e5e70c30c2548fbcea1de8a0a51f161be8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble` - linux; amd64

```console
$ docker pull ubuntu@sha256:1f84a3ed33b02bf3ccd75b06654a5dc1e0faa02b2beac4c37013859f0a26eb52
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28860028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31181e6ba2cef926292d50d592b15d745a9fb256013df363db1810e7060ab49f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e10c600007064e23f53bb653e9e837ccb78fac36df467e76704df73ffac52678`  
		Last Modified: Sun, 07 Apr 2024 17:19:05 GMT  
		Size: 28.9 MB (28860028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b1bac55096baf00b115c63c90d652bc3b61881fa892fcf907d93ac9813b94614
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26102916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab356d34f77ef44955e18cf6d2158771582951f7abef1cf8dbe21f65aa1a8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:55 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:08:04 GMT
ADD file:969299ec7ff65f7cea645f47c5b49e4d321bc39113984c894021da377f00b25a in / 
# Sun, 07 Apr 2024 17:08:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6361534ea0ef9c51acf151b33e52b03a45660ec66315943c40ec2d02634f99bc`  
		Last Modified: Sun, 07 Apr 2024 17:19:17 GMT  
		Size: 26.1 MB (26102916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b61c7c7b34921e6805388eb4cd2bd7adb40f842af583c7af8eb28d3c50e6ea97
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (27980097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daa4940cd722b5042f615f16a268ba712e96f0be896c7dd0cf9310c545a5c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:27 GMT
ADD file:517341670501a6ab8690a40210b8029b114b534a5061f599304cff1e6fd8ad07 in / 
# Sun, 07 Apr 2024 17:00:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43c7ec942a10b2818754e030a717ceb80881eef105a2efc304a3afeb2421e78c`  
		Last Modified: Sun, 07 Apr 2024 17:19:11 GMT  
		Size: 28.0 MB (27980097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:97fd25490e87e94c266c99b5a83e9d5b1be53cf6c509a9fa5b40011842814261
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33445880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b6286411794163651f4e78f7d12209bef2bb473935a52ace8a21905ffd3921`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:29 GMT
ADD file:4ed9f2ccb9342fb3acaaec8d21d9bf5029a86619c6c8878425eadc78e18003b5 in / 
# Sun, 07 Apr 2024 17:00:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8869b87a1c47aa026e7ce2df38a0a3412ebfcfe85bd377c65513aa7fc771d`  
		Last Modified: Sun, 07 Apr 2024 17:19:23 GMT  
		Size: 33.4 MB (33445880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble` - linux; s390x

```console
$ docker pull ubuntu@sha256:63c1538627e447932daae84283e194b14c6323c16a29d9bdbe071e8744c5f0b4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29113387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f38b99e0ca2a6f55155893071f008bb5b14f2d2afb0a48ded1f22e085ccfcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf319107486d1a8ff3845cc8abca0de71f7437518fe348fce75fb7db345a555`  
		Last Modified: Sun, 07 Apr 2024 17:19:30 GMT  
		Size: 29.1 MB (29113387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:noble-20240407.1`

```console
$ docker pull ubuntu@sha256:5b582c80ed6832665ffb6181ab4d3e5e70c30c2548fbcea1de8a0a51f161be8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:noble-20240407.1` - linux; amd64

```console
$ docker pull ubuntu@sha256:1f84a3ed33b02bf3ccd75b06654a5dc1e0faa02b2beac4c37013859f0a26eb52
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 MB (28860028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31181e6ba2cef926292d50d592b15d745a9fb256013df363db1810e7060ab49f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:12:58 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:12:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:12:58 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:13:00 GMT
ADD file:86e27cbcb9656cd837a2abb01bc5989043c00e9d687476bf5efddfd851228eaf in / 
# Sun, 07 Apr 2024 17:13:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e10c600007064e23f53bb653e9e837ccb78fac36df467e76704df73ffac52678`  
		Last Modified: Sun, 07 Apr 2024 17:19:05 GMT  
		Size: 28.9 MB (28860028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240407.1` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b1bac55096baf00b115c63c90d652bc3b61881fa892fcf907d93ac9813b94614
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26102916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab356d34f77ef44955e18cf6d2158771582951f7abef1cf8dbe21f65aa1a8c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:55 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:55 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:08:04 GMT
ADD file:969299ec7ff65f7cea645f47c5b49e4d321bc39113984c894021da377f00b25a in / 
# Sun, 07 Apr 2024 17:08:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6361534ea0ef9c51acf151b33e52b03a45660ec66315943c40ec2d02634f99bc`  
		Last Modified: Sun, 07 Apr 2024 17:19:17 GMT  
		Size: 26.1 MB (26102916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240407.1` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b61c7c7b34921e6805388eb4cd2bd7adb40f842af583c7af8eb28d3c50e6ea97
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (27980097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daa4940cd722b5042f615f16a268ba712e96f0be896c7dd0cf9310c545a5c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:27 GMT
ADD file:517341670501a6ab8690a40210b8029b114b534a5061f599304cff1e6fd8ad07 in / 
# Sun, 07 Apr 2024 17:00:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43c7ec942a10b2818754e030a717ceb80881eef105a2efc304a3afeb2421e78c`  
		Last Modified: Sun, 07 Apr 2024 17:19:11 GMT  
		Size: 28.0 MB (27980097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240407.1` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:97fd25490e87e94c266c99b5a83e9d5b1be53cf6c509a9fa5b40011842814261
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33445880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b6286411794163651f4e78f7d12209bef2bb473935a52ace8a21905ffd3921`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:00:25 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:00:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:00:25 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:00:29 GMT
ADD file:4ed9f2ccb9342fb3acaaec8d21d9bf5029a86619c6c8878425eadc78e18003b5 in / 
# Sun, 07 Apr 2024 17:00:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8869b87a1c47aa026e7ce2df38a0a3412ebfcfe85bd377c65513aa7fc771d`  
		Last Modified: Sun, 07 Apr 2024 17:19:23 GMT  
		Size: 33.4 MB (33445880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:noble-20240407.1` - linux; s390x

```console
$ docker pull ubuntu@sha256:63c1538627e447932daae84283e194b14c6323c16a29d9bdbe071e8744c5f0b4
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29113387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f38b99e0ca2a6f55155893071f008bb5b14f2d2afb0a48ded1f22e085ccfcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 07 Apr 2024 17:07:28 GMT
ARG RELEASE
# Sun, 07 Apr 2024 17:07:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 07 Apr 2024 17:07:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sun, 07 Apr 2024 17:07:31 GMT
ADD file:6aac414b77cc20b9f3f49047a900b0cd7688ca9aafee23883f0221ebccb250f1 in / 
# Sun, 07 Apr 2024 17:07:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dbf319107486d1a8ff3845cc8abca0de71f7437518fe348fce75fb7db345a555`  
		Last Modified: Sun, 07 Apr 2024 17:19:30 GMT  
		Size: 29.1 MB (29113387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:008c4aa50da87ad7bc586a47787491f76c79c62cc5bdbee29121ee9e02c03f3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:667a63093579bd2ffe501ff9ae68eab2674b9aa5d5b908ed59f901d57333ff49
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27233527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93816ef1ab9007d690d5e88dbb2646b371d52f27a44605fee6561519afc15d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:08 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:08 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:10 GMT
ADD file:e20f41d92fb02981d800b49f0872a5a0bc05c8b9f7dc569390c26af4b8d41caa in / 
# Fri, 12 Apr 2024 15:51:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:41771a47f3dbb290996e87044de7dcf7c3bfb29ee4259366c74b5c74a58b0354`  
		Last Modified: Fri, 12 Apr 2024 15:59:58 GMT  
		Size: 27.2 MB (27233527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d2ef4d29f07d2e34e02bd3edbecd7e97c066a5ac1eddaf726d4dab7b4fd30abd
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24887415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a6f00029030e4f1fd73079a98f46caac7940db908032c0e53a2dd347ef6fa2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:42 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:48 GMT
ADD file:7ae24dbfcd35eb56c9df6cfe135ee0660ec7885c25b732bd820de74e6e977e91 in / 
# Fri, 12 Apr 2024 15:50:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a032cb47dd8d01b6383603fb581fd99c856b139e1a013415d969e9421b6803bc`  
		Last Modified: Fri, 12 Apr 2024 16:00:11 GMT  
		Size: 24.9 MB (24887415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1e4c25185533d7bed7864744d2a5b2c43bf1ac7a7f6427267c72828712e4e16a
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26413454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7be742dd48b8ce1c5254b2f75a0f28a5ad54d5cdffe7f198217d9f11618a8f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:12 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:12 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:14 GMT
ADD file:26243ab96da01a7d087b1c824a80d95c015b3c87952acd0ff162515d17c19a31 in / 
# Fri, 12 Apr 2024 15:51:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:942a35531af124aa3c3906d47e8dd6472cec1bfa9ec398abfea155f72c64cc96`  
		Last Modified: Fri, 12 Apr 2024 16:00:05 GMT  
		Size: 26.4 MB (26413454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dfd506bb0626da0d2b3c2b7ac631fb3652efbd1fa781fff75213eb2c7bbe642b
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31364169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc86e239e5f03573f0c9009dd87077ea94c27ae6840005fc08e42f252d28da7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:50:38 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:50:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:50:38 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:50:42 GMT
ADD file:a8da603c55c74defd91d533f7d8ae1989fdabaffbd1dffc9bda21c86eb06e0dd in / 
# Fri, 12 Apr 2024 15:50:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c8a56c06da37682f6872182646d36c2c9d77b6b1578a4acecf0128467910316b`  
		Last Modified: Fri, 12 Apr 2024 16:00:17 GMT  
		Size: 31.4 MB (31364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:fb8daccea84b4657e01ec61e5a1d9dbb75739c8096a2580f9ae1e379846feb54
```

-	Docker Version: 24.0.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27331928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38f300c99459926efcebd5cacdab52ee0900534912b1c75db2556cfec826f1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Apr 2024 15:51:31 GMT
ARG RELEASE
# Fri, 12 Apr 2024 15:51:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 Apr 2024 15:51:31 GMT
LABEL org.opencontainers.image.version=23.10
# Fri, 12 Apr 2024 15:51:33 GMT
ADD file:13a7b46379c7483a76105798c32aac56ed459dca7ef015d973b0e1d68d9b7812 in / 
# Fri, 12 Apr 2024 15:51:33 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2867589a33d86d4239850bd34e12ff3064467a71264788d2dd5d807347b0f1c7`  
		Last Modified: Fri, 12 Apr 2024 16:00:25 GMT  
		Size: 27.3 MB (27331928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
