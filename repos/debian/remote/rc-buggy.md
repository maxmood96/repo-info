## `debian:rc-buggy`

```console
$ docker pull debian@sha256:20abf59aa22a5915d2005da96166e66bd10ba1100f97649d262c93778ebcf437
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:66ad88b218967a1bf0738619b96c52527d51f68cd2f0d6e04eaab3e611afdccf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49617541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc1cffe030f2ce3d152ace77ca17fa5994f7cfc8c4f08e3ac2303af4b796378`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:01:27 GMT
ADD file:48c88afb2094d5db855a4fe872b2cbb76a9d3c1b143c67463318da89ff28ed91 in / 
# Wed, 16 Aug 2023 01:01:27 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:03:11 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c111fea192ed7adbc203c571a96a882a3741644731e862353e7c2f3259608f77`  
		Last Modified: Wed, 16 Aug 2023 01:07:20 GMT  
		Size: 49.6 MB (49617313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9ff1bd6782261332ee9158b965107c9e988f6a6387c7be3e370450562f5529`  
		Last Modified: Wed, 16 Aug 2023 01:10:03 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:d84cf30ada971a1cddac23cf6ed9b92d4bd89cc4efaeb107fce78317f2aaa29a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47404006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94304158ee40407d7606f1650e6375fe54d2f992a42ca2fcaa21bf4ba98da0d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:49:11 GMT
ADD file:2d486f4790de50d5a173ed5147c22ebcaaade283f5bdf6b62bc072050fc164c1 in / 
# Tue, 15 Aug 2023 23:49:11 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:50:23 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0fb27bc4b8f884dd1bc1129dd87397bcc993ec915005657bd21811eb84745100`  
		Last Modified: Tue, 15 Aug 2023 23:53:08 GMT  
		Size: 47.4 MB (47403781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadaab52d9ba2255d3467baf5c79a0867bbb0a36dd36fa8906d0f8482aa039b8`  
		Last Modified: Tue, 15 Aug 2023 23:55:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:da346e29821f4f2e4269f364fc15e4e9d9aef1cf0cf088d36d6a78f1bd9065e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45189507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7b09ef776e4bfa6942af6971c90621b5cf058f6905b82c07215b6ff82d6e62`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:18:42 GMT
ADD file:2a1f1ecc1cfa876ccc22e6ef2a3a4ea39a83aec70ecde3f7cdaddee69dac2002 in / 
# Wed, 16 Aug 2023 00:18:43 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:20:11 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ccc7cdd48defe44f9a45f06f57d69b192155657bc5d244f915958c2027d645c3`  
		Last Modified: Wed, 16 Aug 2023 00:24:10 GMT  
		Size: 45.2 MB (45189279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cd1f2e68eae6f64530c4705bf905131dd11a4db3e291eb8be2fad868bcf8bf`  
		Last Modified: Wed, 16 Aug 2023 00:26:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:72557e4de2cc0e083fff30ca9d73df0c8af932165da5f71e4c3a9378008e0488
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49531955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c427542b410257ab6d703b5771148d09c1abac348563ca67103b5f9740d3c098`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:41:01 GMT
ADD file:8064072457ccf7b4072e08095fa84f96b0fe3387ec8f302afde022186aa3eab5 in / 
# Tue, 15 Aug 2023 23:41:01 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:42:07 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4513653e4d749342b34f60c592adaf0ef4af993e76a913a1c086a4229a0e3afe`  
		Last Modified: Tue, 15 Aug 2023 23:45:54 GMT  
		Size: 49.5 MB (49531730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa17cee307bdacaae57f147ba0619032cfffadd04964efbb24024ca12ea8837`  
		Last Modified: Tue, 15 Aug 2023 23:48:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:a6f79caae9ab92f696cea7ebba8472268e1fd5fc7287ce82716a1dcdde1e1d26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50631580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d4395e55f3f09d62d21748f768187def9b8806b094607456ced6211b7252ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:34 GMT
ADD file:d86f66385d3993c597ac040a976cd8a826b097d014cc4f3b69d8ebfaa5aa6eff in / 
# Tue, 15 Aug 2023 23:40:35 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:42:05 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e41394c7daa90fb4aae0f67d43af5ee9838fb125e249fc0002bfdc3b90bb6c05`  
		Last Modified: Tue, 15 Aug 2023 23:46:33 GMT  
		Size: 50.6 MB (50631355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e323c216a876bebcbf917fb42c503130745bb8533dff5c6243677f5816c2fb8e`  
		Last Modified: Tue, 15 Aug 2023 23:49:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:44e8c187e0425c6697750139a145c593a006be3bc888c30cadaa6a12b58dfa59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49467904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf794caeea741229f0023d87799f04c1d7ac32b0bfc5b4fdf9506f9efc6becb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:11:47 GMT
ADD file:95c4283b49c4076aa446c4909c0386daa26321718fabe3edff87607f56ccb9ab in / 
# Wed, 16 Aug 2023 00:11:54 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:17:27 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:167a77203e448948dbd4957f755862086635c866238669801438bae10f7d885b`  
		Last Modified: Wed, 16 Aug 2023 00:22:59 GMT  
		Size: 49.5 MB (49467676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8661d5236c93648f581dd0bbe1fc69fdd7927c5b56dafcc9b16dae2de296705a`  
		Last Modified: Wed, 16 Aug 2023 00:28:42 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:665057e4c4ae6ca40388742dfb182560f556f00315e47223fdfe232bb425560a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53552105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01d33da77e6a6b1f6d60654776da48bfd8e928958d5980c0ff1e430709eec90`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:11:08 GMT
ADD file:34567402b37eab48970f90189fd56c47e39acba6d260f0587409ca36a8d36458 in / 
# Wed, 16 Aug 2023 01:11:10 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:13:57 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c0db36c7b4f2702f9e0075ee892fe4761e0f37f5cc9d73192725313c01591737`  
		Last Modified: Wed, 16 Aug 2023 01:18:29 GMT  
		Size: 53.6 MB (53551877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282ae467e6c999f35f1c37c45c957c98823a99b4f75e503ec57ee6a649d3b64`  
		Last Modified: Wed, 16 Aug 2023 01:22:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:6c4d765e29e4c70814cebb09cce5b45d23b440008486949921dd8f9413a1cb05
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47907154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac2b2260dd9170b7e1e008d9c6016b387e65a4fc5582ef6bb142f98c5b5980b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:09:00 GMT
ADD file:425a1fbb6a9b871d294541070ed62c4bf0d64e4674431534a38dde2ce691632b in / 
# Wed, 16 Aug 2023 00:09:02 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:10:46 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:016caa5aefd52499e5a24161e54aae743adb2b8df6f4b4dfa6fde37f4391ec21`  
		Last Modified: Wed, 16 Aug 2023 00:11:48 GMT  
		Size: 47.9 MB (47906926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4404529d310595b6572516a1acdd73441e86c644e227b4b5f00528f0e4f3630f`  
		Last Modified: Wed, 16 Aug 2023 00:14:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:6cc309ca7893ab8b32b72ae06d2826ab2a8c89a38177ef8ffb8966116f1afad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48594621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755590bbeb7ab6bb277eb1794c5a52b2f86c06b4ffd45cee2a3918083c9e42ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:43:50 GMT
ADD file:a27e7d7c954291d644437a8054f06f492700f1ce13d3a9e2c3bbd71afd0869cf in / 
# Tue, 15 Aug 2023 23:43:56 GMT
CMD ["bash"]
# Tue, 15 Aug 2023 23:46:34 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:db9f34e47daed3854a411cee94f611a7139b82002ae54802c9a44d3faccaaea7`  
		Last Modified: Tue, 15 Aug 2023 23:49:01 GMT  
		Size: 48.6 MB (48594395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c97c49f18f8a1b027269794dab7d477ddaac2db4db8112ea7c2bd0e0c6d09`  
		Last Modified: Tue, 15 Aug 2023 23:51:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
