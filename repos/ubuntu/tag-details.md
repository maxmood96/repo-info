<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:22.04`](#ubuntu2204)
-	[`ubuntu:22.10`](#ubuntu2210)
-	[`ubuntu:23.04`](#ubuntu2304)
-	[`ubuntu:23.10`](#ubuntu2310)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20230605`](#ubuntufocal-20230605)
-	[`ubuntu:jammy`](#ubuntujammy)
-	[`ubuntu:jammy-20230605`](#ubuntujammy-20230605)
-	[`ubuntu:kinetic`](#ubuntukinetic)
-	[`ubuntu:kinetic-20230605`](#ubuntukinetic-20230605)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:lunar`](#ubuntulunar)
-	[`ubuntu:lunar-20230615`](#ubuntulunar-20230615)
-	[`ubuntu:mantic`](#ubuntumantic)
-	[`ubuntu:mantic-20230607`](#ubuntumantic-20230607)
-	[`ubuntu:rolling`](#ubunturolling)

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:a283507f25d2cd01d60594bb6e7dcae568e3248b359fe39461ffbd80327b6cdf
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
$ docker pull ubuntu@sha256:554e40b15453c788ec799badf0f1ad05c3e5c735b53f940feb8f27cf2ec570c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27506421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626a42b93d93241a6a48d81d921934891f73185547833a64dde06599cf3eafc2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:56e0351b98767487b3c411034be95479ed1710bb6be860db6df0be3a98653027`  
		Last Modified: Mon, 05 Jun 2023 17:26:33 GMT  
		Size: 27.5 MB (27506421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:3831296f7467818605f4c8782b1a74a3488547102640e9cb8b41c42b44e7f526
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef263d65a04f7a877f4868d790eef952ec3a69e4143477edc9f3cc80c4f9c43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:19:26 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:19:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:19:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:19:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:19:31 GMT
ADD file:114d6f55f8c1c4ec7f7d2ba3c803116a188eece1d1b6dbb3bb40c11082194234 in / 
# Mon, 05 Jun 2023 17:19:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f6069ed163b7975b49dc9e8925a15a02473293dca6513363fb11c08764520b8`  
		Last Modified: Mon, 05 Jun 2023 17:26:46 GMT  
		Size: 23.6 MB (23611936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ebdb7ac21fef61242b87d8d00ca0d3f4434c5adf360e771dc1b8db0f75771759
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a494d051d6a9c0e46123cfc516acb84b76884f21684764c166ecf4fe92a7fa4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:07:59 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:07:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:02 GMT
ADD file:6c0661b94e27ede70ca2a8842bdab5bc26b9ae4760b17870eda9d595672795ff in / 
# Mon, 05 Jun 2023 17:08:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb0a6f6b1798ce3ee565023c3a50777fff89bf6761a0985c8ff93aa903f7d0f1`  
		Last Modified: Mon, 05 Jun 2023 17:26:40 GMT  
		Size: 26.0 MB (25974252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1b176384bc513bb425b497364f1d6353ac1b285d48862c22a9b7c450c431d4bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cad30b7d8589358e8074d6fb495d774d8c52cfa8ab35ed10f518a2c8b7586c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:24 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:25 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:28 GMT
ADD file:0a2372ac4d43f0f4ada2b55dd0a359df73a828a9aa9426bfdd05a02b9c4b2bd9 in / 
# Mon, 05 Jun 2023 17:08:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a42700f678f7c62f7053fbbd2b046ac1742685ac4262717c9c6db8a8e872884d`  
		Last Modified: Mon, 05 Jun 2023 17:26:52 GMT  
		Size: 32.1 MB (32070916 bytes)  
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
$ docker pull ubuntu@sha256:2a357c4bd54822267339e601ae86ee3966723bdbcae640a70ace622cc9470c83
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
$ docker pull ubuntu@sha256:83f0c2a8d6f266d687d55b5cb1cb2201148eb7ac449e4202d9646b9083f1cee0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99284ca6cea039c7784d1414608c6e846dd56830c2a13e1341be681c3ffcc8ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b851dcae6ca1461dde247915abc5048061f34332929ca8fb37d9dc18f2e2f44`  
		Last Modified: Mon, 05 Jun 2023 17:20:26 GMT  
		Size: 29.5 MB (29533050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9aa2ce874cc0d140b3344fb6125d0ef540d347bca8a13c2270ca1c7a40490be3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3681d7421d4545f9eb7b1aabcb24b041b347b37705f89a858f831b94d8e2f0bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 16:59:35 GMT
ARG RELEASE
# Mon, 05 Jun 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 16:59:40 GMT
ADD file:5425962ced738173a50965fc5cd95c79d0a319323df4a34e9da3f5037a5264c3 in / 
# Mon, 05 Jun 2023 16:59:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ceecae09ee56d3fb7d5d26ff9505f3aa7e7cc5e54545fbecde69ef046b84f1c`  
		Last Modified: Mon, 05 Jun 2023 17:20:38 GMT  
		Size: 26.1 MB (26140710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:25de8a960c338b7d38aa15c012ceee70d8e29239db97596d6ecc50a5085d8f7a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27346742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb01e8e31210c9bfc5412c3fc1b8b7aea849bc2a9c21f47553bd31cc8fd79f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b2837baf7808226f588fabacb30598287e02d4dbf120eaf968c5299a6c2e9619`  
		Last Modified: Mon, 05 Jun 2023 17:20:32 GMT  
		Size: 27.3 MB (27346742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:eb4e647121c71cc9305e466d9c844a1207f90bab2e689310050e66e8b4f4d534
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16fc5784936f704a4bd8208deeb624554aeb2cdab87301aab60391db8f7ec590`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d3c256ab34973cfc9065065e684e5e5d1dac1eeb77974324e0de68944af26f62`  
		Last Modified: Mon, 05 Jun 2023 17:20:44 GMT  
		Size: 34.6 MB (34591237 bytes)  
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
$ docker pull ubuntu@sha256:a8c0aec3712a0562dc0ecfeeeae4e3de05fefb555b02c06778f69858d30c3bac
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
$ docker pull ubuntu@sha256:80fb4ea0c0a384a3072a6be1879c342bb636b0d105209535ba893ba75ab38ede
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26704595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39f297e9dda29a8d8896051c30f32feb52c9dcfb68e8a561650a1dde97cc94b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:02:32 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:02:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:02:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:02:32 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:02:34 GMT
ADD file:f8bb312bf73c62343d91c9988d58945c5d0fced3f559b95c4dd21a19183d933d in / 
# Mon, 05 Jun 2023 17:02:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:317e06b63fc01feacb4fa7a967d3a8c6fd35296935c83caa85ad28cd20add12b`  
		Last Modified: Mon, 05 Jun 2023 17:21:29 GMT  
		Size: 26.7 MB (26704595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:5dc1502337b177771dd9904822cde9abd2b26ee4014a3c6df7e912a9ef103db3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25098670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1120758c0ceafe38a213551ecf496a3b05011b323c13e36840d566b2ee02416d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:04:06 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:04:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:04:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:04:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:04:15 GMT
ADD file:615be72e62c21704af356d6cfd4e32a7df8dd4b93d0c3ee3ea2e1641127c54ea in / 
# Mon, 05 Jun 2023 17:04:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7eb2ece7978deb374e0aa4623aa1a44d513c34c7a56e23251a0dfbba314ea260`  
		Last Modified: Mon, 05 Jun 2023 17:21:41 GMT  
		Size: 25.1 MB (25098670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:dde2a31e58d07b2ed8be842eafae55b9a46b3629a0915dd6438fb3e484e46d65
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25770482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172adc9ce1cab441186106c04f9663f7b81edc9d3e8908b8dca58180df27ea16`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:02:45 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:02:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:02:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:02:46 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:02:50 GMT
ADD file:b85182b4593c262faef116755e01baa608e8090e1cb697d735485ff0bd5b353e in / 
# Mon, 05 Jun 2023 17:02:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bb573a4d6d791b5d50f1118d01e4c9b2acc927522cec8740ac9957e37eeac29c`  
		Last Modified: Mon, 05 Jun 2023 17:21:35 GMT  
		Size: 25.8 MB (25770482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:22.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b2a4b994153a43ab4941ab8efbc43c189d0c76b9fe4f8dee9f8449cd6ed83d93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31112867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a632c9634c258b38d044be3dfa48ee0aee70c82531def42c6e701c10e15989`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:10:48 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:10:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:10:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:10:48 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:10:52 GMT
ADD file:48c30fe281554302bb6533dd33a43a0877851ac5ba59dc3aff3d3d9ceae6f8a9 in / 
# Mon, 05 Jun 2023 17:10:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e4485626c4310d83f6d257d7c30db7a4fc23c70b98dec3ca37108fef26207e3c`  
		Last Modified: Mon, 05 Jun 2023 17:21:47 GMT  
		Size: 31.1 MB (31112867 bytes)  
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
$ docker pull ubuntu@sha256:23966ecd49ebe3dd30c73ccc79afc423d53a994a95ecb000c9d0c9bfcb05e3cb
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
$ docker pull ubuntu@sha256:09f035f46361d193ded647342903b413d57d05cc06acff8285f9dda9f2d269d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed313b0551f6255bb9ea7fd953363f0f306d9e2e92dc9fb94cbdf70e3dafb6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:28:38 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:28:39 GMT
ADD file:708314051e878a0c6071fb2c8d4458a04ce058f47f2cfaa58c1b5a42e837ca0f in / 
# Thu, 15 Jun 2023 08:28:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a9d46cc3977f1066a9dd08f845b76f7f7d46e4ef74fdf8ed1f4db514ea5a45d`  
		Last Modified: Thu, 15 Jun 2023 09:08:28 GMT  
		Size: 26.8 MB (26836883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:98e3a45616c77d754ce50a12634c507cecf9b53ccb2f48e94b20db7b4b698618
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24636364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678dff67c6b9c6ec4eaccccccd2ffae1ddbf85b5e5309ac56522d7442f3f8c2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb49e82a48f62b12a885a1a02ae80f5261ab51e3f138c0190fc8d119247fd11c`  
		Last Modified: Thu, 15 Jun 2023 09:08:40 GMT  
		Size: 24.6 MB (24636364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2ea9408d05cc2543752070f336452eda81593c2001f9931a0451bad3a45d3a31
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b331a8a5e1bb537caa9a8e3d3f6308563136db02ab0501499e819e36d9f48a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:33:24 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:33:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:33:58 GMT
ADD file:064ac1f238394a53372e0db107e28835aa3c39ed189a15fe85c532bbb50bfbaf in / 
# Thu, 15 Jun 2023 08:33:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8382a46db1cf2ede3739a9337cad793e2228c0e455f8969bbbc14b4d6f28e`  
		Last Modified: Thu, 15 Jun 2023 09:08:34 GMT  
		Size: 26.1 MB (26088803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cac0b3657eb2260df362c4949ec416d6377b36d5c2999e1765874dcbadeca4cd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31029474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0d4e75ccb4b903cf3c7d3515fdbbe2462a8043abbcf13667b6f860fc11302e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:29:14 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:29:17 GMT
ADD file:5ebdf4bd4bc2b27019f20fb1964a395fa504d4f20e208c54237e363895b492d7 in / 
# Thu, 15 Jun 2023 08:29:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:223122c533fb03fa9f10684bc8fb23adf1f08af994530d4c9403f9086da8952b`  
		Last Modified: Thu, 15 Jun 2023 09:08:47 GMT  
		Size: 31.0 MB (31029474 bytes)  
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
$ docker pull ubuntu@sha256:93c55b20cc3b34b0492ea90fe2fad93f1dfba56005bb56ba9bcc3f83d6495c16
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
$ docker pull ubuntu@sha256:07460e809a7141b84050c6d68220c1f7e2aa58b0bc124c40a1440988bfd87e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26931867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0fd6ed554b4fa85755cd2f9fefc45a1bff5e640b1090f4573997837f6c46b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:39:09 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:39:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:39:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:39:09 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:39:10 GMT
ADD file:d8dc8c4236b9885e64ccd27399ed8dddab7d39915d76378527cb730855aba0e1 in / 
# Wed, 07 Jun 2023 04:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a3cc0ea50b9aef0e9b8b228c37edf92b0dfcb177d34ed50433918ae5eec172be`  
		Last Modified: Wed, 07 Jun 2023 04:57:40 GMT  
		Size: 26.9 MB (26931867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bf18ca0b049d010b72c35574c0261ef9c231fffb7588709e05a6b807c081e552
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24478190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eabbb20f267b27e88fe450b3d209313994eeb87c19d8cbdec2b2f8e821a1ce5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:07 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:12 GMT
ADD file:65e05498800189bf1f48f5c6df21d144e18e5e069db55d0b88d45c04cc1fe4de in / 
# Wed, 07 Jun 2023 04:48:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df4275b0f8f556aa5462a1fad0a0a188bc3d7b287bc6120389314f6b9bd6566e`  
		Last Modified: Wed, 07 Jun 2023 04:57:51 GMT  
		Size: 24.5 MB (24478190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d9c68082dd554f1adf3ed6169d08f0aae5431b4a7bddb8c19951eae6bd607097
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26131158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a27f5fa4b6e23e37d77cb2410d8f9efb5a9f5698e10bf3aef9bb503b14497d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:42:14 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:42:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:42:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:42:14 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:42:16 GMT
ADD file:3f4faed988a03b7d05aefe677906592aade4d2bae1ec3f7055c1f10744a38de0 in / 
# Wed, 07 Jun 2023 04:42:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f698dd1f118f52521a462f35505a0bca0dc8a7e17802e11146a6c0acfbfc797d`  
		Last Modified: Wed, 07 Jun 2023 04:57:46 GMT  
		Size: 26.1 MB (26131158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:23.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8d9660ab5ab6a35050e6f5ac4ff4170e85c1e6776e83d075f9331b85215b96a4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30966286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4004a6116d82330c1bb10006b89dcfb699827cd79a405a16dd59e3e33889d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:25 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:26 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:28 GMT
ADD file:6cf1bffac55b7de64803fabdb35baf75349cc0a40c0b4c68ac2690b7123edc85 in / 
# Wed, 07 Jun 2023 04:48:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:537eb27ff37d9fd24f7097996a5a0ed640152c3656390c06baff05ecd549d691`  
		Last Modified: Wed, 07 Jun 2023 04:57:57 GMT  
		Size: 31.0 MB (30966286 bytes)  
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

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:93c55b20cc3b34b0492ea90fe2fad93f1dfba56005bb56ba9bcc3f83d6495c16
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
$ docker pull ubuntu@sha256:07460e809a7141b84050c6d68220c1f7e2aa58b0bc124c40a1440988bfd87e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26931867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0fd6ed554b4fa85755cd2f9fefc45a1bff5e640b1090f4573997837f6c46b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:39:09 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:39:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:39:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:39:09 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:39:10 GMT
ADD file:d8dc8c4236b9885e64ccd27399ed8dddab7d39915d76378527cb730855aba0e1 in / 
# Wed, 07 Jun 2023 04:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a3cc0ea50b9aef0e9b8b228c37edf92b0dfcb177d34ed50433918ae5eec172be`  
		Last Modified: Wed, 07 Jun 2023 04:57:40 GMT  
		Size: 26.9 MB (26931867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bf18ca0b049d010b72c35574c0261ef9c231fffb7588709e05a6b807c081e552
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24478190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eabbb20f267b27e88fe450b3d209313994eeb87c19d8cbdec2b2f8e821a1ce5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:07 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:12 GMT
ADD file:65e05498800189bf1f48f5c6df21d144e18e5e069db55d0b88d45c04cc1fe4de in / 
# Wed, 07 Jun 2023 04:48:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df4275b0f8f556aa5462a1fad0a0a188bc3d7b287bc6120389314f6b9bd6566e`  
		Last Modified: Wed, 07 Jun 2023 04:57:51 GMT  
		Size: 24.5 MB (24478190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d9c68082dd554f1adf3ed6169d08f0aae5431b4a7bddb8c19951eae6bd607097
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26131158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a27f5fa4b6e23e37d77cb2410d8f9efb5a9f5698e10bf3aef9bb503b14497d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:42:14 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:42:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:42:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:42:14 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:42:16 GMT
ADD file:3f4faed988a03b7d05aefe677906592aade4d2bae1ec3f7055c1f10744a38de0 in / 
# Wed, 07 Jun 2023 04:42:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f698dd1f118f52521a462f35505a0bca0dc8a7e17802e11146a6c0acfbfc797d`  
		Last Modified: Wed, 07 Jun 2023 04:57:46 GMT  
		Size: 26.1 MB (26131158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8d9660ab5ab6a35050e6f5ac4ff4170e85c1e6776e83d075f9331b85215b96a4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30966286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4004a6116d82330c1bb10006b89dcfb699827cd79a405a16dd59e3e33889d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:25 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:26 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:28 GMT
ADD file:6cf1bffac55b7de64803fabdb35baf75349cc0a40c0b4c68ac2690b7123edc85 in / 
# Wed, 07 Jun 2023 04:48:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:537eb27ff37d9fd24f7097996a5a0ed640152c3656390c06baff05ecd549d691`  
		Last Modified: Wed, 07 Jun 2023 04:57:57 GMT  
		Size: 31.0 MB (30966286 bytes)  
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
$ docker pull ubuntu@sha256:a283507f25d2cd01d60594bb6e7dcae568e3248b359fe39461ffbd80327b6cdf
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
$ docker pull ubuntu@sha256:554e40b15453c788ec799badf0f1ad05c3e5c735b53f940feb8f27cf2ec570c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27506421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626a42b93d93241a6a48d81d921934891f73185547833a64dde06599cf3eafc2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:56e0351b98767487b3c411034be95479ed1710bb6be860db6df0be3a98653027`  
		Last Modified: Mon, 05 Jun 2023 17:26:33 GMT  
		Size: 27.5 MB (27506421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:3831296f7467818605f4c8782b1a74a3488547102640e9cb8b41c42b44e7f526
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef263d65a04f7a877f4868d790eef952ec3a69e4143477edc9f3cc80c4f9c43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:19:26 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:19:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:19:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:19:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:19:31 GMT
ADD file:114d6f55f8c1c4ec7f7d2ba3c803116a188eece1d1b6dbb3bb40c11082194234 in / 
# Mon, 05 Jun 2023 17:19:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f6069ed163b7975b49dc9e8925a15a02473293dca6513363fb11c08764520b8`  
		Last Modified: Mon, 05 Jun 2023 17:26:46 GMT  
		Size: 23.6 MB (23611936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ebdb7ac21fef61242b87d8d00ca0d3f4434c5adf360e771dc1b8db0f75771759
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a494d051d6a9c0e46123cfc516acb84b76884f21684764c166ecf4fe92a7fa4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:07:59 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:07:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:02 GMT
ADD file:6c0661b94e27ede70ca2a8842bdab5bc26b9ae4760b17870eda9d595672795ff in / 
# Mon, 05 Jun 2023 17:08:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb0a6f6b1798ce3ee565023c3a50777fff89bf6761a0985c8ff93aa903f7d0f1`  
		Last Modified: Mon, 05 Jun 2023 17:26:40 GMT  
		Size: 26.0 MB (25974252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1b176384bc513bb425b497364f1d6353ac1b285d48862c22a9b7c450c431d4bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cad30b7d8589358e8074d6fb495d774d8c52cfa8ab35ed10f518a2c8b7586c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:24 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:25 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:28 GMT
ADD file:0a2372ac4d43f0f4ada2b55dd0a359df73a828a9aa9426bfdd05a02b9c4b2bd9 in / 
# Mon, 05 Jun 2023 17:08:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a42700f678f7c62f7053fbbd2b046ac1742685ac4262717c9c6db8a8e872884d`  
		Last Modified: Mon, 05 Jun 2023 17:26:52 GMT  
		Size: 32.1 MB (32070916 bytes)  
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

## `ubuntu:focal-20230605`

```console
$ docker pull ubuntu@sha256:a4165387d2c3cb47e913959895d7e5d9b32615dbc1e384998ed76989040eb655
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `ubuntu:focal-20230605` - linux; amd64

```console
$ docker pull ubuntu@sha256:554e40b15453c788ec799badf0f1ad05c3e5c735b53f940feb8f27cf2ec570c5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27506421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626a42b93d93241a6a48d81d921934891f73185547833a64dde06599cf3eafc2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:56e0351b98767487b3c411034be95479ed1710bb6be860db6df0be3a98653027`  
		Last Modified: Mon, 05 Jun 2023 17:26:33 GMT  
		Size: 27.5 MB (27506421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230605` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:3831296f7467818605f4c8782b1a74a3488547102640e9cb8b41c42b44e7f526
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23611936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef263d65a04f7a877f4868d790eef952ec3a69e4143477edc9f3cc80c4f9c43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:19:26 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:19:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:19:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:19:27 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:19:31 GMT
ADD file:114d6f55f8c1c4ec7f7d2ba3c803116a188eece1d1b6dbb3bb40c11082194234 in / 
# Mon, 05 Jun 2023 17:19:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f6069ed163b7975b49dc9e8925a15a02473293dca6513363fb11c08764520b8`  
		Last Modified: Mon, 05 Jun 2023 17:26:46 GMT  
		Size: 23.6 MB (23611936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230605` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ebdb7ac21fef61242b87d8d00ca0d3f4434c5adf360e771dc1b8db0f75771759
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25974252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a494d051d6a9c0e46123cfc516acb84b76884f21684764c166ecf4fe92a7fa4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:07:59 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:07:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:02 GMT
ADD file:6c0661b94e27ede70ca2a8842bdab5bc26b9ae4760b17870eda9d595672795ff in / 
# Mon, 05 Jun 2023 17:08:02 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb0a6f6b1798ce3ee565023c3a50777fff89bf6761a0985c8ff93aa903f7d0f1`  
		Last Modified: Mon, 05 Jun 2023 17:26:40 GMT  
		Size: 26.0 MB (25974252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:focal-20230605` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1b176384bc513bb425b497364f1d6353ac1b285d48862c22a9b7c450c431d4bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32070916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cad30b7d8589358e8074d6fb495d774d8c52cfa8ab35ed10f518a2c8b7586c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:24 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:25 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:28 GMT
ADD file:0a2372ac4d43f0f4ada2b55dd0a359df73a828a9aa9426bfdd05a02b9c4b2bd9 in / 
# Mon, 05 Jun 2023 17:08:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a42700f678f7c62f7053fbbd2b046ac1742685ac4262717c9c6db8a8e872884d`  
		Last Modified: Mon, 05 Jun 2023 17:26:52 GMT  
		Size: 32.1 MB (32070916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:jammy`

```console
$ docker pull ubuntu@sha256:2a357c4bd54822267339e601ae86ee3966723bdbcae640a70ace622cc9470c83
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
$ docker pull ubuntu@sha256:83f0c2a8d6f266d687d55b5cb1cb2201148eb7ac449e4202d9646b9083f1cee0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99284ca6cea039c7784d1414608c6e846dd56830c2a13e1341be681c3ffcc8ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b851dcae6ca1461dde247915abc5048061f34332929ca8fb37d9dc18f2e2f44`  
		Last Modified: Mon, 05 Jun 2023 17:20:26 GMT  
		Size: 29.5 MB (29533050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9aa2ce874cc0d140b3344fb6125d0ef540d347bca8a13c2270ca1c7a40490be3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3681d7421d4545f9eb7b1aabcb24b041b347b37705f89a858f831b94d8e2f0bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 16:59:35 GMT
ARG RELEASE
# Mon, 05 Jun 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 16:59:40 GMT
ADD file:5425962ced738173a50965fc5cd95c79d0a319323df4a34e9da3f5037a5264c3 in / 
# Mon, 05 Jun 2023 16:59:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ceecae09ee56d3fb7d5d26ff9505f3aa7e7cc5e54545fbecde69ef046b84f1c`  
		Last Modified: Mon, 05 Jun 2023 17:20:38 GMT  
		Size: 26.1 MB (26140710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:25de8a960c338b7d38aa15c012ceee70d8e29239db97596d6ecc50a5085d8f7a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27346742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb01e8e31210c9bfc5412c3fc1b8b7aea849bc2a9c21f47553bd31cc8fd79f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b2837baf7808226f588fabacb30598287e02d4dbf120eaf968c5299a6c2e9619`  
		Last Modified: Mon, 05 Jun 2023 17:20:32 GMT  
		Size: 27.3 MB (27346742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:eb4e647121c71cc9305e466d9c844a1207f90bab2e689310050e66e8b4f4d534
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16fc5784936f704a4bd8208deeb624554aeb2cdab87301aab60391db8f7ec590`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d3c256ab34973cfc9065065e684e5e5d1dac1eeb77974324e0de68944af26f62`  
		Last Modified: Mon, 05 Jun 2023 17:20:44 GMT  
		Size: 34.6 MB (34591237 bytes)  
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

## `ubuntu:jammy-20230605`

```console
$ docker pull ubuntu@sha256:baf68c93f5cffe5b7c5de38d5c65c8d6ba772078e69c2907343811510c94f95f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `ubuntu:jammy-20230605` - linux; amd64

```console
$ docker pull ubuntu@sha256:83f0c2a8d6f266d687d55b5cb1cb2201148eb7ac449e4202d9646b9083f1cee0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99284ca6cea039c7784d1414608c6e846dd56830c2a13e1341be681c3ffcc8ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b851dcae6ca1461dde247915abc5048061f34332929ca8fb37d9dc18f2e2f44`  
		Last Modified: Mon, 05 Jun 2023 17:20:26 GMT  
		Size: 29.5 MB (29533050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230605` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9aa2ce874cc0d140b3344fb6125d0ef540d347bca8a13c2270ca1c7a40490be3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3681d7421d4545f9eb7b1aabcb24b041b347b37705f89a858f831b94d8e2f0bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 16:59:35 GMT
ARG RELEASE
# Mon, 05 Jun 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 16:59:40 GMT
ADD file:5425962ced738173a50965fc5cd95c79d0a319323df4a34e9da3f5037a5264c3 in / 
# Mon, 05 Jun 2023 16:59:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ceecae09ee56d3fb7d5d26ff9505f3aa7e7cc5e54545fbecde69ef046b84f1c`  
		Last Modified: Mon, 05 Jun 2023 17:20:38 GMT  
		Size: 26.1 MB (26140710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230605` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:25de8a960c338b7d38aa15c012ceee70d8e29239db97596d6ecc50a5085d8f7a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27346742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb01e8e31210c9bfc5412c3fc1b8b7aea849bc2a9c21f47553bd31cc8fd79f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b2837baf7808226f588fabacb30598287e02d4dbf120eaf968c5299a6c2e9619`  
		Last Modified: Mon, 05 Jun 2023 17:20:32 GMT  
		Size: 27.3 MB (27346742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:jammy-20230605` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:eb4e647121c71cc9305e466d9c844a1207f90bab2e689310050e66e8b4f4d534
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16fc5784936f704a4bd8208deeb624554aeb2cdab87301aab60391db8f7ec590`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d3c256ab34973cfc9065065e684e5e5d1dac1eeb77974324e0de68944af26f62`  
		Last Modified: Mon, 05 Jun 2023 17:20:44 GMT  
		Size: 34.6 MB (34591237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:kinetic`

```console
$ docker pull ubuntu@sha256:a8c0aec3712a0562dc0ecfeeeae4e3de05fefb555b02c06778f69858d30c3bac
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
$ docker pull ubuntu@sha256:80fb4ea0c0a384a3072a6be1879c342bb636b0d105209535ba893ba75ab38ede
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26704595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39f297e9dda29a8d8896051c30f32feb52c9dcfb68e8a561650a1dde97cc94b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:02:32 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:02:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:02:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:02:32 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:02:34 GMT
ADD file:f8bb312bf73c62343d91c9988d58945c5d0fced3f559b95c4dd21a19183d933d in / 
# Mon, 05 Jun 2023 17:02:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:317e06b63fc01feacb4fa7a967d3a8c6fd35296935c83caa85ad28cd20add12b`  
		Last Modified: Mon, 05 Jun 2023 17:21:29 GMT  
		Size: 26.7 MB (26704595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:5dc1502337b177771dd9904822cde9abd2b26ee4014a3c6df7e912a9ef103db3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25098670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1120758c0ceafe38a213551ecf496a3b05011b323c13e36840d566b2ee02416d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:04:06 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:04:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:04:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:04:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:04:15 GMT
ADD file:615be72e62c21704af356d6cfd4e32a7df8dd4b93d0c3ee3ea2e1641127c54ea in / 
# Mon, 05 Jun 2023 17:04:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7eb2ece7978deb374e0aa4623aa1a44d513c34c7a56e23251a0dfbba314ea260`  
		Last Modified: Mon, 05 Jun 2023 17:21:41 GMT  
		Size: 25.1 MB (25098670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:dde2a31e58d07b2ed8be842eafae55b9a46b3629a0915dd6438fb3e484e46d65
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25770482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172adc9ce1cab441186106c04f9663f7b81edc9d3e8908b8dca58180df27ea16`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:02:45 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:02:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:02:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:02:46 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:02:50 GMT
ADD file:b85182b4593c262faef116755e01baa608e8090e1cb697d735485ff0bd5b353e in / 
# Mon, 05 Jun 2023 17:02:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bb573a4d6d791b5d50f1118d01e4c9b2acc927522cec8740ac9957e37eeac29c`  
		Last Modified: Mon, 05 Jun 2023 17:21:35 GMT  
		Size: 25.8 MB (25770482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b2a4b994153a43ab4941ab8efbc43c189d0c76b9fe4f8dee9f8449cd6ed83d93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31112867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a632c9634c258b38d044be3dfa48ee0aee70c82531def42c6e701c10e15989`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:10:48 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:10:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:10:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:10:48 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:10:52 GMT
ADD file:48c30fe281554302bb6533dd33a43a0877851ac5ba59dc3aff3d3d9ceae6f8a9 in / 
# Mon, 05 Jun 2023 17:10:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e4485626c4310d83f6d257d7c30db7a4fc23c70b98dec3ca37108fef26207e3c`  
		Last Modified: Mon, 05 Jun 2023 17:21:47 GMT  
		Size: 31.1 MB (31112867 bytes)  
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

## `ubuntu:kinetic-20230605`

```console
$ docker pull ubuntu@sha256:e6ea00f920e2e6974f84a15d4c6c30407d70fdbc1308959f27c2e693f2ea004b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `ubuntu:kinetic-20230605` - linux; amd64

```console
$ docker pull ubuntu@sha256:80fb4ea0c0a384a3072a6be1879c342bb636b0d105209535ba893ba75ab38ede
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26704595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39f297e9dda29a8d8896051c30f32feb52c9dcfb68e8a561650a1dde97cc94b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:02:32 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:02:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:02:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:02:32 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:02:34 GMT
ADD file:f8bb312bf73c62343d91c9988d58945c5d0fced3f559b95c4dd21a19183d933d in / 
# Mon, 05 Jun 2023 17:02:34 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:317e06b63fc01feacb4fa7a967d3a8c6fd35296935c83caa85ad28cd20add12b`  
		Last Modified: Mon, 05 Jun 2023 17:21:29 GMT  
		Size: 26.7 MB (26704595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230605` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:5dc1502337b177771dd9904822cde9abd2b26ee4014a3c6df7e912a9ef103db3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25098670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1120758c0ceafe38a213551ecf496a3b05011b323c13e36840d566b2ee02416d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:04:06 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:04:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:04:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:04:07 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:04:15 GMT
ADD file:615be72e62c21704af356d6cfd4e32a7df8dd4b93d0c3ee3ea2e1641127c54ea in / 
# Mon, 05 Jun 2023 17:04:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7eb2ece7978deb374e0aa4623aa1a44d513c34c7a56e23251a0dfbba314ea260`  
		Last Modified: Mon, 05 Jun 2023 17:21:41 GMT  
		Size: 25.1 MB (25098670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230605` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:dde2a31e58d07b2ed8be842eafae55b9a46b3629a0915dd6438fb3e484e46d65
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25770482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172adc9ce1cab441186106c04f9663f7b81edc9d3e8908b8dca58180df27ea16`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:02:45 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:02:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:02:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:02:46 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:02:50 GMT
ADD file:b85182b4593c262faef116755e01baa608e8090e1cb697d735485ff0bd5b353e in / 
# Mon, 05 Jun 2023 17:02:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bb573a4d6d791b5d50f1118d01e4c9b2acc927522cec8740ac9957e37eeac29c`  
		Last Modified: Mon, 05 Jun 2023 17:21:35 GMT  
		Size: 25.8 MB (25770482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:kinetic-20230605` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:b2a4b994153a43ab4941ab8efbc43c189d0c76b9fe4f8dee9f8449cd6ed83d93
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31112867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a632c9634c258b38d044be3dfa48ee0aee70c82531def42c6e701c10e15989`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:10:48 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:10:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:10:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:10:48 GMT
LABEL org.opencontainers.image.version=22.10
# Mon, 05 Jun 2023 17:10:52 GMT
ADD file:48c30fe281554302bb6533dd33a43a0877851ac5ba59dc3aff3d3d9ceae6f8a9 in / 
# Mon, 05 Jun 2023 17:10:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e4485626c4310d83f6d257d7c30db7a4fc23c70b98dec3ca37108fef26207e3c`  
		Last Modified: Mon, 05 Jun 2023 17:21:47 GMT  
		Size: 31.1 MB (31112867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:2a357c4bd54822267339e601ae86ee3966723bdbcae640a70ace622cc9470c83
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
$ docker pull ubuntu@sha256:83f0c2a8d6f266d687d55b5cb1cb2201148eb7ac449e4202d9646b9083f1cee0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29533050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99284ca6cea039c7784d1414608c6e846dd56830c2a13e1341be681c3ffcc8ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6b851dcae6ca1461dde247915abc5048061f34332929ca8fb37d9dc18f2e2f44`  
		Last Modified: Mon, 05 Jun 2023 17:20:26 GMT  
		Size: 29.5 MB (29533050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:9aa2ce874cc0d140b3344fb6125d0ef540d347bca8a13c2270ca1c7a40490be3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26140710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3681d7421d4545f9eb7b1aabcb24b041b347b37705f89a858f831b94d8e2f0bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 16:59:35 GMT
ARG RELEASE
# Mon, 05 Jun 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 16:59:40 GMT
ADD file:5425962ced738173a50965fc5cd95c79d0a319323df4a34e9da3f5037a5264c3 in / 
# Mon, 05 Jun 2023 16:59:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ceecae09ee56d3fb7d5d26ff9505f3aa7e7cc5e54545fbecde69ef046b84f1c`  
		Last Modified: Mon, 05 Jun 2023 17:20:38 GMT  
		Size: 26.1 MB (26140710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:25de8a960c338b7d38aa15c012ceee70d8e29239db97596d6ecc50a5085d8f7a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27346742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb01e8e31210c9bfc5412c3fc1b8b7aea849bc2a9c21f47553bd31cc8fd79f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b2837baf7808226f588fabacb30598287e02d4dbf120eaf968c5299a6c2e9619`  
		Last Modified: Mon, 05 Jun 2023 17:20:32 GMT  
		Size: 27.3 MB (27346742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:eb4e647121c71cc9305e466d9c844a1207f90bab2e689310050e66e8b4f4d534
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34591237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16fc5784936f704a4bd8208deeb624554aeb2cdab87301aab60391db8f7ec590`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d3c256ab34973cfc9065065e684e5e5d1dac1eeb77974324e0de68944af26f62`  
		Last Modified: Mon, 05 Jun 2023 17:20:44 GMT  
		Size: 34.6 MB (34591237 bytes)  
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
$ docker pull ubuntu@sha256:23966ecd49ebe3dd30c73ccc79afc423d53a994a95ecb000c9d0c9bfcb05e3cb
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
$ docker pull ubuntu@sha256:09f035f46361d193ded647342903b413d57d05cc06acff8285f9dda9f2d269d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed313b0551f6255bb9ea7fd953363f0f306d9e2e92dc9fb94cbdf70e3dafb6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:28:38 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:28:39 GMT
ADD file:708314051e878a0c6071fb2c8d4458a04ce058f47f2cfaa58c1b5a42e837ca0f in / 
# Thu, 15 Jun 2023 08:28:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a9d46cc3977f1066a9dd08f845b76f7f7d46e4ef74fdf8ed1f4db514ea5a45d`  
		Last Modified: Thu, 15 Jun 2023 09:08:28 GMT  
		Size: 26.8 MB (26836883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:98e3a45616c77d754ce50a12634c507cecf9b53ccb2f48e94b20db7b4b698618
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24636364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678dff67c6b9c6ec4eaccccccd2ffae1ddbf85b5e5309ac56522d7442f3f8c2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb49e82a48f62b12a885a1a02ae80f5261ab51e3f138c0190fc8d119247fd11c`  
		Last Modified: Thu, 15 Jun 2023 09:08:40 GMT  
		Size: 24.6 MB (24636364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2ea9408d05cc2543752070f336452eda81593c2001f9931a0451bad3a45d3a31
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b331a8a5e1bb537caa9a8e3d3f6308563136db02ab0501499e819e36d9f48a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:33:24 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:33:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:33:58 GMT
ADD file:064ac1f238394a53372e0db107e28835aa3c39ed189a15fe85c532bbb50bfbaf in / 
# Thu, 15 Jun 2023 08:33:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8382a46db1cf2ede3739a9337cad793e2228c0e455f8969bbbc14b4d6f28e`  
		Last Modified: Thu, 15 Jun 2023 09:08:34 GMT  
		Size: 26.1 MB (26088803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cac0b3657eb2260df362c4949ec416d6377b36d5c2999e1765874dcbadeca4cd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31029474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0d4e75ccb4b903cf3c7d3515fdbbe2462a8043abbcf13667b6f860fc11302e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:29:14 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:29:17 GMT
ADD file:5ebdf4bd4bc2b27019f20fb1964a395fa504d4f20e208c54237e363895b492d7 in / 
# Thu, 15 Jun 2023 08:29:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:223122c533fb03fa9f10684bc8fb23adf1f08af994530d4c9403f9086da8952b`  
		Last Modified: Thu, 15 Jun 2023 09:08:47 GMT  
		Size: 31.0 MB (31029474 bytes)  
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

## `ubuntu:lunar-20230615`

```console
$ docker pull ubuntu@sha256:7b9535676e1e0999e5a9d40721eb1ffd115d4c6cafb104229259071f281ac366
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `ubuntu:lunar-20230615` - linux; amd64

```console
$ docker pull ubuntu@sha256:09f035f46361d193ded647342903b413d57d05cc06acff8285f9dda9f2d269d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed313b0551f6255bb9ea7fd953363f0f306d9e2e92dc9fb94cbdf70e3dafb6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:28:38 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:28:39 GMT
ADD file:708314051e878a0c6071fb2c8d4458a04ce058f47f2cfaa58c1b5a42e837ca0f in / 
# Thu, 15 Jun 2023 08:28:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a9d46cc3977f1066a9dd08f845b76f7f7d46e4ef74fdf8ed1f4db514ea5a45d`  
		Last Modified: Thu, 15 Jun 2023 09:08:28 GMT  
		Size: 26.8 MB (26836883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230615` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:98e3a45616c77d754ce50a12634c507cecf9b53ccb2f48e94b20db7b4b698618
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24636364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678dff67c6b9c6ec4eaccccccd2ffae1ddbf85b5e5309ac56522d7442f3f8c2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb49e82a48f62b12a885a1a02ae80f5261ab51e3f138c0190fc8d119247fd11c`  
		Last Modified: Thu, 15 Jun 2023 09:08:40 GMT  
		Size: 24.6 MB (24636364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230615` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2ea9408d05cc2543752070f336452eda81593c2001f9931a0451bad3a45d3a31
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b331a8a5e1bb537caa9a8e3d3f6308563136db02ab0501499e819e36d9f48a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:33:24 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:33:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:33:58 GMT
ADD file:064ac1f238394a53372e0db107e28835aa3c39ed189a15fe85c532bbb50bfbaf in / 
# Thu, 15 Jun 2023 08:33:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8382a46db1cf2ede3739a9337cad793e2228c0e455f8969bbbc14b4d6f28e`  
		Last Modified: Thu, 15 Jun 2023 09:08:34 GMT  
		Size: 26.1 MB (26088803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:lunar-20230615` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cac0b3657eb2260df362c4949ec416d6377b36d5c2999e1765874dcbadeca4cd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31029474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0d4e75ccb4b903cf3c7d3515fdbbe2462a8043abbcf13667b6f860fc11302e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:29:14 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:29:17 GMT
ADD file:5ebdf4bd4bc2b27019f20fb1964a395fa504d4f20e208c54237e363895b492d7 in / 
# Thu, 15 Jun 2023 08:29:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:223122c533fb03fa9f10684bc8fb23adf1f08af994530d4c9403f9086da8952b`  
		Last Modified: Thu, 15 Jun 2023 09:08:47 GMT  
		Size: 31.0 MB (31029474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:mantic`

```console
$ docker pull ubuntu@sha256:93c55b20cc3b34b0492ea90fe2fad93f1dfba56005bb56ba9bcc3f83d6495c16
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
$ docker pull ubuntu@sha256:07460e809a7141b84050c6d68220c1f7e2aa58b0bc124c40a1440988bfd87e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26931867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0fd6ed554b4fa85755cd2f9fefc45a1bff5e640b1090f4573997837f6c46b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:39:09 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:39:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:39:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:39:09 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:39:10 GMT
ADD file:d8dc8c4236b9885e64ccd27399ed8dddab7d39915d76378527cb730855aba0e1 in / 
# Wed, 07 Jun 2023 04:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a3cc0ea50b9aef0e9b8b228c37edf92b0dfcb177d34ed50433918ae5eec172be`  
		Last Modified: Wed, 07 Jun 2023 04:57:40 GMT  
		Size: 26.9 MB (26931867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bf18ca0b049d010b72c35574c0261ef9c231fffb7588709e05a6b807c081e552
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24478190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eabbb20f267b27e88fe450b3d209313994eeb87c19d8cbdec2b2f8e821a1ce5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:07 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:12 GMT
ADD file:65e05498800189bf1f48f5c6df21d144e18e5e069db55d0b88d45c04cc1fe4de in / 
# Wed, 07 Jun 2023 04:48:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df4275b0f8f556aa5462a1fad0a0a188bc3d7b287bc6120389314f6b9bd6566e`  
		Last Modified: Wed, 07 Jun 2023 04:57:51 GMT  
		Size: 24.5 MB (24478190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d9c68082dd554f1adf3ed6169d08f0aae5431b4a7bddb8c19951eae6bd607097
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26131158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a27f5fa4b6e23e37d77cb2410d8f9efb5a9f5698e10bf3aef9bb503b14497d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:42:14 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:42:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:42:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:42:14 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:42:16 GMT
ADD file:3f4faed988a03b7d05aefe677906592aade4d2bae1ec3f7055c1f10744a38de0 in / 
# Wed, 07 Jun 2023 04:42:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f698dd1f118f52521a462f35505a0bca0dc8a7e17802e11146a6c0acfbfc797d`  
		Last Modified: Wed, 07 Jun 2023 04:57:46 GMT  
		Size: 26.1 MB (26131158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8d9660ab5ab6a35050e6f5ac4ff4170e85c1e6776e83d075f9331b85215b96a4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30966286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4004a6116d82330c1bb10006b89dcfb699827cd79a405a16dd59e3e33889d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:25 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:26 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:28 GMT
ADD file:6cf1bffac55b7de64803fabdb35baf75349cc0a40c0b4c68ac2690b7123edc85 in / 
# Wed, 07 Jun 2023 04:48:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:537eb27ff37d9fd24f7097996a5a0ed640152c3656390c06baff05ecd549d691`  
		Last Modified: Wed, 07 Jun 2023 04:57:57 GMT  
		Size: 31.0 MB (30966286 bytes)  
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

## `ubuntu:mantic-20230607`

```console
$ docker pull ubuntu@sha256:510d40fc1b765402d14198e09ebf181ef941780e0d62e17e11f5ccbd49374b61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `ubuntu:mantic-20230607` - linux; amd64

```console
$ docker pull ubuntu@sha256:07460e809a7141b84050c6d68220c1f7e2aa58b0bc124c40a1440988bfd87e6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26931867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0fd6ed554b4fa85755cd2f9fefc45a1bff5e640b1090f4573997837f6c46b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:39:09 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:39:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:39:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:39:09 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:39:10 GMT
ADD file:d8dc8c4236b9885e64ccd27399ed8dddab7d39915d76378527cb730855aba0e1 in / 
# Wed, 07 Jun 2023 04:39:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:a3cc0ea50b9aef0e9b8b228c37edf92b0dfcb177d34ed50433918ae5eec172be`  
		Last Modified: Wed, 07 Jun 2023 04:57:40 GMT  
		Size: 26.9 MB (26931867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230607` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:bf18ca0b049d010b72c35574c0261ef9c231fffb7588709e05a6b807c081e552
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24478190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eabbb20f267b27e88fe450b3d209313994eeb87c19d8cbdec2b2f8e821a1ce5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:07 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:08 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:12 GMT
ADD file:65e05498800189bf1f48f5c6df21d144e18e5e069db55d0b88d45c04cc1fe4de in / 
# Wed, 07 Jun 2023 04:48:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:df4275b0f8f556aa5462a1fad0a0a188bc3d7b287bc6120389314f6b9bd6566e`  
		Last Modified: Wed, 07 Jun 2023 04:57:51 GMT  
		Size: 24.5 MB (24478190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230607` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d9c68082dd554f1adf3ed6169d08f0aae5431b4a7bddb8c19951eae6bd607097
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26131158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a27f5fa4b6e23e37d77cb2410d8f9efb5a9f5698e10bf3aef9bb503b14497d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:42:14 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:42:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:42:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:42:14 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:42:16 GMT
ADD file:3f4faed988a03b7d05aefe677906592aade4d2bae1ec3f7055c1f10744a38de0 in / 
# Wed, 07 Jun 2023 04:42:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f698dd1f118f52521a462f35505a0bca0dc8a7e17802e11146a6c0acfbfc797d`  
		Last Modified: Wed, 07 Jun 2023 04:57:46 GMT  
		Size: 26.1 MB (26131158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:mantic-20230607` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:8d9660ab5ab6a35050e6f5ac4ff4170e85c1e6776e83d075f9331b85215b96a4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30966286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4004a6116d82330c1bb10006b89dcfb699827cd79a405a16dd59e3e33889d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 07 Jun 2023 04:48:25 GMT
ARG RELEASE
# Wed, 07 Jun 2023 04:48:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Jun 2023 04:48:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Jun 2023 04:48:26 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 07 Jun 2023 04:48:28 GMT
ADD file:6cf1bffac55b7de64803fabdb35baf75349cc0a40c0b4c68ac2690b7123edc85 in / 
# Wed, 07 Jun 2023 04:48:29 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:537eb27ff37d9fd24f7097996a5a0ed640152c3656390c06baff05ecd549d691`  
		Last Modified: Wed, 07 Jun 2023 04:57:57 GMT  
		Size: 31.0 MB (30966286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:23966ecd49ebe3dd30c73ccc79afc423d53a994a95ecb000c9d0c9bfcb05e3cb
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
$ docker pull ubuntu@sha256:09f035f46361d193ded647342903b413d57d05cc06acff8285f9dda9f2d269d5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26836883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed313b0551f6255bb9ea7fd953363f0f306d9e2e92dc9fb94cbdf70e3dafb6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:28:38 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:28:39 GMT
ADD file:708314051e878a0c6071fb2c8d4458a04ce058f47f2cfaa58c1b5a42e837ca0f in / 
# Thu, 15 Jun 2023 08:28:40 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a9d46cc3977f1066a9dd08f845b76f7f7d46e4ef74fdf8ed1f4db514ea5a45d`  
		Last Modified: Thu, 15 Jun 2023 09:08:28 GMT  
		Size: 26.8 MB (26836883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:98e3a45616c77d754ce50a12634c507cecf9b53ccb2f48e94b20db7b4b698618
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24636364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678dff67c6b9c6ec4eaccccccd2ffae1ddbf85b5e5309ac56522d7442f3f8c2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fb49e82a48f62b12a885a1a02ae80f5261ab51e3f138c0190fc8d119247fd11c`  
		Last Modified: Thu, 15 Jun 2023 09:08:40 GMT  
		Size: 24.6 MB (24636364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:2ea9408d05cc2543752070f336452eda81593c2001f9931a0451bad3a45d3a31
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26088803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b331a8a5e1bb537caa9a8e3d3f6308563136db02ab0501499e819e36d9f48a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:33:24 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:33:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:33:25 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:33:58 GMT
ADD file:064ac1f238394a53372e0db107e28835aa3c39ed189a15fe85c532bbb50bfbaf in / 
# Thu, 15 Jun 2023 08:33:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19e8382a46db1cf2ede3739a9337cad793e2228c0e455f8969bbbc14b4d6f28e`  
		Last Modified: Thu, 15 Jun 2023 09:08:34 GMT  
		Size: 26.1 MB (26088803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:cac0b3657eb2260df362c4949ec416d6377b36d5c2999e1765874dcbadeca4cd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (31029474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0d4e75ccb4b903cf3c7d3515fdbbe2462a8043abbcf13667b6f860fc11302e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:29:14 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:29:17 GMT
ADD file:5ebdf4bd4bc2b27019f20fb1964a395fa504d4f20e208c54237e363895b492d7 in / 
# Thu, 15 Jun 2023 08:29:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:223122c533fb03fa9f10684bc8fb23adf1f08af994530d4c9403f9086da8952b`  
		Last Modified: Thu, 15 Jun 2023 09:08:47 GMT  
		Size: 31.0 MB (31029474 bytes)  
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
