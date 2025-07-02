## `buildpack-deps:plucky-curl`

```console
$ docker pull buildpack-deps@sha256:ea987a5f3c682f3bfb4c106a2ef11d215a6630dd76bb6fca1b9e336052738843
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:plucky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d379557793fe3c1185ac93e618b93373fa554f903524f6df26dadfc8a6cda7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49860933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1deb38c3fb2001a46fbf9737b6221a99a4edfd46efcf11baf8ef580a4a9347d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:0eaca8af04f137f2866a51aed71cb0d60a5a9483bab5dace0b797eb156bf8181 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:03c83456f76b8d3372f50dc65e1d9e37069a275d343928676618ba69375be326`  
		Last Modified: Fri, 20 Jun 2025 13:04:27 GMT  
		Size: 29.7 MB (29707855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c2978e07515c3b36a9e013517d5d0fdb1336f1e5f279fcc992ab204e90af30`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 20.2 MB (20153078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:456fc0cf55dc78df3432d1451bdac4095dabb8d169372d62237d22a3dff91fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe33173076dccbfc150241a12f8e8b5182da5b88487fb64a5dc92ed670f4bf2`

```dockerfile
```

-	Layers:
	-	`sha256:6c31b90aa5b52455bb723eedfb5c84db0d50fe1d273d7f63f0f228e50e7aff63`  
		Last Modified: Wed, 02 Jul 2025 04:20:40 GMT  
		Size: 2.6 MB (2613370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddc79b39fbaa9ba72cf5c633ffcf1c0df8e28b1e548d85ee318cb4cf4c91bcd`  
		Last Modified: Wed, 02 Jul 2025 04:20:41 GMT  
		Size: 7.0 KB (6968 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:34aa77893c8b28d9e56bc7a62e6fb06f9f0b12fff856e5f5ca2bf8b21e809d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44701235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09a154981d169289cf8d431070dddbc6e8d551fa914b041fe9da6f5ff702739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:05c7f1c69348eb60b37ad893b492f8522531d4dad90aaa492adef81ba0035320 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:68704530ec64c0182ba82980ddd77e33e790225a854ce8de6f68c61e47ebbd3c`  
		Last Modified: Wed, 02 Jul 2025 09:17:55 GMT  
		Size: 26.8 MB (26836572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bc203684c6220b7e514d46626edcb8d06be0ac56becb9c5edb31eed6845ccf`  
		Last Modified: Wed, 02 Jul 2025 10:23:17 GMT  
		Size: 17.9 MB (17864663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:404c7d5a0108467aa5b0241049db997acbe668cd6caf2d3e24e36cf764adaa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7ff48a1f44a84474d6b6cebb8fc8598d8687db784367e3f5eb0e0288ad17af`

```dockerfile
```

-	Layers:
	-	`sha256:a4b68021875a9b71c082a1cc1879c9dce71e83205c6da6de87234288821fb79f`  
		Last Modified: Wed, 02 Jul 2025 13:20:17 GMT  
		Size: 2.6 MB (2614869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c556328c03e08e0b1d551a173e858d734d490d279dbccc37b8a27763299712`  
		Last Modified: Wed, 02 Jul 2025 13:20:17 GMT  
		Size: 7.0 KB (7026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5faf6dd6a5853e496bb588e9d9265b8486b277af324dbceaa107b753c07d2ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47418746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4515bb46027d2719d143f7f77c3ae2970e4bf0e290c55d078dc132c191258f0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:c160ae00b04c55e9c06204f9fa1d1f23e1af34b08c3d6af3324d53d0c3814a99 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e128784ae52ff5870ff729372dfd45813d006ada9507e5214caaa8e538c0c3f1`  
		Last Modified: Fri, 20 Jun 2025 13:04:27 GMT  
		Size: 28.3 MB (28266501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca280cce07988859d22b1cdb8e3c8cd148dea5bf593f70da6322aea1e6ad9ad`  
		Last Modified: Wed, 02 Jul 2025 04:21:14 GMT  
		Size: 19.2 MB (19152245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fedc06d8c11c6352365028c2cee94a7201aa1b331afe45a20c463a85c097dee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378d5588c1c283f7b008e0bda0554d78c720f4b231caed0053d36af71692631f`

```dockerfile
```

-	Layers:
	-	`sha256:fb586b3326345af3f23ef96d5ca4984a4d50a7a3ddfb4bcd8c082e44ca523e76`  
		Last Modified: Wed, 02 Jul 2025 07:20:37 GMT  
		Size: 2.6 MB (2613627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2f2989c04f55d564a849745d0fe2bc33801cf3ffe2098d9d577be4d8217bd4`  
		Last Modified: Wed, 02 Jul 2025 07:20:38 GMT  
		Size: 7.0 KB (7047 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fc29eda7a31229cff402ac4163e75c19207b073029b18e189f22f363258601e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54513860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9465312b0badb5c65a61b628d2a33b07a5575929153de01df75f1f0242a6330`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:156f0cf6c35fd1c1fe3ffd678ee3fd4f3bb38e0658f83d3b4ba4b270a9107f06 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:95049f5204729939aa808035235c5611a6e0279acb7ac340628502d379700734`  
		Last Modified: Wed, 02 Jul 2025 01:16:09 GMT  
		Size: 32.9 MB (32933417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe1d54ea492fdfbc009de2454599cf62107d14a1bc590e81852da8df2c339dd`  
		Last Modified: Wed, 02 Jul 2025 03:13:07 GMT  
		Size: 21.6 MB (21580443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb7970eaf1ca746884d8f5b5e8948fc363c9a7e5fc320b6f9c173ac51c001030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddae80827657257e39e41100dfe180dc414aea34773d4b18c2f67065e891484`

```dockerfile
```

-	Layers:
	-	`sha256:7ccda2407f9d94ca1f7d60a7ce1ef63880fe25c48b3231296d163e7a3c50e9bf`  
		Last Modified: Wed, 02 Jul 2025 04:20:04 GMT  
		Size: 2.6 MB (2617188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a544e68eecc57532bff893e8bca4faa21731999470724154c744eee0b92c8302`  
		Last Modified: Wed, 02 Jul 2025 04:20:05 GMT  
		Size: 7.0 KB (7000 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:05831af20eacc8063929ae7dd1e5d617fd1e06f27b01118e4acca40df397e0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49629142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bfd76c98e6cd2d4af6bcb2295429be5014c1bba23180dc63d3f316722483be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:62c415a9a11ab2ec8b702ccc72f9307cddb1588a79dc480f7f025fcfe1adba9b in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c0d9a79efc696109b1bd1bfb8f38bbb8d7cab4cc93ee3b1b072d123dc24e0e65`  
		Last Modified: Wed, 02 Jul 2025 01:21:52 GMT  
		Size: 29.7 MB (29740535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018238233b1718e2f61df5fa70efff6c8b736f0fe6ce009ee89a3dd66f15cce6`  
		Last Modified: Wed, 02 Jul 2025 03:20:11 GMT  
		Size: 19.9 MB (19888607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1abc9970c41d6ada94b85afed1710ecb7e086b1553afb92e039324d964d6eb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0b61f81cf9a2d1b4589af654842f0a1619de49add5a468aff921078c89abef`

```dockerfile
```

-	Layers:
	-	`sha256:074c7c05cf5de0ad5ba9c6833bfc86e4b4f3f3d11bb927b05960ae2874234c1a`  
		Last Modified: Wed, 02 Jul 2025 04:20:09 GMT  
		Size: 2.6 MB (2606482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192ebce545710407bef2f77f38888830466c5ca101fa19e6eeae7d1c9e921e9a`  
		Last Modified: Wed, 02 Jul 2025 04:20:09 GMT  
		Size: 7.0 KB (6999 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:plucky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:63422c1863715784979aa72aac71492b936b8c7f6e1d8f93249f6e9997852824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50103558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c0c3d6323b3ed6ed728f2fd35706b47a696c54b47edc69efc38ed0bc740a2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Feb 2025 00:41:24 GMT
ARG RELEASE
# Wed, 12 Feb 2025 00:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Feb 2025 00:41:24 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 12 Feb 2025 00:41:24 GMT
ADD file:65c3a17ff08c38e485d0568f4f81d1da9836ed770a2520181c054658bb406a70 in / 
# Wed, 12 Feb 2025 00:41:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Feb 2025 00:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8d2faba794696654b8419836f3eb5351940dfc517452f2b22b94fd93a86787cd`  
		Last Modified: Wed, 02 Jul 2025 03:45:47 GMT  
		Size: 28.5 MB (28549841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0178a6e17bae3ec6d2f5a9dfedfcef603db4f51fd66d1823b0b0ee74433626`  
		Last Modified: Wed, 02 Jul 2025 04:13:48 GMT  
		Size: 21.6 MB (21553717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:plucky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:810715ceb0080f9adc7ac5a5d51fdbec5b79868fffe8f8c3b1e2c5f3bccceb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e7b6cb8a1e879404b40af58d3d8dd696d99577baddbb02d63d84530c89cfb4`

```dockerfile
```

-	Layers:
	-	`sha256:bb917ef7ae2540a8a4372cbf05888e7c5bafedc291960df06792848db1bf049d`  
		Last Modified: Wed, 02 Jul 2025 07:20:47 GMT  
		Size: 2.6 MB (2615398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3fdeb151f2b9d4e8094aac0b24fee02b37ee20e323e43cdaddaa6304d9548a4`  
		Last Modified: Wed, 02 Jul 2025 07:20:48 GMT  
		Size: 7.0 KB (6968 bytes)  
		MIME: application/vnd.in-toto+json
