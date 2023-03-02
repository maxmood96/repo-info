<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:18.04`](#ubuntu1804)
-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:22.10`](#ubuntu2210)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:bionic`](#ubuntubionic)
-	[`ubuntu:bionic-20230301`](#ubuntubionic-20230301)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20230301`](#ubuntufocal-20230301)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20230301`](#ubuntujammy-20230301)
-	[`ubuntu:kinetic`](#ubuntukinetic)
-	[`ubuntu:kinetic-20230217`](#ubuntukinetic-20230217)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20230301`](#ubuntulunar-20230301)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:18.04`

```console
$ docker pull ubuntu@sha256:1e32b9c52e8f22769df41e8f61066c77b2b35b0a423c4161c0e48eca2fd24f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:18.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:3420178c357dc693532d8c2e592784d0c7f27ce2412cfb029bbbd618fe6ab39d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89fba62bc15f5e402dfc9e1cb0056e72d392301c324359e486d0a043286f642`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:00 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:02 GMT
ADD file:66eb2ef5574cdf80bc0cb3af1637407620c1869f58cc7514395e3f5aea45cc3b in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58289280d3c7925e901df9362a9787a557d2fdee0680e1e4251f9ae50b36cf30`  
		Last Modified: Wed, 01 Mar 2023 03:48:46 GMT  
		Size: 25.7 MB (25688299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d85f9e8f65828689ef2c9054d751a5842e870835f950d0a406e0b64988130661
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21393555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023593b1fda853a972410780b2f6e27925b41ea3cd504f278230c5c4b814eb1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:12:28 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:12:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:12:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:12:28 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:12:32 GMT
ADD file:69c0e030717df18a709c66c528354d7f774a9ec9299f6492fb8ee79990ae36ff in / 
# Wed, 01 Mar 2023 03:12:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:103c14aa01473dfa662a8cba7d45692d6fefb30485916950f6d4ec51a4b43fd7`  
		Last Modified: Wed, 01 Mar 2023 03:48:58 GMT  
		Size: 21.4 MB (21393555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:bb8a2b3669f809c4f1c2838ebe6ed71f09ab82fdfcee099c15bcfea1cd259d03
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22709684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8868b098551911a14ba29b9e4a1c228df9aa7c385ee7a125bae68d0b5343760`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b2e75c88ad8f463c4344f63d9bb4d69b8dd1f7d3655a1616c6d91c3af52406f8`  
		Last Modified: Wed, 01 Mar 2023 03:48:52 GMT  
		Size: 22.7 MB (22709684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; 386

```console
$ docker pull ubuntu@sha256:f3868102d5777e59c9b64fedb552b1a5919984e12d81dd43791c1301c947cad9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26095322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4644b1e2494da2f0c03d28912dee8906d8296c1c5534f887c761aa26f8ead9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:14:52 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:14:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:14:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:14:52 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:14:54 GMT
ADD file:765a9704b3961cee9523a98bfd0de0f97b6075431287fa7b8acd276145cb28c5 in / 
# Wed, 01 Mar 2023 03:14:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a3385078798de93a38ff616a8b809982301aafeebd0483a718563d8068e394ad`  
		Last Modified: Wed, 01 Mar 2023 03:49:04 GMT  
		Size: 26.1 MB (26095322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:3ba412c58b060771f8ef3a36eccf1805aa34df8220ccf1390987398483278dd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fc95142eb9a2fdf17beb483748fffd37108cdbc19904ba48db92163df614ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:15:24 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:15:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:15:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:15:24 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:15:27 GMT
ADD file:ca5a453351fddb6d7937e334f0331321829a5bebca3d726ef3dddad1f23b35c8 in / 
# Wed, 01 Mar 2023 03:15:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6f8d1896a16aa85108b67cccf98712456398f6d3b69d1a0a55deb6dcceb4f31`  
		Last Modified: Wed, 01 Mar 2023 03:49:10 GMT  
		Size: 29.4 MB (29350470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:b4d9005327f5f3c0ade0160e3a95526b86939fcaa6a3966fa0b43a2b05cd8f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24743962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b35062d20f1c130fa373da2a67bc10ed1deea424ca402100bea762c4719dd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d6edf86e8d4c9620690f6069a821bd0c3c7bd704ee797280f8dddcbe584fc493`  
		Last Modified: Wed, 01 Mar 2023 03:49:17 GMT  
		Size: 24.7 MB (24743962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:9fa30fcef427e5e88c76bc41ad37b7cc573e1d79cecb23035e413c4be6e476ab
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
$ docker pull ubuntu@sha256:3626dff0d616e8ee7065a9ac8c7117e904a4178725385910eeecd7f1872fc12d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27503739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c45d0e97988ff0cfa876e9ec145445974b9b384fe0a150b057ffc46039b3a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:47c7644723910b6dfc6ec8b3bd9fed3ac32778cf485ce3a6535ff6b6da06f743`  
		Last Modified: Wed, 01 Mar 2023 06:13:33 GMT  
		Size: 27.5 MB (27503739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:28fc2876b133cb5d811a82fe46a460539f75740c4db62c64cc3140f6d6e0dcfc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23608827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d751c442bab3ca91963425491fa8f6fc716f85faa9c76765afcc1e4bb284891a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:16 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:18 GMT
ADD file:e066e7492699b78467000ed6a4a902a41599ea2d7aa291332c3f76729a1e798e in / 
# Wed, 01 Mar 2023 05:41:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df492d2e5da9a55387449b81ce9a58993fdebb2b0438871000c50f7bd4645680`  
		Last Modified: Wed, 01 Mar 2023 06:13:46 GMT  
		Size: 23.6 MB (23608827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:71201a4c55f72ec33671cfcbf007689df61a13a35f028f94f8c510967dfb52e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ace790b8bce2713e1a71ecd6d34d0fd2014fdfb1298a87b8355790332c4e9c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:698acb83f45f04d40d74b0d6ee8aa8fd71ed17b0b3994faf5d7e098bdbe3c480`  
		Last Modified: Wed, 01 Mar 2023 06:13:40 GMT  
		Size: 26.0 MB (25972559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:eaa46a712883fc656ba80ca3c393fdcebfe4bd7cdd9f750c0d2abbb1242145bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afee3ea1903f271d41371b8442c67d7d97595cb4c28a32bd0bc806252587b21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5685bee6c1bb091c5d12442779aecf13111db414bcfd5b3f136a768e554b38fd`  
		Last Modified: Wed, 01 Mar 2023 06:13:52 GMT  
		Size: 32.1 MB (32068344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:6078e840ec1ac21635eb252bec15e5996aa82132bb6360718d844c26b06aac3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1847ae0c9c6235a617c81ad380d9c664f294db69915fe3a92ddc47f1c9b5ff54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0955d9ac4a1b337f2bc11dbeedde2a1eb43e1deb5c8b95b33e10fa88699770da`  
		Last Modified: Wed, 01 Mar 2023 06:13:59 GMT  
		Size: 26.4 MB (26364209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:2adf22367284330af9f832ffefb717c78239f6251d9d0f58de50b86229ed1427
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
$ docker pull ubuntu@sha256:b2175cd4cfdd5cdb1740b0e6ec6bbb4ea4892801c0ad5101a81f694152b6c559
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f2314a03de34a0a2d552b805411fc9553a02ea71c1291b815b2f645f565683`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:38:47 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:38:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:38:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:38:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:38:48 GMT
ADD file:fb4c8244f4468cdd3f666932f05805a3882d34010d3a0c14b7c20589bf619a9c in / 
# Wed, 01 Mar 2023 04:38:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:76769433fd8a87dd77a6ce33db12156b1ea8dad3da3a95e7c9c36a47ec17b24c`  
		Last Modified: Wed, 01 Mar 2023 05:41:12 GMT  
		Size: 29.5 MB (29533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ab1f462652a6753608b2199d8932dd9df78ec82869bc3b92a4b5a6c7833883b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26139593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a711451e14fc7f8ff8c5187d83e9f8d87faaf4235ce944ef4614df693f0532`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:45:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:45:58 GMT
ADD file:d8e0c2340f91ec5973c8459c1a917be69f6530fe7f88da02eb5b4dd562c31730 in / 
# Wed, 01 Mar 2023 04:45:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edaf8476df4b48455c16cb024a1d8280ec9e49c5cdfe6365d94e06833719f11c`  
		Last Modified: Wed, 01 Mar 2023 05:41:35 GMT  
		Size: 26.1 MB (26139593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b885cc8d4c735d3f407f4318c7ba917f4d95e90599238b25705fa0052490216e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730eeb702b69e53ae1c79541a48af6303d1bd240014dc6b4208ee4f3fab7b681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:47:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:48:01 GMT
ADD file:cf91de9ab30abab112d58c0a7f3bbb35853a02b2e406c65c89430ff049573c47 in / 
# Wed, 01 Mar 2023 04:48:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0a4bfa485d176c141f6b88493559f4802a12bdeb8249869bfc276bc48a3db35`  
		Last Modified: Wed, 01 Mar 2023 05:41:24 GMT  
		Size: 27.3 MB (27347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e16a2cbc79944bdc4ba343cb4c8122b2df63ea1ed9ff3d7d1b68e69de10839a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34593768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0839ad886190c004a34269c256fee12363dbdeca9a6bb037f641189d3671d98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:09:57 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:09:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:09:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:09:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:01 GMT
ADD file:e4d45fbda8cf3ca1613a11d2b929670e0e12b43c66818636afa9ebcbf6b48b59 in / 
# Wed, 01 Mar 2023 05:10:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:477676dacb828b00e0bd0791d7b4ff0c78a073d6945e495f12acfe6df21390ac`  
		Last Modified: Wed, 01 Mar 2023 05:41:42 GMT  
		Size: 34.6 MB (34593768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:5bbb1acb9a1f9fb70ab89aa70ad4ca9683719ed0d6d3a88a429c1c1c9c86b1bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28015900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b171e9c3baa3c3faca501ce7e4c65889216978c0ca1836bc1a9d9400fb71f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:10:39 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:41 GMT
ADD file:db14dc9a9d330115a6699be3c4a344f5fe366ec17e7d3649c4ecb2711605e52b in / 
# Wed, 01 Mar 2023 05:10:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:84342823b8c9656558d3661e99cb03bf0ef7d2a83280a005cac0109d6ea85e16`  
		Last Modified: Wed, 01 Mar 2023 05:41:48 GMT  
		Size: 28.0 MB (28015900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.10`

```console
$ docker pull ubuntu@sha256:699796ebf58f6d43889a7a2a29bcc8e421f8fa86bdc00d3ffededdb37e2a8d4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:22.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:3314ba73393b9a02c8e86e2222d58dcba1a3b8a996f1dae66c59504a4c8be3cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e897cc6288c30ff29bd23718aabd3886f58e1bc2b74f6cbfd74de07349471efe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:43:07 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:43:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:43:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:43:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:43:09 GMT
ADD file:18f562911635a03a9bf9e5fc22863fc2a78a64f7d35c7daa59f2d609b7ca055a in / 
# Mon, 20 Feb 2023 11:43:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:628502e7cb85e3045436055c4aeddc5025cb03ecdd44867b801ced3bf8965327`  
		Last Modified: Mon, 20 Feb 2023 12:45:30 GMT  
		Size: 26.7 MB (26691872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ed12a60343b33406c2d216ab35d3333d6649b5a563b015150ae356f6d20be58f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0852780f0a0f43310f88753ebdd3f20177833b6b2906b06643f2e4316c068a2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 12:11:32 GMT
ARG RELEASE
# Mon, 20 Feb 2023 12:11:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 12:11:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 12:11:33 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 12:11:42 GMT
ADD file:f77393d0d614b99f7ca8de09afc58a2e98d9d25c84c5ff69b50e94e7f191f7bb in / 
# Mon, 20 Feb 2023 12:11:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff79c800f3f5a313dc5958a23f5bf14d0dad7a78ab80d43874f2967135b6997d`  
		Last Modified: Mon, 20 Feb 2023 12:45:42 GMT  
		Size: 25.1 MB (25067866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a36e119b9348bea36ecbb9b9367d154b0394f83f981439a80fc5c60b916f101c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb8244935d2cd79e00e961af7901b46ba6883e2d93c9d2a9574b1b5f3862ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:58:05 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:58:05 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:58:13 GMT
ADD file:7e756337f8554849df664b30203a26f6c39dc303e277292de31fd784b9ff471b in / 
# Mon, 20 Feb 2023 11:58:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c51f53b9906df902bf049503b618304cb5d2c27813f4c2aac45122f47dc4839a`  
		Last Modified: Mon, 20 Feb 2023 12:45:36 GMT  
		Size: 25.8 MB (25757095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dd66c3f4bb116c95d45d63c67aaab4c35b66fff1b25118d707a501a59b2bff1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31109835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4732fb7042171d2c61ded8701b253ef40a74063199b2427f29e31472a5e63de4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:56:23 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:56:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:56:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:56:24 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:56:27 GMT
ADD file:541d2da8938972bd21842a8a4c8d2074a201f6f70eec4400110f90f1bc28f0e1 in / 
# Mon, 20 Feb 2023 11:56:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6acc75be9b62c9e1c43e3638dd9a71550b6564ba67797347220300fc0fa1589`  
		Last Modified: Mon, 20 Feb 2023 12:45:48 GMT  
		Size: 31.1 MB (31109835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:d1d80034b7637699302d5a6bd22c4f53f4533067106685d9696da1157b2d941b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25487269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8ebf48c4951c6350fbb1845f6b278452846c8bb7214df544863bfb1934a06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:44:03 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:44:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:44:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:44:03 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:44:05 GMT
ADD file:9d71356e3a29a835345254e233ddbd3a67941764476c2c7a5a2d0f8a61a84115 in / 
# Mon, 20 Feb 2023 11:44:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8970fa48be7fe8e052dbd1117e1ca9becfc01043da5761f540cd26091a93e34e`  
		Last Modified: Mon, 20 Feb 2023 12:45:53 GMT  
		Size: 25.5 MB (25487269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:5ecfaeaaf7b0351f7ed301e389a13a6ff04f32f6e0e5e65f700b9321913b4497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:23.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:872458e7fe2d23418707f9f1ef1a70417395ba4a2378221633b497a69c147c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26675234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303dd47d2ae803682461a7985c86fb8017a634c489171f7e479a786c6dc865f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:14 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:14 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:41:16 GMT
ADD file:a99f804e480d9a1b56aff6406b4da5a3dea89f11f968e5e02cd4ba5a25e9a7bc in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a64cfb0db31fea25d4887162ae68fabd569a4ed82352dafcf808d6b0d037e46e`  
		Last Modified: Thu, 02 Mar 2023 03:01:35 GMT  
		Size: 26.7 MB (26675234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:274be1059fafc50946027f744026dfc45b206ed0104f2f410317abb1c60c3893
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25396726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956f671980ddd2571da6ae1f4756b0fa01473ea4a33ea53434827184e482b96b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:43 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:44 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:41:53 GMT
ADD file:e4ec0e899927e1fe0388f3524f3382183df8c74bcf9de0e35e1c8120acbc2b7a in / 
# Wed, 01 Mar 2023 05:41:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3d2961b4a8d628a99bcdc6eb91e4e20621273d7b187c659a2fdfcf3f2fc221d8`  
		Last Modified: Thu, 02 Mar 2023 07:54:37 GMT  
		Size: 25.4 MB (25396726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:3a46628c3ceb56f1887c1bb5fb1674b65de4768a32e154fc76d7cf4ecfbe1457
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25942288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643303c1af72c210b87b273a0507b05c8681a451688a3d58f1286e95df6aedd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:57:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:57:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 04:57:30 GMT
ADD file:54e98f6282fdf165c9986b859ed60d05e28d3f9575c1c4915537cba24c6ec95c in / 
# Wed, 01 Mar 2023 04:57:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:21ef52b96a02ee6670b6cf0f06dcbabef72a899daf9624db7ddc45b9eef43ec6`  
		Last Modified: Thu, 02 Mar 2023 01:51:32 GMT  
		Size: 25.9 MB (25942288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:288bd3b2055364df5497ec97396bf44b3d65988d7b2eec5fdf13b9aef753acd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e83d06b82ee0806d088f2e08617e03c43c9fb3d3f30898ee5609d316f2249c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:00:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:00:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:00:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:00:58 GMT
ADD file:dd48763269678622cf7a1219a8b87a1222a24048b5cc1ab133a42cbb854c7f78 in / 
# Wed, 01 Mar 2023 05:00:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f78d61634fad56ff420a62c7b8ed593b1686185cd713fcff97e6583a72c76e87`  
		Last Modified: Thu, 02 Mar 2023 02:47:39 GMT  
		Size: 30.9 MB (30905449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:85848e3e587d544494cd2f0bc972b001d62e5a99888fbf52c6d49b87145ad154
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25539399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2a4b8ebc178b252b928a3e02d0602b8f344e3189ffbf4912c3535c68173def`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:00:55 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:00:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:00:57 GMT
ADD file:88bec1acfbc8ba8a59354ff2c1f510d9e301748628aa39527cca86d8150209e8 in / 
# Wed, 01 Mar 2023 05:00:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7998c14c928de7a493b2abed7ba03802cf44023c1fea6d4aaf5e38f26dce0222`  
		Last Modified: Thu, 02 Mar 2023 01:45:59 GMT  
		Size: 25.5 MB (25539399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:bionic`

```console
$ docker pull ubuntu@sha256:1e32b9c52e8f22769df41e8f61066c77b2b35b0a423c4161c0e48eca2fd24f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic` - linux; amd64

```console
$ docker pull ubuntu@sha256:3420178c357dc693532d8c2e592784d0c7f27ce2412cfb029bbbd618fe6ab39d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89fba62bc15f5e402dfc9e1cb0056e72d392301c324359e486d0a043286f642`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:00 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:02 GMT
ADD file:66eb2ef5574cdf80bc0cb3af1637407620c1869f58cc7514395e3f5aea45cc3b in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58289280d3c7925e901df9362a9787a557d2fdee0680e1e4251f9ae50b36cf30`  
		Last Modified: Wed, 01 Mar 2023 03:48:46 GMT  
		Size: 25.7 MB (25688299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d85f9e8f65828689ef2c9054d751a5842e870835f950d0a406e0b64988130661
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21393555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023593b1fda853a972410780b2f6e27925b41ea3cd504f278230c5c4b814eb1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:12:28 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:12:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:12:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:12:28 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:12:32 GMT
ADD file:69c0e030717df18a709c66c528354d7f774a9ec9299f6492fb8ee79990ae36ff in / 
# Wed, 01 Mar 2023 03:12:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:103c14aa01473dfa662a8cba7d45692d6fefb30485916950f6d4ec51a4b43fd7`  
		Last Modified: Wed, 01 Mar 2023 03:48:58 GMT  
		Size: 21.4 MB (21393555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:bb8a2b3669f809c4f1c2838ebe6ed71f09ab82fdfcee099c15bcfea1cd259d03
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22709684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8868b098551911a14ba29b9e4a1c228df9aa7c385ee7a125bae68d0b5343760`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b2e75c88ad8f463c4344f63d9bb4d69b8dd1f7d3655a1616c6d91c3af52406f8`  
		Last Modified: Wed, 01 Mar 2023 03:48:52 GMT  
		Size: 22.7 MB (22709684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; 386

```console
$ docker pull ubuntu@sha256:f3868102d5777e59c9b64fedb552b1a5919984e12d81dd43791c1301c947cad9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26095322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4644b1e2494da2f0c03d28912dee8906d8296c1c5534f887c761aa26f8ead9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:14:52 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:14:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:14:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:14:52 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:14:54 GMT
ADD file:765a9704b3961cee9523a98bfd0de0f97b6075431287fa7b8acd276145cb28c5 in / 
# Wed, 01 Mar 2023 03:14:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a3385078798de93a38ff616a8b809982301aafeebd0483a718563d8068e394ad`  
		Last Modified: Wed, 01 Mar 2023 03:49:04 GMT  
		Size: 26.1 MB (26095322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:3ba412c58b060771f8ef3a36eccf1805aa34df8220ccf1390987398483278dd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fc95142eb9a2fdf17beb483748fffd37108cdbc19904ba48db92163df614ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:15:24 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:15:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:15:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:15:24 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:15:27 GMT
ADD file:ca5a453351fddb6d7937e334f0331321829a5bebca3d726ef3dddad1f23b35c8 in / 
# Wed, 01 Mar 2023 03:15:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6f8d1896a16aa85108b67cccf98712456398f6d3b69d1a0a55deb6dcceb4f31`  
		Last Modified: Wed, 01 Mar 2023 03:49:10 GMT  
		Size: 29.4 MB (29350470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; s390x

```console
$ docker pull ubuntu@sha256:b4d9005327f5f3c0ade0160e3a95526b86939fcaa6a3966fa0b43a2b05cd8f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24743962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b35062d20f1c130fa373da2a67bc10ed1deea424ca402100bea762c4719dd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d6edf86e8d4c9620690f6069a821bd0c3c7bd704ee797280f8dddcbe584fc493`  
		Last Modified: Wed, 01 Mar 2023 03:49:17 GMT  
		Size: 24.7 MB (24743962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:bionic-20230301`

```console
$ docker pull ubuntu@sha256:1e32b9c52e8f22769df41e8f61066c77b2b35b0a423c4161c0e48eca2fd24f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic-20230301` - linux; amd64

```console
$ docker pull ubuntu@sha256:3420178c357dc693532d8c2e592784d0c7f27ce2412cfb029bbbd618fe6ab39d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89fba62bc15f5e402dfc9e1cb0056e72d392301c324359e486d0a043286f642`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:00 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:00 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:02 GMT
ADD file:66eb2ef5574cdf80bc0cb3af1637407620c1869f58cc7514395e3f5aea45cc3b in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:58289280d3c7925e901df9362a9787a557d2fdee0680e1e4251f9ae50b36cf30`  
		Last Modified: Wed, 01 Mar 2023 03:48:46 GMT  
		Size: 25.7 MB (25688299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230301` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:d85f9e8f65828689ef2c9054d751a5842e870835f950d0a406e0b64988130661
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21393555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023593b1fda853a972410780b2f6e27925b41ea3cd504f278230c5c4b814eb1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:12:28 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:12:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:12:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:12:28 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:12:32 GMT
ADD file:69c0e030717df18a709c66c528354d7f774a9ec9299f6492fb8ee79990ae36ff in / 
# Wed, 01 Mar 2023 03:12:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:103c14aa01473dfa662a8cba7d45692d6fefb30485916950f6d4ec51a4b43fd7`  
		Last Modified: Wed, 01 Mar 2023 03:48:58 GMT  
		Size: 21.4 MB (21393555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230301` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:bb8a2b3669f809c4f1c2838ebe6ed71f09ab82fdfcee099c15bcfea1cd259d03
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22709684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8868b098551911a14ba29b9e4a1c228df9aa7c385ee7a125bae68d0b5343760`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:17:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:17:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:17:55 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:01 GMT
ADD file:0061a9f9e2cbc9ae8577d57391acc2948389599590aa542eedf9a6b8cd0f79b0 in / 
# Wed, 01 Mar 2023 03:18:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b2e75c88ad8f463c4344f63d9bb4d69b8dd1f7d3655a1616c6d91c3af52406f8`  
		Last Modified: Wed, 01 Mar 2023 03:48:52 GMT  
		Size: 22.7 MB (22709684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230301` - linux; 386

```console
$ docker pull ubuntu@sha256:f3868102d5777e59c9b64fedb552b1a5919984e12d81dd43791c1301c947cad9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26095322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4644b1e2494da2f0c03d28912dee8906d8296c1c5534f887c761aa26f8ead9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:14:52 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:14:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:14:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:14:52 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:14:54 GMT
ADD file:765a9704b3961cee9523a98bfd0de0f97b6075431287fa7b8acd276145cb28c5 in / 
# Wed, 01 Mar 2023 03:14:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a3385078798de93a38ff616a8b809982301aafeebd0483a718563d8068e394ad`  
		Last Modified: Wed, 01 Mar 2023 03:49:04 GMT  
		Size: 26.1 MB (26095322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230301` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:3ba412c58b060771f8ef3a36eccf1805aa34df8220ccf1390987398483278dd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fc95142eb9a2fdf17beb483748fffd37108cdbc19904ba48db92163df614ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:15:24 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:15:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:15:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:15:24 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:15:27 GMT
ADD file:ca5a453351fddb6d7937e334f0331321829a5bebca3d726ef3dddad1f23b35c8 in / 
# Wed, 01 Mar 2023 03:15:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6f8d1896a16aa85108b67cccf98712456398f6d3b69d1a0a55deb6dcceb4f31`  
		Last Modified: Wed, 01 Mar 2023 03:49:10 GMT  
		Size: 29.4 MB (29350470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230301` - linux; s390x

```console
$ docker pull ubuntu@sha256:b4d9005327f5f3c0ade0160e3a95526b86939fcaa6a3966fa0b43a2b05cd8f23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24743962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b35062d20f1c130fa373da2a67bc10ed1deea424ca402100bea762c4719dd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d6edf86e8d4c9620690f6069a821bd0c3c7bd704ee797280f8dddcbe584fc493`  
		Last Modified: Wed, 01 Mar 2023 03:49:17 GMT  
		Size: 24.7 MB (24743962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:5ecfaeaaf7b0351f7ed301e389a13a6ff04f32f6e0e5e65f700b9321913b4497
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
$ docker pull ubuntu@sha256:872458e7fe2d23418707f9f1ef1a70417395ba4a2378221633b497a69c147c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26675234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303dd47d2ae803682461a7985c86fb8017a634c489171f7e479a786c6dc865f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:14 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:14 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:41:16 GMT
ADD file:a99f804e480d9a1b56aff6406b4da5a3dea89f11f968e5e02cd4ba5a25e9a7bc in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a64cfb0db31fea25d4887162ae68fabd569a4ed82352dafcf808d6b0d037e46e`  
		Last Modified: Thu, 02 Mar 2023 03:01:35 GMT  
		Size: 26.7 MB (26675234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:274be1059fafc50946027f744026dfc45b206ed0104f2f410317abb1c60c3893
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25396726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956f671980ddd2571da6ae1f4756b0fa01473ea4a33ea53434827184e482b96b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:43 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:44 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:41:53 GMT
ADD file:e4ec0e899927e1fe0388f3524f3382183df8c74bcf9de0e35e1c8120acbc2b7a in / 
# Wed, 01 Mar 2023 05:41:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3d2961b4a8d628a99bcdc6eb91e4e20621273d7b187c659a2fdfcf3f2fc221d8`  
		Last Modified: Thu, 02 Mar 2023 07:54:37 GMT  
		Size: 25.4 MB (25396726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:3a46628c3ceb56f1887c1bb5fb1674b65de4768a32e154fc76d7cf4ecfbe1457
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25942288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643303c1af72c210b87b273a0507b05c8681a451688a3d58f1286e95df6aedd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:57:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:57:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 04:57:30 GMT
ADD file:54e98f6282fdf165c9986b859ed60d05e28d3f9575c1c4915537cba24c6ec95c in / 
# Wed, 01 Mar 2023 04:57:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:21ef52b96a02ee6670b6cf0f06dcbabef72a899daf9624db7ddc45b9eef43ec6`  
		Last Modified: Thu, 02 Mar 2023 01:51:32 GMT  
		Size: 25.9 MB (25942288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:288bd3b2055364df5497ec97396bf44b3d65988d7b2eec5fdf13b9aef753acd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e83d06b82ee0806d088f2e08617e03c43c9fb3d3f30898ee5609d316f2249c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:00:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:00:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:00:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:00:58 GMT
ADD file:dd48763269678622cf7a1219a8b87a1222a24048b5cc1ab133a42cbb854c7f78 in / 
# Wed, 01 Mar 2023 05:00:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f78d61634fad56ff420a62c7b8ed593b1686185cd713fcff97e6583a72c76e87`  
		Last Modified: Thu, 02 Mar 2023 02:47:39 GMT  
		Size: 30.9 MB (30905449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:85848e3e587d544494cd2f0bc972b001d62e5a99888fbf52c6d49b87145ad154
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25539399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2a4b8ebc178b252b928a3e02d0602b8f344e3189ffbf4912c3535c68173def`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:00:55 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:00:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:00:57 GMT
ADD file:88bec1acfbc8ba8a59354ff2c1f510d9e301748628aa39527cca86d8150209e8 in / 
# Wed, 01 Mar 2023 05:00:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7998c14c928de7a493b2abed7ba03802cf44023c1fea6d4aaf5e38f26dce0222`  
		Last Modified: Thu, 02 Mar 2023 01:45:59 GMT  
		Size: 25.5 MB (25539399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:9fa30fcef427e5e88c76bc41ad37b7cc573e1d79cecb23035e413c4be6e476ab
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
$ docker pull ubuntu@sha256:3626dff0d616e8ee7065a9ac8c7117e904a4178725385910eeecd7f1872fc12d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27503739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c45d0e97988ff0cfa876e9ec145445974b9b384fe0a150b057ffc46039b3a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:47c7644723910b6dfc6ec8b3bd9fed3ac32778cf485ce3a6535ff6b6da06f743`  
		Last Modified: Wed, 01 Mar 2023 06:13:33 GMT  
		Size: 27.5 MB (27503739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:28fc2876b133cb5d811a82fe46a460539f75740c4db62c64cc3140f6d6e0dcfc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23608827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d751c442bab3ca91963425491fa8f6fc716f85faa9c76765afcc1e4bb284891a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:16 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:18 GMT
ADD file:e066e7492699b78467000ed6a4a902a41599ea2d7aa291332c3f76729a1e798e in / 
# Wed, 01 Mar 2023 05:41:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df492d2e5da9a55387449b81ce9a58993fdebb2b0438871000c50f7bd4645680`  
		Last Modified: Wed, 01 Mar 2023 06:13:46 GMT  
		Size: 23.6 MB (23608827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:71201a4c55f72ec33671cfcbf007689df61a13a35f028f94f8c510967dfb52e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ace790b8bce2713e1a71ecd6d34d0fd2014fdfb1298a87b8355790332c4e9c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:698acb83f45f04d40d74b0d6ee8aa8fd71ed17b0b3994faf5d7e098bdbe3c480`  
		Last Modified: Wed, 01 Mar 2023 06:13:40 GMT  
		Size: 26.0 MB (25972559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:eaa46a712883fc656ba80ca3c393fdcebfe4bd7cdd9f750c0d2abbb1242145bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afee3ea1903f271d41371b8442c67d7d97595cb4c28a32bd0bc806252587b21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5685bee6c1bb091c5d12442779aecf13111db414bcfd5b3f136a768e554b38fd`  
		Last Modified: Wed, 01 Mar 2023 06:13:52 GMT  
		Size: 32.1 MB (32068344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:6078e840ec1ac21635eb252bec15e5996aa82132bb6360718d844c26b06aac3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1847ae0c9c6235a617c81ad380d9c664f294db69915fe3a92ddc47f1c9b5ff54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0955d9ac4a1b337f2bc11dbeedde2a1eb43e1deb5c8b95b33e10fa88699770da`  
		Last Modified: Wed, 01 Mar 2023 06:13:59 GMT  
		Size: 26.4 MB (26364209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20230301`

```console
$ docker pull ubuntu@sha256:9fa30fcef427e5e88c76bc41ad37b7cc573e1d79cecb23035e413c4be6e476ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20230301` - linux; amd64

```console
$ docker pull ubuntu@sha256:3626dff0d616e8ee7065a9ac8c7117e904a4178725385910eeecd7f1872fc12d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27503739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c45d0e97988ff0cfa876e9ec145445974b9b384fe0a150b057ffc46039b3a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:47c7644723910b6dfc6ec8b3bd9fed3ac32778cf485ce3a6535ff6b6da06f743`  
		Last Modified: Wed, 01 Mar 2023 06:13:33 GMT  
		Size: 27.5 MB (27503739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230301` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:28fc2876b133cb5d811a82fe46a460539f75740c4db62c64cc3140f6d6e0dcfc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23608827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d751c442bab3ca91963425491fa8f6fc716f85faa9c76765afcc1e4bb284891a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:16 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:18 GMT
ADD file:e066e7492699b78467000ed6a4a902a41599ea2d7aa291332c3f76729a1e798e in / 
# Wed, 01 Mar 2023 05:41:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df492d2e5da9a55387449b81ce9a58993fdebb2b0438871000c50f7bd4645680`  
		Last Modified: Wed, 01 Mar 2023 06:13:46 GMT  
		Size: 23.6 MB (23608827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230301` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:71201a4c55f72ec33671cfcbf007689df61a13a35f028f94f8c510967dfb52e1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ace790b8bce2713e1a71ecd6d34d0fd2014fdfb1298a87b8355790332c4e9c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:698acb83f45f04d40d74b0d6ee8aa8fd71ed17b0b3994faf5d7e098bdbe3c480`  
		Last Modified: Wed, 01 Mar 2023 06:13:40 GMT  
		Size: 26.0 MB (25972559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230301` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:eaa46a712883fc656ba80ca3c393fdcebfe4bd7cdd9f750c0d2abbb1242145bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afee3ea1903f271d41371b8442c67d7d97595cb4c28a32bd0bc806252587b21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5685bee6c1bb091c5d12442779aecf13111db414bcfd5b3f136a768e554b38fd`  
		Last Modified: Wed, 01 Mar 2023 06:13:52 GMT  
		Size: 32.1 MB (32068344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230301` - linux; s390x

```console
$ docker pull ubuntu@sha256:6078e840ec1ac21635eb252bec15e5996aa82132bb6360718d844c26b06aac3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1847ae0c9c6235a617c81ad380d9c664f294db69915fe3a92ddc47f1c9b5ff54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0955d9ac4a1b337f2bc11dbeedde2a1eb43e1deb5c8b95b33e10fa88699770da`  
		Last Modified: Wed, 01 Mar 2023 06:13:59 GMT  
		Size: 26.4 MB (26364209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:2adf22367284330af9f832ffefb717c78239f6251d9d0f58de50b86229ed1427
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
$ docker pull ubuntu@sha256:b2175cd4cfdd5cdb1740b0e6ec6bbb4ea4892801c0ad5101a81f694152b6c559
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f2314a03de34a0a2d552b805411fc9553a02ea71c1291b815b2f645f565683`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:38:47 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:38:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:38:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:38:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:38:48 GMT
ADD file:fb4c8244f4468cdd3f666932f05805a3882d34010d3a0c14b7c20589bf619a9c in / 
# Wed, 01 Mar 2023 04:38:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:76769433fd8a87dd77a6ce33db12156b1ea8dad3da3a95e7c9c36a47ec17b24c`  
		Last Modified: Wed, 01 Mar 2023 05:41:12 GMT  
		Size: 29.5 MB (29533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ab1f462652a6753608b2199d8932dd9df78ec82869bc3b92a4b5a6c7833883b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26139593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a711451e14fc7f8ff8c5187d83e9f8d87faaf4235ce944ef4614df693f0532`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:45:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:45:58 GMT
ADD file:d8e0c2340f91ec5973c8459c1a917be69f6530fe7f88da02eb5b4dd562c31730 in / 
# Wed, 01 Mar 2023 04:45:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edaf8476df4b48455c16cb024a1d8280ec9e49c5cdfe6365d94e06833719f11c`  
		Last Modified: Wed, 01 Mar 2023 05:41:35 GMT  
		Size: 26.1 MB (26139593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b885cc8d4c735d3f407f4318c7ba917f4d95e90599238b25705fa0052490216e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730eeb702b69e53ae1c79541a48af6303d1bd240014dc6b4208ee4f3fab7b681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:47:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:48:01 GMT
ADD file:cf91de9ab30abab112d58c0a7f3bbb35853a02b2e406c65c89430ff049573c47 in / 
# Wed, 01 Mar 2023 04:48:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0a4bfa485d176c141f6b88493559f4802a12bdeb8249869bfc276bc48a3db35`  
		Last Modified: Wed, 01 Mar 2023 05:41:24 GMT  
		Size: 27.3 MB (27347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e16a2cbc79944bdc4ba343cb4c8122b2df63ea1ed9ff3d7d1b68e69de10839a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34593768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0839ad886190c004a34269c256fee12363dbdeca9a6bb037f641189d3671d98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:09:57 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:09:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:09:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:09:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:01 GMT
ADD file:e4d45fbda8cf3ca1613a11d2b929670e0e12b43c66818636afa9ebcbf6b48b59 in / 
# Wed, 01 Mar 2023 05:10:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:477676dacb828b00e0bd0791d7b4ff0c78a073d6945e495f12acfe6df21390ac`  
		Last Modified: Wed, 01 Mar 2023 05:41:42 GMT  
		Size: 34.6 MB (34593768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:5bbb1acb9a1f9fb70ab89aa70ad4ca9683719ed0d6d3a88a429c1c1c9c86b1bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28015900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b171e9c3baa3c3faca501ce7e4c65889216978c0ca1836bc1a9d9400fb71f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:10:39 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:41 GMT
ADD file:db14dc9a9d330115a6699be3c4a344f5fe366ec17e7d3649c4ecb2711605e52b in / 
# Wed, 01 Mar 2023 05:10:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:84342823b8c9656558d3661e99cb03bf0ef7d2a83280a005cac0109d6ea85e16`  
		Last Modified: Wed, 01 Mar 2023 05:41:48 GMT  
		Size: 28.0 MB (28015900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20230301`

```console
$ docker pull ubuntu@sha256:2adf22367284330af9f832ffefb717c78239f6251d9d0f58de50b86229ed1427
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20230301` - linux; amd64

```console
$ docker pull ubuntu@sha256:b2175cd4cfdd5cdb1740b0e6ec6bbb4ea4892801c0ad5101a81f694152b6c559
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f2314a03de34a0a2d552b805411fc9553a02ea71c1291b815b2f645f565683`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:38:47 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:38:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:38:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:38:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:38:48 GMT
ADD file:fb4c8244f4468cdd3f666932f05805a3882d34010d3a0c14b7c20589bf619a9c in / 
# Wed, 01 Mar 2023 04:38:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:76769433fd8a87dd77a6ce33db12156b1ea8dad3da3a95e7c9c36a47ec17b24c`  
		Last Modified: Wed, 01 Mar 2023 05:41:12 GMT  
		Size: 29.5 MB (29533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230301` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ab1f462652a6753608b2199d8932dd9df78ec82869bc3b92a4b5a6c7833883b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26139593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a711451e14fc7f8ff8c5187d83e9f8d87faaf4235ce944ef4614df693f0532`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:45:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:45:58 GMT
ADD file:d8e0c2340f91ec5973c8459c1a917be69f6530fe7f88da02eb5b4dd562c31730 in / 
# Wed, 01 Mar 2023 04:45:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edaf8476df4b48455c16cb024a1d8280ec9e49c5cdfe6365d94e06833719f11c`  
		Last Modified: Wed, 01 Mar 2023 05:41:35 GMT  
		Size: 26.1 MB (26139593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230301` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b885cc8d4c735d3f407f4318c7ba917f4d95e90599238b25705fa0052490216e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730eeb702b69e53ae1c79541a48af6303d1bd240014dc6b4208ee4f3fab7b681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:47:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:48:01 GMT
ADD file:cf91de9ab30abab112d58c0a7f3bbb35853a02b2e406c65c89430ff049573c47 in / 
# Wed, 01 Mar 2023 04:48:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0a4bfa485d176c141f6b88493559f4802a12bdeb8249869bfc276bc48a3db35`  
		Last Modified: Wed, 01 Mar 2023 05:41:24 GMT  
		Size: 27.3 MB (27347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230301` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e16a2cbc79944bdc4ba343cb4c8122b2df63ea1ed9ff3d7d1b68e69de10839a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34593768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0839ad886190c004a34269c256fee12363dbdeca9a6bb037f641189d3671d98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:09:57 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:09:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:09:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:09:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:01 GMT
ADD file:e4d45fbda8cf3ca1613a11d2b929670e0e12b43c66818636afa9ebcbf6b48b59 in / 
# Wed, 01 Mar 2023 05:10:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:477676dacb828b00e0bd0791d7b4ff0c78a073d6945e495f12acfe6df21390ac`  
		Last Modified: Wed, 01 Mar 2023 05:41:42 GMT  
		Size: 34.6 MB (34593768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230301` - linux; s390x

```console
$ docker pull ubuntu@sha256:5bbb1acb9a1f9fb70ab89aa70ad4ca9683719ed0d6d3a88a429c1c1c9c86b1bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28015900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b171e9c3baa3c3faca501ce7e4c65889216978c0ca1836bc1a9d9400fb71f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:10:39 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:41 GMT
ADD file:db14dc9a9d330115a6699be3c4a344f5fe366ec17e7d3649c4ecb2711605e52b in / 
# Wed, 01 Mar 2023 05:10:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:84342823b8c9656558d3661e99cb03bf0ef7d2a83280a005cac0109d6ea85e16`  
		Last Modified: Wed, 01 Mar 2023 05:41:48 GMT  
		Size: 28.0 MB (28015900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic`

```console
$ docker pull ubuntu@sha256:699796ebf58f6d43889a7a2a29bcc8e421f8fa86bdc00d3ffededdb37e2a8d4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:kinetic` - linux; amd64

```console
$ docker pull ubuntu@sha256:3314ba73393b9a02c8e86e2222d58dcba1a3b8a996f1dae66c59504a4c8be3cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e897cc6288c30ff29bd23718aabd3886f58e1bc2b74f6cbfd74de07349471efe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:43:07 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:43:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:43:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:43:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:43:09 GMT
ADD file:18f562911635a03a9bf9e5fc22863fc2a78a64f7d35c7daa59f2d609b7ca055a in / 
# Mon, 20 Feb 2023 11:43:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:628502e7cb85e3045436055c4aeddc5025cb03ecdd44867b801ced3bf8965327`  
		Last Modified: Mon, 20 Feb 2023 12:45:30 GMT  
		Size: 26.7 MB (26691872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ed12a60343b33406c2d216ab35d3333d6649b5a563b015150ae356f6d20be58f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0852780f0a0f43310f88753ebdd3f20177833b6b2906b06643f2e4316c068a2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 12:11:32 GMT
ARG RELEASE
# Mon, 20 Feb 2023 12:11:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 12:11:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 12:11:33 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 12:11:42 GMT
ADD file:f77393d0d614b99f7ca8de09afc58a2e98d9d25c84c5ff69b50e94e7f191f7bb in / 
# Mon, 20 Feb 2023 12:11:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff79c800f3f5a313dc5958a23f5bf14d0dad7a78ab80d43874f2967135b6997d`  
		Last Modified: Mon, 20 Feb 2023 12:45:42 GMT  
		Size: 25.1 MB (25067866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a36e119b9348bea36ecbb9b9367d154b0394f83f981439a80fc5c60b916f101c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb8244935d2cd79e00e961af7901b46ba6883e2d93c9d2a9574b1b5f3862ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:58:05 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:58:05 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:58:13 GMT
ADD file:7e756337f8554849df664b30203a26f6c39dc303e277292de31fd784b9ff471b in / 
# Mon, 20 Feb 2023 11:58:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c51f53b9906df902bf049503b618304cb5d2c27813f4c2aac45122f47dc4839a`  
		Last Modified: Mon, 20 Feb 2023 12:45:36 GMT  
		Size: 25.8 MB (25757095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dd66c3f4bb116c95d45d63c67aaab4c35b66fff1b25118d707a501a59b2bff1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31109835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4732fb7042171d2c61ded8701b253ef40a74063199b2427f29e31472a5e63de4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:56:23 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:56:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:56:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:56:24 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:56:27 GMT
ADD file:541d2da8938972bd21842a8a4c8d2074a201f6f70eec4400110f90f1bc28f0e1 in / 
# Mon, 20 Feb 2023 11:56:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6acc75be9b62c9e1c43e3638dd9a71550b6564ba67797347220300fc0fa1589`  
		Last Modified: Mon, 20 Feb 2023 12:45:48 GMT  
		Size: 31.1 MB (31109835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; s390x

```console
$ docker pull ubuntu@sha256:d1d80034b7637699302d5a6bd22c4f53f4533067106685d9696da1157b2d941b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25487269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8ebf48c4951c6350fbb1845f6b278452846c8bb7214df544863bfb1934a06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:44:03 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:44:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:44:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:44:03 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:44:05 GMT
ADD file:9d71356e3a29a835345254e233ddbd3a67941764476c2c7a5a2d0f8a61a84115 in / 
# Mon, 20 Feb 2023 11:44:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8970fa48be7fe8e052dbd1117e1ca9becfc01043da5761f540cd26091a93e34e`  
		Last Modified: Mon, 20 Feb 2023 12:45:53 GMT  
		Size: 25.5 MB (25487269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic-20230217`

```console
$ docker pull ubuntu@sha256:699796ebf58f6d43889a7a2a29bcc8e421f8fa86bdc00d3ffededdb37e2a8d4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:kinetic-20230217` - linux; amd64

```console
$ docker pull ubuntu@sha256:3314ba73393b9a02c8e86e2222d58dcba1a3b8a996f1dae66c59504a4c8be3cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e897cc6288c30ff29bd23718aabd3886f58e1bc2b74f6cbfd74de07349471efe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:43:07 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:43:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:43:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:43:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:43:09 GMT
ADD file:18f562911635a03a9bf9e5fc22863fc2a78a64f7d35c7daa59f2d609b7ca055a in / 
# Mon, 20 Feb 2023 11:43:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:628502e7cb85e3045436055c4aeddc5025cb03ecdd44867b801ced3bf8965327`  
		Last Modified: Mon, 20 Feb 2023 12:45:30 GMT  
		Size: 26.7 MB (26691872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230217` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ed12a60343b33406c2d216ab35d3333d6649b5a563b015150ae356f6d20be58f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0852780f0a0f43310f88753ebdd3f20177833b6b2906b06643f2e4316c068a2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 12:11:32 GMT
ARG RELEASE
# Mon, 20 Feb 2023 12:11:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 12:11:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 12:11:33 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 12:11:42 GMT
ADD file:f77393d0d614b99f7ca8de09afc58a2e98d9d25c84c5ff69b50e94e7f191f7bb in / 
# Mon, 20 Feb 2023 12:11:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff79c800f3f5a313dc5958a23f5bf14d0dad7a78ab80d43874f2967135b6997d`  
		Last Modified: Mon, 20 Feb 2023 12:45:42 GMT  
		Size: 25.1 MB (25067866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230217` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a36e119b9348bea36ecbb9b9367d154b0394f83f981439a80fc5c60b916f101c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb8244935d2cd79e00e961af7901b46ba6883e2d93c9d2a9574b1b5f3862ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:58:05 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:58:05 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:58:13 GMT
ADD file:7e756337f8554849df664b30203a26f6c39dc303e277292de31fd784b9ff471b in / 
# Mon, 20 Feb 2023 11:58:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c51f53b9906df902bf049503b618304cb5d2c27813f4c2aac45122f47dc4839a`  
		Last Modified: Mon, 20 Feb 2023 12:45:36 GMT  
		Size: 25.8 MB (25757095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230217` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dd66c3f4bb116c95d45d63c67aaab4c35b66fff1b25118d707a501a59b2bff1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31109835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4732fb7042171d2c61ded8701b253ef40a74063199b2427f29e31472a5e63de4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:56:23 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:56:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:56:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:56:24 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:56:27 GMT
ADD file:541d2da8938972bd21842a8a4c8d2074a201f6f70eec4400110f90f1bc28f0e1 in / 
# Mon, 20 Feb 2023 11:56:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6acc75be9b62c9e1c43e3638dd9a71550b6564ba67797347220300fc0fa1589`  
		Last Modified: Mon, 20 Feb 2023 12:45:48 GMT  
		Size: 31.1 MB (31109835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230217` - linux; s390x

```console
$ docker pull ubuntu@sha256:d1d80034b7637699302d5a6bd22c4f53f4533067106685d9696da1157b2d941b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25487269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8ebf48c4951c6350fbb1845f6b278452846c8bb7214df544863bfb1934a06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:44:03 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:44:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:44:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:44:03 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:44:05 GMT
ADD file:9d71356e3a29a835345254e233ddbd3a67941764476c2c7a5a2d0f8a61a84115 in / 
# Mon, 20 Feb 2023 11:44:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8970fa48be7fe8e052dbd1117e1ca9becfc01043da5761f540cd26091a93e34e`  
		Last Modified: Mon, 20 Feb 2023 12:45:53 GMT  
		Size: 25.5 MB (25487269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:2adf22367284330af9f832ffefb717c78239f6251d9d0f58de50b86229ed1427
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
$ docker pull ubuntu@sha256:b2175cd4cfdd5cdb1740b0e6ec6bbb4ea4892801c0ad5101a81f694152b6c559
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f2314a03de34a0a2d552b805411fc9553a02ea71c1291b815b2f645f565683`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:38:47 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:38:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:38:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:38:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:38:48 GMT
ADD file:fb4c8244f4468cdd3f666932f05805a3882d34010d3a0c14b7c20589bf619a9c in / 
# Wed, 01 Mar 2023 04:38:49 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:76769433fd8a87dd77a6ce33db12156b1ea8dad3da3a95e7c9c36a47ec17b24c`  
		Last Modified: Wed, 01 Mar 2023 05:41:12 GMT  
		Size: 29.5 MB (29533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ab1f462652a6753608b2199d8932dd9df78ec82869bc3b92a4b5a6c7833883b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26139593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a711451e14fc7f8ff8c5187d83e9f8d87faaf4235ce944ef4614df693f0532`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:45:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:45:58 GMT
ADD file:d8e0c2340f91ec5973c8459c1a917be69f6530fe7f88da02eb5b4dd562c31730 in / 
# Wed, 01 Mar 2023 04:45:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:edaf8476df4b48455c16cb024a1d8280ec9e49c5cdfe6365d94e06833719f11c`  
		Last Modified: Wed, 01 Mar 2023 05:41:35 GMT  
		Size: 26.1 MB (26139593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b885cc8d4c735d3f407f4318c7ba917f4d95e90599238b25705fa0052490216e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27347794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730eeb702b69e53ae1c79541a48af6303d1bd240014dc6b4208ee4f3fab7b681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:47:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:47:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 04:48:01 GMT
ADD file:cf91de9ab30abab112d58c0a7f3bbb35853a02b2e406c65c89430ff049573c47 in / 
# Wed, 01 Mar 2023 04:48:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d0a4bfa485d176c141f6b88493559f4802a12bdeb8249869bfc276bc48a3db35`  
		Last Modified: Wed, 01 Mar 2023 05:41:24 GMT  
		Size: 27.3 MB (27347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:e16a2cbc79944bdc4ba343cb4c8122b2df63ea1ed9ff3d7d1b68e69de10839a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34593768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0839ad886190c004a34269c256fee12363dbdeca9a6bb037f641189d3671d98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:09:57 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:09:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:09:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:09:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:01 GMT
ADD file:e4d45fbda8cf3ca1613a11d2b929670e0e12b43c66818636afa9ebcbf6b48b59 in / 
# Wed, 01 Mar 2023 05:10:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:477676dacb828b00e0bd0791d7b4ff0c78a073d6945e495f12acfe6df21390ac`  
		Last Modified: Wed, 01 Mar 2023 05:41:42 GMT  
		Size: 34.6 MB (34593768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:5bbb1acb9a1f9fb70ab89aa70ad4ca9683719ed0d6d3a88a429c1c1c9c86b1bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28015900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b171e9c3baa3c3faca501ce7e4c65889216978c0ca1836bc1a9d9400fb71f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:10:39 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:10:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:10:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Mar 2023 05:10:41 GMT
ADD file:db14dc9a9d330115a6699be3c4a344f5fe366ec17e7d3649c4ecb2711605e52b in / 
# Wed, 01 Mar 2023 05:10:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:84342823b8c9656558d3661e99cb03bf0ef7d2a83280a005cac0109d6ea85e16`  
		Last Modified: Wed, 01 Mar 2023 05:41:48 GMT  
		Size: 28.0 MB (28015900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:5ecfaeaaf7b0351f7ed301e389a13a6ff04f32f6e0e5e65f700b9321913b4497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar` - linux; amd64

```console
$ docker pull ubuntu@sha256:872458e7fe2d23418707f9f1ef1a70417395ba4a2378221633b497a69c147c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26675234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303dd47d2ae803682461a7985c86fb8017a634c489171f7e479a786c6dc865f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:14 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:14 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:41:16 GMT
ADD file:a99f804e480d9a1b56aff6406b4da5a3dea89f11f968e5e02cd4ba5a25e9a7bc in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a64cfb0db31fea25d4887162ae68fabd569a4ed82352dafcf808d6b0d037e46e`  
		Last Modified: Thu, 02 Mar 2023 03:01:35 GMT  
		Size: 26.7 MB (26675234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:274be1059fafc50946027f744026dfc45b206ed0104f2f410317abb1c60c3893
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25396726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956f671980ddd2571da6ae1f4756b0fa01473ea4a33ea53434827184e482b96b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:43 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:44 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:41:53 GMT
ADD file:e4ec0e899927e1fe0388f3524f3382183df8c74bcf9de0e35e1c8120acbc2b7a in / 
# Wed, 01 Mar 2023 05:41:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3d2961b4a8d628a99bcdc6eb91e4e20621273d7b187c659a2fdfcf3f2fc221d8`  
		Last Modified: Thu, 02 Mar 2023 07:54:37 GMT  
		Size: 25.4 MB (25396726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:3a46628c3ceb56f1887c1bb5fb1674b65de4768a32e154fc76d7cf4ecfbe1457
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25942288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643303c1af72c210b87b273a0507b05c8681a451688a3d58f1286e95df6aedd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:57:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:57:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 04:57:30 GMT
ADD file:54e98f6282fdf165c9986b859ed60d05e28d3f9575c1c4915537cba24c6ec95c in / 
# Wed, 01 Mar 2023 04:57:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:21ef52b96a02ee6670b6cf0f06dcbabef72a899daf9624db7ddc45b9eef43ec6`  
		Last Modified: Thu, 02 Mar 2023 01:51:32 GMT  
		Size: 25.9 MB (25942288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:288bd3b2055364df5497ec97396bf44b3d65988d7b2eec5fdf13b9aef753acd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e83d06b82ee0806d088f2e08617e03c43c9fb3d3f30898ee5609d316f2249c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:00:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:00:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:00:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:00:58 GMT
ADD file:dd48763269678622cf7a1219a8b87a1222a24048b5cc1ab133a42cbb854c7f78 in / 
# Wed, 01 Mar 2023 05:00:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f78d61634fad56ff420a62c7b8ed593b1686185cd713fcff97e6583a72c76e87`  
		Last Modified: Thu, 02 Mar 2023 02:47:39 GMT  
		Size: 30.9 MB (30905449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; s390x

```console
$ docker pull ubuntu@sha256:85848e3e587d544494cd2f0bc972b001d62e5a99888fbf52c6d49b87145ad154
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25539399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2a4b8ebc178b252b928a3e02d0602b8f344e3189ffbf4912c3535c68173def`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:00:55 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:00:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:00:57 GMT
ADD file:88bec1acfbc8ba8a59354ff2c1f510d9e301748628aa39527cca86d8150209e8 in / 
# Wed, 01 Mar 2023 05:00:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7998c14c928de7a493b2abed7ba03802cf44023c1fea6d4aaf5e38f26dce0222`  
		Last Modified: Thu, 02 Mar 2023 01:45:59 GMT  
		Size: 25.5 MB (25539399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar-20230301`

```console
$ docker pull ubuntu@sha256:5ecfaeaaf7b0351f7ed301e389a13a6ff04f32f6e0e5e65f700b9321913b4497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar-20230301` - linux; amd64

```console
$ docker pull ubuntu@sha256:872458e7fe2d23418707f9f1ef1a70417395ba4a2378221633b497a69c147c0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26675234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303dd47d2ae803682461a7985c86fb8017a634c489171f7e479a786c6dc865f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:14 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:14 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:41:16 GMT
ADD file:a99f804e480d9a1b56aff6406b4da5a3dea89f11f968e5e02cd4ba5a25e9a7bc in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a64cfb0db31fea25d4887162ae68fabd569a4ed82352dafcf808d6b0d037e46e`  
		Last Modified: Thu, 02 Mar 2023 03:01:35 GMT  
		Size: 26.7 MB (26675234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230301` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:274be1059fafc50946027f744026dfc45b206ed0104f2f410317abb1c60c3893
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25396726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956f671980ddd2571da6ae1f4756b0fa01473ea4a33ea53434827184e482b96b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:43 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:44 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:41:53 GMT
ADD file:e4ec0e899927e1fe0388f3524f3382183df8c74bcf9de0e35e1c8120acbc2b7a in / 
# Wed, 01 Mar 2023 05:41:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3d2961b4a8d628a99bcdc6eb91e4e20621273d7b187c659a2fdfcf3f2fc221d8`  
		Last Modified: Thu, 02 Mar 2023 07:54:37 GMT  
		Size: 25.4 MB (25396726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230301` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:3a46628c3ceb56f1887c1bb5fb1674b65de4768a32e154fc76d7cf4ecfbe1457
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25942288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643303c1af72c210b87b273a0507b05c8681a451688a3d58f1286e95df6aedd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:57:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:57:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:57:22 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 04:57:30 GMT
ADD file:54e98f6282fdf165c9986b859ed60d05e28d3f9575c1c4915537cba24c6ec95c in / 
# Wed, 01 Mar 2023 04:57:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:21ef52b96a02ee6670b6cf0f06dcbabef72a899daf9624db7ddc45b9eef43ec6`  
		Last Modified: Thu, 02 Mar 2023 01:51:32 GMT  
		Size: 25.9 MB (25942288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230301` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:288bd3b2055364df5497ec97396bf44b3d65988d7b2eec5fdf13b9aef753acd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30905449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e83d06b82ee0806d088f2e08617e03c43c9fb3d3f30898ee5609d316f2249c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:00:54 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:00:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:00:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:00:58 GMT
ADD file:dd48763269678622cf7a1219a8b87a1222a24048b5cc1ab133a42cbb854c7f78 in / 
# Wed, 01 Mar 2023 05:00:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f78d61634fad56ff420a62c7b8ed593b1686185cd713fcff97e6583a72c76e87`  
		Last Modified: Thu, 02 Mar 2023 02:47:39 GMT  
		Size: 30.9 MB (30905449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230301` - linux; s390x

```console
$ docker pull ubuntu@sha256:85848e3e587d544494cd2f0bc972b001d62e5a99888fbf52c6d49b87145ad154
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25539399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2a4b8ebc178b252b928a3e02d0602b8f344e3189ffbf4912c3535c68173def`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 05:00:55 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:00:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:00:55 GMT
LABEL org.opencontainers.image.version=23.04
# Wed, 01 Mar 2023 05:00:57 GMT
ADD file:88bec1acfbc8ba8a59354ff2c1f510d9e301748628aa39527cca86d8150209e8 in / 
# Wed, 01 Mar 2023 05:00:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7998c14c928de7a493b2abed7ba03802cf44023c1fea6d4aaf5e38f26dce0222`  
		Last Modified: Thu, 02 Mar 2023 01:45:59 GMT  
		Size: 25.5 MB (25539399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:699796ebf58f6d43889a7a2a29bcc8e421f8fa86bdc00d3ffededdb37e2a8d4c
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
$ docker pull ubuntu@sha256:3314ba73393b9a02c8e86e2222d58dcba1a3b8a996f1dae66c59504a4c8be3cd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e897cc6288c30ff29bd23718aabd3886f58e1bc2b74f6cbfd74de07349471efe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:43:07 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:43:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:43:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:43:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:43:09 GMT
ADD file:18f562911635a03a9bf9e5fc22863fc2a78a64f7d35c7daa59f2d609b7ca055a in / 
# Mon, 20 Feb 2023 11:43:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:628502e7cb85e3045436055c4aeddc5025cb03ecdd44867b801ced3bf8965327`  
		Last Modified: Mon, 20 Feb 2023 12:45:30 GMT  
		Size: 26.7 MB (26691872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:ed12a60343b33406c2d216ab35d3333d6649b5a563b015150ae356f6d20be58f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0852780f0a0f43310f88753ebdd3f20177833b6b2906b06643f2e4316c068a2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 12:11:32 GMT
ARG RELEASE
# Mon, 20 Feb 2023 12:11:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 12:11:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 12:11:33 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 12:11:42 GMT
ADD file:f77393d0d614b99f7ca8de09afc58a2e98d9d25c84c5ff69b50e94e7f191f7bb in / 
# Mon, 20 Feb 2023 12:11:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ff79c800f3f5a313dc5958a23f5bf14d0dad7a78ab80d43874f2967135b6997d`  
		Last Modified: Mon, 20 Feb 2023 12:45:42 GMT  
		Size: 25.1 MB (25067866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:a36e119b9348bea36ecbb9b9367d154b0394f83f981439a80fc5c60b916f101c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25757095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb8244935d2cd79e00e961af7901b46ba6883e2d93c9d2a9574b1b5f3862ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:58:05 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:58:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:58:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:58:05 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:58:13 GMT
ADD file:7e756337f8554849df664b30203a26f6c39dc303e277292de31fd784b9ff471b in / 
# Mon, 20 Feb 2023 11:58:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c51f53b9906df902bf049503b618304cb5d2c27813f4c2aac45122f47dc4839a`  
		Last Modified: Mon, 20 Feb 2023 12:45:36 GMT  
		Size: 25.8 MB (25757095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dd66c3f4bb116c95d45d63c67aaab4c35b66fff1b25118d707a501a59b2bff1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31109835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4732fb7042171d2c61ded8701b253ef40a74063199b2427f29e31472a5e63de4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:56:23 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:56:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:56:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:56:24 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:56:27 GMT
ADD file:541d2da8938972bd21842a8a4c8d2074a201f6f70eec4400110f90f1bc28f0e1 in / 
# Mon, 20 Feb 2023 11:56:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6acc75be9b62c9e1c43e3638dd9a71550b6564ba67797347220300fc0fa1589`  
		Last Modified: Mon, 20 Feb 2023 12:45:48 GMT  
		Size: 31.1 MB (31109835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:d1d80034b7637699302d5a6bd22c4f53f4533067106685d9696da1157b2d941b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25487269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8ebf48c4951c6350fbb1845f6b278452846c8bb7214df544863bfb1934a06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 20 Feb 2023 11:44:03 GMT
ARG RELEASE
# Mon, 20 Feb 2023 11:44:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Feb 2023 11:44:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Feb 2023 11:44:03 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 20 Feb 2023 11:44:05 GMT
ADD file:9d71356e3a29a835345254e233ddbd3a67941764476c2c7a5a2d0f8a61a84115 in / 
# Mon, 20 Feb 2023 11:44:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8970fa48be7fe8e052dbd1117e1ca9becfc01043da5761f540cd26091a93e34e`  
		Last Modified: Mon, 20 Feb 2023 12:45:53 GMT  
		Size: 25.5 MB (25487269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
