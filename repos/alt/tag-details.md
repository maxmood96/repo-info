<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p10`](#altp10)
-	[`alt:p11`](#altp11)
-	[`alt:sisyphus`](#altsisyphus)

## `alt:latest`

```console
$ docker pull alt@sha256:038031df9afd7e2763c01015933957bd0565666f598b0611c0fa51c6a1797594
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:f20f0ad15c09157813314b8479e40273b77f3433941a19fbac23e218cc04a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47309675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f407182509fea72dd4f82b597674b168f692fc7dcd8cdec94af340c928f37239`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:57 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:57 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 16 Dec 2024 14:36:57 GMT
ADD alt-p10-x86_64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:50159fc3f76b019eaca637bf01a40448dfb722352af8fe507ff41fc1d40ac646`  
		Last Modified: Mon, 16 Dec 2024 19:28:53 GMT  
		Size: 47.3 MB (47309485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305aa293179e1c4469d9f86b52eab3d902aabdf65c10396aa7eaa12951611ede`  
		Last Modified: Mon, 16 Dec 2024 19:28:52 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:b3c3c0ca9cb4cc8b095ac191e41a57e4921279b70e1c31e6a7566d1542eafb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897a63af4f27ae005ca50255bce8198ffe3a34d43a499f659b58a58cdbb3a6ab`

```dockerfile
```

-	Layers:
	-	`sha256:6af45dfde2a25adea6d957249e42d54a7a129be472c20af0fcce64b881666c3a`  
		Last Modified: Mon, 16 Dec 2024 19:28:52 GMT  
		Size: 2.6 MB (2583024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0adb35242a289736816c728d3f56b9769f700a275b1a079b301993f551016e`  
		Last Modified: Mon, 16 Dec 2024 19:28:52 GMT  
		Size: 6.2 KB (6220 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:0d61ad43699c07781490f0cd35083b944311b0718582af19b0d81253ff469d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46478952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8795a5a34811cdbdccdb3c67c8a7fbec4c650bc916186720eebc2e69e4bdc2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:57 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:57 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 16 Dec 2024 14:36:57 GMT
ADD alt-p10-aarch64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e95438d51f0a00ed13b34c8f865621a3d5c62107f755de7c230e8f5fb0b1a0bf`  
		Last Modified: Mon, 16 Dec 2024 19:28:46 GMT  
		Size: 46.5 MB (46478761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f723c247bf307d37b37b4e7b5272b0a0a88c5351e57d157812c3c3500fffa4e9`  
		Last Modified: Mon, 16 Dec 2024 19:28:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:bca4abf9bf35d17395dfc7f59070aea6150de593eb4da17ef95481272010bded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2587954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a687319a517417fc2d4f1f1616348a81cad4e8ae4a2181ff79d9b804a2efb4e0`

```dockerfile
```

-	Layers:
	-	`sha256:fa9e1daf5ec6c861a3002874080ce66b62a4644870643a14f3465ae72aa7f7c7`  
		Last Modified: Mon, 16 Dec 2024 19:28:45 GMT  
		Size: 2.6 MB (2581677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7e4b0c37583cce18d98448691a83d491676e1e144de0dee850ac08f2df48cd`  
		Last Modified: Mon, 16 Dec 2024 19:28:45 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:e7110a73f0673063df85e6d1c768432f22b7f7161c8845621067d30656481e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48049552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d80702fc7efc2ae8da31546d46e59fc68e260b2183181cc3815edb96fb2f64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:57 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:57 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 16 Dec 2024 14:36:57 GMT
ADD alt-p10-i586.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19d9f85d79e44fccd4cb62196723a9dd6cf964c27f2cb8c9c7b56033d033d483`  
		Last Modified: Mon, 16 Dec 2024 19:28:58 GMT  
		Size: 48.0 MB (48049361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965dce7f9e6aee9dc85f5938a87aef4cec0f8646525d86ead80ab64f34149431`  
		Last Modified: Mon, 16 Dec 2024 19:28:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:8f51a247e4b1642ef9bb0d9c08b1f260e38aa83f035a8574ab63f5fccbe6a44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196d733b6b30f79244afdc1e3c2391cbe3d27b16353e5e19b6fe6f83ec22b77a`

```dockerfile
```

-	Layers:
	-	`sha256:68df70939b90577291c020e25c176c113c2db90be0ca31576c425effe30dcedd`  
		Last Modified: Wed, 08 Jan 2025 04:27:40 GMT  
		Size: 2.6 MB (2584867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566ea5fa42544eba5d9d314dc35b916c0447e3e1aa53b790dbc73bea4c976c7e`  
		Last Modified: Mon, 16 Dec 2024 19:28:57 GMT  
		Size: 6.2 KB (6192 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p10`

```console
$ docker pull alt@sha256:038031df9afd7e2763c01015933957bd0565666f598b0611c0fa51c6a1797594
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:p10` - linux; amd64

```console
$ docker pull alt@sha256:f20f0ad15c09157813314b8479e40273b77f3433941a19fbac23e218cc04a6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47309675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f407182509fea72dd4f82b597674b168f692fc7dcd8cdec94af340c928f37239`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:57 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:57 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 16 Dec 2024 14:36:57 GMT
ADD alt-p10-x86_64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:50159fc3f76b019eaca637bf01a40448dfb722352af8fe507ff41fc1d40ac646`  
		Last Modified: Mon, 16 Dec 2024 19:28:53 GMT  
		Size: 47.3 MB (47309485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305aa293179e1c4469d9f86b52eab3d902aabdf65c10396aa7eaa12951611ede`  
		Last Modified: Mon, 16 Dec 2024 19:28:52 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:b3c3c0ca9cb4cc8b095ac191e41a57e4921279b70e1c31e6a7566d1542eafb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897a63af4f27ae005ca50255bce8198ffe3a34d43a499f659b58a58cdbb3a6ab`

```dockerfile
```

-	Layers:
	-	`sha256:6af45dfde2a25adea6d957249e42d54a7a129be472c20af0fcce64b881666c3a`  
		Last Modified: Mon, 16 Dec 2024 19:28:52 GMT  
		Size: 2.6 MB (2583024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0adb35242a289736816c728d3f56b9769f700a275b1a079b301993f551016e`  
		Last Modified: Mon, 16 Dec 2024 19:28:52 GMT  
		Size: 6.2 KB (6220 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:0d61ad43699c07781490f0cd35083b944311b0718582af19b0d81253ff469d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46478952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8795a5a34811cdbdccdb3c67c8a7fbec4c650bc916186720eebc2e69e4bdc2a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:57 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:57 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 16 Dec 2024 14:36:57 GMT
ADD alt-p10-aarch64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e95438d51f0a00ed13b34c8f865621a3d5c62107f755de7c230e8f5fb0b1a0bf`  
		Last Modified: Mon, 16 Dec 2024 19:28:46 GMT  
		Size: 46.5 MB (46478761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f723c247bf307d37b37b4e7b5272b0a0a88c5351e57d157812c3c3500fffa4e9`  
		Last Modified: Mon, 16 Dec 2024 19:28:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:bca4abf9bf35d17395dfc7f59070aea6150de593eb4da17ef95481272010bded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2587954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a687319a517417fc2d4f1f1616348a81cad4e8ae4a2181ff79d9b804a2efb4e0`

```dockerfile
```

-	Layers:
	-	`sha256:fa9e1daf5ec6c861a3002874080ce66b62a4644870643a14f3465ae72aa7f7c7`  
		Last Modified: Mon, 16 Dec 2024 19:28:45 GMT  
		Size: 2.6 MB (2581677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7e4b0c37583cce18d98448691a83d491676e1e144de0dee850ac08f2df48cd`  
		Last Modified: Mon, 16 Dec 2024 19:28:45 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; 386

```console
$ docker pull alt@sha256:e7110a73f0673063df85e6d1c768432f22b7f7161c8845621067d30656481e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48049552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d80702fc7efc2ae8da31546d46e59fc68e260b2183181cc3815edb96fb2f64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:57 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:57 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 16 Dec 2024 14:36:57 GMT
ADD alt-p10-i586.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:19d9f85d79e44fccd4cb62196723a9dd6cf964c27f2cb8c9c7b56033d033d483`  
		Last Modified: Mon, 16 Dec 2024 19:28:58 GMT  
		Size: 48.0 MB (48049361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965dce7f9e6aee9dc85f5938a87aef4cec0f8646525d86ead80ab64f34149431`  
		Last Modified: Mon, 16 Dec 2024 19:28:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:8f51a247e4b1642ef9bb0d9c08b1f260e38aa83f035a8574ab63f5fccbe6a44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2591059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196d733b6b30f79244afdc1e3c2391cbe3d27b16353e5e19b6fe6f83ec22b77a`

```dockerfile
```

-	Layers:
	-	`sha256:68df70939b90577291c020e25c176c113c2db90be0ca31576c425effe30dcedd`  
		Last Modified: Wed, 08 Jan 2025 04:27:40 GMT  
		Size: 2.6 MB (2584867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566ea5fa42544eba5d9d314dc35b916c0447e3e1aa53b790dbc73bea4c976c7e`  
		Last Modified: Mon, 16 Dec 2024 19:28:57 GMT  
		Size: 6.2 KB (6192 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p11`

```console
$ docker pull alt@sha256:301f3053b315587a1584d32f0d46dd9ab3f41120b5b0506e991fb43f1747fd98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:p11` - linux; amd64

```console
$ docker pull alt@sha256:9dedba42989ebcdbd892f296824b8b368779f72f8169c5b014633b9d8c3467ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45396280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2d7fe0f1ad861a6782b49eaab8042c9c14a729b4aa3fb9cc6305dfb06a63e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:37:11 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:37:11 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 16 Dec 2024 14:37:11 GMT
ADD alt-p11-x86_64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:37:11 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:37:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c92e156546b88a6ddd15a15eee145f0b5e3af28bc3ef2cfea960e8f10ecf32c`  
		Last Modified: Mon, 16 Dec 2024 19:29:03 GMT  
		Size: 45.4 MB (45396090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5801442761eef41b14b09fa9540c39d942fa60a0a4002f61790a9e373c39b796`  
		Last Modified: Mon, 16 Dec 2024 19:29:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:7185125396d9c482029907de4d17cc7d868aa293e59e7eac37e776c0ff729845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2549930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10403d0e69ce4282f4d1ead346d979f517f95865aa2ba918edc647419c47ca41`

```dockerfile
```

-	Layers:
	-	`sha256:827e3ffb7563d0e537cc681d353015a768f66f8f974713a3dfe8158d10d69586`  
		Last Modified: Mon, 16 Dec 2024 19:29:02 GMT  
		Size: 2.5 MB (2544002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88469538de8f79150fa5542084fbb438f2beb98508f505cbb66a5f31115d3f2e`  
		Last Modified: Mon, 16 Dec 2024 19:29:01 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:d1c668dd6fbbb7a449532409cd5f199aa85c883b9db7598973d8ccb8e230d4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44180690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59dac6a0134a5260afd910bebedddb2033b861ce2af5cba70acc49ebc7ad255`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:37:11 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:37:11 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 16 Dec 2024 14:37:11 GMT
ADD alt-p11-aarch64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:37:11 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:37:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:48fac58b293355fcc6b8cd299102a1b54d4018c79d2cfeb732074223fa9aa22e`  
		Last Modified: Mon, 16 Dec 2024 19:29:51 GMT  
		Size: 44.2 MB (44180499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c81a85bcc8f7c1cc02a280a357ae822f37fa22c7b5b17caefb3e7f7de8cbfb0`  
		Last Modified: Mon, 16 Dec 2024 19:29:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:da047fa1fadf4494db61e578c928f4e82b551d5430db8b91136423b496b4651f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2549393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b2fe92a1e6badb682867e744b613e8e9a84ecae0b8f879dd3d8c85cca2da8`

```dockerfile
```

-	Layers:
	-	`sha256:9e04a9f2a286c1a32a5203c2d026a291bc2eb8b9659f91a9b1a4a8353d39ad87`  
		Last Modified: Mon, 16 Dec 2024 19:29:50 GMT  
		Size: 2.5 MB (2543419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02882831f5b164083e5af054b92258525bfa090183201f56947771ba5a2861e7`  
		Last Modified: Mon, 16 Dec 2024 19:29:49 GMT  
		Size: 6.0 KB (5974 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; 386

```console
$ docker pull alt@sha256:c6869a756c7eaeefb653d443d6631bea57fa2a5c13e99493a57698772aaf86e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45522315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5d60a775b546624e15719ed47c0fbf2a5984bac8fec88380db157fee1f9159`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:37:11 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:37:11 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Mon, 16 Dec 2024 14:37:11 GMT
ADD alt-p11-i586.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:37:11 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:37:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d67dccfb5a4cd59688755934beea3e27b8a44c5965d4f9ea3accb734887e933c`  
		Last Modified: Mon, 16 Dec 2024 20:07:50 GMT  
		Size: 45.5 MB (45522126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4972dc96b34bada29a11fb90a221de63b5cc8bd6fcf56f28fd25a22a4ebdf19`  
		Last Modified: Mon, 16 Dec 2024 20:07:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:f2fca51735d2ec55a95bf933c6a2cc0715ad45d1ffec7babbf33452be287ea5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2548634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417cb7df2df5cd709579967d65a2272919279d60e5823c52f1e24428db047cf5`

```dockerfile
```

-	Layers:
	-	`sha256:78236f5199606685e53ff2cc04c8bc272f0d0fdf40d5392301a25d84bbd345ec`  
		Last Modified: Mon, 16 Dec 2024 20:07:48 GMT  
		Size: 2.5 MB (2542728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927b48b2558e67401fdccc3eefd4c84ec97370f46ba876674cc6a30dc368fc18`  
		Last Modified: Mon, 16 Dec 2024 20:07:48 GMT  
		Size: 5.9 KB (5906 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:sisyphus`

```console
$ docker pull alt@sha256:c7421cbf44aedaa68ee768f9c6a3324ee04ddf3387fc8394da7725b11559316e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:6f7fea3d1247c5ee6a916be2ead216c209ed05bac5229f3d28149684019ee051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45505331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adca784378c208389d56c53082d07dee60ac6179df0bd4d33470ea4a6c3db35a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:44 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Mon, 16 Dec 2024 14:36:44 GMT
ADD alt-sisyphus-x86_64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4a707a4b524da355aa2661fc84e24d6a08c202cf5fda50161e2d329195657ab3`  
		Last Modified: Mon, 16 Dec 2024 19:28:54 GMT  
		Size: 45.5 MB (45505141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7e687c280fedf3243dc7fbe55445e4ec02ead2f1d2b11851f7df09e9380e52`  
		Last Modified: Mon, 16 Dec 2024 19:28:54 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:8d13aacc89a13fac4bd29a7bbe29eafc06b0ab560323655339ba9ba1d079f16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0322b24417506c3abf9852ad3a54b49d63669b2ca9e5915e02a97bcdbb5b6`

```dockerfile
```

-	Layers:
	-	`sha256:b150d472e8d5bb0dcb21e5f962a82a6a48f74172d3de608ae8adc7a341e916c4`  
		Last Modified: Mon, 16 Dec 2024 19:28:54 GMT  
		Size: 2.5 MB (2533363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e132186628c570f5a24fdc80509d846ad0f441405ec029c4779c7e42be14c654`  
		Last Modified: Mon, 16 Dec 2024 19:28:53 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:e6bf293b72ed6aecd514b7d91f6ec0fa3dcc9ea29e8ef1c414bd8262f3892ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44254122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910629b4193f2cbc56bab2fe15015a7b71a9d0da77aacae8767dec661c4374f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:44 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Mon, 16 Dec 2024 14:36:44 GMT
ADD alt-sisyphus-aarch64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ea1735b70c58d9efb5003f5dfc209e327de3647324cadde458c8e93afcf15dd8`  
		Size: 44.3 MB (44253931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48eda5e1ae93b6f3f1c9181465a233ef6ddd8c59e0c4e4d4a78ef88d348a96`  
		Last Modified: Mon, 16 Dec 2024 19:29:14 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:f8d4a3c5ca8ca00712540fe30c579c046fbd34309bb9c5190b43a09efe173132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5207a659d9b3b493055bf8782b8f2a6f9fce075f58490c5b390efa362e8ccabc`

```dockerfile
```

-	Layers:
	-	`sha256:69d494c76e5d451ad675cf882d0761c341c3c1e58057ce9d6cdba7e8397995da`  
		Last Modified: Mon, 16 Dec 2024 19:29:14 GMT  
		Size: 2.5 MB (2532780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd991cd33bbafb53ffcf8dfbb1f27c399c9a5b8fa23a6f954de97c2e49335ce8`  
		Last Modified: Mon, 16 Dec 2024 19:29:14 GMT  
		Size: 6.0 KB (5973 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:6c8c0dff2b88e84a2b5d3fa11a0a5c51789bd06e131dba746f897357eba048a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45639954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6771b2eb983c39698335e1fd3e8f29872da34b4008d57a08ee982e54fa8edae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:44 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Mon, 16 Dec 2024 14:36:44 GMT
ADD alt-sisyphus-i586.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:def943c8cffd415034ddfb74d8f0a578f4e6c938973fba283ed07adba55cdd47`  
		Last Modified: Mon, 16 Dec 2024 19:29:03 GMT  
		Size: 45.6 MB (45639764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3681c9fb5a9618c6a3a82e1e226eca51c93c7503673ebacadcc0d4a4599d75c`  
		Last Modified: Mon, 16 Dec 2024 19:29:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:eced92d674166746f5e113fafab8ad4bd46d03a2ed014c6eb793c842ef06976a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1600cb93ac90657ce45b571e27cd9a04128fba7e39dd2849571ba288c46ae4bd`

```dockerfile
```

-	Layers:
	-	`sha256:75107a66673639a1ef669bb04ca4842aa86b4e8ecbac60cb695be7c026de17ab`  
		Last Modified: Mon, 16 Dec 2024 19:29:02 GMT  
		Size: 2.5 MB (2532089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f484c446b47290b41bff29655469976ec8e0bd471a35c5036221b22d42f0a6f`  
		Last Modified: Mon, 16 Dec 2024 19:29:01 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; riscv64

```console
$ docker pull alt@sha256:9febaece423faba191f374279ac3c8c1e10955324039024573e91af7422a3099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43490441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec68f85f0afed86d2ea3bf3d2af60ee3dc0406df9a26c1a9fe769c73dbe902d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:44 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Mon, 16 Dec 2024 14:36:44 GMT
ADD alt-sisyphus-riscv64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:60b576ed3f359143510ff313ce327adab2c0f10f63d352a0e668b669c74b1713`  
		Last Modified: Mon, 16 Dec 2024 21:06:00 GMT  
		Size: 43.5 MB (43490250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54fc37e6507857ae3a2fdc4a8ae3aff6eb9e43d985f77bde5c90cbb9e72b9e8`  
		Last Modified: Wed, 08 Jan 2025 05:27:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:b6ddb1e9a0bdc34a754066bd79539aedd9699c6a1cfdf41cc7b09972f321e7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fff6ec339f566d0f19bfefbedfd8487c69a9e7e01692e7c500487e9df4bdfb9`

```dockerfile
```

-	Layers:
	-	`sha256:2e6390fa390e4826ea21d3a88edb3eaf771387080f195a9f020b4a04abd5494e`  
		Last Modified: Mon, 16 Dec 2024 21:05:55 GMT  
		Size: 2.5 MB (2532031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b1d10e49b0feb7cb96d6098f024930df063589f2a05726b8ff62504dbe4f7c`  
		Last Modified: Mon, 16 Dec 2024 21:05:54 GMT  
		Size: 5.9 KB (5947 bytes)  
		MIME: application/vnd.in-toto+json
