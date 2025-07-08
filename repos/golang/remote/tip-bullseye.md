## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:3424961064ed365d002343e4cc870e1af19fadf1c6c3bafad75dbb69eb9d5760
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:79e1e6fbca7a2a1257e0ce9b9b1a047b1235a058e0664a222e7b36951525971b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 MB (293385921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39846d3744e06e16b233ed7f0b7f2d988f442882423a0c4e857a7e9caf932a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75446e4c47db0ab749c0fb25ec297ecfc2126c0e2919a6321ab9607fe3b74956`  
		Last Modified: Mon, 07 Jul 2025 21:08:02 GMT  
		Size: 86.0 MB (86021998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9b1bf1df4ddb6cd2f3ba43fc263309f8c370fe86f15d3de62305a26c4885e3`  
		Last Modified: Mon, 07 Jul 2025 21:08:01 GMT  
		Size: 83.1 MB (83086126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a096ce24627a6cbf6e92a958a9bdd51c75f8432f58e47d1c452b6b8fdc78554`  
		Last Modified: Mon, 07 Jul 2025 21:07:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f532105238435c63e150a577d4d2a2bacdf2fa1d5841b8ababda2037db0e964d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10509220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4adffbb15485a5fcab5affb3fa1238c2575274b118b04c588d4f5396645c988b`

```dockerfile
```

-	Layers:
	-	`sha256:1b27463fd4dffdc5a16793c8d30f70ed93d6154bf19a536df6a0df46ec9d59f3`  
		Last Modified: Mon, 07 Jul 2025 23:24:40 GMT  
		Size: 10.5 MB (10482164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b96247038a4658136b73778c5b9aab10272216b34c9edc51d0f415758c020b`  
		Last Modified: Mon, 07 Jul 2025 23:24:41 GMT  
		Size: 27.1 KB (27056 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:24ba9facc725de532d4f8e042bc7319ade8583e3957cdc6d838196b605e9ea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259679611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce39f6d20fa1b5af240590ae6f3a916c62f07e5c872b3d4b62136dfbde60e9a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:efcf40eae0046ccd92d3b47ff685e1e9cf7a34d0a92f6de893078f115e01f20f`  
		Last Modified: Tue, 01 Jul 2025 01:15:14 GMT  
		Size: 49.0 MB (49043960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6769ed354ec7fde57e63bdf9788543b96fd8f93923607ad70767b9c4cfa25b`  
		Last Modified: Tue, 01 Jul 2025 08:59:49 GMT  
		Size: 14.9 MB (14880774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28365fa3b8363bfd29e20b4b17838c65ddc4bdacb1bf15ca9af5a4045e4feaf7`  
		Last Modified: Tue, 01 Jul 2025 18:29:48 GMT  
		Size: 50.6 MB (50631320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab1ca88e5570437d1ef4898470342c64b77544a6b09526ec16705c6fa2517de`  
		Last Modified: Tue, 01 Jul 2025 21:46:43 GMT  
		Size: 64.9 MB (64942320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69fdb869efc0a02a2300329eae27592000268e157c8997d8c67d1e2518080e9`  
		Last Modified: Mon, 07 Jul 2025 22:02:14 GMT  
		Size: 80.2 MB (80181079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888c0d503ce22c081a2efcf231e7d261512923c22d161176f9fd39a103d68560`  
		Last Modified: Mon, 07 Jul 2025 22:07:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:bd028b003e3ffb482a364bdaba1ad085aac39a6f18f5c7268553817532daa79e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10314538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bfe86af94292ee0eeb73ce533753983eb4753e3ca24c5d4bdd9e79e9d0d1bf`

```dockerfile
```

-	Layers:
	-	`sha256:319b744799919969b6bbded15ea5d68849180136d90d4653e48b1761922456b5`  
		Last Modified: Mon, 07 Jul 2025 23:24:49 GMT  
		Size: 10.3 MB (10287373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca63607b4dd2ac7acc5ffbb140755fb620d4d08c11b307958f913a409c18864`  
		Last Modified: Mon, 07 Jul 2025 23:24:50 GMT  
		Size: 27.2 KB (27165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:081eaa09f039f7d86ecd5034ea92cc2648bd4316de53450bcd7c68c2aa45c06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283342602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b42991f2a57599c0c6337335c37b2d23e73f32102f96ed6e37e3a984685eeb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424250d141bf5f4ec62e698bba9b5695482a3015186d3b14a633da8916bf7dd`  
		Last Modified: Tue, 01 Jul 2025 06:52:24 GMT  
		Size: 15.8 MB (15750716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7766ba090abb327ecb7e9e14ac90bbcc45c5ba6bb8a568ae531c960ff1acad55`  
		Last Modified: Tue, 01 Jul 2025 13:29:45 GMT  
		Size: 54.9 MB (54855722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39156e06be16dad65f82953c32059d1fc94868a93fcb4e5eb5ce8ef6e583ce3f`  
		Last Modified: Tue, 08 Jul 2025 04:44:47 GMT  
		Size: 81.4 MB (81432556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93fe74c58f17b8638ab4c828f8d4b865821c43447e64c8cd4bfbde5a810c7b1`  
		Last Modified: Tue, 08 Jul 2025 05:43:08 GMT  
		Size: 79.1 MB (79051196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d063eb9f9b9b03b69ab017ebb570da3055edb79cd493ad9f93ddc6bb5174226`  
		Last Modified: Tue, 08 Jul 2025 04:44:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ebb367747f12c6bf7e511e55a8dde8abc11507de5a59ddd83aac931180577f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbabddce510faa35a26e29858583ff7068f37ec29ff781b6aa8aa93d23b201f`

```dockerfile
```

-	Layers:
	-	`sha256:dbfb6030d9f520abe28495f72caef7e9959dbc8186b7dfb1b6d41438247973f3`  
		Last Modified: Tue, 08 Jul 2025 05:24:06 GMT  
		Size: 10.5 MB (10483447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cd9c1e8eac4816b50a4a0af394efc86d42889f2741d4b874a05e85d3c1e86f`  
		Last Modified: Tue, 08 Jul 2025 05:24:07 GMT  
		Size: 27.2 KB (27193 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:ff3df3d6b7732893bec587cfba499138314cf3f5f7355421c19bd48be75126cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296277374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e69e2ce4bd3af30ba9ef78d7f3a7a4114479c7cce731ea9f436e7ddba8c767`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05b439f6df174e28bd21dc59eead603def3bcbd47ec6462f86b7758c4db6ef`  
		Last Modified: Tue, 01 Jul 2025 03:19:57 GMT  
		Size: 56.0 MB (56049937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e417711838740b28baf6073f35d2f31cce4a37e51600e6fd9dfc46b1813ea96d`  
		Last Modified: Mon, 07 Jul 2025 21:08:58 GMT  
		Size: 87.4 MB (87448060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fd65ade23887bad8cc24159556378a6549464832612b1c87e5e65754cc9685`  
		Last Modified: Mon, 07 Jul 2025 21:08:46 GMT  
		Size: 81.8 MB (81820379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f187c968c86b8a8b4970b0300af48b23359a92c7c5247b458796e5279c4058e`  
		Last Modified: Mon, 07 Jul 2025 21:08:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:6dd5e77d8c6ec60f552cbe30c3881aac583289be4fef07ea6c3e41a5733767d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c626c24db0bee70cf433cafa925f0771ebda2498d1e6ae91dd5491674f7f09`

```dockerfile
```

-	Layers:
	-	`sha256:f1cfdcc364f7de45db1b56bdf79d19e9721a87b4147688e2b86e88058861673c`  
		Last Modified: Mon, 07 Jul 2025 23:24:57 GMT  
		Size: 10.5 MB (10471501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f67bc0c0b51281ef359385c6ac1102ab875fa4d366d64787695c7d30c8a30b5`  
		Last Modified: Mon, 07 Jul 2025 23:24:58 GMT  
		Size: 27.0 KB (27023 bytes)  
		MIME: application/vnd.in-toto+json
