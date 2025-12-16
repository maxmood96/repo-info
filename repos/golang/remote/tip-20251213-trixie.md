## `golang:tip-20251213-trixie`

```console
$ docker pull golang@sha256:f514d7de8fab808405c7143c4597d02cc700a28374d29a8bc61539fe6c4783be
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

### `golang:tip-20251213-trixie` - linux; amd64

```console
$ docker pull golang@sha256:bf0304a242c41117a61e9423e193664943d76996553aaafe3fd258539cd25db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339820839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a9aaf83cb52d2f9b2ae6dbe7c4d5d5e0665fdc25f76027e311c730e593e35e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:23:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:24:39 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:24:39 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:24:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:24:39 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:24:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:24:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d41a52b8177200ac52bb446c7c3d4174df30543f707759303149c0d29f3b2a1`  
		Last Modified: Mon, 15 Dec 2025 21:25:31 GMT  
		Size: 102.1 MB (102108709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc02f84f9201c7821773dd34545e63ce7af776f9b234f6a13b2589fafa66eab`  
		Last Modified: Mon, 15 Dec 2025 21:25:12 GMT  
		Size: 95.0 MB (95029942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b580f081f2b1504d547e141b7b97de3d460883d53c6ddded0b8fe831fd1dc6e8`  
		Last Modified: Mon, 15 Dec 2025 21:25:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2949cb0fa42c1d0d24fea123db416eec6555b862e02f3e8609fbba028e186392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b2d30900ab9be9e3eb5d076999c4ed955461180d7f52003d423f8eb98dfeae`

```dockerfile
```

-	Layers:
	-	`sha256:0b55a3cb014f30736548f9c46168478305075c2c4ad76572657d2f5023be9a01`  
		Last Modified: Tue, 16 Dec 2025 00:23:33 GMT  
		Size: 10.8 MB (10784508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf96bdf925439bea12cc177c45b9730f3c1ebf3f444bc447cbe8cdad6e36f42b`  
		Last Modified: Tue, 16 Dec 2025 00:23:33 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:d1e9606b4f336651e4f6799a2469dcfdf8ee9abb3abe6d2a94612af7945db93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295907292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206069bd468300114b8e0397e8fa36215ceda3eb0995daa36f6da0ae92f7a230`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:25:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:25:36 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:25:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:25:36 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:25:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:25:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c4eba7a08ba9825cabd599d8641314a004d500b627e05a38640b9d3c0bf389ef`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.7 MB (45718282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6ad1d8bb6e8d2c91990f13409d4d822c19a3b9fb5463aa9033cd860aaa4822`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 23.6 MB (23620171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067e549495a4594bb4406cebf8990f1500f9fbae204461f2b793444540c774bf`  
		Last Modified: Tue, 09 Dec 2025 01:33:43 GMT  
		Size: 62.7 MB (62713415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934d7b9caaa1f454cbaba430561f5b7d60f26ebe16fa0cb9ef0ae589e3f942a1`  
		Last Modified: Mon, 15 Dec 2025 21:26:19 GMT  
		Size: 72.8 MB (72754035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bb87a632660b1037516c680a04b7758d1bccc030a199d5938a3d13de229878`  
		Last Modified: Mon, 15 Dec 2025 21:26:06 GMT  
		Size: 91.1 MB (91101231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020e174a25bb68504a1063168705d2a82427f3f95d980bbf79916990d584565a`  
		Last Modified: Mon, 15 Dec 2025 21:26:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:0ed9484f76daf5c80f2311ca1d63f39140c7600a4cdc57f3420c4119ce8c7baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938f553a0e3cc6a48e70ec248fd3eb0a809f052e5ba412bc6dd5a0e51f2bad66`

```dockerfile
```

-	Layers:
	-	`sha256:fc853653bb071daa1e025c05b7494b0bf61d6bd01ec1ec81be05ea8e69d17c36`  
		Last Modified: Tue, 16 Dec 2025 00:23:43 GMT  
		Size: 10.6 MB (10580395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a95614d45843603ff7be8fe8715107293d3bca340a3a8d626961ea0368c383`  
		Last Modified: Tue, 16 Dec 2025 00:23:43 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:43445e582931ca16d320961d8c67a4fcbbcf12a0740727c58019b263603bfc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.6 MB (330619301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8887f9261469496f099ceedbcf9877f3fd4d95b60fd824f2c9c8e7a1e6a142fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:24:12 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:24:12 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:24:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:24:12 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:24:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:24:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc8a961bfb1e5ea5471b542a7f2d9a067e72625183ab9ea3f51c0c0b82b752a`  
		Last Modified: Mon, 15 Dec 2025 21:24:56 GMT  
		Size: 98.3 MB (98254585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e7781f7b0020f1ea08137b4961d1e1c8dffbf5d0dd96335fd03fec85f64136`  
		Last Modified: Mon, 15 Dec 2025 21:24:55 GMT  
		Size: 90.1 MB (90108378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed71f6deb0a1ee70218f0142b7b7fbe9c927876fadd736571c70ad7e724c4288`  
		Last Modified: Mon, 15 Dec 2025 21:24:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:5adefbb9ea4e7dbc1a098f43f86d685a4fb1eeccbffdc756c68ba119ce0d0fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12137f24707645e89a2abfe301a02abbefdc5bdea69f4a440f6fd575fd5f15bb`

```dockerfile
```

-	Layers:
	-	`sha256:b8294ed8a1ece62e12243caac93baab521591fb4b844cadc87ec84f82a88229a`  
		Last Modified: Tue, 16 Dec 2025 00:23:52 GMT  
		Size: 10.9 MB (10904963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c5972daa6b7389f825a1729cc73de3928521533bc5c13e8fc9be028af876bda`  
		Last Modified: Tue, 16 Dec 2025 00:23:52 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-trixie` - linux; 386

```console
$ docker pull golang@sha256:60bc6812de11f7c0b48bcc8023a4e3979f1079640646b4d5c21498a8841fe8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.8 MB (340847144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9dea01453c749774cd62841048661043be663be2d3876653b32330c748f8b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 21:20:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:22:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:22:50 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:22:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:22:50 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:22:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:22:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798fea9bbf98ef639c9ca23d745bec44c0d7b28fbd93792d4578fc5b43e7569`  
		Last Modified: Mon, 08 Dec 2025 23:14:38 GMT  
		Size: 26.8 MB (26776300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d1731e98c6e5aff4c28a002263af9a4fc5c06d23cbc860d258dafbd603ef2`  
		Last Modified: Tue, 09 Dec 2025 00:24:53 GMT  
		Size: 69.8 MB (69794656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616f27f027d69e5badd4b409c87f8e88e0e1b2b1c502728796cb7e4c0617af6`  
		Last Modified: Mon, 15 Dec 2025 21:23:41 GMT  
		Size: 100.6 MB (100556048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f38140e210287454904f48ab9f4aea2db0ef2d57fe485fd6478e18a07aa5b9`  
		Last Modified: Mon, 15 Dec 2025 21:23:21 GMT  
		Size: 92.9 MB (92918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c392d30edd471645e9a898b39b35014066c8ca69395acd2fa4cdc7ae0613720`  
		Last Modified: Mon, 15 Dec 2025 21:23:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:a36575f2a10467df05b4fc26a34ede521a60c2f7b23ef6cfede94732583b5272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce765d4f7c61a46c86734584118b94b93a4c3c58d600c00d057676dd0ce3392`

```dockerfile
```

-	Layers:
	-	`sha256:5829e2941b07cbd95777d29b030b47168a82e06b752f94c2545808cfc8ac270a`  
		Last Modified: Tue, 16 Dec 2025 00:24:03 GMT  
		Size: 10.8 MB (10755772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63e8dd6604c4f73ca8c78ed52d690170f0875b4d61e967de45eb74b2288cb4ed`  
		Last Modified: Tue, 16 Dec 2025 00:24:04 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:5faaa11e3a41b611e01d01e34f5856df19369e5000b1eecef469a1bd6ba63d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337592778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692e307464c1b27733fdacfb50319348484019f8a7f55f5ecefd540e2d238fcf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 06:20:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:32:59 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:32:59 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:32:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:32:59 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:33:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:33:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79cf54a8287f03b9105a7213ef3a99e05832db0bdcaf506dd64b872bddfd7b`  
		Last Modified: Mon, 08 Dec 2025 23:23:25 GMT  
		Size: 27.0 MB (26996775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbdd943d24ee93fc3b0013d3315e9ace0f4529c7fcae39b318579723e579b6d`  
		Last Modified: Tue, 09 Dec 2025 02:13:21 GMT  
		Size: 73.0 MB (73022086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62094cf6808b342239ceac9c58c9096b769bf275793baaa6699740b93ef88f7b`  
		Last Modified: Tue, 09 Dec 2025 06:22:27 GMT  
		Size: 92.8 MB (92815776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14547495cfe8d3d44ce957beb44799d810dbc881ef14c6f75d1efdc8e9917f3`  
		Last Modified: Mon, 15 Dec 2025 21:34:40 GMT  
		Size: 91.6 MB (91649505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2945255244509b972595ea2cd2141ed54c0c1a14d5fbf0d0c9d42612cbef80fa`  
		Last Modified: Mon, 15 Dec 2025 21:34:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:373f3022b77b2532e8d202724f144ca9f65e3921737f325c8ea94104d134bd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cb4dd45227b1e63d92f161f201f0388f5a4dc31a230d93e13807a6ce26f84f`

```dockerfile
```

-	Layers:
	-	`sha256:50beda32b2fc4941baa88ee89fbf157362545575e71167ade28f421a3be92b4e`  
		Last Modified: Tue, 16 Dec 2025 00:24:13 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8374659c9b353c6ba0f203c5618d3e3ec69972ed30bceaeea0ed8bc56d791cff`  
		Last Modified: Tue, 16 Dec 2025 00:24:14 GMT  
		Size: 28.8 KB (28849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:95bad55ab6f4b44bba05a918e9486e42f327aec52baa2024de52febd869be1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363269882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664ef00ac8d1763f05bf62960b52f1e3ddb19ec9c07d02a12ec1b012c71df12c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 07:00:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 14:08:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 16 Dec 2025 14:08:40 GMT
ENV GOPATH=/go
# Tue, 16 Dec 2025 14:08:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 14:08:40 GMT
COPY /target/ / # buildkit
# Tue, 16 Dec 2025 14:08:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 16 Dec 2025 14:08:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088c9d98910c38f13b1907a28647a9e78cc7ea821df93ab45af07ce2813dcab`  
		Last Modified: Thu, 11 Dec 2025 08:40:59 GMT  
		Size: 25.0 MB (24953834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60a42ed8727e43dc5cd180abfcc19a18468941394808f724b1f4dc00352352`  
		Last Modified: Sun, 14 Dec 2025 08:50:41 GMT  
		Size: 66.7 MB (66660499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4af291d8cbdff6d28ddd144cb820c9d50e09d2eefe7cf2deb9f3384fddd0193`  
		Last Modified: Mon, 15 Dec 2025 07:10:40 GMT  
		Size: 131.6 MB (131594746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ccfd6d0019903e9f30a7248d0011153e90d92f7a748480439ea4f6363c5dfa`  
		Last Modified: Tue, 16 Dec 2025 14:16:03 GMT  
		Size: 92.3 MB (92289512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b58cb3b8de3d47606b6b89bab9c9e87afd2c3b89a355298a472b0a37cebf9a0`  
		Last Modified: Tue, 16 Dec 2025 14:15:56 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e747ea805a87cdf674fb8c3d39923fe3e52b9a8de15de8f00fb574078694d020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b0c8b076e6772f53c883c6c082357e570359516cd0720028e7be78fae4a787`

```dockerfile
```

-	Layers:
	-	`sha256:a69de620ab4a6ccb15f77cf5667217d2df153e2ec2e790dfec544b957f83e264`  
		Last Modified: Tue, 16 Dec 2025 15:23:53 GMT  
		Size: 10.9 MB (10854127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7517101dbb1554791102f3393fb6a0159701d43889359f53cc5e97d7d675aa8d`  
		Last Modified: Tue, 16 Dec 2025 15:23:54 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-trixie` - linux; s390x

```console
$ docker pull golang@sha256:dcb760274ec51232e3f550d673cd6794d0c94b914dfc694b5d1b572a050d34f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314874837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d387cd9f7f66591dd47739b73a77cf126d60ed59ba35a02aa4e94e71b52394`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:23:21 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:23:21 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:23:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:23:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a105dbf5cfcb4e2c38a6c33b07d696009c0c1ce742a7404e87b258f0914a1424`  
		Last Modified: Tue, 09 Dec 2025 01:47:55 GMT  
		Size: 68.6 MB (68624346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2be274f95003449a8278cbc7ab315c7bcb675710ce099ea39eaa8742edd0f0`  
		Last Modified: Tue, 09 Dec 2025 03:00:19 GMT  
		Size: 75.9 MB (75919454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a1c518cab5112d07a0a3193c5ca3ef905e28d8e262915c8e207c186ea2395`  
		Last Modified: Mon, 15 Dec 2025 21:24:04 GMT  
		Size: 94.2 MB (94198456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fe83f6ce0ccd65e37520a4e1571cbd5e865ea2d50329c47c67b99b3d304b5e`  
		Last Modified: Mon, 15 Dec 2025 21:23:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d1f9c1ad45ccaf989d2ce4b8035638b7d55f2721af7d41bc702cdf479d33e704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d08bf0699a849359e9c48ec9028c3d05403f1c54af0ffc9df2818796c180d6`

```dockerfile
```

-	Layers:
	-	`sha256:1da7c969b53faa6d95bfd917752e11da2957c09f3a15efe53545d0715d295c0f`  
		Last Modified: Tue, 16 Dec 2025 00:24:22 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b081bbdc94e770f8cbcb523c0884beeb7ff805177a5dafe7a98fef914bf7c9f`  
		Last Modified: Tue, 16 Dec 2025 00:24:23 GMT  
		Size: 28.8 KB (28791 bytes)  
		MIME: application/vnd.in-toto+json
