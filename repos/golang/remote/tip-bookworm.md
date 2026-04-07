## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:da25a0fb4a10bb588e2b998bf14e0f424414e2a8b5950bff2fcd01ddc2bb40cd
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
$ docker pull golang@sha256:f141ae40621f289d119d06ffcf188de5539ed89865b84bf1917a70bbc6bbc86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293573124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d803cc01362488db9da635bc78ff171d21780fe3dfa4ba493a6452ec01b208`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 09:32:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 15:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 16:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 19:00:47 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 19:00:47 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 19:00:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 19:00:47 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 19:01:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 19:01:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:55bd01c42402ce77937fae9abfba9b351fd4b3fab7f1f58eccf5b2fcf0ac8978`  
		Last Modified: Mon, 16 Mar 2026 21:51:11 GMT  
		Size: 48.8 MB (48782288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a46874b19723e755d13ba2292477f479fd221937f5480b97990afd32f94b3d6`  
		Last Modified: Tue, 17 Mar 2026 09:32:54 GMT  
		Size: 23.6 MB (23615153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510757183cb1996fa93fc6110a5644d68f4a47cbb4c8f08c9a7376b57b6600e1`  
		Last Modified: Tue, 17 Mar 2026 15:10:46 GMT  
		Size: 63.3 MB (63310157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29a828b5f824da9f5aea9f29bedbcb4f1d9ba92baa7cf5754cbe01210a2d907`  
		Last Modified: Tue, 17 Mar 2026 16:31:43 GMT  
		Size: 70.1 MB (70051096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a49cc002fd649c9bd83c36080a1bf497581aea867afaf3dfe1eba57717afaac`  
		Last Modified: Mon, 06 Apr 2026 19:02:59 GMT  
		Size: 87.8 MB (87814272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ac612cf71a136c20fb183e4762a5235e80b70cd88c21ad115bb2798c8090ba`  
		Last Modified: Mon, 06 Apr 2026 19:02:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2fdc0c39794e6b2e37a21a47057faf48c57a1f4a146c02ca10ef683bff92ffe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc4208a58442e52f60a66644bc34435039e854209a403b46c18a7ffa71cab4b`

```dockerfile
```

-	Layers:
	-	`sha256:a89f7f794519e5cd00cfe6b54c725b14f85d317e3858909a32cba07901895d77`  
		Last Modified: Mon, 06 Apr 2026 19:02:50 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:cad67206430c85d980d4a5cb511aa3d77343a90f54b0b327903748fe9ebf51d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329120094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2f1bca908cbcb7b9240574b76a98618631588e1817fe8e9310d848508964d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 06:03:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:50:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 18:57:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:57:14 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:57:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:57:14 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:57:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:57:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6053003aae760c21f129e32066714b891ab6bc6ec6abdf0f13ff20cb85ede`  
		Last Modified: Tue, 17 Mar 2026 01:49:00 GMT  
		Size: 25.7 MB (25671576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc763fa93abbd05d9932abad5e62ea754d4d526450c9517c9e5b75b5c914969`  
		Last Modified: Tue, 17 Mar 2026 06:04:00 GMT  
		Size: 69.8 MB (69846151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa85d4ce5e832d1d4657e93cecd987718fa0d7c00ae8a0ce1f712b8250b7c0b`  
		Last Modified: Mon, 30 Mar 2026 17:51:17 GMT  
		Size: 90.5 MB (90462716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc368d4f4523089f91977c543e8d1f1e4d28e3b0d524ab4ee1d1ce21debe4d`  
		Last Modified: Mon, 06 Apr 2026 18:58:20 GMT  
		Size: 90.8 MB (90802796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ff7ba38b8e4228339491f7d985f097ef10187094e3d30f7d07a17ebe694b81`  
		Last Modified: Mon, 06 Apr 2026 18:58:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:92be87e6efe6faf85f6a74194b5d6aae4f7c8ebd5f7cdc5b8106e1416f88dfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6f81a9b72adbe13484964a41ad6731ff0e001724c2912d7965c7fd9bdc9072`

```dockerfile
```

-	Layers:
	-	`sha256:7b8f86547d6c15982cb4735486c7ac80968aec065b3c200c9e575467340b8a97`  
		Last Modified: Mon, 06 Apr 2026 18:58:33 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48350cab6d7637f5089acb3ac5225acdf4bb6263b4cebe62b4afdbafdcff80e8`  
		Last Modified: Mon, 06 Apr 2026 18:58:32 GMT  
		Size: 28.3 KB (28258 bytes)  
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
