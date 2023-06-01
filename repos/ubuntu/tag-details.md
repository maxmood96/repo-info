<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:18.04`](#ubuntu1804)
-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:22.10`](#ubuntu2210)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:bionic`](#ubuntubionic)
-	[`ubuntu:bionic-20230530`](#ubuntubionic-20230530)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20230412`](#ubuntufocal-20230412)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20230522`](#ubuntujammy-20230522)
-	[`ubuntu:kinetic`](#ubuntukinetic)
-	[`ubuntu:kinetic-20230412`](#ubuntukinetic-20230412)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20230522`](#ubuntulunar-20230522)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20230520`](#ubuntumantic-20230520)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:18.04`

```console
$ docker pull ubuntu@sha256:152dc042452c496007f07ca9127571cb9c29697f42acbfad72324b2bb2e43c98
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
$ docker pull ubuntu@sha256:dca176c9663a7ba4c1f0e710986f5a25e672842963d95b960191e2d9f7185ebe
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25691281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a80a55f492e823bf5d51f1bd5f87ea3eed1cb31788686aa99a2fb61a27af6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Tue, 30 May 2023 10:03:37 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f9d8624e98e31a551d490e0bc3e1ea76319974ddae819c641be1158857b3ddc7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21399001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1317ca4808cd9de6f8eb6c62a64e98491db236396ded4d5c2a6fa959e6d69b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:52:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:52:20 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 30 May 2023 09:52:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:33728956a279755bb5e348de30626ffff0023b589d4fae264c2722ad7c06e207`  
		Last Modified: Tue, 30 May 2023 10:03:48 GMT  
		Size: 21.4 MB (21399001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f97a5103cca28097326814718e711c9c41b54853c26959d73495e40b1dd608f2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22713516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a528908992e9b5bcff8329a22de1749007d0eeeccb93ab85dd5a822b8d46a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Tue, 30 May 2023 10:03:42 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; 386

```console
$ docker pull ubuntu@sha256:fc896f56642f382e99601461c683dee1534f0d4cb7e17bcb3494d5ed0f3a8a06
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26100852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70288ee657e2ad33414f7475c58f2127130d1e4f5b594ad56c992bdf45a6bacc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:14 GMT
ADD file:1f856710b4bf82e95a940e08c6167ef4775a430a38fd2fb575ad7743bacb39b6 in / 
# Tue, 30 May 2023 09:32:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f6c0c474444aad1f51506c3093030e0c946e7e05f0103171197fe2546a31720`  
		Last Modified: Tue, 30 May 2023 10:03:54 GMT  
		Size: 26.1 MB (26100852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f9a073fd91492a05f242ea30fd09deb6deabd8f11c5829eea984711fcd05dd01
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6e782d0b5b700a6de2f2fe068544d7bf7d4f7050b8ac226dfb1a2c08a4a341`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:33:21 GMT
ARG RELEASE
# Tue, 30 May 2023 09:33:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:33:24 GMT
ADD file:0c5b3fc2318612ae30bebd058c1384994f4ee2f836b73d82bd9792993ad4b37c in / 
# Tue, 30 May 2023 09:33:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:98a0461ace5bb1ed4fe07d41b9a9492f383abc089fa0873807ae5697bb052185`  
		Last Modified: Tue, 30 May 2023 10:03:59 GMT  
		Size: 29.4 MB (29350502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:18.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:d703aed6386f192b5287ed5f79b9548055a59edea4166bbe38cdc1b427b999b8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24751131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bc6dbb98e72bc1140977c547bbe933ed0a075ba03899c541b0c3ba9f0f90a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:26:28 GMT
ARG RELEASE
# Tue, 30 May 2023 09:26:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:26:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:26:28 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:26:29 GMT
ADD file:3ed568ba86f7dcc948369fa5141ac64b558b1594643b1e8725d0e4790e4460ce in / 
# Tue, 30 May 2023 09:26:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:63fbc30c112e96fb16b6b903d1edf79ebc150e4e30c9b57ac11fcbff2ac51e7d`  
		Last Modified: Tue, 30 May 2023 10:04:05 GMT  
		Size: 24.8 MB (24751131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:db8bf6f4fb351aa7a26e27ba2686cf35a6a409f65603e59d4c203e58387dc6b3
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
$ docker pull ubuntu@sha256:b795f8e0caaaacad9859a9a38fe1c78154f8301fdaf0872eaf1520d66d9c0b98
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27504674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd6891718934e63638d9ca0ecee018e69b638270fe04990a310e5c78ab4a92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca1778b6935686ad781c27472c4668fc61ec3aeb85494f72deb1921892b9d39e`  
		Last Modified: Thu, 13 Apr 2023 13:45:57 GMT  
		Size: 27.5 MB (27504674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:6de8d817428e3d064da83ce59b4dccf7c6749aa60b36a17ad6cc3b1f7d10123c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23609760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b1180d68d3d67c103b16d57b364242467c2eacbbe69a9ddc04dcf1cf801d75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:39f91c5e27647c786293528ceed473da81ca1f8e8a07bd92474a6d695bad1e22`  
		Last Modified: Thu, 13 Apr 2023 13:46:09 GMT  
		Size: 23.6 MB (23609760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:144e6a778925a0c11c4cd9fe5fce1172e620f215b0410bb43e7fa41bbcfe4522
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758cd4ebb2178eb0cd2ce78dea8ffad569f5bba415c4b33b694e891e7697e854`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8659cf1709ef03be2c0b2dc339b19432bff8a0753d2d7d53f47272f098f56ef4`  
		Last Modified: Thu, 13 Apr 2023 13:46:03 GMT  
		Size: 26.0 MB (25972971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:98fcf155d7d9fe687af0af87ccbe0dcc17338686504d341cf8a731499f40cf16
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd2848d7eadab46995f05c8e09edecfc3845d61e418304136f82bb9e22601d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f161979f5cb055a8a6d3d728b7db322422139cc28b60c716d107993a794cd86c`  
		Last Modified: Thu, 13 Apr 2023 13:46:15 GMT  
		Size: 32.1 MB (32068809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:91c315263bf6ce2500fa1b15cdb916c2c7e77a2e436dafde1788b40bc3105250
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42c37c658114d3d2893b096a54d2deab61f556eb08c89764d35cdf13faf7ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f4c3f72acab731ed4e440147b25e7d155c3d98eb8738b731250868ad184e54d9`  
		Last Modified: Thu, 13 Apr 2023 13:46:21 GMT  
		Size: 26.4 MB (26364733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.04`

```console
$ docker pull ubuntu@sha256:ac58ff7fe25edc58bdf0067ca99df00014dbd032e2246d30a722fa348fd799a5
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
$ docker pull ubuntu@sha256:2fdb1cf4995abb74c035e5f520c0f3a46f12b3377a59e86ecca66d8606ad64f9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6ddc1b2547b2e38dc25b265ac585238a3c23da63976722864dab2a069c74f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:837dd4791cdc6f670708c3a570b72169263806d7ccc2783173b9e88f94878271`  
		Last Modified: Mon, 22 May 2023 18:07:29 GMT  
		Size: 29.5 MB (29534702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c80ed91cdc47229010c4f34f96c3442bc02dca260d0bf26f6c4b047ea7d11cf2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a5c81bff1484d6f6943eb15664ccf9027b66e59244258bee27737f9c50a521`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:52:13 GMT
ARG RELEASE
# Mon, 22 May 2023 17:52:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:52:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:52:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:52:16 GMT
ADD file:52b34a0d4198b5d30380eb1f293fb8916790394fcba96b4759a3f1beeb373b1a in / 
# Mon, 22 May 2023 17:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:68b5e8df6832be9e886e342be08257a6f07c071a6e82751005d3d72c4af06e55`  
		Last Modified: Mon, 22 May 2023 18:07:41 GMT  
		Size: 26.1 MB (26141405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:77bdd217935d10f0e753ed84118e9b11d3ab0a66a82bdf322087354ccd833733
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27349492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2767693332e5523a2734b82f57d1a91510c92237912a96fec46352785e120b3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:952b15bbc7fb957dead5972b258558130aeda588416c0a7a861e916fc08b36d7`  
		Last Modified: Mon, 22 May 2023 18:07:35 GMT  
		Size: 27.3 MB (27349492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:268686ba2c6284461cae1642d9d055e51b16f8e711d49b34638146b78050f5a0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34594849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea41887ad57d6a41c77497c1cc4bcec3195b67b7d73e2b7873ee46590b96672e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:39:12 GMT
ARG RELEASE
# Mon, 22 May 2023 17:39:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:39:16 GMT
ADD file:5b5967ce188eac9717526ca9f6cf6679cbae6ee4b17b207cc3d640c78d9a9788 in / 
# Mon, 22 May 2023 17:39:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2283df590faf676672db76cf3fd8c126945c8e86950777d8e306d757fbf82285`  
		Last Modified: Mon, 22 May 2023 18:07:47 GMT  
		Size: 34.6 MB (34594849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:b0b966f885ea29d809d03d027c3d21182676380b241c3a271aa83f8e9d7bac06
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28017412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9175efc14fb0eb640de06d66d6ae157973afe75950f979e0aad3f8391f51320e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:46:45 GMT
ARG RELEASE
# Mon, 22 May 2023 17:46:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:46:47 GMT
ADD file:7bf1b7a1484e37f289d40f5c1c1cbe321ef337f898dd3d5809193c848a9a3dc2 in / 
# Mon, 22 May 2023 17:46:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8591eece70e54e483b384ce950218057ea0af677115b02a041579bf05da474ec`  
		Last Modified: Mon, 22 May 2023 18:07:55 GMT  
		Size: 28.0 MB (28017412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:22.10`

```console
$ docker pull ubuntu@sha256:a9a425d086dbb34c1b5b99765596e2a3cc79b33826866c51cd4508d8eb327d2b
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
$ docker pull ubuntu@sha256:d69f6ed3c483abe6ed19d7310acacd14012fd62874ea98edccddf6ac7af3ce93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26695202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15f05d8742509cfc142f79dfe4cc2fa4e1b7bd20415675f7b52d3e22fd53670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0963d61c5d36e157f4d244438f1a5213d8590b724d49300d6df8ebf5d70342a9`  
		Last Modified: Fri, 14 Apr 2023 11:09:15 GMT  
		Size: 26.7 MB (26695202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9afa28d1eb80d78129debbef52b3f2a59b19479b2c15f01d16c2beeccd72dc10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781448a65e540dff394a6ae765d032b6c5fee3e0bc008f323330bd44a5aa797`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:049083b382db595e625c4760cee04d50fb6110bda597a3dd936406027ce01994`  
		Last Modified: Fri, 14 Apr 2023 11:09:28 GMT  
		Size: 25.1 MB (25067534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:9ff03c2930fce7e915f3b321c6c601380ffb845140bd36715c44ec31d7ae551e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25759013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490b20d4c90f834abcf386620a8906d21821aaa4db91c4665016883f043a10e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4bb7992c0b6c454d95752fadeb8ec30f02376e386e2dbcde466ab9e74283ed78`  
		Last Modified: Fri, 14 Apr 2023 11:09:21 GMT  
		Size: 25.8 MB (25759013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:56185868328c6dcfff4b9f97915a8868905668fa8ffab0b2b0285dac1dfd84cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa908635f261aa7b8aa52c329990cdc01c4716fdac960a6f3cfff6706f2b56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6864d2efca45377dbba7535ab73bb2a64f10d73c7d97bfbd768b173970bf455`  
		Last Modified: Fri, 14 Apr 2023 11:09:34 GMT  
		Size: 31.1 MB (31113926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:3761fb8cb1cfa0facc994bb50e559e50144c999ff6ac5a43712396f98dd92045
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25488667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d1b46d5d955e3fbe7be0da291db9a566b03ebbac3335bca37d70d66078e9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:91664c4b18004c964fd7a8e4cc1d53adb98ce8158f5d0dde54befa1c1f754635`  
		Last Modified: Fri, 14 Apr 2023 11:09:40 GMT  
		Size: 25.5 MB (25488667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.04`

```console
$ docker pull ubuntu@sha256:9279f41cc6e4df8f87b13ac17c2c6f2a280fd3ca2638d18f8dc94b774486909f
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
$ docker pull ubuntu@sha256:5ed6262a1edb954cae006b966ca70468e982285aa57419b4d2b221a5e11dd881
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d710383bd1efcb401c8e0aca2c596b3b93ab021d1e001b4e90c394af54773632`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 09:16:59 GMT
ARG RELEASE
# Tue, 23 May 2023 09:16:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 09:17:01 GMT
ADD file:6591237a72178b71d79f687b816ad23237fbef0bc3ec42332369d9e7bdaa04e4 in / 
# Tue, 23 May 2023 09:17:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:361237ddf358bcd8b864f2f24bd3d134262cb47ccd30556a7ba97c218f0b3435`  
		Last Modified: Tue, 23 May 2023 09:42:21 GMT  
		Size: 26.8 MB (26825631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f98df397a30936bc4bfcb205d125e9231c6c37077733c2d0a4683969c37e8d43
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24635016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f931f4d70204e5ec5f89bef40edce58b73434720c646e47508966c92562cb0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:12 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:12 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:16 GMT
ADD file:eff76586a1ef817ec09adc4b06a3656dccdfa9eaa17e0580677ed3315d37067b in / 
# Tue, 23 May 2023 08:33:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cec830e76152242e25efac1882b1fd0617ddb70bc9e22f6c702d0c76481a41cb`  
		Last Modified: Tue, 23 May 2023 09:42:32 GMT  
		Size: 24.6 MB (24635016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb688171cf562115f640d289507c9215b42f3c7f88c0c4783b7b5d833b21b477
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b605c4398aab9e1bb450ed620ae949978e2dd3ca158d7c124f4f7e1365364e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:45 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:47 GMT
ADD file:b2902a85ba60d642b00f2d7d7e4f56825749dca527e2d8d5e64d854c76ed28f0 in / 
# Tue, 23 May 2023 08:33:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8e6f677fb231e140748c758073ca5f3833b883f5762e43603976eba228cdaeb`  
		Last Modified: Tue, 23 May 2023 09:42:26 GMT  
		Size: 26.1 MB (26079431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dad6fefabb79c014fe82216113a9c5898e2c28a6fa16e5254856d907eb783bad
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb828ec9db7fa57d058990d9b984ad775b8704f411f1c8d9c919152e894d935`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:36:49 GMT
ARG RELEASE
# Tue, 23 May 2023 08:36:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:36:52 GMT
ADD file:d76035fa745d219f333adeb90e6eedc3b563dca64aa80c2fbe88d7389ba798d2 in / 
# Tue, 23 May 2023 08:36:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e0b93a5ca79f060115dd23deb777acddd707c28a75961b073aea5287cd2a5e8`  
		Last Modified: Tue, 23 May 2023 09:42:38 GMT  
		Size: 31.0 MB (31018854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:ab66eeed2bf32c0326833749dbd50f63d0260d4b7be59dec88142b3ac44357c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25706387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1531d9864af82dc6f98e54333578b74c087e821c0ea4073d89993b89bfcef8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:34:39 GMT
ARG RELEASE
# Tue, 23 May 2023 08:34:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:34:41 GMT
ADD file:390d5b6c76bd6ae4f2901362d9a308f7dc4fa9a83574ec3952e867bc951c1552 in / 
# Tue, 23 May 2023 08:34:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b35c5f24ffbc70a87b2657a3f8b49a4c6030afe433a1a3a28ddff66e5bfc967`  
		Last Modified: Tue, 23 May 2023 09:42:44 GMT  
		Size: 25.7 MB (25706387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:23.10`

```console
$ docker pull ubuntu@sha256:2cde79b4627d38d1448fc264f93e465f18b653bc9a62ee8ec85d99d4e8f39d4c
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
$ docker pull ubuntu@sha256:2977bee81d7883ef1cbeb369d8d2afc21da7977f99e347cf1931c586f7045fee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26880446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e51849785d31c2fe2fd3b45020f7d55aedd165869d0131effe6feb29f17ed9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:41 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:41 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:43 GMT
ADD file:6bd9b5983097734c3050b464660da9015c0e2f93416920b8404ff7d28d8bccd8 in / 
# Sat, 20 May 2023 16:58:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f2131a27ab9c8a2c55e5a33ce861393bf5934a64d16b508f4532a8e749937df7`  
		Last Modified: Sat, 20 May 2023 17:08:21 GMT  
		Size: 26.9 MB (26880446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:af6575b7dfc5526ba8710a748349ed01f849cfbcd11123d86293360284ed0558
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24569382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0252db62febe6af452e6991741e6f20b6d5d6b97c100af170ce4fdbf21655717`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:22 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:25 GMT
ADD file:c7522b8ff46586b3057c8eae94d6cfc77299a4f2ccc3762e6263780ccc7c82c0 in / 
# Sat, 20 May 2023 16:58:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c5174d07727ff19811fe8f7e76bbe8d175a16bcb423918a5e34cba75b7de22dd`  
		Last Modified: Sat, 20 May 2023 17:08:34 GMT  
		Size: 24.6 MB (24569382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ab607dfa49b79e0d99b2061d507dc2e7dc4c35cc53170749ad512d5a224e5b6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26099857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc8a176a7255f169a5952b707290db97b5117aeff26d79fb31091d9e4887030`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:34 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:36 GMT
ADD file:39dff3364ce4bb79539ed5e58493be16a66d424e605cb774559830ba8452bc4d in / 
# Sat, 20 May 2023 16:59:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2f6eed94ce9d338a3640a267747fa4c20b312670df4c690d4412a873474d9345`  
		Last Modified: Sat, 20 May 2023 17:08:28 GMT  
		Size: 26.1 MB (26099857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d461cdc8a2fb842dc2f8ba0789368db6d3b9bd8493f56a8b035e85bb144b8218
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30918336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7067ffebf34c75aaa5a5cc7f9027b0ea2bdf92950f3e54d1183648b0796d7955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:51 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:51 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:54 GMT
ADD file:83fb0f5b40d9233c6017f5c5a9e51e184b8f56b03c54fafa207e9ca28aa2df52 in / 
# Sat, 20 May 2023 16:58:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1322522d35b297f2cf89ef1cb25b604a3ec335526102b1194ea3cac1eda2eee7`  
		Last Modified: Sat, 20 May 2023 17:08:40 GMT  
		Size: 30.9 MB (30918336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:b2c200b149a4e921a060610533f68a963a408bc84c577b8ba20b48a92d0f95fa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25698480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da1786faa70195e4008ab4d55834d2c10535f234b350eb74843b9a3f28d9739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:20 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:22 GMT
ADD file:fb602b3f6c251d8267de1cf0525d0b38aab5966c848182d037bb2890557f0a6e in / 
# Sat, 20 May 2023 16:59:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dabe55d229048645c6b502641876395c6a479819d8566c06fa2d15b894e68605`  
		Last Modified: Sat, 20 May 2023 17:08:47 GMT  
		Size: 25.7 MB (25698480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:bionic`

```console
$ docker pull ubuntu@sha256:152dc042452c496007f07ca9127571cb9c29697f42acbfad72324b2bb2e43c98
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
$ docker pull ubuntu@sha256:dca176c9663a7ba4c1f0e710986f5a25e672842963d95b960191e2d9f7185ebe
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25691281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a80a55f492e823bf5d51f1bd5f87ea3eed1cb31788686aa99a2fb61a27af6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Tue, 30 May 2023 10:03:37 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f9d8624e98e31a551d490e0bc3e1ea76319974ddae819c641be1158857b3ddc7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21399001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1317ca4808cd9de6f8eb6c62a64e98491db236396ded4d5c2a6fa959e6d69b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:52:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:52:20 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 30 May 2023 09:52:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:33728956a279755bb5e348de30626ffff0023b589d4fae264c2722ad7c06e207`  
		Last Modified: Tue, 30 May 2023 10:03:48 GMT  
		Size: 21.4 MB (21399001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f97a5103cca28097326814718e711c9c41b54853c26959d73495e40b1dd608f2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22713516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a528908992e9b5bcff8329a22de1749007d0eeeccb93ab85dd5a822b8d46a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Tue, 30 May 2023 10:03:42 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; 386

```console
$ docker pull ubuntu@sha256:fc896f56642f382e99601461c683dee1534f0d4cb7e17bcb3494d5ed0f3a8a06
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26100852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70288ee657e2ad33414f7475c58f2127130d1e4f5b594ad56c992bdf45a6bacc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:14 GMT
ADD file:1f856710b4bf82e95a940e08c6167ef4775a430a38fd2fb575ad7743bacb39b6 in / 
# Tue, 30 May 2023 09:32:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f6c0c474444aad1f51506c3093030e0c946e7e05f0103171197fe2546a31720`  
		Last Modified: Tue, 30 May 2023 10:03:54 GMT  
		Size: 26.1 MB (26100852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f9a073fd91492a05f242ea30fd09deb6deabd8f11c5829eea984711fcd05dd01
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6e782d0b5b700a6de2f2fe068544d7bf7d4f7050b8ac226dfb1a2c08a4a341`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:33:21 GMT
ARG RELEASE
# Tue, 30 May 2023 09:33:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:33:24 GMT
ADD file:0c5b3fc2318612ae30bebd058c1384994f4ee2f836b73d82bd9792993ad4b37c in / 
# Tue, 30 May 2023 09:33:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:98a0461ace5bb1ed4fe07d41b9a9492f383abc089fa0873807ae5697bb052185`  
		Last Modified: Tue, 30 May 2023 10:03:59 GMT  
		Size: 29.4 MB (29350502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic` - linux; s390x

```console
$ docker pull ubuntu@sha256:d703aed6386f192b5287ed5f79b9548055a59edea4166bbe38cdc1b427b999b8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24751131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bc6dbb98e72bc1140977c547bbe933ed0a075ba03899c541b0c3ba9f0f90a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:26:28 GMT
ARG RELEASE
# Tue, 30 May 2023 09:26:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:26:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:26:28 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:26:29 GMT
ADD file:3ed568ba86f7dcc948369fa5141ac64b558b1594643b1e8725d0e4790e4460ce in / 
# Tue, 30 May 2023 09:26:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:63fbc30c112e96fb16b6b903d1edf79ebc150e4e30c9b57ac11fcbff2ac51e7d`  
		Last Modified: Tue, 30 May 2023 10:04:05 GMT  
		Size: 24.8 MB (24751131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:bionic-20230530`

```console
$ docker pull ubuntu@sha256:152dc042452c496007f07ca9127571cb9c29697f42acbfad72324b2bb2e43c98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic-20230530` - linux; amd64

```console
$ docker pull ubuntu@sha256:dca176c9663a7ba4c1f0e710986f5a25e672842963d95b960191e2d9f7185ebe
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25691281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a80a55f492e823bf5d51f1bd5f87ea3eed1cb31788686aa99a2fb61a27af6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:07 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:07 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:09 GMT
ADD file:3c74e7e08cbf9a87694ce6fa541af617599680fa54d9e48556fc0fbc120b4a83 in / 
# Tue, 30 May 2023 09:32:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7c457f213c7634afb95a0fb2410a74b7b5bc0ba527033362c240c7a11bef4331`  
		Last Modified: Tue, 30 May 2023 10:03:37 GMT  
		Size: 25.7 MB (25691281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230530` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f9d8624e98e31a551d490e0bc3e1ea76319974ddae819c641be1158857b3ddc7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21399001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1317ca4808cd9de6f8eb6c62a64e98491db236396ded4d5c2a6fa959e6d69b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:52:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:52:20 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 30 May 2023 09:52:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:33728956a279755bb5e348de30626ffff0023b589d4fae264c2722ad7c06e207`  
		Last Modified: Tue, 30 May 2023 10:03:48 GMT  
		Size: 21.4 MB (21399001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230530` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:f97a5103cca28097326814718e711c9c41b54853c26959d73495e40b1dd608f2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22713516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a528908992e9b5bcff8329a22de1749007d0eeeccb93ab85dd5a822b8d46a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:064a9bb4736de1b2446f528e4eb37335378392cf9b95043d3e9970e253861702`  
		Last Modified: Tue, 30 May 2023 10:03:42 GMT  
		Size: 22.7 MB (22713516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230530` - linux; 386

```console
$ docker pull ubuntu@sha256:fc896f56642f382e99601461c683dee1534f0d4cb7e17bcb3494d5ed0f3a8a06
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26100852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70288ee657e2ad33414f7475c58f2127130d1e4f5b594ad56c992bdf45a6bacc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:14 GMT
ADD file:1f856710b4bf82e95a940e08c6167ef4775a430a38fd2fb575ad7743bacb39b6 in / 
# Tue, 30 May 2023 09:32:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3f6c0c474444aad1f51506c3093030e0c946e7e05f0103171197fe2546a31720`  
		Last Modified: Tue, 30 May 2023 10:03:54 GMT  
		Size: 26.1 MB (26100852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230530` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:f9a073fd91492a05f242ea30fd09deb6deabd8f11c5829eea984711fcd05dd01
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.4 MB (29350502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6e782d0b5b700a6de2f2fe068544d7bf7d4f7050b8ac226dfb1a2c08a4a341`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:33:21 GMT
ARG RELEASE
# Tue, 30 May 2023 09:33:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:33:21 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:33:24 GMT
ADD file:0c5b3fc2318612ae30bebd058c1384994f4ee2f836b73d82bd9792993ad4b37c in / 
# Tue, 30 May 2023 09:33:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:98a0461ace5bb1ed4fe07d41b9a9492f383abc089fa0873807ae5697bb052185`  
		Last Modified: Tue, 30 May 2023 10:03:59 GMT  
		Size: 29.4 MB (29350502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:bionic-20230530` - linux; s390x

```console
$ docker pull ubuntu@sha256:d703aed6386f192b5287ed5f79b9548055a59edea4166bbe38cdc1b427b999b8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24751131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2bc6dbb98e72bc1140977c547bbe933ed0a075ba03899c541b0c3ba9f0f90a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:26:28 GMT
ARG RELEASE
# Tue, 30 May 2023 09:26:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:26:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:26:28 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:26:29 GMT
ADD file:3ed568ba86f7dcc948369fa5141ac64b558b1594643b1e8725d0e4790e4460ce in / 
# Tue, 30 May 2023 09:26:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:63fbc30c112e96fb16b6b903d1edf79ebc150e4e30c9b57ac11fcbff2ac51e7d`  
		Last Modified: Tue, 30 May 2023 10:04:05 GMT  
		Size: 24.8 MB (24751131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:2cde79b4627d38d1448fc264f93e465f18b653bc9a62ee8ec85d99d4e8f39d4c
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
$ docker pull ubuntu@sha256:2977bee81d7883ef1cbeb369d8d2afc21da7977f99e347cf1931c586f7045fee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26880446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e51849785d31c2fe2fd3b45020f7d55aedd165869d0131effe6feb29f17ed9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:41 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:41 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:43 GMT
ADD file:6bd9b5983097734c3050b464660da9015c0e2f93416920b8404ff7d28d8bccd8 in / 
# Sat, 20 May 2023 16:58:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f2131a27ab9c8a2c55e5a33ce861393bf5934a64d16b508f4532a8e749937df7`  
		Last Modified: Sat, 20 May 2023 17:08:21 GMT  
		Size: 26.9 MB (26880446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:af6575b7dfc5526ba8710a748349ed01f849cfbcd11123d86293360284ed0558
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24569382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0252db62febe6af452e6991741e6f20b6d5d6b97c100af170ce4fdbf21655717`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:22 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:25 GMT
ADD file:c7522b8ff46586b3057c8eae94d6cfc77299a4f2ccc3762e6263780ccc7c82c0 in / 
# Sat, 20 May 2023 16:58:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c5174d07727ff19811fe8f7e76bbe8d175a16bcb423918a5e34cba75b7de22dd`  
		Last Modified: Sat, 20 May 2023 17:08:34 GMT  
		Size: 24.6 MB (24569382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ab607dfa49b79e0d99b2061d507dc2e7dc4c35cc53170749ad512d5a224e5b6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26099857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc8a176a7255f169a5952b707290db97b5117aeff26d79fb31091d9e4887030`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:34 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:36 GMT
ADD file:39dff3364ce4bb79539ed5e58493be16a66d424e605cb774559830ba8452bc4d in / 
# Sat, 20 May 2023 16:59:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2f6eed94ce9d338a3640a267747fa4c20b312670df4c690d4412a873474d9345`  
		Last Modified: Sat, 20 May 2023 17:08:28 GMT  
		Size: 26.1 MB (26099857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d461cdc8a2fb842dc2f8ba0789368db6d3b9bd8493f56a8b035e85bb144b8218
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30918336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7067ffebf34c75aaa5a5cc7f9027b0ea2bdf92950f3e54d1183648b0796d7955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:51 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:51 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:54 GMT
ADD file:83fb0f5b40d9233c6017f5c5a9e51e184b8f56b03c54fafa207e9ca28aa2df52 in / 
# Sat, 20 May 2023 16:58:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1322522d35b297f2cf89ef1cb25b604a3ec335526102b1194ea3cac1eda2eee7`  
		Last Modified: Sat, 20 May 2023 17:08:40 GMT  
		Size: 30.9 MB (30918336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:b2c200b149a4e921a060610533f68a963a408bc84c577b8ba20b48a92d0f95fa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25698480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da1786faa70195e4008ab4d55834d2c10535f234b350eb74843b9a3f28d9739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:20 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:22 GMT
ADD file:fb602b3f6c251d8267de1cf0525d0b38aab5966c848182d037bb2890557f0a6e in / 
# Sat, 20 May 2023 16:59:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dabe55d229048645c6b502641876395c6a479819d8566c06fa2d15b894e68605`  
		Last Modified: Sat, 20 May 2023 17:08:47 GMT  
		Size: 25.7 MB (25698480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:db8bf6f4fb351aa7a26e27ba2686cf35a6a409f65603e59d4c203e58387dc6b3
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
$ docker pull ubuntu@sha256:b795f8e0caaaacad9859a9a38fe1c78154f8301fdaf0872eaf1520d66d9c0b98
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27504674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd6891718934e63638d9ca0ecee018e69b638270fe04990a310e5c78ab4a92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca1778b6935686ad781c27472c4668fc61ec3aeb85494f72deb1921892b9d39e`  
		Last Modified: Thu, 13 Apr 2023 13:45:57 GMT  
		Size: 27.5 MB (27504674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:6de8d817428e3d064da83ce59b4dccf7c6749aa60b36a17ad6cc3b1f7d10123c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23609760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b1180d68d3d67c103b16d57b364242467c2eacbbe69a9ddc04dcf1cf801d75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:39f91c5e27647c786293528ceed473da81ca1f8e8a07bd92474a6d695bad1e22`  
		Last Modified: Thu, 13 Apr 2023 13:46:09 GMT  
		Size: 23.6 MB (23609760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:144e6a778925a0c11c4cd9fe5fce1172e620f215b0410bb43e7fa41bbcfe4522
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758cd4ebb2178eb0cd2ce78dea8ffad569f5bba415c4b33b694e891e7697e854`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8659cf1709ef03be2c0b2dc339b19432bff8a0753d2d7d53f47272f098f56ef4`  
		Last Modified: Thu, 13 Apr 2023 13:46:03 GMT  
		Size: 26.0 MB (25972971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:98fcf155d7d9fe687af0af87ccbe0dcc17338686504d341cf8a731499f40cf16
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd2848d7eadab46995f05c8e09edecfc3845d61e418304136f82bb9e22601d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f161979f5cb055a8a6d3d728b7db322422139cc28b60c716d107993a794cd86c`  
		Last Modified: Thu, 13 Apr 2023 13:46:15 GMT  
		Size: 32.1 MB (32068809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:91c315263bf6ce2500fa1b15cdb916c2c7e77a2e436dafde1788b40bc3105250
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42c37c658114d3d2893b096a54d2deab61f556eb08c89764d35cdf13faf7ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f4c3f72acab731ed4e440147b25e7d155c3d98eb8738b731250868ad184e54d9`  
		Last Modified: Thu, 13 Apr 2023 13:46:21 GMT  
		Size: 26.4 MB (26364733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:focal-20230412`

```console
$ docker pull ubuntu@sha256:db8bf6f4fb351aa7a26e27ba2686cf35a6a409f65603e59d4c203e58387dc6b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20230412` - linux; amd64

```console
$ docker pull ubuntu@sha256:b795f8e0caaaacad9859a9a38fe1c78154f8301fdaf0872eaf1520d66d9c0b98
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27504674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bd6891718934e63638d9ca0ecee018e69b638270fe04990a310e5c78ab4a92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca1778b6935686ad781c27472c4668fc61ec3aeb85494f72deb1921892b9d39e`  
		Last Modified: Thu, 13 Apr 2023 13:45:57 GMT  
		Size: 27.5 MB (27504674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230412` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:6de8d817428e3d064da83ce59b4dccf7c6749aa60b36a17ad6cc3b1f7d10123c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23609760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b1180d68d3d67c103b16d57b364242467c2eacbbe69a9ddc04dcf1cf801d75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:39f91c5e27647c786293528ceed473da81ca1f8e8a07bd92474a6d695bad1e22`  
		Last Modified: Thu, 13 Apr 2023 13:46:09 GMT  
		Size: 23.6 MB (23609760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230412` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:144e6a778925a0c11c4cd9fe5fce1172e620f215b0410bb43e7fa41bbcfe4522
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25972971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758cd4ebb2178eb0cd2ce78dea8ffad569f5bba415c4b33b694e891e7697e854`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8659cf1709ef03be2c0b2dc339b19432bff8a0753d2d7d53f47272f098f56ef4`  
		Last Modified: Thu, 13 Apr 2023 13:46:03 GMT  
		Size: 26.0 MB (25972971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230412` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:98fcf155d7d9fe687af0af87ccbe0dcc17338686504d341cf8a731499f40cf16
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32068809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd2848d7eadab46995f05c8e09edecfc3845d61e418304136f82bb9e22601d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f161979f5cb055a8a6d3d728b7db322422139cc28b60c716d107993a794cd86c`  
		Last Modified: Thu, 13 Apr 2023 13:46:15 GMT  
		Size: 32.1 MB (32068809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230412` - linux; s390x

```console
$ docker pull ubuntu@sha256:91c315263bf6ce2500fa1b15cdb916c2c7e77a2e436dafde1788b40bc3105250
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26364733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42c37c658114d3d2893b096a54d2deab61f556eb08c89764d35cdf13faf7ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f4c3f72acab731ed4e440147b25e7d155c3d98eb8738b731250868ad184e54d9`  
		Last Modified: Thu, 13 Apr 2023 13:46:21 GMT  
		Size: 26.4 MB (26364733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:ac58ff7fe25edc58bdf0067ca99df00014dbd032e2246d30a722fa348fd799a5
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
$ docker pull ubuntu@sha256:2fdb1cf4995abb74c035e5f520c0f3a46f12b3377a59e86ecca66d8606ad64f9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6ddc1b2547b2e38dc25b265ac585238a3c23da63976722864dab2a069c74f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:837dd4791cdc6f670708c3a570b72169263806d7ccc2783173b9e88f94878271`  
		Last Modified: Mon, 22 May 2023 18:07:29 GMT  
		Size: 29.5 MB (29534702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c80ed91cdc47229010c4f34f96c3442bc02dca260d0bf26f6c4b047ea7d11cf2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a5c81bff1484d6f6943eb15664ccf9027b66e59244258bee27737f9c50a521`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:52:13 GMT
ARG RELEASE
# Mon, 22 May 2023 17:52:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:52:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:52:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:52:16 GMT
ADD file:52b34a0d4198b5d30380eb1f293fb8916790394fcba96b4759a3f1beeb373b1a in / 
# Mon, 22 May 2023 17:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:68b5e8df6832be9e886e342be08257a6f07c071a6e82751005d3d72c4af06e55`  
		Last Modified: Mon, 22 May 2023 18:07:41 GMT  
		Size: 26.1 MB (26141405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:77bdd217935d10f0e753ed84118e9b11d3ab0a66a82bdf322087354ccd833733
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27349492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2767693332e5523a2734b82f57d1a91510c92237912a96fec46352785e120b3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:952b15bbc7fb957dead5972b258558130aeda588416c0a7a861e916fc08b36d7`  
		Last Modified: Mon, 22 May 2023 18:07:35 GMT  
		Size: 27.3 MB (27349492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:268686ba2c6284461cae1642d9d055e51b16f8e711d49b34638146b78050f5a0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34594849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea41887ad57d6a41c77497c1cc4bcec3195b67b7d73e2b7873ee46590b96672e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:39:12 GMT
ARG RELEASE
# Mon, 22 May 2023 17:39:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:39:16 GMT
ADD file:5b5967ce188eac9717526ca9f6cf6679cbae6ee4b17b207cc3d640c78d9a9788 in / 
# Mon, 22 May 2023 17:39:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2283df590faf676672db76cf3fd8c126945c8e86950777d8e306d757fbf82285`  
		Last Modified: Mon, 22 May 2023 18:07:47 GMT  
		Size: 34.6 MB (34594849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; s390x

```console
$ docker pull ubuntu@sha256:b0b966f885ea29d809d03d027c3d21182676380b241c3a271aa83f8e9d7bac06
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28017412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9175efc14fb0eb640de06d66d6ae157973afe75950f979e0aad3f8391f51320e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:46:45 GMT
ARG RELEASE
# Mon, 22 May 2023 17:46:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:46:47 GMT
ADD file:7bf1b7a1484e37f289d40f5c1c1cbe321ef337f898dd3d5809193c848a9a3dc2 in / 
# Mon, 22 May 2023 17:46:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8591eece70e54e483b384ce950218057ea0af677115b02a041579bf05da474ec`  
		Last Modified: Mon, 22 May 2023 18:07:55 GMT  
		Size: 28.0 MB (28017412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy-20230522`

```console
$ docker pull ubuntu@sha256:ac58ff7fe25edc58bdf0067ca99df00014dbd032e2246d30a722fa348fd799a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:jammy-20230522` - linux; amd64

```console
$ docker pull ubuntu@sha256:2fdb1cf4995abb74c035e5f520c0f3a46f12b3377a59e86ecca66d8606ad64f9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6ddc1b2547b2e38dc25b265ac585238a3c23da63976722864dab2a069c74f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:837dd4791cdc6f670708c3a570b72169263806d7ccc2783173b9e88f94878271`  
		Last Modified: Mon, 22 May 2023 18:07:29 GMT  
		Size: 29.5 MB (29534702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230522` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c80ed91cdc47229010c4f34f96c3442bc02dca260d0bf26f6c4b047ea7d11cf2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a5c81bff1484d6f6943eb15664ccf9027b66e59244258bee27737f9c50a521`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:52:13 GMT
ARG RELEASE
# Mon, 22 May 2023 17:52:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:52:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:52:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:52:16 GMT
ADD file:52b34a0d4198b5d30380eb1f293fb8916790394fcba96b4759a3f1beeb373b1a in / 
# Mon, 22 May 2023 17:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:68b5e8df6832be9e886e342be08257a6f07c071a6e82751005d3d72c4af06e55`  
		Last Modified: Mon, 22 May 2023 18:07:41 GMT  
		Size: 26.1 MB (26141405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230522` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:77bdd217935d10f0e753ed84118e9b11d3ab0a66a82bdf322087354ccd833733
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27349492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2767693332e5523a2734b82f57d1a91510c92237912a96fec46352785e120b3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:952b15bbc7fb957dead5972b258558130aeda588416c0a7a861e916fc08b36d7`  
		Last Modified: Mon, 22 May 2023 18:07:35 GMT  
		Size: 27.3 MB (27349492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230522` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:268686ba2c6284461cae1642d9d055e51b16f8e711d49b34638146b78050f5a0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34594849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea41887ad57d6a41c77497c1cc4bcec3195b67b7d73e2b7873ee46590b96672e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:39:12 GMT
ARG RELEASE
# Mon, 22 May 2023 17:39:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:39:16 GMT
ADD file:5b5967ce188eac9717526ca9f6cf6679cbae6ee4b17b207cc3d640c78d9a9788 in / 
# Mon, 22 May 2023 17:39:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2283df590faf676672db76cf3fd8c126945c8e86950777d8e306d757fbf82285`  
		Last Modified: Mon, 22 May 2023 18:07:47 GMT  
		Size: 34.6 MB (34594849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230522` - linux; s390x

```console
$ docker pull ubuntu@sha256:b0b966f885ea29d809d03d027c3d21182676380b241c3a271aa83f8e9d7bac06
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28017412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9175efc14fb0eb640de06d66d6ae157973afe75950f979e0aad3f8391f51320e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:46:45 GMT
ARG RELEASE
# Mon, 22 May 2023 17:46:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:46:47 GMT
ADD file:7bf1b7a1484e37f289d40f5c1c1cbe321ef337f898dd3d5809193c848a9a3dc2 in / 
# Mon, 22 May 2023 17:46:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8591eece70e54e483b384ce950218057ea0af677115b02a041579bf05da474ec`  
		Last Modified: Mon, 22 May 2023 18:07:55 GMT  
		Size: 28.0 MB (28017412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic`

```console
$ docker pull ubuntu@sha256:a9a425d086dbb34c1b5b99765596e2a3cc79b33826866c51cd4508d8eb327d2b
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
$ docker pull ubuntu@sha256:d69f6ed3c483abe6ed19d7310acacd14012fd62874ea98edccddf6ac7af3ce93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26695202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15f05d8742509cfc142f79dfe4cc2fa4e1b7bd20415675f7b52d3e22fd53670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0963d61c5d36e157f4d244438f1a5213d8590b724d49300d6df8ebf5d70342a9`  
		Last Modified: Fri, 14 Apr 2023 11:09:15 GMT  
		Size: 26.7 MB (26695202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9afa28d1eb80d78129debbef52b3f2a59b19479b2c15f01d16c2beeccd72dc10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781448a65e540dff394a6ae765d032b6c5fee3e0bc008f323330bd44a5aa797`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:049083b382db595e625c4760cee04d50fb6110bda597a3dd936406027ce01994`  
		Last Modified: Fri, 14 Apr 2023 11:09:28 GMT  
		Size: 25.1 MB (25067534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:9ff03c2930fce7e915f3b321c6c601380ffb845140bd36715c44ec31d7ae551e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25759013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490b20d4c90f834abcf386620a8906d21821aaa4db91c4665016883f043a10e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4bb7992c0b6c454d95752fadeb8ec30f02376e386e2dbcde466ab9e74283ed78`  
		Last Modified: Fri, 14 Apr 2023 11:09:21 GMT  
		Size: 25.8 MB (25759013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:56185868328c6dcfff4b9f97915a8868905668fa8ffab0b2b0285dac1dfd84cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa908635f261aa7b8aa52c329990cdc01c4716fdac960a6f3cfff6706f2b56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6864d2efca45377dbba7535ab73bb2a64f10d73c7d97bfbd768b173970bf455`  
		Last Modified: Fri, 14 Apr 2023 11:09:34 GMT  
		Size: 31.1 MB (31113926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; s390x

```console
$ docker pull ubuntu@sha256:3761fb8cb1cfa0facc994bb50e559e50144c999ff6ac5a43712396f98dd92045
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25488667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d1b46d5d955e3fbe7be0da291db9a566b03ebbac3335bca37d70d66078e9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:91664c4b18004c964fd7a8e4cc1d53adb98ce8158f5d0dde54befa1c1f754635`  
		Last Modified: Fri, 14 Apr 2023 11:09:40 GMT  
		Size: 25.5 MB (25488667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic-20230412`

```console
$ docker pull ubuntu@sha256:a9a425d086dbb34c1b5b99765596e2a3cc79b33826866c51cd4508d8eb327d2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:kinetic-20230412` - linux; amd64

```console
$ docker pull ubuntu@sha256:d69f6ed3c483abe6ed19d7310acacd14012fd62874ea98edccddf6ac7af3ce93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26695202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15f05d8742509cfc142f79dfe4cc2fa4e1b7bd20415675f7b52d3e22fd53670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0963d61c5d36e157f4d244438f1a5213d8590b724d49300d6df8ebf5d70342a9`  
		Last Modified: Fri, 14 Apr 2023 11:09:15 GMT  
		Size: 26.7 MB (26695202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230412` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9afa28d1eb80d78129debbef52b3f2a59b19479b2c15f01d16c2beeccd72dc10
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25067534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781448a65e540dff394a6ae765d032b6c5fee3e0bc008f323330bd44a5aa797`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:049083b382db595e625c4760cee04d50fb6110bda597a3dd936406027ce01994`  
		Last Modified: Fri, 14 Apr 2023 11:09:28 GMT  
		Size: 25.1 MB (25067534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230412` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:9ff03c2930fce7e915f3b321c6c601380ffb845140bd36715c44ec31d7ae551e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25759013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490b20d4c90f834abcf386620a8906d21821aaa4db91c4665016883f043a10e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4bb7992c0b6c454d95752fadeb8ec30f02376e386e2dbcde466ab9e74283ed78`  
		Last Modified: Fri, 14 Apr 2023 11:09:21 GMT  
		Size: 25.8 MB (25759013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230412` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:56185868328c6dcfff4b9f97915a8868905668fa8ffab0b2b0285dac1dfd84cf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31113926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaa908635f261aa7b8aa52c329990cdc01c4716fdac960a6f3cfff6706f2b56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6864d2efca45377dbba7535ab73bb2a64f10d73c7d97bfbd768b173970bf455`  
		Last Modified: Fri, 14 Apr 2023 11:09:34 GMT  
		Size: 31.1 MB (31113926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230412` - linux; s390x

```console
$ docker pull ubuntu@sha256:3761fb8cb1cfa0facc994bb50e559e50144c999ff6ac5a43712396f98dd92045
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25488667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1d1b46d5d955e3fbe7be0da291db9a566b03ebbac3335bca37d70d66078e9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:91664c4b18004c964fd7a8e4cc1d53adb98ce8158f5d0dde54befa1c1f754635`  
		Last Modified: Fri, 14 Apr 2023 11:09:40 GMT  
		Size: 25.5 MB (25488667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:ac58ff7fe25edc58bdf0067ca99df00014dbd032e2246d30a722fa348fd799a5
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
$ docker pull ubuntu@sha256:2fdb1cf4995abb74c035e5f520c0f3a46f12b3377a59e86ecca66d8606ad64f9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6ddc1b2547b2e38dc25b265ac585238a3c23da63976722864dab2a069c74f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:45:50 GMT
ARG RELEASE
# Mon, 22 May 2023 17:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:45:50 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:45:52 GMT
ADD file:2fd2684e989d275c95e18b6f6e9ccf57ca1382ecd8faf4a66961ede28102dedf in / 
# Mon, 22 May 2023 17:45:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:837dd4791cdc6f670708c3a570b72169263806d7ccc2783173b9e88f94878271`  
		Last Modified: Mon, 22 May 2023 18:07:29 GMT  
		Size: 29.5 MB (29534702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c80ed91cdc47229010c4f34f96c3442bc02dca260d0bf26f6c4b047ea7d11cf2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26141405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a5c81bff1484d6f6943eb15664ccf9027b66e59244258bee27737f9c50a521`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:52:13 GMT
ARG RELEASE
# Mon, 22 May 2023 17:52:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:52:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:52:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:52:16 GMT
ADD file:52b34a0d4198b5d30380eb1f293fb8916790394fcba96b4759a3f1beeb373b1a in / 
# Mon, 22 May 2023 17:52:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:68b5e8df6832be9e886e342be08257a6f07c071a6e82751005d3d72c4af06e55`  
		Last Modified: Mon, 22 May 2023 18:07:41 GMT  
		Size: 26.1 MB (26141405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:77bdd217935d10f0e753ed84118e9b11d3ab0a66a82bdf322087354ccd833733
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27349492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2767693332e5523a2734b82f57d1a91510c92237912a96fec46352785e120b3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:53:00 GMT
ARG RELEASE
# Mon, 22 May 2023 17:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:53:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:53:07 GMT
ADD file:f0435ed8dcf91cc69ec63b6b16d9efac56e5a6a7ec518e1fcc3df7457d3113ed in / 
# Mon, 22 May 2023 17:53:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:952b15bbc7fb957dead5972b258558130aeda588416c0a7a861e916fc08b36d7`  
		Last Modified: Mon, 22 May 2023 18:07:35 GMT  
		Size: 27.3 MB (27349492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:268686ba2c6284461cae1642d9d055e51b16f8e711d49b34638146b78050f5a0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34594849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea41887ad57d6a41c77497c1cc4bcec3195b67b7d73e2b7873ee46590b96672e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:39:12 GMT
ARG RELEASE
# Mon, 22 May 2023 17:39:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:39:16 GMT
ADD file:5b5967ce188eac9717526ca9f6cf6679cbae6ee4b17b207cc3d640c78d9a9788 in / 
# Mon, 22 May 2023 17:39:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2283df590faf676672db76cf3fd8c126945c8e86950777d8e306d757fbf82285`  
		Last Modified: Mon, 22 May 2023 18:07:47 GMT  
		Size: 34.6 MB (34594849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:b0b966f885ea29d809d03d027c3d21182676380b241c3a271aa83f8e9d7bac06
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.0 MB (28017412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9175efc14fb0eb640de06d66d6ae157973afe75950f979e0aad3f8391f51320e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 May 2023 17:46:45 GMT
ARG RELEASE
# Mon, 22 May 2023 17:46:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 22 May 2023 17:46:45 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 22 May 2023 17:46:47 GMT
ADD file:7bf1b7a1484e37f289d40f5c1c1cbe321ef337f898dd3d5809193c848a9a3dc2 in / 
# Mon, 22 May 2023 17:46:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8591eece70e54e483b384ce950218057ea0af677115b02a041579bf05da474ec`  
		Last Modified: Mon, 22 May 2023 18:07:55 GMT  
		Size: 28.0 MB (28017412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar`

```console
$ docker pull ubuntu@sha256:9279f41cc6e4df8f87b13ac17c2c6f2a280fd3ca2638d18f8dc94b774486909f
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
$ docker pull ubuntu@sha256:5ed6262a1edb954cae006b966ca70468e982285aa57419b4d2b221a5e11dd881
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d710383bd1efcb401c8e0aca2c596b3b93ab021d1e001b4e90c394af54773632`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 09:16:59 GMT
ARG RELEASE
# Tue, 23 May 2023 09:16:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 09:17:01 GMT
ADD file:6591237a72178b71d79f687b816ad23237fbef0bc3ec42332369d9e7bdaa04e4 in / 
# Tue, 23 May 2023 09:17:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:361237ddf358bcd8b864f2f24bd3d134262cb47ccd30556a7ba97c218f0b3435`  
		Last Modified: Tue, 23 May 2023 09:42:21 GMT  
		Size: 26.8 MB (26825631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f98df397a30936bc4bfcb205d125e9231c6c37077733c2d0a4683969c37e8d43
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24635016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f931f4d70204e5ec5f89bef40edce58b73434720c646e47508966c92562cb0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:12 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:12 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:16 GMT
ADD file:eff76586a1ef817ec09adc4b06a3656dccdfa9eaa17e0580677ed3315d37067b in / 
# Tue, 23 May 2023 08:33:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cec830e76152242e25efac1882b1fd0617ddb70bc9e22f6c702d0c76481a41cb`  
		Last Modified: Tue, 23 May 2023 09:42:32 GMT  
		Size: 24.6 MB (24635016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb688171cf562115f640d289507c9215b42f3c7f88c0c4783b7b5d833b21b477
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b605c4398aab9e1bb450ed620ae949978e2dd3ca158d7c124f4f7e1365364e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:45 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:47 GMT
ADD file:b2902a85ba60d642b00f2d7d7e4f56825749dca527e2d8d5e64d854c76ed28f0 in / 
# Tue, 23 May 2023 08:33:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8e6f677fb231e140748c758073ca5f3833b883f5762e43603976eba228cdaeb`  
		Last Modified: Tue, 23 May 2023 09:42:26 GMT  
		Size: 26.1 MB (26079431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dad6fefabb79c014fe82216113a9c5898e2c28a6fa16e5254856d907eb783bad
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb828ec9db7fa57d058990d9b984ad775b8704f411f1c8d9c919152e894d935`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:36:49 GMT
ARG RELEASE
# Tue, 23 May 2023 08:36:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:36:52 GMT
ADD file:d76035fa745d219f333adeb90e6eedc3b563dca64aa80c2fbe88d7389ba798d2 in / 
# Tue, 23 May 2023 08:36:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e0b93a5ca79f060115dd23deb777acddd707c28a75961b073aea5287cd2a5e8`  
		Last Modified: Tue, 23 May 2023 09:42:38 GMT  
		Size: 31.0 MB (31018854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; s390x

```console
$ docker pull ubuntu@sha256:ab66eeed2bf32c0326833749dbd50f63d0260d4b7be59dec88142b3ac44357c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25706387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1531d9864af82dc6f98e54333578b74c087e821c0ea4073d89993b89bfcef8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:34:39 GMT
ARG RELEASE
# Tue, 23 May 2023 08:34:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:34:41 GMT
ADD file:390d5b6c76bd6ae4f2901362d9a308f7dc4fa9a83574ec3952e867bc951c1552 in / 
# Tue, 23 May 2023 08:34:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b35c5f24ffbc70a87b2657a3f8b49a4c6030afe433a1a3a28ddff66e5bfc967`  
		Last Modified: Tue, 23 May 2023 09:42:44 GMT  
		Size: 25.7 MB (25706387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:lunar-20230522`

```console
$ docker pull ubuntu@sha256:9279f41cc6e4df8f87b13ac17c2c6f2a280fd3ca2638d18f8dc94b774486909f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:lunar-20230522` - linux; amd64

```console
$ docker pull ubuntu@sha256:5ed6262a1edb954cae006b966ca70468e982285aa57419b4d2b221a5e11dd881
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d710383bd1efcb401c8e0aca2c596b3b93ab021d1e001b4e90c394af54773632`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 09:16:59 GMT
ARG RELEASE
# Tue, 23 May 2023 09:16:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 09:17:01 GMT
ADD file:6591237a72178b71d79f687b816ad23237fbef0bc3ec42332369d9e7bdaa04e4 in / 
# Tue, 23 May 2023 09:17:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:361237ddf358bcd8b864f2f24bd3d134262cb47ccd30556a7ba97c218f0b3435`  
		Last Modified: Tue, 23 May 2023 09:42:21 GMT  
		Size: 26.8 MB (26825631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230522` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f98df397a30936bc4bfcb205d125e9231c6c37077733c2d0a4683969c37e8d43
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24635016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f931f4d70204e5ec5f89bef40edce58b73434720c646e47508966c92562cb0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:12 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:12 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:16 GMT
ADD file:eff76586a1ef817ec09adc4b06a3656dccdfa9eaa17e0580677ed3315d37067b in / 
# Tue, 23 May 2023 08:33:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cec830e76152242e25efac1882b1fd0617ddb70bc9e22f6c702d0c76481a41cb`  
		Last Modified: Tue, 23 May 2023 09:42:32 GMT  
		Size: 24.6 MB (24635016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230522` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb688171cf562115f640d289507c9215b42f3c7f88c0c4783b7b5d833b21b477
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b605c4398aab9e1bb450ed620ae949978e2dd3ca158d7c124f4f7e1365364e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:45 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:47 GMT
ADD file:b2902a85ba60d642b00f2d7d7e4f56825749dca527e2d8d5e64d854c76ed28f0 in / 
# Tue, 23 May 2023 08:33:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8e6f677fb231e140748c758073ca5f3833b883f5762e43603976eba228cdaeb`  
		Last Modified: Tue, 23 May 2023 09:42:26 GMT  
		Size: 26.1 MB (26079431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230522` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dad6fefabb79c014fe82216113a9c5898e2c28a6fa16e5254856d907eb783bad
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb828ec9db7fa57d058990d9b984ad775b8704f411f1c8d9c919152e894d935`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:36:49 GMT
ARG RELEASE
# Tue, 23 May 2023 08:36:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:36:52 GMT
ADD file:d76035fa745d219f333adeb90e6eedc3b563dca64aa80c2fbe88d7389ba798d2 in / 
# Tue, 23 May 2023 08:36:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e0b93a5ca79f060115dd23deb777acddd707c28a75961b073aea5287cd2a5e8`  
		Last Modified: Tue, 23 May 2023 09:42:38 GMT  
		Size: 31.0 MB (31018854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230522` - linux; s390x

```console
$ docker pull ubuntu@sha256:ab66eeed2bf32c0326833749dbd50f63d0260d4b7be59dec88142b3ac44357c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25706387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1531d9864af82dc6f98e54333578b74c087e821c0ea4073d89993b89bfcef8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:34:39 GMT
ARG RELEASE
# Tue, 23 May 2023 08:34:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:34:41 GMT
ADD file:390d5b6c76bd6ae4f2901362d9a308f7dc4fa9a83574ec3952e867bc951c1552 in / 
# Tue, 23 May 2023 08:34:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b35c5f24ffbc70a87b2657a3f8b49a4c6030afe433a1a3a28ddff66e5bfc967`  
		Last Modified: Tue, 23 May 2023 09:42:44 GMT  
		Size: 25.7 MB (25706387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:2cde79b4627d38d1448fc264f93e465f18b653bc9a62ee8ec85d99d4e8f39d4c
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
$ docker pull ubuntu@sha256:2977bee81d7883ef1cbeb369d8d2afc21da7977f99e347cf1931c586f7045fee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26880446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e51849785d31c2fe2fd3b45020f7d55aedd165869d0131effe6feb29f17ed9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:41 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:41 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:43 GMT
ADD file:6bd9b5983097734c3050b464660da9015c0e2f93416920b8404ff7d28d8bccd8 in / 
# Sat, 20 May 2023 16:58:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f2131a27ab9c8a2c55e5a33ce861393bf5934a64d16b508f4532a8e749937df7`  
		Last Modified: Sat, 20 May 2023 17:08:21 GMT  
		Size: 26.9 MB (26880446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:af6575b7dfc5526ba8710a748349ed01f849cfbcd11123d86293360284ed0558
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24569382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0252db62febe6af452e6991741e6f20b6d5d6b97c100af170ce4fdbf21655717`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:22 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:25 GMT
ADD file:c7522b8ff46586b3057c8eae94d6cfc77299a4f2ccc3762e6263780ccc7c82c0 in / 
# Sat, 20 May 2023 16:58:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c5174d07727ff19811fe8f7e76bbe8d175a16bcb423918a5e34cba75b7de22dd`  
		Last Modified: Sat, 20 May 2023 17:08:34 GMT  
		Size: 24.6 MB (24569382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ab607dfa49b79e0d99b2061d507dc2e7dc4c35cc53170749ad512d5a224e5b6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26099857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc8a176a7255f169a5952b707290db97b5117aeff26d79fb31091d9e4887030`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:34 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:36 GMT
ADD file:39dff3364ce4bb79539ed5e58493be16a66d424e605cb774559830ba8452bc4d in / 
# Sat, 20 May 2023 16:59:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2f6eed94ce9d338a3640a267747fa4c20b312670df4c690d4412a873474d9345`  
		Last Modified: Sat, 20 May 2023 17:08:28 GMT  
		Size: 26.1 MB (26099857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d461cdc8a2fb842dc2f8ba0789368db6d3b9bd8493f56a8b035e85bb144b8218
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30918336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7067ffebf34c75aaa5a5cc7f9027b0ea2bdf92950f3e54d1183648b0796d7955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:51 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:51 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:54 GMT
ADD file:83fb0f5b40d9233c6017f5c5a9e51e184b8f56b03c54fafa207e9ca28aa2df52 in / 
# Sat, 20 May 2023 16:58:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1322522d35b297f2cf89ef1cb25b604a3ec335526102b1194ea3cac1eda2eee7`  
		Last Modified: Sat, 20 May 2023 17:08:40 GMT  
		Size: 30.9 MB (30918336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; s390x

```console
$ docker pull ubuntu@sha256:b2c200b149a4e921a060610533f68a963a408bc84c577b8ba20b48a92d0f95fa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25698480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da1786faa70195e4008ab4d55834d2c10535f234b350eb74843b9a3f28d9739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:20 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:22 GMT
ADD file:fb602b3f6c251d8267de1cf0525d0b38aab5966c848182d037bb2890557f0a6e in / 
# Sat, 20 May 2023 16:59:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dabe55d229048645c6b502641876395c6a479819d8566c06fa2d15b894e68605`  
		Last Modified: Sat, 20 May 2023 17:08:47 GMT  
		Size: 25.7 MB (25698480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic-20230520`

```console
$ docker pull ubuntu@sha256:2cde79b4627d38d1448fc264f93e465f18b653bc9a62ee8ec85d99d4e8f39d4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:mantic-20230520` - linux; amd64

```console
$ docker pull ubuntu@sha256:2977bee81d7883ef1cbeb369d8d2afc21da7977f99e347cf1931c586f7045fee
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26880446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e51849785d31c2fe2fd3b45020f7d55aedd165869d0131effe6feb29f17ed9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:41 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:41 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:43 GMT
ADD file:6bd9b5983097734c3050b464660da9015c0e2f93416920b8404ff7d28d8bccd8 in / 
# Sat, 20 May 2023 16:58:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f2131a27ab9c8a2c55e5a33ce861393bf5934a64d16b508f4532a8e749937df7`  
		Last Modified: Sat, 20 May 2023 17:08:21 GMT  
		Size: 26.9 MB (26880446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230520` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:af6575b7dfc5526ba8710a748349ed01f849cfbcd11123d86293360284ed0558
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24569382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0252db62febe6af452e6991741e6f20b6d5d6b97c100af170ce4fdbf21655717`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:22 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:25 GMT
ADD file:c7522b8ff46586b3057c8eae94d6cfc77299a4f2ccc3762e6263780ccc7c82c0 in / 
# Sat, 20 May 2023 16:58:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c5174d07727ff19811fe8f7e76bbe8d175a16bcb423918a5e34cba75b7de22dd`  
		Last Modified: Sat, 20 May 2023 17:08:34 GMT  
		Size: 24.6 MB (24569382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230520` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ab607dfa49b79e0d99b2061d507dc2e7dc4c35cc53170749ad512d5a224e5b6f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26099857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc8a176a7255f169a5952b707290db97b5117aeff26d79fb31091d9e4887030`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:34 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:36 GMT
ADD file:39dff3364ce4bb79539ed5e58493be16a66d424e605cb774559830ba8452bc4d in / 
# Sat, 20 May 2023 16:59:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2f6eed94ce9d338a3640a267747fa4c20b312670df4c690d4412a873474d9345`  
		Last Modified: Sat, 20 May 2023 17:08:28 GMT  
		Size: 26.1 MB (26099857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230520` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:d461cdc8a2fb842dc2f8ba0789368db6d3b9bd8493f56a8b035e85bb144b8218
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 MB (30918336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7067ffebf34c75aaa5a5cc7f9027b0ea2bdf92950f3e54d1183648b0796d7955`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:51 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:51 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:54 GMT
ADD file:83fb0f5b40d9233c6017f5c5a9e51e184b8f56b03c54fafa207e9ca28aa2df52 in / 
# Sat, 20 May 2023 16:58:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1322522d35b297f2cf89ef1cb25b604a3ec335526102b1194ea3cac1eda2eee7`  
		Last Modified: Sat, 20 May 2023 17:08:40 GMT  
		Size: 30.9 MB (30918336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230520` - linux; s390x

```console
$ docker pull ubuntu@sha256:b2c200b149a4e921a060610533f68a963a408bc84c577b8ba20b48a92d0f95fa
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25698480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da1786faa70195e4008ab4d55834d2c10535f234b350eb74843b9a3f28d9739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:20 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:22 GMT
ADD file:fb602b3f6c251d8267de1cf0525d0b38aab5966c848182d037bb2890557f0a6e in / 
# Sat, 20 May 2023 16:59:22 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:dabe55d229048645c6b502641876395c6a479819d8566c06fa2d15b894e68605`  
		Last Modified: Sat, 20 May 2023 17:08:47 GMT  
		Size: 25.7 MB (25698480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:9279f41cc6e4df8f87b13ac17c2c6f2a280fd3ca2638d18f8dc94b774486909f
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
$ docker pull ubuntu@sha256:5ed6262a1edb954cae006b966ca70468e982285aa57419b4d2b221a5e11dd881
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26825631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d710383bd1efcb401c8e0aca2c596b3b93ab021d1e001b4e90c394af54773632`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 09:16:59 GMT
ARG RELEASE
# Tue, 23 May 2023 09:16:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 09:16:59 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 09:17:01 GMT
ADD file:6591237a72178b71d79f687b816ad23237fbef0bc3ec42332369d9e7bdaa04e4 in / 
# Tue, 23 May 2023 09:17:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:361237ddf358bcd8b864f2f24bd3d134262cb47ccd30556a7ba97c218f0b3435`  
		Last Modified: Tue, 23 May 2023 09:42:21 GMT  
		Size: 26.8 MB (26825631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:f98df397a30936bc4bfcb205d125e9231c6c37077733c2d0a4683969c37e8d43
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24635016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f931f4d70204e5ec5f89bef40edce58b73434720c646e47508966c92562cb0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:12 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:12 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:16 GMT
ADD file:eff76586a1ef817ec09adc4b06a3656dccdfa9eaa17e0580677ed3315d37067b in / 
# Tue, 23 May 2023 08:33:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cec830e76152242e25efac1882b1fd0617ddb70bc9e22f6c702d0c76481a41cb`  
		Last Modified: Tue, 23 May 2023 09:42:32 GMT  
		Size: 24.6 MB (24635016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:fb688171cf562115f640d289507c9215b42f3c7f88c0c4783b7b5d833b21b477
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26079431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b605c4398aab9e1bb450ed620ae949978e2dd3ca158d7c124f4f7e1365364e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:45 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:47 GMT
ADD file:b2902a85ba60d642b00f2d7d7e4f56825749dca527e2d8d5e64d854c76ed28f0 in / 
# Tue, 23 May 2023 08:33:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d8e6f677fb231e140748c758073ca5f3833b883f5762e43603976eba228cdaeb`  
		Last Modified: Tue, 23 May 2023 09:42:26 GMT  
		Size: 26.1 MB (26079431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:dad6fefabb79c014fe82216113a9c5898e2c28a6fa16e5254856d907eb783bad
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31018854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb828ec9db7fa57d058990d9b984ad775b8704f411f1c8d9c919152e894d935`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:36:49 GMT
ARG RELEASE
# Tue, 23 May 2023 08:36:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:36:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:36:52 GMT
ADD file:d76035fa745d219f333adeb90e6eedc3b563dca64aa80c2fbe88d7389ba798d2 in / 
# Tue, 23 May 2023 08:36:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e0b93a5ca79f060115dd23deb777acddd707c28a75961b073aea5287cd2a5e8`  
		Last Modified: Tue, 23 May 2023 09:42:38 GMT  
		Size: 31.0 MB (31018854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:ab66eeed2bf32c0326833749dbd50f63d0260d4b7be59dec88142b3ac44357c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25706387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1531d9864af82dc6f98e54333578b74c087e821c0ea4073d89993b89bfcef8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:34:39 GMT
ARG RELEASE
# Tue, 23 May 2023 08:34:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:34:41 GMT
ADD file:390d5b6c76bd6ae4f2901362d9a308f7dc4fa9a83574ec3952e867bc951c1552 in / 
# Tue, 23 May 2023 08:34:41 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b35c5f24ffbc70a87b2657a3f8b49a4c6030afe433a1a3a28ddff66e5bfc967`  
		Last Modified: Tue, 23 May 2023 09:42:44 GMT  
		Size: 25.7 MB (25706387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
