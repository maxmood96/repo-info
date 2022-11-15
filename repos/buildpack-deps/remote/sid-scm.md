## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:2eb51066f6e0354f315d107550d327eb9a60c45e2491d11ea8d108e24f225908
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:646259e362bdc52baeba21d30d430f3113e8eb0d1ebe27e2417c02ab801c4f49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128765714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c946fdc6b55aa088aaa47ffc2f053b87bbe332ebf1bda912089091b10270692c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:41 GMT
ADD file:635f36e1a46e6c28b2a6ab0637cca9e47837c3547b17916d1dbb2595fbeb0821 in / 
# Tue, 25 Oct 2022 01:44:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:26:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:26:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:27:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d90f8b044e56f2589b41d1fe9b249b85bde027855731c6f512f0f9401c99e68d`  
		Last Modified: Tue, 25 Oct 2022 01:49:42 GMT  
		Size: 50.6 MB (50641226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e6bcc62372cb6ad18c098f8dda6e9c5b3707abc6e74f2dae7f8032bf929e4d`  
		Last Modified: Tue, 25 Oct 2022 09:49:51 GMT  
		Size: 9.1 MB (9101445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43887f8917a514e50f8816ba51125c208418ba87167de7d84979146bf6e06e`  
		Last Modified: Tue, 25 Oct 2022 09:49:51 GMT  
		Size: 11.2 MB (11180674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8959e14a7057e4471c7c2de00c4d7048aa8bcc79de9966ac8d3b137fb3cd114d`  
		Last Modified: Tue, 25 Oct 2022 09:50:09 GMT  
		Size: 57.8 MB (57842369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5ad2146195d1c03177c9159bfd3ef4af9355177c61289736f94b33bfa3e56c36
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126890346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4e656f8ce8da2c0c28db32b67c3164317a87ac860843caf50ef593a4b83f6b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:31 GMT
ADD file:08f8312faaa666d9d1d3cdf1e0ac577979317e8784c264b29b4d3399045d2adb in / 
# Tue, 15 Nov 2022 01:49:32 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:44:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 05:44:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:351340891f63641ac5516af46a2dfb6b370ea5971d604352dfe16a498646eb52`  
		Last Modified: Tue, 15 Nov 2022 01:54:51 GMT  
		Size: 49.3 MB (49284160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989d5b3af22bb23168efd5d127277e94392a88454e93916c8136bdbbbfdb6c07`  
		Last Modified: Tue, 15 Nov 2022 05:49:45 GMT  
		Size: 8.5 MB (8471398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae7d5b628dfd536fe95d650285c66873a6d0e49fe2d657c2e7317203d6f01c9`  
		Last Modified: Tue, 15 Nov 2022 05:49:45 GMT  
		Size: 11.0 MB (11015001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f1eeef7589c4ac448515182c2e3e5f648683d400190ea8e24edc498dfb4565`  
		Last Modified: Tue, 15 Nov 2022 05:50:07 GMT  
		Size: 58.1 MB (58119787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a561860f10082981df90fba5c6aa55981e40fecf260ba0080defd9528a567d1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119436030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dc4fcc10f9da808a545f44058400fff6da064925bd33d38593a6f1d0880044`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:36 GMT
ADD file:072a31b7cfe6ee4e4a8e0832259c68a602abda7e1a6682cdcb28eba7f0705383 in / 
# Tue, 25 Oct 2022 03:15:36 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:39:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 04:39:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9040ceaeef63642a4aa2653b1350e028be0db975aa9a23c7e441aaa7dc5a11a`  
		Last Modified: Tue, 25 Oct 2022 03:23:25 GMT  
		Size: 47.4 MB (47411564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13b466f981f25c2e1938044e245a8dca528315fa39d2e8a80709f09075fa43e`  
		Last Modified: Wed, 26 Oct 2022 05:13:18 GMT  
		Size: 8.2 MB (8204920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c85fa3e21298caffbfd811747b3acc6991bda175e560e8f8d9c2a8152d1eef`  
		Last Modified: Wed, 26 Oct 2022 05:13:19 GMT  
		Size: 10.5 MB (10458411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab70124f63ca402b0decd346eb68aadc1e78a44dca244108cb94bfbf22164a7`  
		Last Modified: Wed, 26 Oct 2022 05:13:41 GMT  
		Size: 53.4 MB (53361135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:674821747accebcb801ecf610ea740051b0106aceb51dd06264f3151642fbf82
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131004830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035bfb13602d95f0ddad83a8177e40df55de27ee9a9313203ebeb992e7fd145a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:54 GMT
ADD file:ba227e9990636bcf4ac74991aee2f89f076de2adf7a651c75b55b2dc145b5340 in / 
# Tue, 15 Nov 2022 01:41:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:39:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:39:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 05:39:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4831e9d6ed52920992a4dda63cbeb8f430d77a27377294be499a02b93fb1e3b`  
		Last Modified: Tue, 15 Nov 2022 01:46:00 GMT  
		Size: 50.4 MB (50371180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28af2f647d544013c2979fcc9bb3234c113dc9496fa976cc4a2fdf6d0622b2d5`  
		Last Modified: Tue, 15 Nov 2022 05:44:45 GMT  
		Size: 8.8 MB (8849884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70069958d3a3ba34e8ab2a47caf5d5f7b8a3be5ff9bb2a50385ea0deceeff91`  
		Last Modified: Tue, 15 Nov 2022 05:44:45 GMT  
		Size: 11.3 MB (11332918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ba53036e16acaf6e7813d2d4bee2d4d96501cdc5886dc90f6eeb8d38e8586b`  
		Last Modified: Tue, 15 Nov 2022 05:45:01 GMT  
		Size: 60.5 MB (60450848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:727397e319709783655de941e122470c8e5580ec96e62fbc532fce0166e10ea4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131761295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8113ad39378aabee953d3468724d3c1eb3ab375b04cb1942f60a917ec3e0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:23:38 GMT
ADD file:80dabb60a37b1d88f3750adb85c9e159d00b55293f70ad93512f94bd3cfd99bc in / 
# Tue, 25 Oct 2022 02:23:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:18:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 05:19:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:367799113badd94b9683087d6086436649a1fb7127698c42b0d730f5bbedcf86`  
		Last Modified: Tue, 25 Oct 2022 02:30:22 GMT  
		Size: 51.6 MB (51625321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564d2fccc59969c0b37e3bb8384bc6545a4cce125daa11c7e8b599ec0acac788`  
		Last Modified: Tue, 25 Oct 2022 05:30:00 GMT  
		Size: 9.3 MB (9282393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09be9213196e288bdcccf553107591d6fe4f04fccea4da55faea35dd79cfff15`  
		Last Modified: Tue, 25 Oct 2022 05:30:00 GMT  
		Size: 11.4 MB (11379737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cf8ff2ca1128a94c435416195c01bd46e7b32191a4a225527692f374d4e31e`  
		Last Modified: Tue, 25 Oct 2022 05:30:21 GMT  
		Size: 59.5 MB (59473844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:60050f35186dd9de5b2fe0e7d7ce77caba31b3e56aa6123d6d9b233013233cec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126961104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e38c8474f0427fce5ea0a747b91ddb446cf8afbcecb83ea4f683e851fae15a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:39:58 GMT
ADD file:da7998228f2661dd3490a7bee754b7aaed5cf07ebe582e97b32c3985ad0d283c in / 
# Tue, 25 Oct 2022 04:40:04 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:40:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:42:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2275c195d2a35a07739822efcd752aad4e9580392e4129bbac1f6cfe608ee1b`  
		Last Modified: Tue, 25 Oct 2022 04:48:12 GMT  
		Size: 50.9 MB (50901534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45280c218956111f5980d1b17036f589a29dca56a64f196bd8f0bfabf7b2966a`  
		Last Modified: Tue, 25 Oct 2022 09:55:12 GMT  
		Size: 8.5 MB (8465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cd0404c18893ceb6c37012f16133ba8b3c876fa90176ae85b3f9d94f25dafd`  
		Last Modified: Tue, 25 Oct 2022 09:55:12 GMT  
		Size: 10.9 MB (10933561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d962f72168bd74a6b23bbb9da6e07f630f0cb6fa527486ce2dd2d42508351ac`  
		Last Modified: Tue, 25 Oct 2022 09:56:01 GMT  
		Size: 56.7 MB (56660389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b752fc221f409b6cdab8b2847838e201ce3d7c95856590870fa67391d109b85c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139006341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da31aa88a012fc286c9e83bfe13f29518d53fa4afd44a2356ddc53ddc827f65`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:07 GMT
ADD file:6e9efd6bb77c835520332c88cb412f38f0d8573ec3347b090b77965e17131780 in / 
# Tue, 25 Oct 2022 03:14:10 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:17:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:17:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 06:17:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a3962f6ac5b86fa159789ea1e9241ecbb956b3223e8312f7d92d7fbb8bf5485`  
		Last Modified: Tue, 25 Oct 2022 03:20:03 GMT  
		Size: 54.7 MB (54704717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c5225e6c97e35e08afc065bed0fb4156a1727da9a3e12b4a611189682c919a`  
		Last Modified: Tue, 25 Oct 2022 06:50:49 GMT  
		Size: 9.7 MB (9684744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39fe7c3b495d9320ca99478bfddf7a3fa0412a37c56ca95a4cc891ceb738e62`  
		Last Modified: Tue, 25 Oct 2022 06:50:49 GMT  
		Size: 11.9 MB (11937807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9270b45cd7087efea37438ff9651d0078e51c8b476b199cfc26770079313e3`  
		Last Modified: Tue, 25 Oct 2022 06:51:17 GMT  
		Size: 62.7 MB (62679073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:80fe5d929462fbcb8fb502564ba1c94f3a1fb305aff0e201341b695be50f3fd5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122015209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3095c5914c0792da561d083de7026417fc5bec6e01a866d86b2f8f8d796eac27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:39:40 GMT
ADD file:cff1e1a432929527e9bb64bde53e2b614c941bd4631b7bd3634fdda8a7240455 in / 
# Wed, 05 Oct 2022 00:39:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 02:31:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc6da93595cf4d9d589de999765cc4f1efa5e0d8e23ca6dd8b73b18afdc8189`  
		Last Modified: Wed, 05 Oct 2022 00:57:59 GMT  
		Size: 48.9 MB (48857821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554ce58712f86101a4716baede25ee43c9c1fc550b39fb4b3e5fa1622fd3b00b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 8.4 MB (8388012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd132871253f925889ef836099addcf830644843a64a1529bddc510390846a9b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 10.8 MB (10750715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bfc76b3f6f1ba447e697e6e2190cf70e757458cce81446b79426ae4cccdb03`  
		Last Modified: Wed, 05 Oct 2022 03:33:00 GMT  
		Size: 54.0 MB (54018661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4030ace049550e7266628c08a838e0658e705dad4f0491dac2535698df26107b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125732836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d8337e348ae8954f28173bf3c8248b38c98bf8c64e684b15d1dc50a21089c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:54 GMT
ADD file:7dba2ae439c9f5da3fe962e867cee94eafc0b12a74939e13fdf987965ef8191c in / 
# Tue, 25 Oct 2022 01:14:57 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:32:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 02:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1430653806baea9ab2928a0d226c10ba8e7bf4b9b93398f9082ba16edfb2d4b8`  
		Last Modified: Tue, 25 Oct 2022 01:19:17 GMT  
		Size: 49.0 MB (49012977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa67452e329e71787509a1583923b8e1e83b22a2fb76e48111393a03205d4c20`  
		Last Modified: Tue, 25 Oct 2022 02:50:30 GMT  
		Size: 8.7 MB (8738304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7be163526b121ed701b3595b33b6d8755aba04a12b0fd801f9c899cbd3ebd0`  
		Last Modified: Tue, 25 Oct 2022 02:50:30 GMT  
		Size: 11.0 MB (11041665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ea6534b4c7c78beb071314cf02af39dc48f27dffa56b6182c538fc47d868d4`  
		Last Modified: Tue, 25 Oct 2022 02:50:45 GMT  
		Size: 56.9 MB (56939890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
