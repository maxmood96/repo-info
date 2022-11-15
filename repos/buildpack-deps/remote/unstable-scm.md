## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:938b2612b6b1b1991d8649c4af29ccfdf08ddce4724c128843633beb2810c6f5
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
$ docker pull buildpack-deps@sha256:d20398dd80bfd7c7f6815e3a56ab4cb0915fb11bd6b94d110bd77a6ea1323c36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131249101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fbcb734afc617780a7497dd1659b3fc41e11fe61877d879529757d70531066`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:42 GMT
ADD file:ace32e845b2ef519c79a725518e909bcbe50ecb496c1dfc8e96fba83ffaf685b in / 
# Tue, 15 Nov 2022 04:05:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 10:27:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 10:27:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 10:28:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6bf34ac41ed5383f401a5e77ae46b55249a145be0fe8eb1bf8f0e4f7febfb2a`  
		Last Modified: Tue, 15 Nov 2022 04:10:16 GMT  
		Size: 50.3 MB (50311341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f3b9f46f2031bd413417a1f8fa2105dc29dead8d7a2147b9f742ed2892b77e`  
		Last Modified: Tue, 15 Nov 2022 10:33:48 GMT  
		Size: 9.0 MB (9017772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e90be89ed4a456d300e722fcd8f6c47b8e993b6a5037babce8a1e9d84a98721`  
		Last Modified: Tue, 15 Nov 2022 10:33:48 GMT  
		Size: 11.4 MB (11367392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5880bffcaed8da26347aed9dd7a27663ec474ae55943017e4d3286e2bc4c51c`  
		Last Modified: Tue, 15 Nov 2022 10:34:06 GMT  
		Size: 60.6 MB (60552596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

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

### `buildpack-deps:unstable-scm` - linux; arm variant v7

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

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

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

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4b6f5353a01579f353a526f6e6828015f6c1aa45f0daa66d72a0d900dae623a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134572754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2274ab614898acccfe91701572c42606f056d23dda7e9ce82841144e33ebf1d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:42:30 GMT
ADD file:6c7cf2ddf77e13ddd1b27b3e2895b29bf27b8fd6d38de6f5fa7330138f69523b in / 
# Tue, 15 Nov 2022 01:42:31 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 07:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 07:07:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 07:07:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d85d48acbb26d22f92c31ab4d483ab5c9fc0a7db5f67806b2c05a4460060ee4`  
		Last Modified: Tue, 15 Nov 2022 01:48:49 GMT  
		Size: 51.4 MB (51364090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342a208cb77d0844c504e83c807857939a67fb80f38ffb6fb74e683902d17e74`  
		Last Modified: Tue, 15 Nov 2022 07:13:55 GMT  
		Size: 9.2 MB (9195422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e99437fd05453ca2e9063e277126421e73474415f3eaf15d08239e2c8b01f8f`  
		Last Modified: Tue, 15 Nov 2022 07:13:55 GMT  
		Size: 11.6 MB (11570905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfee5dd4dd1d34c745442f7614e178d2f82d1a625b89d8e33c5e23d0d293dad`  
		Last Modified: Tue, 15 Nov 2022 07:14:14 GMT  
		Size: 62.4 MB (62442337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

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

### `buildpack-deps:unstable-scm` - linux; ppc64le

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

### `buildpack-deps:unstable-scm` - linux; riscv64

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

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a59f91f0d062a13a63edac5560cba259fd386d0dbbe835d0eecb5505345a749b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125657998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7604b5df7bdc891e8e0032a0e62aedb2d26be86a5bdc87cb752f4f868f6b577`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:43:11 GMT
ADD file:47253af7a4fe925d592c8b6d41b8dff6122bbdd083ebe6ff091bd90271f78b19 in / 
# Tue, 15 Nov 2022 01:43:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 06:27:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 06:27:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 06:28:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba49eb7f21a2367672851b25b6c120e1a153fdf9884b643d9b288f026a56ddcb`  
		Last Modified: Tue, 15 Nov 2022 01:47:50 GMT  
		Size: 48.7 MB (48716895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a177a53296ae0f27e3066a0176da64ce91aad46f8e4ea7f8c96c9311b9a66820`  
		Last Modified: Tue, 15 Nov 2022 06:36:52 GMT  
		Size: 8.7 MB (8651091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd00d59dc2ed724777bd708f1d6bc0056f53a561c1d8223416db44c865f6d040`  
		Last Modified: Tue, 15 Nov 2022 06:36:52 GMT  
		Size: 11.2 MB (11234625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb14cd11b1167dfbd5954a6d0fd719eb78ee07691ee7736b26a1ceb87584f414`  
		Last Modified: Tue, 15 Nov 2022 06:37:08 GMT  
		Size: 57.1 MB (57055387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
