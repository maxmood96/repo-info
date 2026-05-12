## `golang:tip-trixie`

```console
$ docker pull golang@sha256:1e8aeeeb42d99b8a9eba5ecc25608bdb28c89eea40fe70541d0e692ed7f80422
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

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:33bd0d258ce677ad3a3538799e0c9e7e35eaf5fa4c2eae8d5e0144be72c11be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342359006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc768fff7efb869c17e436f200f324c807df2f5c09e80a5fe060902579ddb25d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:21:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:23:39 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:23:39 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:23:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:23:39 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:23:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:23:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1562a4840d93f4dbd71969d5fc0efd724f19cd11f89b6ac617b64d93cbe0c99`  
		Last Modified: Mon, 11 May 2026 23:24:11 GMT  
		Size: 102.2 MB (102227813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970dd4e15afd4dda5f0073081cf90c52ecab4076d0f8b775deea9b5b1305744d`  
		Last Modified: Mon, 11 May 2026 23:24:11 GMT  
		Size: 97.4 MB (97416403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7243d4afa8ac19d8ebc95e8191961a3ae626b5f79113027fa14877c0dc8b95`  
		Last Modified: Mon, 11 May 2026 23:24:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8adde72270b20f69431243f28ca7b2ce684aa45511c4f4f3fcf3da6f41016569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01b8bcf66c93cac840057b7a2268d3a2994a0a77d2ba243716faf5606c21542`

```dockerfile
```

-	Layers:
	-	`sha256:9c438755bf96b05532ac13de1debf90257f2af77c913d13b15408088e21e1f7d`  
		Last Modified: Mon, 11 May 2026 23:24:08 GMT  
		Size: 10.8 MB (10785713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c042d512af255a6c079db9786b98b38acc957babcb81182fb2547d352587f6b0`  
		Last Modified: Mon, 11 May 2026 23:24:07 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:280b5784233cc29dd33885a8f5ed4e503450e275c3b45eeca26ae0dc83f43f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298225522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa73013d4232c982bff0496c9c19e4cd46e502acd6f6c457b0c050e3fb61eeb7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:31:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:34:28 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:34:28 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:34:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:34:28 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:34:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:34:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54e91da80876b5fdcd3d8cbdf1cebc52bdf513f8a587b419fa82f5fb473a2b30`  
		Last Modified: Fri, 08 May 2026 18:37:56 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa31143502952cbe5df185dc297d98ec2482b596177bb3d2884695855e7091f1`  
		Last Modified: Fri, 08 May 2026 19:45:06 GMT  
		Size: 23.6 MB (23636413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6753753dc173af6d2d0689a1eccd6337abda3fd742e649454b834a7d6c6afc`  
		Last Modified: Fri, 08 May 2026 21:35:45 GMT  
		Size: 62.7 MB (62728028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4044c98db6cda582fb622308ed321cf4329faff771b0d8c60f0ae4147ac926`  
		Last Modified: Mon, 11 May 2026 23:34:56 GMT  
		Size: 72.9 MB (72867277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa5a325591cc56f1ee0a299253454b588317de6e43dc9dde0447e3b98aa2508`  
		Last Modified: Mon, 11 May 2026 23:34:36 GMT  
		Size: 93.3 MB (93255222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e40c5fa6ba847c35daa8bc0b786f0efb92dafc139d6b1fd256e48536477d3f7`  
		Last Modified: Mon, 11 May 2026 23:34:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:3913f1333d89e193ced171b1a23d5e5de94dc20b8e4b10e076247dc4feb5696f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc07e82795f2fe8d0ff816479df83dfaea6bd90add94bfc9b062e30f84839139`

```dockerfile
```

-	Layers:
	-	`sha256:ee3d30742df3ce97f5ad7c948fd5ca0e385b028adb48b2cbf509c1a0d231db47`  
		Last Modified: Mon, 11 May 2026 23:34:55 GMT  
		Size: 10.6 MB (10581600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d593e21eebc5e3a13a9962914bcdb27ced2435e80c500b3728baaf3d72bab991`  
		Last Modified: Mon, 11 May 2026 23:34:54 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:850f7b85393dd88a3e6fc4bb1e524ea4786cb7247b2e7c10c6950412f0693730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332781700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be59055648d87eeffbc6c2257638e34a4e96fc01beae62ea969fb1fc42af8dd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:23:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:23:57 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:23:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:23:57 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:23:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:23:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b912f40be06a584507634e414b188d131c49242b21474da19d201e5668bf7670`  
		Last Modified: Mon, 11 May 2026 23:24:28 GMT  
		Size: 98.4 MB (98373340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff2fbc71fe7b87fac66a8dadd85dade8191c7b4ae8add0914f8708f3a3fd259`  
		Last Modified: Mon, 11 May 2026 23:24:28 GMT  
		Size: 92.1 MB (92123227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8687d8dba1417c6e4f516bafcb3078aab06de3f1327683a949c906685c07147`  
		Last Modified: Mon, 11 May 2026 23:24:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4b50f9148ba0808708c39122eb46108c962573276a7d75c98db90b012fc5582d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a411052924c6b40932c0f642a4be8ca52a70677717ed1c2e42a5e52b1332b095`

```dockerfile
```

-	Layers:
	-	`sha256:a180d741e14ab10008ae87f14cd742afd377996499f65935ba868f6d41d6be9d`  
		Last Modified: Mon, 11 May 2026 23:24:25 GMT  
		Size: 10.9 MB (10906168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e35610ea82279c28d5b86cb68e66880c6e40d375225f9d3d8eb4a64d4f293a4`  
		Last Modified: Mon, 11 May 2026 23:24:24 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:cd25147bda5a98078cad832993aec38337e40ee9af85aa6e357a00b133d27949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.3 MB (343270348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de846ad85fe5839cbb8694507f9a946a1ae219adc2d1060d33608d66bbea420`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:05:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 11 May 2026 23:27:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:29:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:29:09 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:29:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:29:09 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:29:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:29:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802713bb4712073d4a0875914c45b85ffab64ce3389edccc50bbfe0147fa12db`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 26.8 MB (26784941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3633f2ad7dfa64f7e00b07a5405063f2d661e1f1a5e715c57ad65aaaf0f60d5`  
		Last Modified: Fri, 08 May 2026 23:05:42 GMT  
		Size: 69.8 MB (69815583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd4493c2172d2bf9064068ea7c71b1276b08e9fff1c9c6342ca42957fdd41fc`  
		Last Modified: Mon, 11 May 2026 23:29:40 GMT  
		Size: 100.7 MB (100669217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf08a2b699c1c99de16bf0901d8891e91bf0fcf2a4afdcaef52c57556a2e35`  
		Last Modified: Mon, 11 May 2026 23:29:39 GMT  
		Size: 95.2 MB (95174868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f175d923ca50c7e7fbb57547f535ffe5335864bc9edaeb921029044d65420e9`  
		Last Modified: Mon, 11 May 2026 23:29:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:09389e9a55cfe8042f49bc720c8aef6c288075d600f1f84ba90631b560d59c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa15c121d110699ad8b8e5c62bea98c6c2f14aa4aa79773be15221e3d5c26f8a`

```dockerfile
```

-	Layers:
	-	`sha256:3f368d0b69c58d221148761b29d07178e068e2091ba8b420e1a4adbf2d3b0ff4`  
		Last Modified: Mon, 11 May 2026 23:29:34 GMT  
		Size: 10.8 MB (10756976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2be9b76ca76f96f144b9b2dc24c42a8c678c19555721cf1cc511f30e2de1fa43`  
		Last Modified: Mon, 11 May 2026 23:29:33 GMT  
		Size: 28.9 KB (28924 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:2dd63bc2f984aff2e20a51141528601bd88562ba7727fff2d04c99a7266dbf66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340087733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd92d1bc49bdcac285efa544c3e79a764b363e3cef33562e365727c7446c464d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:28:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 06:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 00:42:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 May 2026 00:42:13 GMT
ENV GOPATH=/go
# Tue, 12 May 2026 00:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:42:13 GMT
COPY /target/ / # buildkit
# Tue, 12 May 2026 00:42:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 May 2026 00:42:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0e7e07df0234f8192ac6b8d0fa0e09c4847b899e2e0718e39e5caccda09936`  
		Last Modified: Fri, 08 May 2026 22:32:23 GMT  
		Size: 27.0 MB (27014633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227313c51a1419e3870baa3444012fd55dfddc51f3e0064592c73f0b1336a3d0`  
		Last Modified: Sat, 09 May 2026 03:29:25 GMT  
		Size: 73.0 MB (73039748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994ee9ee43a37b330c0e9ecc8b0d4c61fc214f581c9517cc68b8d35d38579d6`  
		Last Modified: Sat, 09 May 2026 06:14:33 GMT  
		Size: 92.9 MB (92930754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c0dd6efbd44f19e1e0d6c48f823bb7238da1300bf904818347619de09b8359`  
		Last Modified: Tue, 12 May 2026 00:43:15 GMT  
		Size: 94.0 MB (93979275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fea8cb9937689fb509fcb3ca048a2edeb041d5e9145f172a4c222ddeec92bcd`  
		Last Modified: Tue, 12 May 2026 00:43:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:03bfe05ca3ccce00a99d111700ba31af3e4b5c2ef2fe95915b6ea50b7386ce33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454225f2e18804128b6316180aa1793b9bf099062120380cb0b8d4d336f0b50a`

```dockerfile
```

-	Layers:
	-	`sha256:39b053d91bc6aeb1c6ccd0a2f58896a4a3c39056cd0b7acdc1b0c4adffff53c1`  
		Last Modified: Tue, 12 May 2026 00:43:13 GMT  
		Size: 10.8 MB (10781501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be727393a0d1e59bc735b8a0e9615db3220ff9cc6cfa4f802788907944c560ae`  
		Last Modified: Tue, 12 May 2026 00:43:13 GMT  
		Size: 28.8 KB (28849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:b101b3530a834f6f2637934631929654e436fc35c9dda8381ce82629581e3343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365673574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97a02948ed67849ed219091967d854bf2ed613ab8c6e1c2acba313f89ca49b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 19:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 20:31:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 06:45:06 GMT
ENV GOTOOLCHAIN=local
# Wed, 06 May 2026 06:45:06 GMT
ENV GOPATH=/go
# Wed, 06 May 2026 06:45:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 06:45:06 GMT
COPY /target/ / # buildkit
# Wed, 06 May 2026 06:45:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 May 2026 06:45:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad20ed76b58e7abcec15ac3129845a802887c092560883b4939e006992099b`  
		Last Modified: Sun, 26 Apr 2026 15:22:58 GMT  
		Size: 25.0 MB (24955805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233e35e9c32890f2d416d3e6707a14b173707fad25985773c22f4606dee5c05`  
		Last Modified: Sun, 26 Apr 2026 19:10:01 GMT  
		Size: 66.6 MB (66648074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954c4b6ce8f364903d1d8a7ac953d1cbfe6ecf95f3d8c267e0b27a58b6e61bc`  
		Last Modified: Sun, 26 Apr 2026 20:39:36 GMT  
		Size: 131.6 MB (131649887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d77dd072bbe9d4ad01204d701c796e83867bd2e370f7f50879f12652b55ef`  
		Last Modified: Wed, 06 May 2026 06:52:06 GMT  
		Size: 94.6 MB (94621433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9b99fb2cf5b5e5ae00b5a307aede37e49ad6185be029faa9a7d2d16cbe5087`  
		Last Modified: Wed, 06 May 2026 06:51:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1bf3c5cd79effde86c569d59a4efa2efaf655c0e8fc50a49c512abda4bb94a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c76be1fc8380fc35898c9aee1718f73783c88470c254c67dcd5d3aa1bb1a2c`

```dockerfile
```

-	Layers:
	-	`sha256:84108ed3b601c6d36e56b947c104b072e29bbcffee990f2657bc0188c4b980de`  
		Last Modified: Wed, 06 May 2026 06:51:53 GMT  
		Size: 10.9 MB (10855334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c42688186c1da119f2be2e426528f8f693876aea10fa6700f25559591e02c4`  
		Last Modified: Wed, 06 May 2026 06:51:50 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:8c03ada1cfa88a315e631c99600ab5bab1f65f0f1e11af8f698740c7e5562038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.8 MB (316791427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4485be505ea8a931b975d4327af487896aca7207222fc9a1d4f43217814a17f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:54:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 00:16:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:25:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:25:51 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:25:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:25:51 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:25:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:25:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0445f3803885031cb22352d4abf0c173876f6316acd6230b59fe9c5654bfec7`  
		Last Modified: Fri, 08 May 2026 20:54:25 GMT  
		Size: 26.8 MB (26802639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada3bbdd2fc257950c611fd6795ac67747b411ad1789b54a283e0cb1bb22d4b2`  
		Last Modified: Fri, 08 May 2026 22:34:34 GMT  
		Size: 68.6 MB (68627825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c775d8e658bec93d151c4a165505e929181b99ac8cccbcfc3139166ff0a26ccd`  
		Last Modified: Sat, 09 May 2026 00:16:39 GMT  
		Size: 76.0 MB (76040301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccba99e1a42acaee11681a55a3c5791d533460e7e22dee60816a7d3a0553d4c0`  
		Last Modified: Mon, 11 May 2026 23:26:26 GMT  
		Size: 95.9 MB (95948201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc595bf8502cbe7263d82d424c574041e37c96ccea17ee15a3fc00f8d29ce95`  
		Last Modified: Mon, 11 May 2026 23:26:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6c12df383850586442101b8d1f7351416dcd1ca76ec14c14929ac84143db62c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04f8853f2db559c44856ea5937ff61ca50740224f6ba53299eb20a11dd62a26`

```dockerfile
```

-	Layers:
	-	`sha256:74bff90acd364cfe228cc5a67a23a503464cbad460899d582abd58d9724f0269`  
		Last Modified: Mon, 11 May 2026 23:26:26 GMT  
		Size: 10.6 MB (10596861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db7f61eb93f7ae310a770ebdb17f3ca6ca54f69c74f57487ba383bd0ba34b423`  
		Last Modified: Mon, 11 May 2026 23:26:26 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
