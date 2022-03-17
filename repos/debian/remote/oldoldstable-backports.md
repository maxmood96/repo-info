## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:a62c0e704ea7b5dd3e38547c70fbff7a777676c93fb8279d6393a2edd219a9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:7e69b284f52e8d6fce487f3026f27eea0324e3242a247eb8e6e870441dfb18b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45427966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89442dbaa0e45961adb5c8fefa98478e3880c092061392138405432f2ce6035`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:45 GMT
ADD file:2a75b69143ad9db169fb3f263eb62c9a965340a9f6e84ca93ab176cadfb10343 in / 
# Thu, 17 Mar 2022 04:04:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 04:04:53 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3726c797f24fb208cc44da192b3d59c98ecc17a981f53e68a88de8059c17f4d0`  
		Last Modified: Thu, 17 Mar 2022 04:11:15 GMT  
		Size: 45.4 MB (45427736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f9e4929d9b612304c0e84eeee113bbac229e1b4f7f76132fcac9aa0939e780`  
		Last Modified: Thu, 17 Mar 2022 04:11:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fdb0dd8776ad1bcb258ed22cb6a1e8826c94e5e30f726b9486a551d7bfbe8204
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44123799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2433e2d346ef2310d16d2a9636712d39669443637c92165fab10b2ba8d2cae`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:21:13 GMT
ADD file:70bc18337f92735d448398c9f64f0da6642291327ec97705af4ccfd064e8adef in / 
# Thu, 17 Mar 2022 05:21:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 05:21:26 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0821ba1133c41b7b765179f9be93fc916f3afb4ae72100f3f2bc8e9f42aea00e`  
		Last Modified: Thu, 17 Mar 2022 05:37:14 GMT  
		Size: 44.1 MB (44123570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68e2e1200ef32ead498b854bf80c9715e9c69da2505bd88c22a705c79d8a640`  
		Last Modified: Thu, 17 Mar 2022 05:37:25 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:cfc203f8bc53a6cecc4bc7426e83c6b91a6e10bdbc4d31794a3f27e7f778d624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfa5bfbe36fbd5377232b3fd7c736a64d082c89e0a9b25f3b8017069a829a91`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:32:35 GMT
ADD file:273df495cce49102768b41ba8f0c94ccbc7c53623b91b8a7e31ef0a344115c56 in / 
# Thu, 17 Mar 2022 09:32:36 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:32:48 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:82170f35defd7dea012acc55071774a608084a9c93f0970fab860ebff21f5f13`  
		Last Modified: Thu, 17 Mar 2022 09:48:42 GMT  
		Size: 42.2 MB (42151377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aae62e28bf90b414876f104cc744b5896c69d1bf5e6fbeb5eb48ad275407f02`  
		Last Modified: Thu, 17 Mar 2022 09:48:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:948c5089bf477e7bb0d5b3dc726acef26a88e7d489cbbe14d22a45c6d314baa0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43213281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d5a23ee1666625fb7cd8f5f0199720a3be0d04124af8137304e2508fc794d3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:32 GMT
ADD file:0e2e6ae6979f774fdea8fba76045ac4eb39a89d1d370d87d0fd765c6ea220660 in / 
# Thu, 17 Mar 2022 03:22:32 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:22:38 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b6b0bc07fbb744a7d14d4a015f90182fdcd37a2fa720697c1030a2af0370c59f`  
		Last Modified: Thu, 17 Mar 2022 03:29:51 GMT  
		Size: 43.2 MB (43213054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e288327bf5b111740c7ff108fca71e0135d710098f3791f070c8f59888b179`  
		Last Modified: Thu, 17 Mar 2022 03:30:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:35385a0697a2a3755dfd1a98a8c40ba489333b1ab2ce0c6e10f0b050f9dde15c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46148072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d711b965a9ab210e757faab6ea9a22385e4d0915ec93b0644a9eb55456f0fc7c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:16:41 GMT
ADD file:8cdd8e35ef5a5491281b5421821fb3538a5bb0e6973cc14de42e43fa1a5b5735 in / 
# Thu, 17 Mar 2022 08:16:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:16:47 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:284a1f11c698c0759ef4541f991756a09b97facfd133c3ef95326168c5058e66`  
		Last Modified: Thu, 17 Mar 2022 08:25:25 GMT  
		Size: 46.1 MB (46147846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0770287cbf739cd8a2c15631b1cf0d27aeb760fcc35002649ebdd64d9a4be4`  
		Last Modified: Thu, 17 Mar 2022 08:25:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
