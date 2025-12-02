## `golang:1-bookworm`

```console
$ docker pull golang@sha256:5117d68695f57faa6c2b3a49a6f3187ec1f66c75d5b080e4360bfe4c1ada398c
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:2cda9d4e864a146edf71636f5d6d2087210a427c1cefd10027817ae8327a5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289468300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddf366a47201489eafbc9ae0f57c17a900dda836b181035543e8a072dc90c00`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:47:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:47:05 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:05 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:05 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:05 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:47:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:47:07 GMT
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
	-	`sha256:17b4f0a5437aacc31281214a81e0c12b6b94be243dfeb973777be97763c6dd81`  
		Last Modified: Tue, 02 Dec 2025 17:47:58 GMT  
		Size: 92.4 MB (92410456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a62cba54aecb627f3ba7df2180f3225905021445fd2e7169d56943732d82531`  
		Last Modified: Tue, 02 Dec 2025 17:47:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:68ace596cdb6423359652a79c7aa40cc185dbf10a8ffa651fdc37d359cea25de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef26f0366b9968873f305f3dd3780bf0d830b691c011d526e09706bf74e1ea8`

```dockerfile
```

-	Layers:
	-	`sha256:5ebe3f4b60494035f7b7ed3387ee109af42ed12b50e53dc4a49fae362ffb63e8`  
		Last Modified: Tue, 02 Dec 2025 18:10:15 GMT  
		Size: 10.5 MB (10495740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddf4214419750974d83592eac1b2f6daac80adc518b2526d004f566854cb718`  
		Last Modified: Tue, 02 Dec 2025 18:10:16 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:abadfa0478f60d86c2a358c4621a2d56fd61e4330fbeb8ebee23012d3ac779ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251131625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b1d4fa243b169cedccdb4fd9ad2019968ab6dfff3bf6e973411f819066f932`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:48:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:49:44 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:49:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:49:44 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:49:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:49:44 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:49:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:49:46 GMT
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
	-	`sha256:db7e94c8844799c0aecce332df23363ceb55fde4be561bd0f0d9108bc7777fb7`  
		Last Modified: Tue, 02 Dec 2025 17:50:24 GMT  
		Size: 66.3 MB (66276456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf306fc19cfaa820bad4c027c09205ad69f1956ced78ad879e72f67db6c99df`  
		Last Modified: Tue, 02 Dec 2025 17:50:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:59f9e2ed3a283fc7fcee9a3fc0f166e2f7868692cfb1dd7bf1d79525df20784a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9332d70df179125af2a1d2d46c5e48f55982ba0f1038d9dc531c636b8dd35d9c`

```dockerfile
```

-	Layers:
	-	`sha256:be3b3b438459cdbe1dab4c9642fb3b9d12eb7f2626b63ca7b697b566209d4d03`  
		Last Modified: Tue, 02 Dec 2025 18:10:25 GMT  
		Size: 10.3 MB (10302454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8453e874d3abd13cc5c69445af6112cfc75c753eba0e3a56c6527249c6f5761`  
		Last Modified: Tue, 02 Dec 2025 18:10:26 GMT  
		Size: 27.9 KB (27902 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ffe51f4855156e722eaba15c0bd2b270128341b197ebc817429127467532fbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280470864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bdefd1dccff4fd0f0f6fb54d9237320a4919391fc437ac034711d0d0b9c9ac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:46:41 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:46:41 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:46:41 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:46:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:46:41 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:46:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:46:45 GMT
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
	-	`sha256:94f3100af55c6cc1d889f6ee593cf20cf25e90787a422ce85897ebbac375112f`  
		Last Modified: Tue, 02 Dec 2025 17:48:18 GMT  
		Size: 86.5 MB (86490917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdffdcd5eae9143b45e083e7f9a208c7c007cf6a3e0b81b3b6936aa199f9dea`  
		Last Modified: Tue, 02 Dec 2025 17:47:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5b92f943590e2ef6bf5c4b00468558baf39c50a1164f4e47c24a507b65676a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04dcde2b4ec49e4ea6f77c1639d15d2ec2d2fc2d8f93428aca52860f6174bd1c`

```dockerfile
```

-	Layers:
	-	`sha256:c352be7b2f712943551def810e17eb9ec367d730a28b9ef4810da148e3552385`  
		Last Modified: Tue, 02 Dec 2025 18:10:35 GMT  
		Size: 10.5 MB (10523588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedddb04055e555be4daf42f4b5bd60643e56500371adf096d25c2521d5954b0`  
		Last Modified: Tue, 02 Dec 2025 18:10:37 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:4002265cc9fa0518acea37788d13186cba31b7175c3189be7def0e02ace12621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289277148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d507ae67bb6b66cae16fcb3e04dc25ea9f5b93bd501455c714dfe01bc883ac2`
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
# Tue, 02 Dec 2025 17:49:17 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:49:17 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:49:17 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:49:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:49:17 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:49:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:49:19 GMT
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
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2013136094b019ed3e561540c3e51eaca65526c1f568a4efe3e2a96f4459a09a`  
		Last Modified: Tue, 02 Dec 2025 17:49:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0a2aa5f6a3be8f131ef83025b74c003f1bd367345be5a393e6e107f1341e9bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b36f8a7aad96934d14b48751379588aa5fc9c6497788b78e6bcdd64081e316`

```dockerfile
```

-	Layers:
	-	`sha256:c21e1efdd3a24541ab2ebc69211bffc1251aa077c8b2159efda05792d36b8f92`  
		Last Modified: Tue, 02 Dec 2025 18:10:45 GMT  
		Size: 10.5 MB (10475313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934f332bf504974fec183d0eeb4667eb7c692f6c2a5956b3e59e21bdedba2388`  
		Last Modified: Tue, 02 Dec 2025 18:10:46 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:761ac7e26f737551e312d7892c66dc03b90f7c70df31c931e76a3d0b2092e0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262275800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b167ded7bf95732b9a1dcef243fff694d6f308c3bf2e8e5f5ce50ef9825f32`
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
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:46:31 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:46:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:46:31 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:46:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:46:46 GMT
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
	-	`sha256:8a811f73ff0cb3df64f15904472d8c052172a4266c947c138019cab5cd2bb575`  
		Last Modified: Tue, 02 Dec 2025 17:48:38 GMT  
		Size: 56.6 MB (56574424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db03ee1eec28579922a5f9de30a7ddd80a30842e9bfaab86aaa5d32c2de5d4e`  
		Last Modified: Tue, 02 Dec 2025 17:48:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ad348627e37d691609661e66e6a9e72929c5842fe122b3ee393e9f580e5f5993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c09389455c8e6c19b04647e083d1c01dc747cbfd7e6c3f25305e4e4b6cd083`

```dockerfile
```

-	Layers:
	-	`sha256:ce8405d402b5eb07104a14ec9faf8abe87c644ccdda5d7d4a991eddee8746731`  
		Last Modified: Tue, 02 Dec 2025 18:10:53 GMT  
		Size: 27.7 KB (27653 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:0b442fb0c2bd849238282eeaa7c03f201e6038b64f9a3e0dba2151e607a2ac34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296399682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c62fc0082c973d9c1baf444ba6958ff0853784be61fe5c840213f680354af35`
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
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:46:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:46:09 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:46:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:46:17 GMT
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
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32208218379498b58e45f76e2f9d26aac977d5ecd3c41946f19b410c1e662d5`  
		Last Modified: Tue, 02 Dec 2025 17:47:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4ed93d85953c4a8a8ffa84ae941e0684dfbcf4ef42a2661e7711769d4a7e2162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae8cc3485c2415df74461655a8333ac242b7c5f5e7010be2c7bfde0d833aa76`

```dockerfile
```

-	Layers:
	-	`sha256:f1434887448d066fdbdb174fcd5c9ab36f176ac753581728745fd89e175d538a`  
		Last Modified: Tue, 02 Dec 2025 18:10:58 GMT  
		Size: 10.5 MB (10468233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50a52b1f3bbe830f8d53e986dfe53aafbe9a43e8795cbd5d2c26ccce34be37a8`  
		Last Modified: Tue, 02 Dec 2025 18:10:59 GMT  
		Size: 27.8 KB (27845 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:443566ae422ea1fd8c765fe95836674e01bb02d21cbfb457de3ae98bfddb0550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263164764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b322c7710c873551a09fc83e44dd246472ee4eb3abd7d802699a37c82f9de3ca`
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
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:48:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:48:28 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:33 GMT
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
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d419ba7d33a7aff89f4f162d7f80f73a4b62020a51e81530406474b71e63be`  
		Last Modified: Tue, 02 Dec 2025 17:49:42 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:13b8983555e5c86efa6783f4e455d4f534316bad75bd23f6d3c980d7a39888c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c8df7421113e23356fc7e7f38f9bcb33aa21da35df3e72a5bb447b51e5034d`

```dockerfile
```

-	Layers:
	-	`sha256:574178dc48bf43f946eaa533921c51576c88f29a74cd64a08fdd7c507188877d`  
		Last Modified: Tue, 02 Dec 2025 18:11:08 GMT  
		Size: 10.3 MB (10327498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c15c669a60330391eaa2e0d50d8016594646014b9417ca97a1013e6d9ef62b`  
		Last Modified: Tue, 02 Dec 2025 18:11:09 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json
