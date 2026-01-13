## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:bd062d8f828b39b0545334d50b6a68393a78bac8bf2c8f0b7b42b31a38894a49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:63f8cc622484d4919c8efa1a709873c3a4b7efa45c49397b808982c998314b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142680809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b00b7c6f2392505f8719a98ff2f6ef8bd616ae75ef7033bfcb8442dcccb6a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:021dadb2adf7f142f52a3b87e9527c6ae5410bbfc99709f18919770f7bcce486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12102b232575087daec3456b81415b1010576ac0e45300cd0a5421d63f6121a8`

```dockerfile
```

-	Layers:
	-	`sha256:e6766b0f7138d64adf4ff5cb6023cbcf5e681d5c7c60f094212fbdcf9052261a`  
		Last Modified: Tue, 30 Dec 2025 04:25:42 GMT  
		Size: 7.8 MB (7767098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:facd45e8947218a737261140ebddca5599bdc71412a292dae28b67ce6a7c77b5`  
		Last Modified: Tue, 30 Dec 2025 04:25:43 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4f94fb84abbcb7492d83a1bf75a55dc3f1ad91045403279a2f521b485ff8674c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137120764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6d7031a6a1c941930b9acf565d9cdddff9bac8b0ab96480f0e1203a8107956`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:08:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16d4329ceaa8dc305221873389c356e4c5bf3cdb5b245a79ff75a1b1806f3778`  
		Last Modified: Tue, 13 Jan 2026 00:42:16 GMT  
		Size: 47.4 MB (47448362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ac90147d1f1c4bc0ab2c1c245fb4105c9ad56d7e5e75726e8ec474c79f05f`  
		Last Modified: Tue, 13 Jan 2026 02:30:05 GMT  
		Size: 24.4 MB (24353866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b0fe9087175027e9a76a41e2c394603c9345a19f6296b58e7044e930aafb08`  
		Last Modified: Tue, 13 Jan 2026 04:08:45 GMT  
		Size: 65.3 MB (65318536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1f0042994ebfb4b7e41112267f73133bc53bdef6f48966443b56f3d59853c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ecde136f92fd4dfbfa668080745ae46cdf2f7da561b5bf380eb41ac738a6cc`

```dockerfile
```

-	Layers:
	-	`sha256:f2f3e5f5271e89d3c02cadb19bdcf21601238fdacb8d74b67b365622925dcab2`  
		Last Modified: Tue, 13 Jan 2026 05:24:17 GMT  
		Size: 7.8 MB (7769175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26fec3f9028f7ae6c338b5e7e41ffac7e169ed25207e80078a4ba481bb764cae`  
		Last Modified: Tue, 13 Jan 2026 05:24:18 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:40fba909d3b863736126156942f75dc81e45ea61cb25216c7eb34dd85bfa6184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132057869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e1c09e0d485be2e468d9684df5c008a80bc46e2c56405b40f475da8a3d64ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f4296a8ece8abd5a409e5fbdb0cf93258815e4fec9dc768c39a63faf3c16052`  
		Last Modified: Tue, 13 Jan 2026 01:18:45 GMT  
		Size: 45.7 MB (45717820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8e700e2f18987ab9f97abcd0497d5dfc1706a8c057e685438ce3b71d8067c0`  
		Last Modified: Tue, 13 Jan 2026 02:59:15 GMT  
		Size: 23.6 MB (23626665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6f5dfbcc297b2e354e856be84c591ec9f96e89fd8401a4d485596c43b8ed8`  
		Last Modified: Tue, 13 Jan 2026 04:26:15 GMT  
		Size: 62.7 MB (62713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c1b538054f3ac5e83c03d6cc63616799d27a39d289f6cc3478bacf3b49ec2c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f2cb95dce8c71046b397ce0e34d9917a85860edde27498db7bf1991ee8178`

```dockerfile
```

-	Layers:
	-	`sha256:79826f10bbce0ed948d9202da82edb7fa8df4677c56e0c3b38ecace5216015e1`  
		Last Modified: Tue, 13 Jan 2026 05:24:25 GMT  
		Size: 7.8 MB (7768644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db456bca7b291f1bfc89fec724f3f9a3461e4b59ab6ae3ef888a315c7283997b`  
		Last Modified: Tue, 13 Jan 2026 05:24:26 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8119ab350578420190116327ce38e9226fed560a819b506976d4916c4361e74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142255022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e276557c308bf61abcfc36346ee60d4addef22f06f34c33aee4f54a5759ab9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07bd2f4efc761637e2a36f2786027888067b46db13bb374246ba54834b251371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937eb4e9195af3fc59a307e4faaba355a986702a5b78ec703e955c1363cc9a52`

```dockerfile
```

-	Layers:
	-	`sha256:239e86fac866c26929a9222835aea5e9d8d3f3cb912d715f30daeb41398f01ee`  
		Last Modified: Tue, 30 Dec 2025 04:25:43 GMT  
		Size: 7.8 MB (7774773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ad4db7e7e58aba8a75a580c9daff8586372d78e7d220f430868c4128b3f265`  
		Last Modified: Tue, 30 Dec 2025 04:25:44 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eb83bd297d5d536ee27b0deacfaa8f4334fc07df616cf7dbe9f8c4ca83191897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147380358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076ac1fc7e734a671d65a5519f0216a2d1a9567ac3230b9a6014315a62b8d490`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:47 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad78e3f6c783e58b723e0e1c78c005c2b612d1657c3a40830f5d7d97f9d85c`  
		Last Modified: Tue, 13 Jan 2026 03:04:58 GMT  
		Size: 69.8 MB (69803208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6fe88ccf372b9243fafc249c488f9a0329345ef6bcf306b5daeb3b9e391987fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7771821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e736995ab9c4d9c7a0ec0da11ecc0852e472df9fdc7b3c487ebe8a12918e68`

```dockerfile
```

-	Layers:
	-	`sha256:90ea1fde2b6d32a80f5998c27b93d058f06296385ec6722ac90891418cd1c16d`  
		Last Modified: Tue, 13 Jan 2026 05:24:47 GMT  
		Size: 7.8 MB (7764271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db59c0e625f56778af94e83e95d8fd086923d8c2f9dd44368776b9e51de6edfd`  
		Last Modified: Tue, 13 Jan 2026 05:24:48 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:57b78503a128eab88ffafcacdfea874711f665346aa9f3a27be8a02c53ecaa76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153136310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aab931c9f8f7cab2e208d53a5402a44c33c5581cefcdcd46ba891b57d1c08d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd44afe623a2af1e017b0756e314b5b0882afdc551ddbb8ab4a0e0d718eb8f20`  
		Last Modified: Tue, 30 Dec 2025 03:19:14 GMT  
		Size: 27.0 MB (26996817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464b5ef37e07d88bfdddc49e0cb0b76c46c151a0ee23e6a2bd75bd6783f9790`  
		Last Modified: Tue, 30 Dec 2025 08:23:35 GMT  
		Size: 73.0 MB (73031008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:91d81fca5e6c748002000a619bf74adb52e958764c3c6f71a567585a73e8af92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4069a58fb1a0b5869260344405479b130ca91ac90f5a24e7ddf5db615d11db55`

```dockerfile
```

-	Layers:
	-	`sha256:8e2fb6cda59c55f063358b415517bbff8afa47db03b6af15bb6ed5b65628b658`  
		Last Modified: Tue, 30 Dec 2025 11:20:48 GMT  
		Size: 7.8 MB (7774221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1359f5f7767a35fe07f597baf1ef10e3ce7654d9ae7b45ae33320516456727d3`  
		Last Modified: Tue, 30 Dec 2025 11:20:49 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:47f0d7bf4589499bf86ae079371541221d2a24c51a3e91a8f9264d0d2ab97319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139385592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05506de782b06c88c810945b6b4226d362d98d59bc47d8e5b414983cac14730`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 12:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f7933c6ef71f06a1f0f33145f157cbfe6df70a0a3efc496c514e6bf0f3c52`  
		Last Modified: Wed, 31 Dec 2025 10:17:43 GMT  
		Size: 25.0 MB (24953863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e727fba04feac92f30181733d92a9aab095f91af402efca58918b26fc389037e`  
		Last Modified: Thu, 01 Jan 2026 12:46:54 GMT  
		Size: 66.7 MB (66660576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd2dbde918ebc895841fc4434fa07a707f13b9827f60e711f81ea8f9a40b5c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5b684b68309cc1b7a987d1d3029a7ec75401629fef4eef065cb8ad28b1c621`

```dockerfile
```

-	Layers:
	-	`sha256:a438c4d29c04cb19c729472faf5d7c3ca350310f9ae7ffc14da9402993db8ec1`  
		Last Modified: Thu, 01 Jan 2026 14:20:43 GMT  
		Size: 7.8 MB (7756934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cb7e8aa876eab1b676c86c992bb4bcb023509797d46fa4c30ac11d06561536`  
		Last Modified: Thu, 01 Jan 2026 14:20:44 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:53daade8f1cbc4a6574a02e8981d4c7bdb34ac737f1433ca924f2db975466fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144774274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc185d85169425b1a7ca1e53446bb851357271ca572ba53d721266d2f752b2cd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629a9411869af8d59bfb1073c3573138af1f96d808896b3f2fd14cf62fca6dba`  
		Last Modified: Tue, 13 Jan 2026 02:11:34 GMT  
		Size: 26.8 MB (26792892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54b33211ee85001fc045dcc86b026876894b17d1d6f873a415014f68cb0c9f`  
		Last Modified: Tue, 13 Jan 2026 03:16:21 GMT  
		Size: 68.6 MB (68632678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1d742c91dd1041b258636e4ca88422077d42623bcf93e1be017af95baa4e328f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7776627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0605af8a5f07e4dc60a175fd1cf32ca825e2c06789f4f8d303ec0b1a3ade05e6`

```dockerfile
```

-	Layers:
	-	`sha256:7e7c760003a53c37739e20965a2a49d92e4514abfec6a3cd138ae6eb83f8a61a`  
		Last Modified: Tue, 13 Jan 2026 05:25:06 GMT  
		Size: 7.8 MB (7769050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407257e03197cd4f72111790fd83f3c5f34e4b4d5901b1c47e806a3448e43790`  
		Last Modified: Tue, 13 Jan 2026 05:25:06 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
