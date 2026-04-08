## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:c3432cc7819f6ab40121a53538edc1203018aca33db60f908e0669749d009218
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
$ docker pull golang@sha256:cba1dba63289e5001cad79434e6c03d7aec78d34a34a26041793406adbe9f8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323372057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7578b23d6ec6b2eff3a9098b40eac1a2539520b8f3e4f98e75d05b5e64533a0e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:59:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 22:01:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 22:01:49 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 22:01:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 22:01:49 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:01:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:01:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73ef470b7b271fede6f98a4c8376971bd059ce04ebc13b9f86e34e534b89ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:01 GMT  
		Size: 64.4 MB (64396012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13c162d89168989cfd4feaf2746e6ad97afd2de7541b7f0464e1928bf618762`  
		Last Modified: Tue, 07 Apr 2026 22:02:18 GMT  
		Size: 92.4 MB (92448381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8966583daebf02f7188b966cc8cfaaff27cf5fc1ff9b30af37d939f77e22335f`  
		Last Modified: Mon, 06 Apr 2026 18:41:36 GMT  
		Size: 94.0 MB (94000413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb6bf23e31d781542afe5b2003d6f722aa76a549fee87b8b94fa64005174bb7`  
		Last Modified: Tue, 07 Apr 2026 22:02:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:91213e4b1d906ef300aafabe51ce183a1445ff34f752c8b04dc962df222ac3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5e662ce51aa1d06f00c5e47069ea1b844a40abdd307b38953f571890027fb5`

```dockerfile
```

-	Layers:
	-	`sha256:6bb538619b1e85288136ea3b205f27477cbbfdeff81f99cb21268eda1fc12b80`  
		Last Modified: Tue, 07 Apr 2026 22:02:17 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2592f9c87b499ab3a15000de15efcdd18062dc2e15494d3298367a3d99c241`  
		Last Modified: Tue, 07 Apr 2026 22:02:16 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:bfd54ebd5dd3e6ed70fc531d44864bc5b384b64d3785d2bc52bf796a8a3aca45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282244087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9516c907b7285ad42ad87ffc5c8633e7f539e1cfc6efe86b5ccc7a2b0a65d0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 22:00:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 22:03:30 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 22:03:30 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 22:03:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 22:03:30 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:03:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:03:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626437a99246a6d3dc330350016eb9ecbf357123cec9028fd988893fdf863224`  
		Last Modified: Tue, 07 Apr 2026 03:49:22 GMT  
		Size: 59.7 MB (59651814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7febd4c09ebf2f5c4e266befe71222e5dd6a65adf7ccd1d214b5d9666ebf4530`  
		Last Modified: Tue, 07 Apr 2026 22:03:57 GMT  
		Size: 66.3 MB (66305506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866705b29d2f18b79748f9fadfbe79c21fa37d231a94fa79b6aae3edf75ac398`  
		Last Modified: Mon, 06 Apr 2026 18:42:37 GMT  
		Size: 90.1 MB (90136708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9881f593e1088cda4141cc0e19887a971217b0d06c53bb3f7f4629a8516e67`  
		Last Modified: Tue, 07 Apr 2026 22:03:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:46da510117f3ea07afc29a542d8e23530bf9a2edf3e9657bbd05af9c59ee5537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90e0003458b121378fa67db1dabe76af6f7864fc91c509213788e25cd6ccf05`

```dockerfile
```

-	Layers:
	-	`sha256:96c7dedca3482fa6d024b7820c6a608d96e6a65a4fc78c56bae0c7e5c0d4ba12`  
		Last Modified: Tue, 07 Apr 2026 22:03:56 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827a12328bcf2de4b337e33ba9aca43c4c96754996aeaa040974c58061468300`  
		Last Modified: Tue, 07 Apr 2026 22:03:55 GMT  
		Size: 28.5 KB (28496 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a0e7442456f317ebb2603f9582f59f3efbc44a40a9a59be7f0b339f252bfe245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312063525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4e78d8f0ced3c8e7bbabc0363238a2b3e0896b221e0b2c2677b5dd9e930b23`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:52:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 22:00:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:59:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:59:45 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:59:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:59:45 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:02:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:02:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b913dee6e116304b9bb2391ef8aedbb1f5ee16d167338920c7609a48bdd772`  
		Last Modified: Tue, 07 Apr 2026 02:53:06 GMT  
		Size: 64.5 MB (64479508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d56f7adeb1395b83160ae3101db64ec19177ec80f787f9febabb5eed86bbc9`  
		Last Modified: Tue, 07 Apr 2026 22:02:47 GMT  
		Size: 86.5 MB (86520937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ffa2ba5933aea1f1c364c6a791a91c9e49057e35639f30985503d0547a7466`  
		Last Modified: Mon, 06 Apr 2026 18:41:04 GMT  
		Size: 89.1 MB (89084955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787048edde924b447ff990aec247a75f5277a25ec3a6063b0341e43dc838fec4`  
		Last Modified: Tue, 07 Apr 2026 22:02:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1ccb9a6b1637463114789f126ebf089a82252f449b85c0c9382641c704fa0f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f55ad2bdb60f25517d2fc3b1387a2de0cab3617adb003e3ddd59ef6a103fdd`

```dockerfile
```

-	Layers:
	-	`sha256:e4fdafc8735cb985c936c2d7289816bd5a431077e6f7f2beb2b84df463def3ab`  
		Last Modified: Tue, 07 Apr 2026 22:02:45 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5108a39145406101bc7d92b36c4696d37c66d11815b974965d4319ff2721be20`  
		Last Modified: Tue, 07 Apr 2026 22:02:45 GMT  
		Size: 28.5 KB (28521 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:497f5d006c330ad7f75ea800b2b45d107513d2286a5464ff12f5ba3f5ff053da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322297353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf768a7e0e33b60fa5f19a364ae0c33def8cd0cfc59826274ed6a37c07d25fb9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 22:00:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 22:02:33 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 22:02:33 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 22:02:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 22:02:33 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:02:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:02:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240fa1f3927770a46d24419f7704239ba70e841afdde2d9e2629af344b11c262`  
		Last Modified: Tue, 07 Apr 2026 01:45:49 GMT  
		Size: 24.9 MB (24871973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fefd2d4d18c0e4a1f706c31af7edb1bb87765de90f366b612fc4f713dbbfa`  
		Last Modified: Tue, 07 Apr 2026 02:40:53 GMT  
		Size: 66.2 MB (66234451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6881864be0606afb33fecc6d6314b9a37dece7458fbd09fbe022e325dd746f`  
		Last Modified: Tue, 07 Apr 2026 22:03:01 GMT  
		Size: 89.9 MB (89871089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434b82e2680f4d14426f015346712b6e5f30c486655039ad7e1ec71d21151434`  
		Last Modified: Mon, 06 Apr 2026 18:41:48 GMT  
		Size: 91.8 MB (91841768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668f966277ea4e06658b286fbe6dc87c3bdc89571935fa6afb72aaeb996347f4`  
		Last Modified: Tue, 07 Apr 2026 22:02:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b0a32578779a54138b123e9782369f95e1c5f3178487071ac79f8133741fb50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a2abb17bb017ba948501e7345501cd8851d5e1a8ab45a932af26c2eb812999`

```dockerfile
```

-	Layers:
	-	`sha256:df93e9e40e725d706e31c830dc40d0881e74002eae7e587397fce71b47006a02`  
		Last Modified: Tue, 07 Apr 2026 22:02:59 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e00853f2c37aa01b1710810f4bc00e21428756dd7ddb1d342b742fff80e8052`  
		Last Modified: Tue, 07 Apr 2026 22:02:58 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:e899ecdab3e895cac442499199d1bf2c517b343b9d8cef6b8e90f0e6631e92bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293573579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80ee49cb9c452c8f9792fb5926d3e4383cb038e524514c5d626a8cd6c98634f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 15:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 20:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:52:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 23:26:30 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 23:26:30 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 23:26:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 23:26:30 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 23:26:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 23:26:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7a9b4a7963b008240d9a254ca4fd1193c938bed0a9c6fe9c04630f13b1a17a44`  
		Last Modified: Tue, 07 Apr 2026 00:09:37 GMT  
		Size: 48.8 MB (48782593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5370b42611bdad35bb24b3e5a6a342f00eb8523dc8562b7babeca6f19608f4c`  
		Last Modified: Tue, 07 Apr 2026 15:01:37 GMT  
		Size: 23.6 MB (23615262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df968e8deea10f7e740272ffa34126abe9d9673e41bbeb7f3f0d785055e19a4d`  
		Last Modified: Tue, 07 Apr 2026 20:28:18 GMT  
		Size: 63.3 MB (63310060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cf83c0e933a4e8a498aae736ebf10a823fd9ecc755d47233e566e941c9893a`  
		Last Modified: Tue, 07 Apr 2026 21:54:45 GMT  
		Size: 70.1 MB (70051233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a49cc002fd649c9bd83c36080a1bf497581aea867afaf3dfe1eba57717afaac`  
		Last Modified: Mon, 06 Apr 2026 19:02:59 GMT  
		Size: 87.8 MB (87814272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3fdc0ccd7e055cda54177b4f6a0a1dff2e1d6c59b1e8b68282d55a87e7fae1`  
		Last Modified: Tue, 07 Apr 2026 23:28:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:385da35f5e06b941fb256b93a4544b4a8935eef21c7d23a8496ed8a146e6ecd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bba549af06eb6130755cd29d62c68a1384d23bd7e3d94930bdd93323d1de818`

```dockerfile
```

-	Layers:
	-	`sha256:fd1f4ef311bf59b72019d92a611ffb99978a20f1929045944221f61fa0f5191a`  
		Last Modified: Tue, 07 Apr 2026 23:28:37 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:89ae1a658f52af1bfe654fa1351695f50f9aa40510881fd4170a973faf11ced0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329120006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454ad8b0bcbd7a0bec192ab2d6ecf94dafd9b3cb8e141fbd7302b6180150a542`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:21:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:50:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 18:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Apr 2026 02:35:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 08 Apr 2026 02:35:44 GMT
ENV GOPATH=/go
# Wed, 08 Apr 2026 02:35:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 02:35:44 GMT
COPY /target/ / # buildkit
# Wed, 08 Apr 2026 02:35:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 08 Apr 2026 02:35:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a522a501745b6503b15f6badc6170d6fa2321f26576c47b363acd8cb21b2ee`  
		Last Modified: Tue, 07 Apr 2026 04:21:54 GMT  
		Size: 25.7 MB (25671577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f98ce990098f8650217504a159d9031cc264dd29e8af85f749d78eacc319c5a`  
		Last Modified: Tue, 07 Apr 2026 09:51:25 GMT  
		Size: 69.8 MB (69846122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f67f0a7bc2638109117ec62f84bf4d06b91348ec6d8486011aaadaa5f42f65`  
		Last Modified: Tue, 07 Apr 2026 18:22:57 GMT  
		Size: 90.5 MB (90462415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc368d4f4523089f91977c543e8d1f1e4d28e3b0d524ab4ee1d1ce21debe4d`  
		Last Modified: Mon, 06 Apr 2026 18:58:20 GMT  
		Size: 90.8 MB (90802796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab224ff2f119cda447a60ca436e290848a2a172cbdc0cd8f9f14c41b4531efb0`  
		Last Modified: Wed, 08 Apr 2026 02:36:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:804e2784d437405e17f120cbd0eed6b29982658ceeb1f4f153ae86e0790ecfb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfffa03e18a0a068496e0eb866b20247a84dcb177bb0228bd721599c07b4922a`

```dockerfile
```

-	Layers:
	-	`sha256:82a7bddc91991e109323afe7cd56cdb5186be41daf4273523b2bc72dfbd3c351`  
		Last Modified: Wed, 08 Apr 2026 02:36:39 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5c2bcb3347308206ef7fac9fa7a66111222c24cf66ce2474607c34071538d8`  
		Last Modified: Wed, 08 Apr 2026 02:36:38 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:168ba21abc5bc091805e28faf8c6abed37e0af2ec82d51999804f799fb115938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296921349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f716839dd95425551a53f7b9eaddb15318a145dc09d503b8060db0c64e294fe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:04:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:54:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 06:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 22:03:29 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 22:03:29 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 22:03:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 22:03:29 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 22:03:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 22:03:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47976b1872c5d8fc1ceda4d073087f195be5506b083608f5c0a6767f6b55978a`  
		Last Modified: Tue, 07 Apr 2026 03:04:32 GMT  
		Size: 24.0 MB (24033635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3377e46a7f95ad649f4e145572c4253ed3ebf1b9fa463b58c96cf8b20d651ac`  
		Last Modified: Tue, 07 Apr 2026 04:55:04 GMT  
		Size: 63.5 MB (63501358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7550815663570f840c3f2383dbf4c81d9f32d7c2cabee708665295a431772ce6`  
		Last Modified: Tue, 07 Apr 2026 06:02:24 GMT  
		Size: 69.1 MB (69055249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa7bb14b36d862c74817ebfb57b26695332f89670a6fc97f1c869402d1de33e`  
		Last Modified: Mon, 06 Apr 2026 20:04:12 GMT  
		Size: 93.2 MB (93182867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a35293ba1b613a0007252be6c570a3693b127c8b412c67eaaf6b689f6914608`  
		Last Modified: Tue, 07 Apr 2026 22:04:04 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1366120f2b85267f42c9a7011c70edb0500f0a977d4e1adc7d2fc9c05ccddfc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7891caeefedf37918cc9998ac2baeee006cc2736013eda78d8d43c5862cf29`

```dockerfile
```

-	Layers:
	-	`sha256:004192e15814e338434d86cc88b27be1194d5849979d76aaf8211213bc742640`  
		Last Modified: Tue, 07 Apr 2026 22:04:10 GMT  
		Size: 10.3 MB (10328791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4683fd25c77ec1915caa3e7830c4227b11436b1d81437d84c80850bb3b8bcc`  
		Last Modified: Tue, 07 Apr 2026 22:04:09 GMT  
		Size: 28.2 KB (28212 bytes)  
		MIME: application/vnd.in-toto+json
