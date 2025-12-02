## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:24c69e5568ff3801e1f4cb8f9c442cd1ad2f9f6a9130f425b51b4d57b1fef434
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:ba58be6b89d2cb983d0c9bb196b1cabf6bdd10281621be28521782df73b0f17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323430252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1081f5d53e568ae8c5b42d21851f54069ad1af509e63548d9e7b396833275ca0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:09:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:11:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 18:11:38 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 18:11:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:11:38 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 18:11:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 18:11:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b2eece9b24f617524f986db4dd04f977e3e7d6fe15a9088a584147bc6ba05`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 64.4 MB (64396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5822821bad668d80200800175e22510898261521ef564061b4fe3e0872d50efd`  
		Last Modified: Tue, 02 Dec 2025 18:12:19 GMT  
		Size: 92.4 MB (92410490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da39c78191c9be13a8adf6d46ca789532fb58292a09979c1057608fd7cf7b31`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 94.1 MB (94113232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568b438aecbbcc9b57dda85621425511d18cac8cce14c5eabf65cd52996eb0b4`  
		Last Modified: Tue, 02 Dec 2025 18:12:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:dae634cf4f31afcc26a1697aa79a8a574d51485074dc5f6da658c6bf28a9c836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79eda0159ef07c39b8fb658487353b36d36b5486d2bfa9e644e7138e1d503091`

```dockerfile
```

-	Layers:
	-	`sha256:ef5e4b5a1b3056ae41347ee2ea88d0fde06041e58eb126209331e5608d0acc50`  
		Last Modified: Tue, 02 Dec 2025 18:24:46 GMT  
		Size: 10.5 MB (10496390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9ef8c1778bedb1cea0711caf9189b659ae5e20a6cd710b1347629283788862`  
		Last Modified: Tue, 02 Dec 2025 18:24:47 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:2d0881e80dcecb5b923371ec1b3d1238e4e2e0746561c8393d5a1df64c8ed8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282257956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66223fa2ea53b9f7774240388cc6416d6151363f10c619c80fa9aa08913ec99f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:56:20 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:56:20 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:56:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:56:20 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:56:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:56:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b6eb0fb27a6d99b6b7a2a32ab126d30b16ebd113a3a3e174d37a032cde9bd1`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 59.7 MB (59652137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9cf1f0038424663910af2134cc33d1d6a7c69afcbaeb256b17df63bc9b3f41`  
		Last Modified: Tue, 02 Dec 2025 17:57:21 GMT  
		Size: 66.3 MB (66276505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb1234642b8e59fff163165b022247bc43b3cbce7229072851dbefb3454b51c`  
		Last Modified: Mon, 01 Dec 2025 23:59:32 GMT  
		Size: 90.2 MB (90198345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494993d2dbca9192837a5a62adb84e9cf36b2d2efae8d4d097888997e6bf7c66`  
		Last Modified: Tue, 02 Dec 2025 17:57:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1a7e9b538e4647b483465ab892936e44312f873e1f80c61c0e0bb3f3808ecf2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c83b361ceff76eaa1bc293baa06821a99b4865f8002395c4a2a2a7327c9822`

```dockerfile
```

-	Layers:
	-	`sha256:115b9c5b5d83a34ad7a63bc85038578fd7ddb4f94946f98b463fc5c911fef186`  
		Last Modified: Tue, 02 Dec 2025 18:15:14 GMT  
		Size: 10.3 MB (10303086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ad8c2d393ac986d3adb2b415beae208175054aa3fc04d154c4d2b4807cac3b`  
		Last Modified: Tue, 02 Dec 2025 18:15:15 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:13cc31e2030e553d4cc100727c6ebfa2fed02c8703c2dbeb548feffdffbd0703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312031343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d08df7ba68a4473fe23df6d366cf3f1607e3b88fcb7a0d52bf7fcbb44a4fd6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:55:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:55:46 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:55:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:55:46 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:55:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:55:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd5a6bb373c8d41e938fe0238c1be74cbdccceed786031a1eec79a9107e40e2`  
		Last Modified: Tue, 02 Dec 2025 17:56:35 GMT  
		Size: 86.5 MB (86490907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5ad4011b8323fe08610380aae994bb765f6965dfc1e0886815c89502e86415`  
		Last Modified: Mon, 01 Dec 2025 23:57:41 GMT  
		Size: 89.2 MB (89211407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d95f20b4b4618d3d3a65a5566dbc1a398b0631638e7e5ce5a2bb59779001e2`  
		Last Modified: Tue, 02 Dec 2025 17:56:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2158b016f75a10c4d5924379a89419e0293587e2a7dfe144103cab30604a74d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5e611b068b213fdd141231e10063f6c2c9b372b2542b171891f4914d29f4ac`

```dockerfile
```

-	Layers:
	-	`sha256:63b4d67c22d9b9c780d7d85437e131bae2282421ab51e8f5eb9dafc112213226`  
		Last Modified: Tue, 02 Dec 2025 18:15:23 GMT  
		Size: 10.5 MB (10524214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9add83c7bf9e42a40081cf4639c762bf3b0c02405ffd0778551eb7f67fabb85e`  
		Last Modified: Tue, 02 Dec 2025 18:15:24 GMT  
		Size: 28.5 KB (28517 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:101027b44e79d49900c7da063c2d8e40939b3e0a5872ed88dd682f2d819cbb26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322433616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087a79baa13556cd4b554f80140cbaa304b2baa435b71190c7995e124e1b6386`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:48:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:56:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:56:18 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:56:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:56:18 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:56:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:56:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ac37f50532a7306717e1be2f4760a581740981b55bfee41fb74edf971bbbb`  
		Last Modified: Tue, 18 Nov 2025 02:56:28 GMT  
		Size: 24.9 MB (24864418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931488dec4785216610c9f2c064b20b308e9839859b58a6fb0171606dd6f0514`  
		Last Modified: Tue, 18 Nov 2025 04:08:56 GMT  
		Size: 66.2 MB (66233867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99940d98068ebffe542aa0e530f50776c4bedc8799a98d1d1e41edff316d145d`  
		Last Modified: Tue, 02 Dec 2025 17:49:59 GMT  
		Size: 89.8 MB (89839902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bdcb75a4ff23e4aa0af6e0121aa066fd65b3acbe84f5a324aa319fab9e281`  
		Last Modified: Tue, 02 Dec 2025 00:00:09 GMT  
		Size: 92.0 MB (92028405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2a75197593de5a0c98a2ca804596563ece067ce703de33fa3e6e49086af50b`  
		Last Modified: Tue, 02 Dec 2025 17:56:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ed408ccb99a94793c895963ce47bb1c9c211493f440e3bbe8155be3eff258a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6c7a0ada97e97a40baa4969ce359f80be5314af24759e0f83cc09d46ca987a`

```dockerfile
```

-	Layers:
	-	`sha256:8bfbab6cae9b61762e8558f6abb35807dbf8fb95635dede140341efda523175e`  
		Last Modified: Tue, 02 Dec 2025 18:15:31 GMT  
		Size: 10.5 MB (10475971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e26de90290a22fa3f8480fcffd0a8185aa133100ed0656c58288d68522b085`  
		Last Modified: Tue, 02 Dec 2025 18:15:33 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:6d8c2ebf7b07e952c34bd68b80dcfb60ec75c30d5f807d96c86279970c52e4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293586245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4cc9701d1642276740d94454aa10b6b1034fb30c5821f8ba8c29cf52b38aa8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 19:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 23:35:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 00:17:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:17:47 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:17:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:17:47 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:18:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:18:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bf41c56cb3beefc6b6211c26bdc048d41c337f12bc0bbfcfa89dfb5de99b7`  
		Last Modified: Tue, 18 Nov 2025 19:40:58 GMT  
		Size: 23.6 MB (23614038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a4cb619dbd7fcb3e0be3246f973ccbe692039c1fd01a193751c60045de0d3`  
		Last Modified: Tue, 18 Nov 2025 22:12:34 GMT  
		Size: 63.3 MB (63309296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870c654cc97051b29e543234a565ca86980db6e2499d45b06d4424741a820d98`  
		Last Modified: Tue, 18 Nov 2025 23:38:02 GMT  
		Size: 70.0 MB (70016928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c7f57daffd45249d19ff221e963092e3276eb4462e585f2c7fe931b44b1db7`  
		Last Modified: Tue, 02 Dec 2025 00:20:36 GMT  
		Size: 87.9 MB (87884870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd58fe2a5a32e82bd1a56510d897aa3a55c9667da92d0388c7f42a74e4b56a59`  
		Last Modified: Tue, 02 Dec 2025 00:20:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8a9cc45192cab66bb3f0d2c83b88606fbdd22b1a98efa99ad9a87a173e18b908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7dfe820955b254082406ee5664fc8e55c75c06a8d72ec1e554482ccb35ad6a`

```dockerfile
```

-	Layers:
	-	`sha256:b5617c844e8e38d54d23d4ac7fd98cad8956034e8f00e0cd70e984adfa845627`  
		Last Modified: Tue, 02 Dec 2025 21:24:19 GMT  
		Size: 28.2 KB (28238 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:5d5ea45c9cfe78ebd05d6bd29bdb782e9a59057614adaafc0a2e26380b8a9c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329005866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608cc5676f77c37c2cbff2cd0faa1a3fd9da97da092d97dabb107ebad9dc0244`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:51:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 02:50:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 02:50:37 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 02:50:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:50:37 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 02:50:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 02:50:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4b2f55f19507933712a236b970373c1cf970b213a28d26228399c72f67676d0c`  
		Last Modified: Tue, 18 Nov 2025 01:11:32 GMT  
		Size: 52.3 MB (52326963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17787af1df16ce560e48a9be892094ace19b1aecc7f06ca1e97a2e20987822a5`  
		Last Modified: Tue, 18 Nov 2025 04:05:05 GMT  
		Size: 25.7 MB (25672018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4d717b62eb888bb16cb77af768613d5d676b28f09ab1cb591a5130af4b846f`  
		Last Modified: Tue, 18 Nov 2025 06:52:50 GMT  
		Size: 69.8 MB (69845622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88994869d0f332cc70ccbb2ca7f72eb4c56d6ad96b9820d58b6d3da3c3f1260c`  
		Last Modified: Mon, 24 Nov 2025 22:40:06 GMT  
		Size: 90.4 MB (90419974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060ee4242807d5eec61fa095a5c2f00f155044d9c099f2f96b9280a66eec7ef6`  
		Last Modified: Tue, 02 Dec 2025 02:52:27 GMT  
		Size: 90.7 MB (90741131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d48deb93f3cbb45b7edc6ca2db63735814f002cd7dbbf1968321d2fa3ce51e7`  
		Last Modified: Tue, 02 Dec 2025 02:52:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6431cb8da1cb31cc4d138535cfd69bb3a9ef0164f7fe9bf7531b173667c2a47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa918694958c64829bfedeae4b026a7a5cd7fa90b7ad80e02d4da0333d69433`

```dockerfile
```

-	Layers:
	-	`sha256:a1562b29dbc604f3f02ef5771ae87c3481413e2845ef9366a8ad0e8266341c59`  
		Last Modified: Tue, 02 Dec 2025 18:16:08 GMT  
		Size: 10.5 MB (10468873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46dabcf1b48ebd8fd07f1835b9dd71bafebbeb098459c5cd40eb9e1e20f7700f`  
		Last Modified: Tue, 02 Dec 2025 18:16:09 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:0c10ff8f18c8b8adb821d9d5682a3b99286abb61948bdb441fc7ecf6f23c1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296963822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531c53f21af5f20b51988f794e6b28501283f8556c4c12582e58273e54c398d0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Nov 2025 22:38:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 00:24:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:24:38 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:24:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:24:38 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:24:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:24:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:784b9caf46c66ff55a92c27127d39febf2385f329efae62bb4e65b91f3751223`  
		Last Modified: Tue, 18 Nov 2025 01:11:06 GMT  
		Size: 47.1 MB (47137641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f80247bcc58a5a903807561f3aad626158855a07b7817a9ed9975e9775ae2`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 24.0 MB (24027180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099f215b279a7199da193e9e90d7e8e46ea9dfcda3ebe6c6379eb56d436eeae`  
		Last Modified: Tue, 18 Nov 2025 05:57:22 GMT  
		Size: 63.5 MB (63501447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a07a79185a61d38508c944e9242334a0616777b127368548ba02277054991`  
		Last Modified: Mon, 24 Nov 2025 22:39:03 GMT  
		Size: 69.0 MB (69011120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d587a6ce9332cd64ade4d6449590e6112812b54bfc350eb8b57100babd31c208`  
		Last Modified: Tue, 02 Dec 2025 00:25:52 GMT  
		Size: 93.3 MB (93286276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08440b358baed72456badec2929b9cfc484572f9545f484bfe295627a36acbb3`  
		Last Modified: Tue, 02 Dec 2025 00:25:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c6ca64fd394380080549d8d45a9076b878f52c263c3c8a845b55416581cf4da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e417f9d433a0f030bfe3221463bab3a182a55d9f131528a88ea4154da6e256`

```dockerfile
```

-	Layers:
	-	`sha256:c534a0f11537ddf671a0fedaa733ed2db5e7f2c71a5aa7c3c81650f274536a37`  
		Last Modified: Tue, 02 Dec 2025 18:16:17 GMT  
		Size: 10.3 MB (10328148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a2e4c30234303ce5789e5a3b87ca22af218973cb0ab7fecfac06515d83e6ed`  
		Last Modified: Tue, 02 Dec 2025 18:16:18 GMT  
		Size: 28.4 KB (28385 bytes)  
		MIME: application/vnd.in-toto+json
