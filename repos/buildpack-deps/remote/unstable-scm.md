## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:3473523d960fd2a4a0eed194b4dfea595584e6d4ef8337e1f62dd33d323d390b
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:443be2e684c2974f94329fe904ab025826cd45f4a1dc52a922e5b01e66e75ee0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143526369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2039b5a723b3ea6face574998f280f6ceffa6fccad4d36d491512b3da12727d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:22:38 GMT
ADD file:3a737ad8ab65fe5ad068d6094fbf99ce9ed2b5beff9c86daceee8c2c50182bde in / 
# Tue, 12 Mar 2024 01:22:38 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:58:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 05:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:490d250d3b2798e2c88a398b87b4162c8ca53e579e4e79b47fc41c2c2aaca6fb`  
		Last Modified: Tue, 12 Mar 2024 01:28:23 GMT  
		Size: 51.5 MB (51512918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355c7ca394663c3c42de69370984f58c9ec1386fb7bf3892311813e2a6b72eff`  
		Last Modified: Tue, 12 Mar 2024 06:05:25 GMT  
		Size: 25.7 MB (25711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7869bc1de22dbe818f4e768896046e07c479ab857f8c3b31b21028de11d24a`  
		Last Modified: Tue, 12 Mar 2024 06:05:43 GMT  
		Size: 66.3 MB (66301825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1cec2114b9fbc4843b5cf0b9c8fbaa74c4b4b83edaefe5346dfc5a2325eb6d89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136584148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f9fdbbebeb90640507c0fe9c9c7f94c49092e2b2457779acf670d041930ffd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3a1cdabe4cc17ce6f55149b66ca7c16793fb014ff72d99cb1da643581eed76`  
		Last Modified: Tue, 13 Feb 2024 01:56:59 GMT  
		Size: 64.1 MB (64108591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:779fa01b9f5918a69716dbdf3d599dd12913476ec65cd9c5bc05a41183678baa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130757215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d298e5bd648d71e4c86864a1c66f3452d3e31f41781f27ee8a9c9d9a15fd7f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78cb86ad182c3cf9cfed5742a1bbd6365a9bcb95a5f378a558088dbcfe7364a`  
		Last Modified: Tue, 13 Feb 2024 04:31:10 GMT  
		Size: 61.5 MB (61467747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2828cf65ed74a397e66e8fb3eee64bde5f30b20ff6c647bc0748dda91ba50370
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143297356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2904dfc2bc2f7f22ec601d0030925c6a14c76a586d20c697612925d4c9d3a53`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:41 GMT
ADD file:1202a56d8723ce5bee3f68e3d9488cef88889fe8b2bb138cde766ff787577a7b in / 
# Tue, 12 Mar 2024 00:46:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8e7b106821c007c3c67e9a4d248bd2f87194491ad746f2aa752c5b0ba2fca099`  
		Last Modified: Tue, 12 Mar 2024 00:51:35 GMT  
		Size: 51.4 MB (51353263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa13c84a803d4b150b717babd5d0b89e39ce55a7c4c07cfbc3d34a5e4ce85a3`  
		Last Modified: Tue, 12 Mar 2024 01:37:43 GMT  
		Size: 25.4 MB (25434519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde6d0bb19e702e70dc6d3b44c7538729b197d5c5c229f8df55709b3de11f031`  
		Last Modified: Tue, 12 Mar 2024 01:37:59 GMT  
		Size: 66.5 MB (66509574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1d068729c332ba11994a4cff5131b01c94ff9b6b92efdfa718e6c21aa56b8894
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147235669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d65163968032c49ce45edab4098c152481665b9dd3c1e75b80a67e305e8268d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:40 GMT
ADD file:383595e3854ec7f22e8d333af3b6c0a5019c955f674a09a7c4bf1426ec9a661d in / 
# Tue, 12 Mar 2024 00:59:40 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:46:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 07:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8c85e8b663e835053744f416ba1ea5847d00b7b5cb5dac4003e16ea78fe851b3`  
		Last Modified: Tue, 12 Mar 2024 01:05:55 GMT  
		Size: 52.3 MB (52250465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47f5bc6b01caab5e3d97a2a46e554fe0cac205e65d3b0b4fb06e3bd93583c05`  
		Last Modified: Tue, 12 Mar 2024 07:57:19 GMT  
		Size: 26.9 MB (26929666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83523fbcb482e27c181ca315a9234a6bbd14109883ecc6509e9a1578f28c3ce0`  
		Last Modified: Tue, 12 Mar 2024 07:57:42 GMT  
		Size: 68.1 MB (68055538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1035f1df46dc1a3aae80e09fa436194138f417ec7050a3ddd0fefb13e69f7343
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141707822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135a4453410ccc2df5a3d1c5524d8d9332846d820085bbe6c66a5183e1f5e491`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:09:20 GMT
ADD file:19ebc3428f26cc4bc4aed9fbd4cf7f5f3ee4b77b9740ca3ad10c77626e14bc82 in / 
# Tue, 12 Mar 2024 01:09:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:38f59bdee9eac9fb953df0852a9bf0458844eaf90c474ba863879a284671eca6`  
		Last Modified: Tue, 12 Mar 2024 01:21:04 GMT  
		Size: 50.6 MB (50572329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77dad95891fc49c3987711b4646cb679c4a443baceb97ed9b60ab673bd2cbc6`  
		Last Modified: Tue, 12 Mar 2024 02:48:12 GMT  
		Size: 25.8 MB (25808530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f996b43c740b01d384ef1b4622f6eac51f1f4cb47817c970679a8ba8881f17`  
		Last Modified: Tue, 12 Mar 2024 02:49:05 GMT  
		Size: 65.3 MB (65326963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:51bb8364428f698a10be2b4220014b6b4b390e18d6353d03d26159682dca6ba5
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155117994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c97a92304918645a7b172d3251d3dc8b778c7b238d5df12fe2f8552d0debba3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:32:08 GMT
ADD file:5a26866ec93cd672e68eb3b6408e2d78eb1ceb2804d316ab9e215bb248c396ea in / 
# Tue, 12 Mar 2024 00:32:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:51:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:53:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d54e43a79af3d6c46553326fe893093beb487d05a53a78510db1edf5ad46734`  
		Last Modified: Tue, 12 Mar 2024 00:40:01 GMT  
		Size: 55.3 MB (55261063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b06e7f021e50f240952103e6d889ea6a36f09aeae1132a71b34e28c7e5d70c0`  
		Last Modified: Tue, 12 Mar 2024 02:22:32 GMT  
		Size: 28.0 MB (27970194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f298aba92b6ebc1731fe8f0003d6c289890904a73a002d5cbf70fa000e9f484e`  
		Last Modified: Tue, 12 Mar 2024 02:22:52 GMT  
		Size: 71.9 MB (71886737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:152a5cbfa44cf71e3e69318c518f5dd28d8dbbcbe55be8def9fe5a694621dd00
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141027990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ea7a8dc3cc9e8e9699bee6e7550865e5641da7a9b5efcf20db31fc5caf51f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:08:51 GMT
ADD file:ad62fb7e744226b84b9b87b22c6b1e797cb2a179f4f2c7295e0db14b95dcd84a in / 
# Tue, 12 Mar 2024 01:08:54 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:30:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:32:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9c2efbfef38bc6f28418aabddc7ba24be7bed3ebbd2673ebc8db7533e9ae8c47`  
		Last Modified: Tue, 12 Mar 2024 01:11:24 GMT  
		Size: 49.7 MB (49682014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ab338dc4eeec296303efc67a955dedb7028ccf69f05896a788076dbc0a4108`  
		Last Modified: Tue, 12 Mar 2024 01:41:00 GMT  
		Size: 24.7 MB (24700091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca4553b75aacf6fefe0df7808ade0293c53b5a2b5926e00353a53712d08926`  
		Last Modified: Tue, 12 Mar 2024 01:42:04 GMT  
		Size: 66.6 MB (66645885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d427ec1cfd26f5cc4329caa047c62c3bb939f1292ecb240305394e82bd104814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145912110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fc99ad2c6ad7bb89fafd327c80e89d4ec8fe3551f22e538f376ecc0366f941`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:02:33 GMT
ADD file:5d186ec2d875f4307a34d264914243316106515ef9072abb7cf5e80c252da588 in / 
# Tue, 12 Mar 2024 01:02:36 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:21:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec6259c8a823fea482e8e351d24e5f493bd9f11e76074191518e50ac63335314`  
		Last Modified: Tue, 12 Mar 2024 01:22:34 GMT  
		Size: 50.9 MB (50889351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d95670fd7000d49d11835682e227fc4e48c87caf6a3e9e49895a14def51b2b0`  
		Last Modified: Tue, 12 Mar 2024 02:49:09 GMT  
		Size: 26.5 MB (26533843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87389e1f052bd2d528d17fbca9aa5301a48fb6e559141c54ae9654424026ef2`  
		Last Modified: Tue, 12 Mar 2024 02:49:25 GMT  
		Size: 68.5 MB (68488916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
