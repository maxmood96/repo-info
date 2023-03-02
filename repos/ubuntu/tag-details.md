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
$ docker pull ubuntu@sha256:eb25b45bdceafdab343223bb76a5cd5c2491c6ac666d0dfa69530a87b06b8500
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
$ docker pull ubuntu@sha256:fdd3c9372c19afa928f99afde58f0f80a008ebb695a8c5ee37de5adb7feb46de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2df19066aca89df8e5317544a1cb599dc657830184762ff6fdefaaf708db65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:72d9f18d70f395ff9bfae4d193077ccea3ca583e3da3dd66f5c84520c0100727`  
		Last Modified: Thu, 26 Jan 2023 10:11:57 GMT  
		Size: 25.7 MB (25688613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f21972d048d5439834187f47e9e2869e5434a3c5d49f7ef721d3d5f62fe7de60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21395113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17e780dbbcb4f0f3439981b5f09c45d9de103ca383942edbb8842911f2402fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:56:13 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:56:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:56:18 GMT
ADD file:1cc75b54b9c4d0824203532d4bb0eea2aaeafed003e37057b21aa3713b6bb0ea in / 
# Thu, 26 Jan 2023 09:56:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c138257d410403a2127c08e269ac8467b8f2001b22a102934861b65b2f49bc1a`  
		Last Modified: Thu, 26 Jan 2023 10:12:17 GMT  
		Size: 21.4 MB (21395113 bytes)  
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
$ docker pull ubuntu@sha256:fcebd6734dcbffd0c328771b11a0d00a8045f58ee5d3e083d3afdb54c72dab8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26096513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97151d96f64f3b5b7cdb0fadb1c1f8556552cedf32154f23efd48595efabb1e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:57a4d5aed2cd4a1f596f693a8fe5e135bd66dbf401ec169b1848d2316bdcfb2c`  
		Last Modified: Thu, 26 Jan 2023 10:12:23 GMT  
		Size: 26.1 MB (26096513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:da6bd15c918442485ea09b9b4a679ccddef764b03c04a94fa2f0ee75bf9ae709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29351018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e533a2e815a6606d93392dd9f8ff6938a39080b67cfd575045cfe820ede7af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c790564dfb49a61552a6e89c63c7abf84177d16d0f0fb604df022bfcdc6497b`  
		Last Modified: Thu, 26 Jan 2023 10:12:31 GMT  
		Size: 29.4 MB (29351018 bytes)  
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
$ docker pull ubuntu@sha256:de3911cdfaf1376a963a0ca6e72e86c456b268d269bd24fd741725fb2a2ca4be
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
$ docker pull ubuntu@sha256:bffb6799d706144f263f4b91e1226745ffb5643ea0ea89c2f709208e8d70c999
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27503418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40cf56b4be35b04f620bc9cfbef80038fd7370d4ed36d90676223174ecbf0b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b549f31133a955f68f9fa0d93f18436c4a180e12184b999a8ecf14f7eaa83309`  
		Last Modified: Wed, 01 Feb 2023 12:05:25 GMT  
		Size: 27.5 MB (27503418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7bb60f92af1f5062f83b4b0edd5710332e20e1f99ae6c294d8b5bd7d7551a41b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23608452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2238f5e875d6e7d6f10729c620de133ae54eb25518994fcf012e02df6ec9e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:28:35 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:28:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:28:43 GMT
ADD file:6566d63937dd1808d3a4ea5591d4369b9083772d48fad60626fb91243a9f3f53 in / 
# Wed, 01 Feb 2023 11:28:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:363362dbf1847a398cc45b6a5f85ddbc7c633b43b9120f06e1e8cdd10237325a`  
		Last Modified: Wed, 01 Feb 2023 12:05:37 GMT  
		Size: 23.6 MB (23608452 bytes)  
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
$ docker pull ubuntu@sha256:e66e5d8f6f3761ce46b82a167ec4b091e87f0e0902d302b4fb9781f421e9ad23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a648e725100f70f48b2ca60e75e69b4b5e2a7a9abbceba82f43764bc32ca9df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:210cd7d37ec304813e8c7a2036ca7ca250cda0516fe48a4139b60c4cb817eaaf`  
		Last Modified: Wed, 01 Feb 2023 12:05:43 GMT  
		Size: 32.1 MB (32068234 bytes)  
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
$ docker pull ubuntu@sha256:dad0b9789498ed3cf6c7b3ea3183d7565502d5301751044ccee1d8139a580c07
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
$ docker pull ubuntu@sha256:c985bc3f77946b8e92c9a3648c6f31751a7dd972e06604785e47303f4ad47c4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29528717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58db3edaf2be6e80f628796355b1bdeaf8bea1692b402f48b7e7b8d1ff100b02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:677076032cca0a2362d25cf3660072e738d1b96fe860409a33ce901d695d7ee8`  
		Last Modified: Thu, 26 Jan 2023 05:13:54 GMT  
		Size: 29.5 MB (29528717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7f1627151f895be9f4805b8a092f0d17a3365c142c95d44f9c857fc891172fa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26137949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b861da44337925963eb70b8671950999df7d8abfe7f5a9b5f95ff9f4cca7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:40 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:43 GMT
ADD file:12d2a7ddc8445b8f97c960075216eb8e8cd226b84259c7343ef15c65a440b500 in / 
# Thu, 26 Jan 2023 05:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:860e874323ae800886f85ab5c346783e3a9371bd9beb72c5f25e8e20c9dd18bb`  
		Last Modified: Thu, 26 Jan 2023 05:14:09 GMT  
		Size: 26.1 MB (26137949 bytes)  
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
$ docker pull ubuntu@sha256:9ff892e66bc925cfcde0f1007bc1813f2d6c73b90c2681b1f1e35c39678f93fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34588568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d899338973bac5fb325b647c7436507e44918374fff2a72b0da6515946c868a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:58:24 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:58:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:28 GMT
ADD file:f0400001a50847feb579e66e804ec9daaaaeb9a414b4b5cca8bb0c8e9c7fa8f9 in / 
# Thu, 26 Jan 2023 04:58:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:717e115780fa5a198871a9eef15e446084728bf7021e7894e6118f3cd6d26b60`  
		Last Modified: Thu, 26 Jan 2023 05:14:15 GMT  
		Size: 34.6 MB (34588568 bytes)  
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
$ docker pull ubuntu@sha256:a2626d53b5a5e8e7f73664beb605525f300cc9a203b5efef5583cae8560a183a
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
$ docker pull ubuntu@sha256:535c4a5ab0c2937593fb6aa241d9996f6eed02b8598928aa289ffd0416561131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c2f4041af137e6b0ba5c793df3dfdf4e72a4e011ce6847f4cc0247b9bbf7f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:51:12 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:51:13 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:51:14 GMT
ADD file:e886423892b371751386c0ce7147599acb72d8fb528eaaa78092b879d9ff58ce in / 
# Thu, 26 Jan 2023 11:51:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:256644d5a307c3efeca6ae2854b6329a2753157868dc5548e33161b377658e6a`  
		Last Modified: Thu, 26 Jan 2023 12:14:04 GMT  
		Size: 26.7 MB (26691650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b44ef81c8e6d1bd305cc72000c972fcd255a0b3f3bfe4dec81f651a53c8eeb89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25066997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d643d5974c30c06b1d811877a3a8f0047c4278b1fe0801d8d812b3a17ce6c15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:52:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:52:03 GMT
ADD file:d35c57b0dc2840a8b1ef40f7f6cfd826da68611f1ba37a89a382618c8612b52c in / 
# Thu, 26 Jan 2023 11:52:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:697d38f8dfe625e3e751c0b01ddeaaeeff6e8d6f594dd7da227aea3974a49ce1`  
		Last Modified: Thu, 26 Jan 2023 12:14:16 GMT  
		Size: 25.1 MB (25066997 bytes)  
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
$ docker pull ubuntu@sha256:7a248a581d0b98a906b2ba67277834f2613d35179f91872152a7776a81f6c2d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfbc0b60efcd8ea2a51c157e7bc286d8de7e88ae1bf756e0d8a44ff107e21c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:57:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:57:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:57:03 GMT
ADD file:3c2bc98d283cce5149d7992233f5fe644b7239417045faf3f93750b92de5f68e in / 
# Thu, 26 Jan 2023 11:57:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8da618ff876e10064f550b9dc5b51b0d0ae6939f67b56ce9a0c7fa8bb77de40f`  
		Last Modified: Thu, 26 Jan 2023 12:14:22 GMT  
		Size: 31.1 MB (31110147 bytes)  
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
$ docker pull ubuntu@sha256:cb91157e87db4be7e2fc86ff0dfc49adc1bff1d418db19d0627ae5c326938954
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
$ docker pull ubuntu@sha256:52293638ba652a2e8f9e1c1cfcc905839b1f2a9e671ddcc9bf77909b6bf527d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb2152822b716b4deac2996f16bc84db0a14b7cbc549579635590438f9c0e1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:15:52 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:15:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:15:54 GMT
ADD file:915f1a27db0a8b9a9dd58d40086cb7d45b2722e8ceb29ed8bcb306d4dcd3688e in / 
# Sat, 28 Jan 2023 05:15:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db781b8aed497363312ef32499cbfac28821e0494db7f0cadc4e716853e02a12`  
		Last Modified: Sat, 28 Jan 2023 05:21:25 GMT  
		Size: 26.6 MB (26638886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9fbac10f6899f18c2a614e0d7dc2a38af1559e5f0995d3b70bd8c1d57401ff76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25086001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173233681dc2cf6e3fa1246e9ee30ffdbd026b650b163a584cdf76d6b3ae773f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:25 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:31 GMT
ADD file:c0ac354f01ba9deb72bda06f4368650e0cc3ad5c3425ce0eb452561b56a1734a in / 
# Sat, 28 Jan 2023 05:11:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2cf733a376b355703d852c37fb66314a9d27adeb140641f229bd7d5b089c8ef7`  
		Last Modified: Sat, 28 Jan 2023 05:21:37 GMT  
		Size: 25.1 MB (25086001 bytes)  
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
$ docker pull ubuntu@sha256:a8498f0e21515679ba0037a81a4ab642c1d95710be8559a451c53df1d796fe06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30996511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3034f502162557a76be48b558db7cd107c03e20d4ce61ae3773374acca05b38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:09:15 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:09:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:09:19 GMT
ADD file:1c6ae50eb1e182a9aa8f750f61a615d5b3578b7c2f94e58678359bf1f43d3780 in / 
# Sat, 28 Jan 2023 05:09:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b536935eabb902676d3f03adcea225b24ae7144948054cd9b04dd4531193da2f`  
		Last Modified: Sat, 28 Jan 2023 05:21:44 GMT  
		Size: 31.0 MB (30996511 bytes)  
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
$ docker pull ubuntu@sha256:eb25b45bdceafdab343223bb76a5cd5c2491c6ac666d0dfa69530a87b06b8500
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
$ docker pull ubuntu@sha256:fdd3c9372c19afa928f99afde58f0f80a008ebb695a8c5ee37de5adb7feb46de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2df19066aca89df8e5317544a1cb599dc657830184762ff6fdefaaf708db65`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:72d9f18d70f395ff9bfae4d193077ccea3ca583e3da3dd66f5c84520c0100727`  
		Last Modified: Thu, 26 Jan 2023 10:11:57 GMT  
		Size: 25.7 MB (25688613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f21972d048d5439834187f47e9e2869e5434a3c5d49f7ef721d3d5f62fe7de60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21395113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17e780dbbcb4f0f3439981b5f09c45d9de103ca383942edbb8842911f2402fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:56:13 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:56:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:56:18 GMT
ADD file:1cc75b54b9c4d0824203532d4bb0eea2aaeafed003e37057b21aa3713b6bb0ea in / 
# Thu, 26 Jan 2023 09:56:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c138257d410403a2127c08e269ac8467b8f2001b22a102934861b65b2f49bc1a`  
		Last Modified: Thu, 26 Jan 2023 10:12:17 GMT  
		Size: 21.4 MB (21395113 bytes)  
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
$ docker pull ubuntu@sha256:fcebd6734dcbffd0c328771b11a0d00a8045f58ee5d3e083d3afdb54c72dab8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26096513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97151d96f64f3b5b7cdb0fadb1c1f8556552cedf32154f23efd48595efabb1e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:57a4d5aed2cd4a1f596f693a8fe5e135bd66dbf401ec169b1848d2316bdcfb2c`  
		Last Modified: Thu, 26 Jan 2023 10:12:23 GMT  
		Size: 26.1 MB (26096513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:da6bd15c918442485ea09b9b4a679ccddef764b03c04a94fa2f0ee75bf9ae709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29351018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e533a2e815a6606d93392dd9f8ff6938a39080b67cfd575045cfe820ede7af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c790564dfb49a61552a6e89c63c7abf84177d16d0f0fb604df022bfcdc6497b`  
		Last Modified: Thu, 26 Jan 2023 10:12:31 GMT  
		Size: 29.4 MB (29351018 bytes)  
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
$ docker pull ubuntu@sha256:e6e0ce288360f2ecd6279dc7a587661895b583fa08ad31aefabc7ddd24270393
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; s390x

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
$ docker pull ubuntu@sha256:cb91157e87db4be7e2fc86ff0dfc49adc1bff1d418db19d0627ae5c326938954
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
$ docker pull ubuntu@sha256:52293638ba652a2e8f9e1c1cfcc905839b1f2a9e671ddcc9bf77909b6bf527d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb2152822b716b4deac2996f16bc84db0a14b7cbc549579635590438f9c0e1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:15:52 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:15:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:15:54 GMT
ADD file:915f1a27db0a8b9a9dd58d40086cb7d45b2722e8ceb29ed8bcb306d4dcd3688e in / 
# Sat, 28 Jan 2023 05:15:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db781b8aed497363312ef32499cbfac28821e0494db7f0cadc4e716853e02a12`  
		Last Modified: Sat, 28 Jan 2023 05:21:25 GMT  
		Size: 26.6 MB (26638886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9fbac10f6899f18c2a614e0d7dc2a38af1559e5f0995d3b70bd8c1d57401ff76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25086001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173233681dc2cf6e3fa1246e9ee30ffdbd026b650b163a584cdf76d6b3ae773f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:25 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:31 GMT
ADD file:c0ac354f01ba9deb72bda06f4368650e0cc3ad5c3425ce0eb452561b56a1734a in / 
# Sat, 28 Jan 2023 05:11:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2cf733a376b355703d852c37fb66314a9d27adeb140641f229bd7d5b089c8ef7`  
		Last Modified: Sat, 28 Jan 2023 05:21:37 GMT  
		Size: 25.1 MB (25086001 bytes)  
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
$ docker pull ubuntu@sha256:a8498f0e21515679ba0037a81a4ab642c1d95710be8559a451c53df1d796fe06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30996511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3034f502162557a76be48b558db7cd107c03e20d4ce61ae3773374acca05b38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:09:15 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:09:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:09:19 GMT
ADD file:1c6ae50eb1e182a9aa8f750f61a615d5b3578b7c2f94e58678359bf1f43d3780 in / 
# Sat, 28 Jan 2023 05:09:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b536935eabb902676d3f03adcea225b24ae7144948054cd9b04dd4531193da2f`  
		Last Modified: Sat, 28 Jan 2023 05:21:44 GMT  
		Size: 31.0 MB (30996511 bytes)  
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
$ docker pull ubuntu@sha256:de3911cdfaf1376a963a0ca6e72e86c456b268d269bd24fd741725fb2a2ca4be
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
$ docker pull ubuntu@sha256:bffb6799d706144f263f4b91e1226745ffb5643ea0ea89c2f709208e8d70c999
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27503418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40cf56b4be35b04f620bc9cfbef80038fd7370d4ed36d90676223174ecbf0b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b549f31133a955f68f9fa0d93f18436c4a180e12184b999a8ecf14f7eaa83309`  
		Last Modified: Wed, 01 Feb 2023 12:05:25 GMT  
		Size: 27.5 MB (27503418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7bb60f92af1f5062f83b4b0edd5710332e20e1f99ae6c294d8b5bd7d7551a41b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23608452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2238f5e875d6e7d6f10729c620de133ae54eb25518994fcf012e02df6ec9e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:28:35 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:28:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:28:36 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:28:43 GMT
ADD file:6566d63937dd1808d3a4ea5591d4369b9083772d48fad60626fb91243a9f3f53 in / 
# Wed, 01 Feb 2023 11:28:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:363362dbf1847a398cc45b6a5f85ddbc7c633b43b9120f06e1e8cdd10237325a`  
		Last Modified: Wed, 01 Feb 2023 12:05:37 GMT  
		Size: 23.6 MB (23608452 bytes)  
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
$ docker pull ubuntu@sha256:e66e5d8f6f3761ce46b82a167ec4b091e87f0e0902d302b4fb9781f421e9ad23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a648e725100f70f48b2ca60e75e69b4b5e2a7a9abbceba82f43764bc32ca9df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:210cd7d37ec304813e8c7a2036ca7ca250cda0516fe48a4139b60c4cb817eaaf`  
		Last Modified: Wed, 01 Feb 2023 12:05:43 GMT  
		Size: 32.1 MB (32068234 bytes)  
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
$ docker pull ubuntu@sha256:eaaf7cf2c6e20900e2b1e07b7d735306fcdaa60f202961366569fa100361e675
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; s390x

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
$ docker pull ubuntu@sha256:dad0b9789498ed3cf6c7b3ea3183d7565502d5301751044ccee1d8139a580c07
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
$ docker pull ubuntu@sha256:c985bc3f77946b8e92c9a3648c6f31751a7dd972e06604785e47303f4ad47c4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29528717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58db3edaf2be6e80f628796355b1bdeaf8bea1692b402f48b7e7b8d1ff100b02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:677076032cca0a2362d25cf3660072e738d1b96fe860409a33ce901d695d7ee8`  
		Last Modified: Thu, 26 Jan 2023 05:13:54 GMT  
		Size: 29.5 MB (29528717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7f1627151f895be9f4805b8a092f0d17a3365c142c95d44f9c857fc891172fa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26137949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b861da44337925963eb70b8671950999df7d8abfe7f5a9b5f95ff9f4cca7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:40 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:43 GMT
ADD file:12d2a7ddc8445b8f97c960075216eb8e8cd226b84259c7343ef15c65a440b500 in / 
# Thu, 26 Jan 2023 05:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:860e874323ae800886f85ab5c346783e3a9371bd9beb72c5f25e8e20c9dd18bb`  
		Last Modified: Thu, 26 Jan 2023 05:14:09 GMT  
		Size: 26.1 MB (26137949 bytes)  
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
$ docker pull ubuntu@sha256:9ff892e66bc925cfcde0f1007bc1813f2d6c73b90c2681b1f1e35c39678f93fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34588568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d899338973bac5fb325b647c7436507e44918374fff2a72b0da6515946c868a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:58:24 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:58:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:28 GMT
ADD file:f0400001a50847feb579e66e804ec9daaaaeb9a414b4b5cca8bb0c8e9c7fa8f9 in / 
# Thu, 26 Jan 2023 04:58:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:717e115780fa5a198871a9eef15e446084728bf7021e7894e6118f3cd6d26b60`  
		Last Modified: Thu, 26 Jan 2023 05:14:15 GMT  
		Size: 34.6 MB (34588568 bytes)  
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
$ docker pull ubuntu@sha256:9aacf3caaf63eb1bb11717cb435fa142e53a2256a877a9b49c2d148060211297
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; s390x

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
$ docker pull ubuntu@sha256:a2626d53b5a5e8e7f73664beb605525f300cc9a203b5efef5583cae8560a183a
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
$ docker pull ubuntu@sha256:535c4a5ab0c2937593fb6aa241d9996f6eed02b8598928aa289ffd0416561131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c2f4041af137e6b0ba5c793df3dfdf4e72a4e011ce6847f4cc0247b9bbf7f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:51:12 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:51:13 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:51:14 GMT
ADD file:e886423892b371751386c0ce7147599acb72d8fb528eaaa78092b879d9ff58ce in / 
# Thu, 26 Jan 2023 11:51:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:256644d5a307c3efeca6ae2854b6329a2753157868dc5548e33161b377658e6a`  
		Last Modified: Thu, 26 Jan 2023 12:14:04 GMT  
		Size: 26.7 MB (26691650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b44ef81c8e6d1bd305cc72000c972fcd255a0b3f3bfe4dec81f651a53c8eeb89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25066997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d643d5974c30c06b1d811877a3a8f0047c4278b1fe0801d8d812b3a17ce6c15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:52:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:52:03 GMT
ADD file:d35c57b0dc2840a8b1ef40f7f6cfd826da68611f1ba37a89a382618c8612b52c in / 
# Thu, 26 Jan 2023 11:52:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:697d38f8dfe625e3e751c0b01ddeaaeeff6e8d6f594dd7da227aea3974a49ce1`  
		Last Modified: Thu, 26 Jan 2023 12:14:16 GMT  
		Size: 25.1 MB (25066997 bytes)  
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
$ docker pull ubuntu@sha256:7a248a581d0b98a906b2ba67277834f2613d35179f91872152a7776a81f6c2d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfbc0b60efcd8ea2a51c157e7bc286d8de7e88ae1bf756e0d8a44ff107e21c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:57:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:57:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:57:03 GMT
ADD file:3c2bc98d283cce5149d7992233f5fe644b7239417045faf3f93750b92de5f68e in / 
# Thu, 26 Jan 2023 11:57:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8da618ff876e10064f550b9dc5b51b0d0ae6939f67b56ce9a0c7fa8bb77de40f`  
		Last Modified: Thu, 26 Jan 2023 12:14:22 GMT  
		Size: 31.1 MB (31110147 bytes)  
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
$ docker pull ubuntu@sha256:2dd3788ee90185942a7f6258b0196110b89f0a554e1c8a66d677a395d578e71a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; s390x

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
$ docker pull ubuntu@sha256:dad0b9789498ed3cf6c7b3ea3183d7565502d5301751044ccee1d8139a580c07
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
$ docker pull ubuntu@sha256:c985bc3f77946b8e92c9a3648c6f31751a7dd972e06604785e47303f4ad47c4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29528717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58db3edaf2be6e80f628796355b1bdeaf8bea1692b402f48b7e7b8d1ff100b02`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:57:59 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:57:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:02 GMT
ADD file:18e71f049606f6339ce7a995839623f50e6ec6474bfd0a3a7ca799db726f47f6 in / 
# Thu, 26 Jan 2023 04:58:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:677076032cca0a2362d25cf3660072e738d1b96fe860409a33ce901d695d7ee8`  
		Last Modified: Thu, 26 Jan 2023 05:13:54 GMT  
		Size: 29.5 MB (29528717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:7f1627151f895be9f4805b8a092f0d17a3365c142c95d44f9c857fc891172fa2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26137949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b861da44337925963eb70b8671950999df7d8abfe7f5a9b5f95ff9f4cca7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 05:05:40 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:05:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:05:40 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:05:43 GMT
ADD file:12d2a7ddc8445b8f97c960075216eb8e8cd226b84259c7343ef15c65a440b500 in / 
# Thu, 26 Jan 2023 05:05:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:860e874323ae800886f85ab5c346783e3a9371bd9beb72c5f25e8e20c9dd18bb`  
		Last Modified: Thu, 26 Jan 2023 05:14:09 GMT  
		Size: 26.1 MB (26137949 bytes)  
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
$ docker pull ubuntu@sha256:9ff892e66bc925cfcde0f1007bc1813f2d6c73b90c2681b1f1e35c39678f93fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34588568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d899338973bac5fb325b647c7436507e44918374fff2a72b0da6515946c868a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 04:58:24 GMT
ARG RELEASE
# Thu, 26 Jan 2023 04:58:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 04:58:24 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 04:58:28 GMT
ADD file:f0400001a50847feb579e66e804ec9daaaaeb9a414b4b5cca8bb0c8e9c7fa8f9 in / 
# Thu, 26 Jan 2023 04:58:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:717e115780fa5a198871a9eef15e446084728bf7021e7894e6118f3cd6d26b60`  
		Last Modified: Thu, 26 Jan 2023 05:14:15 GMT  
		Size: 34.6 MB (34588568 bytes)  
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
$ docker pull ubuntu@sha256:cb91157e87db4be7e2fc86ff0dfc49adc1bff1d418db19d0627ae5c326938954
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
$ docker pull ubuntu@sha256:52293638ba652a2e8f9e1c1cfcc905839b1f2a9e671ddcc9bf77909b6bf527d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26638886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb2152822b716b4deac2996f16bc84db0a14b7cbc549579635590438f9c0e1d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:15:52 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:15:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:15:52 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:15:54 GMT
ADD file:915f1a27db0a8b9a9dd58d40086cb7d45b2722e8ceb29ed8bcb306d4dcd3688e in / 
# Sat, 28 Jan 2023 05:15:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:db781b8aed497363312ef32499cbfac28821e0494db7f0cadc4e716853e02a12`  
		Last Modified: Sat, 28 Jan 2023 05:21:25 GMT  
		Size: 26.6 MB (26638886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9fbac10f6899f18c2a614e0d7dc2a38af1559e5f0995d3b70bd8c1d57401ff76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25086001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173233681dc2cf6e3fa1246e9ee30ffdbd026b650b163a584cdf76d6b3ae773f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:11:25 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:11:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:11:25 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:11:31 GMT
ADD file:c0ac354f01ba9deb72bda06f4368650e0cc3ad5c3425ce0eb452561b56a1734a in / 
# Sat, 28 Jan 2023 05:11:32 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2cf733a376b355703d852c37fb66314a9d27adeb140641f229bd7d5b089c8ef7`  
		Last Modified: Sat, 28 Jan 2023 05:21:37 GMT  
		Size: 25.1 MB (25086001 bytes)  
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
$ docker pull ubuntu@sha256:a8498f0e21515679ba0037a81a4ab642c1d95710be8559a451c53df1d796fe06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30996511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3034f502162557a76be48b558db7cd107c03e20d4ce61ae3773374acca05b38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Jan 2023 05:09:15 GMT
ARG RELEASE
# Sat, 28 Jan 2023 05:09:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 28 Jan 2023 05:09:16 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 28 Jan 2023 05:09:19 GMT
ADD file:1c6ae50eb1e182a9aa8f750f61a615d5b3578b7c2f94e58678359bf1f43d3780 in / 
# Sat, 28 Jan 2023 05:09:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b536935eabb902676d3f03adcea225b24ae7144948054cd9b04dd4531193da2f`  
		Last Modified: Sat, 28 Jan 2023 05:21:44 GMT  
		Size: 31.0 MB (30996511 bytes)  
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
$ docker pull ubuntu@sha256:99a1a888a6977c5a695018702de1c43ac18d111529a53a09cef67309c29a3215
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; s390x

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
$ docker pull ubuntu@sha256:a2626d53b5a5e8e7f73664beb605525f300cc9a203b5efef5583cae8560a183a
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
$ docker pull ubuntu@sha256:535c4a5ab0c2937593fb6aa241d9996f6eed02b8598928aa289ffd0416561131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26691650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c2f4041af137e6b0ba5c793df3dfdf4e72a4e011ce6847f4cc0247b9bbf7f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:51:12 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:51:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:51:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:51:13 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:51:14 GMT
ADD file:e886423892b371751386c0ce7147599acb72d8fb528eaaa78092b879d9ff58ce in / 
# Thu, 26 Jan 2023 11:51:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:256644d5a307c3efeca6ae2854b6329a2753157868dc5548e33161b377658e6a`  
		Last Modified: Thu, 26 Jan 2023 12:14:04 GMT  
		Size: 26.7 MB (26691650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:b44ef81c8e6d1bd305cc72000c972fcd255a0b3f3bfe4dec81f651a53c8eeb89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25066997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d643d5974c30c06b1d811877a3a8f0047c4278b1fe0801d8d812b3a17ce6c15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:52:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:52:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:52:03 GMT
ADD file:d35c57b0dc2840a8b1ef40f7f6cfd826da68611f1ba37a89a382618c8612b52c in / 
# Thu, 26 Jan 2023 11:52:03 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:697d38f8dfe625e3e751c0b01ddeaaeeff6e8d6f594dd7da227aea3974a49ce1`  
		Last Modified: Thu, 26 Jan 2023 12:14:16 GMT  
		Size: 25.1 MB (25066997 bytes)  
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
$ docker pull ubuntu@sha256:7a248a581d0b98a906b2ba67277834f2613d35179f91872152a7776a81f6c2d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31110147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfbc0b60efcd8ea2a51c157e7bc286d8de7e88ae1bf756e0d8a44ff107e21c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 11:57:00 GMT
ARG RELEASE
# Thu, 26 Jan 2023 11:57:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 11:57:00 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 26 Jan 2023 11:57:03 GMT
ADD file:3c2bc98d283cce5149d7992233f5fe644b7239417045faf3f93750b92de5f68e in / 
# Thu, 26 Jan 2023 11:57:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8da618ff876e10064f550b9dc5b51b0d0ae6939f67b56ce9a0c7fa8bb77de40f`  
		Last Modified: Thu, 26 Jan 2023 12:14:22 GMT  
		Size: 31.1 MB (31110147 bytes)  
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
