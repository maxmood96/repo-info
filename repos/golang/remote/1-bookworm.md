## `golang:1-bookworm`

```console
$ docker pull golang@sha256:4f4ab2c90005e7e63cb631f0b4427f05422f241622ee3ec4727cc5febbf83e34
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
$ docker pull golang@sha256:b6c3f6b2881231dda32428740ea934e556614756b76a6c23129c9d85c3af4630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296592205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2971390d7d1f7152af2166d5ce07dfd2a0e0b2bfc51fb3ad0c96601d70c9e2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:45 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:45 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:45 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:49 GMT
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
	-	`sha256:d3aff15aaed783f017605a6a42a5619b0de3f3d0a969df33d7befbb844d0e587`  
		Last Modified: Tue, 07 Apr 2026 21:14:14 GMT  
		Size: 92.4 MB (92448442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55da06e3b41084804b2e5dbba71d35d26478b19ba8055d07a393cae22e9935f`  
		Last Modified: Tue, 07 Apr 2026 21:13:57 GMT  
		Size: 67.2 MB (67220501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c760900a35f7d88578d25b81f348039d48875448eb74ac8b25d9d31aa2b06b59`  
		Last Modified: Tue, 07 Apr 2026 21:14:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d1eabdf7e64c6128757d18dc58409f6ba545a4bc4ae5563a84dbd7b4f6eba8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e213f3c410a6a5e0f31ff54bdf9f5668f095943682f74d66d536288224fddfc`

```dockerfile
```

-	Layers:
	-	`sha256:31ee5675a86a0154942a2539856e1a14286ab40c45187e834d75ba0bf1f13664`  
		Last Modified: Tue, 07 Apr 2026 21:14:12 GMT  
		Size: 10.5 MB (10497855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff78b3bf17d2eac7eaa15079ce256f72939ce6f1b13ed66dca50aab4110f737`  
		Last Modified: Tue, 07 Apr 2026 21:14:11 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:f2404b0e035f83fa6a5aae13f67afb3be4d83887b760c7c002a98beb87985c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257858352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365bfa59dc69e0c53ec599c3cb8bae28c57b7ac108e8aa21d18ea58eda53fd65`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:14:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:14:17 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:14:17 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:14:17 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:14:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:14:17 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:14:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:14:19 GMT
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
	-	`sha256:f65fa475f9d3e3629b590feb8cdb218c955fbd92b48a8a248440a48f3e43d2a3`  
		Last Modified: Tue, 07 Apr 2026 21:14:43 GMT  
		Size: 66.3 MB (66305504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c0c93980268a0e43ceabcbfa19841d8859d03f3623b4521a7ead3d6e1badd`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 65.8 MB (65750977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a4b59d67099dded1ec1b076e002cb27730f49cf6bd0de1caf24ea5a50a1e2`  
		Last Modified: Tue, 07 Apr 2026 21:14:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:940613d7cce09557ff93932da44ac86c35ff23a2597b93c35d5b769d0be02ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b259b368031f9b33e55145489ff18f1bf4eeaf1468559a9194699460ce80f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:dde94393e908ddbd7826f08ba359c5686b1b16ddb6efb9e99b80fb2319c00f01`  
		Last Modified: Tue, 07 Apr 2026 21:14:41 GMT  
		Size: 10.3 MB (10304567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e5da61303b7f4a29e70b9c526a7118741cf0dba936ce37a62b9e493b568f79`  
		Last Modified: Tue, 07 Apr 2026 21:14:40 GMT  
		Size: 27.9 KB (27903 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2cb42a842776ee83f139d8cd9585b373df769dd014e6d939ab97c9a07e230972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287087434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0257d841f2b8d687bfbcfddf8a17474a78efe88fbb38c56aecc661946edf4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:52:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:13:47 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:47 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:47 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:47 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:51 GMT
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
	-	`sha256:f079040759ad389a9c4b8b7a680f8dd44b7f4faefabaf2f9afe811eb13752fdd`  
		Last Modified: Tue, 07 Apr 2026 21:14:16 GMT  
		Size: 86.5 MB (86521043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e89efc4b5ec39fa30d639b12ad2c7fd994a11ffa608e77427a882d73768d76`  
		Last Modified: Tue, 07 Apr 2026 21:13:44 GMT  
		Size: 64.1 MB (64108758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f0adc5040562e36aca5ed9a21530d16385b311b09ddb004a0aacb5c97845cc`  
		Last Modified: Tue, 07 Apr 2026 21:14:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:064ff3f1f682def02101d6ac6d317be288ba3fa35cbd5b75545e5f3af3e9978c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5182feb8433bc6d157044585fde3890403dbaa5bce147aba01b56e4558b430f6`

```dockerfile
```

-	Layers:
	-	`sha256:d70e74aba21c2eb2f9f57ed4a001c583486b3ccf4cdf11c63d37eae12ae608d5`  
		Last Modified: Tue, 07 Apr 2026 21:14:14 GMT  
		Size: 10.5 MB (10525703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c097b199a99c75bdf68ca70dd182fe1db4313778dfad58ba5c495b7d64c7c8`  
		Last Modified: Tue, 07 Apr 2026 21:14:14 GMT  
		Size: 27.9 KB (27931 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:13a2d2901ef116a1826f3b7a0af95c3ab1137c463da818f15e3ccb4c37108a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295997294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0768de6a7494729095bf31f485c3b8797535c4b73cdc5307d9b2b2c690ec4ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 21:14:20 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:14:20 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:14:20 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:14:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:14:20 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:14:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:14:23 GMT
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
	-	`sha256:f36a2fba98b5d4602eba06d5c9ae526b36d29c581da8bc4bf5327151375fb233`  
		Last Modified: Tue, 07 Apr 2026 21:14:48 GMT  
		Size: 89.9 MB (89871032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469b29d109e367ac43f3e67c104c046d01b1c6cca80443b728b2d38a262b476`  
		Last Modified: Tue, 07 Apr 2026 21:14:00 GMT  
		Size: 65.5 MB (65541767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23121523c93703f2d6d0add85c1173646da57805b3f6d99b27f0582c58d884f2`  
		Last Modified: Tue, 07 Apr 2026 21:14:45 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e7f39291d952b317256e9644b9f645cd5f708fe6867586dedf59421929520007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10505186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee5b8123e04b3ea311e43193326e19f10decf2a95258aaab8c102f6309d8e04`

```dockerfile
```

-	Layers:
	-	`sha256:12c2b2bddf6637dae7931f30cd1d89a2ef25030f9c7300e95a78c7bb54fbb2c8`  
		Last Modified: Tue, 07 Apr 2026 21:14:46 GMT  
		Size: 10.5 MB (10477425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d231db730dd539b9ec4a7395ff80d0e2dc61dd9ccd76bfc231856b3f3bd5354a`  
		Last Modified: Tue, 07 Apr 2026 21:14:45 GMT  
		Size: 27.8 KB (27761 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:a8205d7d2a153a05839976000443d2667eb3d448f791255b3d2a2add544683b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268571916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a301918e35bc51d251d0cd847fd6c19dd1898f70ef8d21751e2f08606be6895`
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
# Tue, 07 Apr 2026 21:52:37 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:52:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:52:37 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:52:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:52:37 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:52:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:52:55 GMT
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
	-	`sha256:2761ec4e39d2251614e6a8f784579a6abcc9088c78049bb387bdbdc174c5c65a`  
		Last Modified: Tue, 07 Apr 2026 21:54:44 GMT  
		Size: 62.8 MB (62812610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b7180d71d7717b7badb01ce50a8ca98509d26f923a67737dfcc881894c36e`  
		Last Modified: Tue, 07 Apr 2026 21:54:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:cced6c538cb0b5add2ed6084fd5b96c429b0128b21c374a3a74122529242aa12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c04b7503d139369845003ddc25120eede80a61dba3c5d4a3511561458456970`

```dockerfile
```

-	Layers:
	-	`sha256:351a5398ff0468004879b4430fd88332d8d52fbfa2b0ab7520271521d3acd558`  
		Last Modified: Tue, 07 Apr 2026 21:54:31 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:fce88cc79da2fbf9302f0cd45bc8bb30d4af5528cec08bdf2e8fd19c40aac54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303074977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47004c49e787772038229cf08cfb6c2c29e92ef7172d5aa871ed01b417eaa1e3`
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
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:27:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:27:19 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:27:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:27:31 GMT
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
	-	`sha256:15fa701b604ea6f9fea3ed6559e2106d2a891e54c2977fbb8bdbf9d75d69aa40`  
		Last Modified: Tue, 07 Apr 2026 21:28:13 GMT  
		Size: 64.8 MB (64757766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cbc4b619270365eb0f88245c5bc454a1698d90a693a24aa22e7e3d17b88d69`  
		Last Modified: Tue, 07 Apr 2026 21:28:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:588dbf7e31237a0c1893f6cf308e005dae3e2ad4ebecd5ec0c786e4c0bfb73e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651f6163ead0c08fa6c0962d3cb66f5a1bd2fac6360307b488205432b0dffa2f`

```dockerfile
```

-	Layers:
	-	`sha256:55edad0fd44e820eb4ad666f4b27915acf4de5dda14791a185e87d6c03ad3e1a`  
		Last Modified: Tue, 07 Apr 2026 21:28:12 GMT  
		Size: 10.5 MB (10470352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68c495c40504b9a4e1fad4764249c41c22b777ef91593f0cfc45f616f4ee1998`  
		Last Modified: Tue, 07 Apr 2026 21:28:11 GMT  
		Size: 27.7 KB (27671 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:c6e1f32cc130614fbcd119bd2e5d0d076ffbb13731bf8f1b3b960dca40a13e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270170667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7eac1d5b9fc4f429e38f2da2990ad867c30bf1a6f446dbdae682cf18477b9da`
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
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:11 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:25 GMT
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
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8449dd569f9d47940d400882d770806e983a90a9706bb0f40cdbe6109fbf7794`  
		Last Modified: Tue, 07 Apr 2026 21:15:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:bed31aea3a3b0944c5d09bbe325975fd164e83153e9a7a4de86faaeffe433203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3af5309c5f5a46e453febcf278c5387fdd9374b4db5b3cf6b27ed4ad199bee`

```dockerfile
```

-	Layers:
	-	`sha256:ad0e129031642ca24669d403df1a5acb0c5b761416f47992466e359711f9a8bc`  
		Last Modified: Tue, 07 Apr 2026 21:15:46 GMT  
		Size: 10.3 MB (10329613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8833ca314d729e27cb163c44d7005716c9c67f48db4028c376920ff30013e6`  
		Last Modified: Tue, 07 Apr 2026 21:15:40 GMT  
		Size: 27.8 KB (27797 bytes)  
		MIME: application/vnd.in-toto+json
