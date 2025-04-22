## `golang:tip`

```console
$ docker pull golang@sha256:443a3e62a3cb60308b3d0b1ca75e79194855f9a3f2a94d45c63e23523dad156a
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:3b69f8a39d4f3aace5da154095b1211f365ae05a129d941fb720380ea97bfc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.1 MB (356087218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15db9612ce193309223499a6857f631307efe81efb6f03c95a939a10e90b9c39`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a87150fe323c4d552a95936008cb4da9e2c3c46964bf17bcf43069cd7c961b`  
		Last Modified: Mon, 21 Apr 2025 22:37:30 GMT  
		Size: 92.3 MB (92331638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25d4babeaf90344f4555f59166692dee6d066349b1a2f5cb41fc36591cc0aa6`  
		Last Modified: Mon, 21 Apr 2025 22:37:14 GMT  
		Size: 126.9 MB (126857323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cae019654f4659802a4dd05b7807fd6974c8bcb30eb0ba28b6e6ab0792f2e03`  
		Last Modified: Mon, 21 Apr 2025 22:37:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:dc49a1636d2ffda85b116706ca3e61a062bf2ea1f2adff1a3a7e4f0303b49b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10299530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115c4cc921eea7c7875555c018dab4f633aad87d93a3ecdc236a76fceb86a9e1`

```dockerfile
```

-	Layers:
	-	`sha256:b50935fc67143fc9ab6dafa16231278bfdf8407dffbb006be1f101fba8ed825c`  
		Last Modified: Mon, 21 Apr 2025 22:37:28 GMT  
		Size: 10.3 MB (10271868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e7f59c751b2394c2ca0a3817c4ce7a7dd95abf78b0a7bad47f44fccf01092a`  
		Last Modified: Mon, 21 Apr 2025 22:37:27 GMT  
		Size: 27.7 KB (27662 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:7cde7afe31451c13c0f1ffb8c87a9240e71944452d6b358b8b795bb9469630a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313851924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd55193c053cba52fb2afb38ddde6f7ff2fca510a2e25c1a6d6b4b5cb09ce834`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a9e8df2c13231c1e0a205f7e3ac9fa85454d09e0c0e5c18afbd185b211ea`  
		Last Modified: Tue, 08 Apr 2025 20:42:26 GMT  
		Size: 66.2 MB (66197481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5cc54485761ae69a05b08a84359a87e39a46bace5d6d721b8ddc84655c07c3`  
		Last Modified: Mon, 21 Apr 2025 23:32:56 GMT  
		Size: 121.9 MB (121899846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d724c8ac99659a96f26fc5702e1c65bfe417418930f20e193543c23e12c02e`  
		Last Modified: Mon, 21 Apr 2025 23:32:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:60884c630823b24859c1db2b0402851f42c76e64defcc6b2e9ce5cd7042d28b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10107977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc752ea2adefb51a8d74f31856e1315a713bd77ed51c695c1c1da611a53fcd5`

```dockerfile
```

-	Layers:
	-	`sha256:0a9a219639fb9bd4ebb466fce0b8948e68c1a711ec8244bab41ed92007349d74`  
		Last Modified: Mon, 21 Apr 2025 23:32:56 GMT  
		Size: 10.1 MB (10080190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a35480719937b98a7645090716444938bae5d58c29d4ed41ed2ddf8704de923`  
		Last Modified: Mon, 21 Apr 2025 23:32:52 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:24e93fff941a45901b8fd4f0d78a4a8bba4a0dfe5c311bb0ec7b057b796363ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342174218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f33dc4f8ae25589bfa3ca81236234be07037933d6ea913d8c1434f3900d299`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f72691c55039fb058e42d1e7433c859beeeeaa9e1b1856b791ba59bd1bc0586`  
		Last Modified: Mon, 14 Apr 2025 21:49:56 GMT  
		Size: 86.4 MB (86397123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49c3c4d9fc32722fbee95cae35a84bb5c2c18fa016fa934c1de17d28a4bfa33`  
		Last Modified: Mon, 21 Apr 2025 23:29:01 GMT  
		Size: 119.5 MB (119549349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ae4b8babb7a3a31a35cbc86d6f32cc1291fd8c6c0ad388f7648869862146e6`  
		Last Modified: Mon, 21 Apr 2025 23:28:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f0fc7a411ffb8151996b0d1e40f45fdf28d905967c451c7d34c488e30d3a6c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10327538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb510d76fe1500f927846d4bf3c829830d4fccd1eecee6a744657c0bf306555`

```dockerfile
```

-	Layers:
	-	`sha256:fc2e03167714a96c7b85bf13ecbc25850bb9f152269749911f6a358afe3685be`  
		Last Modified: Mon, 21 Apr 2025 23:28:58 GMT  
		Size: 10.3 MB (10299715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be8300462cac5f34bf3913808eb5ebb4033ad73a9dff674707c7c65d3b795fa`  
		Last Modified: Mon, 21 Apr 2025 23:28:57 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:ee2b83526ccb677546d7a74eff5ad82c05d87794b99679577b2318bd44634339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.4 MB (355362334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1ad3f73dedb24e46af74c5dfaf0c3be0af5012c961162adce02a6af85e2009`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5195a4ec2165012824dac296e59c02fe61d983135546fb6559239ebe1417585`  
		Last Modified: Mon, 21 Apr 2025 22:37:50 GMT  
		Size: 89.8 MB (89755941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22385500e9d61ec2b239f5d3bd81241409c720a3ebb2a4cf2d458346f64bcc50`  
		Last Modified: Mon, 21 Apr 2025 22:37:44 GMT  
		Size: 125.0 MB (125043477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0387e039ed811ce64fe064ac14f516ffd11d1f60cb819b8f8755af23f0de4d`  
		Last Modified: Mon, 21 Apr 2025 22:37:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:8d43b7d3a913e20a00f862e76307acbff612d7d8bff6ac4c8247892114ccc106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85260748d146e8fb1da35bc8619ac7c6d019859957eeff7b421118d20ca3987`

```dockerfile
```

-	Layers:
	-	`sha256:bb6e554631bf93e9fcf15d0b1e70ad7044bc221277a62724ca13cd433caad302`  
		Last Modified: Mon, 21 Apr 2025 22:37:48 GMT  
		Size: 10.3 MB (10251942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee095db69b8525cfea94ebc818993b277a39ae411c1e2ae93b1db82a1e7811f`  
		Last Modified: Mon, 21 Apr 2025 22:37:47 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:cfbfd9d326b44f65c92d593138097059884f452c9ac160aac3c277e3b35652ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322012665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef5f2bdb4f9e2c61a34fc2d84e5d92c67457935cc9e420a90786eccf0263fc3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f5e7682657f9515783d77fb7efbdd12ea81bbe4c750080727193e5396dfa344f`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 48.8 MB (48774861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca83e3505dc809d18860248927308a5c27c298583b9da5817d702111bdd65622`  
		Last Modified: Tue, 08 Apr 2025 16:31:05 GMT  
		Size: 23.6 MB (23595612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89ecdcc124054ab515f88e8a0bc5260e578fb23450a3ca215363db6cf689231`  
		Last Modified: Wed, 09 Apr 2025 00:38:14 GMT  
		Size: 63.3 MB (63308311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67fb97ca2e19f9a62b9988d33fd9b65b01ccb5cc564c412de1d8c73ed7b28fc`  
		Last Modified: Wed, 09 Apr 2025 08:20:47 GMT  
		Size: 69.9 MB (69916439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c2812d70b5e59d5754f1df87fc74a0a34ccc712a63b78eefe2f011c6124a92`  
		Last Modified: Mon, 14 Apr 2025 23:38:14 GMT  
		Size: 116.4 MB (116417283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdd0da5b4ee14fc37887e4cd57f7a66444abbfbced1bcfc65943dc6f1965b60`  
		Last Modified: Mon, 14 Apr 2025 23:38:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:4d636fb357318064dc08b53039cfd956dc7a1d5e9ea411b91b0bd4a32acc2ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef268210359f1fa797bc31c676dd1bea974acd38258d26aecfa7baa2d31ed07`

```dockerfile
```

-	Layers:
	-	`sha256:cf7139c6c7828d162ca45a756fa275fa592453607ddb683a901d92d0bb2ef624`  
		Last Modified: Mon, 14 Apr 2025 23:38:03 GMT  
		Size: 27.5 KB (27534 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:6af4767af7025e14402fc5860ff7ff3faae87941e9a0fe8365e29519f731ee66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359860686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfb37eac1127b88da8931c4a0421502bfa6cb0366a2190716b9bd6b9c153f47`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ab73478cfc6c2c81f66fffabb6adb3536b4880f0b0cb959b34167c62eb4cc2`  
		Last Modified: Mon, 14 Apr 2025 21:52:04 GMT  
		Size: 90.4 MB (90350288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb73d167b954c764acdc0a85e569cafdf41ff90d8b4ea6c273076608592e7a`  
		Last Modified: Mon, 21 Apr 2025 23:41:09 GMT  
		Size: 121.7 MB (121684495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6af01e1ed6b10dd61ad95c05ea87be415facb174864ea44bc8905c7d448ca1`  
		Last Modified: Mon, 21 Apr 2025 23:41:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:3fff71e6bdc704b3e5046683ba7901a9e278d6c7aa598fb49b7be8aa45c68a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10272282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc809ae7c4728945faeccf38f0b73ed13aea5a673e7569a940ab1bf0c26b563f`

```dockerfile
```

-	Layers:
	-	`sha256:e1567af55e1ed32512a049a2b5e014525757f6351c84230a9727c960b8058e48`  
		Last Modified: Mon, 21 Apr 2025 23:41:09 GMT  
		Size: 10.2 MB (10244561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513fa96eaca3ebe31cba89e34fedabaf3933a2d686fabed0ccdc3134f54384f2`  
		Last Modified: Mon, 21 Apr 2025 23:41:05 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:b047905de57bdbd43ac6ab84444abd47f55c8db5987d5c6363c2d3fae6cd72e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327716485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3913f9143beb0539187b95f88935637528b3965e03604966dc68771fdb06aee0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac9900eeeae74e6b991013801dd4b548da42e9a24a8a017f2f933bdd60bd62`  
		Last Modified: Mon, 14 Apr 2025 21:52:33 GMT  
		Size: 68.9 MB (68936844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221a3257b37adc23c0f99fc0f36d93743cedb18eca41076488eabc753a5b4701`  
		Last Modified: Mon, 21 Apr 2025 23:08:47 GMT  
		Size: 124.1 MB (124121776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5479fe2005aa242d0aa7782e0330a4299e8f83f7230916bcb39b3e6af21bfec`  
		Last Modified: Mon, 21 Apr 2025 23:08:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:c5d7d0964690e3987676897908fc1ffaef4eb4e90b3d44376618ddb043d3e01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10135509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2910a892c3316700bca5d8231b87c78d46529ff3a03d088bccf8c1f36a846216`

```dockerfile
```

-	Layers:
	-	`sha256:0ff9718f13614570e1029e760471816b8a8dd8dee4a42c634edae4f296fcada5`  
		Last Modified: Mon, 21 Apr 2025 23:08:44 GMT  
		Size: 10.1 MB (10107848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df3a8996c5f8d1e2cc016d71119403f37691ede95a9174a8e00d74135d2f0dea`  
		Last Modified: Mon, 21 Apr 2025 23:08:43 GMT  
		Size: 27.7 KB (27661 bytes)  
		MIME: application/vnd.in-toto+json
