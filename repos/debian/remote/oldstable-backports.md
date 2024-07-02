## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:1779387cf7a27bd8e6e66288689f05841eb9ec5a7c3af32f741f7999433e1cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:211fcff4a2f6ae12ae70ad9c81cd7380a2a93ca94af6130cef42f0ab0730d58c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55081625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8eb252bee4dfa8e2711fad0095fad64b28fd3421598641e2bae562e1a0f7db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:34 GMT
ADD file:38e0ab105db32d90421178fd176f2adfe7ea5d104ab21dee8427b1857212618f in / 
# Tue, 02 Jul 2024 01:25:35 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:25:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9d70182e582870b85b1604eedb36c0c5540a5a9cf95a1684d0a97617fa1ce283`  
		Last Modified: Tue, 02 Jul 2024 01:29:45 GMT  
		Size: 55.1 MB (55081400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f66e1bc1ccd7f0ec794c568aa3ed16b5fee4a769840b4ba7b934eea1627a8f0`  
		Last Modified: Tue, 02 Jul 2024 01:29:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:2922e35f9d4564ec48ba09007c3706ca474555f558438a08071e50e590c9b4a5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52586006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f470826fec823fd35ca86d2473e0b14d6f3f0ec9e30fc88d6475071fc2531c0b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:51 GMT
ADD file:9282da1c5b619bc81d6db8df28483015e32928271f0b3a20eb90747eed5fe49a in / 
# Tue, 02 Jul 2024 00:48:51 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:48:54 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a2c15e4bbe8b382b79207194ee6776805f1630ce553a053babc67f3d7f29fa4b`  
		Last Modified: Tue, 02 Jul 2024 00:52:33 GMT  
		Size: 52.6 MB (52585782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae7a0727ae8a69e8a627a0a9847e2647f67fbd45dce2c3719918a4be3dcbb8e`  
		Last Modified: Tue, 02 Jul 2024 00:52:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d9ec11170bc53dc45ce9bee7cf48a99332cb053b345d3935d420488f765b299e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50239252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb537c8987ac4b9fc8f6507644d0b7fa3845405c26bfe10daa01e61eb716dd5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:33 GMT
ADD file:f32baaff9d64686460dccd09e774165b0009acf2fc4248fc59e4dec03862c9b3 in / 
# Tue, 02 Jul 2024 01:00:33 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:00:37 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9dcdd0ee7e3668ff72dadf6f539c6366434b2601c28dc67e826bb47e9d6053e9`  
		Last Modified: Tue, 02 Jul 2024 01:04:19 GMT  
		Size: 50.2 MB (50239026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd67a0f057165f9635b118d50ea80f7608420e4f103537599842d39fc4bf045`  
		Last Modified: Tue, 02 Jul 2024 01:04:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d470c7834ce4e796d708fcabe7c41d7a92a4d06d2968afbd1376fe4fee437548
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53721887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92274a264c37afd1a658edd0a3e5116f468558097978aebdad8e9495ffbc1648`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:58 GMT
ADD file:15a04866a1a28523798f9f7254b7bfc591fd26b891018866c2f2a98fc9626132 in / 
# Tue, 02 Jul 2024 00:39:59 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:40:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8d13c62a49a498ddc0ea037d935b1e0af1c721c91f5e1cd7fc5e131c81150536`  
		Last Modified: Tue, 02 Jul 2024 00:43:21 GMT  
		Size: 53.7 MB (53721662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86eab011a00c513c96b36e05e49dfcd3df1efb0eaa9bd3c9539e7e9ce56ed3a`  
		Last Modified: Tue, 02 Jul 2024 00:43:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:0ffb783349c92086021e747c26b71ef33a778d984d7cd60cc8e1c6c61199687b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56065199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e622c272d36b0a48464ed25ac828f43ce0f035c7d382242226bbc7b2741bd3cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:27 GMT
ADD file:abace1c14fdae6a01fdc58e25dedc4c696a84d42ed47c558cfa40ccb72e8b281 in / 
# Tue, 02 Jul 2024 00:39:28 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:39:32 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1fb690179f80ed8752683ae01dd9bc4f99561181fb3c592ef2e5adaed753b88a`  
		Last Modified: Tue, 02 Jul 2024 00:43:47 GMT  
		Size: 56.1 MB (56064976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7f102b95d4629c697e2bb613a77fd6c8c804cec6e98984af0210a7e1092ff6`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:91585e0317f85e5fcd8746a5f05860c899cc089a0492bf00cb12d2167f0d64c1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53306405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5b7b9357e4e453cb1f7900856fae0f7b47c06767e317644bc63f5b018d2d5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:20:14 GMT
ADD file:4480037f30f8d6ecb45d7a1c16e0762bf212e300f18fd9f18206ff83f024d1e9 in / 
# Tue, 02 Jul 2024 01:20:20 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:20:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:308cceb65a95693415f063e35a620a0f8c84091bc3e1e55e22de31fd54556857`  
		Last Modified: Tue, 02 Jul 2024 01:31:37 GMT  
		Size: 53.3 MB (53306180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f1f47284fa2dd75a73e3684ecdd2074a2c2e2d66407251e0a460371f45b91f`  
		Last Modified: Tue, 02 Jul 2024 01:31:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:6eda27be15e8510e66b4a161f8375d82c2e38db1806862ef73250600d73dac91
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6e972a5b83a41346e303cc7f40cf117cb2b3584c7552117614800a93822bb4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:15 GMT
ADD file:625f76cf9d3e50d5a69f8e1d60090bebd64541aee9ddda3dd412ec4e42fb0270 in / 
# Tue, 02 Jul 2024 01:18:17 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:18:22 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:946f5e3e37aa5974ba23ab7558c3afad41f89d2271c0530433b4accd7fe31158`  
		Last Modified: Tue, 02 Jul 2024 01:23:09 GMT  
		Size: 59.0 MB (58950366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf72555629b2f100caa5af13bd1beec83edefc50ee3cc7ae50245c6c5523955`  
		Last Modified: Tue, 02 Jul 2024 01:23:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:1c150a56ec8bc7ed50f1914a1feaf1862862de87e1c8a0a1e2b2d157dd48ecfd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53320007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1464148eb7273a5f79c82dd3806da5f30bc342331b97cf77606d9660702c2bf6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:44:27 GMT
ADD file:125cc7d3d92dd0303f08959cf53c6588c2919c713aa0720548faf4a6bcf5a8d0 in / 
# Tue, 02 Jul 2024 00:44:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:44:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:360c7f6073a0c5dd5e973de18b243a148acbaa9d309e3552e8ef5e7787e679a1`  
		Last Modified: Tue, 02 Jul 2024 00:49:24 GMT  
		Size: 53.3 MB (53319783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc38cb5208f6a345c0d8b9b3f27667e6a04cc48e687061655ba1b4adbd6a4e6`  
		Last Modified: Tue, 02 Jul 2024 00:49:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
