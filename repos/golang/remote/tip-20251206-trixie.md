## `golang:tip-20251206-trixie`

```console
$ docker pull golang@sha256:7e3301c3f16110a0e04b6dbefa3338174c901a0763fe979e1ea46ce6bc40f1e9
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

### `golang:tip-20251206-trixie` - linux; amd64

```console
$ docker pull golang@sha256:e1a47954b2bca5ed5a1ecce79e25358c4d681c271155531523e02d675e386ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339178518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc7d41502dd0e8018aff07dfab2a05af29d7f281bc8e20a804810856064aff4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 20:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:38:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:38:42 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:38:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:38:42 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:38:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:38:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae668646f447b181fe300ae6756351b6167aa2578be449b167ba79ed4926798`  
		Last Modified: Tue, 18 Nov 2025 05:11:30 GMT  
		Size: 25.6 MB (25613858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e6e687b6ce78177a4cac678dd533c8e72b97469f030783b6bb491f681fd4c`  
		Last Modified: Tue, 18 Nov 2025 06:39:26 GMT  
		Size: 67.8 MB (67779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8327b2b8dc8eb9c35d68d2d50b9a58684f0413afad8a137586067ea729efbc`  
		Last Modified: Mon, 08 Dec 2025 20:39:30 GMT  
		Size: 102.1 MB (102108911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949364a36b81a9ad117004649aaa40ca173e0cb5059f62e3ed14f9d09d82b4b7`  
		Last Modified: Mon, 08 Dec 2025 20:07:50 GMT  
		Size: 94.4 MB (94386989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decfab50d2425a8b87d80d1d3c70f13bf6dbacb77e9151015a9f5de02c29bada`  
		Last Modified: Mon, 08 Dec 2025 20:39:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251206-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f4baae8c6de278eec3883ca568049ab1352af12de3dfd7e088d69cf009af1bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec2ea8538ed0a381864b2053b043b2ee72f75429e1df2add328bf161159477c`

```dockerfile
```

-	Layers:
	-	`sha256:529858491450b847fdd900e5aae535e89d783aa53def1a55451b1a545a1b5829`  
		Last Modified: Mon, 08 Dec 2025 21:23:29 GMT  
		Size: 10.8 MB (10784508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1cac8d62157591ac1e5f8120a35789425b54ab3bca36553d4c340a3674fcf25`  
		Last Modified: Mon, 08 Dec 2025 21:23:30 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251206-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:80367f59938784b080441b3286606059167a38344025fdb08e6dc71800e8e131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295257228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac4b44e8aa3f24e9314c07557317ae60aa6226a48dc8b35833ee533cbc771de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 20:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:19:49 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:19:49 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:19:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:19:49 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:19:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:19:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcec123a6a2e24d64f8dd8d3ff01f16ba0839656e71d971698d0e8151a28a21`  
		Last Modified: Tue, 18 Nov 2025 01:14:26 GMT  
		Size: 45.7 MB (45718279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebfeb92d3792e2087594f2ee9ee695fe97cc51ccaf846f755d71e0b58f7f78c`  
		Last Modified: Tue, 18 Nov 2025 04:00:39 GMT  
		Size: 23.6 MB (23620000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c45847805af09aa76d6ba7f34b42945f6767f5c3049e5027681335f35a18d5`  
		Last Modified: Tue, 18 Nov 2025 05:29:07 GMT  
		Size: 62.7 MB (62713438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e74497eb8cdf16a7871cf72d5c68a8558af50eaad7c4a5decdd68ca7ffb2329`  
		Last Modified: Mon, 08 Dec 2025 20:20:46 GMT  
		Size: 72.8 MB (72754080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fa0b6c68e96e333f64da015866d36d22ecf4302421d4e561b2c28faa5b8bbd`  
		Last Modified: Mon, 08 Dec 2025 20:20:43 GMT  
		Size: 90.5 MB (90451274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2fa04a9b8f23021f2a046ea059405e06968fda80ed20657e49af0be67c3c00`  
		Last Modified: Mon, 08 Dec 2025 20:20:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251206-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:3a8db55fe8af18a9491a9f9f2de25efe25371a557e73d8b21994e7f9da9bf446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7938ee2e8f0e18458e53e7e99bbff5baaefba11c58fa7a733b002fe537d23b84`

```dockerfile
```

-	Layers:
	-	`sha256:7cef21eba6f73bb305263ee8479ad47e871e9f448eac177a32aaba42241249ab`  
		Last Modified: Mon, 08 Dec 2025 21:23:38 GMT  
		Size: 10.6 MB (10580395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8285757167f5d2de3d415a72487a8cdcbdb63157689a43272546a653c8473a71`  
		Last Modified: Mon, 08 Dec 2025 21:23:39 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251206-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:32836709610782d22ef4308aecc8ba47ac45cf2fcb0e60d2627306bfec835857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (329965181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bddcb7b8479c15c9e8d64d741a7e910f28b4865164dc34a9f2b88601b70cc9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 20:07:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:09:10 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:09:10 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:09:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:09:10 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:09:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:09:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0c06b0c54bbeafcda8fa12eeb466e06ac3010b738faaf5c10b8bf332488f57`  
		Last Modified: Mon, 08 Dec 2025 20:09:52 GMT  
		Size: 98.3 MB (98254013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2568df0f74d7435ccc404d81d30d0f293c9c2980ac0f029d1100be5d1622d029`  
		Last Modified: Mon, 08 Dec 2025 20:09:47 GMT  
		Size: 89.5 MB (89455005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9c210458451ad0edfc9749b4f8ca0bef73c5f575ba7f1ae74691eef3c0c734`  
		Last Modified: Mon, 08 Dec 2025 20:09:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251206-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ef86593caf0c4c520037124a99c737b2011af4940d129a545d8ca7bc33ef2f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad391d6c65df640509586f6cb48c063eeaf35b1673d063317212bbae92f454ea`

```dockerfile
```

-	Layers:
	-	`sha256:a9e75b14064fc908a98c559be69c21dcff19bfbdc7a76c616b2853854bd2e696`  
		Last Modified: Mon, 08 Dec 2025 21:25:00 GMT  
		Size: 10.9 MB (10904963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:066fc19c134e7226d5db81ae9d850e482e61cc84c8136d428a4182babe2bb3ec`  
		Last Modified: Mon, 08 Dec 2025 21:25:02 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251206-trixie` - linux; 386

```console
$ docker pull golang@sha256:79b7232cadb57c33c19b8ea553a84aec68e739977048bc17e7257c42f60554b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340214222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac60648eafe25c99876d849935778ed291f44df3ec558396f48a3192cf6d49`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:11:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 20:06:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:07:45 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:07:45 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:07:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:07:45 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:07:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:07:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf2a49c122745d1757b9ecb1c9b1d8252491e66b62d1c279080155aaa530a615`  
		Last Modified: Tue, 18 Nov 2025 01:13:10 GMT  
		Size: 50.8 MB (50801744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cfb736286179e6858e8b04a47a815f4071567b3b6f8b36ca52b15e872e6cea`  
		Last Modified: Tue, 18 Nov 2025 02:57:24 GMT  
		Size: 26.8 MB (26776415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c892592b339e9b2ca91d682c607a5e915b21a67ae25c1c71d1f3ef8ea35c2f`  
		Last Modified: Tue, 18 Nov 2025 04:11:31 GMT  
		Size: 69.8 MB (69803141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ac5e381f0e5df52c82d6bcedb490ee9c47d185713d244da5d4bc6952ef287a`  
		Last Modified: Mon, 08 Dec 2025 20:08:52 GMT  
		Size: 100.6 MB (100555245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2714e644cc32cbf0646554d2bf879368eb0872b6982a8a69088b6c556adfd2f1`  
		Last Modified: Mon, 08 Dec 2025 20:08:50 GMT  
		Size: 92.3 MB (92277519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a06828390a66642168d383ecb49ba941705f69b0df6931500cb93e82da8dc9`  
		Last Modified: Mon, 08 Dec 2025 20:08:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251206-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:a97f89c8a7dd60d590bfe2767a227afa0f5d1587388838903162aa5fe1f8bf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa366d1cae0a5c27d6a906091528f513ea5cbb81999eb787907d63e8876d95fe`

```dockerfile
```

-	Layers:
	-	`sha256:9e4aa8baa9ab587e171bd42e8eaf8825fb2e6f941b9cdd1cfd938e26a987a4fe`  
		Last Modified: Mon, 08 Dec 2025 21:25:10 GMT  
		Size: 10.8 MB (10755772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4f6672d7c53aa2b7121c1f5cf0ce2df0ed4cbed5175780512e947103f6c0f9`  
		Last Modified: Mon, 08 Dec 2025 21:25:11 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251206-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:ed7fa89754d3cd16dc98bdafc367a6f33fcfd6c9fae05563d0d8edb6c1de4885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336939156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a30423a01a43acd7a49581d7c3ffc20e5a3da474d167e0d3d95223dd02071de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 20:23:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:23:03 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:23:03 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:23:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:23:03 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:23:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:23:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859b52534a1e3522c593c1835bd1bee34ff20a865f32f140257d45048a18099`  
		Last Modified: Tue, 18 Nov 2025 04:09:23 GMT  
		Size: 27.0 MB (26996919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b1a22ff6e7093fdd1dd2648adedf5202ef1304de7d17f711c19601d3a80e`  
		Last Modified: Tue, 18 Nov 2025 06:54:27 GMT  
		Size: 73.0 MB (73021903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdd5a669f8beb96d309458fb81310aa7be4fe1105c4dbdd4ea4d48c62862bc1`  
		Last Modified: Mon, 08 Dec 2025 20:25:35 GMT  
		Size: 92.8 MB (92815363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7f78d7b3fff51dbf03b6fcb119f6f6c12d036239dbfd1e84cb159ba6461fe1`  
		Last Modified: Mon, 08 Dec 2025 20:25:32 GMT  
		Size: 91.0 MB (90996328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b785097b43b631c1f6935f92a6fd283e25c0e6acca1b146701d706ce63efd9`  
		Last Modified: Mon, 08 Dec 2025 20:25:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251206-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2327de737ecc51acf84195371a64141b0796f1346e754981bf096116a9a94122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e385b5c874bc657e86377c3dfb86f78a0ae594ba5e35c7c06b85e96e56af5af6`

```dockerfile
```

-	Layers:
	-	`sha256:89cf1dae0fc81355e8771e868014269670aff9e542915d7336c677963a6c6210`  
		Last Modified: Mon, 08 Dec 2025 21:25:19 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af2fb5d1213c6a399bdbd8a7ec1c72880bf7b8aa676e2adff290c0aa3947238`  
		Last Modified: Mon, 08 Dec 2025 21:25:20 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251206-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:b905545ac8b37bec605caa5e808c84d3f01069754ee3b256c366c3d10c50d545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362622571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f96f04b012d10ab4b7b8cfa08d8cdaab95b514af8049e17685335f6fed28594d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 22:09:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 21:37:12 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 21:37:12 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 21:37:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 21:37:12 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 21:37:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 21:37:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8d0f17fde453d9cf0b99bedd3dfac5dd06317d587dd69852c68ca1441ce0e8`  
		Last Modified: Sat, 22 Nov 2025 22:24:09 GMT  
		Size: 131.6 MB (131594403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305a0d5488487114fae9eff5e7d2b05535888e36450abce33d63c253df6ef6b0`  
		Last Modified: Mon, 08 Dec 2025 21:44:31 GMT  
		Size: 91.6 MB (91642118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07da303d0d950638e957a56a3b39814c9e55ac2892839419d8a9f6f0ae0d97c0`  
		Last Modified: Mon, 08 Dec 2025 21:44:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251206-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:55e3207b77dcbcfdf284161b1f94d7f3fef10c06ba8104a5801141501553d44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de13ea6d17cf0c1f42f4ccfb52cf46dea3b5ce1efdf07f1401dc1a22e58e6a83`

```dockerfile
```

-	Layers:
	-	`sha256:ac8085cfbc7f39ef016fe7e681ddfda381a50a4d9fe4f97fddec307512669479`  
		Last Modified: Tue, 09 Dec 2025 00:24:17 GMT  
		Size: 10.9 MB (10854127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8009f3896f20c8579d1ab4c4971b01648ef5ac5e9cfdc24e4138458c0be5e0e8`  
		Last Modified: Tue, 09 Dec 2025 00:24:18 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251206-trixie` - linux; s390x

```console
$ docker pull golang@sha256:cf2a606831ad84732dbbf4b3f1fa726400905db761007e53efafa730b3156f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.2 MB (314229497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ed064829a2aea54a5025a5c895dc479448736bf56b449923f7769e8889b856`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 20:10:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:22 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:10:22 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:10:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:22 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:10:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:10:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811fd500c593f696ff4afefd96c823d7f8788d50f510057207bfc40b4a405ca`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 26.8 MB (26786539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4530c943529730620c01f6bab681e114e8a52bebc697a9164bab0bee08dc992`  
		Last Modified: Tue, 18 Nov 2025 05:58:03 GMT  
		Size: 68.6 MB (68624056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51acb2dface84e0e0eb6392de5a8c292dbfca225ce36b716088967ba9c237347`  
		Last Modified: Mon, 08 Dec 2025 20:11:27 GMT  
		Size: 75.9 MB (75919603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d45aee96e59637b1f14b3eb6f81f4f4c64edb3653263ca9a0c489bd88115cb`  
		Last Modified: Mon, 08 Dec 2025 20:11:07 GMT  
		Size: 93.6 MB (93553127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0a97ada81fd2009cb6cfad8f325c2cd5468c75cc93be28cc3bd27ea18bd4df`  
		Last Modified: Mon, 08 Dec 2025 20:11:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251206-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b54714e0f70e769edbcb16c62f2ebbe9dca41a82631df3ed7ae70b6b0b3f7cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b7f00870c6361b35b9ee6d392ae58852d3cc25b6a7f375ba15a012fbad656a`

```dockerfile
```

-	Layers:
	-	`sha256:c4eb3f12f07acceeadef36c1459dde30182b8ec21cadc9760d4bbda2981e01aa`  
		Last Modified: Mon, 08 Dec 2025 21:25:29 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b87289b0feed5bf7911e1754718ad8c287f26652b94b613304db312d21f61ef`  
		Last Modified: Mon, 08 Dec 2025 21:25:30 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
