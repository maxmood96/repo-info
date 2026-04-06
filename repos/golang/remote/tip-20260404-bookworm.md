## `golang:tip-20260404-bookworm`

```console
$ docker pull golang@sha256:53a896b13a1d0c0065c04a96c268142d6c5573e52eb64bd3d3ee14d615cb633f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `golang:tip-20260404-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:62580a4f86704d248b062bd2fd260b18d70ea00a3b21bb87743c9d1f5d779783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323371542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b295cc4880bd7ec85f3a644ecfe1e53242a6eb79fc1a6b322217a4be2d57ecb1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 18:42:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 18:41:03 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:41:03 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:41:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:41:03 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:43:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:43:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6327e9716e6200837b08ca81753fabe770de7331917525fe1b7aa028ce848ae`  
		Last Modified: Mon, 06 Apr 2026 18:44:17 GMT  
		Size: 92.4 MB (92448562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8966583daebf02f7188b966cc8cfaaff27cf5fc1ff9b30af37d939f77e22335f`  
		Last Modified: Mon, 06 Apr 2026 18:41:36 GMT  
		Size: 94.0 MB (94000413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33258eb15bec11785a6c25adb963e347c9ac59e616559eb87262bf3a759f1282`  
		Last Modified: Mon, 06 Apr 2026 18:44:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260404-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:df61c3981dda7f81d5c62303de590c36f25c542212d4e4fcffcd44254e4697a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241f5ae0ba8285c7900e895fb95af21f61f7688426bb763545ea735c59c94be6`

```dockerfile
```

-	Layers:
	-	`sha256:a3740df5dbc9d83b911f022f50bfaf511ac3740fbbec10a3d72d4c97ebe75438`  
		Last Modified: Mon, 06 Apr 2026 18:44:15 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b019eca77287986a93b7920c53cfb20f93facb84d0aad17ccc898e8d78f26ad`  
		Last Modified: Mon, 06 Apr 2026 18:44:15 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260404-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:6671e060b2cfebf4258a278a85f1ac9dc821e942586c3b45dde019542e0f2d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282244026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923ac821635c531644c91a6e5196bb164502c31b3089e82c1c579b54873a2da9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:51:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 18:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 18:42:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:42:36 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:42:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:42:36 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:42:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:42:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c259f98025fcc3d44333815b426fe9bea34608d38b537248297aff1482d389`  
		Last Modified: Tue, 17 Mar 2026 00:51:25 GMT  
		Size: 59.7 MB (59652088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f2ec18a80b6fe93cf840e8c6f60c977c90d43a523b08aabfbff2138554688d`  
		Last Modified: Mon, 06 Apr 2026 18:43:04 GMT  
		Size: 66.3 MB (66305448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866705b29d2f18b79748f9fadfbe79c21fa37d231a94fa79b6aae3edf75ac398`  
		Last Modified: Mon, 06 Apr 2026 18:42:37 GMT  
		Size: 90.1 MB (90136708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a84d56dc3da3652921e358dc3a9a16b7d619530958ff8f0336cce750cb09a81`  
		Last Modified: Mon, 06 Apr 2026 18:43:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260404-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:cb786e8da17e0eeada14ae8cd5a6c26fc11244271454cd8fe404de72869af39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7621f30bd372cc4f10b3a8486236781ac71b40a59ef0422cbc345a3791099887`

```dockerfile
```

-	Layers:
	-	`sha256:44b72ce3151c18d30775e57787fe30989ae256536d16fd8a4e9474f77470f7fd`  
		Last Modified: Mon, 06 Apr 2026 18:43:02 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66895f6b18c5b3431e9a1f888d8ed28085af703475a5de47f44ec955d7e1045c`  
		Last Modified: Mon, 06 Apr 2026 18:43:01 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260404-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c5fbbc8bc14c925fff9ab8c46641a5f442e31a9085750277cf776abcec55ec53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312063714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177ce1fff33d229bbd2985e38ba4625037556ff737f162a5e74c0e9f9c06c578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 18:42:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 18:43:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:43:40 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:43:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:43:40 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:43:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:43:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca783ea1337def56452574549c57e59bfd0b96dbdf0e602fbe9cc8bad73fca1a`  
		Last Modified: Mon, 06 Apr 2026 18:44:10 GMT  
		Size: 86.5 MB (86521426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ffa2ba5933aea1f1c364c6a791a91c9e49057e35639f30985503d0547a7466`  
		Last Modified: Mon, 06 Apr 2026 18:41:04 GMT  
		Size: 89.1 MB (89084955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb2110b9d17b1ff57ec62eee1697e3c996d7ce6f111ce63a43fed893ceb3eb7`  
		Last Modified: Mon, 06 Apr 2026 18:44:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260404-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4e02dbea1071ac60604dfaae8bd5b90af4d6f6829cfe1734d81a360041fe6dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1414e511b29fc528d90e7c7d826227dc2828c2891bee604b65e44345658a3b4`

```dockerfile
```

-	Layers:
	-	`sha256:85fc3bfd730577e039c60651cfdac791df622dbaf1e6b43111c2555600e23d7c`  
		Last Modified: Mon, 06 Apr 2026 18:44:07 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dceca035af6862ca8a664aaea7e904b4cfdef80e8404c115d0024b3dbd37e438`  
		Last Modified: Mon, 06 Apr 2026 18:44:06 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260404-bookworm` - linux; 386

```console
$ docker pull golang@sha256:a721b5d4904a38e3eca06d19da3b8a27c99bc90a35e82f777dfb05a61a4300bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322297392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1f175093d28fe57c33ccd1a8da9f42da3d6c79bf75d34d6513a2ab578879ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:41:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 18:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Apr 2026 18:42:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 06 Apr 2026 18:42:07 GMT
ENV GOPATH=/go
# Mon, 06 Apr 2026 18:42:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:42:07 GMT
COPY /target/ / # buildkit
# Mon, 06 Apr 2026 18:42:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 06 Apr 2026 18:42:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7cf39578e27046e7ba7fa5d4d45df198790a004a9eb86583e977b3b055c88`  
		Last Modified: Mon, 16 Mar 2026 22:43:53 GMT  
		Size: 24.9 MB (24871994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9d2da3801adad27eefa73bb7b5ab6c0c94f46583823a923caa8e9b995a97b`  
		Last Modified: Mon, 16 Mar 2026 23:41:39 GMT  
		Size: 66.2 MB (66234305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735a3866235440c99400aa2e71bbb38cd2e333e68f8cce52cc33624044d2a94b`  
		Last Modified: Mon, 06 Apr 2026 18:42:36 GMT  
		Size: 89.9 MB (89871514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434b82e2680f4d14426f015346712b6e5f30c486655039ad7e1ec71d21151434`  
		Last Modified: Mon, 06 Apr 2026 18:41:48 GMT  
		Size: 91.8 MB (91841768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0809f85429130468da8f20993e5f49f45e7982c49baa24245d17d8c049af43`  
		Last Modified: Mon, 06 Apr 2026 18:42:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260404-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:249fea99d7979dc549f154d2970ff942ed8cfd9b45813d4e8c83584d1e28744f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954176be203e190d2eafc923994cc8b52887f08ed3ac94c023ed92852b68c9a1`

```dockerfile
```

-	Layers:
	-	`sha256:bbaa266bed4442c241016041f59841fca60253c3669af007fe529dd0a3043ae6`  
		Last Modified: Mon, 06 Apr 2026 18:42:33 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cb24b4eb3aa34ee2dc22505f6fcec52cf5289eeced3abb73583e6031378fbdb`  
		Last Modified: Mon, 06 Apr 2026 18:42:32 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260404-bookworm` - linux; mips64le

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

### `golang:tip-20260404-bookworm` - unknown; unknown

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

### `golang:tip-20260404-bookworm` - linux; ppc64le

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

### `golang:tip-20260404-bookworm` - unknown; unknown

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
