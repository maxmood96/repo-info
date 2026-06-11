## `debian:rc-buggy`

```console
$ docker pull debian@sha256:7eb64c441b334d6435fc514f31ef348b2c42c7a403905830366fbf2e36ea2d8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:575a976e47dc70ad8866ed5a4c225308ee032ac3009da1b93a19710d668d1247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48801437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74c2d3e585daa3916050faf0c65b0e111f35eda28f44e08d4fcd8bd6e3ad8df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:16:14 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e4bfb5fe24dc0230d4f97c7feccc03abb781a438997364a53c10057b40c735`  
		Last Modified: Thu, 11 Jun 2026 00:16:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:eff2c7644bfdf6cb1ad3e1299c5590bceb12b192c00c7c627942b7550f9541bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591ce2b94d3a56b142e034a1fba2cab9aed79273a455fa2c49a2200573cf4a0b`

```dockerfile
```

-	Layers:
	-	`sha256:6a610bf347b5c0fd8e70a86a159c3f77565db14432d26cde08ff383c5873d56c`  
		Last Modified: Thu, 11 Jun 2026 00:16:20 GMT  
		Size: 3.2 MB (3153477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8063c8e208576ff5f98486ef6b59ebae8888eaba8c1e635258165c99180e77a`  
		Last Modified: Thu, 11 Jun 2026 00:16:20 GMT  
		Size: 6.1 KB (6055 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:64b80277b3be0a923b2b9a2b92b65542f774db9dfe75ad7d8cd7f4aa8e8af598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45703465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a236065e56bba9dd93ed63e18cf618679dfd9f08a71d1a427bf68b50088e8dc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:16:04 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6dddbc4e0b590efd809489171b20c0c05ae23facbf49b0dac491dc8f542364ec`  
		Last Modified: Wed, 10 Jun 2026 23:42:26 GMT  
		Size: 45.7 MB (45703240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f48a3dbdc2a4dd43b6c0aa0290d531f0398ce02b5bae36e8beaad10663c428f`  
		Last Modified: Thu, 11 Jun 2026 00:16:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:1cd801e24dfb159ace5af159cb5dcf51a52a7af905c4957fc0dd9da7dad4134a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0f1729c403d0c9572fafa098268b22b2ac23725488f0baf01a06e911976a17`

```dockerfile
```

-	Layers:
	-	`sha256:1cc6306a69eadf77ca9589d6f0ede44db01716629bee6d045d2805e7c69b75b2`  
		Last Modified: Thu, 11 Jun 2026 00:16:10 GMT  
		Size: 3.2 MB (3154847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc778f0387cd671e42a633a217ac3356fbf932e6b589e58b5b30e2299c1f6d14`  
		Last Modified: Thu, 11 Jun 2026 00:16:10 GMT  
		Size: 6.1 KB (6117 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:febc13602ee3ee825613224c7fc545ac8b216c063ae647f155f22f2e47c2488f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48818782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce93c81d966df9c90aec6a680b0b7df2f0945cdfa16f0d0d71285c24da96813f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:15:31 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6690e347586746af2bdedf6049221922a991b4799733e8eae40a661a548a49`  
		Last Modified: Thu, 11 Jun 2026 00:15:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:9c1dcd0817f2034813731d24c8ec3c81f057f41eb65b7a2cbb4ccbb1022cc2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b29fccf5a8ad88d2b4bf53a36934b4718b45498e5611dda1ea8b02e640013a`

```dockerfile
```

-	Layers:
	-	`sha256:7878a17f9cae5b4d3f5839fc0e1bdccd3f5f3b533e1ed1552620c7fb8250cc9e`  
		Last Modified: Thu, 11 Jun 2026 00:15:38 GMT  
		Size: 3.2 MB (3158159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb10560c3245f4c96be27c09a42ab52d0ac6369d7033d92ed59b2b2586e4feb3`  
		Last Modified: Thu, 11 Jun 2026 00:15:38 GMT  
		Size: 6.1 KB (6135 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:84c4b23700957c057125ba11997407450e4088b643f8cc6753e83726f0540550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50105625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b03f075b3c71f76b19494b1118dad2dd8b77543ae30e632ed83ca6795c421b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:15:52 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:a32252638de41825057387ef73b5d4de843fa9726fc243c76636da258263cc3f`  
		Last Modified: Wed, 10 Jun 2026 23:40:40 GMT  
		Size: 50.1 MB (50105399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095eec939130c3447b4b7681c64f61614e9ca2f074ea6a8af24703e3619c3cb4`  
		Last Modified: Thu, 11 Jun 2026 00:15:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:a4746b46a8b210c7dbee9bdd9e9fd60b309f076ae48c884639f1222c6dca9a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90b80e2556f2cee8ac79be2ac00a82c5f7502a9049daaca93d616382149a65f`

```dockerfile
```

-	Layers:
	-	`sha256:1cd933b499acb3b4553436862f89117c4a4654bf6bbb571a99a0c0e56692745c`  
		Last Modified: Thu, 11 Jun 2026 00:15:58 GMT  
		Size: 3.2 MB (3150673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d885ee43f43ff154104365f6383e5430d7f84aac3fc2bcc38cc7799e638f202`  
		Last Modified: Thu, 11 Jun 2026 00:15:58 GMT  
		Size: 6.0 KB (6034 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:2596d120f3fc0763958af83e3889d21bf1c457d46fcc6fa2836bc7bdbb2cce10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54046348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596660fae76660d9cfb27ff2fb25af3a5a40d513a9910cf00e52569fa5d6ac8a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 22:57:06 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:0bda88a8fa865607f7a3bfe01b25fa99681c2572077bbfaf6b7e16e1f51b5b50`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 54.0 MB (54046122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fa55d9bfda937f854aadecc43e80392689ac4cf3d469274dd108a6cb24b88c`  
		Last Modified: Tue, 19 May 2026 22:57:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:c3ca163c29a2fc5da980bd5a496addaa1cae9c17108e1b1aa9c04c56baad489f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2694dd20715b7cdfb71311d18c859b64d442cd2aca098a6e24b0d1cf8ffcf51f`

```dockerfile
```

-	Layers:
	-	`sha256:bae3757dabbf83fcd64be41b1fc276ef844ba714d6af9788ced573f202e8ac7a`  
		Last Modified: Tue, 19 May 2026 22:57:18 GMT  
		Size: 3.1 MB (3148585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191f6627d54545e891e46061eb43dbeb9100890bf29874562f941c903d780668`  
		Last Modified: Tue, 19 May 2026 22:57:17 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:671df20e38881595d9aae2b895a2fa73c1f7784f96bf93783e7d54343bf7201e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46808623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ba03718a25cdfb79d47b8e8fa80dbdfd24ffb9b8e0a5129cd31b02741f1419`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 01:53:21 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d609dbe8a64103ca9a52594c54358bca867134ca11c5bdbab5024849e5765438`  
		Last Modified: Tue, 19 May 2026 23:39:28 GMT  
		Size: 46.8 MB (46808398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d2d041bd6bda77686d57014db197a623dd9fc68cf6cb4ec5300adec86f95c1`  
		Last Modified: Wed, 20 May 2026 01:54:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:8f7ced750b15e09f4b732777a2b329a8e33c4454b73e8d3adedb25ed0447a379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3142676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6256e28a2d1c2a0d7470807efeee79982ae332243d1af8cbaae34f4a87e3534`

```dockerfile
```

-	Layers:
	-	`sha256:3f51651757f3de963e5a012939139fc55d65f4e39732b8e9d21cd4c7e0cfa8b6`  
		Last Modified: Wed, 20 May 2026 01:54:13 GMT  
		Size: 3.1 MB (3136588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637296b259d2263737f1073aef8e8ee5da06ae84adedef73f5b6ae60d3286efb`  
		Last Modified: Wed, 20 May 2026 01:54:13 GMT  
		Size: 6.1 KB (6088 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:84ed11d1f796e74d22413448838baed846fa46faffa66d0f43f0b5d7888b752a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48542044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f38843e5c17c4e57e72d9f00125bb2fe452b03027ae23fceb64e430e6b9e37d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:15:47 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:fb23912042361f66d2c3fed63550770682f92117280cb0cf2a2611ef14ea13e4`  
		Last Modified: Wed, 10 Jun 2026 23:41:42 GMT  
		Size: 48.5 MB (48541819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cf07a1a14e33306090d7af6de63339f2b02e34496730ab6034cedeec75e105`  
		Last Modified: Thu, 11 Jun 2026 00:15:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:547f06d75aa3af63df53934613e25790ca22daa1fc8962a465f6cddbc1cd3c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc477c1b3ab6595867eef0d776efde2fb81ea56cd32ae8fc7bea3fcfa26de5b0`

```dockerfile
```

-	Layers:
	-	`sha256:c30aeed4cd48ae9c8944a5fd35f14c3db44a6e09e52584eee6f37a8dcbb6fed9`  
		Last Modified: Thu, 11 Jun 2026 00:15:59 GMT  
		Size: 3.2 MB (3154928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd2c30236215ae06d88abf6260c1a470da037cd3ddf07e9bb9013826461a5ef3`  
		Last Modified: Thu, 11 Jun 2026 00:15:59 GMT  
		Size: 6.1 KB (6056 bytes)  
		MIME: application/vnd.in-toto+json
