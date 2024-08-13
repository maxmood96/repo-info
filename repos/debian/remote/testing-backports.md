## `debian:testing-backports`

```console
$ docker pull debian@sha256:7655e937ec63053717ae0d70cbf9ec462d5d251687b32a699a72b6ce964e78f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:ff3106457c87c25f1b03331f02c02a0fc6befde5b8dacee463738b30347ea66f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52841415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dc7c4065286c17de620933191a24b95cc4b1b2760c8cb83a9cce0f5af5cff8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:50 GMT
ADD file:c90c835a37f0040007d62990bb1a7701bf8fac5f7be2a95c4f7a4c904831114d in / 
# Tue, 13 Aug 2024 00:21:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:21:54 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:276a3574c9ee1c4e17bd0ae7c30a212b1753e64ed85ab3e2e18b0cb5c66114cb`  
		Last Modified: Tue, 13 Aug 2024 00:26:09 GMT  
		Size: 52.8 MB (52841190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16395e5ad90301b65617fda015440c3ead7e2240b8af30458ac4161dbd39731`  
		Last Modified: Tue, 13 Aug 2024 00:26:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ff42c60b548c385f7745e25d702da7f37ae2346a7acc2fb1efb51ba2db03a241
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49871838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae93d7495c463139380333ed48f1726fbc3f0e8e2041f9830a6ee5f5c137943d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:56:41 GMT
ADD file:05efa5f5b988a1cb5fd3df274b996265b1fa7a3bbeb40c17046fda4d9ae12b3a in / 
# Tue, 13 Aug 2024 00:56:41 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:56:44 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f8e646f71ce015281e32447febba37320f3e2ae16d1d1348afebc52635fb89d9`  
		Last Modified: Tue, 13 Aug 2024 01:01:11 GMT  
		Size: 49.9 MB (49871616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1cb8a175f03cb520723bc0ba2fcdd4f06d87e8c831b0e1a09a94778b8d36fe`  
		Last Modified: Tue, 13 Aug 2024 01:01:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:be97bdd109182762c999efe4fd090cb9da6dc7a4e11cfcca98122f47fc05cb6b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47364352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dee1c5b1ef78ff130f276ced115bf0ea88f55cc0d08560701f6a010d6604ffe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:58:58 GMT
ADD file:7c16429b99132f2926d89f5f0fd8f3c140b0b8084d5fc1c29f987b7ed691887d in / 
# Tue, 13 Aug 2024 00:58:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:59:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1972c9246ea9d716d8bcbd0378513bed7e8e96d8aa374d9d7c1bb14e59eb684e`  
		Last Modified: Tue, 13 Aug 2024 01:03:26 GMT  
		Size: 47.4 MB (47364130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1f0e39691bffc65275878f2fe8870b4d98ca0b79ff7707f0dd160e1ec97b23`  
		Last Modified: Tue, 13 Aug 2024 01:03:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:140f2eb5c1f606fcd886939533fff82fac72706b48afadac0f3f0dc6ecc1ca7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53152664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df0a22d879470ae41ad1171e0d70fe71d873391937f32f13dcfd16409539c5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:56 GMT
ADD file:8e46df4c5628fc2d0e9a0a8340d8fa4ae995b7f8eaea4a37d8c2340483d7f6ba in / 
# Tue, 13 Aug 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:40:59 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:516e6d7b27c596c99ccee734286b90644fb195a47b2b25bde8302e9b90e7bb8a`  
		Last Modified: Tue, 13 Aug 2024 00:45:09 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fb5ea8f8c032fc9c688b8a2bfe7f695414e872b102f918a53f4f5ac590c033`  
		Last Modified: Tue, 13 Aug 2024 00:45:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:8be1ce83eb26fab05945108cf60f933e1c272df513edaa2f3819049047959d6d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53777721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37662941e812635d9cfb5b4533e369b5189231c82bac7908c0b899988311628`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:32 GMT
ADD file:d314a8f63c9f1d85a2203498b9edfc74b1eb162577fd916e9a60a76e8ba9a215 in / 
# Tue, 13 Aug 2024 00:40:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:40:37 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2c6b5caa249e1585a0026deda552f84c91fc3f07b38ba8da9ec02df86e83a490`  
		Last Modified: Tue, 13 Aug 2024 00:45:21 GMT  
		Size: 53.8 MB (53777498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c5d52276343f813961e9011fc2d2ff3e222964c442dbc86847b737d690f71d`  
		Last Modified: Tue, 13 Aug 2024 00:45:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:0c405447769d2c29ff01e830718e1854305521c4910b57c99d61b3c91ff6cb1c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51717836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f8ad5fe4aebf26fc632831a2f4ac26e0675c6e09f9cb77e64a499c899ff6dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:16:53 GMT
ADD file:dfd6a600c17166a96225ad39f19647fff90e607d44d8a94167f21fe2c9def7e5 in / 
# Tue, 13 Aug 2024 00:16:59 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:17:14 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:54c87afb94ad6750b9c0116fbb8a043f9c4f22ac43f898d59e11edf18d2c56d4`  
		Last Modified: Tue, 13 Aug 2024 00:28:23 GMT  
		Size: 51.7 MB (51717612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e955cb77d3a3eb6c62484291ce870612a34f1978a86e2a5669eb2ef818517843`  
		Last Modified: Tue, 13 Aug 2024 00:28:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:58c060ca0baf70c3d043ba04e32cd2236bb48fa2d66b3606bb67fc319d0928ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56775809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b200dbdefcda38c9513e97abebd91c45468597a192ace9e54e3fe18d6f7700`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:23:59 GMT
ADD file:12b03032064b0d5c80915c492086c246ce1d59ac440f1c69120dbbd189616533 in / 
# Tue, 13 Aug 2024 00:24:02 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:24:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f628e11a36e335721280197a03583f0306cbf039619a6c06323192058009cb53`  
		Last Modified: Tue, 13 Aug 2024 00:29:34 GMT  
		Size: 56.8 MB (56775585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9b8b3c2669edd2b7b9d349db3c40f8a5e43bf730737b43784836ff7f23633e`  
		Last Modified: Tue, 13 Aug 2024 00:29:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:1e9433a66b06e3fe69d25676ec6b4a4a833a357820f10b568a8e647ced2beb23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51127422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1f42909c6de3250b49909febc3c19fa7685f276868ec2f88fe2671f81acbea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:12:07 GMT
ADD file:52b983ed2ad4f2b7372fe244036fa274e305c652cc773028b8d61d68868812b7 in / 
# Tue, 13 Aug 2024 00:12:10 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:12:22 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0f4dcbe9066fd7cf9df1f5c2e6f31e2bcb9fe3ec2a5221e465d90eed0eeab067`  
		Last Modified: Tue, 13 Aug 2024 00:17:31 GMT  
		Size: 51.1 MB (51127197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58597e153883797c9d6ebf2d4cb3c5e0ddefd3bfa8458725188e9b1c6909808b`  
		Last Modified: Tue, 13 Aug 2024 00:17:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:11cdbb21546f1fae19a0382dd16c5074763b014f1477ef5f9fd3da690d644145
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52481139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f02c6d55122fff3ada9d5948c313e9f689f3715fda588b4d9d830e3790e703`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:44:53 GMT
ADD file:ed752b0badb744224b241435cc89ae12d907a42dd7d2f82dd6104492ce4dac7c in / 
# Tue, 13 Aug 2024 00:44:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:45:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fbb046efc9e91cdd2b169c0d71ad77aca5166c293df778872751338e08dfc6ab`  
		Last Modified: Tue, 13 Aug 2024 00:49:17 GMT  
		Size: 52.5 MB (52480916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cef3d92d897137c97bc2ef53d672862166b1e67cac44a4585fe940e0bf69bf8`  
		Last Modified: Tue, 13 Aug 2024 00:49:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
