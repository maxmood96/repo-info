## `debian:testing-backports`

```console
$ docker pull debian@sha256:9c6d98f675bec11d7e7dfe8c9678b518147e7c7117de1ad0f657a168f54ebaa0
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
$ docker pull debian@sha256:7266d469c5684e64fdc4771279e8c92c1cef612c293a592fc4efc5b55aa07ebb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50107295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4776fad490aa9f15fbe31003e87c225c3eaaa88f581896fea262c5070dd80c98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:49:43 GMT
ADD file:1aff6dddbfddcca844322bda5bfd098a855c07d34fe5704dca7171f5c1f56ece in / 
# Wed, 04 Sep 2024 21:49:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:49:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a50fe0a1bbe705d3679428469219f780f9136db589d5f4f8595d79515abf6bcf`  
		Last Modified: Wed, 04 Sep 2024 21:54:03 GMT  
		Size: 50.1 MB (50107073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a295897e198650ad0c8c7425f41f8695b5e1c319d03971703ae5b389a537b158`  
		Last Modified: Wed, 04 Sep 2024 21:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b5c8fb0e94a8b6efe85e57869994cc665e8bdd36a30acaa0543d434a2b5e94d2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47600589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc410bba7a5b4723193879edf3f122d24b281113797957b2f11320ba9ad6834`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:59:37 GMT
ADD file:58e7480ad070c187e966d1f49cf6bfd6820edf36f8bfb4adf8cf4a7539a92063 in / 
# Wed, 04 Sep 2024 21:59:38 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:59:41 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:95514cfe4ae89b3874639f2bbaad4efb19ac5fa1f1880dc900f00a4707da1483`  
		Last Modified: Wed, 04 Sep 2024 22:04:20 GMT  
		Size: 47.6 MB (47600364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffc6b76bc413b9321f0cebb3a500eb19b2fe5b40096e23161d4d3bf7e45afc0`  
		Last Modified: Wed, 04 Sep 2024 22:04:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:259de614e5adbca203a3c5656e9cb3bcfc533c70f3969fa4f572462e9e963b0c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53594580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a31460be948ad0030a6ba35a8ebb75086127f10daf07a542ee72d3a706c1d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:57 GMT
ADD file:394779f4486ebaf8490ab95548a898d31798f528981c6abde9a64ae9541ad916 in / 
# Wed, 04 Sep 2024 21:40:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:41:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1d833a2b98580c8c6fbc93eec4d1f948a740704ada36d9bfe4881cc92113a70f`  
		Last Modified: Wed, 04 Sep 2024 21:44:46 GMT  
		Size: 53.6 MB (53594358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7651c52de501fd52bde87e9099070ac23c277073f556c906021ba9535f210ade`  
		Last Modified: Wed, 04 Sep 2024 21:44:54 GMT  
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
$ docker pull debian@sha256:b5b11fc830864310f26ff3b8d82a2216defd977b66fcc89fb7ca669df575b13a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52746701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d825c97cb5f6fc232bddd7fe36a9d331248943bd4b876c5f13562dba53b5499`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:45:05 GMT
ADD file:59e982fbd6b5364ff9e3c3a4656bf6cb6795d637a02c788e4db61959964e2b65 in / 
# Wed, 04 Sep 2024 21:45:07 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 21:45:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ff4f98e3072ebdb612b0732715fb700fbfdf55f51351132742a0b343fd7fbfc8`  
		Last Modified: Wed, 04 Sep 2024 21:49:29 GMT  
		Size: 52.7 MB (52746481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9d15d8ccef68b03dfd0744aed04e68b335a892560e79b98cf9cfee1a5a2cac`  
		Last Modified: Wed, 04 Sep 2024 21:49:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
