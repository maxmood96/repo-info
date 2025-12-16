## `golang:tip-20251213-bookworm`

```console
$ docker pull golang@sha256:5be33cc0f3cc3a405d6361640db4af55edf10a6f07efd427f5bf28f0f5a5ec9b
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

### `golang:tip-20251213-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:c56ee36e719b98efe7a539d5154fbae7a5a4d2b23760f4144cf5411cc1e6e582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324347197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a063f6966ad7e7eaf3856f4e8f794742c2267b2f3a47db325923326f62eb9d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:23:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:24:49 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:24:49 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:24:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:24:49 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:24:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:24:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc431fd237b74b86b5b82955301a4a121dbc1ca8d60b346a038b52b63b2d341`  
		Last Modified: Mon, 15 Dec 2025 21:25:41 GMT  
		Size: 92.4 MB (92410505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc02f84f9201c7821773dd34545e63ce7af776f9b234f6a13b2589fafa66eab`  
		Last Modified: Mon, 15 Dec 2025 21:25:12 GMT  
		Size: 95.0 MB (95029942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f8a63fd089838d22aeda883ef43fb411b49a3b1e993772c02ca69374771cc`  
		Last Modified: Mon, 15 Dec 2025 21:25:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ffbd7db4b713f405a4e8aaf6acb1c54ad8ff854e080951a48c170fbda1158359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a45be2709dfee8bc092794b8f87150c4c9df81de33eebc3654c37c5cbf6ce5f`

```dockerfile
```

-	Layers:
	-	`sha256:16ec5fb68a03471499c101fd3e8bdc9a7d02d35675ae8a16e9a988a7c60a9cd3`  
		Last Modified: Tue, 16 Dec 2025 00:24:41 GMT  
		Size: 10.5 MB (10496388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c177b326f7d5111c649364f251b087a7180e64fb84156395256ac6a2821c76f`  
		Last Modified: Tue, 16 Dec 2025 00:24:42 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:aa5ebbf788ad08aa50095aa9356b8de09cd5dbf5bdc0645a65627192dd2d108c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283161460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fcd54b73bd17033fcfcae9cc19d0cecf32b54c0f37f57bd5134847aaf0c356`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:25:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:25:37 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:25:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:25:37 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:25:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:25:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66aa6761aa99c557c882b6cb71cf839a06b4634c5e4d98e4a93d946b4554c6f`  
		Last Modified: Tue, 09 Dec 2025 01:33:23 GMT  
		Size: 59.7 MB (59652900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd03e7a15eff673c0b9b0ec05cd07e5782f7b8f98fcf7932c6c97a82b85655e`  
		Last Modified: Mon, 15 Dec 2025 21:26:15 GMT  
		Size: 66.3 MB (66276470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bb87a632660b1037516c680a04b7758d1bccc030a199d5938a3d13de229878`  
		Last Modified: Mon, 15 Dec 2025 21:26:06 GMT  
		Size: 91.1 MB (91101231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924e02db304776059df1c703b1d4673bf56c7b0e77ef9ff8a86f36816f4cfe36`  
		Last Modified: Mon, 15 Dec 2025 21:26:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ebe31017a2a1878d5c1d569719834722e88febbee2ed94fd08e09976b588a123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2816a18adf63c52e13cd95469de38a33908b9a86782cc4562ed5ae5b5cbbf037`

```dockerfile
```

-	Layers:
	-	`sha256:366fa9a90b4d4c16683817f8662794789daa190a8ee5724f8da86677e0473b2c`  
		Last Modified: Tue, 16 Dec 2025 00:24:52 GMT  
		Size: 10.3 MB (10303084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47f6fc1b4c6f69dbd7aca7ecb21882fe2bd1150e7f44476318f59144cbc6e99c`  
		Last Modified: Tue, 16 Dec 2025 00:24:53 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:114a5c10c8e7aa5fb2c3ee992ef625ef5842064cf76efe6b6cda7abf95426896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312928361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f53c3a07e199675eb21a248b0554ebaee63ef3746be559dfb4ac2e793ddbd9c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:24:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:24:20 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:24:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:24:20 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:24:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:24:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bcbdedb4e41f42d3514ff8bdf2206e81983ed8453e4193062d95399fae72de`  
		Last Modified: Mon, 15 Dec 2025 21:25:12 GMT  
		Size: 86.5 MB (86491019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e7781f7b0020f1ea08137b4961d1e1c8dffbf5d0dd96335fd03fec85f64136`  
		Last Modified: Mon, 15 Dec 2025 21:24:55 GMT  
		Size: 90.1 MB (90108378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6895a985a5f770d2073e6e23848433ca43bbc8e6cc8f28b0a4a06a2be4bc677e`  
		Last Modified: Mon, 15 Dec 2025 21:24:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c449c67a8e7200af4df6891a835d797f9ce36b970492ef9d9f3aa0040627dc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e100d0f673d5d2ebf478a9945dfaba3f9a1ca2ba1e97d8066e53f271a26193d9`

```dockerfile
```

-	Layers:
	-	`sha256:b0c989ae893d411bf94c7e740fba34c06167f2b115f1fdaa447373871df826ee`  
		Last Modified: Tue, 16 Dec 2025 00:25:04 GMT  
		Size: 10.5 MB (10524212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:969f650a749b3e94591dfecdb629045b2e30a7578bd3ba1d546e257a5d3ceb56`  
		Last Modified: Tue, 16 Dec 2025 00:25:05 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-bookworm` - linux; 386

```console
$ docker pull golang@sha256:7923b68f406c3e7b5df9bdffad8ce112982a2bd7445b8b7ebeccf961b058f4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323324326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c86a758fa311d2cad0e8ea79849c42fb82bd7a026d13db761bd84f826ae605`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:14:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:22:49 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:22:49 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:22:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:22:49 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:22:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:22:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8c9cca3d9f455dde3fab1917d275b029f5f2978fcd1f8f1b757098b58abc9d`  
		Last Modified: Mon, 08 Dec 2025 23:14:28 GMT  
		Size: 24.9 MB (24864339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd442778352104a3bf918f8351b8ac2573f9aa7b0d9136092884f7f79017f9a2`  
		Last Modified: Tue, 09 Dec 2025 00:24:01 GMT  
		Size: 66.2 MB (66233858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a334c4b0f156bbb85ec4337b8a6724943d6ac83b8d61e93ea1bad22a2675d1`  
		Last Modified: Mon, 15 Dec 2025 21:23:31 GMT  
		Size: 89.8 MB (89840819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f38140e210287454904f48ab9f4aea2db0ef2d57fe485fd6478e18a07aa5b9`  
		Last Modified: Mon, 15 Dec 2025 21:23:21 GMT  
		Size: 92.9 MB (92918333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae15b0f3bf020f3269152cc95282c6e92b383fd9d53f038fac62d4b4d1a38f9`  
		Last Modified: Mon, 15 Dec 2025 21:23:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:09a902cd45e27d37ef0a9fd7cb25205071b4b3576d6ae9d49c508d7fbba644fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c051301b0a21deb6e31b6b58213ad30ea5e2e2699a74bd00466243d7e683203`

```dockerfile
```

-	Layers:
	-	`sha256:693ff61db4545ee30e2b52c0e6c37ccabfa8f64cd9df8a5312b098ebc0126da5`  
		Last Modified: Tue, 16 Dec 2025 00:25:15 GMT  
		Size: 10.5 MB (10475969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0630d312f991152b2849290999d8ce51d9a8c3affafc725d349396b42814b88e`  
		Last Modified: Tue, 16 Dec 2025 00:25:16 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:9456f25f212d6b564484d829644141738b23555da4d798d948ffd63c0b3874ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294483630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f8f3cd83d2fe65c673d13ee55879a0eeda43dd0800bdfdf546e46994968a90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 15:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:09:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 21:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:38:46 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:38:46 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:38:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:38:46 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:39:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:39:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:39c87c0b77499147a54de9b3e5bae714c175e6e770a910d9f420c4e6fb61ba58`  
		Last Modified: Mon, 08 Dec 2025 22:14:39 GMT  
		Size: 48.8 MB (48760897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1571bb35c4ff72a581f317370ae35a4e1c5896fc868d9d6a6a545382b80d1b1`  
		Last Modified: Tue, 09 Dec 2025 15:10:23 GMT  
		Size: 23.6 MB (23613949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7e7f53e0184cfbc8481d8bf6e3898908651f4106389843dddb844d4e45ba75`  
		Last Modified: Tue, 09 Dec 2025 20:10:46 GMT  
		Size: 63.3 MB (63309593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c4012ce2cba975e6e5e0c4498492dadfcd953fd94bfbda58e546a544114552`  
		Last Modified: Tue, 09 Dec 2025 22:01:04 GMT  
		Size: 70.0 MB (70017142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691f72d91cd2cab4628edbb34bea4a751c0b3073001f04678d8b20562e7f1ffb`  
		Last Modified: Mon, 15 Dec 2025 21:41:24 GMT  
		Size: 88.8 MB (88781892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0cc836db6182f59369685583ca9bed95ef4ff2d924fb6902a42e1da8954c82`  
		Last Modified: Mon, 15 Dec 2025 21:41:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e814ae1452ad77f103c4a8d77d8aee371544c90b7313683c5e4893931bbae909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa00699a332d90d9e20502d47a6b0dbc76ad0d3adfdb20a371a20b7aacff81ba`

```dockerfile
```

-	Layers:
	-	`sha256:18778338601745384e64c2e525b1d09226755e1216ee47068b2df4a97ec5ab67`  
		Last Modified: Tue, 16 Dec 2025 00:25:24 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:30a041833a4d3b605199cd484b3a5636e059d8298ca01205d93a2e4ba082cf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329914803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38a0a96c8903b95fec6547d068264d231aab8dffbec9dbf6dd3fafcf29b57aa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
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
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4109a037ac4c69c3ce26e6d14e10c867842083c363485abd63db45502611991`  
		Last Modified: Mon, 08 Dec 2025 22:28:59 GMT  
		Size: 25.7 MB (25672209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2b93c70c0b05a907d16ae217d77a407e9aa88f69499ffbfee4375b49ab6c01`  
		Last Modified: Mon, 08 Dec 2025 23:22:14 GMT  
		Size: 69.8 MB (69846008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fcf0300c06237c12ec60c09556f95a6b8c833ba82bfc5828beb977742de538`  
		Last Modified: Tue, 09 Dec 2025 02:13:29 GMT  
		Size: 90.4 MB (90419946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14547495cfe8d3d44ce957beb44799d810dbc881ef14c6f75d1efdc8e9917f3`  
		Last Modified: Mon, 15 Dec 2025 21:34:40 GMT  
		Size: 91.6 MB (91649505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df681ee7a98ddcfc99de01262550e97ecffd86070ad6f563e9fa7c663870ca66`  
		Last Modified: Mon, 15 Dec 2025 21:34:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251213-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8b47f4e1c2a5fe40ea38990344d3cef85d23b17ee9a401b4fadc70843fe2bbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5e2804c6b6ecf7e48c1c25d10db6b05c84ed82f2cf2efab570a65133346200`

```dockerfile
```

-	Layers:
	-	`sha256:e9af9ffbd64a21175df322e80593eb117a176e6b2ec604797f2059587a982364`  
		Last Modified: Tue, 16 Dec 2025 00:25:28 GMT  
		Size: 10.5 MB (10468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93305cc474b23efd09eaefacb4d4010b7595380231ba83545a729c2c60581938`  
		Last Modified: Tue, 16 Dec 2025 00:25:29 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251213-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:5c3ae21df32c5bd1c4f775224b85c1ec2665f98da63ac1e64dcc4cbdd1a3f257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297874650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f587cdb2094f16a74688e034201faf2c688a79971781aebce13ddde8b479efa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:10:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:59:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Dec 2025 21:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Dec 2025 21:23:24 GMT
ENV GOPATH=/go
# Mon, 15 Dec 2025 21:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Dec 2025 21:23:24 GMT
COPY /target/ / # buildkit
# Mon, 15 Dec 2025 21:23:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Dec 2025 21:23:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4635598f3b0f128359fc25d526138bfeb1cfd50aa2df3f8a5a9214cdae1551f`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 24.0 MB (24027286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c85977b1427cc2c2afbab15cfdcc745e64492465bdc1299648a91c7787a768`  
		Last Modified: Tue, 09 Dec 2025 01:46:34 GMT  
		Size: 63.5 MB (63501228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7c78d8ef4c672ad3a1b17951daa282f21316a1dab32f99d9430a850ba86084`  
		Last Modified: Tue, 09 Dec 2025 03:00:20 GMT  
		Size: 69.0 MB (69009858 bytes)  
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

### `golang:tip-20251213-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:05f09448e217ae59fc354d12a5ccc49392bce2c3d30badfc4049e5248492a47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10356359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4fd28498d2223b36d4fd15847bbbee60abdd452bb0a76a5a33942659a3cda0`

```dockerfile
```

-	Layers:
	-	`sha256:5d92ad17fc86f84e6cd75b0c9a9a36a524eab218487b37e32aafed0aa1b3b42b`  
		Last Modified: Tue, 16 Dec 2025 00:25:38 GMT  
		Size: 10.3 MB (10328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87489376679a5203e3ab7ef55aee11e2afe985b463eeb9a18d7dd7dc1acd1528`  
		Last Modified: Tue, 16 Dec 2025 00:25:39 GMT  
		Size: 28.2 KB (28213 bytes)  
		MIME: application/vnd.in-toto+json
