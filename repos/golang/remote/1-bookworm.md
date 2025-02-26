## `golang:1-bookworm`

```console
$ docker pull golang@sha256:b970e6d47c09fdd34179acef5c4fecaf6410f0b597a759733b3cbea04b4e604a
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
$ docker pull golang@sha256:c95c2e62864701a6f5c2aaee76f2b68e5474e7a14f4c3aece5f6ff26a618d9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308066473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245780beb82f97496ad0dee2d70c6fd2bfa56adedb229a3e25c9e801dd262b5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9760da4e8f07741fae4c26020e61eb395607959e93d79f06d31fc27130f7f938`  
		Last Modified: Tue, 25 Feb 2025 04:17:30 GMT  
		Size: 92.3 MB (92331986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a60326dddc23e8774b39171d6496c16678bd44e52909e9a94763d62f3cbf89`  
		Last Modified: Wed, 12 Feb 2025 10:27:40 GMT  
		Size: 78.8 MB (78805485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8985a99e1ce35674006027d832983346299ede6596587b3c974723c0345c8b81`  
		Last Modified: Tue, 25 Feb 2025 04:17:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:707a19c625a9252eafa68b4cbea23189a056588993c660288ef228631d90a4b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10309771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2847abf26d10753aaa0f56d35c2eb3e147b581f72383f261cf7c0c0c67acd6f4`

```dockerfile
```

-	Layers:
	-	`sha256:384019955cc9811ff7b8a13b3d98cf7c0fd7c956ae42d80a41e7f5d1beb88c81`  
		Last Modified: Tue, 25 Feb 2025 04:17:28 GMT  
		Size: 10.3 MB (10282125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1cc47aa8b744276d0fe820861d053c125ad1413883c32b38123317806f06081`  
		Last Modified: Tue, 25 Feb 2025 04:17:27 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:5855825ca573649e48284fb86bade085cc32001bd6b3609ad27fb451cb7202df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268936239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f32ab5fec7782b5a1bc09805f9db45419050a649d809e537104e6f0d436c9bf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3654867856e71cf6e49b9c0cd4aa53b8135e92c7f0694dd70469ea7e9aef8a87`  
		Last Modified: Tue, 25 Feb 2025 17:00:54 GMT  
		Size: 66.2 MB (66187481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ff7ce8adbb73c193102166498a2962195641bfa6bbc14e5dfa44f02e4d7d0f`  
		Last Modified: Wed, 12 Feb 2025 17:45:53 GMT  
		Size: 77.0 MB (76968450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28b2d314d3c9bd29dfd2a70e4a88c7396d05566d50e6cb34eb5b2185d6a97c`  
		Last Modified: Tue, 25 Feb 2025 17:00:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5fccede323ff550e62fb9a1fece7798146f8a587b3411b2fea38c2809e6c4820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10118262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f99d79ac8f8a7980f70bf08ea5fdfa89a4cd5c6083a8f6d8f35655d08e2b2f`

```dockerfile
```

-	Layers:
	-	`sha256:c3190cd4391adbcb350cbc3562ec1f8adf12febf386edca61d19f11d7575e804`  
		Last Modified: Tue, 25 Feb 2025 17:00:52 GMT  
		Size: 10.1 MB (10090483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c67a202d9d610cf0f0b57f3daae5750042685933188b330403057d2ab61385`  
		Last Modified: Tue, 25 Feb 2025 17:00:51 GMT  
		Size: 27.8 KB (27779 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5c88f55fef728fd89659bc38ec611b43cc2e8447fa0457ba854002eb95c487b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297704572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afbe4dc5c94d3dbafa1e9b7a2af7d95cc5a394bf67c6dc5a2bc4ead57b30175`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9b8f871d0f3123ba15451c10996dab2d9e3570418f2ca8959fe0f2505e3356`  
		Last Modified: Tue, 25 Feb 2025 15:28:23 GMT  
		Size: 86.4 MB (86383529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18364ce0d2587c74fc30d8602f743c52178d9e6408c64d9091baffbff467af7`  
		Last Modified: Wed, 12 Feb 2025 09:53:13 GMT  
		Size: 75.1 MB (75060222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349146bc915ab644c1732fc873caaf444abef0ba611d35a0d9d3502f076b3094`  
		Last Modified: Tue, 25 Feb 2025 15:28:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d2d93b4a05d8a337d1f92a1aa40982cfc6849214c4cbaebf27afe3fb0dc272ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10337848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42106e07d540871db0673cd9a07f8b1f265fed3d4dbec49444d93c2e5daa2fce`

```dockerfile
```

-	Layers:
	-	`sha256:d539999b5642a98011b485e0674029935a853ed205ce6582782f3e5689bd377b`  
		Last Modified: Tue, 25 Feb 2025 15:28:21 GMT  
		Size: 10.3 MB (10310020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae84e5eb6c398dbaf7772b704f4e1d5b1692012b83a9a50ab17217c2ee00de33`  
		Last Modified: Tue, 25 Feb 2025 15:28:21 GMT  
		Size: 27.8 KB (27828 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:98839b84b95b4aa50e7bb488fdae07e456feef65073937c8684ead428782875c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307070186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab0319cc8a32c84aee713a6a30e6825da290f93d14d00e7dfd905b44d306db4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca163299b0e606d2916a03bd0f60c5903c6e5abeab65da3a8c490174697c929`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 24.9 MB (24899353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c3400be327e90dc9e848a16d4b0fcd191708de152e68c6b4888d83c61f441`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 66.2 MB (66237814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568ce875033c0aac30d14c8d8d41c6ee7b2e30b5f085ba8e11e45a272bc38d28`  
		Last Modified: Tue, 25 Feb 2025 04:17:28 GMT  
		Size: 89.7 MB (89744330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366fc1b7517b38e35749547747afd275840849b03e59ce7bdb829acdcf634998`  
		Last Modified: Wed, 12 Feb 2025 17:30:21 GMT  
		Size: 76.7 MB (76730079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a10af13c3c1ddf947bd7776220d62b2bf343f286493a5af8cdfe6b0f11ba547`  
		Last Modified: Tue, 25 Feb 2025 04:17:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c32ca9d2de24934421eeb593db8d6ba7bdc70fa65d24295af133c11efe04bf32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10289770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8584715a69283a727e1ffb70967c1d13f9b9783b9297ae7215c188fb27c251f9`

```dockerfile
```

-	Layers:
	-	`sha256:fbcbefb45315f51f44575025eb11972debad1cfcb261d69e39236ee8978885e7`  
		Last Modified: Tue, 25 Feb 2025 04:17:25 GMT  
		Size: 10.3 MB (10262180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1235f202b9543fdc11325a2e467c7c42190c13d9f445888d86d69fc0f39ac7f8`  
		Last Modified: Tue, 25 Feb 2025 04:17:24 GMT  
		Size: 27.6 KB (27590 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:a600f89fc3304113ef4975d972f5ad82d37e456d841ac867db2341839443e452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278393675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3470499d31709c5c87a77f6914bbca6a5e319c0547a32ec3ebdc79d7c069f6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54f151aa1b87c0945bf97dbd3c72581adb102deeee7a48dedc6ef51580d82ec8`  
		Last Modified: Tue, 25 Feb 2025 01:30:30 GMT  
		Size: 48.8 MB (48758989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93e2f55385d2f9849f5c49ddc6a441349700a7ac20dcafe37c022942621cef`  
		Last Modified: Tue, 25 Feb 2025 14:48:27 GMT  
		Size: 23.7 MB (23652239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406e93c581655a2c5138779556e6b049332bee85d015285d3106e767693cb64d`  
		Last Modified: Tue, 25 Feb 2025 22:26:26 GMT  
		Size: 63.3 MB (63306786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301664e1162c99caec998294841f4102a356459d19e18d2615cfe952fdad457`  
		Last Modified: Wed, 26 Feb 2025 02:31:50 GMT  
		Size: 69.9 MB (69904803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515f03cdc28580af1ed6f05f4fe0e8a389d42a92bcd6f0d3cc282625175488a9`  
		Last Modified: Wed, 12 Feb 2025 17:33:41 GMT  
		Size: 72.8 MB (72770700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076ea83da216661e2a183c9a299e7a96e94273697c832693f44d1832ecbb4ff8`  
		Last Modified: Wed, 26 Feb 2025 02:31:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b65687b6e0bfea11e7cb71c8a78dee6f7f43bc7b418f9bc9d37856823020a5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3a77a3379a3809faca4df334e4eab4c0e121163425a435c45db8cad7c1779f`

```dockerfile
```

-	Layers:
	-	`sha256:44a95e1cdf349aff2a2c9de226ac21f542040aed7c7ab862bd32ccd43e4e1287`  
		Last Modified: Wed, 26 Feb 2025 02:31:43 GMT  
		Size: 27.5 KB (27537 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:3547eaf6bf777ff203f0562087a89103bef56cd720ad547b46512490d3858055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313556915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4f4e94f2cb3dafa08d36fac0dc14d92ee5e633b8106102488acb0eb97a98d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50eddab3d8a04dda752c64b51fbaa29916204149752323327524cec69525c60b`  
		Last Modified: Tue, 25 Feb 2025 11:58:59 GMT  
		Size: 90.3 MB (90316651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b7c4c3ab33b16dd1aa80a96c66161c50757bc73ad50fd5e3235ed3f8700038`  
		Last Modified: Wed, 12 Feb 2025 17:44:43 GMT  
		Size: 75.4 MB (75371105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdffae5034f145c7ac995f0c932b120d009301f93d2845a8ed1e5328418480ae`  
		Last Modified: Tue, 25 Feb 2025 11:58:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b228e31b170975c540635d0c90b3a6baf89991023b100b4b5a57b592e7d098bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bd9150ea7261c2bfeafaa5bbe3a94592f2d43f0e0df0b481ff170ab0f9003a`

```dockerfile
```

-	Layers:
	-	`sha256:eff2c6706e5f4ac89427c508d72704bff5b6e19c0cdeb2ae9f23d1cf05dc46a5`  
		Last Modified: Tue, 25 Feb 2025 11:58:57 GMT  
		Size: 10.3 MB (10254844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f9e886de8c59403e3c72fc0ebced8626a777544f6632547a8d7575231d56298`  
		Last Modified: Tue, 25 Feb 2025 11:58:56 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:9d06c44e29d666801636a8680f1643fb12a5c5cbfb1b922680565026c2a88f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281208786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68eaa7838f146a5038cf01722508eb07c4705ed3326dfc40a6b84fdb7e278d8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16676c94eed4de3ccdb41bd857bcf5d665d34b49ee6681f62964150c8db326cc`  
		Last Modified: Tue, 25 Feb 2025 09:28:53 GMT  
		Size: 68.9 MB (68903037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5930b6893bd720b83184453384f2d98bb6ef640665d0b46f232b2c1eed78c3e4`  
		Last Modified: Wed, 12 Feb 2025 17:58:22 GMT  
		Size: 77.6 MB (77618898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429bbb940cc11f7b62459be5df36ba354570591ae422101c4eed254e96857374`  
		Last Modified: Tue, 25 Feb 2025 09:28:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:97b2f200c3fdbe57b9d095a2ca177df144d59bccec15ac29bdb2e174c1c5b9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10145751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b58873027cf4b8a948242e4e20f8997e57b8ce5252e55eba820da9037d56b`

```dockerfile
```

-	Layers:
	-	`sha256:6cb95831edaa86064d12d1280450a728fbb295aed837af68e70918c7d850759d`  
		Last Modified: Tue, 25 Feb 2025 09:28:51 GMT  
		Size: 10.1 MB (10118105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:585b6e41376da6af38818ec2108806203bab0ec5701cb3b51b49ff9d4811eaee`  
		Last Modified: Tue, 25 Feb 2025 09:28:51 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json
